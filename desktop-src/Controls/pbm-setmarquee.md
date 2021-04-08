---
title: PBM_SETMARQUEE Meldung (kommstrg. h)
description: Legt die Statusanzeige auf den Marquee-Modus fest. Dies bewirkt, dass die Statusanzeige wie ein Marquee verschoben wird.
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- Windows-Steuerelemente für PBM_SETMARQUEE Meldung
topic_type:
- apiref
api_name:
- PBM_SETMARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9229291113f034924cf9ce8112c0e99376d37932
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956811"
---
# <a name="pbm_setmarquee-message"></a><span data-ttu-id="067ff-105">PBM- \_ setmarquee-Nachricht</span><span class="sxs-lookup"><span data-stu-id="067ff-105">PBM\_SETMARQUEE message</span></span>

<span data-ttu-id="067ff-106">Legt die Statusanzeige auf den Marquee-Modus fest.</span><span class="sxs-lookup"><span data-stu-id="067ff-106">Sets the progress bar to marquee mode.</span></span> <span data-ttu-id="067ff-107">Dies bewirkt, dass die Statusanzeige wie ein Marquee verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="067ff-107">This causes the progress bar to move like a marquee.</span></span>

## <a name="parameters"></a><span data-ttu-id="067ff-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="067ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="067ff-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="067ff-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="067ff-110">Gibt an, ob der Marquee-Modus aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="067ff-110">Indicates whether to turn the marquee mode on or off.</span></span>

</dd> <dt>

<span data-ttu-id="067ff-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="067ff-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="067ff-112">Zeit (in Millisekunden) zwischen der Aktualisierung der Marquee-Animation.</span><span class="sxs-lookup"><span data-stu-id="067ff-112">Time, in milliseconds, between marquee animation updates.</span></span> <span data-ttu-id="067ff-113">Wenn dieser Parameter 0 (null) ist, wird die Marquee-Animation alle 30 Millisekunden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="067ff-113">If this parameter is zero, the marquee animation is updated every 30 milliseconds.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="067ff-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="067ff-114">Return value</span></span>

<span data-ttu-id="067ff-115">Gibt immer **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="067ff-115">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="067ff-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="067ff-116">Remarks</span></span>

<span data-ttu-id="067ff-117">Verwenden Sie diese Meldung, wenn Sie den Fortschritt im Hinblick auf den Abschluss nicht kennen, aber angeben möchten, dass der Fortschritt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="067ff-117">Use this message when you do not know the amount of progress toward completion but wish to indicate that progress is being made.</span></span>

<span data-ttu-id="067ff-118">Senden Sie die **PBM- \_ setmarquee** -Nachricht, um die Animation zu starten oder zu unterbinden.</span><span class="sxs-lookup"><span data-stu-id="067ff-118">Send the **PBM\_SETMARQUEE** message to start or stop the animation.</span></span>

> [!Note]  
> <span data-ttu-id="067ff-119">Sie müssen den Steuer Stil des Steuer Elements auf [**PSB- \_ Marquee**](progress-bar-control-styles.md) festlegen, bevor Sie versuchen, die Animation zu starten.</span><span class="sxs-lookup"><span data-stu-id="067ff-119">You must set the control style to [**PBS\_MARQUEE**](progress-bar-control-styles.md) before attempting to start the animation.</span></span>

 

> [!Note]  
> <span data-ttu-id="067ff-120">Diese Meldung erfordert ComCtl32.dll-Version 6,00 oder höher.</span><span class="sxs-lookup"><span data-stu-id="067ff-120">This message requires ComCtl32.dll version 6.00 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="067ff-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="067ff-121">Requirements</span></span>



| <span data-ttu-id="067ff-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="067ff-122">Requirement</span></span> | <span data-ttu-id="067ff-123">Wert</span><span class="sxs-lookup"><span data-stu-id="067ff-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="067ff-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="067ff-124">Minimum supported client</span></span><br/> | <span data-ttu-id="067ff-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="067ff-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="067ff-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="067ff-126">Minimum supported server</span></span><br/> | <span data-ttu-id="067ff-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="067ff-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="067ff-128">Header</span><span class="sxs-lookup"><span data-stu-id="067ff-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="067ff-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="067ff-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





