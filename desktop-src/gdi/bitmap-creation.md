---
description: Verwenden Sie zum Erstellen einer Bitmap die Funktionen CreateBitmap, CreateBitmapIndirect oder CreateCompatibleBitmap, CreateDIBitmap und CreateDiscardableBitmap.
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: Bitmaperstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db37dd14f8be47ebf93c7ee7f586c54c2e55ea900402d9c255a3196987aaed43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038258"
---
# <a name="bitmap-creation"></a>Bitmaperstellung

Verwenden Sie zum Erstellen einer Bitmap die Funktionen [**CreateBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)oder [**CreateCompatibleBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)und [**CreateDiscardableBitmap.**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap)

Mit diesen Funktionen können Sie die Breite und Höhe der Bitmap in Pixel angeben. Mit der Funktion [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) und [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) können Sie auch die Anzahl der Farbebenen und die Anzahl der Bits angeben, die zum Identifizieren der Farbe erforderlich sind. Andererseits verwenden die Funktionen [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) und [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) einen angegebenen Gerätekontext, um die Anzahl der Farbebenen und die Anzahl der Bits abzurufen, die zum Identifizieren der Farbe erforderlich sind.

Die [**CreateDIBitmap-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) erstellt eine geräteabhängige Bitmap aus einer geräteunabhängigen Bitmap. Sie enthält eine Farbtabelle, die beschreibt, wie Pixelwerte RGB-Farbwerten entsprechen. Weitere Informationen finden Sie unter [Geräteabhängige Bitmaps](device-dependent-bitmaps.md) und [geräteunabhängige Bitmaps.](device-independent-bitmaps.md)

Nachdem die Bitmap erstellt wurde, können Sie ihre Größe, die Anzahl der Farbebenen oder die Anzahl der Bits, die zum Identifizieren der Farbe erforderlich sind, nicht ändern.

Wenn Sie keine Bitmap mehr benötigen, rufen Sie die [**DeleteObject-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) auf, um sie zu löschen.

 

 



