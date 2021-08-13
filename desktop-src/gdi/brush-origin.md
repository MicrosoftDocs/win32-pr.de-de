---
description: Wenn eine Anwendung eine Zeichnungsfunktion aufruft, um eine Form zu zeichnen, positioniert das System einen Pinsel am Anfang des Zeichnungsvorgang und ordnet ein Pixel in der Pinselbitmap dem Clientbereich am Fensteranfang zu, bei dem es sich um die linke obere Ecke des Fensters handelt.
ms.assetid: b951fd9a-1e87-4b17-9be8-263896c73922
title: Brush Origin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ccdc1dfa370ceb84216c89d562ef56dd206ce744b3be4fd38deb87175c1cf73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400390"
---
# <a name="brush-origin"></a>Brush Origin

Wenn eine Anwendung eine Zeichnungsfunktion aufruft, um eine Form zu zeichnen, positioniert das System einen Pinsel am Anfang des Zeichnungsvorgang und ordnet ein Pixel in der Pinselbitmap dem Clientbereich am Fensteranfang *zu,* bei dem es sich um die linke obere Ecke des Fensters handelt. Die Koordinaten des Pixels, das vom System als *Pinsel-Ursprung bezeichnet wird.* Der Standardpinsel-Ursprung befindet sich in der linken oberen Ecke der Pinselbitmap an den Koordinaten (0,0). Das System kopiert dann den Pinsel über den Clientbereich und bildet ein Muster, das so hoch ist wie die Bitmap. Der Kopiervorgang wird Zeilen für Zeile fortgesetzt, bis der gesamte Clientbereich gefüllt ist. Das Pinselmuster ist jedoch nur innerhalb der Grenzen der angegebenen Form sichtbar.

Es gibt Instanzen, in denen der Standardmäßige Pinsel-Ursprung nicht verwendet werden soll. Beispielsweise kann es erforderlich sein, dass eine Anwendung denselben Pinsel verwendet, um die Hintergründe der übergeordneten und untergeordneten Fenster zu zeichnen und den Hintergrund eines untergeordneten Fensters mit dem Hintergrund des übergeordneten Fensters zu mischen. Hierzu sollte die Anwendung den Pinselaussprung zurücksetzen, indem sie die [**SetBrushOrgEx-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) aufruft und den Ursprung um die erforderliche Anzahl von Pixeln verschiebt. (Eine Anwendung kann den aktuellen Pinsel-Ursprung abrufen, indem sie die [**GetBrushOrgEx-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) aufruft.)

Die folgende Abbildung zeigt einen mit fünf Zeigen gefüllten Stern mit einem anwendungsdefinierten Pinsel. Die Abbildung zeigt ein vergrößertes Bild des Pinsels sowie die Position, der er zu Beginn des Farbvorgang zugeordnet wurde.

![Abbildung, die zeigt, dass der Pinsel des Ursprungs des Fensters zugeordnet ist](images/csbru-01.png)

 

 



