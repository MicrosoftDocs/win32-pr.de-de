---
description: Die \_ WMI-Zuordnungsklasse Win32 PhysicalMemoryLocation bezieht sich auf ein Array von physischem Speicher und dessen physischem Speicher.
ms.assetid: 40252428-77ca-4dfb-8048-c05096a114d8
ms.tgt_platform: multiple
title: Win32_PhysicalMemoryLocation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryLocation
- Win32_PhysicalMemoryLocation.LocationWithinContainer
- Win32_PhysicalMemoryLocation.PartComponent
- Win32_PhysicalMemoryLocation.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10f4822312619b5b7fb811a998d82527b6e8bd0bd604e0d2095dae5103935e41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972060"
---
# <a name="win32_physicalmemorylocation-class"></a>Win32 \_ PhysicalMemoryLocation-Klasse

Die **WMI-Zuordnungsklasse \_ Win32 PhysicalMemoryLocation** bezieht sich auf ein Array von physischem Speicher und dessen physischem Speicher. [](../wmisdk/retrieving-a-class.md)

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF562-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_PhysicalMemoryLocation : CIM_PackagedComponent
{
  string                        LocationWithinContainer;
  Win32_PhysicalMemory      REF PartComponent;
  Win32_PhysicalMemoryArray REF GroupComponent;
};
```

## <a name="members"></a>Member

Die **Win32 \_ PhysicalMemoryLocation-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ PhysicalMemoryLocation-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ PhysicalMemoryArray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PhysicalMemoryArray")
</dt> </dl>

Ein [**Win32 \_ PhysicalMemoryArray,**](win32-physicalmemoryarray.md) das das physische Speicherarray darstellt, das den physischen Speicher enthält.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Freiformzeichenfolge, die die Positionierung des physischen Elements innerhalb des physischen Pakets darstellt. Informationen relativ zu den stationären Elementen im Container (z. B. "Zweiter Laufwerksschacht von oben"), Winkel, Höhe und andere Daten können in dieser Eigenschaft aufgezeichnet werden. Diese Zeichenfolge kann das CIM Location-Objekt ergänzen oder verwenden, statt [**es \_ zu**](cim-location.md) instanziieren.

Diese Eigenschaft wird vom [**\_ CIM-Container geerbt.**](cim-container.md)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ PhysicalMemory**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PhysicalMemory")
</dt> </dl>

Ein [**Win32 \_ PhysicalMemory,**](win32-physicalmemory.md) das den physischen Speicher darstellt, der im Physischen Speicherarray enthalten ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ PhysicalMemoryLocation-Klasse** wird von [**CIM \_ PackagedComponent abgeleitet.**](cim-packagedcomponent.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ PackagedComponent**](cim-packagedcomponent.md)
</dt> <dt>

[Hardwareklassen des Computersystems](computer-system-hardware-classes.md)
</dt> </dl>

 

 
