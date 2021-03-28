---
description: Das System stellt sechs Aktien Schriftarten bereit.
ms.assetid: 349ea57f-dd25-4e33-bbdf-63a320eae3a0
title: Verwenden einer Kurs Schriftart zum Zeichnen von Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a7e580175956185bcc26a7ebbae8d46dfff078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960517"
---
# <a name="using-a-stock-font-to-draw-text"></a>Verwenden einer Kurs Schriftart zum Zeichnen von Text

Das System stellt sechs Aktien Schriftarten bereit. Eine Aktien Schriftart ist eine logische Schriftart, die eine Anwendung abrufen kann, indem Sie die [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) -Funktion aufrufen und die angeforderte Schriftart angibt. Die folgende Liste enthält die Werte, die Sie angeben können, um eine Aktien Schriftart zu erhalten.



| Wert                 | Bedeutung                                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ANSI \_ - \_ Schriftart     | Gibt eine fest breiten-Schriftart an, die auf dem Windows-Zeichensatz basiert. In der Regel wird eine Courier Schriftart verwendet.                                                                                                                                                                                                |
| ANSI \_ var- \_ Schriftart       | Gibt eine proportionale Schriftart basierend auf dem Windows-Zeichensatz an. MS Sans Serif wird normalerweise verwendet.                                                                                                                                                                                              |
| \_Standard \_ Schriftart des Geräts | Gibt die bevorzugte Schriftart für das angegebene Gerät an. Dies ist in der Regel die System Schriftart für Anzeigegeräte. bei einigen Punktmatrix Druckern ist dies jedoch eine Schriftart, die sich auf dem Gerät befindet. (Das Drucken mit dieser Schriftart ist in der Regel schneller als das Drucken mit einer heruntergeladenen Bitmapschriftart).    |
| \_Schriftart für festes OEM \_      | Gibt eine fest breiten-Schriftart an, die auf einem OEM-Zeichensatz basiert. Bei IBM-Computern und-Kompatibilitäten basiert die OEM-Schriftart auf dem IBM-PC-Zeichensatz.                                                                                                                                                 |
| System \_ Schriftart          | Gibt die System Schriftart an. Dabei handelt es sich um eine proportionale Schriftart, die auf dem Windows-Zeichensatz basiert und vom Betriebssystem verwendet wird, um Fenstertitel, Menü Namen und Text in Dialogfeldern anzuzeigen. Die System Schriftart ist immer verfügbar. Andere Schriftarten sind nur verfügbar, wenn Sie installiert wurden. |
| \_Schriftart des fixierten Systems \_   | Gibt eine fest breiten-Schriftart an, die in frühen Versionen von Windows mit der System Schriftart kompatibel ist.                                                                                                                                                                                                        |



 

Weitere Informationen zu Schriftarten finden Sie unter Informationen [zu Schriftarten](about-fonts.md).

Im folgenden Beispiel wird ein Handle der Variablen Aktien Schriftart abgerufen, in einen Gerätekontext ausgewählt und dann mithilfe der Schriftart eine Zeichenfolge geschrieben:


```C++
HFONT hFont, hOldFont; 

// Retrieve a handle to the variable stock font.  
hFont = (HFONT)GetStockObject(ANSI_VAR_FONT); 

// Select the variable stock font into the specified device context. 
if (hOldFont = (HFONT)SelectObject(hdc, hFont)) 
{
    // Display the text string.  
    TextOut(hdc, 10, 50, L"Sample ANSI_VAR_FONT text", 25); 

    // Restore the original font.        
    SelectObject(hdc, hOldFont); 
}
```



Wenn keine anderen Aktien Schriftarten verfügbar sind, gibt [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) ein Handle für die System Schriftart (System \_ Schriftart) zurück. Sie sollten nur dann Stock Fonts verwenden, wenn der Kartenmodus für den Gerätekontext der Anwendung mm- \_ Text ist.

 

 



