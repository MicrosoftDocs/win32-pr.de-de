---
description: Die CIM \_ fromdirector Action-Zuordnung identifiziert das Quellverzeichnis für die Datei Aktion.
ms.assetid: 25d06dad-ae39-4cfc-9331-4be7ef02d87c
ms.tgt_platform: multiple
title: CIM_FromDirectoryAction-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FromDirectoryAction
- CIM_FromDirectoryAction.FileName
- CIM_FromDirectoryAction.SourceDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f485fa32561e746afa16a899a1392b4fddc18f1f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861252"
---
# <a name="cim_fromdirectoryaction-class"></a>CIM \_ fromdirectoryaction-Klasse

Die **CIM \_ fromdirector Action** -Zuordnung identifiziert das Quellverzeichnis für die Datei Aktion. Wenn diese Zuordnung verwendet wird, wird davon ausgegangen, dass das Quellverzeichnis durch eine vorherige Aktion erstellt wurde. Diese Zuordnung darf nicht mit einer [**CIM \_ fromdirector yspecification**](cim-fromdirectoryspecification.md) -Zuordnung vorhanden sein. eine Datei Aktion kann nur ein einzelnes Quellverzeichnis umfassen.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{55D5B446-DB2A-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_FromDirectoryAction
{
  CIM_FileAction      REF FileName;
  CIM_DirectoryAction REF SourceDirectory;
};
```

## <a name="members"></a>Member

Die **CIM \_ fromdirectoryaction** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ fromdirectoryaction** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ fileaction**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Verweis auf den Dateinamen.

</dd> <dt>

**SourceDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ directoriyaction**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Verweis auf das Quellverzeichnis.

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



 

