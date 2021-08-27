---
description: In diesem Thema werden die Formattypen für Zeichenfolgen beschrieben, mit denen das Formatbild für eine Zeitzeichenfolge erstellt wird. Jedes Formatbild besteht aus einer Kombination aus einer Zeichenfolge der einzelnen Formattypen.
ms.assetid: a5e87d88-4037-4302-99b7-179bfb03fac3
title: Bilder im Format "Stunde", "Minute" und "Sekunde"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e201e72e4da621334a46f20c47e1dd5f731d7ea443bb9970ce07bb7f4e5455
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130390"
---
# <a name="hour-minute-and-second-format-pictures"></a>Bilder im Format "Stunde", "Minute" und "Sekunde"

In diesem Thema werden die Formattypen für Zeichenfolgen beschrieben, mit denen das Formatbild für eine Zeitzeichenfolge erstellt wird. Jedes Formatbild besteht aus einer Kombination aus einer Zeichenfolge der einzelnen Formattypen.

> [!Note]  
> In den Formattypen müssen die Buchstaben "m", "s" und "t" Kleinbuchstaben sein, und der Buchstabe "h" muss Kleinbuchstaben sein, um die 12-Stunden-Uhr oder den Großbuchstaben ("H") zum Bezeichnen der 24-Stunden-Uhr zu bezeichnen.

Einfache Anführungszeichen können verwendet werden, um Zeichen zu markieren, die genau wie angegeben angezeigt werden sollen. Wenn die Anwendung ein einfaches Anführungszeichen anzeigen muss, sollte sie zwei einfache Anführungszeichen in einer Zeile platzieren. Beispielsweise wird "abc''bar' als "abc'bar" angezeigt.

In der folgenden Tabelle werden die Formattypen definiert, die zur Darstellung von Stunden verwendet werden.

| String | Bedeutung                                                             |
|--------|---------------------------------------------------------------------|
| h.      | Stunden ohne führende Nullen für einstellige Stunden (12-Stunden-Uhr). |
| hh     | Stunden mit führenden Nullen für einstellige Stunden (12-Stunden-Uhr).    |
| H      | Stunden ohne führende Nullen für einstellige Stunden (24-Stunden-Uhr). |
| HH     | Stunden mit führenden Nullen für einstellige Stunden (24-Stunden-Uhr).    |

In der folgenden Tabelle werden die Formattypen definiert, die für die Darstellung von Minuten verwendet werden.

| String | Bedeutung                                                 |
|--------|---------------------------------------------------------|
| m      | Minuten ohne führende Nullen für einstellige Minuten. |
| MM     | Minuten mit führenden Nullen für einstellige Minuten.    |

In der folgenden Tabelle werden die Formattypen definiert, die zur Darstellung von Sekunden verwendet werden.

| String | Bedeutung                                                 |
|--------|---------------------------------------------------------|
| s      | Sekunden ohne führende Nullen für einstellige Sekunden. |
| ss     | Sekunden mit führenden Nullen für einstellige Sekunden.    |

In der folgenden Tabelle werden die Formattypen definiert, die zum Darstellen eines Zeitmarkers verwendet werden.

| String | Bedeutung|
| ---    | ---    |
| t      | Ein-Zeichen-Zeitmarkierungszeichenfolge.<br />**Hinweis:** Dieses Format wird nicht für die Verwendung mit bestimmten Sprachen empfohlen, z. B. Japanisch (Japan). Bei diesem Format verwendet eine Anwendung immer das erste Zeichen [](locale-s1159.md) aus der Zeitmarkierungszeichenfolge, die durch LOCALE_S1159 (AM) und LOCALE_S2359 [(PM)](locale-s2359.md) definiert wird. Aus diesem Grund kann die Anwendung eine falsche Formatierung mit der gleichen Zeichenfolge erstellen, die für AM und PM verwendet wird.|
| tt     | Mehrzeichenige Zeitmarkerzeichenfolge. |
