---
title: PBM_SETSTATE Meldung (kommstrg. h)
description: Legt den Status der Statusanzeige fest.
ms.assetid: 4626f334-db74-4618-8fc7-e6f21c88ca19
keywords:
- Windows-Steuerelemente für PBM_SETSTATE Meldung
topic_type:
- apiref
api_name:
- PBM_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c91e94bcc909957264eff776e56d3580b2c36ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477907"
---
# <a name="pbm_setstate-message"></a><span data-ttu-id="f5f49-104">PBM- \_ SetState-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f5f49-104">PBM\_SETSTATE message</span></span>

<span data-ttu-id="f5f49-105">Legt den Status der Statusanzeige fest.</span><span class="sxs-lookup"><span data-stu-id="f5f49-105">Sets the state of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5f49-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5f49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5f49-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5f49-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5f49-108">Status der Statusanzeige, die festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f5f49-108">State of the progress bar that is being set.</span></span> <span data-ttu-id="f5f49-109">Einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="f5f49-109">One of the following values.</span></span>



| <span data-ttu-id="f5f49-110">Wert</span><span class="sxs-lookup"><span data-stu-id="f5f49-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="f5f49-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f5f49-111">Meaning</span></span>                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <span data-ttu-id="f5f49-112"><dt>**PBST \_ Normal**</dt></span><span class="sxs-lookup"><span data-stu-id="f5f49-112"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="f5f49-113">Läuft.</span><span class="sxs-lookup"><span data-stu-id="f5f49-113">In progress.</span></span><br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <span data-ttu-id="f5f49-114"><dt>**PBST- \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="f5f49-114"><dt>**PBST\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="f5f49-115">Fehler.</span><span class="sxs-lookup"><span data-stu-id="f5f49-115">Error.</span></span><br/>       |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <span data-ttu-id="f5f49-116"><dt>**PBST \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="f5f49-116"><dt>**PBST\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="f5f49-117">Angehalten.</span><span class="sxs-lookup"><span data-stu-id="f5f49-117">Paused.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="f5f49-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5f49-118">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f5f49-119">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f5f49-119">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5f49-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5f49-120">Return value</span></span>

<span data-ttu-id="f5f49-121">Gibt den vorherigen Zustand zurück.</span><span class="sxs-lookup"><span data-stu-id="f5f49-121">Returns the previous state.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5f49-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5f49-122">Requirements</span></span>



| <span data-ttu-id="f5f49-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5f49-123">Requirement</span></span> | <span data-ttu-id="f5f49-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f5f49-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f49-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5f49-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f5f49-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5f49-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5f49-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5f49-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f5f49-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5f49-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5f49-129">Header</span><span class="sxs-lookup"><span data-stu-id="f5f49-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5f49-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5f49-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





