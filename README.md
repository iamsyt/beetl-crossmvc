beetl-crossmvc
==============


Beetl-Cross ���Խ��MVC�� m��VC�ķ��룬���������ø����jsǰ����Ա�������ѵĲ�����ģ��Ŀ�����Ҳ������ȫջ������Ա�ȼ��о�������V�㼼��
Beetl-Cross  ����Beetlģ������������js�﷨�����ܶ���֧��V����������һ����׼�Ĺ淶�����̣�ʹ�ú��ģ���ܽ�Ϊ�����ı����ǰ�˿�����ԱЭ�������Ͳ��ԣ����޷�ļ��ɵ����MVC�����

~~~~~xml

�磺ǰ����Ա����һ����¼���棬��Ҫ���һ���򵥵�controller����

�����ļ���ǰ����Ա����д�ö���ǰ��һ��Service���󣬽�����ʲô���ĺ������
<domain base="/ctr" />
        <controller requestURL="/login"  responseURL="/index.html" responseValue="/login.value">
	<controller requestURL="/user?name=${1}&"  responseURL="user${1}" responseValue="/cccc_value.html">
		<request name="" value="">
		<response tt="" value="">
		<template name="/commont.value">
        </controller>
</domain>

~~~~~


~~~~~javascript
//login.value

var user ={name:'joeli',age:12,lastLogin:date()};
var logHistor = []
var cookies = {}

~~~~~

������ǰ����Ա�Ϳ��Կ���index.html,��ʹ�� long.value ����ı�������:


~~~~~html

<div > ��ӭ ${user.name},�ϴε�½ʱ�� ${user.lastLogin,'yy-MM-dd'} </div>


~~~~~

ǰ�˿�����Ա��Ҫ ���� Beetl-Cross ģ���Ŀ¼���ɣ�������һ��webserver������ȡdomain.xml �ļ���ģ��MVC�е�C��M��ǰ����Ա��������п��԰������ý��в��ԺͿ���ģ��

������ͨ��һ�����͵�Ŀ¼�ṹ

[ROOT]
   [resource]
         [images]  
   [pages]
         login.html
         index.html
   [value]
         long.value
   domain.xml