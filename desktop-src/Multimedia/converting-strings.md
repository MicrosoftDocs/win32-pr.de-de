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
# <a name="converting-strings"></a><span data-ttu-id="2e590-104">Konvertieren von Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="2e590-104">Converting Strings</span></span>

<span data-ttu-id="2e590-105">Wenn Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion verwenden, sind alle mit dem-Befehl übergebenen Werte und alle Rückgabewerte Text Zeichenfolgen, sodass die Anwendung Konvertierungs Routinen benötigt, um von Variablen in Zeichen folgen oder wieder zurück zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="2e590-105">When you use the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function, all values passed with the command and all return values are text strings, so your application needs conversion routines to translate from variables to strings or back again.</span></span> <span data-ttu-id="2e590-106">Im folgenden Beispiel wird das Quell Rechteck abgerufen und die zurückgegebene Zeichenfolge in Rechteck Koordinaten konvertiert.</span><span class="sxs-lookup"><span data-stu-id="2e590-106">The following example retrieves the source rectangle and converts the returned string into rectangle coordinates.</span></span>


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
> <span data-ttu-id="2e590-107">**Rect** -Strukturen werden in MCI anders behandelt als in anderen Teilen von Windows. in MCI enthält das **Rechte** Element die Breite des Rechtecks, und der **untere** Member enthält seine Höhe.</span><span class="sxs-lookup"><span data-stu-id="2e590-107">**RECT** structures are handled differently in MCI than in other parts of Windows; in MCI, the **right** member contains the width of the rectangle and the **bottom** member contains its height.</span></span> <span data-ttu-id="2e590-108">In der Zeichen folgen Schnittstelle wird ein Rechteck als *x1*, *Y1*, *x2* und *Y2* angegeben.</span><span class="sxs-lookup"><span data-stu-id="2e590-108">In the string interface, a rectangle is specified as *X1*, *Y1*, *X2*, and *Y2*.</span></span> <span data-ttu-id="2e590-109">Die Koordinaten *x1* und *Y1* geben die linke obere Ecke des Rechtecks an, und die Koordinaten *x2* und *Y2* geben die Breite und Höhe an.</span><span class="sxs-lookup"><span data-stu-id="2e590-109">The coordinates *X1* and *Y1* specify the upper-left corner of the rectangle, and the coordinates *X2* and *Y2* specify the width and height.</span></span>

 

 

 