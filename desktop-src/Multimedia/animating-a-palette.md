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
# <a name="animating-a-palette"></a><span data-ttu-id="1ebdb-107">Animieren einer Palette</span><span class="sxs-lookup"><span data-stu-id="1ebdb-107">Animating a Palette</span></span>

<span data-ttu-id="1ebdb-108">Im folgenden Beispiel wird eine Palette mithilfe der [**drawdibrealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize)-, [**drawdibchangepalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)-und [**drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) -Funktionen animiert.</span><span class="sxs-lookup"><span data-stu-id="1ebdb-108">The following example animates a palette by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize), [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette), and [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) functions.</span></span>

<span data-ttu-id="1ebdb-109">Sie können die Farben einer Bitmap ändern, indem Sie die [**drawdibbegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) -Funktion in Kombination mit [**drawdibchangepalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)verwenden.</span><span class="sxs-lookup"><span data-stu-id="1ebdb-109">You can change the colors of a bitmap by using the [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) function in combination with [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette).</span></span> <span data-ttu-id="1ebdb-110">Geben Sie zum Zulassen von Palettenänderungen zunächst das DDF- \_ animieren-Flag im **drawdibbegin**-aufrufsvorgang an.</span><span class="sxs-lookup"><span data-stu-id="1ebdb-110">First, to allow palette changes, specify the DDF\_ANIMATE flag in the call to **DrawDibBegin**.</span></span> <span data-ttu-id="1ebdb-111">Legen Sie anschließend die Farb Tabellenwerte aus den paletteneinträgen mithilfe von **drawdibchangepalette** fest.</span><span class="sxs-lookup"><span data-stu-id="1ebdb-111">Second, set the color table values from the palette entries by using **DrawDibChangePalette**.</span></span>

<span data-ttu-id="1ebdb-112">Wenn *lppe* z. b. eine Adresse des [PaletteEntry](/previous-versions//ms532623(v=vs.85)) -Arrays ist, das die neuen Farben enthält, und *lpbi* die [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur ist, die in [**drawdibbegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) oder [**drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw)verwendet wird, aktualisiert das folgende Fragment die DIB-Farbtabelle.</span><span class="sxs-lookup"><span data-stu-id="1ebdb-112">For example, if *lppe* is an address of the [PALETTEENTRY](/previous-versions//ms532623(v=vs.85)) array containing the new colors, and *lpbi* is the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure used in [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) or [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw), the following fragment updates the DIB color table.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1ebdb-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ebdb-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ebdb-114">Verwenden von drawdib</span><span class="sxs-lookup"><span data-stu-id="1ebdb-114">Using DrawDib</span></span>](using-drawdib.md)
</dt> </dl>

 

 