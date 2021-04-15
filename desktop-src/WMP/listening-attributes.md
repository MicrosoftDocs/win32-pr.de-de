---
title: Lauschen von Attributen
description: Lauschen von Attributen
ms.assetid: 51b10507-5c2e-49ca-b560-6db6a1a7ee87
keywords:
- Windows Media Player Skins, lauschen von Attributen
- Skins, lauschen von Attributen
- Referenz für Skins, lauschen von Attributen
- lauschen von Attributen
- Attribute, lauschen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349a549966f7fba5ea152f8f0bb002a92f6dfb8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515675"
---
# <a name="listening-attributes"></a><span data-ttu-id="64c2e-108">Lauschen von Attributen</span><span class="sxs-lookup"><span data-stu-id="64c2e-108">Listening Attributes</span></span>

<span data-ttu-id="64c2e-109">Ein lauschen-Attribut wird verwendet, um ein Attribut mit einem anderen zu verbinden, sodass sich der Wert jedes Mal ändert, wenn sich der Wert des anderen Attributs ändert.</span><span class="sxs-lookup"><span data-stu-id="64c2e-109">A listening attribute is used to connect one attribute to another so that its value changes every time the value of the other attribute changes.</span></span>

<span data-ttu-id="64c2e-110">Das Abhör Attribut **wmpprop:** ist das nützlichste.</span><span class="sxs-lookup"><span data-stu-id="64c2e-110">The listening attribute **wmpprop:** is the most useful.</span></span> <span data-ttu-id="64c2e-111">Wenn der Wert eines Attributs als **wmpprop:** eines zweiten Attributs angegeben ist, wird der erste Wert automatisch aktualisiert, um den zweiten Wert jedes Mal widerzuspiegeln, wenn sich der zweite Wert ändert.</span><span class="sxs-lookup"><span data-stu-id="64c2e-111">If the value of one attribute is specified to be the **wmpprop:** of a second attribute, the first value will be automatically updated to reflect the second value each time the second value changes.</span></span>

<span data-ttu-id="64c2e-112">**Beispiel:**</span><span class="sxs-lookup"><span data-stu-id="64c2e-112">**Example:**</span></span>


```C++
<TEXT
  value="wmpprop:mySlider.value"
/>

```



<span data-ttu-id="64c2e-113">Auf diese Weise kann der Wert von myslider, der durch die Position des Schieberegler-Steuer Elements angezeigt wird, auch als Zahl in einem Textfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="64c2e-113">In this way, the value of mySlider, shown by the position of the slider control, can also be shown as a number within a text box.</span></span>

<span data-ttu-id="64c2e-114">Die beiden anderen Überwachungs Attribute **wmpaktivierte:** und **wmpdeaktivierte** Attribute können verwendet werden, um das **aktivierte** Attribut eines Steuer Elements zu ändern, je nachdem, ob seine Funktionalität aktuell im Player verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="64c2e-114">The two other listening attributes, **wmpenabled:** and **wmpdisabled:**, can be used to change the **enabled** attribute of a control depending on whether its functionality is currently available in the player.</span></span> <span data-ttu-id="64c2e-115">Diese Attribute können nur auf Methoden des Steuer Elements "Steuer **Elemente** " lauschen.</span><span class="sxs-lookup"><span data-stu-id="64c2e-115">These attributes can listen only to methods of the **Controls** object.</span></span>

<span data-ttu-id="64c2e-116">**Beispiel:**</span><span class="sxs-lookup"><span data-stu-id="64c2e-116">**Example:**</span></span>


```C++
<BUTTON 
  id="play" 
  enabled="wmpenabled:player.controls.play"
/>

```



## <a name="related-topics"></a><span data-ttu-id="64c2e-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64c2e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64c2e-118">**Verschiedenes**</span><span class="sxs-lookup"><span data-stu-id="64c2e-118">**Miscellaneous**</span></span>](miscellaneous.md)
</dt> </dl>

 

 




