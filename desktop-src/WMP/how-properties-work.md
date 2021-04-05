---
title: Funktionsweise von Eigenschaften
description: Funktionsweise von Eigenschaften
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- Windows Media Player-Plug-ins, Echo-Beispiel Eigenschaften
- Plug-ins, Echo-Beispiel Eigenschaften
- Plug-Ins für die digitale Signalverarbeitung, Echo-Beispiel Eigenschaften
- DSP-Plug-ins, Echo-Beispiel Eigenschaften
- Echo DSP-Plug-in-Beispiel, Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad37b71ddc6a097dd43e1ac41147c571f81a67a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711562"
---
# <a name="how-properties-work"></a><span data-ttu-id="9cc8b-108">Funktionsweise von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9cc8b-108">How Properties Work</span></span>

<span data-ttu-id="9cc8b-109">Eigenschaftswerte werden in Element Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9cc8b-109">Property values are stored in member variables.</span></span>

<span data-ttu-id="9cc8b-110">Eigenschaften werden über Methoden Paare zugänglich gemacht.</span><span class="sxs-lookup"><span data-stu-id="9cc8b-110">Properties are made accessible by method pairs.</span></span> <span data-ttu-id="9cc8b-111">Eine Methode stellt die-Implementierung bereit, um den Eigenschafts Wert anzugeben. der Name beginnt mit Put \_ .</span><span class="sxs-lookup"><span data-stu-id="9cc8b-111">One method provides the implementation to specify the property value; its name starts with put\_.</span></span> <span data-ttu-id="9cc8b-112">Die andere Methode stellt die-Implementierung bereit, um den Eigenschafts Wert abzurufen. der Name beginnt mit get \_ .</span><span class="sxs-lookup"><span data-stu-id="9cc8b-112">The other method provides the implementation to retrieve the property value; its name starts with get\_.</span></span> <span data-ttu-id="9cc8b-113">Die Schnittstellen Definition ist in Echo. idl enthalten.</span><span class="sxs-lookup"><span data-stu-id="9cc8b-113">The interface definition is in Echo.idl.</span></span> <span data-ttu-id="9cc8b-114">Die Eigenschaften Methoden Prototypen befinden sich in Echo. h.</span><span class="sxs-lookup"><span data-stu-id="9cc8b-114">The property method prototypes are in Echo.h.</span></span> <span data-ttu-id="9cc8b-115">Sie werden in Echo. cpp implementiert.</span><span class="sxs-lookup"><span data-stu-id="9cc8b-115">They are implemented in Echo.cpp.</span></span>

<span data-ttu-id="9cc8b-116">In den nächsten drei Abschnitten erfahren Sie, wie Sie die vorhandenen Eigenschaften Methoden entsprechend Ihren Anforderungen ändern und wie Sie die Methoden für eine zusätzliche Eigenschaft hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9cc8b-116">The next three sections will show you how to modify the existing property methods to suit your needs and how to add the methods for an additional property.</span></span>

-   [<span data-ttu-id="9cc8b-117">Variablen zum Speichern von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9cc8b-117">Variables to Store Properties</span></span>](variables-to-store-properties.md)
-   [<span data-ttu-id="9cc8b-118">Ändern der Scale-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9cc8b-118">Modifying the Scale Property</span></span>](modifying-the-scale-property.md)
-   [<span data-ttu-id="9cc8b-119">Hinzufügen der Eigenschaft "nass Mischung"</span><span class="sxs-lookup"><span data-stu-id="9cc8b-119">Adding the Wet Mix Property</span></span>](adding-the-wet-mix-property.md)

## <a name="related-topics"></a><span data-ttu-id="9cc8b-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9cc8b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cc8b-121">**Echo-Beispiel Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="9cc8b-121">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




