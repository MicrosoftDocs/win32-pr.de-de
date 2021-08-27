---
description: Die Methoden und Eigenschaften des SWbemLastError-Objekts enthalten und bearbeiten Fehlerobjekte.
ms.assetid: 11a652fa-29e8-437b-8e62-e28e56a8a38d
ms.tgt_platform: multiple
title: SWbemLastError-Objekt (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError
- Associators_
- AssociatorsAsync_
- Delete_
- DeleteAsync_
- ExecMethod_
- ExecMethodAsync_
- Instances_
- InstancesAsync_
- Put_
- PutAsync_
- References_
- ReferencesAsync_
- SpawnDerivedClass_
- SpawnInstance_
- Subclasses_
- SubclassesAsync_
- Derivation_
- get_Derivation_
- Methods_
- get_Methods_
- Qualifiers_
- get_Qualifiers_
- Security_
- get_Security_
- ISWbemLastError
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a73312c38857b57f3ffeec8fcaf8a9ea5847001393d0a03d4916da76ffcb8c0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314459"
---
# <a name="swbemlasterror-object"></a>SWbemLastError-Objekt

Die Methoden und Eigenschaften des **SWbemLastError-Objekts** enthalten und bearbeiten Fehlerobjekte. Die Methoden und Eigenschaften dieses Objekts sind identisch mit denen des [**SWbemObject-Objekts,**](swbemobject.md) werden jedoch verwendet, um Fehlerinformationen anstelle von WMI-Klasseninformationen zu enthalten. Dieses Objekt kann durch den VBScript **CreateObject-Aufruf erstellt** werden.

Sie können ein **SWbemLastError-Fehlerobjekt** erstellen, um die erweiterten Fehlerinformationen zu überprüfen, die einem vorherigen Methodenaufruf zugeordnet sind. Wenn keine Fehlerinformationen verfügbar sind, tritt beim Erstellen eines Fehlerobjekts ein Fehler auf. Wenn der Aufruf erfolgreich ist und ein Fehlerobjekt zurückgegeben wird, wird der Status des Objekts zurückgesetzt. Bei weiteren Versuchen, ein Fehlerobjekt abzurufen, tritt ein Fehler auf, bis ein neuer Fehler auftritt. Wenn Sie einen asynchronen Aufruf ausführen, bei dem ein Fehler auftritt, wird ihnen möglicherweise ein **SWbemLastError-Objekt** vom [**SWbemSink.OnCompleted-Ereignis**](swbemsink-oncompleted.md) im *objWbemErrorObject-Parameter* zurückgegeben.

## <a name="members"></a>Member

Das **SWbemLastError-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **SWbemLastError-Objekt** verfügt über diese Methoden.



| Methode                                                   | Beschreibung                                                                                  |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| **Associators\_**                                        | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/> |
| **AssociatorsAsync\_**                                   | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/> |
| [**Klon\_**](swbemlasterror-clone-.md)                 | Erstellt eine Kopie des aktuellen -Objekts.<br/>                                               |
| [**Compareto\_**](swbemlasterror-compareto-.md)         | Testet zwei -Objekte auf Gleichheit.<br/>                                                   |
| **Löschen\_**                                             | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/> |
| **DeleteAsync\_**                                        | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/> |
| **ExecMethod\_**                                         | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/> |
| **ExecMethodAsync\_**                                    | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/> |
| [**GetObjectText\_**](swbemlasterror-getobjecttext-.md) | Ruft die Textdarstellung des Objekts ab, das mit MOF-Syntax geschrieben wurde.<br/>       |
| **Instanzen\_**                                          | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/> |
| **InstancesAsync\_**                                     | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/> |
| **Put\_**                                                | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/> |
| **PutAsync\_**                                           | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/> |
| **Literatur\_**                                         | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/> |
| **ReferencesAsync\_**                                    | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/> |
| **SpawnDerivedClass\_**                                  | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/> |
| **SpawnInstance\_**                                      | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/> |
| **Unterklassen von  werden erstellt.\_**                                         | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/> |
| **UnterklassenAsync\_**                                    | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **SWbemLastError-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                      | Zugriffstyp          | Beschreibung                                                                                                                                                   |
|:--------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ableitung\_**<br/>                                   | Schreibgeschützt<br/> | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/>                                                                  |
| **Methoden\_** <br/>                                     | Schreibgeschützt<br/> | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/>                                                                  |
| [**Pfad\_**](swbemlasterror-path-.md)<br/>             | Schreibgeschützt<br/> | Enthält ein [**SWbemObjectPath-Objekt,**](swbemobjectpath.md) das den Objektpfad der aktuellen Klasse oder Instanz darstellt.<br/>                    |
| [**Eigenschaften\_**](swbemlasterror-properties-.md)<br/> | Schreibgeschützt<br/> | Stellt die Auflistung der Eigenschaften des **SWbemLastError-Objekts** dar. Diese Eigenschaft ist ein [**SWbemPropertySet-Objekt.**](swbempropertyset.md)<br/> |
| **Qualifikation\_**<br/>                                   | Schreibgeschützt<br/> | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/>                                                                  |
| **Sicherheit\_**<br/>                                     | Schreibgeschützt<br/> | Wird nicht verwendet. Das [**SWbemObject-Objekt**](swbemobject.md) bietet die gleiche Methode.<br/>                                                                  |



 

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Beispiel wird veranschaulicht, wie Fehler- und Fehlerobjektinformationen überprüft werden.


```VB
On Error Resume Next

'Ask for non-existent class to force error

Set t_Service = GetObject("winmgmts://./root/default")
Set t_Object = t_Service.Get("Nosuchclass000")

if Err = 0 Then
 WScript.Echo "Got a class"
Else
 WScript.Echo ""
 WScript.Echo "Err Information:"
 WScript.Echo ""
 WScript.Echo "  Source:", Err.Source
 WScript.Echo "  Description:", Err.Description
 WScript.Echo "  Number", "0x" & Hex(Err.Number)

 'Create the last error object
 set t_Object = CreateObject("WbemScripting.SWbemLastError")
 WScript.Echo ""
 WScript.Echo "WMI Last Error Information:"
 WScript.Echo ""
 WScript.Echo " Operation:", t_Object.Operation
 WScript.Echo " Provider:", t_Object.ProviderName

 strDescr = t_Object.Description
 strPInfo = t_Object.ParameterInfo
 strCode = t_Object.StatusCode

 if (strDescr <> nothing) Then
  WScript.Echo " Description:", strDescr  
 end if

 if (strPInfo <> nothing) Then
  WScript.Echo " Parameter Info:", strPInfo  
 end if

 if (strCode <> nothing) Then
  WScript.Echo " Status:", strCode  
 end if

 WScript.Echo ""
 Err.Clear
 set t_Object2 = CreateObject("WbemScripting.SWbemLastError")
 if Err = 0 Then
    WScript.Echo "Got the error object again - this shouldn't have happened!" 
 Else
    Err.Clear
    WScript.Echo "Couldn't get last error again - as expected"
 End if
End If

```



Im folgenden Perl-Beispiel wird veranschaulicht, wie Fehler- und Fehlerobjektinformationen überprüft werden.


```
use strict;
use Win32::OLE;

my ( $t_Service, $t_Object, $t_Object2, $strDescr, $strPInfo, $strCode );

# Close STDERR file handle to eliminate redundant error message
close(STDERR);

# Ask for non-existent class to force error 
$t_Service = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default"); 
$t_Object = $t_Service->Get("Nosuchclass000");

if (defined $t_Object)
{
 print "Got a class\n"; 
}
else
{
 print "\nErr Information:\n\n";
 print Win32::OLE->LastError, "\n";

 # Create the last error object
 $t_Object = new Win32::OLE 'WbemScripting.SWbemLastError';
 print "\nWMI Last Error Information:\n\n";
 print " Operation: ", $t_Object->{Operation}, "\n";
 print " Provider: ", $t_Object->{ProviderName}, "\n";
 
 $strDescr = $t_Object->{Description};
 $strPInfo = $t_Object->{ParameterInfo};
 $strCode = $t_Object->{StatusCode};

 if (defined $strDescr)
 {
  print " Description: ", $strDescr, "\n";  
 }

 if (defined $strPInfo)
 {
  print " Parameter Info: ", $strPInfo, "\n";  
 }

 if (defined $strCode)
 {
  print " Status: ", $strCode, "\n";  
 }

 print "\n";

 $t_Object2 = new Win32::OLE 'WbemScripting.SWbemLastError';
 if (defined $t_Object2)
 {
  print "Got the error object again - this shouldn't have happened!\n";
 }
 else
 {
  print "Couldn't get last error again - as expected\n";
 }
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Skripterstellung für API-Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




