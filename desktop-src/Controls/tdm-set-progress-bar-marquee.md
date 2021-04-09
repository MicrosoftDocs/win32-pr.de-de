---
title: TDM_SET_PROGRESS_BAR_MARQUEE Meldung (kommstrg. h)
description: Startet und beendet die Marquee-Anzeige der Statusanzeige in einem Aufgaben Dialogfeld und legt die Geschwindigkeit des Marquee fest.
ms.assetid: df947171-a916-4db9-abe0-57a3bf11037f
keywords:
- Windows-Steuerelemente für TDM_SET_PROGRESS_BAR_MARQUEE Meldung
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_MARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f73d3d4308d2e3f963c015b6e36f385902bea6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040944"
---
# <a name="tdm_set_progress_bar_marquee-message"></a><span data-ttu-id="54f9b-104">TDM \_ Festlegen der Statusanzeige- \_ \_ \_ Marquee-Nachricht</span><span class="sxs-lookup"><span data-stu-id="54f9b-104">TDM\_SET\_PROGRESS\_BAR\_MARQUEE message</span></span>

<span data-ttu-id="54f9b-105">Startet und beendet die Marquee-Anzeige der Statusanzeige in einem Aufgaben Dialogfeld und legt die Geschwindigkeit des Marquee fest.</span><span class="sxs-lookup"><span data-stu-id="54f9b-105">Starts and stops the marquee display of the progress bar in a task dialog, and sets the speed of the marquee.</span></span>

## <a name="parameters"></a><span data-ttu-id="54f9b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54f9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54f9b-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54f9b-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54f9b-108">Ein **boolescher** Wert, der angibt, ob die Marquee-Anzeige ein-oder ausgeschaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="54f9b-108">A **BOOL** that indicates whether to turn the marquee display on or off.</span></span> <span data-ttu-id="54f9b-109">Verwenden Sie **true** , um die Marquee-Anzeige zu aktivieren, oder **false** , um Sie zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="54f9b-109">Use **TRUE** to turn on the marquee display, or **FALSE** to turn it off.</span></span>

</dd> <dt>

<span data-ttu-id="54f9b-110">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54f9b-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54f9b-111">Ein **uint** , der die Zeit in Millisekunden zwischen den Marquee-Animations Aktualisierungen angibt.</span><span class="sxs-lookup"><span data-stu-id="54f9b-111">A **UINT** that specifies the time, in milliseconds, between marquee animation updates.</span></span> <span data-ttu-id="54f9b-112">Wenn dieser Parameter 0 (null) ist, wird die Marquee-Animation alle 30 Millisekunden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="54f9b-112">If this parameter is zero, the marquee animation is updated every 30 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54f9b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54f9b-113">Return value</span></span>

<span data-ttu-id="54f9b-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="54f9b-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="54f9b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54f9b-115">Remarks</span></span>

<span data-ttu-id="54f9b-116">Informationen zum Marquee-Modus finden Sie unter Statusanzeige- [Steuer](progress-bar-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="54f9b-116">For information on marquee mode, see [Progress Bar Control](progress-bar-control.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54f9b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54f9b-117">Requirements</span></span>



| <span data-ttu-id="54f9b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54f9b-118">Requirement</span></span> | <span data-ttu-id="54f9b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="54f9b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54f9b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54f9b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="54f9b-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54f9b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54f9b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54f9b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="54f9b-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54f9b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54f9b-124">Header</span><span class="sxs-lookup"><span data-stu-id="54f9b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="54f9b-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="54f9b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





