---
description: Ein "taubemprivilegeset"-Objekt ist eine Sammlung von "taubemprivilege"-Objekten in einem "Swap Security"-Objekt, das bestimmte Berechtigungen für ein Windows-Verwaltungsinstrumentation (WMI)-Objekt anfordert.
ms.assetid: 073cf2d4-f7ee-45a6-8fa6-ca77a4870346
ms.tgt_platform: multiple
title: Taubemprivilegeset-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet
- ISWbemPrivilegeSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b2946f8b1f745c0db123ed33dab312cbbe9d16c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344719"
---
# <a name="swbemprivilegeset-object"></a>Swap-Objekt

Ein " **taubemprivilegeset** "-Objekt ist eine Sammlung von " [**taubemprivilege**](swbemprivilege.md) "-Objekten in einem " [**Swap Security**](swbemsecurity.md) "-Objekt, das bestimmte Berechtigungen für ein Windows-Verwaltungsinstrumentation (WMI)-Objekt anfordert. Weitere Informationen finden Sie in der Liste der Berechtigungen unter [**Berechtigungs Konstanten**](privilege-constants.md). Der Auflistung werden Elemente mithilfe der [**Add**](swbemprivilegeset-add.md) -Methode und der [**addasstring**](swbemprivilegeset-addasstring.md) -Methode hinzugefügt. Elemente werden mithilfe der- [**Element**](swbemprivilegeset-item.md) Methode aus der-Auflistung abgerufen und mithilfe der [**Remove**](swbemprivilegeset-remove.md) -Methode entfernt. Dieses Objekt kann nicht durch den VBScript-Methoden aufgerufene " [samateobject](/previous-versions//xzysf6hc(v=vs.85)) " erstellt werden. Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).

Ein-Objekt vom typ' **Swap** ' ist ein Satz von Berechtigungs Überschreibungs Anforderungen für ein bestimmtes Objekt. Wenn ein API-Befehl mit diesem-Objekt ausgeführt wird, werden die Anforderungen zur außer Kraft Setzung von Berechtigungen versucht. Das Objekt " **taubemprivilegeset** " definiert nicht die für den aktuellen Benutzer oder den aktuellen Prozess verfügbaren Berechtigungen. Anders ausgedrückt: durch das Abrufen der Berechtigungen für ein WMI-Objekt werden nicht die Berechtigungseinstellungen identifiziert, die für die Verbindung mit WMI hergestellt werden, oder die Berechtigungen, die beim Übermitteln eines Objekts an eine Senke wirksam werden.

## <a name="members"></a>Member

Das Objekt " **taubemprivilegeset** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **taubemprivilegeset** -Objekt verfügt über diese Methoden.



| Methode                                               | BESCHREIBUNG                                                                                                                                                             |
|:-----------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eren**](swbemprivilegeset-add.md)                 | Fügt der **slibemprivilegeset** -Auflistung mithilfe einer [wbemprivilegeenum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) -Konstante ein " [**slibemprivilege**](swbemprivilege.md) "-Objekt hinzu.<br/> |
| [**Addasstring**](swbemprivilegeset-addasstring.md) | Fügt der-Auflistung von " **taubemprivilegeset** " mithilfe einer Berechtigungs Zeichenfolge ein "" [**-Objekt "**](swbemprivilege.md) ".<br/>                                    |
| [**DeleteAll**](swbemprivilegeset-deleteall.md)     | Löscht alle Berechtigungen aus der Auflistung.<br/>                                                                                                              |
| [**Element**](swbemprivilegeset-item.md)               | Ruft [**ein-**](swbemprivilege.md) Objekt aus der-Auflistung ab. Dies ist die Standardmethode dieses Objekts.<br/>                                 |
| [**Aufgeh**](swbemprivilegeset-remove.md)           | Entfernt ein [**-**](swbemprivilege.md) Objekt aus der Auflistung.<br/>                                                                              |



 

### <a name="properties"></a>Eigenschaften

Das Objekt " **taubemprivilegeset** " verfügt über diese Eigenschaften.



| Eigenschaft                                            | Zugriffstyp          | BESCHREIBUNG                                       |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Countdown**](swbemprivilegeset-count.md)<br/> | Schreibgeschützt<br/> | Die Anzahl der Elemente in der Auflistung.<br/> |



 

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird ein Objekt vom Typ "slibemprivileges" abgerufen, und der Auflistung werden alle verfügbaren Berechtigungen gemäß dem Wert hinzugefügt, wie in [**wbemprivilegeenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)definiert.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\cimv2")
set colPrivileges = objWMIService.Security_.Privileges
For I = 1 To 27
colPrivileges.Add(I)
Next
' Display information about each privilege 
For Each objItem In colPrivileges
wscript.echo objItem.Identifier & vbtab & objItem.Name _
    & vbtab & objItem.Displayname _
    & vbtab & "Enabled = " & objItem.IsEnabled
