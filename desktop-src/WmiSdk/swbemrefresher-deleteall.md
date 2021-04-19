---
description: Die Methode "Swap. DeleteAll" entfernt alle Elemente aus der Auflistung im Objekt "Swap-Aktualisierungs Programm". Das Swap-Aktualisierungs Objekt.
ms.assetid: c6e462d3-52b3-40c0-9a9c-fa268415a5f0
ms.tgt_platform: multiple
title: Taubemaktusher. DeleteAll-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ddeb1c5fc8e7fb1f9c5682a2da0d9a1d6f53ba5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355101"
---
# <a name="swbemrefresherdeleteall-method"></a><span data-ttu-id="254ca-103">Taubemaktusher. DeleteAll-Methode</span><span class="sxs-lookup"><span data-stu-id="254ca-103">SWbemRefresher.DeleteAll method</span></span>

<span data-ttu-id="254ca-104">Die Methode " **Swap. DeleteAll** " entfernt alle Elemente aus der Auflistung im Objekt " [**Swap**](swbemrefresher.md) -Aktualisierungs Programm".</span><span class="sxs-lookup"><span data-stu-id="254ca-104">The **SWbemRefresher.DeleteAll** method removes all the items from the collection in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="254ca-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="254ca-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="254ca-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="254ca-106">Syntax</span></span>


```VB
SWbemRefresher.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="254ca-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="254ca-107">Parameters</span></span>

<span data-ttu-id="254ca-108">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="254ca-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="254ca-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="254ca-109">Return value</span></span>

<span data-ttu-id="254ca-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="254ca-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="254ca-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="254ca-111">Remarks</span></span>

<span data-ttu-id="254ca-112">[**Die Aktualisierungs Eigenschaft für**](swbemrefreshableitem-refresher.md) das zugehörige " [**Swap**](swbemrefreshableitem.md) "-Element für jedes entfernte Element ist auf **null** festgelegt, was darauf hinweist, dass es kein übergeordnetes Aktualisierungs Programm mehr aufweist.</span><span class="sxs-lookup"><span data-stu-id="254ca-112">The corresponding [**SWbemRefreshableItem**](swbemrefreshableitem.md) for each removed item has its [**Refresher**](swbemrefreshableitem-refresher.md) property set to **NULL**, which indicates that it no longer has a parent refresher.</span></span>

## <a name="requirements"></a><span data-ttu-id="254ca-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="254ca-113">Requirements</span></span>



| <span data-ttu-id="254ca-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="254ca-114">Requirement</span></span> | <span data-ttu-id="254ca-115">Wert</span><span class="sxs-lookup"><span data-stu-id="254ca-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="254ca-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="254ca-116">Minimum supported client</span></span><br/> | <span data-ttu-id="254ca-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="254ca-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="254ca-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="254ca-118">Minimum supported server</span></span><br/> | <span data-ttu-id="254ca-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="254ca-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="254ca-120">Header</span><span class="sxs-lookup"><span data-stu-id="254ca-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="254ca-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="254ca-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="254ca-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="254ca-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="254ca-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="254ca-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="254ca-124">DLL</span><span class="sxs-lookup"><span data-stu-id="254ca-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="254ca-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="254ca-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="254ca-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="254ca-126">CLSID</span></span><br/>                    | <span data-ttu-id="254ca-127">CLSID- \_ Austauschprogramm</span><span class="sxs-lookup"><span data-stu-id="254ca-127">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="254ca-128">IID</span><span class="sxs-lookup"><span data-stu-id="254ca-128">IID</span></span><br/>                      | <span data-ttu-id="254ca-129">IID \_ iswbemfreshsher</span><span class="sxs-lookup"><span data-stu-id="254ca-129">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="254ca-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="254ca-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="254ca-131">**Swap-Aktualisierungs Programm**</span><span class="sxs-lookup"><span data-stu-id="254ca-131">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




