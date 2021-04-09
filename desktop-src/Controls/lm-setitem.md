---
title: LM_SETITEM Meldung (kommstrg. h)
description: Legt die Zustände und Attribute eines Elements fest.
ms.assetid: 02a68a31-2541-480e-b768-449d40e5e9e0
keywords:
- Windows-Steuerelemente für LM_SETITEM Meldung
topic_type:
- apiref
api_name:
- LM_SETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11888a76b11ccec7e8e659ca3a33bb23a71667ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102915"
---
# <a name="lm_setitem-message"></a><span data-ttu-id="432d3-104">LM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="432d3-104">LM\_SETITEM message</span></span>

<span data-ttu-id="432d3-105">Legt die Zustände und Attribute eines Elements fest.</span><span class="sxs-lookup"><span data-stu-id="432d3-105">Sets the states and attributes of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="432d3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="432d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="432d3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="432d3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="432d3-108">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="432d3-108">Must be **NULL**.</span></span> </dd> <dt>

<span data-ttu-id="432d3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="432d3-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="432d3-110">Ein Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LItem</a> -Struktur, die die für den Link gewünschten neuen Zustände und Attribute enthält.</span><span class="sxs-lookup"><span data-stu-id="432d3-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LITEM</a> structure containing the new states and attributes desired for the link.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="432d3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="432d3-111">Return value</span></span>

<span data-ttu-id="432d3-112">Gibt **true** zurück, wenn die Nachricht beim Festlegen der angegebenen Werte und Attribute erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="432d3-112">Returns **TRUE** if the message succeeds in setting the values and attributes specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="432d3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="432d3-113">Remarks</span></span>

<span data-ttu-id="432d3-114">Bei der [**LM- \_ GetItem**](lm-getitem.md) -Nachricht kann nur über den numerischen Index auf Links zugegriffen werden, die im **iLink** -Member von [**LItem**](/windows/win32/api/commctrl/ns-commctrl-litem)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="432d3-114">With the [**LM\_GETITEM**](lm-getitem.md) message, links can only be accessed through the numeric index returned in the **iLink** member of [**LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem).</span></span> <span data-ttu-id="432d3-115">Der Zugriff auf den Link über den in **szid** zurückgegebenen ID-Namen wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="432d3-115">Accessing the link through the ID name returned in **szID** is not supported.</span></span>

> [!Note]  
> <span data-ttu-id="432d3-116">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comctl32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="432d3-116">To use this message, you must provide a manifest specifying Comctl32.dll version 6.0.</span></span> <span data-ttu-id="432d3-117">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="432d3-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="432d3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="432d3-118">Requirements</span></span>



| <span data-ttu-id="432d3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="432d3-119">Requirement</span></span> | <span data-ttu-id="432d3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="432d3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="432d3-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="432d3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="432d3-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="432d3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="432d3-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="432d3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="432d3-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="432d3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="432d3-125">Header</span><span class="sxs-lookup"><span data-stu-id="432d3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="432d3-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="432d3-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





