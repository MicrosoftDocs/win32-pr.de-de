---
title: TCM_GETCURFOCUS Meldung (kommstrg. h)
description: Gibt den Index des Elements zurück, das in einem Registerkarten-Steuerelement den Fokus besitzt. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ getcurrfocus-Makros senden.
ms.assetid: ae6ee159-c769-41d6-b0bb-2a9ade4c0e71
keywords:
- Windows-Steuerelemente für TCM_GETCURFOCUS Meldung
topic_type:
- apiref
api_name:
- TCM_GETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0d0f3d2bbd4a7cf0ab2a63c5a988f60768eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957040"
---
# <a name="tcm_getcurfocus-message"></a><span data-ttu-id="74b49-105">TCM \_ getcurrfocus-Nachricht</span><span class="sxs-lookup"><span data-stu-id="74b49-105">TCM\_GETCURFOCUS message</span></span>

<span data-ttu-id="74b49-106">Gibt den Index des Elements zurück, das in einem Registerkarten-Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="74b49-106">Returns the index of the item that has the focus in a tab control.</span></span> <span data-ttu-id="74b49-107">Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ getcurrfocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="74b49-107">You can send this message explicitly or by using the [**TabCtrl\_GetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="74b49-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="74b49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74b49-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74b49-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="74b49-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="74b49-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="74b49-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74b49-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="74b49-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="74b49-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74b49-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74b49-113">Return value</span></span>

<span data-ttu-id="74b49-114">Gibt den Index des Registerkarten Elements zurück, das den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="74b49-114">Returns the index of the tab item that has the focus.</span></span>

## <a name="remarks"></a><span data-ttu-id="74b49-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74b49-115">Remarks</span></span>

<span data-ttu-id="74b49-116">Das Element, das den Fokus besitzt, kann sich von dem ausgewählten Element unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="74b49-116">The item that has the focus may be different than the selected item.</span></span>

## <a name="requirements"></a><span data-ttu-id="74b49-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74b49-117">Requirements</span></span>



| <span data-ttu-id="74b49-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74b49-118">Requirement</span></span> | <span data-ttu-id="74b49-119">Wert</span><span class="sxs-lookup"><span data-stu-id="74b49-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74b49-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74b49-120">Minimum supported client</span></span><br/> | <span data-ttu-id="74b49-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74b49-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74b49-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74b49-122">Minimum supported server</span></span><br/> | <span data-ttu-id="74b49-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74b49-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74b49-124">Header</span><span class="sxs-lookup"><span data-stu-id="74b49-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="74b49-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="74b49-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





