# AndroidStudyNote
Android学习笔记

Android问题解决方案
1、Android WebView加载网页不显示图片解决办法
摘要：问题描述:WebView加载网页,图片显示不了环境:1、网页地址是https地址,图片地址是http地址2、Android5.0.0解决方案webView.getSettings().setJavaScriptEnabled(true);//启用jswebView.getSettings().setBlockNetworkImage(false);//解决图片不显示if(Build.VERSION.SDK_INT>=Build.VERSION_CODES.LOLLIPO

问题描述: 
WebView加载网页,图片显示不了


环境: 
1、网页地址是https地址,图片地址是http地址
2、Android 5.0.0


解决方案 
webView.getSettings().setJavaScriptEnabled(true); // 启用js 
webView.getSettings().setBlockNetworkImage(false); // 解决图片不显示 
if(Build.VERSION.SDK_INT >= Build.VERSION_CODES.LOLLIPOP { 
webView.getSettings().setMixedContentMode(WebSettings.MIXED_CONTENT_ALWAYS_ALLOW); 
} 
