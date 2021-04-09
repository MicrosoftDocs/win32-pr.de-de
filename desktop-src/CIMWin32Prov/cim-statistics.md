---
description: Die CIM \_ Statistics-Klasse stellt eine Zuordnung dar, die verwaltete Systemelemente mit den statistischen Gruppen verknüpft, die für Sie gelten.
ms.assetid: fc75991b-adcd-4e47-b610-7503f6bb7c03
ms.tgt_platform: multiple
title: CIM_Statistics-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Statistics
- CIM_Statistics.Element
- CIM_Statistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b35299a52c771ee3bcb76673ef1e2164af3b3180
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958207"
---
# <a name="cim_statistics-class"></a>CIM- \_ Statistik Klasse

Die **CIM \_ Statistics** -Klasse stellt eine Zuordnung dar, die verwaltete Systemelemente mit den statistischen Gruppen verknüpft, die für Sie gelten.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Association, UUID("{956597A3-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_Statistics
{
  CIM_ManagedSystemElement   REF Element;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a>Member

Die **CIM- \_ Statistik** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ Statistics** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedSystemElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf die [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Klasse, für die statistische Daten oder Metrikdaten definiert werden.

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



 

 




