---
description: Die CIM \_ -Export Klasse stellt eine Zuordnung zwischen einem lokalen Dateisystem und den zugehörigen Verzeichnissen dar, die angeben, dass die angegebenen Verzeichnisse zum Einbinden verfügbar sind.
ms.assetid: 4c43ba5a-e003-4985-85b3-68ecf13a4bf5
ms.tgt_platform: multiple
title: CIM_Export-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Export
- CIM_Export.Directory
- CIM_Export.ExportedDirectoryName
- CIM_Export.LocalFS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 447601b61fb79cfa779ea0cab75962c835210c52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958410"
---
# <a name="cim_export-class"></a>CIM- \_ Export Klasse

Die **CIM- \_ Export** Klasse stellt eine Zuordnung zwischen einem lokalen Dateisystem und den zugehörigen Verzeichnissen dar, die angeben, dass die angegebenen Verzeichnisse zum Einbinden verfügbar sind. Beim Exportieren eines vollständigen Dateisystems sollte das Verzeichnis auf das oberste Verzeichnis des Dateisystems verweisen.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Association, UUID("{75BCF4F8-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Export
{
  CIM_Directory       REF Directory;
  string                  ExportedDirectoryName;
  CIM_LocalFileSystem REF LocalFS;
};
```

## <a name="members"></a>Member

Die **CIM- \_ Export** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ Export** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Verzeichnis**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Verzeichnis**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf das Verzeichnis, das für die Network File System (NFS)-einreilegung exportiert wird

</dd> <dt>

**Exporteddirecteryname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name, unter dem das Verzeichnis exportiert wird.

</dd> <dt>

**Localfs**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LocalFile System**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Verweis auf das lokale Dateisystem.

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



 

