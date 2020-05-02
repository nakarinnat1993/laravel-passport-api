<p align="center"><img src="https://res.cloudinary.com/dtfbvvkyp/image/upload/v1566331377/laravel-logolockup-cmyk-red.svg" width="400"></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/license.svg" alt="License"></a>
</p>

## Laravel API with passport
<p><a name="introduction"></a></p>
<h2 id="introduction">Introduction</h2>
<p>Laravel already makes it easy to perform authentication via traditional login forms, but what about APIs? APIs typically use tokens to authenticate users and do not maintain session state between requests. Laravel makes API authentication a breeze using Laravel Passport, which provides a full OAuth2 server implementation for your Laravel application in a matter of minutes. Passport is built on top of the <a href="https://github.com/thephpleague/oauth2-server">League OAuth2 server</a> that is maintained by Andy Millington and Simon Hamp.</p>
<blockquote>
<p>{note} This documentation assumes you are already familiar with OAuth2. If you do not know anything about OAuth2, consider familiarizing yourself with the general <a href="https://oauth2.thephpleague.com/terminology/">terminology</a> and features of OAuth2 before continuing.</p>
</blockquote>
<p><a name="upgrading"></a></p>
<h2 id="upgrading">Upgrading Passport</h2>
<p>When upgrading to a new major version of Passport, it's important that you carefully review <a href="https://github.com/laravel/passport/blob/master/UPGRADE.md">the upgrade guide</a>.</p>
<p><a name="installation"></a></p>
<h2 id="installation">Installation</h2>
<p>To get started, install Passport via the Composer package manager:</p>
<pre><code>composer require laravel/passport</code></pre>
<p>The Passport service provider registers its own database migration directory with the framework, so you should migrate your database after installing the package. The Passport migrations will create the tables your application needs to store clients and access tokens:</p>
<pre><code>php artisan migrate</code></pre>
<p>Next, you should run the <code>passport:install</code> command. This command will create the encryption keys needed to generate secure access tokens. In addition, the command will create &quot;personal access&quot; and &quot;password grant&quot; clients which will be used to generate access tokens:</p>
<pre><code>php artisan passport:install</code></pre>


