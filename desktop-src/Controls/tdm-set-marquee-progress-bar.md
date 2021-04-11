---
title: TDM_SET_MARQUEE_PROGRESS_BAR Meldung (kommstrg. h)
description: Gibt an, ob die gehostete Statusanzeige eines Aufgaben Dialogfelds im Marquee-Modus angezeigt werden soll.
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- Windows-Steuerelemente für TDM_SET_MARQUEE_PROGRESS_BAR Meldung
topic_type:
- apiref
api_name:
- TDM_SET_MARQUEE_PROGRESS_BAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a9384826b89d07c6564dc511d4909058871ca3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105969"
---
# <a name="tdm_set_marquee_progress_bar-message"></a><span data-ttu-id="bc787-104">TDM \_ Set \_ Marquee \_ - \_ Statusanzeige Meldung</span><span class="sxs-lookup"><span data-stu-id="bc787-104">TDM\_SET\_MARQUEE\_PROGRESS\_BAR message</span></span>

<span data-ttu-id="bc787-105">Gibt an, ob die gehostete Statusanzeige eines Aufgaben Dialogfelds im Marquee-Modus angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc787-105">Indicates whether the hosted progress bar of a task dialog should be displayed in marquee mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="bc787-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc787-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc787-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc787-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc787-108">Ein **boolescher** Wert, der angibt, ob die Statusanzeige im Marquee-Modus angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc787-108">A **BOOL** that indicates whether the progress bar should be shown in marquee mode.</span></span> <span data-ttu-id="bc787-109">Der Wert **true** wechselt im Marquee-Modus, und der Wert **false** schaltet den Marquee-Modus um.</span><span class="sxs-lookup"><span data-stu-id="bc787-109">A value of **TRUE** turns on marquee mode, and a value of **FALSE** turns off marquee mode.</span></span>

</dd> <dt>

<span data-ttu-id="bc787-110">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc787-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc787-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="bc787-111">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc787-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc787-112">Return value</span></span>

<span data-ttu-id="bc787-113">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bc787-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc787-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc787-114">Remarks</span></span>

<span data-ttu-id="bc787-115">Informationen zum Marquee-Modus finden Sie unter Statusanzeige- [Steuer](progress-bar-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="bc787-115">For information on marquee mode, see [Progress Bar Control](progress-bar-control.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc787-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc787-116">Requirements</span></span>



| <span data-ttu-id="bc787-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc787-117">Requirement</span></span> | <span data-ttu-id="bc787-118">Wert</span><span class="sxs-lookup"><span data-stu-id="bc787-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc787-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc787-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bc787-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc787-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bc787-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc787-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bc787-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc787-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bc787-123">Header</span><span class="sxs-lookup"><span data-stu-id="bc787-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc787-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc787-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





