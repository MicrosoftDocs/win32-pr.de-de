---
description: Die CIM ProductSupport-Klasse stellt eine Zuordnung zwischen Produkt- und Supportzugriff dar, die vermittelt, \_ wie Support für das Produkt erhalten wird.
ms.assetid: 61c62556-0cf3-438c-b9c7-152505bf7ed6
ms.tgt_platform: multiple
title: CIM_ProductSupport-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSupport
- CIM_ProductSupport.Product
- CIM_ProductSupport.Support
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a33efc39481ebe94b6aa8802d469e218d026aba34ab8da6cddf3f136b45a6d3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118421447"
---
# <a name="cim_productsupport-class"></a>CIM \_ ProductSupport-Klasse

Die **CIM \_ ProductSupport-Klasse** stellt eine Zuordnung zwischen Produkt- und Supportzugriff dar, die vermittelt, wie Support für das Produkt erhalten wird. Für ein Produkt stehen verschiedene Supporttypen zur Verfügung. das gleiche Supportobjekt kann Unterstützung für mehrere Produkte bereitstellen.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{8D6D6880-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductSupport
{
  CIM_Product       REF Product;
  CIM_SupportAccess REF Support;
};
```

## <a name="members"></a>Member

Die **CIM \_ ProductSupport-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ProductSupport-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Produkt**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Produkt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf das Produkt.

</dd> <dt>

**Unterstützung**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ SupportAccess**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf den Produktsupport.

</dd> </dl>

## <a name="remarks"></a>Hinweise

WMI implementiert diese Klasse nicht.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




