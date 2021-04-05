---
title: Hinzufügen von Visualisierungen
description: Hinzufügen von Visualisierungen
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- Erstellen von Skins, Visualisierungen
- Windows Media Player Skins, Visualisierungen
- Skins, Visualisierungen
- Visualisierungen, Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9750b114d99af8c59777ea28ff4dab85a56dd229
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710787"
---
# <a name="adding-visualizations"></a><span data-ttu-id="be79a-107">Hinzufügen von Visualisierungen</span><span class="sxs-lookup"><span data-stu-id="be79a-107">Adding Visualizations</span></span>

<span data-ttu-id="be79a-108">Sie können ein Visualisierungs Fenster auf die gleiche Weise hinzufügen, wie Sie ein Videofenster hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="be79a-108">You can add a visualization window the same way you added a video window.</span></span> <span data-ttu-id="be79a-109">Dieselbe Skin kann verwendet werden, es wird jedoch ein **Effects** -Element verwendet.</span><span class="sxs-lookup"><span data-stu-id="be79a-109">The same skin can be used, but an **EFFECTS** element is used.</span></span>

<span data-ttu-id="be79a-110">Zuerst müssen Sie das **Effects** -Element hinzufügen und ihm eine ID und eine Größe geben:</span><span class="sxs-lookup"><span data-stu-id="be79a-110">First you must add the **EFFECTS** element and give it an ID and size:</span></span>


```C++
       <EFFECTS
            id = "myeffects"
            top = "25"
            left = "88"
            width = "180"
            height = "150"/>

```



<span data-ttu-id="be79a-111">Anschließend können Sie die beiden Schaltflächen als vorherige und nächste Visualisierungs Code Zeichenfolge zuweisen:</span><span class="sxs-lookup"><span data-stu-id="be79a-111">Then you can assign the two buttons a previous and next visualization code string:</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Next"
            onClick = "JScript:myeffects.next(); " />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Previous"
            onClick = "JScript:myeffects.previous(); " />

```



<span data-ttu-id="be79a-112">Die Ebenen und Bitmaps waren dieselben, die im Video Beispiel verwendet wurden, mit dem Unterschied, dass der Wiedergabe Pfeil horizontal kopiert und gekippt wurde.</span><span class="sxs-lookup"><span data-stu-id="be79a-112">The layers and bitmaps were the same ones used in the video example, except that the play arrow was copied and flipped horizontally.</span></span>

<span data-ttu-id="be79a-113">Schließlich wurde ein einfaches **Player** -Element mit dem **URL** -Attribut hinzugefügt, um einen zu Wiedergabe enden Song auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="be79a-113">Finally, a simple **PLAYER** element with the **URL** attribute was added to choose a song to play.</span></span>


```C++
      <PLAYER
          URL = "https://proseware.com/mellow.wma">
      </PLAYER>

```



<span data-ttu-id="be79a-114">Im Beispiel Abschnitt des SDK sehen Sie eine ähnliche Funktionsweise für die Visualisierung.</span><span class="sxs-lookup"><span data-stu-id="be79a-114">You can see a similar working visualization skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be79a-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="be79a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be79a-116">**Leitfaden zum Erstellen von Skin**</span><span class="sxs-lookup"><span data-stu-id="be79a-116">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




