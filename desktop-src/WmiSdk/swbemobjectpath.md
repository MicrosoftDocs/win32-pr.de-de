---
description: Verwenden Sie die Methoden und Eigenschaften des SWbemObjectPath-Objekts, um einen Objektpfad zu erstellen und zu überprüfen. Dieses Objekt kann durch den VBScript CreateObject-Aufruf erstellt werden.
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.tgt_platform: multiple
title: SWbemObjectPath-Objekt (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath
- ISWbemObjectPath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2d7273b39c5cdccea7e46a077c925247846cd9ca255fc1dba20a95aeb159b773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313549"
---
# <a name="swbemobjectpath-object"></a>SWbemObjectPath-Objekt

Verwenden Sie die Methoden und Eigenschaften des **SWbemObjectPath-Objekts,** um einen Objektpfad zu erstellen und zu überprüfen. Dieses Objekt kann durch den VBScript **CreateObject-Aufruf erstellt** werden.

## <a name="members"></a>Member

Das **SWbemObjectPath-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **SWbemObjectPath-Objekt** verfügt über diese Methoden.



| Methode                                                   | Beschreibung                                                     |
|:---------------------------------------------------------|:----------------------------------------------------------------|
| [**SetAsClass**](swbemobjectpath-setasclass.md)         | Erzwingt, dass der Pfad eine WMI-Klasse adressiert.<br/>              |
| [**SetAsSingleton**](swbemobjectpath-setassingleton.md) | Erzwingt, dass der Pfad eine Singleton-WMI-Instanz adressiert.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **SWbemObjectPath-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                              | Zugriffstyp           | Beschreibung                                                                                                                                                                          |
|:----------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Behörde**](swbemobjectpath-authority.md)<br/>             | Lesen/Schreiben<br/> | Eine Zeichenfolge, die die Authority-Komponente des Objektpfads definiert.<br/>                                                                                                           |
| [**Klasse**](swbemobjectpath-class.md)<br/>                     | Lesen/Schreiben<br/> | Name der Klasse, die Teil des Objektpfads ist.<br/>                                                                                                                        |
| [**DisplayName**](swbemobjectpath-displayname.md)<br/>         | Lesen/Schreiben<br/> | Eine Zeichenfolge, die den Pfad in einem Formular enthält, das als Monikeranzeigename verwendet werden kann. Weitere Informationen [finden Sie unter Erstellen einer WMI-Anwendung oder eines Skripts.](creating-a-wmi-application-or-script.md)<br/> |
| [**IsClass**](swbemobjectpath-isclass.md)<br/>                 | Schreibgeschützt<br/>  | Boolescher Wert, der angibt, ob dieser Pfad eine Klasse darstellt. Dies entspricht der [ \_ \_ Eigenschaft "Property"](wmi-system-properties.md) in der COM-API.<br/>                    |
| [**IsSingleton**](swbemobjectpath-issingleton.md)<br/>         | Schreibgeschützt<br/>  | Boolescher Wert, der angibt, ob dieser Pfad eine Singletoninstanz darstellt.<br/>                                                                                                |
| [**Schlüssel**](swbemobjectpath-keys.md)<br/>                       | Schreibgeschützt<br/>  | Ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) das die Schlüsselwertbindungen enthält.<br/>                                                                          |
| [**Gebietsschema**](swbemobjectpath-locale.md)<br/>                   | Lesen/Schreiben<br/> | Eine Zeichenfolge, die das -Locale für diesen Objektpfad enthält.<br/>                                                                                                                     |
| [**Namespace**](swbemobjectpath-namespace.md)<br/>             | Lesen/Schreiben<br/> | Der Name des Namespace, der Teil des Objektpfads ist. Dies ist identisch mit der [ \_ \_ Namespace-Eigenschaft](wmi-system-properties.md) in der COM-API.<br/>                        |
| [**ParentNamespace**](swbemobjectpath-parentnamespace.md)<br/> | Schreibgeschützt<br/>  | Der Name des übergeordneten Elements des Namespace, der Teil des Objektpfads ist.<br/>                                                                                                      |
| [**Pfad**](swbemobjectpath-path.md)<br/>                       | Lesen/Schreiben<br/> | Enthält den absoluten Pfad. Dies ist identisch mit der [ \_ \_ Path-Systemeigenschaft](wmi-system-properties.md) in der COM-API. Dies ist die Standardeigenschaft dieses Objekts.<br/>    |
| [**Relpath**](swbemobjectpath-relpath.md)<br/>                 | Lesen/Schreiben<br/> | Enthält den relativen Pfad. Dies ist identisch mit der [ \_ \_ Relpath-Systemeigenschaft](wmi-system-properties.md) in der COM-API.<br/>                                              |
| [**Sicherheit\_**](swbemobjectpath-security-.md)<br/>            | Schreibgeschützt<br/>  | Wird zum Lesen oder Ändern der Sicherheitseinstellungen verwendet.<br/>                                                                                                                             |
| [**Server**](swbemobjectpath-server.md)<br/>                   | Lesen/Schreiben<br/> | Name des Servers. Dies ist identisch mit der [ \_ \_ Server-Systemeigenschaft](wmi-system-properties.md) in der COM-API.<br/>                                                       |



 

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Objektpfade erstellt werden.


