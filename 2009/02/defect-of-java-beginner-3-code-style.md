
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="zh-CN">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=gb18030" />
<meta name="generator" content="Python script by program.think@gmail.com" />
<meta name="provider" content="program-think.blogspot.com" />
<link type="text/css" rel="stylesheet" href="../../css/program-think.css" />
<title>Java���ֵ�ͨ��[3]��ȱ�����õı��ϰ�� - �������Ĳ���</title>
</head>
<body>
<div id="main" style="width:100%;">
<h1><a href="../../index.md" title="�ص���ҳ">Java���ֵ�ͨ��[3]��ȱ�����õı��ϰ��</a></h1>
<div class="post-info"><span class="date-header">2009-02-04</span><a href="../../tags/E7BC96E7A88B.md" class="tag">���</a> <a href="../../tags/E7BC96E7A88B.Java.md" class="tag">���.Java</a> </div>
<hr>
<div class="post">
�����ϴ����ˡ�<a href="../../2009/01/defect-of-java-beginner-2-oo.md">ȱ��������������</a>����������˵˵���ϰ�ߵ����⡣����˵����Щ��ϰ�ߴ󲿷ֶ��ǿ����Եģ�C++��Python����Ҳ�У������Ҵ󲿷ֶ���Ҫ��ƽʱ���ϵ�Ŭ�����������ĵ���<!--program-think--><br /><br />������<b>���������</b><a name="naming"> </a><br />������Щ����д���򣬵���Ҫ����ĳ����������Ҳ�����Ǻ������������������ȣ�ʱ�������һ�ü��̣����־������......�������ں�����ĳbug���������Լ�д�Ĵ���ʱ�����а����ֹ��������������д����զ���������󣿡�<br />���������ҳ��������Ĳ���˵���������淶�����˰������ڸ������൱�ձ飬�������˼��ֵ��͵���Ϊ����̲ģ��������£�ʹ�õ���ĸ����������ʹ��һЩû̫������ı�����������s1��s2��s3������ͬһ��ҵ�����ʹ�ò�ͬ������/��д�������ö���������񾭷��ѣ���ʹ��ƴ��������������Ŷ����и�̨��ʿ�������⣬�Ͳ��ˣ���<br /><br />������<b>ϰ���ڴ����copy &amp; paste</b><a name="copy_and_paste"> </a><br />��������һ�����ձ�����⡣�ܶ�����д�����ʱ���������Ҫд��ĳ��������ǰ����д��ĳ��������࣬�Ͱ�ԭ�����Ǹ�������������Ȼ����΢�ļ��£����л���ϲ�����ֿ��ٸ㶨��һ�����ܡ�......<br />����ͬѧ�������Ҳϲ����ô�ɣ���Ҫע���ˡ����������Ǵ����ζ�����á��ع� - ���Ƽ��д������ơ����ᷨ������Ҫ��Դ�����´����ά���Դ���½������㽫����Ҫ���ӹ��ܻ��޸�bug��ʱ��Ҫͬʱ�Ķ�����ط�������ʱ������Ѿ��벻�������ȴ����м�����¡�ˡ�<br /><br />������<b>Magic Number�����</b><a name="magic_number"> </a><br />���������û����˵����Magic Number�����ȿ���<a href="http://en.wikipedia.org/wiki/Magic_number_(programming)#Unnamed_numerical_constant" target="_blank" rel="nofollow">����</a>���˽�һ�¡�<br />����Ϊ��˵��Magic Number�����⣬���Ҹ�������˵�¶��������и�ҵ���߼�����Ҫ����10��ĳ�ʱ�ȴ��������ôд���sleep��䣿�ҹ��ƴ󲿷��˲������������д����<br />����1��ֱ��д��sleep(10*1000);����<br />����2������һ������TIMEOUT_XXX = 10*1000;Ȼ��sleep(TIMEOUT_XXX);<br />����3���������ļ��м���һ����ʱ�Ȼ������ȡ�����ļ���ó�ʱֵ��Ȼ�����sleep�����˴��ᵽ��<b>�����ļ�</b>�ǹ���ģ���ָ���ֿ����ڴ洢������Ϣ�Ļ��ƣ���xml�ļ������ݿ�ȣ�<br />��������������������д��1������ϲ������Ӳ���롣Ӳ���벻��ȱ���ɶ��ԣ����Ҿ��к͡����뿽��ճ�������ƵĴ����ζ�����ܻ���ڶ��Magic Number��¡�����������պ�ά����<br />��������д��2����д��1�Ժã����ٿɶ��Ժ��ˣ������ǣ�����һ��������������Ҫ����<b>����ʱ</b>������ʱ���������Ҫ�����û������Ƴ�ʱ���������д��2��ȱ��������¶���š�<br /><br />������<b>������϶�̫��</b><a name="coupling"> </a><br />����ÿ��˵��MVC�������ģʽ������ÿ��Java������Ա����˵��ͷͷ�ǵ�������˵��˵������д�����ʱ��������д���Ĵ����ǲ������ġ�����˵��������Ϸֱ�����Щ�������ʲô����������ƣ������������������ƣ��Һ����ר������һ�£�����ȫ�����׵��˾͸����ˡ�<br />�������Ժܶ�Java���ֵĴ�����϶ȴ�Ҳ�Ͳ���Ϊ���ˡ�����������������Ա���Ĵ��룬����ҵ���߼�������һ�𣬴����ζ��ҪѬ���ˡ����ع����޴����֣�ֻ�������Ƶ���д��<br /><br />������<b>��GC�軵</b><a name="gc"> </a><br />��������Java�����Բ����ṩ���ڴ���������ջ��ƣ�����Աֻ�������ڴ棬����Ҫ�ٹ����ͷŵ����⡣��˺ܶ����������˻�ϰ�ߣ�����������Դ���������ݿ����ӣ�Ҳֻ���벻�ͷţ���Щ�������������ΪJVM�����㶨��Դ���գ���<br />��������Щ����Ȼ֪����Դ��Ҫ�ͷţ����ǳ������ǣ�����д�˴����ݿ����Ӻ���ش��룬<b>����</b>д�ر����ݿ�����ʱ��ͻȻ���˽���ȥ���з���������Ͱ��������ˣ���<br />���������ϰ�߻ᵼ����Դ��й¶������Դй¶�������ڴ�й¶��Ҫ���������д�ĳ����ǳ�ʱ�����еģ�����������WebServer�ϣ���ʱ�䳤�˻�������Դ�ľ��������������̳����⡣<br /><br />������һ�����ӣ���һ�¡�<a href="../../2009/02/defect-of-java-beginner-4-exception.md">�쳣����ʹ�ò���</a>����<div class="blogger-post-footer">
</div>
<hr>
<div class="copyright">
<h4>��Ȩ����</h4>
���������е�ԭ�����£����߽Ա�����Ȩ��ת�ر�����������������ֱ������������Գ�������ʽע������<a href="mailto:program.think@gmail.com">�������</a>�ͱ���ԭʼ��ַ��<br>
<a href="/2009/02/defect-of-java-beginner-3-code-style.md">2009/02/defect-of-java-beginner-3-code-style.md</a>
</div>
</div>
</body>
</html>