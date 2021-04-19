---
title: Iwmpdvd-Domänen Eigenschaft
description: Die Domänen Eigenschaft ruft die aktuelle Domäne der DVD ab.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- Domänen Eigenschaften Fenster Media Player
- Domänen Eigenschaft Windows Media Player, iwmpdvd-Schnittstelle
- Iwmpdvd-Schnittstelle, Windows Media Player, Domäne (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPDVD.domain
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6546a8288160fe80f7df4a7c41ea79a0edc905f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367792"
---
# <a name="iwmpdvddomain-property"></a><span data-ttu-id="fd477-106">Iwmpdvd::d omain-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fd477-106">IWMPDVD::domain property</span></span>

<span data-ttu-id="fd477-107">Die **Domänen** Eigenschaft ruft die aktuelle Domäne der DVD ab.</span><span class="sxs-lookup"><span data-stu-id="fd477-107">The **domain** property gets the current domain of the DVD.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd477-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd477-108">Syntax</span></span>


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a><span data-ttu-id="fd477-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fd477-109">Property value</span></span>

<span data-ttu-id="fd477-110">Ein **System. String** -Wert, der einem der folgenden Werte entspricht.</span><span class="sxs-lookup"><span data-stu-id="fd477-110">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="fd477-111">Wert</span><span class="sxs-lookup"><span data-stu-id="fd477-111">Value</span></span>                                                                                        | <span data-ttu-id="fd477-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fd477-112">Meaning</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd477-113"><dt>FirstPlay</dt></span><span class="sxs-lookup"><span data-stu-id="fd477-113"><dt>firstPlay</dt></span></span> </dl>         | <span data-ttu-id="fd477-114">Die Standard Initialisierung einer DVD-CD wird durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd477-114">Performing default initialization of a DVD disc.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="fd477-115"><dt>videomanagermenu</dt></span><span class="sxs-lookup"><span data-stu-id="fd477-115"><dt>videoManagerMenu</dt></span></span> </dl>  | <span data-ttu-id="fd477-116">Anzeigen von Menüs für die gesamte Festplatte. Wird auch als "topmenu" für Windows-Media Player bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fd477-116">Displaying menus for the entire disc. Also known as topMenu for Windows Media Player.</span></span> <span data-ttu-id="fd477-117">Wird üblicherweise als Titelmenü oder im oberen Menü bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fd477-117">Commonly called the title menu or the top menu.</span></span><br/> |
| <dl> <span data-ttu-id="fd477-118"><dt>videotitlesetmenu</dt></span><span class="sxs-lookup"><span data-stu-id="fd477-118"><dt>videoTitleSetMenu</dt></span></span> </dl> | <span data-ttu-id="fd477-119">Anzeigen von Menüs für den aktuellen Titel Satz.</span><span class="sxs-lookup"><span data-stu-id="fd477-119">Displaying menus for the current title set.</span></span> <span data-ttu-id="fd477-120">Wird auch als titlemenu für Windows-Media Player bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fd477-120">Also known as titleMenu for Windows Media Player.</span></span> <span data-ttu-id="fd477-121">Wird üblicherweise als Stamm Menü bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fd477-121">Commonly called the root menu.</span></span><br/>          |
| <dl> <span data-ttu-id="fd477-122"><dt>title</dt></span><span class="sxs-lookup"><span data-stu-id="fd477-122"><dt>title</dt></span></span> </dl>             | <span data-ttu-id="fd477-123">Normalerweise zeigt den aktuellen Titel an.</span><span class="sxs-lookup"><span data-stu-id="fd477-123">Usually, displaying the current title.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="fd477-124"><dt>stop</dt></span><span class="sxs-lookup"><span data-stu-id="fd477-124"><dt>stop</dt></span></span> </dl>              | <span data-ttu-id="fd477-125">Der DVD-Navigator befindet sich in der DVD-stoppdomäne.</span><span class="sxs-lookup"><span data-stu-id="fd477-125">The DVD Navigator is in the DVD Stop domain.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="fd477-126"><dt>definiert</dt></span><span class="sxs-lookup"><span data-stu-id="fd477-126"><dt>undefined</dt></span></span> </dl>         | <span data-ttu-id="fd477-127">Windows Media Player befindet sich nicht in einer DVD-Domäne.</span><span class="sxs-lookup"><span data-stu-id="fd477-127">Windows Media Player is not in any DVD domain.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="fd477-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd477-128">Remarks</span></span>

<span data-ttu-id="fd477-129">Jede DVD wird unterschiedlich verfasst.</span><span class="sxs-lookup"><span data-stu-id="fd477-129">Every DVD is authored differently.</span></span> <span data-ttu-id="fd477-130">Einige DVDs enthalten nicht die Domänen FirstPlay, videomanagermenu oder videotitlesetmenu.</span><span class="sxs-lookup"><span data-stu-id="fd477-130">Some DVDs do not contain the firstPlay, videoManagerMenu, or videoTitleSetMenu domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd477-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd477-131">Requirements</span></span>



| <span data-ttu-id="fd477-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd477-132">Requirement</span></span> | <span data-ttu-id="fd477-133">Wert</span><span class="sxs-lookup"><span data-stu-id="fd477-133">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd477-134">Version</span><span class="sxs-lookup"><span data-stu-id="fd477-134">Version</span></span><br/>   | <span data-ttu-id="fd477-135">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="fd477-135">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fd477-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="fd477-136">Namespace</span></span><br/> | <span data-ttu-id="fd477-137">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fd477-137">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fd477-138">Assembly</span><span class="sxs-lookup"><span data-stu-id="fd477-138">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fd477-139"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fd477-139"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd477-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd477-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd477-141">**Iwmpdvd-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="fd477-141">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





