---
title: LVM_GETCALLBACKMASK Meldung (kommstrg. h)
description: Ruft die Rückruf Maske für ein Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetCallbackMask-Makros senden.
ms.assetid: fb05593d-14b9-4e53-acb3-d5ac61e517ec
keywords:
- Windows-Steuerelemente für LVM_GETCALLBACKMASK Meldung
topic_type:
- apiref
api_name:
- LVM_GETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68438b748f5260bb7cc6e43702442aa4cbe3a84e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475177"
---
# <a name="lvm_getcallbackmask-message"></a><span data-ttu-id="13565-105">LVM \_ GetCallbackMask-Meldung</span><span class="sxs-lookup"><span data-stu-id="13565-105">LVM\_GETCALLBACKMASK message</span></span>

<span data-ttu-id="13565-106">Ruft die Rückruf Maske für ein Listenansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="13565-106">Gets the callback mask for a list-view control.</span></span> <span data-ttu-id="13565-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="13565-107">You can send this message explicitly or by using the [**ListView\_GetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="13565-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="13565-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13565-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="13565-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="13565-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="13565-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="13565-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13565-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="13565-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="13565-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13565-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13565-113">Return value</span></span>

<span data-ttu-id="13565-114">Gibt die Rückruf Maske zurück.</span><span class="sxs-lookup"><span data-stu-id="13565-114">Returns the callback mask.</span></span>

## <a name="requirements"></a><span data-ttu-id="13565-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13565-115">Requirements</span></span>



| <span data-ttu-id="13565-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13565-116">Requirement</span></span> | <span data-ttu-id="13565-117">Wert</span><span class="sxs-lookup"><span data-stu-id="13565-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="13565-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13565-118">Minimum supported client</span></span><br/> | <span data-ttu-id="13565-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13565-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="13565-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13565-120">Minimum supported server</span></span><br/> | <span data-ttu-id="13565-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13565-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="13565-122">Header</span><span class="sxs-lookup"><span data-stu-id="13565-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="13565-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="13565-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





