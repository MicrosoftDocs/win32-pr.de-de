---
description: Ein SWbemPrivilegeSet-Objekt ist eine Sammlung von SWbemPrivilege-Objekten in einem SWbemSecurity-Objekt, das bestimmte Berechtigungen für ein WMI-Objekt (Windows Management Instrumentation) an fordert.
ms.assetid: 073cf2d4-f7ee-45a6-8fa6-ca77a4870346
ms.tgt_platform: multiple
title: SWbemPrivilegeSet-Objekt (Wbemdisp.h)
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
ms.openlocfilehash: 2117aec6fada67bddce9f07a6c985c73a3dcd93ef217ed7fe77dc46cc5659d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991950"
---
# <a name="swbemprivilegeset-object"></a>SWbemPrivilegeSet-Objekt

Ein **SWbemPrivilegeSet-Objekt** ist eine Sammlung von [**SWbemPrivilege-Objekten**](swbemprivilege.md) in einem [**SWbemSecurity-Objekt,**](swbemsecurity.md) das bestimmte Berechtigungen für ein WMI-Objekt (Windows Management Instrumentation) an fordert. Weitere Informationen finden Sie in der Liste der Berechtigungen unter [**Privilege Constants**](privilege-constants.md). Elemente werden der Auflistung mithilfe der Methoden [**Add**](swbemprivilegeset-add.md) und [**AddAsString**](swbemprivilegeset-addasstring.md) hinzugefügt. Elemente werden mithilfe der [**Item-Methode**](swbemprivilegeset-item.md) aus der Auflistung abgerufen und mithilfe der [**Remove-Methode**](swbemprivilegeset-remove.md) entfernt. Dieses Objekt kann nicht durch den VBScript [CreateObject-Methodenaufruf](/previous-versions//xzysf6hc(v=vs.85)) erstellt werden. Weitere Informationen finden Sie unter [Zugreifen auf eine Auflistung.](accessing-a-collection.md)

Ein **SWbemPrivilegeSet-Objekt** ist ein Satz von Anforderungen zur Berechtigungsüberschreibung für ein bestimmtes Objekt. Wenn ein API-Aufruf mit diesem Objekt erfolgt, werden die Anforderungen zur Berechtigungsüberschreibung versucht. Das **SWbemPrivilegeSet-Objekt** definiert nicht die Berechtigungen, die dem aktuellen Benutzer oder Prozess zur Verfügung stehen. Anders ausgedrückt: Durch das Abrufen der Berechtigungen für ein WMI-Objekt werden weder die Berechtigungseinstellungen identifiziert, die für die Verbindung mit WMI vorgenommen werden, noch die Berechtigungen, die wirksam sind, wenn ein Objekt an eine Senke übermittelt wird.

## <a name="members"></a>Member

Das **SWbemPrivilegeSet-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **SWbemPrivilegeSet-Objekt** verfügt über diese Methoden.



| Methode                                               | Beschreibung                                                                                                                                                             |
|:-----------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Hinzufügen**](swbemprivilegeset-add.md)                 | Fügt der Sammlung **SWbemPrivilegeSet** mithilfe einer [WbemPrivilegeEnum-Konstante ein SWbemPrivilege-Objekt](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) hinzu. [](swbemprivilege.md)<br/> |
| [**AddAsString**](swbemprivilegeset-addasstring.md) | Fügt der [**Sammlung SWbemPrivilegeSet**](swbemprivilege.md) mithilfe einer Berechtigungszeichenfolge ein **SWbemPrivilege-Objekt** hinzu.<br/>                                    |
| [**DeleteAll**](swbemprivilegeset-deleteall.md)     | Löscht alle Berechtigungen aus der Auflistung.<br/>                                                                                                              |
| [**Element**](swbemprivilegeset-item.md)               | Ruft ein [**SWbemPrivilege-Objekt**](swbemprivilege.md) aus der Auflistung ab. Dies ist die Standardmethode dieses Objekts.<br/>                                 |
| [**Entfernen**](swbemprivilegeset-remove.md)           | Entfernt ein [**SWbemPrivilege-Objekt**](swbemprivilege.md) aus der Auflistung.<br/>                                                                              |



 

### <a name="properties"></a>Eigenschaften

Das **SWbemPrivilegeSet-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                            | Zugriffstyp          | Beschreibung                                       |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Anzahl**](swbemprivilegeset-count.md)<br/> | Schreibgeschützt<br/> | Die Anzahl der Elemente in der Auflistung.<br/> |



 

## <a name="examples"></a>Beispiele

Das folgende VBScript-Codebeispiel erhält ein SWbemPrivileges-Objekt und fügt der Sammlung alle verfügbaren Berechtigungen nach Berechtigungswert hinzu, wie in [**WbemPrivilegeEnum definiert.**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)


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



Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Berechtigungen mithilfe des **SWbemPrivilegeSet-Objekts hinzugefügt** werden.


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



Im folgenden Perl-Codebeispiel wird veranschaulicht, wie Berechtigungen mithilfe des **SWbemPrivilegeSet-Objekts hinzugefügt** werden.


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
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilegeSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemPrivilegeSet<br/>                                                      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Ausführen privilegierter Vorgänge](executing-privileged-operations.md)
</dt> <dt>

[Ausführen privilegierter Vorgänge mit VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[Skripterstellung für API-Objekte](scripting-api-objects.md)
</dt> <dt>

[**Berechtigungskonst constants**](privilege-constants.md)
</dt> </dl>

 

