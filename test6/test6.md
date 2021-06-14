<h1><a name="_Toc74614346"></a>医患管理系统</h1>
<p>目录</p>
<p><a href="#_Toc74614346">医患管理系统... 2</a></p>
<p><a href="#_Toc74614347">引言... 3</a></p>
<p><a href="#_Toc74614348">1 表设计... 3</a></p>
<p><a href="#_Toc74614349"> &nbsp;&nbsp;&nbsp;&nbsp; 1.1 病患信息表... 3</a></p>
<p><a href="#_Toc74614350"> &nbsp;&nbsp;&nbsp;&nbsp; 1.2 医生信息表... 3</a></p>
<p><a href="#_Toc74614351"> &nbsp;&nbsp;&nbsp;&nbsp; 1.3 类别信息表... 4</a></p>
<p><a href="#_Toc74614352"> &nbsp;&nbsp;&nbsp;&nbsp; 1.4 科室信息表... 4</a></p>
<p><a href="#_Toc74614353"> &nbsp;&nbsp;&nbsp;&nbsp; 1.5 项目信息表... 4</a></p>
<p><a href="#_Toc74614354"> &nbsp;&nbsp;&nbsp;&nbsp; 1.6 诊断结果信息表... 4</a></p>
<p><a href="#_Toc74614355"> &nbsp;&nbsp;&nbsp;&nbsp; 1.7 用户信息表... 5</a></p>
<p><a href="#_Toc74614356"> &nbsp;&nbsp;&nbsp;&nbsp; 1.8 用户类别信息表... 5</a></p>
<p><a href="#_Toc74614357">2 创建表空间... 5</a></p>
<p><a href="#_Toc74614358"> &nbsp;&nbsp;&nbsp;&nbsp; 2.1 永久表空间的创建... 5</a></p>
<p><a href="#_Toc74614359"> &nbsp;&nbsp;&nbsp;&nbsp; 2.2 临时表空间的创建... 5</a></p>
<p><a href="#_Toc74614360"> &nbsp;&nbsp;&nbsp;&nbsp; 2.3 撤销表空间的创建... 6</a></p>
<p><a href="#_Toc74614361">3 修改表空间... 6</a></p>
<p><a href="#_Toc74614362">&nbsp;&nbsp;&nbsp;&nbsp;  3.1 通过数据字典查看表空间... 6</a></p>
<p><a href="#_Toc74614363"> &nbsp;&nbsp;&nbsp;&nbsp; 3.2 修改表空间对应的数据文件的大小... 6</a></p>
<p><a href="#_Toc74614364"> &nbsp;&nbsp;&nbsp;&nbsp; 3.3 为表空间添加一个新的数据文件... 6</a></p>
<p><a href="#_Toc74614365"> &nbsp;&nbsp;&nbsp;&nbsp; 3.4 删除新建的数据文件... 7</a></p>
<p><a href="#_Toc74614366">4 表的相关操作... 7</a></p>
<p><a href="#_Toc74614367"> &nbsp;&nbsp;&nbsp;&nbsp; 4.1 表的创建... 7</a></p>
<p><a href="#_Toc74614368"> &nbsp;&nbsp;&nbsp;&nbsp; 4.2 索引... 9</a></p>
<p><a href="#_Toc74614369"> &nbsp;&nbsp;&nbsp;&nbsp; 4.3 视图... 10</a></p>
<p><a href="#_Toc74614370"> &nbsp;&nbsp;&nbsp;&nbsp; 4.4 使用序列... 10</a></p>
<p><a href="#_Toc74614371">5 查询... 12</a></p>
<p><a href="#_Toc74614372"> &nbsp;&nbsp;&nbsp;&nbsp; 5.1 SQL语言基础... 12</a></p>
<p><a href="#_Toc74614373"> &nbsp;&nbsp;&nbsp;&nbsp; 5.2 子查询与高级查询... 12</a></p>
<p><a href="#_Toc74614374">6 SQL语句... 13</a></p>
<p><a href="#_Toc74614375"> &nbsp;&nbsp;&nbsp;&nbsp; 6.1 显示表中的编号为1的类别名... 13</a></p>
<p><a href="#_Toc74614376"> &nbsp;&nbsp;&nbsp;&nbsp; 6.2 判断诊断结果61分所处的等级... 14</a></p>
<p><a href="#_Toc74614377"> &nbsp;&nbsp;&nbsp;&nbsp; 6.3 判断患者的诊断结果是否健康... 14</a></p>
<p><a href="#_Toc74614378">7 创建存储过程... 15</a></p>
<p><a href="#_Toc74614379"> &nbsp;&nbsp;&nbsp;&nbsp;  7.1 创建一个存储过程update_patient 15</a></p>
<p><a href="#_Toc74614380"> &nbsp;&nbsp;&nbsp;&nbsp; 7.2 创建一个存储过程get_Result_information. 15</a></p>
<p><a href="#_Toc74614381">8 函数设计... 16</a></p>
<p><a href="#_Toc74614382"> &nbsp;&nbsp;&nbsp;&nbsp; 8.1 创建一个函数get_Pname. 16</a></p>
<p><a href="#_Toc74614383"> &nbsp;&nbsp;&nbsp;&nbsp; 8.2 创建一个函数re_pat_info. 17</a></p>
<p><a href="#_Toc74614384">9 备份方案... 18</a></p>
<p><a href="#_Toc74614385"> &nbsp;&nbsp;&nbsp;&nbsp; 9.1 RMAN（备份与恢复管理器）... 18</a></p>
<p>&nbsp;</p>
<h2><a name="_Toc74614347"></a>引言</h2>
<p>&nbsp;&nbsp;&nbsp; 医患管理系统是一个医院必不可少的一部分，随着互联网的普及和计算机的普遍使用，医患管理系统，有了更大的发展空间，通过对医患管理系统的开发可以提高医务人员以及患者就诊的工作效率，因此开发设计这样一套医患管理系统软件是很必要的事情。</p>
<p>&nbsp; &nbsp;&nbsp;医患管理系统是一个医院不可缺少的部分，一个良好的医患管理系统，可以方便用户进行预约挂号，病例查询等等的操作，医生在系统上对病人发布他的就诊诊断信息，对医生查看患者的过往病逝以及诊断病人的病情有十分重要的作用。由于各个医院在这方面都有需求，所以如何管理，这些庞大的数据就变得更加的复杂，传统的医患管理系统，不仅工作量大，而且很容易出现问题，有效率低，保密性差的缺点。</p>
<p>&nbsp;&nbsp;&nbsp; 但是目前我们通过技术手段可以很好的解决这些问题，借助sql来对医生和患者的数据今进行管理，使医院的管理更上一层楼，方便大众，服务大众。</p>
<h2><a name="_Toc74614348"></a>1 表设计</h2>
<h3><a name="_Toc74614349"></a>1.1 病患信息表</h3>
<p>表1.1&nbsp; 病患信息表(Patient)</p>
<table width="557">
<tbody>
<tr>
<td width="114">
<p><strong>字段名</strong></p>
</td>
<td width="118">
<p><strong>数据类型</strong></p>
</td>
<td width="103">
<p><strong>长度</strong></p>
</td>
<td width="103">
<p><strong>是否为空</strong></p>
</td>
<td width="118">
<p><strong>名称</strong></p>
</td>
</tr>
<tr>
<td width="114">
<p>Pno</p>
</td>
<td width="118">
<p>NUMBER</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>病号</p>
</td>
</tr>
<tr>
<td width="114">
<p>Pname</p>
</td>
<td width="118">
<p>VARCHAR2</p>
</td>
<td width="103">
<p>4</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>病患姓名</p>
</td>
</tr>
<tr>
<td width="114">
<p>Sex</p>
</td>
<td width="118">
<p>CHAR</p>
</td>
<td width="103">
<p>2</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>性别</p>
</td>
</tr>
<tr>
<td width="114">
<p>Cateid</p>
</td>
<td width="118">
<p>NUMBER</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>类别号</p>
</td>
</tr>
<tr>
<td width="114">
<p>Departid</p>
</td>
<td width="118">
<p>NUMBER</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>科室号</p>
</td>
</tr>
</tbody>
</table>
<h3><a name="_Toc74614350"></a>1.2 医生信息表</h3>
<p>表1.2&nbsp; 医生信息表(Doctor)</p>
<table width="557">
<tbody>
<tr>
<td width="114">
<p><strong>字段名</strong></p>
</td>
<td width="118">
<p><strong>数据类型</strong></p>
</td>
<td width="103">
<p><strong>长度</strong></p>
</td>
<td width="103">
<p><strong>是否为空</strong></p>
</td>
<td width="118">
<p><strong>名称</strong></p>
</td>
</tr>
<tr>
<td width="114">
<p>Dno</p>
</td>
<td width="118">
<p>NUMBER</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>医生编号</p>
</td>
</tr>
<tr>
<td width="114">
<p>Dname</p>
</td>
<td width="118">
<p>VARCHAR2</p>
</td>
<td width="103">
<p>4</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>医生姓名</p>
</td>
</tr>
<tr>
<td width="114">
<p>Sex</p>
</td>
<td width="118">
<p>CHAR</p>
</td>
<td width="103">
<p>2</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>性别</p>
</td>
</tr>
<tr>
<td width="114">
<p>Departid</p>
</td>
<td width="118">
<p>NUMBER</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>科室号</p>
</td>
</tr>
</tbody>
</table>
<h3><a name="_Toc74614351"></a>1.3 类别信息表</h3>
<p>表1.3&nbsp; 类别信息表(Cate)</p>
<table width="660">
<tbody>
<tr>
<td width="114">
<p><strong>字段名</strong></p>
</td>
<td width="118">
<p><strong>数据类型</strong></p>
</td>
<td width="103">
<p><strong>&nbsp;</strong></p>
</td>
<td width="103">
<p><strong>长度</strong></p>
</td>
<td width="103">
<p><strong>是否为空</strong></p>
</td>
<td width="118">
<p><strong>名称</strong></p>
</td>
</tr>
<tr>
<td width="114">
<p>Cateid</p>
</td>
<td width="118">
<p>NUMBER</p>
</td>
<td width="103">
<p>&nbsp;</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>科室号</p>
</td>
</tr>
<tr>
<td width="114">
<p>DepPname</p>
</td>
<td width="118">
<p>VARCHAR2</p>
</td>
<td width="103">
<p>&nbsp;</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>科室名</p>
</td>
</tr>
<tr>
<td width="114">
<p>Departid</p>
</td>
<td width="118">
<p>NUMBER</p>
</td>
<td width="103">
<p>&nbsp;</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>所在科室</p>
</td>
</tr>
</tbody>
</table>
<h3><a name="_Toc74614352"></a>1.4 科室信息表</h3>
<p>表1.4&nbsp; 科室信息表(Depart)</p>
<table width="557">
<tbody>
<tr>
<td width="114">
<p><strong>字段名</strong></p>
</td>
<td width="118">
<p><strong>数据类型</strong></p>
</td>
<td width="103">
<p><strong>长度</strong></p>
</td>
<td width="103">
<p><strong>是否为空</strong></p>
</td>
<td width="118">
<p><strong>名称</strong></p>
</td>
</tr>
<tr>
<td width="114">
<p>Departid</p>
</td>
<td width="118">
<p>NUMBER</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>科室号</p>
</td>
</tr>
<tr>
<td width="114">
<p>DeparDname</p>
</td>
<td width="118">
<p>VARCHAR2</p>
</td>
<td width="103">
<p>20</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>科室名</p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<h3><a name="_Toc74614353"></a>1.5 项目信息表</h3>
<p>表1.5&nbsp; 项目信息表(Project)</p>
<table width="557">
<tbody>
<tr>
<td width="114">
<p><strong>字段名</strong></p>
</td>
<td width="118">
<p><strong>数据类型</strong></p>
</td>
<td width="103">
<p><strong>长度</strong></p>
</td>
<td width="103">
<p><strong>是否为空</strong></p>
</td>
<td width="118">
<p><strong>名称</strong></p>
</td>
</tr>
<tr>
<td width="114">
<p>Cno</p>
</td>
<td width="118">
<p>NUMBER</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>项目编号</p>
</td>
</tr>
<tr>
<td width="114">
<p>Cname</p>
</td>
<td width="118">
<p>VARCHAR2</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>项目名称</p>
</td>
</tr>
<tr>
<td width="114">
<p>Credit</p>
</td>
<td width="118">
<p>NUMBER</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>指标</p>
</td>
</tr>
</tbody>
</table>
<h3><a name="_Toc74614354"></a>1.6 诊断结果信息表</h3>
<p>表1.6&nbsp; 诊断结果信息表(Result)</p>
<table width="557">
<tbody>
<tr>
<td width="114">
<p><strong>字段名</strong></p>
</td>
<td width="118">
<p><strong>数据类型</strong></p>
</td>
<td width="103">
<p><strong>长度</strong></p>
</td>
<td width="103">
<p><strong>是否为空</strong></p>
</td>
<td width="118">
<p><strong>名称</strong></p>
</td>
</tr>
<tr>
<td width="114">
<p>Pno</p>
</td>
<td width="118">
<p>NUMBER</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>病号</p>
</td>
</tr>
<tr>
<td width="114">
<p>Pname</p>
</td>
<td width="118">
<p>VARCHAR2</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>病患姓名</p>
</td>
</tr>
<tr>
<td width="114">
<p>Cno</p>
</td>
<td width="118">
<p>NUMBER</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>项目编号</p>
</td>
</tr>
<tr>
<td width="114">
<p>Cname</p>
</td>
<td width="118">
<p>VARCHAR2</p>
</td>
<td width="103">
<p>20</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>项目名称</p>
</td>
</tr>
<tr>
<td width="114">
<p>Result</p>
</td>
<td width="118">
<p>NUMBER</p>
</td>
<td width="103">
<p>3</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>诊断结果</p>
</td>
</tr>
<tr>
<td width="114">
<p>Credit</p>
</td>
<td width="118">
<p>NUMBER</p>
</td>
<td width="103">
<p>3</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>指标</p>
</td>
</tr>
</tbody>
</table>
<h3><a name="_Toc74614355"></a>1.7 用户信息表</h3>
<p>表1.7&nbsp; 用户信息表(Users)</p>
<table width="557">
<tbody>
<tr>
<td width="114">
<p><strong>字段名</strong></p>
</td>
<td width="118">
<p><strong>数据类型</strong></p>
</td>
<td width="103">
<p><strong>长度</strong></p>
</td>
<td width="103">
<p><strong>是否为空</strong></p>
</td>
<td width="118">
<p><strong>名称</strong></p>
</td>
</tr>
<tr>
<td width="114">
<p>Userid</p>
</td>
<td width="118">
<p>VARCHAR2</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>登陆账号</p>
</td>
</tr>
<tr>
<td width="114">
<p>Uname</p>
</td>
<td width="118">
<p>VARCHAR2</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>用户名</p>
</td>
</tr>
<tr>
<td width="114">
<p>Pwd</p>
</td>
<td width="118">
<p>VARCHAR2</p>
</td>
<td width="103">
<p>20</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>密码</p>
</td>
</tr>
<tr>
<td width="114">
<p>Typeid</p>
</td>
<td width="118">
<p>NUMBER</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>用户类别</p>
</td>
</tr>
</tbody>
</table>
<h3><a name="_Toc74614356"></a>1.8 用户类别信息表</h3>
<p>表1.8&nbsp; 用户类别信息表(Type)</p>
<table width="557">
<tbody>
<tr>
<td width="114">
<p><strong>字段名</strong></p>
</td>
<td width="118">
<p><strong>数据类型</strong></p>
</td>
<td width="103">
<p><strong>长度</strong></p>
</td>
<td width="103">
<p><strong>是否为空</strong></p>
</td>
<td width="118">
<p><strong>名称</strong></p>
</td>
</tr>
<tr>
<td width="114">
<p>Typeid</p>
</td>
<td width="118">
<p>NUMBER</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>类别编号</p>
</td>
</tr>
<tr>
<td width="114">
<p>Typename</p>
</td>
<td width="118">
<p>VARCHAR2</p>
</td>
<td width="103">
<p>10</p>
</td>
<td width="103">
<p>否</p>
</td>
<td width="118">
<p>类别名称</p>
</td>
</tr>
</tbody>
</table>
<h2><a name="_Toc74614357"></a>2 创建表空间</h2>
<h3><a name="_Toc74614358"></a>2.1 永久表空间的创建</h3>
<p>SQL&gt; create tablespace hosspace</p>
<p>&nbsp; 2&nbsp; datafile 'D:\homework\oraclehomework\BoBo\hosspace.dbf'</p>
<p>&nbsp; 3&nbsp; size 50m</p>
<p>&nbsp; 4&nbsp; autoextend on</p>
<p>&nbsp; 5&nbsp; next 5m</p>
<p>&nbsp; 6&nbsp; maxsize 100m;</p>
<h3><a name="_Toc74614359"></a>2.2 临时表空间的创建</h3>
<p>SQL&gt; create temporary tablespace patienttemp</p>
<p>&nbsp; 2&nbsp; tempfile 'D:\homework\oraclehomework\BoBo\patienttemp.dbf'</p>
<p>&nbsp; 3&nbsp; size 10m</p>
<p>&nbsp; 4&nbsp; autoextend on</p>
<p>&nbsp; 5&nbsp; next 2m</p>
<p>&nbsp; 6&nbsp; maxsize 20m;</p>
<h3><a name="_Toc74614360"></a>2.3 撤销表空间的创建</h3>
<p>SQL&gt; create undo tablespace hosundo</p>
<p>&nbsp; 2&nbsp; datafile 'D:\homework\oraclehomework\BoBo\hosundo.dbf'</p>
<p>&nbsp; 3&nbsp; size 50m</p>
<p>&nbsp; 4&nbsp; autoextend on</p>
<p>&nbsp; 5&nbsp; next 5m</p>
<p>&nbsp; 6&nbsp; maxsize 100m;</p>
<h2><a name="_Toc74614361"></a>3 修改表空间</h2>
<h3><a name="_Toc74614362"></a>3.1 通过数据字典查看表空间</h3>
<p>SQL&gt; select tablespace_name,file_name,bytes</p>
<p>&nbsp; 2&nbsp; from dba_data_files</p>
<p>&nbsp; &nbsp;3&nbsp; where tablespace_name='HOSSPACE';</p>
<p>&nbsp;</p>
<p>TABLESPACE_NAME</p>
<p>------------------------------</p>
<p>FILE_NAME</p>
<p>--------------------------------------------------</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp; BYTES</p>
<p>----------</p>
<p>HOSSPACE</p>
<p>D:\homework\oraclehomework\BoBo\HOSSPACE.DBF</p>
<p>&nbsp; 52428800</p>
<h3><a name="_Toc74614363"></a>3.2 修改表空间对应的数据文件的大小</h3>
<p>SQL&gt; alter database</p>
<p>&nbsp; 2&nbsp; datafile 'D:\homework\oraclehomework\BoBo\HOSSPACE.DBF'</p>
<p>&nbsp; 3&nbsp; resize 40m;</p>
<h3><a name="_Toc74614364"></a>3.3 为表空间添加一个新的数据文件</h3>
<p>SQL&gt; alter tablespace hosspace</p>
<p>&nbsp; 2&nbsp; add datafile</p>
<p>&nbsp; 3&nbsp; 'D:\homework\oraclehomework\BoBo\HOSSPACE1.DBF'</p>
<p>&nbsp; 4&nbsp; size 10m</p>
<p>&nbsp; 5&nbsp; autoextend on next 5m maxsize 40m;</p>
<h3><a name="_Toc74614365"></a>3.4 删除新建的数据文件</h3>
<p>SQL&gt; alter tablespace hosspace</p>
<p>&nbsp; 2&nbsp; drop datafile 'D:\homework\oraclehomework\BoBo\HOSSPACE1.DBF';</p>
<h2><a name="_Toc74614366"></a>4 表的相关操作</h2>
<h3><a name="_Toc74614367"></a>4.1 表的创建</h3>
<h4>4.1.1 创建用户类别表</h4>
<p>SQL&gt; create table user_type(</p>
<p>&nbsp; 2&nbsp; typeid number(10) primary key,</p>
<p>&nbsp; 3&nbsp; typename varchar2(10) not null</p>
<p>&nbsp; 4&nbsp; )tablespace patientspace;</p>
<p>表已创建。</p>
<h4>4.1.2 创建用户信息表</h4>
<p>SQL&gt; create table users(</p>
<p>&nbsp; 2&nbsp; userid varchar2(10) primary key,</p>
<p>&nbsp; 3&nbsp; uname varchar2(10) not null,</p>
<p>&nbsp; 4&nbsp; pwd varchar2(20) not null,</p>
<p>&nbsp; 5&nbsp; typeid number(10) not null,</p>
<p>&nbsp; 6&nbsp; constraint users_type foreign key (typeid)</p>
<p>&nbsp; 7&nbsp; references type(typeid)</p>
<p>&nbsp; 8&nbsp; )tablespace patientspace;</p>
<p>表已创建。</p>
<h4>4.1.3 创建科室信息表</h4>
<p>SQL&gt; create table Depart(</p>
<p>2&nbsp; Departid number(10) primary key,</p>
<p>3&nbsp; DeparDname varchar(20) not null)</p>
<p>4&nbsp; tablespace patientspace;</p>
<p>表已创建。</p>
<h4>4.1.4 创建类别信息表</h4>
<p>SQL&gt; create table Cate(</p>
<p>2&nbsp; Cateid number(10) primary key,</p>
<p>3&nbsp; DepPname varchar2(10) not null,</p>
<p>&nbsp; 4&nbsp; Departid number(10) not null,</p>
<p>&nbsp; 5&nbsp; constraint Cate_Depart foreign key(Departid)</p>
<p>&nbsp; 6&nbsp; references Depart(Departid)</p>
<p>&nbsp; 7&nbsp; ) tablespace patientspace;</p>
<p>表已创建。</p>
<h4>4.1.5 创建病患信息表</h4>
<p>SQL&gt; create table patient(</p>
<p>&nbsp; 2&nbsp; Pno number(10) primary key,</p>
<p>&nbsp; 3&nbsp; Pname varchar2(4) not null,&nbsp;&nbsp;&nbsp;</p>
<p>&nbsp; 4&nbsp; sex char(2) not null</p>
<p>&nbsp; 5&nbsp; check (sex in('男','女')),</p>
<p>&nbsp; 6&nbsp; Cateid number(10) not null,</p>
<p>&nbsp; 7&nbsp; Departid number(10) not null,</p>
<p>&nbsp; 8&nbsp; constraint patient_Cate foreign key(Cateid)</p>
<p>&nbsp; 9&nbsp; references Cate(Cateid),</p>
<p>&nbsp;10&nbsp; constraint patient_Depart foreign key(Departid)</p>
<p>&nbsp;11&nbsp; references Depart(Departid)</p>
<p>&nbsp;12&nbsp; )tablespace patientspace;</p>
<p>表已创建。</p>
<h4>4.1.6 创建医生信息表</h4>
<p>SQL&gt; create table doctor(</p>
<p>&nbsp; 2&nbsp; Dno number(10) primary key,</p>
<p>&nbsp; 3&nbsp; Dname varchar2(4) not null,</p>
<p>&nbsp; 4&nbsp; sex char(2) not null</p>
<p>&nbsp; 5&nbsp; check (sex in('男','女')),</p>
<p>&nbsp; 6&nbsp; Departid number(10) not null,</p>
<p>&nbsp; 7&nbsp; constraint doctor_Depart foreign key(Departid)references Depart(Departid)</p>
<p>8&nbsp; )tablespace patientspace;</p>
<p>表已创建。</p>
<h4>4.1.7 创建项目信息表</h4>
<p>SQL&gt; create table project(</p>
<p>&nbsp; 2&nbsp; cno number(10) primary key,</p>
<p>&nbsp; 3&nbsp; cname varchar(20) unique not null,</p>
<p>&nbsp; 4&nbsp; credit number(2) not null)tablespace patientspace;</p>
<p>表已创建。</p>
<h4>4.1.8 创建诊断结果信息表</h4>
<p>SQL&gt; create table Result(</p>
<p>&nbsp; 2&nbsp; Pno number(10) primary key,</p>
<p>&nbsp; 3&nbsp; Pname varchar2(10) not null,</p>
<p>&nbsp; 4&nbsp; cno number(10) not null,</p>
<p>&nbsp; 5&nbsp; cname varchar2(20) not null,</p>
<p>&nbsp; 6&nbsp; Result number(3) not null,</p>
<p>&nbsp; 7&nbsp; credit number(3) not null,</p>
<p>&nbsp; 8&nbsp; constraint Result_patient foreign key(Pno)references patient(Pno),</p>
<p>&nbsp;9&nbsp; constraint Result_project foreign key(cno)references project(cno)</p>
<p>&nbsp;10&nbsp; )tablespace patientspace;</p>
<p>表已创建。</p>
<h3><a name="_Toc74614368"></a>4.2 索引</h3>
<h4>4.2.1 在表中的列上创建索引</h4>
<p>SQL&gt; create index DepPname_index</p>
<p>&nbsp; 2&nbsp; on Cate(DepPname)</p>
<p>&nbsp; 3&nbsp; tablespace patientspace;</p>
<h4>4.2.2 打开表中列上的索引的监控状态</h4>
<p>SQL&gt; alter index DepPname_index monitoring usage;</p>
<p>索引已更改。</p>
<p>通过数字字典v$object_usage可以查看哪些索引正在被监控</p>
<p>SQL&gt; column index_name format a15;</p>
<p>SQL&gt; column table_name format a15;</p>
<p>SQL&gt; select index_name,table_name,monitoring,</p>
<p>&nbsp; 2&nbsp; used,start_monitoring,end_monitoring</p>
<p>&nbsp; 3&nbsp; from v$object_usage;</p>
<p>&nbsp;</p>
<p>INDEX_NAME&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; TABLE_NAME&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; MON USE START_MONITORING&nbsp;&nbsp;&nbsp; END_MONITORING</p>
<p>--------------- --------------- --- --- ------------------- ----------------</p>
<p>DEPPNAME_INDEX CATE&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; YES NO&nbsp; 06/04/2021 15:04:26</p>
<h3><a name="_Toc74614369"></a>4.3 视图</h3>
<h4>4.3.1 创建基于Cate表和Depart表的视图</h4>
<p>SQL&gt; create view v1</p>
<p>&nbsp; 2&nbsp; as</p>
<p>&nbsp; 3&nbsp; select c.Cateid,c.DepPname,m.DeparDname</p>
<p>&nbsp; 4&nbsp; from Cate c left join Depart m</p>
<p>&nbsp; 5&nbsp; on c.Departid=m.Departid;</p>
<p>视图已创建。</p>
<h4>4.3.2 创建基于Result表的视图</h4>
<p>SQL&gt; create view v2</p>
<p>&nbsp; 2&nbsp; as</p>
<p>&nbsp; 3&nbsp; select Pno,Pname,cname,Result from Result where Result&lt;60;</p>
<p>视图已创建。</p>
<h3><a name="_Toc74614370"></a>4.4 使用序列</h3>
<p>创建一个名为patient_seq的序列</p>
<p>SQL&gt; create sequence patient_seq</p>
<p>&nbsp; 2&nbsp; start with 1</p>
<p>&nbsp; 3&nbsp; increment by 1</p>
<p>&nbsp; 4&nbsp; nocache</p>
<p>&nbsp; 5&nbsp; nocycle</p>
<p>&nbsp; 6&nbsp; order;</p>
<p>序列已创建。</p>
<p>&nbsp;</p>
<p>对表插入数据。</p>
<p>```</p>
<p>-- patient表数据插入20000</p>
<p>declare</p>
<p>i int;</p>
<p>Pno number(20);</p>
<p>Pname VARCHAR2(100);</p>
<p>sex VARCHAR2(100);</p>
<p>Cateid number(20);</p>
<p>Departid number(20);</p>
<p>begin</p>
<p>i:=1;</p>
<p>while i&lt;=20000</p>
<p>loop</p>
<p>Pno:=i;</p>
<p>Pname:= ''|| i;</p>
<p>sex := '男'|| i;</p>
<p>Cateid := '123'|| i;</p>
<p>Departid := '123'|| i;</p>
<p>insert into train_( Pno,Pname,sex,Cateid,Departid) values (Pno,Pname,sex,Cateid,Departid);</p>
<p>i:=i+1;</p>
<p>end loop;</p>
<p>commit;</p>
<p>end;</p>
<p>/</p>
<p>&nbsp;</p>
<p>-- Result表数据插入20000</p>
<p>&nbsp;</p>
<p>declare</p>
<p>i int;</p>
<p>Pno number(20);</p>
<p>Pname VARCHAR2(100);</p>
<p>cno VARCHAR2(100);</p>
<p>cname number(20);</p>
<p>Result number(20);</p>
<p>credit number(3)</p>
<p>begin</p>
<p>i:=1;</p>
<p>while i&lt;=20000</p>
<p>loop</p>
<p>Pno:=i;</p>
<p>Pname:= ''|| i;</p>
<p>sex := '男'|| i;</p>
<p>Cateid := '123'|| i;</p>
<p>Departid := '123'|| i;</p>
<p>insert into train_( Pno,Pname,cno,cname,Result,credit) values( Pno,Pname,cno,cname,Result,credit);</p>
<p>i:=i+1;</p>
<p>end loop;</p>
<p>commit;</p>
<p>end;</p>
<p>/</p>
<h2><a name="_Toc74614371"></a>5 查询</h2>
<h3><a name="_Toc74614372"></a>5.1 SQL语言基础</h3>
<p>统计各专业女同学人数</p>
<p>SQL&gt; select Departid,count(*) from patient</p>
<p>&nbsp; 2&nbsp; where sex='女'</p>
<p>&nbsp; 3&nbsp; group by Departid</p>
<p>&nbsp; 4&nbsp; having count(*)&gt;0</p>
<p>&nbsp; 5&nbsp; order by count(*) desc;</p>
<h3><a name="_Toc74614373"></a>5.2 子查询与高级查询</h3>
<h4>5.2.1 查询诊断结果评分大于80分的病患的编号和平均诊断结果</h4>
<p>SQL&gt; select Pno, avg(Result) from Result</p>
<p>2&nbsp; group by Pno</p>
<p>3&nbsp; having avg(Result)&gt;80;</p>
<h4>5.2.2 查询&ldquo;1&rdquo;诊断结果比&ldquo;2&ldquo;诊断结果评分高的所有病患编号</h4>
<p>SQL&gt; select a.Pno</p>
<p>&nbsp; 2&nbsp; from (select * from Result s where s.cno = 1) a,</p>
<p>&nbsp; 3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (select * from Result s where s.cno = 2) b</p>
<p>&nbsp; 4&nbsp; where a.Pno = b.Pno</p>
<p>&nbsp; 5&nbsp; and a.Result &gt; b.Result;</p>
<h4>5.2.3 查询姓&ldquo;刘&ldquo;的病患名单</h4>
<p>SQL&gt; select * from patient where Pname like '刘%';</p>
<h4>5.2.4 查询1项以上诊断结果不健康的病患的编号及其平均诊断结果评分</h4>
<p>SQL&gt; select Pno, avg(Result)&nbsp; from Result</p>
<p>&nbsp; 2&nbsp; group by Pno having Pno in(</p>
<p>&nbsp; 3&nbsp; select Pno from Result</p>
<p>&nbsp; 4&nbsp; where Result&lt;60</p>
<p>&nbsp; 5&nbsp; group by Pno</p>
<p>&nbsp; 6&nbsp; having count(*) &gt;1);</p>
<h4>5.2.5 查询类别信息的同时显示其所在科室名称</h4>
<p>SQL&gt; select c.Cateid,c.DepPname,m.DeparDname</p>
<p>&nbsp; 2&nbsp; from Cate c left join Depart m</p>
<p>&nbsp; 3&nbsp; on c.Departid=m.Departid;</p>
<h4>5.2.6 查询每种类别被患者选择的数目</h4>
<p>SQL&gt; select cno, count(*) rs,</p>
<p>&nbsp; 2&nbsp; (select cname from project</p>
<p>&nbsp; 3&nbsp; where cno=Result.cno)</p>
<p>&nbsp; 4&nbsp; cname from Result</p>
<p>&nbsp; 5&nbsp; group by cno;</p>
<h4>5.2.7 查询所有病患的就诊信息</h4>
<p>SQL&gt; select s.Pno, s.Pname patdenDname,</p>
<p>&nbsp; 2&nbsp; c.cno, c.cname projectname</p>
<p>&nbsp; 3&nbsp; from patient s, Result g, project c</p>
<p>&nbsp; 4&nbsp; where s.Pno=g.Pno and g.cno=c.cno;</p>
<h2><a name="_Toc74614374"></a>6 SQL语句</h2>
<h3><a name="_Toc74614375"></a>6.1 显示表中的编号为1的类别名</h3>
<p>使用PL/SQL程序块，输出显示project表中的编号为1的类别名。</p>
<p>SQL&gt; set serveroutput on;</p>
<p>SQL&gt; declare</p>
<p>&nbsp; 2&nbsp; id constant number(10):=1;</p>
<p>&nbsp; 3&nbsp; name varchar2(30);</p>
<p>&nbsp; 4&nbsp; begin</p>
<p>&nbsp; 5&nbsp; select cname into name</p>
<p>&nbsp; 6&nbsp; from project where cno=id;</p>
<p>&nbsp; 7&nbsp; dbms_output.put_line(id||name);</p>
<p>&nbsp; 8&nbsp; end;</p>
<p>&nbsp; 9&nbsp; /</p>
<p>1oracle</p>
<p>PL/SQL 过程已成功完成。</p>
<h3><a name="_Toc74614376"></a>6.2 判断诊断结果61分所处的等级</h3>
<p>在PL/SQL中，使用if条件语句判断诊断结果61分所处的等级。</p>
<p>SQL&gt; declare</p>
<p>&nbsp; 2&nbsp; score binary_integer:=61;</p>
<p>&nbsp; 3&nbsp; begin</p>
<p>&nbsp; 4&nbsp; if score &gt;=90 then</p>
<p>&nbsp; 5&nbsp; dbms_output.put_line('优秀');</p>
<p>&nbsp; 6&nbsp; elsif score&gt;=80 then</p>
<p>&nbsp; 7&nbsp; dbms_output.put_line('良好');</p>
<p>&nbsp; 8&nbsp; elsif score&gt;=70 then</p>
<p>&nbsp; 9&nbsp; dbms_output.put_line('中等');</p>
<p>&nbsp;10&nbsp; elsif score&gt;=60 then</p>
<p>&nbsp;11&nbsp; dbms_output.put_line('健康');</p>
<p>&nbsp;12&nbsp; else</p>
<p>&nbsp;13&nbsp; dbms_output.put_line('不健康');</p>
<p>&nbsp;14&nbsp; end if;</p>
<p>&nbsp;15&nbsp; end;</p>
<p>&nbsp;16&nbsp; /</p>
<p>健康</p>
<h3><a name="_Toc74614377"></a>6.3 判断患者的诊断结果是否健康</h3>
<p>在PL/SQL中，查询所有患者的诊断结果是否有不健康，如有不健康就触发异常并输出。</p>
<p>SQL&gt; declare</p>
<p>&nbsp; 2&nbsp; cursor c1 is select Pname from Result where Result&lt;60;</p>
<p>&nbsp; 3&nbsp; one Result.Pname%type;</p>
<p>&nbsp; 4&nbsp; e1 exception;</p>
<p>&nbsp; 5&nbsp; begin</p>
<p>&nbsp; 6&nbsp; open c1;</p>
<p>&nbsp; 7&nbsp; fetch c1 into one;</p>
<p>&nbsp; 8&nbsp; if c1%found then raise e1;</p>
<p>&nbsp; 9&nbsp; end if;</p>
<p>&nbsp;10&nbsp; exception</p>
<p>&nbsp;11&nbsp; when e1 then</p>
<p>&nbsp;12&nbsp; dbms_output.put_line(one||'不健康');</p>
<p>&nbsp;13&nbsp; close c1;</p>
<p>&nbsp;14&nbsp; end;</p>
<p>&nbsp;15&nbsp; /</p>
<p>杨不健康</p>
<p>PL/SQL 过程已成功完成。</p>
<h2><a name="_Toc74614378"></a>7 创建存储过程</h2>
<h3><a name="_Toc74614379"></a>7.1 创建一个存储过程update_patient</h3>
<p>创建一个存储过程update_patient，该过程用来将patient表中的编号为1的患者的姓名改为&rdquo;惨惨&rdquo;。</p>
<p>SQL&gt; create procedure update_patient</p>
<p>&nbsp; 2&nbsp; as</p>
<p>&nbsp; 3&nbsp; begin</p>
<p>&nbsp; 4&nbsp; update patient set Pname='惨惨' where Pno =1;</p>
<p>&nbsp; 5&nbsp; end update_patient;</p>
<p>&nbsp; 6&nbsp; /</p>
<p>过程已创建。</p>
<p>使用execute语句调用存储过程，如下：</p>
<p>SQL&gt; execute update_patient;</p>
<p>PL/SQL 过程已成功完成。</p>
<h3><a name="_Toc74614380"></a>7.2 创建一个存储过程get_Result_information</h3>
<p>采取直接在存储过程中使用DBMS_OUTPUT.PUT_LINE过程输出相关内容。</p>
<p>SQL&gt; create or replace procedure get_Result_information</p>
<p>&nbsp; 2&nbsp; (s_no number)</p>
<p>&nbsp; 3&nbsp; as</p>
<p>&nbsp; 4&nbsp; s_name varchar2(10);</p>
<p>&nbsp; 5&nbsp; c_no number;</p>
<p>&nbsp; 6&nbsp; c_name varchar2(20);</p>
<p>&nbsp; 7&nbsp; s_Result number(3);</p>
<p>&nbsp; 8&nbsp; c_credit number(3);</p>
<p>&nbsp; 9&nbsp; begin</p>
<p>&nbsp;10&nbsp; select Pname,cno,cname,Result,credit</p>
<p>&nbsp;11&nbsp; into s_name,c_no,c_name,s_Result,c_credit</p>
<p>&nbsp;12&nbsp; from Result where Pno=s_no;</p>
<p>&nbsp;13&nbsp; DBMS_OUTPUT.PUT_LINE('患者姓名：'||s_name);</p>
<p>&nbsp;14&nbsp; DBMS_OUTPUT.PUT_LINE('类别编号：'||c_no);</p>
<p>&nbsp;15&nbsp; DBMS_OUTPUT.PUT_LINE('类别名称：'||c_name);</p>
<p>&nbsp;16&nbsp; DBMS_OUTPUT.PUT_LINE('诊断结果：'||s_Result);</p>
<p>&nbsp;17&nbsp; DBMS_OUTPUT.PUT_LINE('指标：'||c_credit);</p>
<p>&nbsp;18&nbsp; end get_Result_information;</p>
<p>&nbsp;19&nbsp; /</p>
<p>&nbsp;</p>
<p>过程已创建。</p>
<p>&nbsp;</p>
<p>调用get_Result_information存储过程。例如获取Pno为1401的患者的成绩信息，如下：</p>
<p>SQL&gt; set serveroutput on</p>
<p>SQL&gt; exec get_Result_information(1402);</p>
<p>患者姓名：杨</p>
<p>类别编号：2</p>
<p>类别名称：java</p>
<p>诊断结果：40</p>
<p>指标：8</p>
<p>&nbsp;</p>
<p>PL/SQL 过程已成功完成。</p>
<h2><a name="_Toc74614381"></a>8 函数设计</h2>
<h3><a name="_Toc74614382"></a>8.1 创建一个函数get_Pname</h3>
<p>创建一个函数get_Pname，该函数实现按Pno获取Pname，函数创建如下：</p>
<p>SQL&gt; create function get_Pname(pat_num number)</p>
<p>&nbsp; 2&nbsp; return varchar2 as</p>
<p>&nbsp; 3&nbsp; pat_name patient.Pname%type;</p>
<p>&nbsp; 4&nbsp; begin</p>
<p>&nbsp; 5&nbsp; select Pname into pat_name from patient where Pno=pat_num;</p>
<p>&nbsp; 6&nbsp; return pat_name;</p>
<p>&nbsp; 7&nbsp; end get_Pname;</p>
<p>&nbsp; 8&nbsp; /</p>
<p>&nbsp;</p>
<p>函数已创建。</p>
<p><strong>&nbsp;</strong></p>
<p>因为函数是具有返回值的，所以它类似于一个表达式，调用函数可以直接使用select语句，如下：</p>
<p>SQL&gt; select get_Pname(1) from dual;</p>
<p>&nbsp;</p>
<p>GET_PNAME(1)</p>
<p>-----------------------------------------------------------------</p>
<p>shen</p>
<h3><a name="_Toc74614383"></a>8.2 创建一个函数re_pat_info</h3>
<p>创建一个函数re_pat_info,以班级号为参数，返回各个班级总平均分。</p>
<p>SQL&gt; create or replace function re_pat_info(cl_id number) return varchar2 is</p>
<p>&nbsp; 2&nbsp;&nbsp;&nbsp; v_result varchar2(100);</p>
<p>&nbsp; 3&nbsp;&nbsp;&nbsp; cursor cur_Cate is</p>
<p>&nbsp; 4&nbsp;&nbsp;&nbsp;&nbsp; select a.DepPname as DepPname,</p>
<p>&nbsp; 5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; round(avg(Result), 2) as avg_score</p>
<p>&nbsp; 6&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; from Cate a</p>
<p>&nbsp; 7&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; inner join patient b</p>
<p>&nbsp; 8&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on a.Cateid = b.Cateid</p>
<p>&nbsp; 9&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; inner join Result c</p>
<p>&nbsp;10&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on c.Pno = b.Pno</p>
<p>&nbsp;11&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; where a.Cateid = cl_id</p>
<p>&nbsp;12&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; group by a.DepPname;</p>
<p>&nbsp;13&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; c_row cur_Cate%rowtype;</p>
<p>&nbsp;14&nbsp; begin</p>
<p>&nbsp;15&nbsp;&nbsp;&nbsp; for c_row in cur_Cate loop</p>
<p>&nbsp;16&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; dbms_output.put_line('班级：' || c_row.DepPname ||</p>
<p>&nbsp;17&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; '总平均分为：' || c_row.avg_score);</p>
<p>&nbsp;18&nbsp;&nbsp;&nbsp; end loop;</p>
<p>&nbsp;19&nbsp;&nbsp;&nbsp; return v_result;</p>
<p>&nbsp;20&nbsp; end;</p>
<p>&nbsp;21&nbsp;&nbsp; /</p>
<p>&nbsp;</p>
<p>调用函数：</p>
<p>SQL&gt; declare</p>
<p>&nbsp; 2&nbsp; t varchar2(50);</p>
<p>&nbsp; 3&nbsp; v_number number(10);</p>
<p>&nbsp; 4&nbsp; cursor cur is select Cateid from Cate;</p>
<p>&nbsp; 5&nbsp; begin</p>
<p>&nbsp; 6&nbsp;&nbsp;&nbsp; open cur;</p>
<p>&nbsp; 7&nbsp;&nbsp;&nbsp; fetch cur into v_number;</p>
<p>&nbsp; 8&nbsp;&nbsp;&nbsp; while cur%found loop</p>
<p>&nbsp; 9&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; t:=re_pat_info(v_number);</p>
<p>&nbsp;10&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; fetch cur into v_number;</p>
<p>&nbsp;11&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; end loop;</p>
<p>&nbsp;12&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; close cur;</p>
<p>&nbsp;13&nbsp; end;</p>
<p>&nbsp;14&nbsp; /</p>
<h2><a name="_Toc74614384"></a>9 备份方案</h2>
<h3><a name="_Toc74614385"></a>9.1 RMAN（备份与恢复管理器）</h3>
<h4>9.1.1 为目录创建一个单独的表空间</h4>
<p>SQL&gt;Create tablespace tools datafile &lsquo;fielname&rsquo; size 50m;</p>
<h4>9.1.2创建RMAN用户</h4>
<p>SQL&gt;Create user RMAN identified by RMAN default tablespace tools temporary tablespace temp;</p>
<h4>9.1.3 给RMAN授予权限</h4>
<p>SQL&gt;Grant connect , resource , recovery_catalog_owner to rman;</p>
<h4>9.1.4 打开RMAN</h4>
<p>$&gt;RMAN</p>
<h4>9.1.5 连接数据库</h4>
<p>RMAN&gt;connect catalog rman/rman</p>
<h4>9.1.6 创建恢复目录</h4>
<p>RMAN&gt;Create catalog tablespace tools</p>
<p>注册目标数据库，恢复目录创建成功后，就可以注册目标数据库了，目标数据库就是需要备份的数据库，一个恢复目录可以注册多个目标数据库，注册目标数据库的命令为：</p>
<p>$&gt;RMAN target internal/password catalog rman/rman@rcdb;</p>
<p>RMAN&gt;Register database;</p>
<p>数据库注册完成,就可以用RMAN来进行备份了，更多命令请参考ORACLE联机手册或《ORACLE8i备份与恢复手册》。</p>
<p>注销数据库不是简单的在RMAN提示下反注册就可以了，需要运行一个程序包，过程如下：</p>
<p>（1）. 连接目标数据库，获得目标数据库ID</p>
<p>$&gt; RMAN target internal/password catalog rman/rman@rcdb;</p>
<p>&nbsp;RMAN-06005: connected to target database: RMAN (DBID=1231209694)</p>
<p>（2）. 查询恢复目录，得到更详细的信息</p>
<p>SQL&gt; SELECT db_key, db_id FROM db WHERE db_id = 1231209694;</p>
<p>DB_KEY&nbsp;&nbsp;&nbsp;&nbsp; DB_ID&nbsp;&nbsp;&nbsp;&nbsp;</p>
<p>---------- ---------------</p>
<p>&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;1 1856492365</p>
<p>1 row selected.</p>
<p>（3）.运行过程dbms_rcvcat.unregisterdatabase注销数据库，如</p>
<p>SQL&gt; EXECUTE dbms_rcvcat.unregisterdatabase(1 , 1856492365)</p>
<p>（4）采用RMAN进行备份</p>
<p>&nbsp;</p>
<p>1).备份整个数据库</p>
<p>&nbsp;backup full tag &lsquo;basicdb&rsquo; format &lsquo;/bak/oradata/full_%u_%s_%p&rsquo; database;</p>
<p>2).备份一个表空间</p>
<p>&nbsp;backup tag &lsquo;tsuser&rsquo; format &lsquo;/bak/oradata/tsuser_%u_%s_%p&rsquo; tablespace users;</p>
<p>3).备份归档日志</p>
<p>&nbsp;backup tag &lsquo;alog&rsquo; format &lsquo;/bak/archivebak/arcbak_%u_%s_%p&rsquo; archivelog all delete input;</p>
