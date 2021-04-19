---
title: Unterschiede zwischen den Objekt Modellen
description: Unterschiede zwischen den Objekt Modellen
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Windows Media Player, Objektmodell
- Windows Media Player-Objektmodell, Versions Unterschiede
- Objektmodell, Versions Unterschiede
- Windows Media Player ActiveX-Steuerelement, Versions Unterschiede
- ActiveX-Steuerelement, Versions Unterschiede
- Windows Media Player Mobile ActiveX-Steuerelement, Versions Unterschiede
- Windows Media Player Mobile, Objektmodell
- Migrations Handbuch, Versions Unterschiede
- Versionen von Windows Media Player, Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5341067e2daad0f44fbdd7075f0f543bac2fd4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341256"
---
# <a name="differences-between-the-object-models"></a><span data-ttu-id="e1c7b-112">Unterschiede zwischen den Objekt Modellen</span><span class="sxs-lookup"><span data-stu-id="e1c7b-112">Differences Between the Object Models</span></span>

<span data-ttu-id="e1c7b-113">Zwischen dem Objektmodell Windows Media Player 6,4 und dem Objektmodell Windows Media Player 7 oder höher bestehen zwei wesentliche Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="e1c7b-113">There are two primary differences between the Windows Media Player 6.4 object model and the Windows Media Player 7 or later object model.</span></span>

-   <span data-ttu-id="e1c7b-114">**CLSID** Das Objektmodell von Windows Media Player 7 oder höher ist eine vollständige Abweichung vom Objektmodell der Version 6,4.</span><span class="sxs-lookup"><span data-stu-id="e1c7b-114">**CLSID** The Windows Media Player 7 or later object model is a complete departure from the version 6.4 object model.</span></span> <span data-ttu-id="e1c7b-115">Die Component Object Model (com)-Spezifikation erfordert, dass alle vorhandenen Schnittstellen in neuen Versionen einer COM-Komponente weiterhin funktionieren.</span><span class="sxs-lookup"><span data-stu-id="e1c7b-115">The Component Object Model (COM) specification requires that all existing interfaces must continue to function in new versions of a COM component.</span></span> <span data-ttu-id="e1c7b-116">Dies bedeutet, dass neue Schnittstellen zu einer COM-Komponente hinzugefügt werden können, vorhandene Schnittstellen jedoch nie geändert werden müssen, um sicherzustellen, dass der ältere Client Code immer mit der jeweiligen Komponente funktioniert, für die er verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1c7b-116">This means that new interfaces can be added to a COM component, but existing interfaces must never be altered, ensuring older client code will always work with the particular component it was designed to use.</span></span> <span data-ttu-id="e1c7b-117">Das ActiveX-Steuerelement von Windows Media Player 7 oder höher hat daher eine neue Klassen-ID: 6BF 52a52-394a-11d3-b153-00c04s faa6.</span><span class="sxs-lookup"><span data-stu-id="e1c7b-117">Therefore, the Windows Media Player 7 or later ActiveX control has a new class ID: 6BF52A52-394A-11D3-B153-00C04F79FAA6.</span></span> <span data-ttu-id="e1c7b-118">Wenn Sie die neuen Funktionen des Steuer Elements für diese Version nutzen möchten, müssen Sie die CLSID ändern.</span><span class="sxs-lookup"><span data-stu-id="e1c7b-118">If you want to take advantage of the new functionality of the control for this version, you must change your CLSID.</span></span>
-   <span data-ttu-id="e1c7b-119">**Hierarchisches Objektmodell** Wenn Sie das ActiveX-Steuerelement von Windows Media Player 6,4 verwendet haben, haben Sie möglicherweise bemerkt, dass auf alle Eigenschaften, Methoden und Ereignisse über das gleiche Objekt zugegriffen wird: das **Player** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="e1c7b-119">**Hierarchical Object Model** If you've been using the Windows Media Player 6.4 ActiveX control, you may have noticed that all the properties, methods, and events are accessed through the same object: the **Player** object.</span></span> <span data-ttu-id="e1c7b-120">Im Gegensatz dazu ist das Objektmodell Windows Media Player 7 oder höher als eine Hierarchie von Objekten organisiert.</span><span class="sxs-lookup"><span data-stu-id="e1c7b-120">By contrast, the Windows Media Player 7 or later object model is organized as a hierarchy of objects.</span></span> <span data-ttu-id="e1c7b-121">Das **Player** -Objekt ist nach wie vor das Root-Objekt, aber auf Funktionen wird jetzt über eine Vielzahl von untergeordneten Objekten zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="e1c7b-121">The **Player** object is still the root object, but functions are now accessed through a variety of child objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1c7b-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1c7b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1c7b-123">**Handbuch für die Migration des Objektmodells**</span><span class="sxs-lookup"><span data-stu-id="e1c7b-123">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




