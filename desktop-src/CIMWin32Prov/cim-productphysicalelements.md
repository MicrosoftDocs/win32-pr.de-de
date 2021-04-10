---
description: Die CIM \_ productphysicalelements-Klasse stellt die physischen Elemente dar, die ein Produkt bilden.
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
ms.openlocfilehash: a581293426c421de0dd76636a9f446f245f6ab32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126302"
---
# <a name="cim_productphysicalelements-class"></a>CIM \_ productphysicalelements-Klasse

Die **CIM \_ productphysicalelements** -Klasse stellt die physischen Elemente dar, die ein Produkt bilden.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **CIM \_ productphysicalelements** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ productphysicalelements** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Komponente**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ PhysicalElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf das physische Element, das Bestandteil des Produkts ist.

</dd> <dt>

**Produkt**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Produkt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Verweis auf das Produkt.

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



 

