---
title: Schaltflächen (Windows Media Player SDK)
description: Schaltflächen
ms.assetid: 1212e2d9-e8f8-45d8-8c7f-20865c9c9c94
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Übersicht
- Skins, Schaltflächen Übersicht
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f06eb2fe21ee18a24f92e92d4fa760e9c76887
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102758"
---
# <a name="buttons-windows-media-player-sdk"></a><span data-ttu-id="5453d-107">Schaltflächen (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="5453d-107">Buttons (Windows Media Player SDK)</span></span>

<span data-ttu-id="5453d-108">Sie möchten eine oder mehrere Schaltflächen in der Skin verwenden, und jede Schaltfläche muss in der Skin-Definitionsdatei definiert werden.</span><span class="sxs-lookup"><span data-stu-id="5453d-108">You will want to use one or more buttons in your skin, and each button must be defined in the skin definition file.</span></span> <span data-ttu-id="5453d-109">Wenn Sie in diesem Abschnitt keine Schaltfläche definieren, kann Sie von der Skin nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5453d-109">If you do not define a button in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="5453d-110">Der Schaltflächen Abschnitt der Skin-Definitionsdatei beginnt mit der folgenden Zeile:</span><span class="sxs-lookup"><span data-stu-id="5453d-110">The buttons section of the skin definition file begins with this line:</span></span>


```C++
[ Buttons ]

```



<span data-ttu-id="5453d-111">Anschließend müssen Sie eine oder mehrere Zeilen hinzufügen, die Informationen zu den einzelnen Schaltflächen in der Skin enthalten.</span><span class="sxs-lookup"><span data-stu-id="5453d-111">You then must add one or more lines that contain information about each of the buttons in your skin.</span></span> <span data-ttu-id="5453d-112">Eine typische Zeile könnte wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="5453d-112">A typical line might be:</span></span>


```C++
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98

```



<span data-ttu-id="5453d-113">Beachten Sie, dass dieser Code als eine Zeile typisiert werden muss, die mit "PLAYPAUSE" beginnt und mit "Pushvorgang @ 160, 98" endet.</span><span class="sxs-lookup"><span data-stu-id="5453d-113">Note that this code should be typed as one line starting with "PlayPause" and ending with "Pushed @ 160,98".</span></span>

<span data-ttu-id="5453d-114">Sie können die folgende Vorlage für den Schaltflächen Abschnitt Ihrer Skin-Definitionsdatei verwenden:</span><span class="sxs-lookup"><span data-stu-id="5453d-114">You can use the following template for the Button section of your skin definition file:</span></span>


```C++
//  <Function> <Type>     <Location>     <Push Image Src> <Dis Image Src>    <Hit R,G,B> <Norm 2 Image Src> <Push 2 Image Src>
//  ---------- ------     ----------     ---------------- ---------------    ----------- ------------------ ------------------

```



<span data-ttu-id="5453d-115">Beachten Sie, dass diese als einzelne Zeilen eingegeben werden müssen, wobei der erste mit "// <Function> " beginnt und mit " &lt; Push 2 Image src &gt; " endet.</span><span class="sxs-lookup"><span data-stu-id="5453d-115">Again, note that these should be typed as single lines, the first starting with "// <Function>" and ending with "&lt;Push 2 Image Src&gt;".</span></span> <span data-ttu-id="5453d-116">Die zweite Zeile beginnt mit "//----------" und endet mit "------------------.".</span><span class="sxs-lookup"><span data-stu-id="5453d-116">The second line starts with "// ----------" and ends with "------------------."</span></span>

<span data-ttu-id="5453d-117">Die Schaltflächen Informationen für jede Zeile im Schaltflächen Abschnitt müssen in der folgenden Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5453d-117">Button information for each line in the Button section must appear in the following order.</span></span> <span data-ttu-id="5453d-118">Nur die ersten sechs Teile der Zeile sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5453d-118">Only the first six parts of the line are required.</span></span> <span data-ttu-id="5453d-119">Sekundäre Images sind nur enthalten, wenn Sie benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="5453d-119">Secondary images are not included unless they are needed.</span></span>

1.  [<span data-ttu-id="5453d-120">Button-Funktion</span><span class="sxs-lookup"><span data-stu-id="5453d-120">Button Function</span></span>](button-function.md)
2.  [<span data-ttu-id="5453d-121">Schalt Flächentyp</span><span class="sxs-lookup"><span data-stu-id="5453d-121">Button Type</span></span>](button-type.md)
3.  [<span data-ttu-id="5453d-122">Schaltflächen Position</span><span class="sxs-lookup"><span data-stu-id="5453d-122">Button Location</span></span>](button-location.md)
4.  [<span data-ttu-id="5453d-123">Bildquelle mit pushübertragung</span><span class="sxs-lookup"><span data-stu-id="5453d-123">Pushed Image Source</span></span>](pushed-image-source.md)
5.  [<span data-ttu-id="5453d-124">Bildquelle für deaktivierte Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="5453d-124">Image Source for Disabled Button</span></span>](image-source-for-disabled-button.md)
6.  [<span data-ttu-id="5453d-125">RGB-Farbe</span><span class="sxs-lookup"><span data-stu-id="5453d-125">Hit RGB Color</span></span>](hit-rgb-color.md)
7.  [<span data-ttu-id="5453d-126">Normale sekundäre Image Quelle</span><span class="sxs-lookup"><span data-stu-id="5453d-126">Normal Secondary Image Source</span></span>](normal-secondary-image-source.md)
8.  [<span data-ttu-id="5453d-127">Normale tertiäre Image Quelle</span><span class="sxs-lookup"><span data-stu-id="5453d-127">Normal Tertiary Image Source</span></span>](normal-tertiary-image-source.md)
9.  [<span data-ttu-id="5453d-128">Quelle für das sekundäre Image</span><span class="sxs-lookup"><span data-stu-id="5453d-128">Pushed Secondary Image Source</span></span>](pushed-secondary-image-source.md)
10. [<span data-ttu-id="5453d-129">Quelle für tertiäres Image übermittelt</span><span class="sxs-lookup"><span data-stu-id="5453d-129">Pushed Tertiary Image Source</span></span>](pushed-tertiary-image-source.md)

<span data-ttu-id="5453d-130">Ein Beispiel für einen Schaltflächen Code finden Sie im [Abschnitt Sample Button](sample-button-section.md).</span><span class="sxs-lookup"><span data-stu-id="5453d-130">For an example of button code, see [Sample Button Section](sample-button-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5453d-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5453d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5453d-132">**Skin-Referenz**</span><span class="sxs-lookup"><span data-stu-id="5453d-132">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