```VB
on error resume next 
Set ObjectPath = CreateObject("WbemScripting.SWbemObjectPath")
ObjectPath.Server = "dingle"
ObjectPath.Namespace = "root/default/something"
ObjectPath.Class = "ho"
ObjectPath.Keys.Add "fred1", 10
ObjectPath.Keys.Add "fred2", -34
ObjectPath.Keys.Add "fred3", 65234654
ObjectPath.Keys.Add "fred4", "Wahaay"
ObjectPath.Keys.Add "fred5", -786186777

if err <> 0 then 
 WScript.Echo err.number
end if 

WScript.Echo "Pass 1:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.ImpersonationLevel = 3

WScript.Echo "Pass 2:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.AuthenticationLevel = 5

WScript.Echo "Pass 3:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

Set Privileges = ObjectPath.Security_.Privileges
if err <> 0 then
 WScript.Echo Hex(Err.Number), Err.Description
end if
Privileges.Add 8
Privileges.Add 20, false

WScript.Echo "Pass 4:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.DisplayName = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah"

WScript.Echo "Pass 5:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""
```



Im folgenden Perl-Codebeispiel wird veranschaulicht, wie Objektpfade erstellt werden.


```
use strict;
use Win32::OLE;
use constant FALSE=>"false";

my ( $ObjectPath, $Privileges );

eval { $ObjectPath = new Win32::OLE 'WbemScripting.SWbemObjectPath'; };
unless($@)
{
 eval
 {
  $ObjectPath->{Server} = "dingle";
  $ObjectPath->{Namespace} = "root/default/something";
  $ObjectPath->{Class} = "ho";
  $ObjectPath->{Keys}->Add("fred1", 10);
  $ObjectPath->{Keys}->Add("fred2", -34);
  $ObjectPath->{Keys}->Add("fred3", 65234654);
  $ObjectPath->{Keys}->Add("fred4", "Wahaay");
  $ObjectPath->{Keys}->Add("fred5", -786186777);
 };
 unless($@)
 {
  print "\n";
  print "Pass 1:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{ImpersonationLevel} = 3 ;

  print "Pass 2:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{AuthenticationLevel} = 5 ;

  print "Pass 3:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  eval { $Privileges = $ObjectPath->{Security_}->{Privileges}; };
  unless($@)
  {
   $Privileges->Add(8);
   $Privileges->Add(20,FALSE);

   print "Pass 4:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n\n";

   $ObjectPath->{DisplayName} = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah";

   print "Pass 5:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n";
  }
  else
  {
   print STDERR Win32::OLE->LastError, "\n";
  }
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
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
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Skripterstellung für API-Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




