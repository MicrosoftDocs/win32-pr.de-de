---
description: Verwenden Sie die Methoden und Eigenschaften des Objekts "errbemubjectpath", um einen Objekt Pfad zu erstellen und zu überprüfen. Dieses Objekt kann durch den VBScript-Befehl "up-Object" erstellt werden.
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.tgt_platform: multiple
title: Errbemubjectpath-Objekt (wbemdisp. h)
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
ms.openlocfilehash: 1e6836cd58970f3667d8f629a678d55bec5185a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360164"
---
# <a name="swbemobjectpath-object"></a>Errbemubjectpath-Objekt

Verwenden Sie die Methoden und Eigenschaften des Objekts " **errbemubjectpath** ", um einen Objekt Pfad zu erstellen und zu überprüfen. Dieses Objekt kann durch den VBScript-Befehl "up- **Object** " erstellt werden.

## <a name="members"></a>Member

Das Objekt " **errbeporbjectpath** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das Objekt " **errbemubjectpath** " verfügt über diese Methoden.



| Methode                                                   | BESCHREIBUNG                                                     |
|:---------------------------------------------------------|:----------------------------------------------------------------|
| [**-Klasse**](swbemobjectpath-setasclass.md)         | Erzwingt, dass der Pfad eine WMI-Klasse adressiert.<br/>              |
| [**"Ttassingleton"**](swbemobjectpath-setassingleton.md) | Erzwingt, dass der Pfad eine Singleton-WMI-Instanz adressiert.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das Objekt " **errbemubjectpath** " verfügt über diese Eigenschaften.



| Eigenschaft                                                              | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                          |
|:----------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autoritative Stelle**](swbemobjectpath-authority.md)<br/>             | Lesen/Schreiben<br/> | Eine Zeichenfolge, die die Autoritäts Komponente des Objekt Pfads definiert.<br/>                                                                                                           |
| [**Klasse**](swbemobjectpath-class.md)<br/>                     | Lesen/Schreiben<br/> | Der Name der Klasse, die Teil des Objekt Pfads ist.<br/>                                                                                                                        |
| [**DisplayName**](swbemobjectpath-displayname.md)<br/>         | Lesen/Schreiben<br/> | Eine Zeichenfolge, die den Pfad in einem Formular enthält, das als Moniker-Anzeige Name verwendet werden kann. Siehe [Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md).<br/> |
| [**IsClass**](swbemobjectpath-isclass.md)<br/>                 | Schreibgeschützt<br/>  | Boolescher Wert, der angibt, ob dieser Pfad eine Klasse darstellt. Dies entspricht der Eigenschaft " [ \_ \_ Eigenschaft" in der com](wmi-system-properties.md) -API.<br/>                    |
| [**IsSingleton**](swbemobjectpath-issingleton.md)<br/>         | Schreibgeschützt<br/>  | Boolescher Wert, der angibt, ob dieser Pfad eine Singleton-Instanz darstellt.<br/>                                                                                                |
| [**Schlüssel**](swbemobjectpath-keys.md)<br/>                       | Schreibgeschützt<br/>  | Ein [**-**](swbemnamedvalueset.md) Objekt, das die Schlüsselwert Bindungen enthält.<br/>                                                                          |
| [**Gebietsschema**](swbemobjectpath-locale.md)<br/>                   | Lesen/Schreiben<br/> | Eine Zeichenfolge, die das Gebiets Schema für diesen Objekt Pfad enthält.<br/>                                                                                                                     |
| [**Namespace**](swbemobjectpath-namespace.md)<br/>             | Lesen/Schreiben<br/> | Der Name des Namespace, der Teil des Objekt Pfads ist. Dies entspricht der [ \_ \_ Namespace](wmi-system-properties.md) -Eigenschaft in der com-API.<br/>                        |
| [**Namespace**](swbemobjectpath-parentnamespace.md)<br/> | Schreibgeschützt<br/>  | Der Name des übergeordneten Elements des Namespace, der Teil des Objekt Pfads ist.<br/>                                                                                                      |
| [**ADS**](swbemobjectpath-path.md)<br/>                       | Lesen/Schreiben<br/> | Enthält den absoluten Pfad. Dies entspricht der Eigenschaft [ \_ \_ path](wmi-system-properties.md) System in der com-API. Dies ist die Standard Eigenschaft dieses Objekts.<br/>    |
| [**RelPath**](swbemobjectpath-relpath.md)<br/>                 | Lesen/Schreiben<br/> | Enthält den relativen Pfad. Dies entspricht der Eigenschaft " [ \_ \_ RelPath](wmi-system-properties.md) System" in der com-API.<br/>                                              |
| [**Sicherheit\_**](swbemobjectpath-security-.md)<br/>            | Schreibgeschützt<br/>  | Wird verwendet, um die Sicherheitseinstellungen zu lesen oder zu ändern.<br/>                                                                                                                             |
| [**Servers**](swbemobjectpath-server.md)<br/>                   | Lesen/Schreiben<br/> | Name des Servers. Dies entspricht der [ \_ \_ Server](wmi-system-properties.md) System Eigenschaft in der com-API.<br/>                                                       |



 

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Objekt Pfade erstellt werden.


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



Im folgenden perl-Codebeispiel wird veranschaulicht, wie Objekt Pfade erstellt werden.


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
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Austausch Pfad<br/>                                                       |
| IID<br/>                      | IID \_ iswbemubjectpath<br/>                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




