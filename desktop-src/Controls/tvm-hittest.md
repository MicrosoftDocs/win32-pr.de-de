---
title: TVM_HITTEST Meldung (kommstrg. h)
description: Bestimmt den Speicherort des angegebenen Punkts relativ zum Client Bereich eines Strukturansicht-Steuer Elements. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ HitTest-Makros senden.
ms.assetid: 18ea3737-f429-4c10-9133-3b5729aa36fa
keywords:
- Windows-Steuerelemente für TVM_HITTEST Meldung
topic_type:
- apiref
api_name:
- TVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b91a11892a2bb904d2cd7d82b5b08cea18331b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040348"
---
# <a name="tvm_hittest-message"></a><span data-ttu-id="ca41e-105">TVM- \_ HitTest-Meldung</span><span class="sxs-lookup"><span data-stu-id="ca41e-105">TVM\_HITTEST message</span></span>

<span data-ttu-id="ca41e-106">Bestimmt den Speicherort des angegebenen Punkts relativ zum Client Bereich eines Strukturansicht-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="ca41e-106">Determines the location of the specified point relative to the client area of a tree-view control.</span></span> <span data-ttu-id="ca41e-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="ca41e-107">You can send this message explicitly or by using the [**TreeView\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ca41e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca41e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca41e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca41e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ca41e-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ca41e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ca41e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca41e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca41e-112">Zeiger auf eine [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ca41e-112">Pointer to a [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) structure.</span></span> <span data-ttu-id="ca41e-113">Wenn die Nachricht gesendet wird, gibt der **PT** -Member die Koordinaten des zu testenden Punkts an.</span><span class="sxs-lookup"><span data-stu-id="ca41e-113">When the message is sent, the **pt** member specifies the coordinates of the point to test.</span></span> <span data-ttu-id="ca41e-114">Wenn die Meldung zurückgegeben wird, ist das **Hitem** -Element das Handle für das Element am angegebenen Punkt oder **null** , wenn kein Element den Punkt einnimmt.</span><span class="sxs-lookup"><span data-stu-id="ca41e-114">When the message returns, the **hItem** member is the handle to the item at the specified point or **NULL** if no item occupies the point.</span></span> <span data-ttu-id="ca41e-115">Wenn die Nachricht zurückgegeben wird, ist der **Flags** -Member außerdem ein Treffer Testwert, der die Position des angegebenen Punkts angibt.</span><span class="sxs-lookup"><span data-stu-id="ca41e-115">Also, when the message returns, the **flags** member is a hit test value that indicates the location of the specified point.</span></span> <span data-ttu-id="ca41e-116">Eine Liste der Treffer Test Werte finden Sie in der Beschreibung der **TVHITTESTINFO** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ca41e-116">For a list of hit test values, see the description of the **TVHITTESTINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca41e-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca41e-117">Return value</span></span>

<span data-ttu-id="ca41e-118">Gibt das Handle für das Struktur Ansichts Element zurück, das den angegebenen Punkt einnimmt, oder **null** , wenn kein Element den Punkt einnimmt.</span><span class="sxs-lookup"><span data-stu-id="ca41e-118">Returns the handle to the tree-view item that occupies the specified point, or **NULL** if no item occupies the point.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca41e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca41e-119">Requirements</span></span>



| <span data-ttu-id="ca41e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca41e-120">Requirement</span></span> | <span data-ttu-id="ca41e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ca41e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca41e-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca41e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ca41e-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca41e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca41e-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca41e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ca41e-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca41e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca41e-126">Header</span><span class="sxs-lookup"><span data-stu-id="ca41e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca41e-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca41e-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





