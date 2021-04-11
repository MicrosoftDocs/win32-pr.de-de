---
description: Die CIM \_ -Bereitstellungs Klasse stellt eine Zuordnung zwischen einem Dateisystem und einem Verzeichnis dar, an das es angefügt ist.
ms.assetid: abf1833b-9b39-45c0-8400-2be2bf3a1c3c
ms.tgt_platform: multiple
title: CIM_Mount-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Mount
- CIM_Mount.Dependent
- CIM_Mount.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b86587466517a10302b3109a521e902a66892c4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127080"
---
# <a name="cim_mount-class"></a>CIM \_ Mount-Klasse

Die **CIM \_** -Bereitstellungs Klasse stellt eine Zuordnung zwischen einem Dateisystem und einem Verzeichnis dar, an das es angefügt ist.

Die Semantik dieser Beziehung erfordert, dass das eingebundene Verzeichnis in einem Dateisystem (über die Dateispeicher Zuordnung) enthalten ist, das sich von dem Dateisystem unterscheidet, auf das als abhängige verwiesen wird. Das Dateisystem, das das Verzeichnis enthält, kann lokal oder Remote sein. Beispielsweise kann ein lokales Dateisystem auf einem Solaris-Computersystem ein Verzeichnis aus dem Dateisystem einbinden, auf das über das Crom-Laufwerk des Computers (d. h. ein anderes lokales Dateisystem) zugegriffen wird. Auf der anderen Seite wird das Verzeichnis zunächst in einem "Remote Fall" vom Dateisystem exportiert, das auf einem anderen Computersystem gehostet wird, z. b. als Dateiserver. Um die beiden bereit Stellungen zu unterscheiden, sollte für die Verzeichnisse, auf die Remote zugegriffen werden kann, immer eine [**CIM- \_ Export**](cim-export.md) Zuordnung definiert werden.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{75BCF4F6-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Mount : CIM_Dependency
{
  CIM_NFS       REF Dependent;
  CIM_Directory REF Antecedent;
};
```

## <a name="members"></a>Member

Die **CIM \_** -Einstellungsklasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_** -Einstellungsklasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Verzeichnis**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Ein [**CIM- \_ Verzeichnis**](cim-directory.md) , das das eingebundene Verzeichnis beschreibt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ NFS**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Ein [**CIM- \_ NFS**](cim-nfs.md) , das das Dateisystem beschreibt, in dem das Verzeichnis eingebunden ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**CIM \_** Die Einschleusung wird von [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

