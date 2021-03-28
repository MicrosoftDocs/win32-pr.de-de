---
description: Dieser Abschnitt enthält ein Beispiel zur Veranschaulichung der Erstellung eines Bilds und des Prozesses, in dem die entsprechenden Datensätze in einer Metadatei gespeichert werden.
ms.assetid: 8be95fef-93dc-4c9c-a0d3-840918c00e43
title: Anzeigen eines Bilds und speichern in einer erweiterten Metadatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8eee65f2f82a7b8ccdad86e99987df6a06a4f5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754433"
---
# <a name="displaying-a-picture-and-storing-it-in-an-enhanced-metafile"></a><span data-ttu-id="2e985-103">Anzeigen eines Bilds und speichern in einer erweiterten Metadatei</span><span class="sxs-lookup"><span data-stu-id="2e985-103">Displaying a Picture and Storing It in an Enhanced Metafile</span></span>

<span data-ttu-id="2e985-104">Dieser Abschnitt enthält ein Beispiel zur Veranschaulichung der Erstellung eines Bilds und des Prozesses, in dem die entsprechenden Datensätze in einer Metadatei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2e985-104">This section contains an example demonstrating the creation of a picture and the process of storing the corresponding records in a metafile.</span></span> <span data-ttu-id="2e985-105">Im Beispiel wird ein Bild auf die Anzeige gezeichnet oder in einer Metadatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2e985-105">The example draws a picture to the display or stores it in a metafile.</span></span> <span data-ttu-id="2e985-106">Wenn ein Anzeigegeräte Kontext Handle angegeben ist, wird ein Bild mithilfe verschiedener GDI-Funktionen auf den Bildschirm gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2e985-106">If a display device context handle is given, it draws a picture to the screen using various GDI functions.</span></span> <span data-ttu-id="2e985-107">Wenn ein erweiterter Metadatei-Gerätekontext angegeben wird, wird das gleiche Bild in der erweiterten Metadatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2e985-107">If an enhanced metafile device context is given, it stores the same picture in the enhanced metafile.</span></span>


```C++
void DrawOrStore(HWND hwnd, HDC hdcMeta, HDC hdcDisplay) 
{ 
 
RECT rect; 
HDC hDC; 
int fnMapModeOld; 
HBRUSH hbrOld; 
 
// Draw it to the display DC or store it in the metafile device context.  
 
if (hdcMeta) 
    hDC = hdcMeta; 
else 
    hDC = hdcDisplay; 
 
// Set the mapping mode in the device context.  
 
fnMapModeOld = SetMapMode(hDC, MM_LOENGLISH); 
 
// Find the midpoint of the client area.  
 
GetClientRect(hwnd, (LPRECT)&rect); 
DPtoLP(hDC, (LPPOINT)&rect, 2); 
 
// Select a gray brush.  
 
hbrOld = SelectObject(hDC, GetStockObject(GRAY_BRUSH)); 
 
// Draw a circle with a one inch radius.  
 
Ellipse(hDC, (rect.right/2 - 100), (rect.bottom/2 + 100), 
       (rect.right/2 + 100), (rect.bottom/2 - 100)); 
 
// Perform additional drawing here.  
 
 
 
// Set the device context back to its original state.  
 
SetMapMode(hDC, fnMapModeOld); 
SelectObject(hDC, hbrOld); 
} 
```



 

 



