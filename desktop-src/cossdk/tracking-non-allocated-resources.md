---
description: Nachverfolgen nicht zugewiesener Ressourcen
ms.assetid: ebaca876-5249-4b6b-b0d5-08f098e3f5f5
title: Nachverfolgen nicht zugewiesener Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c9f814e08798b4fbb0f160e0d0e0f8aabebba7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342607"
---
# <a name="tracking-non-allocated-resources"></a><span data-ttu-id="fd4e3-103">Nachverfolgen nicht zugewiesener Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fd4e3-103">Tracking Non-Allocated Resources</span></span>

<span data-ttu-id="fd4e3-104">Der Dispenser Manager kann eine Ressource, die nicht inventarisiert ist, basierend auf dem Wissen der Lebensdauer des Objekts nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-104">The dispenser manager can track a resource that is not inventoried, based on knowledge of the object's lifetime.</span></span> <span data-ttu-id="fd4e3-105">Wenn eine nach verfolgte, nicht zugewiesene Ressource freigegeben wird, wird Sie zerstört und daher nicht an die Inventur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-105">When a tracked, non-allocated resource is freed, it is destroyed and therefore not returned to inventory.</span></span> <span data-ttu-id="fd4e3-106">Dieser Modus für Ressourcen, die für die Erstellung und Zerstörung kostengünstiger sind, ist nützlicher als die Speicherung im Inventar.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-106">This track-only mode for resources that are inexpensive to create and destroy is more useful than storing them in inventory.</span></span> <span data-ttu-id="fd4e3-107">Dieser Modus ist auch nützlich für die Verwaltung eines Speicher Verteilers oder für eine Ressource, die schwer zu inventarisieren ist, da zu viele verschiedene Typen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-107">This mode is also useful for managing a memory dispenser or for a resource that is difficult to inventory because there are too many different types.</span></span>

<span data-ttu-id="fd4e3-108">Im Modus "nur Nachverfolgung" erstellt ein Ressourcen Verteiler direkt eine angeforderte Ressource, anstatt den Dispenser-Manager aufzufordern, einen aus dem Inventar zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-108">In track-only mode, a resource dispenser directly creates a requested resource instead of asking the dispenser manager to allocate one from inventory.</span></span> <span data-ttu-id="fd4e3-109">Bevor diese Ressource an die anfordernde Anwendungs Komponente zurückgegeben wird, weist der Ressourcen Verteiler dem Dispenser Manager an, die Ressource zu überprüfen. auf diese Weise wird sichergestellt, dass selbst dann, wenn die Komponente die Ressource nicht freigibt, der Dispenser-Manager dies tut, wenn die Lebensdauer der Komponente übersteigt.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-109">Before returning this resource to the requesting application component, the resource dispenser tells the dispenser manager to track the resource, which ensures that even if the component neglects to free the resource, the dispenser manager will do so when the component's lifetime is over.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd4e3-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd4e3-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd4e3-111">Konzepte des com+-Ressourcen Verteilers</span><span class="sxs-lookup"><span data-stu-id="fd4e3-111">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



