---
title: Konvertieren von Zeichenfolgen
description: Konvertieren von Zeichenfolgen
ms.assetid: 40621c71-4264-40bc-b6c3-6b639d2f28fa
keywords:
- mciSendString-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1db4cb4b3d02a93adecc82d6ce95de436fb2e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948612"
---
# <a name="converting-strings"></a>Konvertieren von Zeichenfolgen

Wenn Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion verwenden, sind alle mit dem-Befehl übergebenen Werte und alle Rückgabewerte Text Zeichenfolgen, sodass die Anwendung Konvertierungs Routinen benötigt, um von Variablen in Zeichen folgen oder wieder zurück zu übersetzen. Im folgenden Beispiel wird das Quell Rechteck abgerufen und die zurückgegebene Zeichenfolge in Rechteck Koordinaten konvertiert.


```C++
BOOL GetSourceRect(LPTSTR lpstrAlias, LPRECT lprc) 
{ 
    TCHAR achRetBuff[128]; 
    TCHAR achCommandBuff[128]; 

    int result;
    MCIERROR err;
 
    // Build the command string. 
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("where %s source"), 
        lpstrAlias); 

    if (result == -1)
    {
        return FALSE;
    }
    
    // Clear the RECT.
    SetRectEmpty(lprc);
 
    // Send the MCI command. 
    err = mciSendString(
        achCommandBuff, 
        achRetBuff, 
        sizeof(achRetBuff), 
        NULL);

    if (err != 0)
    {
        return FALSE;
    }
        
    // The rectangle is returned as "x y dx dy". 
    // Translate the string into the RECT structure. 

    // Warning: This example omits error checking
    // for the _tcstok_s and _tstoi functions.
    TCHAR *p; 
    TCHAR *context;

    // Left.
    p = _tcstok_s(achRetBuff, TEXT(" "), &context);
    lprc->left = _tstoi(p);

    // Top.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->top = _tstoi(p);

    // Right.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->right = _tstoi(p);
    
    // Bottom.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->bottom = _tstoi(p);

    return TRUE;
}
 
```



> [!Note]  
> **Rect** -Strukturen werden in MCI anders behandelt als in anderen Teilen von Windows. in MCI enthält das **Rechte** Element die Breite des Rechtecks, und der **untere** Member enthält seine Höhe. In der Zeichen folgen Schnittstelle wird ein Rechteck als *x1*, *Y1*, *x2* und *Y2* angegeben. Die Koordinaten *x1* und *Y1* geben die linke obere Ecke des Rechtecks an, und die Koordinaten *x2* und *Y2* geben die Breite und Höhe an.

 

 

 