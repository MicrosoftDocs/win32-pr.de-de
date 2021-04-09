---
title: Abschnitt "Bitmaps"
description: Abschnitt "Bitmaps"
ms.assetid: db2801e5-c55a-4681-9fe9-6027f28653e0
keywords:
- Windows Media Player Mobile Skins, Bitmaps
- Skins, Bitmaps
- Erstellen von Skins, Bitmaps (Abschnitt)
- Schreiben von Code für Skins, Bitmaps (Abschnitt)
- Bitmaps in Skins, Bitmaps (Abschnitt)
- Skin-Definitions Dateien, Abschnitt "Bitmaps"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4a5e41e8e2b095b199a072e31abde3c1cbaa29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036879"
---
# <a name="bitmaps-section"></a><span data-ttu-id="3bbb0-109">Abschnitt "Bitmaps"</span><span class="sxs-lookup"><span data-stu-id="3bbb0-109">Bitmaps Section</span></span>

<span data-ttu-id="3bbb0-110">Als nächstes müssen Sie über einen Abschnitt verfügen, der die einzelnen Bitmapdateien definiert.</span><span class="sxs-lookup"><span data-stu-id="3bbb0-110">Next, you must have a section that defines each of your bitmap files.</span></span> <span data-ttu-id="3bbb0-111">Jedem Bitmaptyp, den Sie verwenden, muss eine Datei zugewiesen sein, aber Sie können über mehrere Typen mit derselben Bitmap verfügen.</span><span class="sxs-lookup"><span data-stu-id="3bbb0-111">Each type of bitmap you will use must have a file assigned to it, though you can have more than one type using the same bitmap.</span></span>


```C++
[ Bitmaps ]

//  <Name>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



<span data-ttu-id="3bbb0-112">Der Abschnitt Bitmaps muss mit dem Wort Bitmaps in eckigen Klammern und dann einer Zeile für jeden Bitmaptyp beginnen, den Sie definieren möchten.</span><span class="sxs-lookup"><span data-stu-id="3bbb0-112">The Bitmaps section must begin with the word Bitmaps in brackets and then a line for each bitmap type you want to define.</span></span> <span data-ttu-id="3bbb0-113">In diesem Beispiel wurden fünf Typen von Bitmaps definiert.</span><span class="sxs-lookup"><span data-stu-id="3bbb0-113">In this example, five types of bitmaps were defined.</span></span> <span data-ttu-id="3bbb0-114">Weitere Informationen zum Abschnitt Bitmaps finden Sie unter [Bitmaps](bitmaps.md) in der Skin-Referenz.</span><span class="sxs-lookup"><span data-stu-id="3bbb0-114">For more about the Bitmaps section, see [Bitmaps](bitmaps.md) in the Skin Reference.</span></span>

> [!Note]  
> <span data-ttu-id="3bbb0-115">Die Region und die Super Bitmaps sind in Windows Media Player 10 Mobile oder höher als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="3bbb0-115">The Region and Super bitmaps are deprecated in Windows Media Player 10 Mobile or later skins.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3bbb0-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3bbb0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bbb0-117">**Schreiben des Codes**</span><span class="sxs-lookup"><span data-stu-id="3bbb0-117">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




