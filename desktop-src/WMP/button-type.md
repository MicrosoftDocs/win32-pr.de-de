---
title: Schalt Flächentyp
description: Schalt Flächentyp
ms.assetid: 0c9e72d5-5cc4-4d6f-b184-2c8c8487e366
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Typen
- Skins, Schaltflächen Typen
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58eeb7402a13730fd7f4030d2e4326fe7f18e63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855683"
---
# <a name="button-type"></a><span data-ttu-id="ac644-107">Schalt Flächentyp</span><span class="sxs-lookup"><span data-stu-id="ac644-107">Button Type</span></span>

<span data-ttu-id="ac644-108">Schaltflächen verfügen über zwei allgemeine Typen: "Location" und "Region".</span><span class="sxs-lookup"><span data-stu-id="ac644-108">Buttons come in two general types: location and region.</span></span> <span data-ttu-id="ac644-109">Jeder allgemeine Typ verfügt über drei bestimmte Typen, die jeweils sechs Schaltflächen Typen erstellen.</span><span class="sxs-lookup"><span data-stu-id="ac644-109">Each general type has three specific types, making six button types in all.</span></span>

> [!Note]  
> <span data-ttu-id="ac644-110">Schaltflächen Typen sind in Skins für Windows Media Player 10 Mobile oder höher veraltet.</span><span class="sxs-lookup"><span data-stu-id="ac644-110">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="ac644-111">Location-Schaltflächen Typen</span><span class="sxs-lookup"><span data-stu-id="ac644-111">Location Button Types</span></span>

<span data-ttu-id="ac644-112">Standort Schaltflächen verwenden Koordinaten, um Ihre Positionen relativ zum Hintergrund zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ac644-112">Location buttons use coordinates to define their locations relative to the background.</span></span> <span data-ttu-id="ac644-113">In der folgenden Tabelle sind die Werte aufgeführt, die für Speicherort-Schaltflächen Typen gültig sind.</span><span class="sxs-lookup"><span data-stu-id="ac644-113">The following table shows the values that are valid for location button types.</span></span> <span data-ttu-id="ac644-114">Sie müssen keine Werte für Typen definieren, die in der Skin nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac644-114">You do not need to define values for types you will not be using in your skin.</span></span>



| <span data-ttu-id="ac644-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ac644-115">Value</span></span>  | <span data-ttu-id="ac644-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac644-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac644-117">Push</span><span class="sxs-lookup"><span data-stu-id="ac644-117">Push</span></span>   | <span data-ttu-id="ac644-118">Definiert eine Schaltfläche, die ein Ereignis einmal auslöst.</span><span class="sxs-lookup"><span data-stu-id="ac644-118">Defines a button that triggers an event once.</span></span> <span data-ttu-id="ac644-119">Die Schaltfläche muss jedes Mal pusht werden, um weitere Ereignisse zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="ac644-119">The button must be pushed each time to trigger further events.</span></span> <span data-ttu-id="ac644-120">Ein Beispiel wäre eine Schaltfläche, die zum nächsten Element in der Wiedergabeliste wechselt.</span><span class="sxs-lookup"><span data-stu-id="ac644-120">An example would be a button that moves to the next item in the playlist.</span></span> <span data-ttu-id="ac644-121">Der Speicherort der Schaltfläche wird durch seine Koordinaten definiert.</span><span class="sxs-lookup"><span data-stu-id="ac644-121">The location of the button is defined by its coordinates.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ac644-122">Ein-/Ausschalten</span><span class="sxs-lookup"><span data-stu-id="ac644-122">Toggle</span></span> | <span data-ttu-id="ac644-123">Definiert eine Schaltfläche, die ein Ereignis auslöst, das einen Zustand ändert.</span><span class="sxs-lookup"><span data-stu-id="ac644-123">Defines a button that triggers an event that changes a state.</span></span> <span data-ttu-id="ac644-124">Der Status bleibt bestehen, bis die Schaltfläche erneut verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="ac644-124">The state remains until the button is pushed again.</span></span> <span data-ttu-id="ac644-125">Ein Beispiel ist eine Schaltfläche, mit der die Wiedergabeliste heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="ac644-125">An example is a button that shuffles the playlist.</span></span> <span data-ttu-id="ac644-126">Wenn sich die Wiedergabeliste in einem gemischten Zustand befindet, bleibt Sie gemischt, bis die Schaltfläche erneut verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="ac644-126">Once the playlist is in a shuffled state, it will remain shuffled until the button is pushed again.</span></span> <span data-ttu-id="ac644-127">Der Speicherort der Schaltfläche wird durch seine Koordinaten definiert.</span><span class="sxs-lookup"><span data-stu-id="ac644-127">The location of the button is defined by its coordinates.</span></span>                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ac644-128">2push</span><span class="sxs-lookup"><span data-stu-id="ac644-128">2Push</span></span>  | <span data-ttu-id="ac644-129">Definiert eine Schaltfläche, die ein Ereignis auslöst, und wechselt in einen Zustand, der zum Auslösen eines anderen Ereignisses bereit ist.</span><span class="sxs-lookup"><span data-stu-id="ac644-129">Defines a button that triggers an event, and then changes to a state that is ready to trigger a different event.</span></span> <span data-ttu-id="ac644-130">Die beiden Zustände werden jedes Mal ein-und ausgeschaltet, wenn die Schaltfläche gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="ac644-130">The two states are toggled every time the button is pushed.</span></span> <span data-ttu-id="ac644-131">Ein Beispiel hierfür ist eine Schaltfläche, die die Funktion **PLAYPAUSE** verwendet, um zwischen Wiedergabe und Anhalten des aktuellen Medien Elements zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="ac644-131">An example is a button that uses the **PlayPause** function to toggle between playing and pausing the current media item.</span></span> <span data-ttu-id="ac644-132">Wenn die Schaltfläche zum ersten Mal per Pushvorgang übertragen wird, wird der primäre Wiedergabe Zustand ausgelöst und ein sekundäres Bild angezeigt, um anzugeben, dass ein **Pausen** Ereignis ausgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="ac644-132">When the button is pushed the first time, the primary Play state is triggered and a secondary image is displayed to indicate that a **Pause** event can be triggered.</span></span> <span data-ttu-id="ac644-133">Wenn die Schaltfläche erneut verschoben wird, wird der Pause-Zustand ausgelöst, und das ursprüngliche Bild wird angezeigt, um anzugeben, dass ein **Wiedergabe** Ereignis ausgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="ac644-133">When the button is pushed again, the Pause state is triggered and the original image is displayed to indicate that a **Play** event can be triggered.</span></span> <span data-ttu-id="ac644-134">Der Speicherort der Schaltfläche wird durch seine Koordinaten definiert.</span><span class="sxs-lookup"><span data-stu-id="ac644-134">The location of the button is defined by its coordinates.</span></span> |



 

