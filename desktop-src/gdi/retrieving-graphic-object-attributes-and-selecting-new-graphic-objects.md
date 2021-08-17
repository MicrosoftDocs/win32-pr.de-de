---
title: Abrufen von Objektattributen und Auswählen neuer Objekte
description: Eine Anwendung kann die Attribute für Einen Stift, Pinsel, Palette, Schriftart oder Bitmap abrufen, indem sie die Funktionen GetCurrentObject und GetObject aufruft.
ms.assetid: 09d8412f-a67d-48d5-9c04-9233dee43cf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c58d946f61a6a83dcfeb2ddae24d735d3596e5e864cf672bab832d7db3aedf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886145"
---
# <a name="retrieve-object-attributes-select-new-objects"></a>Abrufen von Objektattributen und Auswählen neuer Objekte

Eine Anwendung kann die Attribute für Einen Stift, Pinsel, Palette, Schriftart oder Bitmap abrufen, indem sie die Funktionen [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) und [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) aufruft. Die **GetCurrentObject-Funktion** gibt ein Handle zurück, das das derzeit im DC ausgewählte Objekt identifiziert. Die **GetObject-Funktion** gibt eine Struktur zurück, die die Attribute des Objekts beschreibt.

Das folgende Beispiel zeigt, wie eine Anwendung die aktuellen Pinselattribute abrufen und die abgerufenen Daten verwenden kann, um zu bestimmen, ob ein neuer Pinsel ausgewählt werden muss.


```C++
    HDC hdc;                     // display DC handle  
    HBRUSH hbrushNew, hbrushOld; // brush handles  
    HBRUSH hbrush;               // brush handle  
    LOGBRUSH lb;                 // logical-brush structure  
 
    // Retrieve a handle identifying the current brush.  
 
    hbrush = GetCurrentObject(hdc, OBJ_BRUSH); 
 
    // Retrieve a LOGBRUSH structure that contains the  
    // current brush attributes.  
 
    GetObject(hbrush, sizeof(LOGBRUSH), &lb); 
 
    // If the current brush is not a solid-black brush,  
    // replace it with the solid-black stock brush.  
 
    if ((lb.lbStyle != BS_SOLID) 
           || (lb.lbColor != 0x000000)) 
    { 
        hbrushNew = GetStockObject(BLACK_BRUSH); 
        hbrushOld = SelectObject(hdc, hbrushNew); 
    } 
 
    // Perform painting operations with the white brush.  
 
 
    // After completing the last painting operation with the new  
    // brush, the application should select the original brush back  
    // into the device context and delete the new brush.  
    // In this example, hbrushNew contains a handle to a stock object.  
    // It is not necessary (but it is not harmful) to call  
    // DeleteObject on a stock object. If hbrushNew contained a handle  
    // to a brush created by a function such as CreateBrushIndirect,  
    // it would be necessary to call DeleteObject.  
 
    SelectObject(hdc, hbrushOld); 
    DeleteObject(hbrushNew); 
```



> [!Note]
>
> Die Anwendung hat das ursprüngliche Pinselhandle beim ersten Aufruf der [**SelectObject-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) gespeichert. Dieses Handle wird gespeichert, sodass der ursprüngliche Pinsel wieder auf dem DC ausgewählt werden kann, nachdem der letzte Malvorgang mit dem neuen Pinsel abgeschlossen wurde. Nachdem der ursprüngliche Pinsel wieder auf dem DC ausgewählt wurde, wird der neue Pinsel gelöscht, wodurch Arbeitsspeicher im GDI-Heap freigegeben wird.

 

 

 



