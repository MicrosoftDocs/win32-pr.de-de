---
description: Listet die unterstützten Quell Modi für einen Videomonitor in seinem Monitor Deskriptor auf, sofern vorhanden.
ms.assetid: cca59d28-bd93-4df2-989e-0516dd8eae83
title: Wmimonitorlistedsupportedsourcemodes-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedSupportedSourceModes
- WmiMonitorListedSupportedSourceModes.Active
- WmiMonitorListedSupportedSourceModes.InstanceName
- WmiMonitorListedSupportedSourceModes.NumOfMonitorSourceModes
- WmiMonitorListedSupportedSourceModes.PreferredMonitorSourceModeIndex
- WmiMonitorListedSupportedSourceModes.MonitorSourceModes
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 35cb4b3548654c72686a8843cc697f109f661d87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357861"
---
# <a name="wmimonitorlistedsupportedsourcemodes-class"></a>Wmimonitorlistedsupportedsourcemodes-Klasse

**Wmimonitorlistedsupportedsourcemodes** listet die unterstützten Quell Modi für einen Videomonitor in seinem Monitor Deskriptor auf, sofern vorhanden. Für Monitore, die keine Beschreibung aufweisen, wird diese Liste der Modi basierend auf der Art des Monitors generiert, wie vom Monitor Bustreiber angegeben.

## <a name="syntax"></a>Syntax

``` syntax
class WmiMonitorListedSupportedSourceModes : MSMonitorClass
{
  boolean             Active;
  string              InstanceName;
  uint16              NumOfMonitorSourceModes;
  uint16              PreferredMonitorSourceModeIndex;
  VideoModeDescriptor MonitorSourceModes[];
};
```

## <a name="members"></a>Member

Die **wmimonitorlistedsupportedsourcemodes** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **wmimonitorlistedsupportedsourcemodes** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktiven Monitor an.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Der Name der spezifischen Monitor Instanz.

</dd> <dt>

**Monitorsourcemodes**
</dt> <dd> <dl> <dt>

Datentyp: **videomodedescriptor** -Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Listet die Monitor Quellmodi auf, die durch Instanzen der [**videomodedescriptor**](videomodedescriptor.md) -Klasse dargestellt werden.

</dd> <dt>

**Numuf monitorsourcemodes**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der aufgeführten unterstützten Monitor Quellen Modus.

</dd> <dt>

**Preferredmonitorsourcemodeingedex**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bevorzugter Monitor Quell Modus-Index.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




