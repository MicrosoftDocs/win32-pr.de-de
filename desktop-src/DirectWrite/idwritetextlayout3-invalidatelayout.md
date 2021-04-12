---
title: IDWriteTextLayout3 invalidatelayout-Methode
description: Macht das Layout ungültig und erzwingt, dass das Layout neu gemessen wird, bevor die Metriken oder Zeichnungsfunktionen aufgerufen werden. Dies ist hilfreich, wenn sich die Position einer Schriftart ändert und das Layout neu gezeichnet werden soll, oder wenn die Größe eines Clients idschreiteinlineobject-Änderungen implementiert hat.
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
keywords:
- Invalidatelayout-Methode direkt schreiben
- Invalidatelayout-Methode Direct Write, IDWriteTextLayout3-Schnittstelle
- IDWriteTextLayout3 Interface Direct Write, invalidatelayout-Methode
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.InvalidateLayout
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5df97d4590f62f586a570d52428b6560a7d88df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104403"
---
# <a name="idwritetextlayout3invalidatelayout-method"></a><span data-ttu-id="cc9c6-107">IDWriteTextLayout3:: invalidatelayout-Methode</span><span class="sxs-lookup"><span data-stu-id="cc9c6-107">IDWriteTextLayout3::InvalidateLayout method</span></span>

<span data-ttu-id="cc9c6-108">Macht das Layout ungültig und erzwingt, dass das Layout neu gemessen wird, bevor die Metriken oder Zeichnungsfunktionen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cc9c6-108">Invalidates the layout, forcing layout to remeasure before calling the metrics or drawing functions.</span></span> <span data-ttu-id="cc9c6-109">Dies ist hilfreich, wenn sich die Position einer Schriftart ändert und das Layout neu gezeichnet werden soll, oder wenn die Größe eines Clients idschreiteinlineobject-Änderungen implementiert hat.</span><span class="sxs-lookup"><span data-stu-id="cc9c6-109">This is useful if the locality of a font changes, and layout should be redrawn, or if the size of a client implemented IDWriteInlineObject changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc9c6-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc9c6-110">Syntax</span></span>


```C++
HRESULT InvalidateLayout();
```



## <a name="parameters"></a><span data-ttu-id="cc9c6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc9c6-111">Parameters</span></span>

<span data-ttu-id="cc9c6-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cc9c6-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cc9c6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc9c6-113">Return value</span></span>

<span data-ttu-id="cc9c6-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="cc9c6-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc9c6-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cc9c6-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc9c6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc9c6-116">Requirements</span></span>



| <span data-ttu-id="cc9c6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc9c6-117">Requirement</span></span> | <span data-ttu-id="cc9c6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cc9c6-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc9c6-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc9c6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cc9c6-120">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="cc9c6-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cc9c6-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc9c6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cc9c6-122">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc9c6-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cc9c6-123">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="cc9c6-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="cc9c6-124">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="cc9c6-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="cc9c6-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cc9c6-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="cc9c6-126"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc9c6-126"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cc9c6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="cc9c6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc9c6-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc9c6-128"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cc9c6-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc9c6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc9c6-130">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="cc9c6-130">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





