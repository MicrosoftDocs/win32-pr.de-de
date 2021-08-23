---
title: Bereitstellen von Steuerelementen zum Zuschneiden und Strecken von Bildern
description: Bereitstellen von Steuerelementen zum Zuschneiden und Strecken von Bildern
ms.assetid: cc62d70d-3f5f-477c-bc09-ab8ab0a9dce3
keywords:
- MCIWndGetSource-Makro
- MCIWndPutSource-Makro
- MCIWndGetDest-Makro
- MCIWndPutDest-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712dddf0d022b63bccb3c64157df796585569b72604dc82746417d725c4135dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805750"
---
# <a name="providing-controls-for-cropping-and-stretching-images"></a>Bereitstellen von Steuerelementen zum Zuschneiden und Strecken von Bildern

Mit MCIWnd können Sie Bilder eines Videoclips zuschneiden und strecken. Um diese Features zu verstehen, müssen Sie die Beziehungen zwischen Framegröße, Quellrechteck, Zielrechteck *und* *Wiedergabebereich verstehen.*

Ein Videoclip besteht aus mehreren Frames, die jeweils ein Bild enthalten. Die Framegröße eines Videoclips ist die Größe des Bilds im aktuellen Frame. In der Regel hat ein Videoclip eine Framegröße, da alle Bilder im Clip die gleiche Größe haben.

Das Quellrechteck ist ein rechteckiger Bereich, der die Frames eines Videoclips überlagert. Das Quellrechteck definiert den Teil jedes Frames, der während der Wiedergabe angezeigt wird. Wenn ein Videoclip mit MCIWnd geladen wird, wird das Quellrechteck mit den gleichen Dimensionen und der gleichen Position wie der ursprüngliche Frame des Videoclips initialisiert.

Das Zielrechteck ist ein rechteckiger Bereich, der ein virtuelles Wiedergabefenster definiert. Das Zielrechteck empfängt die Bilddaten aus dem Quellrechteck für jeden Frame des Videoclips. Wenn die Quell- und Zielrechteckdimensionen unterschiedlich sind, passt MCIWnd die Bilddaten nach Bedarf horizontal und vertikal an, um das Zielrechteck zu füllen. Wenn ein Videoclip mit MCIWnd geladen wird, wird das Zielrechteck mit den gleichen Dimensionen und der gleichen Position wie der ursprüngliche Frame des Videoclips initialisiert.

Der Wiedergabebereich ist der Teil eines MCIWnd-Fensters, das von einer Anwendung zum Anzeigen des Videoclips verwendet wird. Der Wiedergabebereich ist der Clientbereich eines MCIWnd-Fensters oder der Teil des Clientbereichs, der die MCIWnd-Symbolleiste ausschließt. Wenn ein Videoclip mit MCIWnd geladen wird, wird der Wiedergabebereich mit den gleichen Dimensionen und der gleichen Position wie der ursprüngliche Frame des Videoclips initialisiert.

Sie können einen Videoclip mithilfe der [**Makros MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) und [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) zuschneiden, um das Quellrechteck zu ändern. Das Zuschneiden eines Bilds bestimmt nur, welcher Teil der Frames während der Wiedergabe angezeigt wird. Sie ändert nicht den Inhalt der Datei, die abgespielt wird. Bevor Sie ein Bild zuschneiden, können Sie die aktuelle Größe des Quellrechtecks mithilfe von **MCIWndGetSource abrufen.** Nachdem die neue Größe und Position des Quellrechtecks berechnet wurden, können Sie die Zuschneidegrenzen des Quellrechtecks mithilfe von **MCIWndPutSource festlegen.**

Sie können einen Videoclip mithilfe der Makros [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) und [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) strecken, um das Zielrechteck zu ändern. Wenn Sie einen Videoclip strecken, wird die Framegröße eines Videoclips vertikal, horizontal oder in beide Richtungen verlängert oder verkürzt. Bevor Sie ein Bild strecken, können Sie die aktuelle Größe und Position des Zielrechtecks mithilfe von **MCIWndGetDest abrufen.** Mit **dem MCIWndPutDest-Makro** können Sie das Zielrechteck neu definieren. Stretching kann das Bild während der Wiedergabe verzerren, ändert jedoch nicht den Inhalt der Datei, die abgespielt wird.

Wenn die Größe des Zielrechtecks größer als der Wiedergabebereich wird, können Sie angeben, welcher Teil des Wiedergabebereichs den Videoclip mithilfe von **MCIWndPutDest anzeigen soll.**

> [!Note]  
> Das [**MCIWndPutDest-Makro**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) ändert die Größe des Wiedergabebereichs nicht. Um das MCIWnd-Fenster zusammen mit dem Zielrechteck zu strecken, müssen Sie die aktuelle Größe des MCIWnd-Fensters kennen und neue Fensterdimensionen basierend auf dem Zielrechteck ausgibt. Sie können die MCIWnd-Fensterdimensionen mithilfe der [GetWindowRect-Funktion](/windows/win32/api/winuser/nf-winuser-getwindowrect) abrufen und die Größe des MCIWnd-Fensters mithilfe der [SetWindowPos-Funktion](/windows/win32/api/winuser/nf-winuser-setwindowpos) ändern.

 

 

 