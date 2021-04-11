---
title: Zeichnen eines Anzeige Kontexts
description: Zeichnen eines Anzeige Kontexts
ms.assetid: c3328375-faa3-4b29-a155-8a25cc62269f
keywords:
- Drawdib, Gerätekontext (DC)
- Drawdib, Zeichnen von DCS
- Drawdibrealize-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1c79c2b7bb938cc34527b23cfc66fda6d19503
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036930"
---
# <a name="drawing-a-display-context"></a>Zeichnen eines Anzeige Kontexts

Im folgenden Beispiel wird ein drawdib-DC mithilfe der [**drawdibrealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) -Funktion vorbereitet, bevor mehrere Bilder in einer bitmapsequenz angezeigt werden.


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

[Verwenden von drawdib](using-drawdib.md)
</dt> </dl>

 

 




