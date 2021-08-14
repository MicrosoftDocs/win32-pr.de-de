---
description: Definiert Datums-/Uhrzeitintervalle in einem Format, das der Datums- und Uhrzeitsyntax ähnelt, indem die Zeichenfolge für Tage, Stunden, Minuten, Sekunden und Mikrosekunden in die Felder zerbricht.
ms.assetid: 13a3ca74-e3e9-44d7-9254-e288eb70ae4c
ms.tgt_platform: multiple
title: Intervallformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30db455b6b39349b3da2f8328b22597d8b9c16c47387ba7f6b15d81e62ceb134
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318536"
---
# <a name="interval-format"></a>Intervallformat

WMI definiert Datums-/Uhrzeitintervalle in einem Format, das der Datums- und Uhrzeitsyntax ähnelt, indem die Zeichenfolge für Tage, Stunden, Minuten, Sekunden und Mikrosekunden in die Felder zerbricht.

Das folgende Beispiel zeigt das Format eines Datums-/Uhrzeitintervalls.

``` syntax
ddddddddHHMMSS.mmmmmm:000
```

In der folgenden Tabelle sind die Felder des Datums-/Uhrzeitintervalls aufgeführt.



| Feld    | BESCHREIBUNG                                                                                                                                                                                                                                  |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ddddddddd | Acht Ziffern, die eine Anzahl von Tagen darstellen (000000000 bis 99999999).                                                                                                                                                                    |
| HH       | Zweistellige Stunde des Tages, die die 24-Stunden-Uhr verwendet (00 bis 23).                                                                                                                                                                       |
| MM       | Zweistellige Minute in der Stunde (00 bis 59).                                                                                                                                                                                                |
| SS       | Zweistellige Anzahl von Sekunden in der Minute (00 bis 59).                                                                                                                                                                                   |
| Mmmmmm   | Sechsstellige Anzahl von Mikrosekunden im zweiten (0000000 bis 999999). Ihre Implementierung ist nicht erforderlich, um die Auswertung mithilfe dieses Felds zu unterstützen, aber dieses Feld muss immer vorhanden sein, um die Zeichenfolge mit fester Länge zu erhalten. |



 

Intervalle haben immer einen nach folgenden ":000" als die letzten vier Zeichen. Darüber hinaus können Sie im Gegensatz zu Datum und Uhrzeit keine Sternchen verwenden, um nicht verwendete Felder anzugeben. Darüber hinaus müssen alle Eigenschaften des Typs [CIM \_ DATETIME,](cim-datetime.md) die Intervalle darstellen, mit dem SubType-Standardqualifizierer markiert werden, während der Qualifizierer auf "interval" festgelegt ist. [](standard-wmi-qualifiers.md)

Die folgende Zeichenfolge stellt ein Intervall von 1 Tag, 12 Stunden, 0 Minuten und 32 Sekunden dar.

``` syntax
00000001120032.000000:000
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datums- und Uhrzeitformat](date-and-time-format.md)
</dt> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> <dt>

[CIM \_ DATETIME](cim-datetime.md)
</dt> </dl>

 

 



