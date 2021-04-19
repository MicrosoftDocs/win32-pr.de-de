---
title: Album Kunst
description: Album Kunst
ms.assetid: a5996232-e1ee-41ae-a6ca-f841321644fe
keywords:
- Windows Media Player Mobile Skins, Albumkunst
- Skins, Albumkunst
- Referenz für Skins, Albumkunst
- kunstdateien für Skins, Albumkunst
- Albumkunst in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0974f8683da98469e75a4472d086dcb1a244c75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342045"
---
# <a name="album-art"></a><span data-ttu-id="8bd60-108">Album Kunst</span><span class="sxs-lookup"><span data-stu-id="8bd60-108">Album Art</span></span>

<span data-ttu-id="8bd60-109">Wenn Sie ein Skin für Windows Media Player 10 Mobile oder höher erstellen, empfiehlt es sich, albumgrafiken anzuzeigen, die sich auf das aktuell wiedergegebene Medien Element beziehen.</span><span class="sxs-lookup"><span data-stu-id="8bd60-109">When you create a skin for Windows Media Player 10 Mobile or later, you may want to display album art that relates to the currently playing media item.</span></span> <span data-ttu-id="8bd60-110">Wenn Sie Ihre Skin entwerfen, sollten Sie Platz im Hintergrundbild reservieren, um die Albumkunst zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="8bd60-110">When you design your skin, you will want to reserve space in the Background image to contain the album art.</span></span>

<span data-ttu-id="8bd60-111">Der Abschnitt "Album-Art" der Skin-Definitionsdatei muss mit der folgenden Zeile beginnen:</span><span class="sxs-lookup"><span data-stu-id="8bd60-111">The Album Art section of the skin definition file must begin with the following line:</span></span>


```C++
[ Album Art ]

```



<span data-ttu-id="8bd60-112">Anschließend müssen Sie Informationen hinzufügen, die den Speicherort und die Größe der albumgrafiken in der Skin angeben.</span><span class="sxs-lookup"><span data-stu-id="8bd60-112">You then must add information that specifies the location and size of the album art in your skin.</span></span> <span data-ttu-id="8bd60-113">Sie müssen vier positive ganze Zahlen eingeben, getrennt durch Kommas, die die linke, obere, Breite und Höhe der Art des Albums in Pixel relativ zum Hintergrundbild definieren.</span><span class="sxs-lookup"><span data-stu-id="8bd60-113">You must enter four positive integers, separated by commas that define the left, top, width, and height of the album art, in pixels, relative to the background image.</span></span> <span data-ttu-id="8bd60-114">Im folgenden Beispiel wird gezeigt, wie Dimensionen angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="8bd60-114">The following example shows how to specify dimensions:</span></span>


```C++
//  <Location>
//  ----------
   5,37,230,155

```



<span data-ttu-id="8bd60-115">Wenn Sie planen, einen Video Abschnitt in der Skin einzuschließen, können Sie die gleiche Größe und den gleichen Speicherort für Ihre Albumkunst verwenden, um Platz zu sparen.</span><span class="sxs-lookup"><span data-stu-id="8bd60-115">If you plan on including a video section in your skin, you can use the same size and location for your album art to conserve space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8bd60-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8bd60-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bd60-117">**Skin-Referenz**</span><span class="sxs-lookup"><span data-stu-id="8bd60-117">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




