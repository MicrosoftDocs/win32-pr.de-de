---
description: Die Anwendung verwendet die in diesem Thema beschriebenen Elemente zum Erstellen einer Bild Zeichenfolge mit einem null-terminierten Format.
ms.assetid: c18868a9-6912-46fd-93f5-d8021937b049
title: Format Abbildungen für Tag, Monat, Jahr und ERA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c83439cc33c1caf067b5c6f41234a6f1ddc4dcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867935"
---
# <a name="day-month-year-and-era-format-pictures"></a>Format Abbildungen für Tag, Monat, Jahr und ERA

Die Anwendung verwendet die in diesem Thema beschriebenen Elemente zum Erstellen einer Bild Zeichenfolge mit einem null-terminierten Format. Wenn Leerzeichen verwendet werden, um die Elemente in der Zeichenfolge zu trennen, werden diese Leerzeichen an derselben Position in der Ausgabe Zeichenfolge angezeigt.

> [!Note]  
> Die Format Typen "d", "g" und "y" müssen in Kleinbuchstaben angegeben werden, und der Buchstabe "M" muss in Großbuchstaben angegeben werden.

 

Um z. b. die Datums Zeichenfolge "Wed, Aug 31 94" zu erhalten, verwendet die Anwendung die Bild Zeichenfolge "ddd", "MMM dd yy".

Die Anwendung verwendet einfache Anführungszeichen, um Zeichen so zu markieren, dass Sie genau wie angegeben angezeigt werden. Wenn die Anwendung ein einzelnes Anführungszeichen anzeigen muss, sollte Sie zwei einfache Anführungszeichen in einer Zeile platzieren. Beispielsweise wird ' abc ' ' Bar ' als ' ABl-Leiste ' angezeigt.

In der folgenden Tabelle sind die Format Typen definiert, die zur Darstellung von Tagen verwendet werden.



| Formattyp | Bedeutung                                                                                                                                                                                                                                                                                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| d           | Tag des Monats als Ziffern ohne führende Nullen für Einstellige Tage.                                                                                                                                                                                                                                                                                                   |
| dd          | Tag des Monats als Ziffern mit führenden Nullen für Einstellige Tage.                                                                                                                                                                                                                                                                                                      |
| ddd         | Abgekürzte Wochentag, wie durch einen Gebiets Schema- [ \_ sabbrevdayname \*](locale-sabbrev-constants.md) -Wert angegeben, z. b. "Mon" in englischer Sprache (USA).**Windows Vista und höher:** wenn eine kurze Version des Wochentags erforderlich ist, sollte Ihre Anwendung das [Gebiets Schema \_ sshortestdayname \*](locale-sshortestdayname-constants.md) -Konstanten verwenden.<br/> |
| dddd        | Der Tag der Woche gemäß Angabe durch den Wert eines [locale \_ sdayname \* ](locale-sdayname-constants.md) -Werts.                                                                                                                                                                                                                                                                              |



 

In der folgenden Tabelle sind die Format Typen definiert, die zur Darstellung von Monaten verwendet werden.



| Formattyp | Bedeutung                                                                                                                                                                          |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| M           | Monat als Ziffern ohne führende Nullen für einstellige Monate.                                                                                                                   |
| MM          | Monat als Ziffern mit führenden Nullen für einstellige Monate.                                                                                                                      |
| MMM         | Abgekürzte Monat, wie durch einen Gebiets Schema- [ \_ sabbrevmonthname \* ](locale-sabbrev-constants.md) -Wert angegeben, z. b. "Nov" in englischer Sprache (USA).                             |
| MMMM        | Der von einem Gebiets Schema [- \_ smonthname \* ](locale-smonthname-constants.md) -Wert angegebene Monat, z. b. "November" für Englisch (USA) und "Noviembre" für Spanisch (Spanien). |



 

In der folgenden Tabelle sind die Format Typen definiert, die zur Darstellung von Jahren verwendet werden.



| Formattyp | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Y           | Jahr, das nur durch die letzte Ziffer dargestellt wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| yy          | Jahr, das nur durch die letzten zwei Ziffern dargestellt wird. Für einstellige Jahre wird eine führende Null hinzugefügt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| yyyy        | Jahr, das durch eine vollständige vier oder fünf Ziffern dargestellt wird, je nach verwendetem Kalender. Thailändische und koreanische Kalender haben fünfstellige Jahre. Das Muster "yyyy" zeigt fünf Ziffern für diese beiden Kalender und vier Ziffern für alle anderen unterstützten Kalender. Kalender mit einstelligen oder zweistelligen Jahres Angaben, z. b. für den japanischen Kaiser, werden unterschiedlich dargestellt. Eine einstellige Jahres Angabe wird mit einer führenden Null dargestellt, z. b. "03". Eine zweistellige Jahres Angabe wird mit zwei Ziffern dargestellt, z. b. "13". Es werden keine weiteren führenden Nullen angezeigt. |
| yyyyy       | Verhält sich identisch mit "yyyy".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

In der folgenden Tabelle sind die Format Typen definiert, die zur Darstellung eines Zeitraums oder eines Zeitraums verwendet werden.



| Formattyp | Bedeutung                                                                                                                                                                              |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g, GG       | Die Zeichenfolge für den Zeitraum/die Ära ist gemäß dem Wert der CAL- \_ Server Zeichenfolge formatiert Die Format Abbildungen "g" und "gg" in einer Datums Zeichenfolge werden ignoriert, wenn keine zugeordnete Zeit-oder Zeit Zeichenfolge vorhanden ist. |



 

 

 




