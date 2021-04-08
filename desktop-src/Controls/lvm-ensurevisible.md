---
title: LVM_ENSUREVISIBLE Meldung (kommstrg. h)
description: Stellt sicher, dass ein Listen Ansichts Element entweder vollständig oder teilweise sichtbar ist, und führt ggf. einen Bildlauf im Listenansicht-Steuerelement durch Sie können diese Nachricht explizit oder mithilfe des ListView \_ EnsureVisible-Makros senden.
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- Windows-Steuerelemente für LVM_ENSUREVISIBLE Meldung
topic_type:
- apiref
api_name:
- LVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0ff4009399988f20f3e162114f91e4cff02820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949427"
---
# <a name="lvm_ensurevisible-message"></a><span data-ttu-id="6488a-105">LVM \_ EnsureVisible-Meldung</span><span class="sxs-lookup"><span data-stu-id="6488a-105">LVM\_ENSUREVISIBLE message</span></span>

<span data-ttu-id="6488a-106">Stellt sicher, dass ein Listen Ansichts Element entweder vollständig oder teilweise sichtbar ist, und führt ggf. einen Bildlauf im Listenansicht-Steuerelement durch</span><span class="sxs-lookup"><span data-stu-id="6488a-106">Ensures that a list-view item is either entirely or partially visible, scrolling the list-view control if necessary.</span></span> <span data-ttu-id="6488a-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="6488a-107">You can send this message explicitly or by using the [**ListView\_EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6488a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6488a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6488a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6488a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6488a-110">Der Index des Listen Ansichts Elements.</span><span class="sxs-lookup"><span data-stu-id="6488a-110">The index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="6488a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6488a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6488a-112">Ein-Wert, der angibt, ob das Element vollständig sichtbar sein muss.</span><span class="sxs-lookup"><span data-stu-id="6488a-112">A value specifying whether the item must be entirely visible.</span></span> <span data-ttu-id="6488a-113">Wenn dieser Parameter **true** ist, wird kein Bildlauf durchgeführt, wenn das Element mindestens teilweise sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="6488a-113">If this parameter is **TRUE**, no scrolling occurs if the item is at least partially visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6488a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6488a-114">Return value</span></span>

<span data-ttu-id="6488a-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="6488a-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6488a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6488a-116">Remarks</span></span>

<span data-ttu-id="6488a-117">Die Meldung schlägt fehl, wenn der Fenster Stil [**LVS \_ NoScroll**](list-view-window-styles.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="6488a-117">The message fails if the window style includes [**LVS\_NOSCROLL**](list-view-window-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6488a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6488a-118">Requirements</span></span>



| <span data-ttu-id="6488a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6488a-119">Requirement</span></span> | <span data-ttu-id="6488a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6488a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6488a-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6488a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6488a-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6488a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6488a-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6488a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6488a-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6488a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6488a-125">Header</span><span class="sxs-lookup"><span data-stu-id="6488a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6488a-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6488a-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





