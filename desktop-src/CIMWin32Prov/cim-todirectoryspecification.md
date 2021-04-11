---
description: Die CIM- \_ Verzeichnisdienst Spezifikation identifiziert das Zielverzeichnis für die Datei Aktion.
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
ms.openlocfilehash: e0728f605e02195a6bf2bd4beb0ca67fe8744e12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127769"
---
# <a name="cim_todirectoryspecification-class"></a>CIM- \_ Klasse für directoryspecification

Die **CIM \_** -Verzeichnisdienst Spezifikation identifiziert das Zielverzeichnis für die Datei Aktion. Wenn diese Zuordnung verwendet wird, wird davon ausgegangen, dass das Zielverzeichnis bereits vorhanden ist. Diese Zuordnung darf nicht mit einer [**CIM-" \_ dedirector yaction**](cim-todirectoryaction.md) "-Zuordnung vorhanden sein, da eine Datei Aktion nur ein einzelnes Zielverzeichnis umfassen kann.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **CIM \_ todirectoryspecification** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die CIM-Klasse " **\_ dedirectoryspecification** " verfügt über diese Eigenschaften.

<dl> <dt>

**DestinationDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ directoriyspecification**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Verweis auf das Zielverzeichnis.

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ copyfileaction**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Verweis auf den Dateinamen.

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



 

