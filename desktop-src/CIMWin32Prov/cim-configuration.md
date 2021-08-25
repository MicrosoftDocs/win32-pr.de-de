---
description: Das \_ CIM-Konfigurationsobjekt ermöglicht das Gruppieren von Parametersätzen (definiert in CIM-Einstellungsobjekten) und Abhängigkeiten für ein \_ oder mehrere verwaltete Systemelemente.
ms.assetid: f597fe78-be50-4d31-b1eb-d219acaf1751
ms.tgt_platform: multiple
title: CIM_Configuration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Configuration
- CIM_Configuration.Caption
- CIM_Configuration.Description
- CIM_Configuration.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c6df2338d46438bf3e1af371ebbce8b36f1a337f26a4785064119cca45bece46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924930"
---
# <a name="cim_configuration-class"></a>\_CIM-Konfigurationsklasse

Das **\_ CIM-Konfigurationsobjekt** ermöglicht das Gruppieren von Parametersätzen (definiert in [**\_ CIM-Einstellungsobjekten)**](cim-setting.md) und Abhängigkeiten für ein oder mehrere verwaltete Systemelemente. Dieses Objekt stellt ein bestimmtes Verhalten oder einen gewünschten Funktionszustand für die verwalteten Systemelemente dar. Der gewünschte Funktionszustand wird in der Regel durch externe Anforderungen wie Zeit oder Standort gesteuert. Wenn Sie beispielsweise von zu Hause aus eine Verbindung mit einem E-Mail-System herstellen möchten, besteht eine Abhängigkeit von einem Modem. eine Abhängigkeit von einem Netzwerkadapter ist hingegen am Arbeitsplatz vorhanden. Einstellungen für die relevanten logischen Geräte (in diesem Beispiel: MODEMS-Modem und Netzwerkadapter) können durch die **CIM-Konfiguration definiert und aggregiert \_ werden.** Aus diesem Grund können zwei Konfigurationen Verbinden an E-Mail gesendet werden, indem die relevanten Abhängigkeiten und [**CIM-Einstellungsobjekte \_ gruppieren**](cim-setting.md) werden.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{4C51D7AE-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_Configuration
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a>Member

Die **\_ CIM-Konfigurationsklasse** verfügt über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ CIM-Konfigurationsklasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Textbeschreibung des **\_ CIM-Konfigurationsobjekts.**

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des **\_ CIM-Konfigurationsobjekts.**

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Bezeichnung, unter der **das \_ CIM-Konfigurationsobjekt** bekannt ist.

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



 

