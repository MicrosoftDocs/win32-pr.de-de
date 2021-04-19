---
description: Stellt die Funktionen und die Verwaltung eines Band Laufwerks dar.
ms.assetid: 8140fd9a-8a12-43b4-bc61-ec143e5d754c
title: CIM_TapeDrive-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive
- CIM_TapeDrive.EOTWarningZoneSize
- CIM_TapeDrive.MaxPartitionCount
- CIM_TapeDrive.Padding
- CIM_TapeDrive.MaxRewindTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b92360388b71abcb0b67d30fddea9b4f5ed7920f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349777"
---
# <a name="cim_tapedrive-class-hyper-v-management"></a>CIM_TapeDrive-Klasse (Hyper-V-Verwaltung)

Stellt die Funktionen und die Verwaltung eines Band Laufwerks dar.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices")]
class CIM_TapeDrive : CIM_MediaAccessDevice
{
  uint32 EOTWarningZoneSize;
  uint32 MaxPartitionCount;
  uint32 Padding;
  uint64 MaxRewindTime;
};
```

## <a name="members"></a>Member

Die **CIM \_ TapeDrive** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ TapeDrive** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**EOTWarningZoneSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **Punit** ("Byte")
</dt> </dl>

Die Größe (in Bytes) des Bereichs, der als "Ende des Bands" festgelegt ist. Der Zugriff in diesem Bereich generiert die Warnung "Ende des Bands".

</dd> <dt>

**MaxPartitionCount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Partitions Anzahl für das Bandlaufwerk.

</dd> <dt>

**Maxrewindtime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden"), **Punit** ("Second \* 10 ^-3")
</dt> </dl>

Die Zeit (in Millisekunden), die vom physisch entfernten Punkt auf dem Band an den Anfang verschoben werden soll.

</dd> <dt>

**Auffüllen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **Punit** ("Byte")
</dt> </dl>

Die Anzahl von Bytes, die zwischen Blöcken auf Bandmedien eingefügt werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)
</dt> </dl>

 

