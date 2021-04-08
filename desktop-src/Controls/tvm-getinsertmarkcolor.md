---
title: TVM_GETINSERTMARKCOLOR Meldung (kommstrg. h)
description: Ruft die Farbe ab, die verwendet wird, um die Einfügemarke für die Strukturansicht zu zeichnen. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ getinsertmarkcolor-Makros senden.
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- Windows-Steuerelemente für TVM_GETINSERTMARKCOLOR Meldung
topic_type:
- apiref
api_name:
- TVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61416a428fed88ece8f50ca640dd9a05ec131614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957095"
---
# <a name="tvm_getinsertmarkcolor-message"></a><span data-ttu-id="df8b0-105">TVM \_ getinsertmarkcolor-Meldung</span><span class="sxs-lookup"><span data-stu-id="df8b0-105">TVM\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="df8b0-106">Ruft die Farbe ab, die verwendet wird, um die Einfügemarke für die Strukturansicht zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="df8b0-106">Retrieves the color used to draw the insertion mark for the tree view.</span></span> <span data-ttu-id="df8b0-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ getinsertmarkcolor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="df8b0-107">You can send this message explicitly or by using the [**TreeView\_GetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="df8b0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="df8b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df8b0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df8b0-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="df8b0-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="df8b0-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="df8b0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df8b0-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="df8b0-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="df8b0-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df8b0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df8b0-113">Return value</span></span>

<span data-ttu-id="df8b0-114">Gibt einen [**COLORREF**](/windows/desktop/gdi/colorref) -Wert zurück, der die Farbe der aktuellen Einfügemarke enthält.</span><span class="sxs-lookup"><span data-stu-id="df8b0-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that contains the current insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="df8b0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df8b0-115">Requirements</span></span>



| <span data-ttu-id="df8b0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df8b0-116">Requirement</span></span> | <span data-ttu-id="df8b0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="df8b0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df8b0-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df8b0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="df8b0-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df8b0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="df8b0-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df8b0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="df8b0-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df8b0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="df8b0-122">Header</span><span class="sxs-lookup"><span data-stu-id="df8b0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="df8b0-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="df8b0-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df8b0-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df8b0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df8b0-125">**TVM-Wert für "". \_**</span><span class="sxs-lookup"><span data-stu-id="df8b0-125">**TVM\_SETINSERTMARKCOLOR**</span></span>](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

