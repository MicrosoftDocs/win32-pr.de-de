---
description: Stellt Einstellungsdaten für eine virtuelle Festplatte bereit.
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
ms.openlocfilehash: 6e13efbb068d15ca4051995e7d9f317eb2ccacab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128409"
---
# <a name="msvm_virtualharddisksettingdata-class"></a>MSVM \_ virtualharddisksettingdata-Klasse

Stellt Einstellungsdaten für eine virtuelle Festplatte bereit.

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

Die **MSVM \_ virtualharddisksettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ virtualharddisksettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**BlockSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die von der virtuellen Festplatte verwendete Blockgröße in Bytes.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Einstellungen für die Festplatte der virtuellen Festplatte" festgelegt.

</dd> <dt>

**Dataalignment**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt die gewünschte Ausrichtung (in Bytes) für die Daten Nutzlast des virtuellen Datenträgers an.

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Festlegen von Daten für eine virtuelle Festplatte" festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Format**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Das Format für die virtuelle Festplatte. Dabei handelt es sich um einen der folgenden Werte.

<dt>

<span id="VHD"></span><span id="vhd"></span>

<span id="VHD"></span><span id="vhd"></span>**VHD** (2)


</dt> <dd></dd> <dt>

<span id="VHDX"></span><span id="vhdx"></span>

<span id="VHDX"></span><span id="vhdx"></span>**Vhdx** (3)


</dt> <dd></dd> <dt>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**Vhdset** (4)


</dt> <dd>

> [!Note]  
> In Windows 10 und Windows Server 2016 hinzugefügt.

 

</dd> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.

</dd> <dt>

**Ispmemcompatible**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der virtuelle Datenträger als Sicherungs Speicher für ein dauerhaftes Speichergerät verwendet werden kann.

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

</dd> <dt>

**Logicalsector size**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die von der virtuellen Festplatte verwendete logische Sektorgröße in Bytes.

</dd> <dt>

**MaxInternalSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die maximale Größe der virtuellen Festplatte, die vom virtuellen Computer angezeigt werden kann (in Bytes). Diese Größe wird auf das nächstgrößte Vielfache der Sektorgröße aufgerundet.

</dd> <dt>

**Parametifizierer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der GUID, der verwendet wird, um das übergeordnete Element der virtuellen Festplatte eindeutig zu identifizieren. Wenn die virtuelle Festplatte nicht über ein übergeordnetes Element verfügt, ist dieses Feld leer.

> [!Note]  
> In Windows 10 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**ParentPath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Das übergeordnete Element der virtuellen Festplatte. Wenn die virtuelle Festplatte nicht über ein übergeordnetes Element verfügt, ist diese Eigenschaft leer.

</dd> <dt>

**"Parametritimestamp"**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitstempel des übergeordneten Elements der virtuellen Festplatte. Wenn die virtuelle Festplatte nicht über ein übergeordnetes Element verfügt, ist dieses Feld leer.

> [!Note]  
> In Windows 10 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**Pfad**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der voll qualifizierte Pfad der virtuellen Festplatte.

</dd> <dt>

**Physicalsector size**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die physische Sektorgröße, die von der virtuellen Festplatte verwendet wird (in Bytes).

</dd> <dt>

**Pmemaddressabstractiontype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die für diese virtuelle Festplatte zu verwendende persistente Speicher Adress Abstraktion-Methode.

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

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

**Type**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Typ der virtuellen Festplatte. Dabei handelt es sich um einen der folgenden Werte.

<dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

**Korrigiert** (2)


</dt> <dd></dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>

**Dynamisch** (3)


</dt> <dd></dd> <dt>

<span id="Differencing"></span><span id="differencing"></span><span id="DIFFERENCING"></span>

**Differenzierung** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualDiskId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die GUID, die zur eindeutigen Identifizierung des virtuellen Datenträgers verwendet wird.

Wenn die [**MSVM-Methode " \_ imagemanagementservice. getvirtualharddisksettingdata**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) " eine Instanz von " **MSVM \_ virtualharddisksettingdata**" zurückgibt, kann der Client diese Eigenschaft verwenden, um die eindeutige Datenträger-ID der virtuellen Festplatte zu erhalten.

Bei der Konflikterkennung kann ein Client den **virtualdiskid** -Wert auf eine neue GUID festlegen und diese **MSVM \_ virtualharddisksettingdata** -Instanz an die [**MSVM \_ imagemanagementservice. setvirtualharddisksettingdata**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) -Methode übergeben, um die Datenträger-ID der virtuellen Festplatte zu ändern. Wenn es sich bei der VHD nicht um eine vhdx-VHD handelt oder wenn die VHD angefügt ist, schlägt der Vorgang fehl. Der Vorgang schlägt auch fehl, wenn der bestandene Wert falsch formatiert ist, d. h. keine GUID ist oder alle 0s enthält. Der Vorgang wird im Hintergrund erfolgreich ausgeführt, wenn der bestandene Wert mit der aktuellen Datenträger-ID identisch ist.

Fehler, die von der Funktion " [**setvirtualdiskinformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) " generiert werden, werden über diese Eigenschaft aufgehotet. Ein Client kann auch denselben Mechanismus verwenden, um den **virtualdiskid** -Wert bei der VHD-Erstellung über die [**MSVM \_ imagemanagementservice. kreatevirtualharddisk**](createvirtualharddisk-msvm-imagemanagementservice.md) -Methode im gleichen Namespace bereitzustellen. Dies kann zum Erstellen von VHD1-oder VHD2-VHDs verwendet werden.

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**Getvirtualharddisksettingdata**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)
</dt> </dl>

 

