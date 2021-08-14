---
description: Die AGGREGATION CIM \_ StorageDefect erfasst die Speicherfehler für einen Speicherspeicher.
ms.assetid: 7acd3d25-4691-43cb-badc-662684989345
ms.tgt_platform: multiple
title: CIM_StorageDefect-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageDefect
- CIM_StorageDefect.Error
- CIM_StorageDefect.Extent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 157714f9af979b34d647b1b02b1055b1cdac2ca0d84d3328c2c4740f9992024e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118420968"
---
# <a name="cim_storagedefect-class"></a>CIM \_ StorageDefect-Klasse

Die **AGGREGATION CIM \_ StorageDefect** erfasst die Speicherfehler für einen Speicherspeicher.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{5CC70817-DB31-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_StorageDefect
{
  CIM_StorageError  REF Error;
  CIM_StorageExtent REF Extent;
};
```

## <a name="members"></a>Member

Die **CIM \_ StorageDefect-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ StorageDefect-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Fehler**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ StorageError**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schwach**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Verweis auf das Fehlerobjekt, das die Start- und Endadressen definiert, die dem Speicher extent zugeordnet sind.

</dd> <dt>

**Extent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ StorageExtent**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Verweis auf den Speicher extent, in dem die Fehler aufgetreten sind.

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



 