Next
```



Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Berechtigungen mithilfe des-Objekts von " **Swap** " hinzugefügt werden.


```VB
on error resume next

const wbemPrivilegeSecurity = 8
const wbemPrivilegeDebug = 20

set locator = CreateObject("WbemScripting.SWbemLocator")

' Add a single privilege using SWbemPrivilegeSet.Add

locator.Security_.Privileges.Add wbemPrivilegeSecurity 
Set Privilege = locator.Security_.Privileges(wbemPrivilegeSecurity)
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
locator.Security_.Privileges.Add 6535
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

locator.Security_.Privileges.Add wbemPrivilegeDebug 

locator.Security_.Privileges(wbemPrivilegeDebug).IsEnabled = false

' Add a single privilege using SWbemPrivilegeSet.AddAsString

Set Privilege = locator.Security_.Privileges.AddAsString ("SeChangeNotifyPrivilege")
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
locator.Security_.Privileges.AddAsString "SeChungeNotifyPrivilege"
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

WScript.Echo ""
for each Privilege in locator.Security_.Privileges
 WScript.Echo "[" & Privilege.DisplayName & "]", Privilege.Identifier, Privilege.Name, Privilege.IsEnabled
next

if err <> 0 then
 WScript.Echo Err.Number, Err.Description, Err.Source
end if 
```



Im folgenden perl-Codebeispiel wird das Hinzufügen von Berechtigungen mithilfe des-Objekts " **Swap** " veranschaulicht.


```
use strict;
use Win32::OLE;

close(STDERR);

my ($locator, $Privilege);
my $wbemPrivilegeSecurity = 8;
my $wbemPrivilegeDebug = 20;

eval { $locator = new Win32::OLE 'WbemScripting.SWbemLocator';};

if (!$@ && defined $locator)
{
 # Add a single privilege using SWbemPrivilegeSet.Add
 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeSecurity);
 $Privilege = $locator->{Security_}->Privileges($wbemPrivilegeSecurity);
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
 eval { $locator->{Security_}->{Privileges}->Add(6535); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);

 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeDebug); 
 $locator->{Security_}->Privileges($wbemPrivilegeDebug)->{IsEnabled} = 0;

 # Add a single privilege using SWbemPrivilegeSet.AddAsString
 $Privilege = $locator->{Security_}->{Privileges}->AddAsString ("SeChangeNotifyPrivilege");
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
 eval {$locator->{Security_}->{Privileges}->AddAsString ("SeChungeNotifyPrivilege"); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);
 print "\n";

 foreach $Privilege (in {$locator->{Security_}->{Privileges}})
 {
  printf "[%s] %d %s %d \n" , $Privilege->{DisplayName}, $Privilege->{Identifier}, $Privilege->{Name}, $Privilege->{IsEnabled};
 }
}
else
{
 print Win32::OLE->LastError, "\n";
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
| CLSID<br/>                    | CLSID- \_ Swap-taubemprivilegeset<br/>                                                     |
| IID<br/>                      | IID \_ iswbemprivilegeset<br/>                                                      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ausführen privilegierter Vorgänge](executing-privileged-operations.md)
</dt> <dt>

[Ausführen privilegierter Vorgänge mit VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[Wbemprivilegeumum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> <dt>

[**Berechtigungs Konstanten**](privilege-constants.md)
</dt> </dl>

 

