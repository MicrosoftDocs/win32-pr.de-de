---
title: D1104 möglicher Lecks
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: Die Factory wurde freigegeben, die von ihr erstellte Schnittstelle ist aber immer noch aktiv. Obwohl es für das Freigeben von Ressourcen nach der Freigabe der Factory gültig ist, könnte dieser Zustand auf einen Speichermangel hindeuten.
keywords:
- D1104 möglicher Lecks Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 71ccbee152d60a73fbea5ebac2a1074534b69c3a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312197"
---
# <a name="d1104-possible-leak"></a><span data-ttu-id="cdf9d-105">D1104: möglicher Lecks</span><span class="sxs-lookup"><span data-stu-id="cdf9d-105">D1104: Possible Leak</span></span>

<span data-ttu-id="cdf9d-106">Die Factory- \[ *Factory* \] wurde freigegeben, aber die \[  \] daraus erstellte Schnittstellen Schnittstelle ist immer noch aktiv.</span><span class="sxs-lookup"><span data-stu-id="cdf9d-106">The factory \[*factory*\] was released but the interface \[*interface*\] created from it is still alive.</span></span> <span data-ttu-id="cdf9d-107">Obwohl es für das Freigeben von Ressourcen nach der Freigabe der Factory gültig ist, könnte dieser Zustand auf einen Speichermangel hindeuten.</span><span class="sxs-lookup"><span data-stu-id="cdf9d-107">While it is valid to release resources after releasing the factory, this condition could be indicative of a memory leak.</span></span>

## <a name="placeholders"></a><span data-ttu-id="cdf9d-108">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="cdf9d-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="cdf9d-109"><span id="factory"></span><span id="FACTORY"></span>*schen*</span><span class="sxs-lookup"><span data-stu-id="cdf9d-109"><span id="factory"></span><span id="FACTORY"></span>*factory*</span></span>
</dt> <dd>

<span data-ttu-id="cdf9d-110">Die Adresse der freigegebenen Factory.</span><span class="sxs-lookup"><span data-stu-id="cdf9d-110">The address of the factory that was released.</span></span>

</dd> <dt>

<span data-ttu-id="cdf9d-111"><span id="interface"></span><span id="INTERFACE"></span>*berfläche*</span><span class="sxs-lookup"><span data-stu-id="cdf9d-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="cdf9d-112">Die Adresse der-Schnittstelle, die in der *Factory* erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="cdf9d-112">The address of the interface that was created on the *factory*.</span></span>

</dd> </dl> 

|             |             |
|-------------|-------------|
| <span data-ttu-id="cdf9d-113">Fehlerstufe</span><span class="sxs-lookup"><span data-stu-id="cdf9d-113">Error Level</span></span> | <span data-ttu-id="cdf9d-114">Information</span><span class="sxs-lookup"><span data-stu-id="cdf9d-114">Information</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="cdf9d-115">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="cdf9d-115">Possible Causes</span></span>

<span data-ttu-id="cdf9d-116">Die Factory wurde freigegeben, die von ihr erstellte Schnittstelle ist aber immer noch aktiv.</span><span class="sxs-lookup"><span data-stu-id="cdf9d-116">The factory was released but the interface created from it is still alive.</span></span>

 

 




