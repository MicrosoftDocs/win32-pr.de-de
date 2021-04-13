---
title: LVM_DELETEALLITEMS Meldung (kommstrg. h)
description: Entfernt alle Elemente aus einem Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des ListView \_ DeleteAllItems-Makros senden.
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- Windows-Steuerelemente für LVM_DELETEALLITEMS Meldung
topic_type:
- apiref
api_name:
- LVM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e92344e3cccf7578b8953206a9550022f6c6095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475201"
---
# <a name="lvm_deleteallitems-message"></a><span data-ttu-id="7629b-105">LVM \_ DeleteAllItems-Meldung</span><span class="sxs-lookup"><span data-stu-id="7629b-105">LVM\_DELETEALLITEMS message</span></span>

<span data-ttu-id="7629b-106">Entfernt alle Elemente aus einem Listenansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="7629b-106">Removes all items from a list-view control.</span></span> <span data-ttu-id="7629b-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="7629b-107">You can send this message explicitly or by using the [**ListView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7629b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7629b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7629b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7629b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7629b-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="7629b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7629b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7629b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7629b-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="7629b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7629b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7629b-113">Return value</span></span>

<span data-ttu-id="7629b-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="7629b-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7629b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7629b-115">Remarks</span></span>

<span data-ttu-id="7629b-116">Wenn ein Listenansicht-Steuerelement die **LVM- \_ DeleteAllItems** -Nachricht empfängt, sendet es den [**LVN \_ DeleteAllItems**](lvn-deleteallitems.md) -Benachrichtigungs Code an das übergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="7629b-116">When a list-view control receives the **LVM\_DELETEALLITEMS** message, it sends the [**LVN\_DELETEALLITEMS**](lvn-deleteallitems.md) notification code to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="7629b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7629b-117">Requirements</span></span>



| <span data-ttu-id="7629b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7629b-118">Requirement</span></span> | <span data-ttu-id="7629b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7629b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7629b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7629b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7629b-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7629b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7629b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7629b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7629b-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7629b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7629b-124">Header</span><span class="sxs-lookup"><span data-stu-id="7629b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7629b-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="7629b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





