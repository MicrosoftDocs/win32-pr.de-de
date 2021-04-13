---
description: Automatische Ressourcenrückgewinnung
ms.assetid: c889dd3f-82d1-4bc3-ac2c-6f468d5b2c7f
title: Automatische Ressourcenrückgewinnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f76721df1a3858c9ad97d2f696115fff2eb6d3d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342289"
---
# <a name="automatic-resource-reclamation"></a><span data-ttu-id="8f5cc-103">Automatische Ressourcenrückgewinnung</span><span class="sxs-lookup"><span data-stu-id="8f5cc-103">Automatic Resource Reclamation</span></span>

<span data-ttu-id="8f5cc-104">Com+ benachrichtigt den Dispenser Manager, wenn die Lebensdauer eines Objekts endet.</span><span class="sxs-lookup"><span data-stu-id="8f5cc-104">COM+ notifies the dispenser manager each time an object's lifetime ends.</span></span> <span data-ttu-id="8f5cc-105">Der Dispenser-Manager benachrichtigt dann jeden Inhaber des registrierten Ressourcen Verteilers, ob er über Ressourcen verfügt, die noch von diesem Objekt aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="8f5cc-105">The dispenser manager then notifies each registered resource dispenser's Holder to see whether it has any resources still held by this object.</span></span> <span data-ttu-id="8f5cc-106">Wenn dies der Fall ist, werden diese Ressourcen freigegeben. Dadurch wird die Möglichkeit von Ressourcenverlusten durch Komponenten verhindert, die Ressourcen über einen Ressourcen Verteiler erhalten.</span><span class="sxs-lookup"><span data-stu-id="8f5cc-106">If so, those resources are freed, preventing the possibility of resource leaks by components that get resources through a resource dispenser.</span></span>

<span data-ttu-id="8f5cc-107">Bei der automatischen Freigabe handelt es sich um eine Option, die standardmäßig deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8f5cc-107">The auto-reclamation feature is an option that is turned off by default.</span></span> <span data-ttu-id="8f5cc-108">Ein Ressourcen Verteiler kann diese Option aktivieren und garantiert, dass ein Verweis auf eine Ressource, die an ein Objekt ausgegeben wird, niemals von den Objektmethoden zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8f5cc-108">A resource dispenser can choose to enable this option and, in doing so, guarantees that a reference to any resource dispensed to an object is never returned by the object methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f5cc-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8f5cc-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f5cc-110">Konzepte des com+-Ressourcen Verteilers</span><span class="sxs-lookup"><span data-stu-id="8f5cc-110">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



