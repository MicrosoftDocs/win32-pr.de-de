---
description: Die CIM-Zuordnungs Slots-Zuordnung \_ beschreibt das Layout von Slots auf einem hostboard oder einer Adapterkarte.
ms.assetid: d604647f-7b2f-4f99-8d98-adf115ae9dfb
ms.tgt_platform: multiple
title: CIM_AdjacentSlots-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AdjacentSlots
- CIM_AdjacentSlots.DistanceBetweenSlots
- CIM_AdjacentSlots.SharedSlots
- CIM_AdjacentSlots.SlotA
- CIM_AdjacentSlots.SlotB
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 695f9c668d6f75864e46026deac9a969993596ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127221"
---
# <a name="cim_adjacentslots-class"></a>CIM-Klasse "- \_ Klasse"

Die **CIM \_** -Zuordnungs Slots-Zuordnung beschreibt das Layout von Slots auf einem hostboard oder einer Adapterkarte. Informationen, wie z. b. der Abstand zwischen den Slots und ob Sie "Shared" sind (wenn eine aufgefüllt wird, der andere Slot kann nicht verwendet werden), werden als Zuordnungs Eigenschaften übermittelt.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Association, UUID("{FAF76B88-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AdjacentSlots
{
  real32       DistanceBetweenSlots;
  boolean      SharedSlots;
  CIM_Slot REF SlotA;
  CIM_Slot REF SlotB;
};
```

## <a name="members"></a>Member

Die **CIM \_** -Klasse "-Klasse" verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_** -Klasse "-Klasse" verfügt über diese Eigenschaften.

<dl> <dt>

**Distancebetweenslots**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")
</dt> </dl>

Abstand in Zoll zwischen angrenzenden Slots.

</dd> <dt>

**Sharedslots**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass einer der Slots durch eine Adapterkarte aufgefüllt wird. der andere Slot muss leer gelassen werden.

</dd> <dt>

**Slota**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Slot**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf einen der angrenzenden Slots.

</dd> <dt>

**Slotb**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Slot**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf den "anderen" angrenzenden Slot.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von WMI nicht implementiert.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

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

[CIM-Klassen](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

