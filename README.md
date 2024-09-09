# salesforce-with-devops
day 1 ---6:=============================
-----sfdx commands------
create two org consider one is dev and other is qa
dev is source org and qa is target org
download vs code and install sales force cli 
to check sales force cli installed command is----  sfdx
to install project to get necessary folders and menifestfile command is---- sfdx force:project:create --projectname  mywork --manifest
to login to dev and qa orgs command is-----sfdx auth:web:login --instanceurl https://login.salesforce.com --setalias aliasname
to check list of orgs connected command is-----sfdx force:org:list
to retrieve data from source org dev command is---sfdx force:source:retrieve --manifest manifestpath -u devorgname
to retrieve data from target org qa command is---sfdx force:source:deploy --manifest manifestpath -u qaorgname

-----manifestfile---------
for fields and objects - in normal way in type take member as api name of object and name as customobject and another type take field 
for profile ----u have to prepare profile admin(user which given permissions) as well as the field
for apex class--- u can prepare apex class as type and insert in member class as well as testcase file
for standard object if piclist is changed  we have to take from salesforce standard objects (standard valueset salesforce)(https://developer.salesforce.com/docs/atlas.en-us.api_meta.meta/api_meta/standardvalueset_names.htm)

------post and pre destructive changes---------
in order detete the fields and there references for(pagelayouts,profiles)we use predestructivechanges(we can keep manifest file empty)
in order detete the fields and there references for(flows,validation rules,apex class)we use postdestructivechanges(we have update manifest file)

-------errors----------
two types of errors one is warning and other is error
--ignorewarning  -g | --ignorewarnings
--ignoreerrors   -o | --ignoreerrors

-------for test cases--------
https://developer.salesforce.com/docs/atlas.en-us.240.0.sfdx_cli_reference.meta/sfdx_cli_reference/cli_reference_force_source.htm#cli_reference_force_source_deploy
[-l TESTLEVEL] and [-r RUNTESTS]









