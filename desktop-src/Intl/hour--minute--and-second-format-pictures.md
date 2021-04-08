---
description: Dieses Thema beschreibt die Format Typen für Zeichen folgen, die zum Verfassen des Format Bilds für eine Zeit Zeichenfolge verwendet werden. Jedes Format Bild besteht aus einer Kombination aus einer Zeichenfolge der einzelnen Format Typen.
ms.assetid: a5e87d88-4037-4302-99b7-179bfb03fac3
title: Bilder im Format "Stunde, Minute und Sekunde"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589c04fea0d6ce2f522436c30c39c873e3a7165e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050608"
---
# <a name="hour-minute-and-second-format-pictures"></a>Bilder im Format "Stunde, Minute und Sekunde"

Dieses Thema beschreibt die Format Typen für Zeichen folgen, die zum Verfassen des Format Bilds für eine Zeit Zeichenfolge verwendet werden. Jedes Format Bild besteht aus einer Kombination aus einer Zeichenfolge der einzelnen Format Typen.

> [!Note]  
> In den Format Typen müssen die Buchstaben "m", "s" und "t" in Kleinbuchstaben eingegeben werden, und der Buchstabe "h" muss klein geschrieben sein, um die 12-Stunden-Uhr oder den Großbuchstaben ("h") anzugeben, um den 24-Stunden-Takt anzugeben.

Einfache Anführungszeichen können verwendet werden, um Zeichen zu markieren, die genau wie angegeben angezeigt werden sollen. Wenn die Anwendung ein einzelnes Anführungszeichen anzeigen muss, sollte Sie zwei einfache Anführungszeichen in einer Zeile platzieren. Beispielsweise wird ' abc ' ' Bar ' als ' ABl-Leiste ' angezeigt.

In der folgenden Tabelle sind die Format Typen definiert, die zur Darstellung von Stunden verwendet werden.

| String | Bedeutung                                                             |
|--------|---------------------------------------------------------------------|
| h.      | Stunden ohne führende Nullen für Einstellige Stunden (12-Stunden-Takt). |
| hh     | Stunden mit führenden Nullen für Einstellige Stunden (12-Stunden-Takt).    |
| H      | Stunden ohne führende Nullen für Einstellige Stunden (24-Stunden-Takt). |
| HH     | Stunden mit führenden Nullen für Einstellige Stunden (24-Stunden-Takt).    |

In der folgenden Tabelle sind die Format Typen definiert, die zur Darstellung von Minuten verwendet werden.

| String | Bedeutung                                                 |
|--------|---------------------------------------------------------|
| m      | Minuten ohne führende Nullen für Einstellige Minuten. |
| MM     | Minuten mit führenden Nullen für Einstellige Minuten.    |

In der folgenden Tabelle sind die Format Typen definiert, die zur Darstellung von Sekunden verwendet werden.

| String | Bedeutung                                                 |
|--------|---------------------------------------------------------|
| s      | Sekunden ohne führende Nullen für Einstellige Sekunden. |
| ss     | Sekunden mit führenden Nullen für Einstellige Sekunden.    |

In der folgenden Tabelle sind die Format Typen definiert, die zur Darstellung eines Zeit Markers verwendet werden.

| String | Bedeutung|
| ---    | ---    |
| t      | Zeichenfolge mit einem Zeichen.<br />**Hinweis:** Dieses Format wird nicht für die Verwendung mit bestimmten Sprachen, wie z. b. Japanisch (Japan), empfohlen. Bei diesem Format übernimmt eine Anwendung immer das erste Zeichen aus der Zeit Marker-Zeichenfolge, die durch [LOCALE_S1159](locale-s1159.md) (am) und [LOCALE_S2359](locale-s2359.md) (PM) definiert wird. Aus diesem Grund kann die Anwendung eine falsche Formatierung mit derselben Zeichenfolge erstellen, die sowohl für am als auch für PM verwendet wird.|
| tt     | Zeichenfolge für Zeichen folgen mit mehreren Zeichen. |
