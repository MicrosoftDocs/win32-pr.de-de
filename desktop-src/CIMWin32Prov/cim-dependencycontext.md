---
description: Die CIM \_ DependencyContext-Beziehung ordnet eine \_ CIM-Abhängigkeitsklasse mindestens einem CIM-Konfigurationsobjekt \_ zu. Beispielsweise können sich die Abhängigkeiten eines Computersystems basierend auf dem Netzwerk ändern, an das das System angefügt ist.
ms.assetid: 9f35fc41-1bfa-4018-a54c-64c875c710d4
ms.tgt_platform: multiple
title: CIM_DependencyContext-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DependencyContext
- CIM_DependencyContext.Context
- CIM_DependencyContext.Dependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 845086b7d41eb03227d6b5b47240ef4bf9e1a2c35f8049c96d5c665800b327e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924640"
---
# <a name="cim_dependencycontext-class"></a>CIM \_ DependencyContext-Klasse

Die **CIM \_ DependencyContext-Beziehung** ordnet eine [**\_ CIM-Abhängigkeitsklasse**](cim-dependency.md) mindestens einem [**CIM-Konfigurationsobjekt \_**](cim-configuration.md) zu. Beispielsweise können sich die Abhängigkeiten eines Computersystems basierend auf dem Netzwerk ändern, an das das System angefügt ist.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Aggregation, Association, UUID("{A228E208-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DependencyContext
{
  CIM_Configuration REF Context;
  CIM_Dependency    REF Dependency;
};
```

## <a name="members"></a>Member

Die **CIM \_ DependencyContext-Klasse** verfügt über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ DependencyContext-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Context**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Konfiguration**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Aggregieren**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Verweis auf das Konfigurationsobjekt, das die Abhängigkeit aggregiert.

</dd> <dt>

**Abhängigkeit**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Abhängigkeit**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf eine aggregierte Abhängigkeit.

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



 