<span data-ttu-id="ac644-135">Regions-Schaltflächen Typen</span><span class="sxs-lookup"><span data-stu-id="ac644-135">Region Button Types</span></span>

<span data-ttu-id="ac644-136">Bereichs Schaltflächen verwenden Farbbereiche im Regions Bild, um zu definieren, wo Abzweigungen für eine bestimmte Schaltfläche verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ac644-136">Region buttons use color areas in the Region image to define where taps will be processed for a particular button.</span></span> <span data-ttu-id="ac644-137">In der folgenden Tabelle sind die Werte aufgeführt, die für Regions Schaltflächen Typen gültig sind.</span><span class="sxs-lookup"><span data-stu-id="ac644-137">The following table shows the values that are valid for region button types.</span></span> <span data-ttu-id="ac644-138">Sie müssen keine Werte für Typen definieren, die in der Skin nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac644-138">You do not need to define values for types you will not be using in your skin.</span></span>



| <span data-ttu-id="ac644-139">Wert</span><span class="sxs-lookup"><span data-stu-id="ac644-139">Value</span></span>     | <span data-ttu-id="ac644-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac644-140">Description</span></span>                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac644-141">Pushtreffer</span><span class="sxs-lookup"><span data-stu-id="ac644-141">PushHit</span></span>   | <span data-ttu-id="ac644-142">Vergleichbar mit dem Wert der Push-Schaltfläche, mit dem Unterschied, dass der Trefferbereich der Schaltfläche durch den Farbwert im Bereichs Bild definiert wird.</span><span class="sxs-lookup"><span data-stu-id="ac644-142">Similar to the Push button value except that the hit area of the button is defined by the color value in the Region image.</span></span>   |
| <span data-ttu-id="ac644-143">Ein-und klein Treffer</span><span class="sxs-lookup"><span data-stu-id="ac644-143">ToggleHit</span></span> | <span data-ttu-id="ac644-144">Ähnlich wie beim Wert der UMSCHALT Fläche, mit der Ausnahme, dass der Trefferbereich der Schaltfläche durch den Farbwert im Bild des Bereichs definiert wird.</span><span class="sxs-lookup"><span data-stu-id="ac644-144">Similar to the Toggle button value except that the hit area of the button is defined by the color value in the Region image.</span></span> |
| <span data-ttu-id="ac644-145">2pushhit</span><span class="sxs-lookup"><span data-stu-id="ac644-145">2PushHit</span></span>  | <span data-ttu-id="ac644-146">Ähnelt dem 2push-Schaltflächen Wert, mit dem Unterschied, dass der Trefferbereich der Schaltfläche durch den Farbwert im Bereichs Bild definiert wird.</span><span class="sxs-lookup"><span data-stu-id="ac644-146">Similar to the 2Push button value except that the hit area of the button is defined by the color value in the Region image.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="ac644-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ac644-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac644-148">**Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="ac644-148">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




