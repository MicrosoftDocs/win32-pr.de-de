---
description: Ein Ausschneidebereich ist eines der Grafikobjekte, die eine Anwendung in einem Gerätekontext (DC) auswählen kann.
ms.assetid: d9238ee5-3305-4e85-aef3-2c5c8b74aacd
title: Ausschneiden von Regionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0647d44d82e289b702e9111b62c5a138c8a0fa059428a6173af36f4eeca657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105915"
---
# <a name="clipping-regions"></a>Ausschneiden von Regionen

Ein Ausschneidebereich ist eines der Grafikobjekte, die eine Anwendung in einem Gerätekontext (DC) auswählen kann. Sie ist in der Regel rechteckig. Einige Gerätekontexte bieten einen vordefinierten oder standardmäßigen Ausschneidebereich, andere nicht. Wenn Sie beispielsweise ein Gerätekontexthandl von der [**BeginPaint-Funktion**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) abrufen, enthält der DC einen vordefinierten rechteckigen Ausschneidebereich, der dem ungültigen Rechteck entspricht, das neu gepaint werden muss. Wenn Sie jedoch ein Gerätekontexthandler abrufen, indem Sie die [**GetDC-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdc) mit einem **NULL**_hWnd-Parameter_ aufrufen oder indem Sie die [**CreateDC-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) aufrufen, enthält der Domänencontroller keinen Standardausschneidebereich. Weitere Informationen zu Gerätekontexten, die von der **BeginPaint-Funktion zurückgegeben** werden, finden Sie unter [Zeichnen und Zeichnen](painting-and-drawing.md) von . Weitere Informationen zu Gerätekontexten, die von den **Funktionen CreateDC** und **GetDC** zurückgegeben werden, finden Sie unter [Gerätekontexte.](device-contexts.md)

Anwendungen können eine Vielzahl von Vorgängen für Ausschneideregionen ausführen. Einige dieser Vorgänge erfordern ein Handle, das die Region identifiziert, andere nicht. Beispielsweise kann eine Anwendung die folgenden Vorgänge direkt im Ausschneidebereich eines Gerätekontexts ausführen.

-   Bestimmen Sie, ob die Grafikausgabe innerhalb der Rahmen der Region angezeigt wird, indem Sie Koordinaten der entsprechenden Linie, des Bogens, der Bitmap, des Texts oder der ausgefüllten Form an die [**PtVisible-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible) übergeben.
-   Bestimmen Sie, ob ein Teil des Clientbereichs eine Region überschneidet, indem Sie die [**RectVisible-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) aufrufen.
-   Verschieben Sie den vorhandenen Bereich um einen angegebenen Offset, indem Sie die [**OffsetClipRgn-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn) aufrufen.
-   Schließen Sie einen rechteckigen Teil des Clientbereichs aus dem aktuellen Ausschneidebereich aus, indem Sie die [**ExcludeClipRect-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect) aufrufen.
-   Kombinieren Sie einen rechteckigen Teil des Clientbereichs mit dem aktuellen Ausschneidebereich, indem Sie die [**IntersectClipRect-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) aufrufen.

Nach dem Abrufen eines Handles, das den Ausschneidebereich identifiziert, kann eine Anwendung einen beliebigen Vorgang ausführen, der für Regionen üblich ist, z. B.:

-   Kombinieren einer Kopie des aktuellen Clippingbereichs mit einer zweiten Region durch Aufrufen der [**CombineRgn-Funktion.**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn)
-   Vergleichen Sie eine Kopie des aktuellen Ausschneidebereichs mit einer zweiten Region, indem Sie die [**EqualRgn-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-equalrgn) aufrufen.
-   Bestimmen Sie, ob sich ein Punkt innerhalb einer Kopie des aktuellen Ausschneidebereichs befindet, indem Sie die [**PtInRegion-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) aufrufen.

 

 



