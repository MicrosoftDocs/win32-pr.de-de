---
description: Um eine Bitmap zu erstellen, verwenden Sie die Funktionen "up", "kreatebitmap", "up" oder "kreatecompatiblebitmap", "kreatedibitmap" und "kreateverwerdablebitmap".
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: Bitmap-Erstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00a0bc5a39d1b5e6053a34a87c28d6792a42b0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215219"
---
# <a name="bitmap-creation"></a>Bitmap-Erstellung

Um eine Bitmap zu erstellen, verwenden [**Sie die Funktionen**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)"up", "kreatebitmap", "up" oder [](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)" [**kreatecompatiblebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) ", " [**kreatedibitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)" und " [**kreateverwerdablebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap)".

Mit diesen Funktionen können Sie die Breite und Höhe der Bitmap in Pixel angeben. Mit der Funktion "up- [**Bitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) " und der Funktion " [**kreatebitmapindirekte**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) " können Sie auch die Anzahl von Farbebenen und die Anzahl der Bits angeben, die zum Identifizieren der Farbe erforderlich sind. Andererseits verwenden die Funktionen " [**kreatecompatiblebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) " und " [**deateverwerdablebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) " einen angegebenen Gerätekontext, um die Anzahl von Farbebenen und die Anzahl der Bits, die zum Identifizieren der Farbe erforderlich sind, abzurufen.

Die Funktion " [**kreatedibitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) " erstellt eine Geräte abhängige Bitmap aus einer geräteunabhängigen Bitmap. Sie enthält eine Farbtabelle, in der beschrieben wird, wie Pixelwerte RGB-Farbwerten entsprechen. Weitere Informationen finden Sie unter [Geräte abhängige Bitmaps](device-dependent-bitmaps.md) und [geräteunabhängige Bitmaps](device-independent-bitmaps.md).

Nachdem die Bitmap erstellt wurde, können Sie die Größe, die Anzahl von Farbebenen oder die Anzahl der Bits, die zum Identifizieren der Farbe erforderlich sind, nicht ändern.

Wenn Sie keine Bitmap mehr benötigen, können Sie die [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) -Funktion aufrufen, um Sie zu löschen.

 

 



