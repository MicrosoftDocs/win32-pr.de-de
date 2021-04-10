---
description: Die CIM \_ productfru-Klasse stellt eine Zuordnung zwischen dem Produkt und einer ersetzbaren (Feld) Einheit (FRU) dar, die Informationen zu Produktkomponenten bereitstellt, die bereits waren oder ersetzt werden.
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
ms.openlocfilehash: b141d16adb50c5bc3f8d6be682a90aa4921061ef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126307"
---
# <a name="cim_productfru-class"></a>CIM \_ productfru-Klasse

Die **CIM \_ productfru** -Klasse stellt eine Zuordnung zwischen dem Produkt und einer ersetzbaren (Feld) Einheit (FRU) dar, die Informationen zu Produktkomponenten bereitstellt, die bereits waren oder ersetzt werden.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **CIM \_ productfru** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ productfru** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**FRU**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ FRU**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf das FRU-.

</dd> <dt>

**Produkt**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Produkt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Verweis auf das Produkt, auf das die FRU angewendet wird.

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



 

