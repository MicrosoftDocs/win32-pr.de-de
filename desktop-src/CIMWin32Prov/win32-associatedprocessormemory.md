---
description: Die \_ WMI-Zuordnungsklasse Win32 AssociatedProcessorMemory verknüpft einen Prozessor und seinen Cachespeicher.
ms.assetid: 23da2a9d-772e-4258-9489-07d47801b2d8
ms.tgt_platform: multiple
title: Win32_AssociatedProcessorMemory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AssociatedProcessorMemory
- Win32_AssociatedProcessorMemory.BusSpeed
- Win32_AssociatedProcessorMemory.Dependent
- Win32_AssociatedProcessorMemory.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8740aca290bbe116f867915fd15f4f2683bfe3b2d4c4a2e8cc731516ba8a0a09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109630"
---
# <a name="win32_associatedprocessormemory-class"></a>Win32 \_ AssociatedProcessorMemory-Klasse

Die [WMI-Zuordnungsklasse](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ AssociatedProcessorMemory** verknüpft einen Prozessor und seinen Cachespeicher.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{074737F0-ACBC-11d2-ABF6-00805F538618}"), AMENDMENT]
class Win32_AssociatedProcessorMemory : CIM_AssociatedProcessorMemory
{
  uint32                BusSpeed;
  Win32_Processor   REF Dependent;
  Win32_CacheMemory REF Antecedent;
};
```

## <a name="members"></a>Member

Die **Win32 \_ AssociatedProcessorMemory-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ AssociatedProcessorMemory-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ CacheMemory**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ CacheMemory")
</dt> </dl>

Ein [**Win32 \_ CacheMemory,**](win32-cachememory.md) der den für den Prozessor verfügbaren Cachespeicher beschreibt.

</dd> <dt>

**BusSpeed**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")
</dt> </dl>

Geschwindigkeit des Bus in Megahertz (MHz) zwischen Prozessor und Arbeitsspeicher.

Diese Eigenschaft wird von [**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md)geerbt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **\_ Win32-Prozessor**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ Processor")
</dt> </dl>

Ein [**\_ Win32-Prozessor,**](win32-processor.md) der den Prozessor beschreibt, der den Cachespeicher verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ AssociatedProcessorMemory-Klasse** wird von [**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md)abgeleitet.

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

[**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md)
</dt> <dt>

[Computersystemhardwareklassen](computer-system-hardware-classes.md)
</dt> </dl>

 

