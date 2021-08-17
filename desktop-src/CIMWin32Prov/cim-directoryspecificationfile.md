---
description: Die CIM \_ DirectorySpecificationFile-Zuordnung stellt das Verzeichnis dar, das die durch Verweisen auf die CIM \_ DirectorySpecification-Klasse angegebene Datei enthält.
ms.assetid: 57fe996e-6bd4-4070-9e99-460b2a36243f
ms.tgt_platform: multiple
title: CIM_DirectorySpecificationFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecificationFile
- CIM_DirectorySpecificationFile.DirectorySpecification
- CIM_DirectorySpecificationFile.FileSpecification
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d26cf0ff32380d6d0fb1daaa7e10e06159664b98778a074327c5a6d8654fd270
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119321350"
---
# <a name="cim_directoryspecificationfile-class"></a>CIM \_ DirectorySpecificationFile-Klasse

Die **CIM \_ DirectorySpecificationFile-Zuordnung** stellt das Verzeichnis dar, das die datei enthält, die durch Verweisen auf die [**CIM \_ DirectorySpecification-Klasse**](cim-directoryspecification.md) angegeben wird.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{BCD64CCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_DirectorySpecificationFile
{
  CIM_DirectorySpecification REF DirectorySpecification;
  CIM_FileSpecification      REF FileSpecification;
};
```

## <a name="members"></a>Member

Die **CIM \_ DirectorySpecificationFile-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ DirectorySpecificationFile-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**DirectorySpecification**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ DirectorySpecification**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max.**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min.**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Verweis auf die Verzeichnisspezifikation.

</dd> <dt>

**FileSpecification**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ FileSpecification**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min.**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Verweis auf die Dateispezifikation.

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



 

