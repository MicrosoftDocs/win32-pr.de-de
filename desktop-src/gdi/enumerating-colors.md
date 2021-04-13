---
description: Sie können bestimmen, wie viele Farben ein Gerät unterstützt und welche Farben Dies sind, indem Sie die Anzahl der Farben für das Gerät abrufen und die Farben der ausgezisten Stifte auflisten.
ms.assetid: cbaa3732-e55e-42af-93de-390450d38fc9
title: Auflisten von Farben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca39ec9817ecab07c2c2bc42b08fbee83333f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978616"
---
# <a name="enumerating-colors"></a>Auflisten von Farben

Sie können bestimmen, wie viele Farben ein Gerät unterstützt und welche Farben Dies sind, indem Sie die Anzahl der Farben für das Gerät abrufen und die Farben der ausgezisten Stifte auflisten. Verwenden Sie zum Abrufen der Anzahl von Farben die [**gettovicecaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion mit dem numcolors-Wert. Verwenden Sie zum Auflisten von ausgehosten listeneln die [**enumubjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) -Funktion und eine entsprechende Rückruffunktion, die Informationen zu jedem Stift empfängt.


```C++
// GetTheColors - returns the count and color values of solid colors 
// Returns a pointer to the array containing colors 
// hdc - handle to device context 

COLORREF *GetTheColors(HDC hdc)
{
    int cColors;
    COLORREF *aColors;

    // Get the number of colors. 
    cColors = GetDeviceCaps(hdc, NUMCOLORS);

    // Allocate space for the array. 
    aColors = (COLORREF *)LocalAlloc(LPTR, sizeof(COLORREF) * 
        (cColors+1));

    // Save the count of colors in first element. 
    aColors[0] = (LONG)cColors;

    // Enumerate all pens and save solid colors in the array. 
    EnumObjects(hdc, OBJ_PEN, (GOBJENUMPROC)MyEnumProc, (LONG)aColors);

    // Refresh the count of colors. 
    aColors[0] = (LONG)cColors;

    return aColors;
}

int MyEnumProc(LPVOID lp, LPBYTE lpb)
{
    LPLOGPEN lopn;
    COLORREF *aColors;
    int iColor;

    lopn = (LPLOGPEN)lp;
    aColors = (COLORREF *)lpb;

    if (lopn->lopnStyle==PS_SOLID) 
    {
        // Check for too many colors. 
        if ((iColor = (int)aColors[0]) <= 0)
             return 0;
        aColors[iColor] = lopn->lopnColor;
        aColors[0]--;
    }
    return 1;
}
```



 

 



