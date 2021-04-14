---
description: Sie können die Menge an Zeichen, die Ihre Anwendung durchführt, bei der Verarbeitung der WM-Zeichnungs Nachricht begrenzen, \_ indem Sie die Größe und den Speicherort des Aktualisierungs Bereichs bestimmen.
ms.assetid: 3407014d-6427-45e9-8be4-b8037ca5438f
title: Neuzeichnen in der Aktualisierungs Region
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f90518db1a66b98fc7f4bd5961f2cfa581bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993879"
---
# <a name="redrawing-in-the-update-region"></a>Neuzeichnen in der Aktualisierungs Region

Sie können die Menge an Zeichen, die Ihre Anwendung durchführt, bei der Verarbeitung der WM-Zeichnungs Nachricht begrenzen, indem Sie die Größe und den Speicherort des Aktualisierungs Bereichs bestimmen. [**\_**](wm-paint.md) Da das System beim Erstellen des Clippingbereichs für den Gerätekontext des Fensters den Aktualisierungs Bereich verwendet, können Sie den Aktualisierungs Bereich indirekt ermitteln, indem Sie den Ausschneide Bereich untersuchen.

Im folgenden Beispiel zeichnet die Fenster Prozedur ein Dreieck, ein Rechteck, ein Pentagon und ein Sechseck, aber nur, wenn sich alle oder ein Teil jeder Abbildung innerhalb des Aktualisierungs Bereichs befindet. Die Fenster Prozedur verwendet die Funktion " [**rectvisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) " und ein "100-by-100"-Rechteck, um zu bestimmen, ob sich eine Abbildung im Ausschneide Bereich (und somit in der Update Region) für den gemeinsamen Gerätekontext befindet, der von [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)abgerufen wurde.


```C++
POINT aptTriangle[4]  = {50,2, 98,86,  2,86, 50,2}, 
      aptRectangle[5] = { 2,2, 98,2,  98,98,  2,98, 2,2}, 
      aptPentagon[6]  = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]   = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
  . 
  . 
  . 
 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            SetRect(&rc, 0, 0, 100, 100); 
 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptTriangle, 4); 
 
            SetViewportOrgEx(hdc, 100, 0, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptRectangle, 5); 
 
            SetViewportOrgEx(hdc, 0, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptPentagon, 6); 
 
            SetViewportOrgEx(hdc, 100, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptHexagon, 7); 
            EndPaint(hwnd, &ps); 
            return 0L; 
 
  . 
  . 
  . 
```



Die Koordinaten jeder Abbildung in diesem Beispiel liegen innerhalb desselben 100-by-100-Rechtecks. Vor dem Zeichnen einer Abbildung legt die Fenster Prozedur den Ansichts Anschluss mithilfe der [**setviewportorgex**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) -Funktion auf einen anderen Teil des Client Bereichs fest. Dadurch wird verhindert, dass Abbildungen oberhalb der anderen gezeichnet werden. Das Ändern des Ansichts Ansichts Ursprungs wirkt sich nicht auf den Clippingbereich aus, wirkt sich jedoch darauf aus, wie die Koordinaten des Rechtecks, das an [**rectvisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) übergeben wird Wenn Sie den Ursprung ändern, können Sie auch ein einzelnes Rechteck verwenden, um den Aktualisierungs Bereich anstelle einzelner Rechtecke für jede Abbildung zu überprüfen.

 

 



