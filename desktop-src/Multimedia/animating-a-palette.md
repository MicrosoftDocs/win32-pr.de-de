---
title: Animieren einer Palette
description: Animieren einer Palette
ms.assetid: 89493cc3-eca9-407f-99c2-903fba16992c
keywords:
- DrawDib, Paletten
- DrawDibRealize-Funktion
- DrawDibDraw-Funktion
- DrawDibChangePalette-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be9613e4e648fad0b1fafe5d48d091ab13c9b6c358eda4a858c1d5517ab8fc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808420"
---
# <a name="animating-a-palette"></a>Animieren einer Palette

Im folgenden Beispiel wird eine Palette mithilfe der Funktionen [**DrawDibRealize,**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)und [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) animiert.

Sie können die Farben einer Bitmap ändern, indem Sie die [**DrawDibBegin-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) in Kombination mit [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)verwenden. Um Palettenänderungen zuzulassen, geben Sie zunächst das DDF \_ ANIMATE-Flag im Aufruf von **DrawDibBegin** an. Legen Sie als Zweites die Farbtabellenwerte aus den Paletteneinträgen fest, indem **Sie DrawDibChangePalette** verwenden.

Wenn *lppe* beispielsweise eine Adresse des [PALETTEENTRY-Arrays](/previous-versions//ms532623(v=vs.85)) ist, das die neuen Farben enthält, und *lpbi* die [**BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) ist, die in [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) oder [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw)verwendet wird, aktualisiert das folgende Fragment die DIB-Farbtabelle.


```C++
hdc = GetDC(hwnd); 
DrawDibBegin(hdd, ....., DDF_ANIMATE); 
DrawDibRealize(hdd, hdc, fBackground); 
DrawDibDraw(hdd, hdc, ...., DDF_SAME_DRAW|DDF_SAME_HDC); 
 
// Call to change color. 
DrawDibChangePalette(hDD, iStart, iLen, lppe); 
. 
. 
. 
ReleaseDC(hwnd, hdc); 

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DrawDib](using-drawdib.md)
</dt> </dl>

 

 