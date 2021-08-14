---
description: Die \_ CIM-Klasse ProductPhysicalElements stellt die physischen Elemente dar, aus denen sich ein Produkt zusammen setzt.
ms.assetid: cf23098a-f61e-4778-883e-1a5138af3da0
ms.tgt_platform: multiple
title: CIM_ProductPhysicalElements-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductPhysicalElements
- CIM_ProductPhysicalElements.Component
- CIM_ProductPhysicalElements.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fa9d9103b317482e3fbd2cf1187775335f551a224f111f1b9e4d8c149f70a39b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118421641"
---
# <a name="cim_productphysicalelements-class"></a>CIM \_ ProductPhysicalElements-Klasse

Die **\_ CIM-Klasse ProductPhysicalElements** stellt die physischen Elemente dar, aus denen sich ein Produkt zusammen setzt.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird aus Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{502F00A0-DB2B-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_ProductPhysicalElements
{
  CIM_PhysicalElement REF Component;
  CIM_Product         REF Product;
};
```

## <a name="members"></a>Member

Die **CIM \_ ProductPhysicalElements-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ CIM-Klasse ProductPhysicalElements** verfügt über diese Eigenschaften.

<dl> <dt>

**Komponente**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ PhysicalElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf das physische Element, das Teil des Produkts ist.

</dd> <dt>

**Produkt**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Produkt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Aggregieren,**](/windows/desktop/WmiSdk/standard-qualifiers) [**Max.**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Verweis auf das Produkt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

WMI implementiert diese Klasse nicht.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

