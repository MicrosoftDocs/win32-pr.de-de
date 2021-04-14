---
description: Die CIM \_ relatedstatistics-Zuordnung stellt Hierarchien und Abhängigkeiten verwandter CIM \_ statisticalinformation-Klassen dar.
ms.assetid: f5cea01d-7854-4ad4-a89e-db0ce9f4a83f
ms.tgt_platform: multiple
title: CIM_RelatedStatistics-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RelatedStatistics
- CIM_RelatedStatistics.RelatedStats
- CIM_RelatedStatistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01fb70535a4ae8f84d637cf92a06eee4fe318a49
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523115"
---
# <a name="cim_relatedstatistics-class"></a>CIM \_ relatedstatistics-Klasse

Die **CIM \_ relatedstatistics** -Zuordnung stellt Hierarchien und Abhängigkeiten verwandter [**CIM \_ statisticalinformation**](cim-statisticalinformation.md) -Klassen dar.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Association, UUID("{956597A4-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_RelatedStatistics
{
  CIM_StatisticalInformation REF RelatedStats;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a>Member

Die **CIM \_ relatedstatistics** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ relatedstatistics** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Relatedstats**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ statisticalinformation**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf die zugehörigen Statistiken oder Metriken.

</dd> <dt>

**Stats**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ statisticalinformation**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf die statistischen Informationen oder das Objekt.

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



 

 




