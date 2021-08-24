---
description: Die CIM \_ Mount-Klasse stellt eine Zuordnung zwischen einem Dateisystem und einem Verzeichnis dar, an das es angefügt ist.
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
ms.openlocfilehash: 1298c695237ac40097b0c081d313769ee4e4e1190571b1bdd58137e25d53c10a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821020"
---
# <a name="cim_mount-class"></a>\_CIM-Bereitstellungsklasse

Die **CIM \_ Mount-Klasse** stellt eine Zuordnung zwischen einem Dateisystem und einem Verzeichnis dar, an das es angefügt ist.

Die Semantik dieser Beziehung erfordert, dass das bereitgestellte Verzeichnis in einem Dateisystem (über die Dateispeicherzuordnung) enthalten ist, das sich vom Dateisystem unterscheidet, auf das als abhängig verwiesen wird. Das Verzeichnis, das das Dateisystem enthält, kann lokal oder remote sein. Beispielsweise kann ein lokales Dateisystem auf einem Solaris-Computersystem ein Verzeichnis aus dem Dateisystem einbinden, auf das über das C DOSE-Laufwerk des Computers (d. h. ein anderes lokales Dateisystem) zugegriffen wird. Andererseits wird das Verzeichnis in einem "Remote"-Fall zuerst von seinem Dateisystem exportiert, das auf einem anderen Computersystem gehostet wird, das z. B. als Dateiserver fungiert. Um die beiden Bereitstellungen zu unterscheiden, sollte immer eine [**CIM \_ Export-Zuordnung**](cim-export.md) für die Remotezugriffs-/eingebundenen Verzeichnisse definiert werden.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **CIM \_ Mount-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ Mount-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ Directory**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max.**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Ein [**\_ CIM-Verzeichnis,**](cim-directory.md) das das bereitgestellte Verzeichnis beschreibt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ NFS**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Ein [**\_ CIM-NFS,**](cim-nfs.md) der das Dateisystem beschreibt, in dem das Verzeichnis eingebunden ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**CIM \_ Die Bereitstellung** wird von [**\_ CIM-Abhängigkeit**](cim-dependency.md)abgeleitet.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

