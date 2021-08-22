---
description: Das System bietet sechs Stockfonts.
ms.assetid: 349ea57f-dd25-4e33-bbdf-63a320eae3a0
title: Verwenden einer Stock Font zum Zeichnen von Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9bd140a931a13f6232235036fb7b9cf3de1a20505666e869f214219b7a60a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468330"
---
# <a name="using-a-stock-font-to-draw-text"></a>Verwenden einer Stock Font zum Zeichnen von Text

Das System bietet sechs Stockfonts. Eine Stock-Schriftart ist eine logische Schriftart, die eine Anwendung durch Aufrufen der [GetStockObject-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) und Angeben der angeforderten Schriftart abrufen kann. Die folgende Liste enthält die Werte, die Sie angeben können, um eine Kursschriftart zu erhalten.



| Wert                 | Bedeutung                                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ANSI \_ FIXED \_ FONT     | Gibt eine Monospaceschriftart basierend auf dem zeichenbasierten Windows an. In der Regel wird eine Courier-Schriftart verwendet.                                                                                                                                                                                                |
| SCHRIFTART "ANSI \_ \_ VAR"       | Gibt eine proportionale Schriftart basierend auf dem zeichenbasierten Windows an. MS Sans Serif wird in der Regel verwendet.                                                                                                                                                                                              |
| \_STANDARDSCHRIFTART DES \_ GERÄTS | Gibt die bevorzugte Schriftart für das angegebene Gerät an. Dies ist in der Regel die Schriftart System für Anzeigegeräte. Bei einigen Punktmatrixdruckern ist dies jedoch eine Schriftart, die sich auf dem Gerät befindet. (Das Drucken mit dieser Schriftart ist in der Regel schneller als das Drucken mit einer heruntergeladenen Bitmapschriftart.)    |
| FESTE \_ \_ OEM-SCHRIFTART      | Gibt eine Monospaceschriftart basierend auf einem OEM-Zeichensatz an. Bei IBM-Computern und -Kompatiblen basiert die OEM-Schriftart auf dem IBM PC-Zeichensatz.                                                                                                                                                 |
| \_SYSTEMSCHRIFTART          | Gibt die Schriftart System an. Dies ist eine proportionale Schriftart, die auf Windows Zeichensatz basiert und vom Betriebssystem verwendet wird, um Fenstertitel, Menünamen und Text in Dialogfeldern anzuzeigen. Die Schriftart System ist immer verfügbar. Andere Schriftarten sind nur verfügbar, wenn sie installiert wurden. |
| FESTE \_ \_ SYSTEMSCHRIFTART   | Gibt eine Monospaceschriftart an, die mit der Schriftart System in frühen Versionen von Windows.                                                                                                                                                                                                        |



 

Weitere Informationen zu Schriftarten finden Sie unter [Informationen zu Schriftarten.](about-fonts.md)

Im folgenden Beispiel wird ein Handle für die Stockschriftart der Variablen abgerufen, in einen Gerätekontext ausgewählt und dann eine Zeichenfolge mit dieser Schriftart schreibt:


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



Wenn andere Stockfonts nicht verfügbar sind, [gibt GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) ein Handle an die Schriftart System (SYSTEM \_ FONT) zurück. Sie sollten stock fonts nur verwenden, wenn der Zuordnungsmodus für den Gerätekontext Ihrer Anwendung MM \_ TEXT ist.

 

 



