---
description: Wenn eine Anwendung eine Zeichnungs Funktion aufruft, um eine Form zu zeichnen, positioniert das System einen Pinsel am Anfang des Zeichnungs Vorgangs und ordnet ein Pixel in der Pinsel Bitmap dem Client Bereich am Fenster Ursprung zu. Dies ist die linke obere Ecke des Fensters.
ms.assetid: b951fd9a-1e87-4b17-9be8-263896c73922
title: Pinsel Ursprung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 016237b97a52da6fd7fa14a3b6ba2dc25b03b96e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571193"
---
# <a name="brush-origin"></a>Pinsel Ursprung

Wenn eine Anwendung eine Zeichnungs Funktion aufruft, um eine Form zu zeichnen, positioniert das System einen Pinsel am Anfang des Zeichnungs Vorgangs und ordnet ein Pixel in der Pinsel Bitmap dem Client Bereich am *Fenster Ursprung* zu. Dies ist die linke obere Ecke des Fensters. Die Koordinaten des Pixels, das vom System zugeordnet wird, werden als *Pinsel Ursprung* bezeichnet. Der Standard Pinsel Ursprung befindet sich in der oberen linken Ecke der Pinsel Bitmap an den Koordinaten (0,0). Das System kopiert dann den Pinsel in den Client Bereich und bildet so ein Muster, das so groß wie die Bitmap ist. Der Kopiervorgang wird zeilenweise fortgesetzt, bis der gesamte Client Bereich ausgefüllt ist. Allerdings ist das Pinsel Muster nur innerhalb der Grenzen der angegebenen Form sichtbar.

Es gibt Instanzen, wenn der Standard Pinsel Ursprung nicht verwendet werden soll. Beispielsweise kann es erforderlich sein, dass eine Anwendung denselben Pinsel verwendet, um die Hintergründe der übergeordneten und untergeordneten Fenster zu zeichnen und den Hintergrund eines untergeordneten Fensters mit dem des übergeordneten Fensters zu mischen. Zu diesem Zweck sollte die Anwendung den Pinsel Ursprung zurücksetzen, indem Sie die Funktion [**setbrushorgex**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) aufruft und den Ursprung um die erforderliche Anzahl von Pixeln verschiebt. (Eine Anwendung kann den aktuellen Pinsel Ursprung durch Aufrufen der [**getbrushorgex**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) -Funktion abrufen.)

In der folgenden Abbildung ist ein fünf zeiiger Stern dargestellt, der mit einem von der Anwendung definierten Pinsel gefüllt wurde. Die Abbildung zeigt ein Zoom Bild des Pinsels sowie den Speicherort, an dem er am Anfang des Paint-Vorgangs zugeordnet wurde.

![Abbildung, die anzeigt, dass der Pinsel Ursprung dem Fenster Ursprung zugeordnet ist](images/csbru-01.png)

 

 



