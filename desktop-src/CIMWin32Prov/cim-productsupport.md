---
description: Die CIM \_ productsupport-Klasse stellt eine Zuordnung Zwischenprodukt und Support Zugriff dar, die die Art der Unterstützung für das Produkt übermittelt.
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
ms.openlocfilehash: 8d1b39e1eef8f9686eee66c629120feaea51c778
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342979"
---
# <a name="cim_productsupport-class"></a>CIM \_ productsupport-Klasse

Die **CIM \_ productsupport** -Klasse stellt eine Zuordnung Zwischenprodukt und Support Zugriff dar, die die Art der Unterstützung für das Produkt übermittelt. Für ein Produkt sind verschiedene Support Typen verfügbar. das gleiche Support Objekt bietet Unterstützung für mehrere Produkte.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **CIM \_ productsupport** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ productsupport** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Produkt**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Produkt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf das Produkt.

</dd> <dt>

**Unterstützung**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ supportaccess**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf den Produktsupport.

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



 

 




