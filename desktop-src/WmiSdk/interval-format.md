---
description: Definiert Datums-/uhrzeitintervalle mit einem Format, das der Datums-und Uhrzeit Syntax ähnelt, indem die Zeichenfolge in die Felder für Tage, Stunden, Minuten, Sekunden und Mikrosekunden aufgeteilt wird.
ms.assetid: 13a3ca74-e3e9-44d7-9254-e288eb70ae4c
ms.tgt_platform: multiple
title: Intervall Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10e13d5febbce22648ec76961269ab18b1c028a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357069"
---
# <a name="interval-format"></a>Intervall Format

WMI definiert Datums-/uhrzeitintervalle mit einem Format, das der Datums-und Uhrzeit Syntax ähnelt, indem die Zeichenfolge in die Felder für Tage, Stunden, Minuten, Sekunden und Mikrosekunden aufgeteilt wird.

Das folgende Beispiel zeigt das Format eines Datums-/uhrzeitintervalls.

``` syntax
ddddddddHHMMSS.mmmmmm:000
```

In der folgenden Tabelle sind die Felder des Datums-/uhrzeitintervalls aufgeführt.



| Feld    | BESCHREIBUNG                                                                                                                                                                                                                                  |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dddddddd | Acht Ziffern, die eine Anzahl von Tagen darstellen (00000000 bis 99999999).                                                                                                                                                                    |
| HH       | Zweistellige Stunden Angabe des Tages, bei dem das 24-Stunden-Format (00 bis 23) verwendet wird.                                                                                                                                                                       |
| MM       | Zweistellige Minuten Angabe in der Stunde (00 bis 59).                                                                                                                                                                                                |
| SS       | Zweistellige Anzahl von Sekunden in der Minute (00 bis 59).                                                                                                                                                                                   |
| mmmmmm   | Sechsstellige Anzahl von Mikrosekunden im zweiten Wert (000000 bis 999999). Ihre Implementierung ist nicht erforderlich, um die Auswertung mit diesem Feld zu unterstützen, aber dieses Feld muss immer vorhanden sein, um die Länge der Zeichenfolge mit fester Länge beizubehalten. |



 

Intervalle verfügen immer über eine nachfolgende ": 000"-in den letzten vier Zeichen. Darüber hinaus können Sie im Gegensatz zu Datum und Uhrzeit nicht verwendete Felder mithilfe von Sternchen angeben. Außerdem müssen alle Eigenschaften vom Typ [CIM \_ DateTime](cim-datetime.md) , die Intervalle darstellen, mit dem [Untertyp](standard-wmi-qualifiers.md) Standard Qualifizierer gekennzeichnet werden, wobei der Qualifizierer auf "Interval" festgelegt ist.

Die folgende Zeichenfolge stellt ein Intervall von 1 Tag, 12 Stunden, 0 Minuten und 32 Sekunden dar.

``` syntax
00000001120032.000000:000
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datums-und Uhrzeit Format](date-and-time-format.md)
</dt> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> <dt>

[CIM- \_ DateTime](cim-datetime.md)
</dt> </dl>

 

 



