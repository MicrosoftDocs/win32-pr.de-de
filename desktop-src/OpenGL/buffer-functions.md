---
title: Pufferfunktionen
description: Um den Inhalt eines Offscreen-Puffers in einen Bildschirm Puffer zu kopieren, nennen Sie die Anwendung "Austausch Puffer".
ms.assetid: 605eba4e-ee38-4e62-adf8-1b7894030cb0
keywords:
- WGL-Funktionen, Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a93858b8085171a9139bc5ab329e531ddbb699
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106351828"
---
# <a name="buffer-functions"></a>Pufferfunktionen

Um den Inhalt eines Offscreen-Puffers in einen Bildschirm Puffer zu kopieren, nennen Sie die [**Anwendung "Austausch Puffer**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)". Die Funktion " **Swap-Puffer** " übernimmt ein Handle für einen Gerätekontext. Das aktuelle Pixel Format für den angegebenen Gerätekontext muss einen Hintergrund Puffer enthalten. Standardmäßig ist der Hintergrund Puffer außerhalb des Bildschirms, und der vordere Puffer ist auf dem Bildschirm.

> [!Note]  
> Die **swapbuffers** -Funktion tauscht nicht wirklich den Inhalt der beiden Puffer aus, sondern kopiert den Inhalt eines Puffers in einen anderen. Der Inhalt des Offscreen-Puffers ist nach einem **callapbuffers-Austausch** nicht definiert. Folglich ist das Ergebnis von zwei aufeinander folgenden Aufrufen von " **Austausch Puffer** " nicht definiert.

 

In der folgenden Abbildung wird gezeigt, wie die Inhalte der Puffer beim Aufrufen von " **Austausch Puffern**" kopiert werden.

![Das Diagramm zeigt die nicht definierten Ergebnisse von aufeinander folgenden Aufrufen der Funktion "Swap" an.](images/opengl00.png)

Mehrere OpenGL Core-Funktionen verwalten auch Puffer. Die [**gldrawbuffer**](gldrawbuffer.md) -Funktion ist die für die doppelte Pufferung relevanteste. Sie gibt die Frame Puffer oder Puffer an, die OpenGL in zeichnet.

Die folgenden Funktionen wirken sich auch auf Puffer aus:

-   [**glread Buffer**](glreadbuffer.md)
-   [**glread Pixels**](glreadpixels.md)
-   [**glcopypixels**](glcopypixels.md)
-   [**glaccum**](glaccum.md)
-   [**glcolormask**](glcolormask.md)
-   [**gldepthmask**](gldepthmask.md)
-   [**glindexmask**](glindexmask.md)
-   [**glstencilmask**](glstencilmask.md)
-   [**glclearaccum**](glclearaccum.md)
-   [**glclearcolor**](glclearcolor.md)
-   [**glcleartiefe**](glcleardepth.md)
-   [**glclearindex**](glclearindex.md)
-   [**glclearstencil**](glclearstencil.md)

 

 




