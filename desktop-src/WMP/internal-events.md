---
title: Interne Ereignisse
description: Interne Ereignisse
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- Windows Media Player Skins, interne Ereignisse
- Skins, interne Ereignisse
- Ereignisse, intern
- Schreiben von Code für Skins, interne Ereignisse
- interne Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08ed2abca3f23a89ea6fe261a29639d671e0d58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947500"
---
# <a name="internal-events"></a><span data-ttu-id="7a9d3-108">Interne Ereignisse</span><span class="sxs-lookup"><span data-stu-id="7a9d3-108">Internal Events</span></span>

<span data-ttu-id="7a9d3-109">Sie können Änderungen erkennen, die in Windows-Media Player oder Änderungen in ihrer eigenen Skin auftreten.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-109">You can detect changes that occur in Windows Media Player or changes in your own skin.</span></span> <span data-ttu-id="7a9d3-110">Dabei kann es sich um Änderungen in den Eigenschaften oder Methoden von Windows-Media Player Objekten, Änderungen in den Skin-Attributen usw. handeln.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-110">These can be changes in Windows Media Player object properties or methods, changes in skin attributes, and so on.</span></span>

## <a name="windows-media-player-property-changes"></a><span data-ttu-id="7a9d3-111">Änderungen an der Windows Media Player-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7a9d3-111">Windows Media Player Property Changes</span></span>

<span data-ttu-id="7a9d3-112">Sie können Änderungen in Windows Media Player mithilfe des wmpprop-Listener verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-112">You can process changes in Windows Media Player by using the wmpprop listener.</span></span> <span data-ttu-id="7a9d3-113">Sie müssen den Listener als Wert eines Attributs einrichten.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-113">You must set up the listener as a value of an attribute.</span></span> <span data-ttu-id="7a9d3-114">Fügen Sie den Wert in doppelte Anführungszeichen ein, und beginnen Sie mit dem Wort "wmpprop", gefolgt von einem Doppelpunkt.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-114">Put the value in double quotes, and start with the word "wmpprop" followed by a colon.</span></span> <span data-ttu-id="7a9d3-115">Dann fügen Sie die Eigenschaft ein, die Sie überwachen möchten.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-115">Then you include the property you want to listen to.</span></span> <span data-ttu-id="7a9d3-116">Wenn sich die-Eigenschaft ändert, ändert sich auch der Wert des-Attributs.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-116">When the property changes, the value of the attribute will change also.</span></span> <span data-ttu-id="7a9d3-117">Wenn Sie z. b. einen Wert für den Schieberegler Element ändern möchten, wenn sich der Wert des **CurrentPosition** -Attributs ändert, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="7a9d3-117">For example, to have a slider element value change whenever the value of the **currentPosition** attribute changes, type the following:</span></span>


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   <span data-ttu-id="7a9d3-118">**Wichtig** Verwenden Sie wmpprop nicht für Windows-Media Player Methoden.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-118">**Important** Do not use wmpprop on Windows Media Player methods.</span></span> <span data-ttu-id="7a9d3-119">Unerwartete Ergebnisse können auftreten.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-119">Unexpected results may occur.</span></span>

## <a name="windows-media-player-method-changes"></a><span data-ttu-id="7a9d3-120">Windows Media Player-Methoden Änderungen</span><span class="sxs-lookup"><span data-stu-id="7a9d3-120">Windows Media Player Method Changes</span></span>

<span data-ttu-id="7a9d3-121">Sie können Ihre Skin auf die Verfügbarkeit von Methoden unter Windows Media Player mithilfe von wmpaktiviertem und wmpdeaktiviert festlegen.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-121">You can make your skin respond to the availability of methods on Windows Media Player using wmpenabled and wmpdisabled.</span></span> <span data-ttu-id="7a9d3-122">Diese werden ähnlich wie der wmpprop-Listener verwendet, mit dem Unterschied, dass Sie diese nur für Methoden des **Steuer** Element Objekts verwenden können, die von der **IsAvailable** -Methode unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-122">These are used similarly to the wmpprop listener except that you can only use these on methods of the **Control** object that are supported by the **isAvailable** method.</span></span>

