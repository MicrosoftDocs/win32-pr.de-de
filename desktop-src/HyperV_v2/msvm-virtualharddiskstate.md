---
description: Stellt Zustandsinformationen für ein vorhandenes virtuelles Festplatten Abbild bereit.
ms.assetid: b0177906-71dc-4be8-b351-97d7ef427acd
title: Msvm_VirtualHardDiskState-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskState
- Msvm_VirtualHardDiskState.FileSize
- Msvm_VirtualHardDiskState.InUse
- Msvm_VirtualHardDiskState.MinInternalSize
- Msvm_VirtualHardDiskState.PhysicalSectorSize
- Msvm_VirtualHardDiskState.Alignment
- Msvm_VirtualHardDiskState.FragmentationPercentage
- Msvm_VirtualHardDiskState.Timestamp
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 15d0a8b150e83c17946a6d1b66c7086383f08466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484355"
---
# <a name="msvm_virtualharddiskstate-class"></a>MSVM \_ virtualharddiskstate-Klasse

Stellt Zustandsinformationen für ein vorhandenes virtuelles Festplatten Abbild bereit.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskState
{
  uint64   FileSize;
  boolean  InUse;
  uint64   MinInternalSize;
  uint32   PhysicalSectorSize;
  uint32   Alignment;
  uint32   FragmentationPercentage;
  DATETIME Timestamp;
};
```

## <a name="members"></a>Member

Die Klasse " **MSVM \_ virtualharddiskstate** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ virtualharddiskstate** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Ausrichtung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ der Ausrichtung der virtuellen Festplatte an. Dabei handelt es sich um einen der folgenden Werte.



| Wert                                                                        | Bedeutung                        |
|------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>0</dt> </dl> | 512-Byte-Ausrichtung.<br/> |
| <dl> <dt>1</dt> </dl> | 4-KB-Ausrichtung.<br/>     |



 

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Größe der virtuellen Festplatten Datei (die tatsächliche Menge an Speicher, die von der Datei belegt wird) in Bytes.

</dd> <dt>

**Fragmentationprozentsatz**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Näherungswert für den Prozentsatz der virtuellen Festplattenblöcke, die in der virtuellen Festplatten Datei fragmentiert sind.

</dd> <dt>

**Derzeit verwendeten**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft ist für eine spätere Verwendung vorgesehen.

</dd> <dt>

**Mininternalsize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die minimale Größe, auf die die virtuelle Festplatte verkleinert werden kann (in Bytes). Diese Größe wird auf das nächstgrößte Vielfache der Sektorgröße aufgerundet.

</dd> <dt>

**Physicalsector size**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die physische Sektorgröße, die vom zugrunde liegenden physischen Datenträger verwendet wird (in Bytes).

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitstempel der virtuellen Festplatte

> [!Note]  
> In Windows 10 und Windows Server 2016 hinzugefügt.

 

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

[**Getvirtualharddiskstate**](getvirtualharddiskstate-msvm-imagemanagementservice.md)
</dt> </dl>

 

 




