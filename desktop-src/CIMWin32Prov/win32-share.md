---
description: Die Win32 \_ Share-Klasse stellt eine freigegebene Ressource auf einem Computersystem dar, auf dem Windows. Dies kann ein Laufwerk, ein Drucker, eine prozessübergreifende Kommunikation oder ein anderes sharable-Gerät sein. Weitere Informationen zum Abrufen von WMI-Klassen finden Sie unter Abrufen einer Klasse.
ms.assetid: 2d47b726-a0fe-47f3-9e96-d1d507655e56
ms.tgt_platform: multiple
title: Win32_Share-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share
- Win32_Share.Caption
- Win32_Share.Description
- Win32_Share.InstallDate
- Win32_Share.Status
- Win32_Share.AccessMask
- Win32_Share.AllowMaximum
- Win32_Share.MaximumAllowed
- Win32_Share.Name
- Win32_Share.Path
- Win32_Share.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 258116c3d6f01db938033056069aa036a3eaad23e44b31d80838ad26f570faa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117834152"
---
# <a name="win32_share-class"></a>Win32 \_ Share-Klasse

Die **Win32 \_ Share-Klasse** stellt eine freigegebene Ressource auf einem Computersystem dar, auf dem Windows. Dies kann ein Laufwerk, ein Drucker, eine prozessübergreifende Kommunikation oder ein anderes sharable-Gerät sein. Weitere Informationen zum Abrufen von WMI-Klassen finden Sie unter [Abrufen einer Klasse.](../wmisdk/retrieving-a-class.md)

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_Share : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  AllowMaximum;
  uint32   MaximumAllowed;
  string   Name;
  string   Path;
  uint32   Type;
};
```

## <a name="members"></a>Member

Die **Win32 \_ Share-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ Share-Klasse** verfügt über diese Methoden.



| Methode                                                             | Beschreibung                                                                                                                                                                                                         |
|:-------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Erstellen**](create-method-in-class-win32-share.md)               | Klassenmethode, die die Freigabe für eine Serverressource initiiert.<br/>                                                                                                                                               |
| [**Löschen**](delete-method-in-class-win32-share.md)               | Klassenmethode, die einen Freigabenamen aus der Liste der freigegebenen Ressourcen eines Servers löscht und verbindungen mit der freigegebenen Ressource trennt.<br/>                                                                       |
| [**GetAccessMask**](getaccessmask-method-in-class-win32-share.md) | Gibt die Zugriffsrechte für die Freigabe zurück, die von dem Benutzer oder der Gruppe gehalten werden, für den bzw. die die Instanz zurückgegeben wird. Sie sollten diese Methode statt der **AccessMask-Eigenschaft** verwenden, die immer **NULL ist.**<br/> |
| [**SetShareInfo**](setshareinfo-method-in-class-win32-share.md)   | Klassenmethode, die die Parameter einer freigegebenen Ressource festgelegt.<br/>                                                                                                                                              |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ Share-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Accessmask**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **VERALTET**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Diese Eigenschaft ist veraltet und wird nicht mehr verwendet. Verwenden Sie [**stattdessen die \_ Win32 Share.GetAccessMask-Methode.**](getaccessmask-method-in-class-win32-share.md) Der Wert der **AccessMask-Eigenschaft** wird von WMI **auf NULL** festgelegt. Weitere Informationen zum Festlegen des Zugriffs beim Erstellen einer Freigabe finden Sie unter [**Create-Methode.**](create-method-in-class-win32-share.md)

</dd> <dt>

**AllowMaximum**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ max \_ uses")
</dt> </dl>

Die Anzahl gleichzeitiger Benutzer für diese Ressource wurde eingeschränkt. True **gibt an,** dass der Wert in der **MaximumAllowed-Eigenschaft** ignoriert wird.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Eine kurze Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Eine Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Installation date")
</dt> </dl>

Gibt an, wann das Objekt installiert wurde. Das Fehlen eines Werts gibt nicht an, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**MaximumAllowed**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ max \_ uses")
</dt> </dl>

Begrenzen Sie die maximale Anzahl von Benutzern, die diese Ressource gleichzeitig verwenden dürfen. Der Wert ist nur gültig, wenn die **AllowMaximum-Eigenschaft** auf **FALSE festgelegt ist.**

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**schlüssel**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1) \| shi1 \_ netname")
</dt> </dl>

Alias für einen Pfad, der als Freigabe auf einem Computersystem eingerichtet ist, auf dem Windows.

Windows 2008: \\ "SERVER01 \\ public" – Windows Server 2008 erfordert, dass Sie die UNC in den Namen eingeben.

</dd> <dt>

**Path**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ path")
</dt> </dl>

Lokaler Pfad der Windows Freigabe.

Beispiel: "C: \\ Programme"

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Eine Zeichenfolge, die den aktuellen Status des Objekts angibt. Betriebsstatus und nicht betriebsbereiter Status können definiert werden. Der Betriebsstatus kann "OK", "Heruntergestuft" und "Fehler vor dem Ausfall" enthalten. "Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. B. eine SMART-fähige Festplatte).

Nicht betriebsbereite Status können "Error", "Starting", "Stopping" und "Service" sein. "Dienst" kann während der Spiegelung des Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen administrativen Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

Folgende Werte sind gültig:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Fehler** ("Fehler")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Heruntergestuft** ("Heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("Unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Wird** gestartet ("Wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Beenden** ("Wird beendet")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Mannslast** ("1000")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("Kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorenes Komma** ("Verlorenes Komma")


</dt> <dd></dd> </dl>

</dd> <dt>

**Typ**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Netzwerkverwaltungsstrukturen \| SHARE INFO \| [**\_ \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502-Typ") \_
</dt> </dl>

Typ der Ressource, die freigegeben wird. Zu den Typen gehören Datenträgerlaufwerke, Druckwarteschlangen, prozessübergreifende Kommunikation (Interprocess Communications, IPC) und allgemeine Geräte.

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**Laufwerk** (0)


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

**Druckwarteschlange** (1)


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

**Gerät** (2)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (3)


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

**Datenträgeradministrator** (2147483648)


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

**Druckwarteschlangenadministrator** (2147483649)


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

**Geräteadministrator** (2147483650)


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

**IPC-Administrator** (2147483651)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ Share-Klasse** wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.

Die Create-Methode in dieser Klasse ist eine statische Methode. Die Methoden **Delete,** **GetAccessMask** und **SetShareInfo** sind alle Instanzmethoden.

Abhängig von Ihren Sicherheitsberechtigungen können Sie möglicherweise nicht alle Eigenschaften dieser Klasse abrufen. Beispielsweise können die Eigenschaften **AllowMaximum,** **MaximumAllowed,** **Path** und **Type** NULL zurückgeben. Im Allgemeinen können Power Users und Administratoren alle Eigenschaftswerte abrufen.

## <a name="examples"></a>Beispiele

Im folgenden[Skriptcenter-Codebeispiel](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) werden alle Freigaben auf einem Computer und alle Freigabeberechtigungen für jede Freigabe aufgelistet.

Das PowerShell-Beispiel [Get Share Information similar to Win32 \_ Share](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) fragt Win32 Share ab \_ und stellt die Ergebnisse bereit.

Im folgenden PowerShell-Beispiel werden die Freigaben auf dem lokalen System angezeigt.


```PowerShell
$shares = Get-WMIObject -class Win32_share
"Shares on : {0}" -f $((gwmi win32_computersystem).name)
$shares | sort name | ft -auto
```



Wenn Sie genauer filtern möchten, können Sie alternativ den folgenden PowerShell-Codeausschnitt verwenden:


```PowerShell
gwmi -q "SELECT * FROM Win32_Share WHERE Name != 'ADMIN$' AND Name != 'IPC$'"
```



Im folgenden VBScript-Beispiel werden die Freigaben auf dem lokalen System angezeigt.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_Share")


For Each objItem in colItems 
 Wscript.Echo "Name: " & objItem.Name
 Wscript.Echo "Caption: " & objItem.Caption & "=" & objItem.Path
Next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> <dt>

[WMI-Aufgaben: Dateien und Ordner](../wmisdk/wmi-tasks--files-and-folders.md)
</dt> </dl>

 

 
