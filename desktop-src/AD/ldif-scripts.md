---
title: LDIF-Skripts
description: Das LDAP Data Interchange Format (LDIF) ist ein IETF-Standard (Internet Engineering Task Force), der definiert, wie Verzeichnisdaten zwischen Verzeichnisservern importiert und exportiert werden, die LDAP-Dienstanbieter verwenden.
ms.assetid: a87d0d34-96c0-4cef-a38e-30a7e2291a7a
ms.tgt_platform: multiple
keywords:
- LDIF Scripts Active Directory
- LDIF Scripts Active Directory , About
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad45c51fc16b3c19c3e59f4cfba2e006d4df900c20ce7ddc1b801478a22982c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187084"
---
# <a name="ldif-scripts"></a>LDIF-Skripts

Das LDAP Data Interchange Format (LDIF) ist ein IETF-Standard (Internet Engineering Task Force), der definiert, wie Verzeichnisdaten zwischen Verzeichnisservern importiert und exportiert werden, die LDAP-Dienstanbieter verwenden. Windows 2000 und Windows Server 2003 enthalten das Befehlszeilenprogramm LDIFDE, mit dem Verzeichnisobjekte mithilfe von LDIF-Dateien in Active Directory Domain Services importiert werden können. MIT LDIFDE können Sie einen Filter auf eine bestimmte Zeichenfolge festlegen, um Verzeichnisobjekte in Active Directory Domain Services als LDIF-Dateien zu suchen und aufzulisten, die von Schemaadministratoren leicht gelesen werden können.

Beim Importieren einer Unicode-Datei importiert LDIFDE die Datei als Unicode, wenn sie den Unicode-Bezeichner am Anfang der Datei enthält. Wenn Sie eine Datei als Unicode importieren möchten, wenn sie nicht den Unicode-Bezeichner am Anfang der Datei enthält, können Sie den Schalter -u verwenden, um den Import als Unicode zu erzwingen.

Der Standardmodus zum Exportieren von Dateien ist ANSI. Wenn Unicode-Einträge vorhanden sind, werden sie in das Base64-Format konvertiert. Verwenden Sie den Schalter -u, um eine Datei in das Unicode-Format zu exportieren.

Eine LDIF-Datei muss Schemaänderungen anwenden, wenn Abhängigkeiten zwischen den hinzugefügten Attributen bestehen. Beispielsweise sollten Vorwärtslinkattribute vor dem entsprechenden Backlinkattribut hinzugefügt werden. Sie müssen auch den Schemacache aktualisieren, bevor Sie Klassen hinzufügen, die von Attributen oder Klassen abhängen, die zuvor im LDIF-Skript hinzugefügt wurden. Weitere Informationen finden Sie im folgenden Codebeispiel.

Beachten Sie, dass Sie für binäre Werte die Werte als base64 codieren müssen. Base64-Codierung ist in IETF RFC 2045, Abschnitt 6.8 definiert.