<span data-ttu-id="7a9d3-123">Beispielsweise können Sie eine Schaltfläche nur aktivieren, wenn die **Play** -Methode aktiviert ist, indem Sie Code wie den folgenden verwenden:</span><span class="sxs-lookup"><span data-stu-id="7a9d3-123">For example, you could enable a button only when the **Play** method is enabled, using code like this:</span></span>


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   <span data-ttu-id="7a9d3-124">**Wichtig** Verwenden Sie wmpaktivierte oder wmpdeaktivierte Windows-Media Player Eigenschaften nicht.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-124">**Important** Do not use wmpenabled or wmpdisabled on Windows Media Player properties.</span></span> <span data-ttu-id="7a9d3-125">Unerwartete Ergebnisse können auftreten.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-125">Unexpected results may occur.</span></span>

## <a name="skin-attribute-changes"></a><span data-ttu-id="7a9d3-126">Skin-Attribut Änderungen</span><span class="sxs-lookup"><span data-stu-id="7a9d3-126">Skin Attribute Changes</span></span>

<span data-ttu-id="7a9d3-127">Sie können auf Änderungen in den Skin-Attributen auf eine von zwei Arten reagieren, indem Sie wmpprop oder das **\_ OnChange** -Ereignis verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-127">You can respond to changes in your skin attributes in one of two ways, by using wmpprop or the **\_onchange** event.</span></span>

<span data-ttu-id="7a9d3-128">Sie können wmpprop verwenden, um auf Änderungen in ihrer eigenen Skin zu lauschen.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-128">You can use wmpprop to listen for changes in your own skin.</span></span> <span data-ttu-id="7a9d3-129">Wenn Sie z. b. den Wert des Schiebereglers in einem Textfeld anzeigen möchten, können Sie Folgendes eingeben:</span><span class="sxs-lookup"><span data-stu-id="7a9d3-129">For example, to show the Slider value in a text box, you could type the following:</span></span>


```C++
<TEXT ... value="wmpprop:mySlider.value">

```



<span data-ttu-id="7a9d3-130">Sie können das **\_ OnChange** -Ereignis verwenden, um Ereignisse in einem Element zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-130">You can use the **\_onchange** event to process events inside an element.</span></span> <span data-ttu-id="7a9d3-131">Sie müssen den Namen des Attributs, das Sie nachverfolgen möchten, an **\_ OnChange** anfügen.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-131">You must attach the name of the attribute you want to track to **\_onchange**.</span></span> <span data-ttu-id="7a9d3-132">Wenn Sie z. b. den Wert eines Textfelds überprüfen möchten, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="7a9d3-132">For example, if you want to track the value of a text box, you would type:</span></span>


```C++
value_onchange

```



<span data-ttu-id="7a9d3-133">Anschließend würden Sie eine JScript-Zeichenfolge zuweisen, die Sie ausführen möchten, wenn sich der Wert ändert.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-133">You would then assign a JScript string that you want to run when the value changes.</span></span> <span data-ttu-id="7a9d3-134">Um z. b. auf eine Änderung des Werts eines Textfelds zu reagieren, das zum Anpassen des Umfangs von Windows Media Player verwendet werden kann, geben Sie Folgendes in Ihrem **Text** -Element als Attribut ein:</span><span class="sxs-lookup"><span data-stu-id="7a9d3-134">For example, to respond to a change in the value of a text box that can be used to adjust the volume of Windows Media Player, type the following inside your **TEXT** element as an attribute:</span></span>


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a><span data-ttu-id="7a9d3-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7a9d3-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a9d3-136">**Behandeln von Ereignissen**</span><span class="sxs-lookup"><span data-stu-id="7a9d3-136">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




