---
description: Das Merge-Objekt ermöglicht den Zugriff auf andere Objekte der obersten Ebene. Vor dem Laden der für com erforderlichen Automatisierungsunterstützung muss ein Merge-Objekt erstellt werden, um auf die Funktionen in Mergemod.dll zugreifen zu können.
ms.assetid: 3f76ee8a-d195-4a69-99a3-31ef2c1c72d5
title: Merge-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1379202d4f252560a381f8af09b30741faa060ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218343"
---
# <a name="merge-object"></a><span data-ttu-id="06aeb-104">Merge-Objekt</span><span class="sxs-lookup"><span data-stu-id="06aeb-104">Merge Object</span></span>

<span data-ttu-id="06aeb-105">Das **Merge** -Objekt ermöglicht den Zugriff auf andere Objekte der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="06aeb-105">The **Merge** object provides access to other top-level objects.</span></span> <span data-ttu-id="06aeb-106">Vor dem Laden der für com erforderlichen Automatisierungsunterstützung muss ein **Merge** -Objekt erstellt werden, um auf die Funktionen in Mergemod.dll zugreifen zu können.</span><span class="sxs-lookup"><span data-stu-id="06aeb-106">A **Merge** object must be created before loading the automation support required by COM to access the functions in Mergemod.dll.</span></span>

<span data-ttu-id="06aeb-107">Mergemod.dll bietet bei der Buildzeit Zugriff auf die erweiterte Funktionalität über eine zweite Version der vorhandenen CLSID.</span><span class="sxs-lookup"><span data-stu-id="06aeb-107">Mergemod.dll provides access to the extended functionality at build time through a second version of the existing CLSID.</span></span> <span data-ttu-id="06aeb-108">Diese CLSID unterstützt die vorhandene Funktionalität, die über die [**imsmmerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) -Schnittstelle verfügbar ist, aber die Standardschnittstelle für das Objekt (und die zugeordnete duale Schnittstelle) ist die [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) -Schnittstelle anstelle der **imsmmerge** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="06aeb-108">This CLSID supports existing functionality available through the [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) interface, but the default interface on the object (and the associated dual interface) is the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) interface instead of the **IMsmMerge** interface.</span></span>

 

 
