---
description: Die ZUORDNUNG \_ CIM ToDirectorySpecification identifiziert das Zielverzeichnis für die Dateiaktion.
ms.assetid: ab31101f-1948-4b3d-baef-0d61d5898b21
ms.tgt_platform: multiple
title: CIM_ToDirectorySpecification-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectorySpecification
- CIM_ToDirectorySpecification.DestinationDirectory
- CIM_ToDirectorySpecification.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e079a5012760507adfd9bff6b9716a6828e1f3e9b516ec252895ab8e93e801d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118677386"
---
# <a name="cim_todirectoryspecification-class"></a>CIM \_ ToDirectorySpecification-Klasse

Die **ZUORDNUNG CIM \_ ToDirectorySpecification** identifiziert das Zielverzeichnis für die Dateiaktion. Wenn diese Zuordnung verwendet wird, wird davon ausgegangen, dass das Zielverzeichnis bereits vorhanden ist. Diese Zuordnung kann nicht mit einer [**CIM \_ ToDirectoryAction-Zuordnung**](cim-todirectoryaction.md) vorhanden sein, da eine Dateiaktion nur ein einzelnes Zielverzeichnis umfassen kann.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{C3E25A3C-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectorySpecification
{
  CIM_DirectorySpecification REF DestinationDirectory;
  CIM_CopyFileAction         REF FileName;
};
```

## <a name="members"></a>Member

Die **CIM \_ ToDirectorySpecification-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ToDirectorySpecification-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**DestinationDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ DirectorySpecification**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Verweis auf das Zielverzeichnis.

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ CopyFileAction**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Verweis auf den Dateinamen.

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



 

