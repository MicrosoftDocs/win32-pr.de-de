---
title: Erstellen benutzerdefinierter Schieberegler
description: Erstellen benutzerdefinierter Schieberegler
ms.assetid: eb26ba44-a891-4cb6-be74-5acf881e896f
keywords:
- Erstellen von Skins, Schieberegler
- Windows Media Player Skins, Schieberegler
- Skins, Schieberegler
- Schieberegler in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f205d46af003589fcc2c3b741a253ea08fae12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515914"
---
# <a name="creating-custom-sliders"></a><span data-ttu-id="5aa7a-107">Erstellen benutzerdefinierter Schieberegler</span><span class="sxs-lookup"><span data-stu-id="5aa7a-107">Creating Custom Sliders</span></span>

<span data-ttu-id="5aa7a-108">Sie können benutzerdefinierte Schieberegler in jeder beliebigen Form erstellen.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-108">You can create custom sliders in any shape you want.</span></span> <span data-ttu-id="5aa7a-109">In diesem Beispiel wird ein einfacher Strip ausgewählt, aber die tatsächliche Form kann etwas sein.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-109">For this example, a simple strip is chosen, but the actual shape can be anything.</span></span> <span data-ttu-id="5aa7a-110">Dies ist der Code für das **customslider** -Element:</span><span class="sxs-lookup"><span data-stu-id="5aa7a-110">Here is the code for the **CUSTOMSLIDER** element:</span></span>


```C++
<CustomSlider 
  top="160"
  left="130"
  min="0"
  max="100"
  toolTip="volume control"
  image="slider.bmp"
  positionImage="graymap.bmp"
  enabled="true"
  value="wmpprop:player.settings.volume"
  value_onchange="player.settings.volume = value" />

```



<span data-ttu-id="5aa7a-111">Dadurch wird ein Anfangswert für den Schieberegler festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-111">This sets up an initial value for the slider.</span></span> <span data-ttu-id="5aa7a-112">Es werden zwei neue Bitmaps eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-112">Two new bitmaps are introduced.</span></span> <span data-ttu-id="5aa7a-113">Eine ist die Graustufen Bitmap (slider.bmp), die definiert, welche Werte verwendet werden, wenn darauf geklickt wird, und die andere (slider.bmp), die bestimmt, welches Bild angezeigt wird, wenn auf einen bestimmten Teil der grau Skala geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-113">One is the grayscale bitmap (slider.bmp) that defines which values will be used when clicked on, and the other (slider.bmp) that determines which image will be shown when a particular portion of the grayscale is clicked on.</span></span>

<span data-ttu-id="5aa7a-114">Der Anfangswert wird durch lauschen auf dem Volume mit wmpprop festgelegt, und das Volume kann geändert werden, wenn der Benutzer auf einen Teil des Schiebereglers klickt, der eine Änderung des Werts auslöst.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-114">The initial value is determined by listening to the volume with wmpprop and then the volume can be changed when the user clicks on a portion of the slider that triggers a change in value.</span></span>

<span data-ttu-id="5aa7a-115">Sie können im Abschnitt "Sample" des SDK einen ähnlichen Schieberegler für den Schieberegler sehen.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-115">You can see a similar working slider skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5aa7a-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5aa7a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aa7a-117">**Leitfaden zum Erstellen von Skin**</span><span class="sxs-lookup"><span data-stu-id="5aa7a-117">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




