---
description: Die CIM- \_ directoryspecificationfile-Zuordnung stellt das Verzeichnis dar, das die Datei enthält, die durch Verweisen auf die CIM- \_ directoryspecification-Klasse angegeben wird.
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
ms.openlocfilehash: 1877d9864a76334c2b2e00fc7822adb09b91028b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127184"
---
# <a name="cim_directoryspecificationfile-class"></a>CIM- \_ directoryspecificationfile-Klasse

Die **CIM- \_ directoryspecificationfile-Zuordnung** stellt das Verzeichnis dar, das die Datei enthält, die durch Verweisen auf die CIM- [**\_ directoryspecification**](cim-directoryspecification.md) -Klasse angegeben wird.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **CIM- \_ directoryspecificationfile** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ directoryspecificationfile** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Directoriyspecification**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ directoriyspecification**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Verweis auf die Verzeichnis Spezifikation.

</dd> <dt>

**File Specification**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ File Specification**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Verweis auf die Datei Spezifikation.

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



 

