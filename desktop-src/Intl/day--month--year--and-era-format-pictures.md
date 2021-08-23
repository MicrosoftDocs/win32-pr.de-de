---
description: Die Anwendung verwendet die in diesem Thema beschriebenen Elemente, um eine auf NULL endende Formatbildzeichenfolge zu erstellen.
ms.assetid: c18868a9-6912-46fd-93f5-d8021937b049
title: Bilder im Format "Day", "Month", "Year" und "Era"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ae1adf82a202ebb08f199bb252e59c0f35aab8ad35b60ac57a8ebbe102711c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068270"
---
# <a name="day-month-year-and-era-format-pictures"></a>Bilder im Format "Day", "Month", "Year" und "Era"

Die Anwendung verwendet die in diesem Thema beschriebenen Elemente, um eine auf NULL endende Formatbildzeichenfolge zu erstellen. Wenn Leerzeichen verwendet werden, um die Elemente in der Zeichenfolge zu trennen, werden diese Leerzeichen an der gleichen Position in der Ausgabezeichenfolge angezeigt.

> [!Note]  
> Die Formattypen "d", "g" und "y" müssen klein geschrieben sein, und der Buchstabe "M" muss groß geschrieben sein.

 

Um beispielsweise die Datumszeichenfolge "Wed, Aug 31 94" abzurufen, verwendet die Anwendung die Bildzeichenfolge "ddd',' MMM dd yy".

Die Anwendung verwendet einfache Anführungszeichen, um Zeichen so zu markieren, dass sie genau wie angegeben angezeigt werden. Wenn die Anwendung ein einfaches Anführungszeichen anzeigen muss, sollten zwei einfache Anführungszeichen in eine Zeile gesetzt werden. Beispielsweise wird 'abc''bar' als "abc'bar" angezeigt.

In der folgenden Tabelle werden die Formattypen definiert, die zur Darstellung von Tagen verwendet werden.



| Formattyp | Bedeutung                                                                                                                                                                                                                                                                                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| d           | Tag des Monats als Ziffern ohne führende Nullen für einstellige Tage.                                                                                                                                                                                                                                                                                                   |
| dd          | Tag des Monats als Ziffern mit führenden Nullen für einstellige Tage.                                                                                                                                                                                                                                                                                                      |
| ddd         | Abgekürzter Tag der Woche, wie durch einen [ \_ LOCALE-WERT \* VOM TAGBREVDAYNAME](locale-sabbrev-constants.md) angegeben, z. B. "Mon" auf Englisch (USA).**Windows Vista und höher:** Wenn eine kurze Version des Wochentags erforderlich ist, sollte Ihre Anwendung die [ \_ LOCALE-Konstanten SSHORTESTDAYNAME \*](locale-sshortestdayname-constants.md) verwenden.<br/> |
| dddd        | Tag der Woche, wie durch einen [LOCALE \_ \* SDAYNAME-Wert](locale-sdayname-constants.md) angegeben.                                                                                                                                                                                                                                                                              |



 

In der folgenden Tabelle werden die Formattypen definiert, die verwendet werden, um Monate darzustellen.



| Formattyp | Bedeutung                                                                                                                                                                          |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| M           | Monat als Ziffern ohne führende Nullen für einstellige Monate.                                                                                                                   |
| MM          | Monat als Ziffern mit führenden Nullen für einstellige Monate.                                                                                                                      |
| MMM         | Abgekürzter Monat, wie durch einen [ \_ \* LOCALE-WERT VOMBREVMONTHNAME](locale-sabbrev-constants.md) angegeben, z.B. "November" auf Englisch (USA).                             |
| MMMM        | Monat, wie durch einen [LOCALE \_ \* SMONTHNAME-Wert](locale-smonthname-constants.md) angegeben, z. B. "November" für Englisch (USA) und "Quotimembre" für Spanisch (Spanien). |



 

In der folgenden Tabelle werden die Formattypen definiert, die für die Darstellung von Jahren verwendet werden.



| Formattyp | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| y           | Jahr, das nur durch die letzte Ziffer dargestellt wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| yy          | Jahr, das nur durch die letzten beiden Ziffern dargestellt wird. Für einstellige Jahre wird eine führende Null hinzugefügt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| yyyy        | Jahr, dargestellt durch vollständige vier oder fünf Ziffern, abhängig vom verwendeten Kalender. Thailändische und koreanische Kalender haben fünfstellige Jahre. Das Muster "yyyy" zeigt fünf Ziffern für diese beiden Kalender und vier Ziffern für alle anderen unterstützten Kalender an. Kalender mit ein- oder zweistelligen Jahren, z. B. für die japanische Epoche, werden unterschiedlich dargestellt. Ein einstelliges Jahr wird mit einer führenden Null dargestellt, z.B. "03". Ein zweistelliges Jahr wird mit zwei Ziffern dargestellt, z.B. "13". Es werden keine zusätzlichen führenden Nullen angezeigt. |
| yyyyy       | Verhält sich identisch mit "yyyy".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

In der folgenden Tabelle werden die Formattypen definiert, die verwendet werden, um einen Punkt oder zeitraum darzustellen.



| Formattyp | Bedeutung                                                                                                                                                                              |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g, gg       | Period/era string formatiert, wie durch den \_ CAL-WERT VONSTRING angegeben. Die Bilder im Format "g" und "gg" in einer Datumszeichenfolge werden ignoriert, wenn kein Zeitraum oder eine Punktzeichenfolge zugeordnet ist. |



 

 

 




