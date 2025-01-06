// ==UserScript==
// @name         "app.kuaijing" free
// @namespace    http://tampermonkey.net/
// @version      2025-01-02
// @description  "app.kuaijing" free. Automatically remove elements with class "ant-modal-root"
// @author       You
// @match        *://app.kuaijingai.com/*
// @grant        none
// @license      Sufjan
// ==/UserScript==
 
(function() {
    'use strict';
    console.log("\"app.kuaijing\" free");
 
    // 等待页面完全加载
    window.addEventListener('load', () => {
        console.log("Page loaded.");
 
        // 定义一个函数，用于删除 class="ant-modal-root" 的整个元素
        function removeAntModalRootElements() {
            const elements = document.querySelectorAll('.ant-modal-root');
            elements.forEach(element => {
                element.remove();
            });
            console.log(`Removed ${elements.length} ant-modal-root element(s).`);
        }
 
        // 初始调用，删除页面中已有的 ant-modal-root 元素
        removeAntModalRootElements();
 
        // 监听 DOM 变化，实时删除新添加的 ant-modal-root 元素
        const observer = new MutationObserver(() => {
            removeAntModalRootElements();
        });
 
        // 配置 MutationObserver，监听整个文档的子树变化
        observer.observe(document.body, {
            childList: true,
            subtree: true
        });
        console.log("MutationObserver initialized.");
    });
})();
