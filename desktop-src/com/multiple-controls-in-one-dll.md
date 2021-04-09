---
title: Mehrere Steuerelemente in einer dll
description: Mehrere Steuerelemente in einer dll
ms.assetid: 76c1c0ef-af24-43e8-b3a7-337841c338ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e11c91faa26420f37df330ad7f1d9eff4587f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036394"
---
# <a name="multiple-controls-in-one-dll"></a><span data-ttu-id="ae8aa-103">Mehrere Steuerelemente in einer dll</span><span class="sxs-lookup"><span data-stu-id="ae8aa-103">Multiple Controls in One DLL</span></span>

<span data-ttu-id="ae8aa-104">Eine einzelne. ocx-dll kann eine beliebige Anzahl von ActiveX-Steuerelementen Container und somit die Verteilung und Verwendung eines Satzes verwandter Steuerelemente vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="ae8aa-104">A single .ocx DLL can container any number of ActiveX controls, thus simplifying the distribution and use of a set of related controls.</span></span>

<span data-ttu-id="ae8aa-105">Wenn Sie mehrere Steuerelemente in einer einzelnen dll versenden, achten Sie darauf, dass Sie den Herstellernamen in jedem Steuerelement Namen in das Paket einschließen.</span><span class="sxs-lookup"><span data-stu-id="ae8aa-105">If you ship multiple controls in a single DLL, be sure to include the vendor name in each control name in the package.</span></span> <span data-ttu-id="ae8aa-106">Wenn Sie die Namen der Lieferanten in die einzelnen Steuerelement Namen einschließen, können Benutzer Steuerelemente in einem Paket problemlos identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ae8aa-106">Including the vendors' names in each control name will enable users to easily identify controls within a package.</span></span> <span data-ttu-id="ae8aa-107">Wenn Sie z. b. eine DLL bereitstellen, die drei Steuerelemente, Con1, Con2 und Con3 implementiert, sollten die Namen der Steuerelemente wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="ae8aa-107">For example, if you ship a DLL that implements three controls, Con1, Con2, and Con3, then the control names should be:</span></span>

-   <span data-ttu-id="ae8aa-108">*Name Ihres Unternehmens* Con1-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ae8aa-108">*Your company name* Con1 Control</span></span>

-   <span data-ttu-id="ae8aa-109">*Name Ihres Unternehmens* Con2-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ae8aa-109">*Your company name* Con2 Control</span></span>

-   <span data-ttu-id="ae8aa-110">*Name Ihres Unternehmens* Con3-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ae8aa-110">*Your company name* Con3 Control</span></span>

 

 




