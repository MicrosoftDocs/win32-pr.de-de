---
description: Der WDM-Klassen Anbieter definiert die wmibinarymufresource-Klasse \\ im \\ WMI-Stamm Namespace, um die Aufgabe zu unterstützen, den Status der Daten im WMI-Repository zu verfolgen.
ms.assetid: 57416a36-5b3a-4d04-808c-09adc597c47a
title: Wmibinarymufresource-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIBinaryMofResource
- WMIBinaryMofResource.HighDateTime
- WMIBinaryMofResource.LowDateTime
- WMIBinaryMofResource.MofProcessed
- WMIBinaryMofResource.Name
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 715436ef19308c811e5486926b3cd7e59ee9de0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863331"
---
# <a name="wmibinarymofresource-class"></a>Wmibinarymufresource-Klasse

Der WDM-Klassen Anbieter definiert die **wmibinarymufresource** -Klasse \\ im \\ WMI-Stamm Namespace, um die Aufgabe zu unterstützen, den Status der Daten im WMI-Repository zu verfolgen.

## <a name="syntax"></a>Syntax

``` syntax
class WMIBinaryMofResource
{
  uint32  HighDateTime;
  uint32  LowDateTime;
  boolean MofProcessed;
  string  Name;
};
```

## <a name="members"></a>Member

Die **wmibinarymufresource** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **wmibinarymufresource** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Highdatetime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Hohe Hälfte des Datums-/Uhrzeitstempels.

</dd> <dt>

**Lowdatetime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Niedrige Hälfte des Datums-/Uhrzeitstempels.

</dd> <dt>

**Durch die Verarbeitung**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Flag, das angibt, ob die MOF-Datei vollständig verarbeitet wurde.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Der Name des WDM-fähigen Treibers, der über eine binäre MOF-Datei verfügt, die im WMI-Repository erfolgreich kompiliert wurde.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der WDM-Klassen Anbieter erstellt eine Instanz von **wmibinarymufresource** für jeden WDM-Treiber, der eine binäre MOF-Datei bereitstellt.

Wenn WMI den Anbieter initialisiert, vergleicht der Anbieter den Zeitstempel mit dem Zeitstempel der Treiber Image Datei. Wenn sich die Zeitstempel unterscheiden, kompiliert WMI die MOF-Datei erneut.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                     |
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                               |
| MOF<br/>                      | <dl> <dt>WMI. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WDM-Anbieter](wdm-provider.md)
</dt> </dl>

 

