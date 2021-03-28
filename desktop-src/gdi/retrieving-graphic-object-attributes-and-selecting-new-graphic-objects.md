---
title: Objekt Attribute abrufen, neue Objekte auswählen
description: Eine Anwendung kann die Attribute für einen Stift, einen Pinsel, eine Palette, eine Schriftart oder eine Bitmap abrufen, indem Sie die Funktionen getcurrentobject und GetObject aufruft.
ms.assetid: 09d8412f-a67d-48d5-9c04-9233dee43cf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b18dcef03bf769e8b2d11574429b64f481b1a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978304"
---
# <a name="retrieve-object-attributes-select-new-objects"></a>Objekt Attribute abrufen, neue Objekte auswählen

Eine Anwendung kann die Attribute für einen Stift, einen Pinsel, eine Palette, eine Schriftart oder eine Bitmap abrufen, indem Sie die Funktionen [**getcurrentobject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) und [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) aufruft. Die **getcurrentobject** -Funktion gibt ein Handle zurück, das das derzeit im DC ausgewählte Objekt identifiziert. die **GetObject** -Funktion gibt eine-Struktur zurück, die die Attribute des-Objekts beschreibt.

Das folgende Beispiel zeigt, wie eine Anwendung die aktuellen Pinsel Attribute abrufen und die abgerufenen Daten verwenden kann, um zu bestimmen, ob es erforderlich ist, einen neuen Pinsel auszuwählen.


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
> Die Anwendung hat den ursprünglichen Pinsel Handle beim ersten Aufrufen der [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion gespeichert. Dieses Handle wird gespeichert, sodass der ursprüngliche Pinsel wieder in den DC ausgewählt werden kann, nachdem der letzte Zeichnungs Vorgang mit dem neuen Pinsel abgeschlossen wurde. Nachdem der Original Pinsel wieder in den Domänen Controller ausgewählt wurde, wird der neue Pinsel gelöscht und gibt Speicher im GDI-Heap frei.

 

 

 



