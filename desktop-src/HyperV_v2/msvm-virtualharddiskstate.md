---
description: Stellt Statusinformationen für ein vorhandenes Image einer virtuellen Festplatte zur Verfügung.
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
ms.openlocfilehash: c5896e8b19d2897084997bd01b65bbb0d6e80e0ca15f662fff38871bdc0b6755
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426310"
---
# <a name="msvm_virtualharddiskstate-class"></a>Msvm \_ VirtualHardDiskState-Klasse

Stellt Statusinformationen für ein vorhandenes Image einer virtuellen Festplatte zur Verfügung.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **Msvm \_ VirtualHardDiskState-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ VirtualHardDiskState-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Ausrichtung**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Ausrichtungstyp der virtuellen Festplatte an. Dies ist einer der folgenden Werte.



| Wert                                                                        | Bedeutung                        |
|------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>0</dt> </dl> | 512-Byte-Ausrichtung.<br/> |
| <dl> <dt>1</dt> </dl> | 4-KB-Ausrichtung.<br/>     |



 

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Größe der virtuellen Festplattendatei (die tatsächliche Speichermenge, die von der Datei verbraucht wird) in Bytes.

</dd> <dt>

**FragmentationPercentage**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Näherung des Prozentsatzes der virtuellen Datenträgerblöcke, die in der datei der virtuellen Festplatte fragmentiert sind.

</dd> <dt>

**InUse**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft ist für eine spätere Verwendung vorgesehen.

</dd> <dt>

**MinInternalSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Mindestgröße, auf die die virtuelle Festplatte verkleinert werden kann (in Bytes). Diese Größe wird auf das nächstgrößerste Vielfache der Sektorgröße aufgerundet.

</dd> <dt>

**PhysicalSectorSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die vom zugrunde liegenden physischen Datenträger verwendete physische Sektorgröße in Bytes.

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Datentyp: **DATETIME**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitstempel der virtuellen Festplatte

> [!Note]  
> Hinzugefügt in Windows 10 und Windows Server 2016.

 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**GetVirtualHardDiskState**](getvirtualharddiskstate-msvm-imagemanagementservice.md)
</dt> </dl>

 

 




