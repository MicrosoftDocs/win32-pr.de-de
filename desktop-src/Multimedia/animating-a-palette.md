---
title: Animieren einer Palette
description: Animieren einer Palette
ms.assetid: 89493cc3-eca9-407f-99c2-903fba16992c
keywords:
- Drawdib, Paletten
- Drawdibrealize-Funktion
- Drawdibdraw-Funktion
- Drawdibchangepalette-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e023ba8ee2c4791ebc8c3f2ac7ebf9a198f4a5ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726728"
---
# <a name="animating-a-palette"></a>Animieren einer Palette

Im folgenden Beispiel wird eine Palette mithilfe der [**drawdibrealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize)-, [**drawdibchangepalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)-und [**drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) -Funktionen animiert.

Sie können die Farben einer Bitmap ändern, indem Sie die [**drawdibbegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) -Funktion in Kombination mit [**drawdibchangepalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)verwenden. Geben Sie zum Zulassen von Palettenänderungen zunächst das DDF- \_ animieren-Flag im **drawdibbegin**-aufrufsvorgang an. Legen Sie anschließend die Farb Tabellenwerte aus den paletteneinträgen mithilfe von **drawdibchangepalette** fest.

Wenn *lppe* z. b. eine Adresse des [PaletteEntry](/previous-versions//ms532623(v=vs.85)) -Arrays ist, das die neuen Farben enthält, und *lpbi* die [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur ist, die in [**drawdibbegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) oder [**drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw)verwendet wird, aktualisiert das folgende Fragment die DIB-Farbtabelle.


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

[Verwenden von drawdib](using-drawdib.md)
</dt> </dl>

 

 