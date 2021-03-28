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
# <a name="retrieve-object-attributes-select-new-objects"></a><span data-ttu-id="b42f4-103">Objekt Attribute abrufen, neue Objekte auswählen</span><span class="sxs-lookup"><span data-stu-id="b42f4-103">Retrieve object attributes, select new objects</span></span>

<span data-ttu-id="b42f4-104">Eine Anwendung kann die Attribute für einen Stift, einen Pinsel, eine Palette, eine Schriftart oder eine Bitmap abrufen, indem Sie die Funktionen [**getcurrentobject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) und [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) aufruft.</span><span class="sxs-lookup"><span data-stu-id="b42f4-104">An application can retrieve the attributes for a pen, brush, palette, font, or bitmap by calling the [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) and [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) functions.</span></span> <span data-ttu-id="b42f4-105">Die **getcurrentobject** -Funktion gibt ein Handle zurück, das das derzeit im DC ausgewählte Objekt identifiziert. die **GetObject** -Funktion gibt eine-Struktur zurück, die die Attribute des-Objekts beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b42f4-105">The **GetCurrentObject** function returns a handle identifying the object currently selected into the DC; the **GetObject** function returns a structure that describes the attributes of the object.</span></span>

<span data-ttu-id="b42f4-106">Das folgende Beispiel zeigt, wie eine Anwendung die aktuellen Pinsel Attribute abrufen und die abgerufenen Daten verwenden kann, um zu bestimmen, ob es erforderlich ist, einen neuen Pinsel auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="b42f4-106">The following example shows how an application can retrieve the current brush attributes and use the retrieved data to determine whether it is necessary to select a new brush.</span></span>


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
> <span data-ttu-id="b42f4-107">Die Anwendung hat den ursprünglichen Pinsel Handle beim ersten Aufrufen der [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b42f4-107">The application saved the original brush handle when calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function the first time.</span></span> <span data-ttu-id="b42f4-108">Dieses Handle wird gespeichert, sodass der ursprüngliche Pinsel wieder in den DC ausgewählt werden kann, nachdem der letzte Zeichnungs Vorgang mit dem neuen Pinsel abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="b42f4-108">This handle is saved so that the original brush can be selected back into the DC after the last painting operation has been completed with the new brush.</span></span> <span data-ttu-id="b42f4-109">Nachdem der Original Pinsel wieder in den Domänen Controller ausgewählt wurde, wird der neue Pinsel gelöscht und gibt Speicher im GDI-Heap frei.</span><span class="sxs-lookup"><span data-stu-id="b42f4-109">After the original brush is selected back into the DC, the new brush is deleted, freeing memory in the GDI heap.</span></span>

 

 

 



