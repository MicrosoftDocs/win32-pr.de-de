---
description: Die Win32 \_ ClusterShare-Klasse stellt eine freigegebene Ressource in einem Cluster dar.
ms.assetid: 6c8b40e3-431f-4728-a389-affbc04b8415
ms.tgt_platform: multiple
title: Win32_ClusterShare-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare
- Win32_ClusterShare.Caption
- Win32_ClusterShare.Description
- Win32_ClusterShare.InstallDate
- Win32_ClusterShare.Status
- Win32_ClusterShare.AccessMask
- Win32_ClusterShare.AllowMaximum
- Win32_ClusterShare.MaximumAllowed
- Win32_ClusterShare.Name
- Win32_ClusterShare.Path
- Win32_ClusterShare.Type
- Win32_ClusterShare.ServerName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 66be06bf3a8433a7dba1eb28e6123adb03d622803745838158aa80bda0e8e594
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118417991"
---
# <a name="win32_clustershare-class"></a>Win32 \_ ClusterShare-Klasse

\[Die **Win32 \_ ClusterShare-Klasse** ist veraltet. Verwenden Sie stattdessen [**die \_ MSFT-Klassen FileShare**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) und [**MSFT \_ SMFileShare.**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare)\]

Die Win32 \_ ClusterShare-Klasse stellt eine freigegebene Ressource in einem Cluster dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_ClusterShare : Win32_Share
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
  string   ServerName;
};
```

## <a name="members"></a>Member

Die **Win32 \_ ClusterShare-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ ClusterShare-Klasse** verfügt über diese Methoden.



| Methode                                                    | BESCHREIBUNG                                                      |
|:----------------------------------------------------------|:-----------------------------------------------------------------|
| [**Erstellen**](create-win32-clustershare.md)               | Erstellt eine neue **Win32 \_ ClusterShare-Instanz.**<br/>       |
| [**Löschen**](delete-win32-clustershare.md)               | Löscht eine **Win32 \_ ClusterShare-Instanz.**<br/>           |
| [**GetAccessMask**](getaccessmask-win32-clustershare.md) | Gibt eine Bitmap mit den Zugriffsrechten für die Freigabe zurück.<br/> |
| [**SetShareInfo**](setshareinfo-win32-clustershare.md)   | Legt die Parameter der freigegebenen Ressource fest.<br/>           |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ ClusterShare-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Accessmask**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **VERALTET**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Diese Eigenschaft ist veraltet und wird nicht mehr verwendet. Verwenden Sie [**stattdessen die \_ Win32 Share.GetAccessMask-Methode.**](getaccessmask-method-in-class-win32-share.md) Der Wert der **AccessMask-Eigenschaft** wird von WMI **auf NULL** festgelegt. Weitere Informationen zum Festlegen des Zugriffs beim Erstellen einer Freigabe finden Sie unter [**Create-Methode.**](create-method-in-class-win32-share.md)

Diese Eigenschaft wird von [**Win32 Share \_ geerbt.**](win32-share.md)

</dd> <dt>

**AllowMaximum**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ max \_ uses")
</dt> </dl>

Die Anzahl gleichzeitiger Benutzer für diese Ressource wurde eingeschränkt. True **gibt an,** dass der Wert in **der MaximumAllowed-Eigenschaft** ignoriert wird.

Diese Eigenschaft wird von [**Win32 Share \_ geerbt.**](win32-share.md)

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Eine kurze Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
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

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Installation date")
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

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ max \_ uses")
</dt> </dl>

Begrenzen Sie die maximale Anzahl von Benutzern, die diese Ressource gleichzeitig verwenden dürfen. Der Wert ist nur gültig, wenn die **AllowMaximum-Eigenschaft** auf **FALSE festgelegt ist.**

Diese Eigenschaft wird von [**Win32 Share \_ geerbt.**](win32-share.md)

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1) \| shi1 \_ netname")
</dt> </dl>

Alias für einen Pfad, der als Freigabe auf einem Computersystem eingerichtet ist, auf dem Windows.

Windows 2008-Beispiel: \\ "SERVER01 \\ public" – Windows Server 2008 erfordert, dass Sie die UNC in den Namen eingeben.

Diese Eigenschaft wird von [**Win32 Share \_ geerbt.**](win32-share.md)

</dd> <dt>

**Path**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ path")
</dt> </dl>

Lokaler Pfad der Windows Freigabe.

Beispiel: "C: \\ Programme"

Diese Eigenschaft wird von [**Win32 Share \_ geerbt.**](win32-share.md)

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ServerName"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503) \| shi503 \_ servername")
</dt> </dl>

Der Clusterserver, auf dem die Freigabe gehostet wird.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
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

**Wird beendet** ("Wird beendet")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Striche** ("Strich")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("Kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Lost Comm** ("Lost Comm")


</dt> <dd></dd> </dl>

</dd> <dt>

**Typ**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ type")
</dt> </dl>

Der Typ der Ressource, die freigegeben wird. Folgende Typen sind möglich: Laufwerke, Druckwarteschlangen, prozessübergreifende Kommunikation (Interprocess Communications, IPC) und allgemeine Geräte.

Diese Eigenschaft wird von [**Win32 Share \_ geerbt.**](win32-share.md)

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

**Datenträgerlaufwerkadministrator** (2147483648)


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

**Druckwarteschlangenadministrator** (2147483649)


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

**Geräteadministrator** (2147483650)


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

**IPC Admin** (2147483651)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32-Freigabe \_**](win32-share.md)
</dt> </dl>

 

