---
title: DVD. Domäne
description: Die Domänen Eigenschaft ruft die aktuelle Domäne der DVD ab.
ms.assetid: 74f4a6a3-8518-48c7-b023-f0255a3a62fd
keywords:
- DVD. Domänen-Windows-Media Player
topic_type:
- apiref
api_name:
- DVD.domain
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4a2af92abe533fed7a13e48cb7c0724223bbc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340597"
---
# <a name="dvddomain"></a><span data-ttu-id="3a291-104">DVD. Domäne</span><span class="sxs-lookup"><span data-stu-id="3a291-104">DVD.domain</span></span>

<span data-ttu-id="3a291-105">Die **Domänen** Eigenschaft ruft die aktuelle Domäne der DVD ab.</span><span class="sxs-lookup"><span data-stu-id="3a291-105">The **domain** property retrieves the current domain of the DVD.</span></span>

``` syntax
player.dvd.domain
      
```

## <a name="possible-values"></a><span data-ttu-id="3a291-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="3a291-106">Possible Values</span></span>

<span data-ttu-id="3a291-107">Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge** , die einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="3a291-107">This property is a read-only **String** containing one of the following values.</span></span>



| <span data-ttu-id="3a291-108">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3a291-108">String</span></span>            | <span data-ttu-id="3a291-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a291-109">Description</span></span>                                                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a291-110">FirstPlay</span><span class="sxs-lookup"><span data-stu-id="3a291-110">firstPlay</span></span>         | <span data-ttu-id="3a291-111">Die Standard Initialisierung einer DVD-CD wird durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a291-111">Performing default initialization of a DVD disc.</span></span>                                                                                      |
| <span data-ttu-id="3a291-112">videomanagermenu</span><span class="sxs-lookup"><span data-stu-id="3a291-112">videoManagerMenu</span></span>  | <span data-ttu-id="3a291-113">Anzeigen von Menüs für die gesamte Festplatte. Wird auch als "topmenu" für Windows-Media Player bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3a291-113">Displaying menus for the entire disc. Also known as topMenu for Windows Media Player.</span></span> <span data-ttu-id="3a291-114">Wird üblicherweise als Titelmenü oder im oberen Menü bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3a291-114">Commonly called the title menu or the top menu.</span></span> |
| <span data-ttu-id="3a291-115">videotitlesetmenu</span><span class="sxs-lookup"><span data-stu-id="3a291-115">videoTitleSetMenu</span></span> | <span data-ttu-id="3a291-116">Anzeigen von Menüs für den aktuellen Titel Satz.</span><span class="sxs-lookup"><span data-stu-id="3a291-116">Displaying menus for current title set.</span></span> <span data-ttu-id="3a291-117">Wird auch als titlemenu für Windows-Media Player bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3a291-117">Also known as titleMenu for Windows Media Player.</span></span> <span data-ttu-id="3a291-118">Wird üblicherweise als Stamm Menü bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3a291-118">Commonly called the root menu.</span></span>              |
| <span data-ttu-id="3a291-119">title</span><span class="sxs-lookup"><span data-stu-id="3a291-119">title</span></span>             | <span data-ttu-id="3a291-120">Normalerweise wird der aktuelle Titel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3a291-120">Usually displaying the current title.</span></span>                                                                                                 |
| <span data-ttu-id="3a291-121">stop</span><span class="sxs-lookup"><span data-stu-id="3a291-121">stop</span></span>              | <span data-ttu-id="3a291-122">Der DVD-Navigator befindet sich in der DVD-stoppdomäne.</span><span class="sxs-lookup"><span data-stu-id="3a291-122">The DVD Navigator is in the DVD Stop domain.</span></span>                                                                                          |
| <span data-ttu-id="3a291-123">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="3a291-123">undefined</span></span>         | <span data-ttu-id="3a291-124">Der Player befindet sich nicht in einer DVD-Domäne.</span><span class="sxs-lookup"><span data-stu-id="3a291-124">Player is not in any DVD domain.</span></span>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="3a291-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a291-125">Remarks</span></span>

<span data-ttu-id="3a291-126">Jede DVD wird unterschiedlich verfasst.</span><span class="sxs-lookup"><span data-stu-id="3a291-126">Every DVD is authored differently.</span></span> <span data-ttu-id="3a291-127">Einige DVDs enthalten nicht die Domänen FirstPlay, videomanagermenu oder videotitlesetmenu.</span><span class="sxs-lookup"><span data-stu-id="3a291-127">Some DVDs do not contain the firstPlay, videoManagerMenu, or videoTitleSetMenu domains.</span></span>

<span data-ttu-id="3a291-128">**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer eine leere Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="3a291-128">**Windows Media Player 10 Mobile:** This property always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a291-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a291-129">Requirements</span></span>



| <span data-ttu-id="3a291-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a291-130">Requirement</span></span> | <span data-ttu-id="3a291-131">Wert</span><span class="sxs-lookup"><span data-stu-id="3a291-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a291-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a291-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3a291-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a291-133">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a291-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a291-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3a291-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a291-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3a291-136">Version</span><span class="sxs-lookup"><span data-stu-id="3a291-136">Version</span></span><br/>                  | <span data-ttu-id="3a291-137">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="3a291-137">Windows Media Player for Windows XP or later</span></span><br/>                            |
| <span data-ttu-id="3a291-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3a291-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a291-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a291-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a291-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a291-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a291-141">**DVD-Objekt**</span><span class="sxs-lookup"><span data-stu-id="3a291-141">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





