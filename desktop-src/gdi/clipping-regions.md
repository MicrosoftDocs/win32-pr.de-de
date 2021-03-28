---
description: Ein Ausschneide Bereich ist eines der Grafik Objekte, die von einer Anwendung in einen Gerätekontext (DC) ausgewählt werden können.
ms.assetid: d9238ee5-3305-4e85-aef3-2c5c8b74aacd
title: Clipping-Bereiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a830e05b2a9ce709183f23fad66f937c8c512acd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130829"
---
# <a name="clipping-regions"></a>Clipping-Bereiche

Ein Ausschneide Bereich ist eines der Grafik Objekte, die von einer Anwendung in einen Gerätekontext (DC) ausgewählt werden können. Es ist in der Regel rechteckig. Einige Geräte Kontexte stellen einen vordefinierten oder standardmäßigen Clippingbereich bereit, andere hingegen nicht. Wenn Sie z. b. ein Gerätekontext Handle von der [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) -Funktion abrufen, enthält der DC einen vordefinierten, rechteckigen Clippingbereich, der dem ungültigen Rechteck entspricht, das neu gezeichnet werden muss. Wenn Sie jedoch ein Gerätekontext handle abrufen, indem Sie die [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -Funktion mit einem **null**-_HWND_ -Parameter aufrufen, oder indem Sie die [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) -Funktion aufrufen, enthält der DC keinen standardmäßigen Clippingbereich. Weitere Informationen zu den von der **BeginPaint** -Funktion zurückgegebenen Geräte Kontexten finden Sie unter [Zeichnen und zeichnen](painting-and-drawing.md) . Weitere Informationen zu den von den Funktionen " **kreatedc** " und " **GetDC** " zurückgegebenen Geräte Kontexten finden Sie unter [Geräte Kontexte](device-contexts.md).

Anwendungen können eine Vielzahl von Vorgängen für Clippingbereiche durchführen. Einige dieser Vorgänge erfordern ein Handle, das den Bereich identifiziert, und einige nicht. Beispielsweise kann eine Anwendung die folgenden Vorgänge direkt in einem Clippingbereich eines Geräte Kontexts ausführen.

-   Bestimmen Sie, ob die Grafikausgabe innerhalb der Grenzen des Bereichs angezeigt wird, indem Sie Koordinaten der entsprechenden Zeile, des Bogens, der Bitmap, des Texts oder der gefüllten Form an die [**ptvisible**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible) -Funktion übergeben.
-   Bestimmen Sie, ob ein Teil des Client Bereichs durch Aufrufen der Funktion " [**rectvisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) " einen Bereich überschneidet.
-   Verschieben Sie den vorhandenen Bereich um einen angegebenen Offset, indem Sie die [**offsetcliprgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn) -Funktion aufrufen.
-   Schließen Sie einen rechteckigen Teil des Client Bereichs aus dem aktuellen Clippingbereich aus, indem Sie die [**excludecliprect**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect) -Funktion aufrufen.
-   Kombiniert einen rechteckigen Teil des Client Bereichs mit dem aktuellen Clippingbereich, indem die [**IntersectClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) -Funktion aufgerufen wird.

Nach dem Abrufen eines Handles, das den Clippingbereich identifiziert, kann eine Anwendung jeden Vorgang ausführen, der in den Regionen üblich ist, wie z. b.:

-   Kombinieren einer Kopie des aktuellen Clippingbereichs mit einem zweiten Bereich durch Aufrufen der [**combinergn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) -Funktion.
-   Vergleicht eine Kopie des aktuellen Clippingbereichs mit einem zweiten Bereich, indem die [**equalrgn**](/windows/desktop/api/Wingdi/nf-wingdi-equalrgn) -Funktion aufgerufen wird.
-   Bestimmt, ob ein Punkt innerhalb des Inneren einer Kopie des aktuellen Clippingbereichs liegt, indem die [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) -Funktion aufgerufen wird.

 

 



