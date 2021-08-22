---
title: Konvertieren von Zeichenfolgen
description: Konvertieren von Zeichenfolgen
ms.assetid: 40621c71-4264-40bc-b6c3-6b639d2f28fa
keywords:
- mciSendString-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efeb5801c46d89686ed3fe9fcf25b311d57d4d553c220902907ac0e70a5b7e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144793"
---
# <a name="converting-strings"></a>Konvertieren von Zeichenfolgen

Wenn Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) verwenden, sind alle mit dem Befehl übergebenen Werte und alle Rückgabewerte Textzeichenfolgen, sodass Ihre Anwendung Konvertierungsroutinen benötigt, um aus Variablen in Zeichenfolgen oder wieder zurück zu übersetzen. Im folgenden Beispiel wird das Quellrechteck abgerufen und die zurückgegebene Zeichenfolge in Rechteckkoordinaten konvertiert.


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
> **RECT-Strukturen** werden in MCI anders behandelt als in anderen Teilen von Windows. in MCI enthält das **rechte** Element die Breite des Rechtecks, und das **untere** Element enthält seine Höhe. In der Zeichenfolgenschnittstelle wird ein Rechteck als *X1,* *Y1,* *X2* und *Y2* angegeben. Die Koordinaten *X1* und *Y1* geben die obere linke Ecke des Rechtecks an, und die Koordinaten *X2* und *Y2* geben die Breite und Höhe an.

 

 

 