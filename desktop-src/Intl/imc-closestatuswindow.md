---
description: Weist das IME-Fenster an, das Statusfenster auszublenden. Um diesen Befehl zu senden, verwendet die Anwendung die WM- \_ IME- \_ Steuerungs Meldung mit den unten gezeigten Parametereinstellungen.
ms.assetid: e3da5962-a652-409e-b0ec-eb93671049b4
title: IMC_CLOSESTATUSWINDOW Befehl (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 207f04d53f269318f87ed11038cbd6817d5e607e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869263"
---
# <a name="imc_closestatuswindow-command"></a><span data-ttu-id="c5b61-104">IMC \_ closestatus Window-Befehl</span><span class="sxs-lookup"><span data-stu-id="c5b61-104">IMC\_CLOSESTATUSWINDOW command</span></span>

<span data-ttu-id="c5b61-105">Weist das IME-Fenster an, das Statusfenster auszublenden.</span><span class="sxs-lookup"><span data-stu-id="c5b61-105">Instructs the IME window to hide the status window.</span></span> <span data-ttu-id="c5b61-106">Um diesen Befehl zu senden, verwendet die Anwendung die [**WM- \_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung mit den unten gezeigten Parametereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="c5b61-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_CLOSESTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="c5b61-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5b61-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5b61-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5b61-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="c5b61-109">Legen Sie auf "IMC \_ closestatus Window" fest.</span><span class="sxs-lookup"><span data-stu-id="c5b61-109">Set to IMC\_CLOSESTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="c5b61-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="c5b61-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="c5b61-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5b61-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5b61-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5b61-112">Return Value</span></span>

<span data-ttu-id="c5b61-113">Gibt bei Erfolg 0 zurück oder andernfalls einen Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c5b61-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5b61-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5b61-114">Remarks</span></span>

<span data-ttu-id="c5b61-115">Wenn das Fenster IME-Status bereits ausgeblendet ist, führt dieser Befehl nichts aus.</span><span class="sxs-lookup"><span data-stu-id="c5b61-115">When the IME status window is already hidden, this command does nothing.</span></span> <span data-ttu-id="c5b61-116">Obwohl eine Anwendung diesen Befehl an das IME-Fenster senden kann, erhält die Anwendung nicht den entsprechenden [IMN \_ closestatus Window](imn-closestatuswindow.md) -Befehl.</span><span class="sxs-lookup"><span data-stu-id="c5b61-116">Although an application can send this command to the IME window, the application does not receive the corresponding [IMN\_CLOSESTATUSWINDOW](imn-closestatuswindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5b61-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5b61-117">Requirements</span></span>



| <span data-ttu-id="c5b61-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5b61-118">Requirement</span></span> | <span data-ttu-id="c5b61-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c5b61-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b61-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5b61-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c5b61-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5b61-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c5b61-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5b61-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c5b61-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5b61-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c5b61-124">Header</span><span class="sxs-lookup"><span data-stu-id="c5b61-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5b61-125"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5b61-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5b61-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5b61-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5b61-127">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="c5b61-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="c5b61-128">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="c5b61-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> </dl>

 

 




