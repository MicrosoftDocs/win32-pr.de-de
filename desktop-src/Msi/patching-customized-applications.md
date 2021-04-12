---
description: Wenn Sie einen Patch und eine oder mehrere Anpassungs Transformationen in eine Anwendung installieren, wird der Patch in der Regel zuerst installiert, gefolgt von den Anpassungs Transformationen.
ms.assetid: 39a58174-fa62-42e3-a0aa-4cc541c2e36b
title: Patchen von angepassten Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289685ebc390de750ea9c47ddfae6ef58ec87116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345549"
---
# <a name="patching-customized-applications"></a><span data-ttu-id="73b34-103">Patchen von angepassten Anwendungen</span><span class="sxs-lookup"><span data-stu-id="73b34-103">Patching Customized Applications</span></span>

<span data-ttu-id="73b34-104">Wenn Sie einen Patch und eine oder mehrere Anpassungs Transformationen in eine Anwendung installieren, wird der Patch in der Regel zuerst installiert, gefolgt von den Anpassungs Transformationen.</span><span class="sxs-lookup"><span data-stu-id="73b34-104">When installing a patch and one or more customization transforms to an application, the patch is typically installed first, followed by the customization transforms.</span></span> <span data-ttu-id="73b34-105">Der Patch wird von der nachfolgenden Installation der Anpassung nicht untergliedert.</span><span class="sxs-lookup"><span data-stu-id="73b34-105">By design, the patch is not broken by the subsequent installation of the customization.</span></span> <span data-ttu-id="73b34-106">Allerdings kann die Anpassung bei der erstmaligen Installation der Transformationen und dann dem Patch unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="73b34-106">However, installing the transforms first, and then the patch, may break the customization.</span></span>

<span data-ttu-id="73b34-107">Beispielsweise kann eine Unterbrechung der Anpassung auftreten, wenn ein Patch verwendet wird, um ein Produkt von Version 1 auf Version 2 zu aktualisieren, und eine Anpassungs Transformation, die für Version 1 funktioniert, nicht für Version 2 funktioniert.</span><span class="sxs-lookup"><span data-stu-id="73b34-107">For example, a break in the customization could occur when a patch is used to update a product from version 1 to version 2 and a customization transform that works for version 1 does not work for version 2.</span></span> <span data-ttu-id="73b34-108">In diesem Fall kann der Patch für die Versions Aktualisierung nicht auf ein angepasstes Produkt angewendet werden, ohne zunächst deinstallieren und dann das ursprüngliche Produkt neu installieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="73b34-108">In this case, the version update patch cannot be applied to a customized product without first uninstalling and then reinstalling the original product.</span></span>

 

 



