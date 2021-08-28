---
description: Die ZUORDNUNG CIM \_ FromDirectorySpecification identifiziert das Quellverzeichnis für die Dateiaktion.
ms.assetid: 031ff95f-aa68-4b05-92a6-97a5e0d8956f
ms.tgt_platform: multiple
title: CIM_FromDirectorySpecification-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FromDirectorySpecification
- CIM_FromDirectorySpecification.FileName
- CIM_FromDirectorySpecification.SourceDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bcb08f58e744e9926a3c4734ac1b8ad4fb75e3288b96ae0c0a7622c5e4109b79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320910"
---
# <a name="cim_fromdirectoryspecification-class"></a>CIM \_ FromDirectorySpecification-Klasse

Die **ZUORDNUNG CIM \_ FromDirectorySpecification** identifiziert das Quellverzeichnis für die Dateiaktion. Wenn diese Zuordnung verwendet wird, wird davon ausgegangen, dass das Quellverzeichnis bereits vorhanden ist. Diese Zuordnung kann nicht mit einer [**CIM \_ FromDirectoryAction-Zuordnung**](cim-fromdirectoryaction.md) vorhanden sein. Eine Dateiaktion kann nur ein einzelnes Quellverzeichnis umfassen.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{6715375E-DB2A-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_FromDirectorySpecification
{
  CIM_FileAction             REF FileName;
  CIM_DirectorySpecification REF SourceDirectory;
};
```

## <a name="members"></a>Member

Die **CIM \_ FromDirectorySpecification-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ FromDirectorySpecification-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ FileAction**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Verweis auf den Dateinamen.

</dd> <dt>

**SourceDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ DirectorySpecification**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max.**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min.**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Verweis auf das Quellverzeichnis.

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



 

