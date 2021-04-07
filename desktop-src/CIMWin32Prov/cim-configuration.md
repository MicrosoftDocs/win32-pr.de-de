---
description: Das CIM \_ -Konfigurationsobjekt ermöglicht die Gruppierung von Parametersätzen (definiert in CIM- \_ Einstellungs Objekten) und Abhängigkeiten für ein oder mehrere verwaltete Systemelemente.
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
ms.openlocfilehash: c069f5c7186d08f01b54fe02c0568dbb4ff43d26
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748601"
---
# <a name="cim_configuration-class"></a>CIM- \_ Konfigurations Klasse

Das **CIM- \_ Konfigurations** Objekt ermöglicht die Gruppierung von Parametersätzen (definiert in [**CIM- \_ Einstellungs**](cim-setting.md) Objekten) und Abhängigkeiten für ein oder mehrere verwaltete Systemelemente. Dieses Objekt stellt ein bestimmtes Verhalten oder einen gewünschten funktionalen Zustand für die verwalteten Systemelemente dar. Der gewünschte funktionale Zustand wird in der Regel durch externe Anforderungen, z. b. Zeit oder Speicherort, gesteuert. Wenn Sie z. b. eine Verbindung mit einem e-Mail-System von Hause aus herstellen möchten, besteht eine Abhängigkeit von einem Modem eine Abhängigkeit von einem Netzwerkadapter ist dagegen bei der Arbeit vorhanden. Einstellungen für die entsprechenden logischen Geräte (in diesem Beispiel für das Modem-Modem und den Netzwerkadapter) können durch die **CIM- \_ Konfiguration** definiert und aggregiert werden. Daher können zwei "Connect to Mail"-Konfigurationen definiert werden, indem die relevanten Abhängigkeiten und [**CIM- \_ Einstellungs**](cim-setting.md) Objekte gruppiert werden.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **CIM- \_ Konfigurations** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ Konfigurations** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Textbeschreibung des **CIM- \_ Konfigurations** Objekts.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des **CIM- \_ Konfigurations** Objekts.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Bezeichnung, nach der das **CIM- \_ Konfigurations** Objekt bekannt ist.

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



 

