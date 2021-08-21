---
description: Die CIM \_ CompatibleProduct-Klasse stellt eine Zuordnung zwischen Produkten dar, die angibt, ob zwei Referenzprodukte interoperabel sind, z. B. ob sie zusammen installiert werden können oder ob eines der physischen Container für das andere sein kann usw.
ms.assetid: d822b052-981a-4a66-8404-b4f5f4681502
ms.tgt_platform: multiple
title: CIM_CompatibleProduct-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CompatibleProduct
- CIM_CompatibleProduct.CompatibilityDescription
- CIM_CompatibleProduct.CompatibleProduct
- CIM_CompatibleProduct.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5d0d4721d8554723bb9ab808ff55884bb896f59e6050103cf127cc4df77109f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080874"
---
# <a name="cim_compatibleproduct-class"></a>CIM \_ CompatibleProduct-Klasse

Die **CIM \_ CompatibleProduct-Klasse** stellt eine Zuordnung zwischen Produkten dar, die angibt, ob zwei Referenzprodukte interoperabel sind, z. B. ob sie zusammen installiert werden können oder ob eines der physischen Container für das andere sein kann usw.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{2F648FBA-DB22-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_CompatibleProduct
{
  string          CompatibilityDescription;
  CIM_Product REF CompatibleProduct;
  CIM_Product REF Product;
};
```

## <a name="members"></a>Member

Die **CIM \_ CompatibleProduct-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ CompatibleProduct-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CompatibilityDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Freiformzeichenfolge, die definiert, wie die beiden Referenzprodukte interoperabel und kompatibel sind und ob Kompatibilitätseinschränkungen bestehen.

</dd> <dt>

**CompatibleProduct**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Produkt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf das kompatible Produkt.

</dd> <dt>

**Produkt**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Produkt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf das Produkt, für das kompatible Angebote definiert sind.

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



 

 




