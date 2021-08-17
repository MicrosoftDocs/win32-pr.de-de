---
description: Stellt Einstellungsdaten für eine virtuelle Festplatte zur
ms.assetid: 492a0b81-86b2-4d7d-a118-6ec14e3971ed
title: Msvm_VirtualHardDiskSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskSettingData
- Msvm_VirtualHardDiskSettingData.InstanceID
- Msvm_VirtualHardDiskSettingData.Caption
- Msvm_VirtualHardDiskSettingData.Description
- Msvm_VirtualHardDiskSettingData.ElementName
- Msvm_VirtualHardDiskSettingData.Type
- Msvm_VirtualHardDiskSettingData.Format
- Msvm_VirtualHardDiskSettingData.Path
- Msvm_VirtualHardDiskSettingData.ParentPath
- Msvm_VirtualHardDiskSettingData.ParentTimestamp
- Msvm_VirtualHardDiskSettingData.ParentIdentifier
- Msvm_VirtualHardDiskSettingData.MaxInternalSize
- Msvm_VirtualHardDiskSettingData.BlockSize
- Msvm_VirtualHardDiskSettingData.LogicalSectorSize
- Msvm_VirtualHardDiskSettingData.PhysicalSectorSize
- Msvm_VirtualHardDiskSettingData.VirtualDiskId
- Msvm_VirtualHardDiskSettingData.DataAlignment
- Msvm_VirtualHardDiskSettingData.PmemAddressAbstractionType
- Msvm_VirtualHardDiskSettingData.IsPmemCompatible
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7f87ba072aaff03ab415ccabe803546a89192ecb1e28d85b628dd0655d47421
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068420"
---
# <a name="msvm_virtualharddisksettingdata-class"></a>Msvm \_ VirtualHardDiskSettingData-Klasse

