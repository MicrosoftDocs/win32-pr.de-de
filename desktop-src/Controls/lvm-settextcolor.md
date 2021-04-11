---
title: LVM_SETTEXTCOLOR Meldung (kommstrg. h)
description: Legt die Textfarbe eines Listenansicht-Steuer Elements fest. Sie können diese Nachricht explizit oder mithilfe des ListView \_ SetTextColor-Makros senden.
ms.assetid: ff90c18b-0cd7-4331-bcd8-61044e891d1f
keywords:
- Windows-Steuerelemente für LVM_SETTEXTCOLOR Meldung
topic_type:
- apiref
api_name:
- LVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b30c965bd523cd5638c894b47fc4785ffbdd09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103355"
---
# <a name="lvm_settextcolor-message"></a><span data-ttu-id="9c327-105">LVM- \_ SetTextColor-Meldung</span><span class="sxs-lookup"><span data-stu-id="9c327-105">LVM\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="9c327-106">Legt die Textfarbe eines Listenansicht-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="9c327-106">Sets the text color of a list-view control.</span></span> <span data-ttu-id="9c327-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="9c327-107">You can send this message explicitly or by using the [**ListView\_SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9c327-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c327-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c327-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c327-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9c327-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9c327-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9c327-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c327-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c327-112">Ein [**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der die neue Textfarbe angibt.</span><span class="sxs-lookup"><span data-stu-id="9c327-112">A [**COLORREF**](/windows/desktop/gdi/colorref) that specifies the new text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c327-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c327-113">Return value</span></span>

<span data-ttu-id="9c327-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="9c327-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c327-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c327-115">Requirements</span></span>



| <span data-ttu-id="9c327-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c327-116">Requirement</span></span> | <span data-ttu-id="9c327-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9c327-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c327-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c327-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9c327-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c327-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c327-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c327-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9c327-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c327-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c327-122">Header</span><span class="sxs-lookup"><span data-stu-id="9c327-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c327-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c327-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

