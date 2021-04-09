---
title: LM_GETITEM Meldung (kommstrg. h)
description: Ruft die Zustände und Attribute eines Elements ab.
ms.assetid: 75381f28-04d7-4a5c-bc0e-4cc74a06553f
keywords:
- Windows-Steuerelemente für LM_GETITEM Meldung
topic_type:
- apiref
api_name:
- LM_GETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb0e05f896df00f3762c53e6f5f62119cb3645f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102919"
---
# <a name="lm_getitem-message"></a><span data-ttu-id="d2642-104">LM- \_ GetItem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d2642-104">LM\_GETITEM message</span></span>

<span data-ttu-id="d2642-105">Ruft die Zustände und Attribute eines Elements ab.</span><span class="sxs-lookup"><span data-stu-id="d2642-105">Retrieves the states and attributes of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2642-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2642-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2642-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2642-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d2642-108">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="d2642-108">Must be **NULL**.</span></span> </dd> <dt>

<span data-ttu-id="d2642-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2642-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d2642-110">Ein Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LItem</a> -Struktur, die mit Informationen über das Element aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2642-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LITEM</a> structure to be filled with information about the item.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2642-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2642-111">Return value</span></span>

<span data-ttu-id="d2642-112">Gibt " **true** " zurück, wenn die Nachricht erfolgreich die angegebenen Werte und Attribute erhält.</span><span class="sxs-lookup"><span data-stu-id="d2642-112">Returns **TRUE** if the message succeeds in getting the values and attributes specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2642-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2642-113">Remarks</span></span>

<span data-ttu-id="d2642-114">Bei der **LM- \_ GetItem** -Nachricht kann nur über den numerischen Index auf Links zugegriffen werden, die im **iLink** -Member von [**LItem**](/windows/win32/api/commctrl/ns-commctrl-litem)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d2642-114">With the **LM\_GETITEM** message, links can only be accessed through the numeric index returned in the **iLink** member of [**LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem).</span></span> <span data-ttu-id="d2642-115">Der Zugriff auf den Link über den in **szid** zurückgegebenen ID-Namen wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2642-115">Accessing the link through the ID name returned in **szID** is not supported.</span></span>

> [!Note]  
> <span data-ttu-id="d2642-116">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="d2642-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d2642-117">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d2642-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d2642-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2642-118">Requirements</span></span>



| <span data-ttu-id="d2642-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2642-119">Requirement</span></span> | <span data-ttu-id="d2642-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d2642-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2642-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2642-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d2642-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2642-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2642-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2642-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d2642-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2642-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2642-125">Header</span><span class="sxs-lookup"><span data-stu-id="d2642-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2642-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2642-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





