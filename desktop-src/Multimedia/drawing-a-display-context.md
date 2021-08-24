---
title: Zeichnen eines Anzeigekontexts
description: Zeichnen eines Anzeigekontexts
ms.assetid: c3328375-faa3-4b29-a155-8a25cc62269f
keywords:
- DrawDib, Gerätekontext (DC)
- DrawDib, Zeichnen von DCs
- DrawDibRealize-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0f10d533fff97064ba3c6a081a2f1d0aaa9e1b72011f2baa1ac3a6bd1a81d43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678720"
---
# <a name="drawing-a-display-context"></a>Zeichnen eines Anzeigekontexts

Im folgenden Beispiel wird ein DrawDib-DC mithilfe der [**DrawDibRealize-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) vorbereitet, bevor mehrere Bilder in einer Bitmapsequenz angezeigt werden.


```C++
hdc = GetDC(hwnd); 
DrawDibBegin(hdd, hdc, dxDest, dyDest, lpbi, dxSrc, dySrc, NULL); 
DrawDibRealize(hdd, hdc, fBackground); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
ReleaseDC(hwnd, hdc); 

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DrawDib](using-drawdib.md)
</dt> </dl>

 

 




