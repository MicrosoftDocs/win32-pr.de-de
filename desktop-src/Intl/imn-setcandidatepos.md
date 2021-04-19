---
description: Benachrichtigt eine Anwendung, wenn die Verarbeitung der Kandidaten abgeschlossen ist und der IME im Begriff ist, das Kandidaten Fenster zu verschieben. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Benachrichtigungs Meldung mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: 64252d88-130b-44c3-854a-78b01def7a13
title: IMN_SETCANDIDATEPOS Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03171a76ce94572d2425f8e75f1cbe45b7efe4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353504"
---
# <a name="imn_setcandidatepos-notification-code"></a><span data-ttu-id="11ee8-104">IMN \_ setcandidatepos-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="11ee8-104">IMN\_SETCANDIDATEPOS notification code</span></span>

<span data-ttu-id="11ee8-105">Benachrichtigt eine Anwendung, wenn die Verarbeitung der Kandidaten abgeschlossen ist und der IME im Begriff ist, das Kandidaten Fenster zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="11ee8-105">Notifies an application when candidate processing has finished and the IME is about to move the candidate window.</span></span> <span data-ttu-id="11ee8-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Benachrichtigungs**](wm-ime-notify.md) Meldung mit den Parametereinstellungen, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="11ee8-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="11ee8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="11ee8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11ee8-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="11ee8-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="11ee8-109">Legen Sie auf IMN \_ setcandidatepos fest.</span><span class="sxs-lookup"><span data-stu-id="11ee8-109">Set to IMN\_SETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="11ee8-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="11ee8-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="11ee8-111">Flag der Kandidatenliste.</span><span class="sxs-lookup"><span data-stu-id="11ee8-111">Candidate list flag.</span></span> <span data-ttu-id="11ee8-112">Jedes Bit entspricht einer Kandidatenliste: Bit 0 bis zur ersten Liste, Bit 1 bis zum zweiten usw.</span><span class="sxs-lookup"><span data-stu-id="11ee8-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="11ee8-113">Wenn ein angegebenes Bit 1 ist, wird das entsprechende Kandidaten Fenster verschoben.</span><span class="sxs-lookup"><span data-stu-id="11ee8-113">If a specified bit is 1, the corresponding candidate window is about to be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11ee8-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11ee8-114">Return Value</span></span>

<span data-ttu-id="11ee8-115">Dieser Befehl weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="11ee8-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="11ee8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11ee8-116">Remarks</span></span>

<span data-ttu-id="11ee8-117">Eine Anwendung sollte diesen Befehl verarbeiten, wenn Sie das Kandidaten Fenster selbst anzeigt.</span><span class="sxs-lookup"><span data-stu-id="11ee8-117">An application should process this command if it displays the candidate window itself.</span></span>

<span data-ttu-id="11ee8-118">Das Fenster IME verschiebt das Kandidaten Fenster, wenn es diesen Befehl verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="11ee8-118">The IME window moves the candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="11ee8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11ee8-119">Requirements</span></span>



| <span data-ttu-id="11ee8-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11ee8-120">Requirement</span></span> | <span data-ttu-id="11ee8-121">Wert</span><span class="sxs-lookup"><span data-stu-id="11ee8-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11ee8-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11ee8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="11ee8-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11ee8-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="11ee8-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11ee8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="11ee8-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11ee8-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="11ee8-126">Header</span><span class="sxs-lookup"><span data-stu-id="11ee8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="11ee8-127"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11ee8-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11ee8-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11ee8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11ee8-129">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="11ee8-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="11ee8-130">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="11ee8-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="11ee8-131">**WM- \_ IME \_ Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="11ee8-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




