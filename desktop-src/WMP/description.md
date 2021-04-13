---
title: Beschreibung (Windows Media Player SDK)
description: BESCHREIBUNG
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Windows Media Player Mobile Skins, Beschreibungs Abschnitt
- Skins, Beschreibungs Abschnitt
- Referenz für Skins, Beschreibungs Abschnitt
- Beschreibungs Abschnitt in Skins
- Skin-Definitions Dateien, Beschreibungs Abschnitt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a1b714fb917f9d13ee710509cfc5bf696e3eef
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391422"
---
# <a name="description-windows-media-player-sdk"></a><span data-ttu-id="43a7a-108">Beschreibung (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="43a7a-108">Description (Windows Media Player SDK)</span></span>

<span data-ttu-id="43a7a-109">Wenn Sie ein Skin für Windows Media Player 9-Reihe für Windows Mobile 2003 oder höher erstellen, müssen Sie einen Beschreibungs Abschnitt einschließen.</span><span class="sxs-lookup"><span data-stu-id="43a7a-109">When you create a skin for Windows Media Player 9 Series for Windows Mobile 2003 or later, you must include a Description section.</span></span> <span data-ttu-id="43a7a-110">Im Abschnitt Beschreibung können Sie die Breite und Höhe der Anzeige, die Bildschirmauflösung und die Anzeige Ausrichtung angeben, für die die Skin entworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="43a7a-110">The Description section enables you to specify the width and height of the display, the display resolution, and the display orientation for which the skin was designed.</span></span> <span data-ttu-id="43a7a-111">Der Beschreibungs Abschnitt muss in der Skin-Definitionsdatei vor jedem anderen Abschnitt und unmittelbar nach der Deklaration der ersten Version angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="43a7a-111">The Description section must appear in the skin definition file before any other section, and just after the initial version declaration.</span></span>

<span data-ttu-id="43a7a-112">Der Beschreibungs Abschnitt der Skin-Definitionsdatei muss mit der folgenden Zeile beginnen:</span><span class="sxs-lookup"><span data-stu-id="43a7a-112">The Description section of the skin definition file must begin with the following line:</span></span>


```C++
[ Description ]

```



<span data-ttu-id="43a7a-113">Anschließend müssen Sie Informationen zu den Dimensionen der Skin und der Bildschirmauflösung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="43a7a-113">You then must add information about the dimensions of the skin and the display resolution.</span></span> <span data-ttu-id="43a7a-114">Im folgenden Beispiel wird gezeigt, wie Dimensionen angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="43a7a-114">The following example shows how to specify dimensions:</span></span>


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



<span data-ttu-id="43a7a-115">Dies gibt an, dass Sie die Skin so entworfen haben, dass Sie 240 Pixel Breite, 320 Pixel hoch und die Verwendung der 96 dpi-Anzeige Auflösung anzeigt.</span><span class="sxs-lookup"><span data-stu-id="43a7a-115">This specifies that you designed the skin to be displayed 240 pixels wide, 320 pixels high, and using 96 DPI display resolution.</span></span> <span data-ttu-id="43a7a-116">Beachten Sie, dass dies eine Ausrichtung im Hochformat impliziert.</span><span class="sxs-lookup"><span data-stu-id="43a7a-116">Note that this implies a portrait mode orientation.</span></span>

<span data-ttu-id="43a7a-117">Sie können optional den Orientierungs Modus angeben, für den Sie die Skin im Abschnitt Beschreibung entworfen haben.</span><span class="sxs-lookup"><span data-stu-id="43a7a-117">You may optionally specify the orientation mode for which you designed the skin in the description section.</span></span> <span data-ttu-id="43a7a-118">Im folgenden Beispiel wird gezeigt, wie Sie die Ausrichtung angeben:</span><span class="sxs-lookup"><span data-stu-id="43a7a-118">The following example shows how to specify orientation:</span></span>


```C++
//     <Orientation>

//     -------------

    Orientation Portrait

```



<span data-ttu-id="43a7a-119">In der folgenden Tabelle sind die Werte aufgelistet, die Sie für die Ausrichtung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="43a7a-119">The following table lists the values you may use for Orientation.</span></span>



| <span data-ttu-id="43a7a-120">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="43a7a-120">Orientation</span></span> | <span data-ttu-id="43a7a-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43a7a-121">Description</span></span>                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43a7a-122">Querformat</span><span class="sxs-lookup"><span data-stu-id="43a7a-122">Landscape</span></span>   | <span data-ttu-id="43a7a-123">Die Breite der Skin ist größer als die Höhe der Skin.</span><span class="sxs-lookup"><span data-stu-id="43a7a-123">The width of the skin is greater than height of the skin.</span></span> <span data-ttu-id="43a7a-124">Die Anzeige ist horizontal ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="43a7a-124">The display is oriented in a horizontal fashion.</span></span>   |
| <span data-ttu-id="43a7a-125">Hochformat</span><span class="sxs-lookup"><span data-stu-id="43a7a-125">Portrait</span></span>    | <span data-ttu-id="43a7a-126">Die Höhe der Skin ist größer als die Breite der Skin.</span><span class="sxs-lookup"><span data-stu-id="43a7a-126">The height of the skin is greater than the width of the skin.</span></span> <span data-ttu-id="43a7a-127">Die Anzeige ist vertikal ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="43a7a-127">The display is oriented in a vertical fashion.</span></span> |
| <span data-ttu-id="43a7a-128">Square</span><span class="sxs-lookup"><span data-stu-id="43a7a-128">Square</span></span>      | <span data-ttu-id="43a7a-129">Die Höhe der Skin ist gleich der Breite der Skin.</span><span class="sxs-lookup"><span data-stu-id="43a7a-129">The height of the skin is equal to the width of the skin.</span></span> <span data-ttu-id="43a7a-130">Die Anzeige hat keine Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="43a7a-130">The display has no orientation.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="43a7a-131">Windows Media Player 9-Serie für Windows Mobile 2003 zeigt nur eine bestimmte Skin an, wenn der in der Skin-Definitionsdatei angegebene Beschreibungs Abschnitt mit dem aktuellen Status des Geräts übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="43a7a-131">Windows Media Player 9 Series for Windows Mobile 2003 will only display a particular skin when the description section specified in the skin definition file matches the current state of the device.</span></span>

 

<span data-ttu-id="43a7a-132">Sie sollten darauf achten, dass Sie immer die richtigen Dimensionen, die richtige Auflösung und die richtige Ausrichtung angeben, für die die Skin erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="43a7a-132">You should be careful to always specify the correct dimensions, resolution, and orientation for which your skin was authored.</span></span> <span data-ttu-id="43a7a-133">Wenn die von der Skin angegebenen Dimensionen z. b. eine Querformat Beschreibung beschreiben, ist die Skin nicht verfügbar, wenn sich das Gerät im Hochformat befindet, auch wenn Sie das Hochformat in der Leitungs Linie angeben.</span><span class="sxs-lookup"><span data-stu-id="43a7a-133">For example, if the dimensions specified by your skin describe a landscape orientation, your skin will not be available when the device is in portrait mode, even if you specify Portrait in the orientation line.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43a7a-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43a7a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43a7a-135">**Skin-Referenz**</span><span class="sxs-lookup"><span data-stu-id="43a7a-135">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




