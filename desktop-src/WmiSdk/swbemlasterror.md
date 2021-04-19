---
description: Die-Methoden und-Eigenschaften des-Objekts von "taubemlasterror" enthalten Fehler Objekte und bearbeiten diese.
ms.assetid: 11a652fa-29e8-437b-8e62-e28e56a8a38d
ms.tgt_platform: multiple
title: Taubemlasterror-Objekt (wbemdisp. h)
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
ms.openlocfilehash: a00d8e3421800acab7cc4958ddc1e6a75f101958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348885"
---
# <a name="swbemlasterror-object"></a>Taubemlasterror-Objekt

Die-Methoden und-Eigenschaften des-Objekts von " **taubemlasterror** " enthalten Fehler Objekte und bearbeiten diese. Die Methoden und Eigenschaften dieses Objekts sind identisch mit denen des WS [**-Objekts,**](swbemobject.md) werden jedoch verwendet, um Fehlerinformationen anstelle von WMI-Klassen Informationen zu enthalten. Dieses Objekt kann durch den VBScript-Befehl "up- **Object** " erstellt werden.

Sie können das Fehler Objekt " **taubemlasterror** " erstellen, um die erweiterten Fehlerinformationen zu überprüfen, die einem vorherigen Methoden Aufruftyp zugeordnet sind. Wenn keine Fehlerinformationen verfügbar sind, tritt beim Versuch, ein Fehler Objekt zu erstellen, ein Fehler auf. Wenn der-Vorgang erfolgreich ist und ein Fehler Objekt zurückgibt, wird der Status des Objekts zurückgesetzt. Weitere Versuche, ein Fehler Objekt abzurufen, schlagen fehl, bis ein neuer Fehler auftritt. Wenn Sie einen asynchronen-Rückruf ausführen, der fehlschlägt, kann ein " **slibemlasterror** "-Objekt vom Ereignis " [**slibemsink. onabgeschlossene**](swbemsink-oncompleted.md) " im Parameter " *objWbemErrorObject* " zurückgegeben werden.

## <a name="members"></a>Member

Das Objekt " **taubemlasterror** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **taubemlasterror** -Objekt verfügt über diese Methoden.



| Methode                                                   | BESCHREIBUNG                                                                                  |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| **ASSOCIATORS\_**                                        | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/> |
| **Associatorsasync\_**                                   | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/> |
| [**Klon\_**](swbemlasterror-clone-.md)                 | Erstellt eine Kopie des aktuellen-Objekts.<br/>                                               |
| [**CompareTo\_**](swbemlasterror-compareto-.md)         | Testet zwei-Objekte auf Gleichheit.<br/>                                                   |
| **Lösch\_**                                             | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/> |
| **DeleteAsync\_**                                        | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/> |
| **ExecMethod\_**                                         | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/> |
| **ExecMethodAsync\_**                                    | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/> |
| [**Getobjecttext\_**](swbemlasterror-getobjecttext-.md) | Ruft die Textdarstellung des-Objekts ab, das mit der MOF-Syntax geschrieben wurde.<br/>       |
| **Instanzen\_**                                          | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/> |
| **Instancesasync\_**                                     | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/> |
| **Stellte\_**                                                | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/> |
| **Putasync\_**                                           | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/> |
| **References\_**                                         | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/> |
| **Referencesasync\_**                                    | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/> |
| **SpawnDerivedClass\_**                                  | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/> |
| **SpawnInstance\_**                                      | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/> |
| **Unterklassen von  werden erstellt.\_**                                         | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/> |
| **Subclassesasync\_**                                    | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **taubemlasterror** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                      | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                   |
|:--------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ableitung\_**<br/>                                   | Schreibgeschützt<br/> | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/>                                                                  |
| **Methoden\_** <br/>                                     | Schreibgeschützt<br/> | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/>                                                                  |
| [**ADS\_**](swbemlasterror-path-.md)<br/>             | Schreibgeschützt<br/> | Enthält ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt, das den Objekt Pfad der aktuellen Klasse oder Instanz darstellt.<br/>                    |
| [**Eigenschaften\_**](swbemlasterror-properties-.md)<br/> | Schreibgeschützt<br/> | Stellt die Auflistung von Eigenschaften des-Objekts von " **Swap LastError** " dar. Bei dieser Eigenschaft handelt es sich um ein Objekt vom [**typaustausch**](swbempropertyset.md) .<br/> |
| **Qualifikation\_**<br/>                                   | Schreibgeschützt<br/> | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/>                                                                  |
| **Sicherheit\_**<br/>                                     | Schreibgeschützt<br/> | Nicht verwendet. Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.<br/>                                                                  |



 

## <a name="examples"></a>Beispiele

Das folgende VBScript-Beispiel veranschaulicht, wie Fehler-und Fehler Objektinformationen überprüft werden.


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



Das folgende perl-Beispiel veranschaulicht, wie Fehler-und Fehler Objektinformationen überprüft werden.


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
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austausch Fehler<br/>                                                        |
| IID<br/>                      | IID \_ iswbemlasterror<br/>                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