Weitere Informationen zum Format von LDIF-Dateien finden Sie auf der Website der Internet Engineering Task Force unter [THE LDAP Data Interchange Format (LDIF) – Technical Specification](https://www.ietf.org/rfc/rfc2849.txt) (RFC 2849).

## <a name="ntds-specific-ldif-changetypes"></a>NTDS-spezifische LDIF-Änderungstypen

Es ist besser, ntdsSchema-Änderungstypen zu verwenden, \* anstatt ldifde -k aufzurufen. Die Option -k von ldifde ignoriert einen größeren Satz von LDAP-Fehlern. Die vollständige Liste der ignorierten Fehler lautet wie folgt:

-   Das -Objekt ist bereits ein Mitglied der Gruppe.
-   Eine Objektklassenverletzung (d. h. die angegebene Objektklasse ist nicht vorhanden), wenn das importierte Objekt keine anderen Attribute aufweist.
-   Objekt ist bereits vorhanden (**LDAP \_ ALREADY \_ EXISTS**)
-   Einschränkungsverletzung (**LDAP \_ CONSTRAINT \_ VIOLATION**)
-   Attribut oder Wert bereits vorhanden (**\_ LDAP-ATTRIBUT ODER WERT \_ \_ \_ EXISTS**)
-   no such object (**LDAP \_ NO SUCH \_ \_ OBJECT**)

Die folgenden Änderungstypen sind speziell für Schemaupgradevorgänge konzipiert.



| Changetype                      | BESCHREIBUNG                                                                                                                                                                                                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ntdsSchemaAdd**<br/>    | **ntdsSchemaAdd** entspricht dem **Hinzufügen** in einer LDIF-Datei. Der einzige Unterschied besteht darin, dass **ntdsSchemaAdd** dazu führen würde, dass ldifde einen **Add-Vorgang** überspringt, wenn das Objekt bereits im Schema vorhanden ist. (**LDAP \_ ALREADY \_ EXISTS** wird ignoriert.)<br/>                                   |
| **ntdsSchemaModify**<br/> | **ntdsSchemaModify** entspricht **der Änderung** in einer LDIF-Datei. Der einzige Unterschied besteht darin, dass **ntdsSchemaModify** dazu führen würde, dass ldifde einen **Änderungsvorgang** überspringt, wenn das Objekt nicht im Schema gefunden wird. (**LDAP NO SUCH \_ \_ \_ OBJECT** wird ignoriert.)<br/>                        |
| **ntdsSchemaDelete**<br/> | **ntdsSchemaDelete** entspricht dem **Löschen** in einer LDIF-Datei. Der einzige Unterschied besteht darin, dass **ntdsSchemaDelete** dazu führen würde, dass ldifde einen **Löschvorgang** überspringt, wenn das Objekt nicht im Schema gefunden wird. (**LDAP NO SUCH \_ \_ \_ OBJECT** wird ignoriert.)<br/>                        |
| **ntdsSchemaModRdn**<br/> | **ntdsSchemaModRdn** entspricht **modrdn** in einer LDIF-Datei. Der einzige Unterschied besteht darin, dass **ntdsSchemaModRdn** bewirkt, dass ldifde einen modify-relative-distinguished-name-Vorgang überspringt, wenn das Objekt nicht im Schema gefunden wird. (**LDAP NO SUCH \_ \_ \_ OBJECT** wird ignoriert.)<br/> |



 

## <a name="example"></a>Beispiel

Das folgende Codebeispiel enthält Folgendes:

-   Myschemaext.ldf ist ein LDIF-Skript, das neue Attribute und Klassen enthält. Beachten Sie, dass es sich bei dieser Datei um eine geänderte Version der Datei handelt, die aus Lgetattcls.vbs generiert wurde. Beachten Sie auch, dass das Attribut **My-Test-Attribute-DN-FL** vor **My-Test-Attribute-DN-BL** verschoben wurde, da der Rücklink (**My-Test-Attribute-DN-BL**) von der Weiterleitungsverknüpfung (**My-Test-Attribute-DN-FL**) abhängig ist. Darüber hinaus wird das Betriebsattribut **schemaUpdateNow** an zwei Stellen festgelegt, um Aktualisierungen des Schemacaches auszulösen, sodass abhängige Attribute und Klassen zum Hinzufügen der beiden Klassen im Skript verfügbar sind.
    > [!Note]  
    > Informationen zur Quelle der ID in den linkID:-Anweisungen finden Sie im Thema [Abrufen einer Link-ID.](obtaining-a-link-id.md)

     

-   Lgetattcls.vbs ist eine VBScript-Datei, die das LDIF-Skript generiert, das als Ausgangspunkt für myschemaext.ldf verwendet wird. Beachten Sie, dass der aktuelle Schemapfad durch CN=Schema,CN=Configuration,DC=myorg,DC=com ersetzt wird. Sie können DC=myorg,DC=com ersetzen, um den Distinguished Name (DN) widerzuspiegeln, der im LDIF-Skript veröffentlicht werden soll. Stellen Sie sicher, dass LSETATTCLS.VBS die Änderung in seinem **sFromDN** widerspiegelt, sodass der richtige DN ersetzt wird, wenn das LDIF-Skript angewendet wird. Beachten Sie auch, dass das Skript ein Präfix verwendet, um die Klassen und Attribute zu finden, die Sie auch definieren und ein Präfix für alle Klassen und Attribute verwenden sollten. Weitere Informationen finden Sie unter [Benennen von Attributen und Klassen.](naming-attributes-and-classes.md) Darüber hinaus gibt das Skript nur die erforderlichen Attribute für die **AttributeSchema-** und **classSchema-Objekte** in die LDIF-Datei aus.
-   Lsetattcls.vbs ist eine VBScript-Datei, die das Skript Myschemaext.ldf verwendet, um die neuen Attribute und Klassen im Skript hinzuzufügen. Stellen Sie sicher, dass der Schemamaster in geschrieben werden kann, bevor Sie das Skript ausführen.

## <a name="myschemaextldf"></a>MYSCHEMAEXT. Ldf

``` syntax
dn: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-CaseExactString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.65
attributeSyntax: 2.5.5.3
cn: My-Test-Attribute-CaseExactString
description: Test attribute of syntax CaseExactString used to show how to add a CaseExactString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeCaseExactString
distinguishedName: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMSyntax: 27
name: My-Test-Attribute-CaseExactString
schemaIDGUID:: 6ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-FL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.614
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-FL
description: Test forward link attribute of syntax DN used to show how to add a forward link attribute. Back link is My-Test-Attribute-DN-BL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNFL
linkID: 1.2.840.113556.1.2.50
distinguishedName: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-FL
schemaIDGUID:: YGLudffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-BL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.615
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-BL
description: Test back link attribute of syntax DN used to show how to add a back link attribute. Forward link is My-Test-Attribute-DN-FL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNBL
linkID: 1.2.840.113556.6.1234
distinguishedName: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-BL
schemaIDGUID:: jFfbhffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-Regular
attributeID: 1.2.840.113556.1.4.7000.159.24.10.613
attributeSyntax: 2.5.5.12
cn: My-Test-Attribute-DN-Regular
description: Test attribute of syntax DN used to show how to add a DN attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNRegular
distinguishedName: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 64
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-Regular
schemaIDGUID:: 5QSznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DNString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.611
attributeSyntax: 2.5.5.14
cn: My-Test-Attribute-DNString
description: Test attribute of syntax DNString used to show how to add a DNString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNString
distinguishedName: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KoZIhvcUAQEBDA==
oMSyntax: 127
rangeLower: 1
rangeUpper: 64
name: My-Test-Attribute-DNString
schemaIDGUID:: 5ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0

DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Auxiliary-Class1
description: Test class used to show how to add an auxiliary class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestAuxiliaryClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.11
instanceType: 4
objectClassCategory: 3
schemaIDGUID:: mmsxdsXb0hGL0AAA+HW2YA==
subClassOf: Top
mayContain: my-Test-Attribute-DNString
mustContain: description
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Structural-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Structural-Class1
auxiliaryClass: myTestAuxiliaryClass1
defaultHidingValue: FALSE
defaultObjectCategory: CN=Organizational-Unit,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
defaultSecurityDescriptor: D:(A;;RPWPCRCCDCLCLOLORCWOWDSDDTDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU)
admindescription: Test class used to show how to add a structure class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestStructuralClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.12
mayContain: myTestAttributeDNFL
mayContain: wWWHomePage
mustContain: url
instanceType: 4
objectClassCategory: 1
possSuperiors: organizationalUnit
rDNAttID: ou
schemaIDGUID:: 1HsnsL7b0hGL0AAA+HW2YA==
subClassOf: organizationalUnit
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

## <a name="lgetattclsvbs"></a>LGETATTCLS.VBS


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object and get the
' reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext1.ldf"
sFromDN = sSchema
sToDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sAttrPrefix = "My-Test"
sFilter = "(&((cn=" & sAttrPrefix & "*)(|(objectCategory=classSchema)_
(objectCategory=attributeSchema))))"
sRetAttr = "dn,adminDescription,adminDisplayName,governsID,cn,mayContain,_
mustContain,systemMayContain,systemMustContain,lDAPDisplayName,_
objectClassCategory,distinguishedName,objectCategory,objectClass,_
possSuperiors,systemPossSuperiors,subClassOf,defaultObjectCategory,_
name,schemaIDGUID,auxiliaryClass,auxiliaryClass,systemAuxiliaryClass,_
description,defaultHidingValue,rDNAttId,defaultSecurityDescriptor,_
attributeID,attributeSecurityGUID,attributeSyntax,_
isMemberOfPartialAttributeSet,isSingleValued,mAPIID,oMSyntax,rangeLower,_
rangeUpper,searchFlags,oMObjectClass,linkID"
 
' Add flag rootDN.
sCommand = "ldifde -d " & sSchema 
sCommand = sCommand & " -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
' Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for attributes.
sCommand = sCommand & " -r " & sFilter
' Add flag for attributes to return.
sCommand = sCommand & " -l " & sRetAttr
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText) strText = "Error 0x"_
 & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



## <a name="lsetattclsvbs"></a>LSETATTCLS.VBS


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
'''''''''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
'''''''''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("serverReference")
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
' strText = "Schema Master has the following DN: "& sComputer
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext.ldf"
sFromDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sToDN = sSchema
' Add flag replace fromDN with ToDN.
sCommand = "ldifde -i -k -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
'Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for my attributes.
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 





