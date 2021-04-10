---
description: Die Win32- \_ Freigabe Klasse stellt eine freigegebene Ressource auf einem Computersystem dar, auf dem Windows ausgeführt wird. Hierbei kann es sich um ein Laufwerk, einen Drucker, eine prozessübergreifende Kommunikation oder ein anderes shardgerät handeln. Weitere Informationen zum Abrufen von WMI-Klassen finden Sie unter Abrufen einer Klasse.
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
ms.openlocfilehash: e871880da5aa9819de4a9eaaf3c6f074bd198d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127320"
---
# <a name="win32_share-class"></a>Win32- \_ Freigabe Klasse

Die **Win32- \_ Freigabe** Klasse stellt eine freigegebene Ressource auf einem Computersystem dar, auf dem Windows ausgeführt wird. Hierbei kann es sich um ein Laufwerk, einen Drucker, eine prozessübergreifende Kommunikation oder ein anderes shardgerät handeln. Weitere Informationen zum Abrufen von WMI-Klassen finden Sie unter [Abrufen einer Klasse](../wmisdk/retrieving-a-class.md).

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

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

Die **Win32- \_ Freigabe** Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32- \_ Freigabe** Klasse verfügt über diese Methoden.



| Methode                                                             | BESCHREIBUNG                                                                                                                                                                                                         |
|:-------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Stelle**](create-method-in-class-win32-share.md)               | Klassenmethode, die die Freigabe für eine Server Ressource initiiert.<br/>                                                                                                                                               |
| [**Lösch**](delete-method-in-class-win32-share.md)               | Class-Methode, die einen Freigabe Namen aus der Liste der freigegebenen Ressourcen eines Servers löscht, wobei Verbindungen mit der freigegebenen Ressource getrennt werden.<br/>                                                                       |
| [**Getaccessmask**](getaccessmask-method-in-class-win32-share.md) | Gibt die Zugriffsrechte für die Freigabe zurück, die der Benutzer oder die Gruppe hat, in dessen Namen die Instanz zurückgegeben wird. Sie sollten diese Methode anstelle der **AccessMask** -Eigenschaft verwenden, die immer **null** ist.<br/> |
| [**Setshareingefo**](setshareinfo-method-in-class-win32-share.md)   | Klassenmethode, mit der die Parameter einer freigegebenen Ressource festgelegt werden.<br/>                                                                                                                                              |



 

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ Freigabe** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Diese Eigenschaft ist veraltet und wird nicht mehr verwendet. Verwenden Sie stattdessen die Win32-Methode " [**\_ share. getaccessmask**](getaccessmask-method-in-class-win32-share.md) ". Der Wert der **AccessMask** -Eigenschaft wird von WMI auf **null** festgelegt. Weitere Informationen zum Festlegen des Zugriffs beim Erstellen einer Freigabe finden Sie unter der [**Create**](create-method-in-class-win32-share.md) -Methode.

</dd> <dt>

**AllowMaximum**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ Info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ uses")
</dt> </dl>

Die Anzahl von gleichzeitigen Benutzern für diese Ressource ist beschränkt. **True** gibt an, dass der Wert in der **MaximumAllowed** -Eigenschaft ignoriert wird.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Eine kurze Textbeschreibung des-Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Eine Textbeschreibung des-Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")
</dt> </dl>

Gibt an, wann das Objekt installiert wurde. Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**MaximumAllowed**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ Info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ uses")
</dt> </dl>

Limit für die maximale Anzahl von Benutzern, die diese Ressource gleichzeitig verwenden dürfen. Der Wert ist nur gültig, wenn die **AllowMaximum** -Eigenschaft auf **false** festgelegt ist.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ Info \_ 1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1) \| shi1 \_ NetName")
</dt> </dl>

Alias, der an einen Pfad übergeben wird, der als Freigabe auf einem Computersystem mit Windows eingerichtet ist.

Windows 2008-Beispiel: " \\ Server01 \\ Public"-Windows Server 2008 erfordert, dass Sie die UNC-Datei im Namen platzieren.

</dd> <dt>

**Pfad**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ Info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ path")
</dt> </dl>

Lokaler Pfad der Windows-Freigabe.

Beispiel: "C: \\ Programmdateien"

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Eine Zeichenfolge, die den aktuellen Status des Objekts angibt. Der Betriebsstatus und der nicht betriebliche Status können definiert werden. Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten. "Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).

Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten. "Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

Folgende Werte sind gültig:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Fehler** ("Fehler")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Herunter **gestuft ("** heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred-** Fehler ("pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

Wird **gestartet** ("wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

Wird **beendet ("wird angehalten** ")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Betont** ("gestresst")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Nicht wiederherstellen** ("nicht wiederherstellen")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorene** Kommunikations ("verlorene Kommunikations-")


</dt> <dd></dd> </dl>

</dd> <dt>

**Type**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ Info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Type")
</dt> </dl>

Der Typ der freigegebenen Ressource. Zu den Typen zählen: Laufwerke, Druck Warteschlangen, prozessübergreifende Kommunikation (prozessübergreifende Communications, IPC) und allgemeine Geräte.

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**Laufwerk (0** )


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

**Druck Warteschlange** (1)


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

**Gerät** (2)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (3)


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

**Laufwerks Administrator** (2147483648)


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

**Administrator der Druck Warteschlange** (2147483649)


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

**Geräte Administrator** (2147483650)


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

**IPC admin** (2147483651)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ Freigabe** Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.

Die Create-Methode in dieser Klasse ist eine statische Methode. Die Methoden **Delete**, **getaccessmask** und **setshareinfo** sind alle Instanzmethoden.

Abhängig von den Sicherheits Berechtigungen können Sie möglicherweise nicht alle Eigenschaften dieser Klasse abrufen. Beispielsweise können die Eigenschaften " **AllowMaximum**", " **MaximumAllowed**", " **path**" und " **Type** " NULL zurückgeben. Im Allgemeinen können Poweruser und Administratoren alle Eigenschaftswerte abrufen.

## <a name="examples"></a>Beispiele

Im folgenden Skript Center-[Codebeispiel](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) werden alle Freigaben auf einem Computer aufgelistet und alle Freigabe Berechtigungen für die einzelnen Freigaben aufgelistet.

Die [Informationen zur Freigabe von Freigabe Informationen ähnlich wie Win32 \_ share](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) PowerShell Sample Queries Win32 \_ share und liefert die Ergebnisse.

Im folgenden PowerShell-Beispiel werden die Freigaben auf dem lokalen System angezeigt.


```PowerShell
$shares = Get-WMIObject -class Win32_share
"Shares on : {0}" -f $((gwmi win32_computersystem).name)
$shares | sort name | ft -auto
```



Wenn Sie den Filter genauer filtern möchten, können Sie alternativ den folgenden PowerShell-Code Ausschnitt verwenden:


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
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> <dt>

[WMI-Tasks: Dateien und Ordner](../wmisdk/wmi-tasks--files-and-folders.md)
</dt> </dl>

 

 
