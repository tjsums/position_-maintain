# position_-maintain

<!DOCTYPE html>
<html lang="zh-cn" ng-app="myApp" ng-controller="PublicController" ng-click="win_click($event)">
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8"/>
<head>
    <meta http-equiv="X-UA-Compatible" content="chrome=1">
    <base href="/">
    <meta charset="utf-8">
    <meta http-equiv="Expires" content="0">
    <meta http-equiv="Pragma" content="no-cache">
    <meta http-equiv="Cache-control" content="no-cache">
    <meta http-equiv="Cache" content="no-cache">
    <meta name="viewport"
          content="width=device-width, initial-scale=1.0, user-scalable=0, minimum-scale=1.0, maximum-scale=1.0">
    <title><%= params.special_title?params.special_title:"HCM Cloud"%></title>
    <meta name="keywords" content="HCM,Cloud,HR,人力资源,云,云服务">
    <meta name="description" content="HCM Cloud,超出你想像的人力资源服务空间">
    <link rel="shortcut icon" href="/img?index=<%= params.company_logo%>"/>
    <link rel="bookmark" href="<%= params.cdn_host %>/static/resources/images/hcmcloud.ico"/>

    <%- include('lib/css', {libs: params.css_libs,cdn:params.cdn_host,theme:params.cc_highlight}); %>
    <link rel="stylesheet" href="/api/auth/get_customer_css">
</head>
<body>

<ui-view class="h-c-main-frame"></ui-view>
<carousel-panel></carousel-panel>
<div class="waiting-box" ng-show="is_waitting_show" ng-cloak>
    <div class="waiting"></div>
</div>
<script type="text/javascript" src="<%= params.cdn_host %>/static/resources/lib/jquery.min.js"></script>
<script type="text/javascript"
        src="<%= params.cdn_host %>/static/resources/lib/jquery.nicescroll.min.js"></script>
<script type="text/javascript"
        src="<%= params.cdn_host %>/static/resources/lib/jquery.orgchart.js"></script>

<%- include('lib/init_js', params); %>
<%- include('lib/js', {libs: params.js_libs,cdn:params.cdn_host}); %>

<% if (params.server_disable_map!='true') { %>
<script type="text/javascript" src="https://api.map.baidu.com/api?v=2.0&ak=D7KG4CoeclWrYbUGU7dMCGfS9Uhn0YFz"></script>
<script charset="utf-8" src="https://map.qq.com/api/js?v=2.exp&libraries=convertor"></script>
<%}%>

</body>
</html>