Stellt Einstellungsdaten für eine virtuelle Festplatte zur

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Virtual Hard Disk Setting Data";
  string   Description = "Setting Data for a Virtual Hard Disk";
  string   ElementName;
  uint16   Type;
  uint16   Format;
  string   Path;
  string   ParentPath;
  DATETIME ParentTimestamp;
  string   ParentIdentifier;
  uint64   MaxInternalSize;
  uint32   BlockSize;
  uint32   LogicalSectorSize;
  uint32   PhysicalSectorSize;
  string   VirtualDiskId;
  uint64   DataAlignment;
  uint16   PmemAddressAbstractionType;
  boolean  IsPmemCompatible;
};
```

## <a name="members"></a>Member

Die **Msvm \_ VirtualHardDiskSettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ VirtualHardDiskSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Blöcke**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die von der virtuellen Festplatte verwendete Blockgröße in Bytes.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)und immer auf "Virtual Hard Disk Setting Data" festgelegt.

</dd> <dt>

**DataAlignment**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt die gewünschte Ausrichtung für die Datennutzlast des virtuellen Datenträgers in Bytes an.

> [!Note]  
> Hinzugefügt in Windows 10 Version 1709.

 

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)und immer auf "Setting Data for a Virtual Hard Disk" (Festlegen von Daten für eine virtuelle Festplatte) festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Format**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Das Format für die virtuelle Festplatte. Dies ist einer der folgenden Werte.

<dt>

<span id="VHD"></span><span id="vhd"></span>

<span id="VHD"></span><span id="vhd"></span>**VHD** (2)


</dt> <dd></dd> <dt>

<span id="VHDX"></span><span id="vhdx"></span>

<span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)


</dt> <dd></dd> <dt>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4)


</dt> <dd>

> [!Note]  
> Hinzugefügt in Windows 10 und Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ SettingData geerbt.**](/previous-versions//cc136911(v=vs.85))

</dd> <dt>

**IsPmemCompatible**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der virtuelle Datenträger als Hintergrundspeicher für ein persistentes Speichergerät verwendet werden kann.

> [!Note]  
> Hinzugefügt in Windows 10 Version 1709.

 

</dd> <dt>

**LogicalSectorSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die logische Sektorgröße, die von der virtuellen Festplatte in Bytes verwendet wird.

</dd> <dt>

**MaxInternalSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die maximale Größe der virtuellen Festplatte in Byte, die vom virtuellen Computer angezeigt werden kann. Diese Größe wird auf das nächstgrößerste Vielfache der Sektorgröße aufgerundet.

</dd> <dt>

**ParentIdentifier**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die GUID, mit der das übergeordnete Element der virtuellen Festplatte eindeutig identifiziert wird. Wenn die virtuelle Festplatte nicht über ein übergeordnetes Element verfügt, ist dieses Feld leer.

> [!Note]  
> Hinzugefügt in Windows 10 und Windows Server 2016.

 

</dd> <dt>

**ParentPath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Das übergeordnete Element der virtuellen Festplatte. Wenn die virtuelle Festplatte nicht über ein übergeordnetes Element verfügt, ist diese Eigenschaft leer.

</dd> <dt>

**ParentTimestamp**
</dt> <dd> <dl> <dt>

Datentyp: **DATETIME**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitstempel des übergeordneten Elements der virtuellen Festplatte. Wenn die virtuelle Festplatte nicht über ein übergeordnetes Element verfügt, ist dieses Feld leer.

> [!Note]  
> Hinzugefügt in Windows 10 und Windows Server 2016.

 

</dd> <dt>

**Path**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der vollqualifizierte Pfad der virtuellen Festplatte.

</dd> <dt>

**PhysicalSectorSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die von der virtuellen Festplatte verwendete physische Sektorgröße in Bytes.

</dd> <dt>

**PmemAddressAbstractionType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die persistente Speicheradressenabstraktionsmethode, die mit diesem virtuellen Datenträger verwendet werden soll.

> [!Note]  
> Hinzugefügt in Windows 10 Version 1709.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Keine** (0)


</dt> <dd></dd> <dt>

<span id="BTT"></span><span id="btt"></span>

**BTT** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Typ**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Typ der virtuellen Festplatte. Dies ist einer der folgenden Werte.

<dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

**Behoben** (2)


</dt> <dd></dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>

**Dynamisch** (3)


</dt> <dd></dd> <dt>

<span id="Differencing"></span><span id="differencing"></span><span id="DIFFERENCING"></span>

**Differenzieren** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualDiskId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die GUID, die verwendet wird, um den virtuellen Datenträger eindeutig zu identifizieren.

Wenn die [**Msvm \_ ImageManagementService.GetVirtualHardDiskSettingData-Methode**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) eine Instanz von **Msvm \_ VirtualHardDiskSettingData** zurückgibt, kann der Client diese Eigenschaft verwenden, um die eindeutige Datenträger-ID der VHD abzurufen.

Bei der Konflikterkennung oder auf andere Weise kann ein Client den **VirtualDiskId-Wert** auf eine neue GUID festlegen und diese **Msvm \_ VirtualHardDiskSettingData-Instanz** an die [**Methode Msvm \_ ImageManagementService.SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) übergeben, um die Datenträger-ID der VHD zu ändern. Wenn die VHD keine VHDX-VHD ist oder die VHD angefügt ist, schlägt der Vorgang fehl. Der Vorgang schlägt auch fehl, wenn der übergebene Wert falsch formatiert ist, d. h. keine GUID oder alle 0(e) hat. Der Vorgang wird automatisch erfolgreich ausgeführt, wenn der übergebene Wert mit der aktuellen Datenträger-ID identisch ist.

Fehler, die von der [**SetVirtualDiskInformation-Funktion**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) generiert werden, werden über diese Eigenschaft ausgelöst. Ein Client kann auch den gleichen Mechanismus verwenden, um den **VirtualDiskId-Wert** bei der VHD-Erstellung über die [**Msvm \_ ImageManagementService.CreateVirtualHardDisk-Methode**](createvirtualharddisk-msvm-imagemanagementservice.md) im gleichen Namespace bereitzustellen. Dies kann zum Erstellen von VHD1- oder VHD2-VHDs verwendet werden.

**Windows 8.1:** Dieser Wert wird erst Windows 8.1 und Windows Server 2012 R2 unterstützt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)
</dt> </dl>

 

