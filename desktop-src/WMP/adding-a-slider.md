---
title: Fügen eines Schiebereglers
description: Fügen eines Schiebereglers
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- Erstellen von Skins, Schieberegler
- Windows Media Player Skins, Schieberegler
- Skins, Schieberegler
- Schieberegler in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efcae55b3826b69a7c88fed5a23a262526c9dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037216"
---
# <a name="adding-a-slider"></a><span data-ttu-id="60815-107">Fügen eines Schiebereglers</span><span class="sxs-lookup"><span data-stu-id="60815-107">Adding a Slider</span></span>

<span data-ttu-id="60815-108">Sie können einen Schieberegler hinzufügen, um die aktuelle Position des Mediums anzuzeigen. Außerdem können Sie den Benutzer aktivieren, um die Position in der aktuellen Mediendatei zu ändern.</span><span class="sxs-lookup"><span data-stu-id="60815-108">You can add a slider to show the current position of the media, and also enable the user to change the position in the current media file.</span></span>

<span data-ttu-id="60815-109">Zuerst müssen Sie das **Slider** -Element hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="60815-109">First you must add the **SLIDER** element:</span></span>


```C++
<SLIDER
  id = "myslider"
  min = "0"
  max = "wmpprop:player.currentMedia.duration"
  onmouseup = "player.controls.currentPosition = myslider.value; "
  tooltip = "current position"
  height = "10"
  width = "180"
  top = "150"
  left = "88"
  backgroundColor = "red"
  foregroundColor = "blue"
  thumbImage = "thumb.bmp"/>

```



<span data-ttu-id="60815-110">Dadurch wird ein Maximalwert basierend auf der Dauer der aktuellen Mediendatei festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60815-110">This sets a maximum value based on the duration of the current media file.</span></span> <span data-ttu-id="60815-111">Hierbei wird ein kleines Ziehpunkt für das Ziehpunkt-Bild verwendet</span><span class="sxs-lookup"><span data-stu-id="60815-111">This uses a tiny thumb image bitmap that is just a 10 pixel by 10 pixel green square.</span></span> <span data-ttu-id="60815-112">Der Hintergrund des Schiebereglers wird rot angezeigt, und der Vordergrund wird blau dargestellt.</span><span class="sxs-lookup"><span data-stu-id="60815-112">The background of the slider will be red and the foreground will be blue.</span></span> <span data-ttu-id="60815-113">Wenn der Benutzer das Ziehpunkt Bild an eine neue Position zieht und die Maustaste loslässt, werden die Medien an diese Position geändert.</span><span class="sxs-lookup"><span data-stu-id="60815-113">When the user drags the thumb image to a new position and lets go of the mouse button, the media will change to that position.</span></span>

<span data-ttu-id="60815-114">Der Schieberegler wird jedoch nicht von sich selbst verschoben, es sei denn, Sie messen die aktuelle Position mit dem **CurrentPosition \_ OnChange** -Attribut des **Controls** -Elements, das in das **Player** -Element eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="60815-114">But the slider will not move by itself unless you measure the current position with the **currentPosition\_onchange** attribute of the **CONTROLS** element, which is embedded in the **PLAYER** element.</span></span>


```C++
<PLAYER
    URL = "https://proseware.com/laure.wma">

    <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition; "/>

</PLAYER>

```



<span data-ttu-id="60815-115">Wenn sich die Position des Mediums ändert, wird ein Ereignis ausgelöst, das dann die Codezeile ausführt, die den Wert des Schiebereglers an die aktuelle Position des Mediums ändert.</span><span class="sxs-lookup"><span data-stu-id="60815-115">When the position of the media changes, this fires an event which then runs the line of code that changes the value of the slider to the current position of the media.</span></span>

<span data-ttu-id="60815-116">Sie können im Abschnitt "Sample" des SDK einen ähnlichen Schieberegler für den Schieberegler sehen.</span><span class="sxs-lookup"><span data-stu-id="60815-116">You can see a similar working slider skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60815-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60815-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60815-118">**Leitfaden zum Erstellen von Skin**</span><span class="sxs-lookup"><span data-stu-id="60815-118">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




