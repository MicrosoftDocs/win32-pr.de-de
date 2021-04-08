---
title: LVM_SETHOTCURSOR Meldung (kommstrg. h)
description: Legt den hcursor-Wert fest, den das Listenansicht-Steuerelement verwendet, wenn sich der Zeiger über einem Element befindet, während die Hot-Überwachung aktiviert ist.
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- Windows-Steuerelemente für LVM_SETHOTCURSOR Meldung
topic_type:
- apiref
api_name:
- LVM_SETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e743f74eda3b59f04f6f4793b47d76da3bab881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739945"
---
# <a name="lvm_sethotcursor-message"></a><span data-ttu-id="5d568-104">LVM- \_ messagecursor-Nachricht</span><span class="sxs-lookup"><span data-stu-id="5d568-104">LVM\_SETHOTCURSOR message</span></span>

<span data-ttu-id="5d568-105">Legt den hcursor-Wert fest, den das Listenansicht-Steuerelement verwendet, wenn sich der Zeiger über einem Element befindet, während die Hot-Überwachung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5d568-105">Sets the HCURSOR value that the list-view control uses when the pointer is over an item while hot tracking is enabled.</span></span> <span data-ttu-id="5d568-106">Sie können diese Nachricht explizit senden oder das [**ListView- \_ prätcursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="5d568-106">You can send this message explicitly or use the [**ListView\_SetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) macro.</span></span> <span data-ttu-id="5d568-107">Um zu überprüfen, ob Hot Tracking aktiviert ist, aufrufen Sie [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span><span class="sxs-lookup"><span data-stu-id="5d568-107">To check whether hot tracking is enabled, call [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span>

## <a name="parameters"></a><span data-ttu-id="5d568-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d568-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d568-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d568-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5d568-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="5d568-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5d568-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d568-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d568-112">Handle für den Cursor, der festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d568-112">Handle to the cursor to be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d568-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d568-113">Return value</span></span>

<span data-ttu-id="5d568-114">Gibt einen hcursor-Wert zurück, der der vorherige Hot-Cursor ist.</span><span class="sxs-lookup"><span data-stu-id="5d568-114">Returns an HCURSOR value that is the previous hot cursor.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d568-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d568-115">Remarks</span></span>

<span data-ttu-id="5d568-116">Ein Listenansicht-Steuerelement verwendet die Hot-Tracking-und Hover-Auswahl, wenn der [**LVS \_ Ex \_ trackselect**](extended-list-view-styles.md) -Stil festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5d568-116">A list-view control uses hot tracking and hover selection when the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) style is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d568-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d568-117">Requirements</span></span>



| <span data-ttu-id="5d568-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d568-118">Requirement</span></span> | <span data-ttu-id="5d568-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5d568-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d568-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d568-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5d568-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d568-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5d568-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d568-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5d568-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d568-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d568-124">Header</span><span class="sxs-lookup"><span data-stu-id="5d568-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d568-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d568-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

