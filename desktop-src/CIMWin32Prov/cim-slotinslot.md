---
description: Die CIM \_ slotinslot-Beziehung stellt die Fähigkeit eines speziellen Adapters dar, die vorhandene slotstruktur zu erweitern, um ansonsten inkompatible Karten zu ermöglichen, die an einem Frame oder einem hostingboard angeschlossen werden.
ms.assetid: 688231de-49fd-415d-b2c8-ef0dd4dcaee4
ms.tgt_platform: multiple
title: CIM_SlotInSlot-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SlotInSlot
- CIM_SlotInSlot.Dependent
- CIM_SlotInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0102a431393906b5ff98339569a027cbe3ef5b40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343580"
---
# <a name="cim_slotinslot-class"></a>CIM \_ slotinslot-Klasse

Die **CIM \_ slotinslot** -Beziehung stellt die Fähigkeit eines speziellen Adapters dar, die vorhandene slotstruktur zu erweitern, um ansonsten inkompatible Karten zu ermöglichen, die an einem Frame oder einem hostingboard angeschlossen werden. Slots sind spezielle Connectortypen, in die normalerweise Adapterkarten eingefügt werden. Der Adapter erstellt effektiv einen neuen Slot und kann sich (konzeptionell) als Slot in einem Slot vorstellen. Karten, die andernfalls physisch oder physisch mit den vorhandenen Slots nicht kompatibel sind, werden durch die Schnittstellen mit dem vom Adapter bereitgestellten Slot unterstützt. Beispielsweise sind Netzwerk Boards sehr aufwendig. Wenn neue Hardware verfügbar wird, ändern sich Chassis-und Karten Konfigurationen. Um die Investition ihrer Kunden zu schützen, werden Netzwerkhersteller spezielle Adapter bereitstellen, mit denen alte Karten in neue Chassis-oder hostingboards oder neue Karten eingefügt werden können, um Sie in alte Karten einzufügen, indem ein spezieller Adapter verwendet wird, der über einen oder mehrere vorhandene Slots passt und einen neuen Slot anzeigt, in den die Karte passt.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{FAF76B87-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_SlotInSlot : CIM_ConnectedTo
{
  CIM_Slot REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a>Member

Die **CIM \_ slotinslot** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ slotinslot** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Slot**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")
</dt> </dl>

Ein [**CIM- \_ Slot**](cim-slot.md) , der die vorhandenen Slots des hostingboards beschreibt, oder Frame, die an eine Karte angepasst werden, die andernfalls physisch und/oder nicht physisch kompatibel wäre.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Slot**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein [**CIM- \_ Slot**](cim-slot.md) , der den neuen Slot beschreibt, der vom Adapterboard bereitgestellt wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **CIM \_ slotinslot** -Klasse wird von [**CIM \_ connectedto**](cim-connectedto.md)abgeleitet.

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

[**CIM \_ connectedto**](cim-connectedto.md)
</dt> </dl>

 

