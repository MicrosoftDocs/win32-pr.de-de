---
description: Die CIM \_ ProductFRU-Klasse stellt eine Zuordnung zwischen dem Produkt und einer FRU (Field Replaceable Unit) dar, die Informationen zu Produktkomponenten bereitstellt, die ersetzt wurden oder ersetzt werden.
ms.assetid: 15d682e5-cd90-4fc4-8fff-e3fe1d2a0ac4
ms.tgt_platform: multiple
title: CIM_ProductFRU-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductFRU
- CIM_ProductFRU.FRU
- CIM_ProductFRU.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06457b7f5eccd7364fa7882301ec0a195cb5bfc3af46d4040570d1ecb2e2f635
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020948"
---
# <a name="cim_productfru-class"></a>CIM \_ ProductFRU-Klasse

Die **CIM \_ ProductFRU-Klasse** stellt eine Zuordnung zwischen dem Produkt und einer FRU (Field Replaceable Unit) dar, die Informationen zu Produktkomponenten bereitstellt, die ersetzt wurden oder ersetzt werden.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird aus Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{EB98A1B2-DB36-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductFRU
{
  CIM_FRU     REF FRU;
  CIM_Product REF Product;
};
```

## <a name="members"></a>Member

Die **CIM \_ ProductFRU-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ProductFRU-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**FRU**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ FRU**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf die FRU.

</dd> <dt>

**Produkt**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Produkt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max.**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Verweis auf das Produkt, auf das die FRU angewendet wird.

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



 

