---
description: Benachrichtigt eine Anwendung, wenn ein IME im Begriff ist, das Statusfenster zu erstellen. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Benachrichtigungs Meldung mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: bbd85c72-aa78-4e1d-8a7a-490650b2d782
title: IMN_OPENSTATUSWINDOW Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca33771d1474c2f2ac78551a31545cecc2e513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363504"
---
# <a name="imn_openstatuswindow-notification-code"></a><span data-ttu-id="5cce3-104">Unn \_ openstatus Window-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="5cce3-104">IMN\_OPENSTATUSWINDOW notification code</span></span>

<span data-ttu-id="5cce3-105">Benachrichtigt eine Anwendung, wenn ein IME im Begriff ist, das Statusfenster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5cce3-105">Notifies an application when an IME is about to create the status window.</span></span> <span data-ttu-id="5cce3-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Benachrichtigungs**](wm-ime-notify.md) Meldung mit den Parametereinstellungen, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="5cce3-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_OPENSTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="5cce3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cce3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cce3-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="5cce3-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="5cce3-109">Legen Sie auf IMN \_ openstatus Window fest.</span><span class="sxs-lookup"><span data-stu-id="5cce3-109">Set to IMN\_OPENSTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="5cce3-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="5cce3-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="5cce3-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5cce3-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cce3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5cce3-112">Return Value</span></span>

<span data-ttu-id="5cce3-113">Dieser Befehl weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="5cce3-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cce3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5cce3-114">Remarks</span></span>

<span data-ttu-id="5cce3-115">Eine Anwendung verarbeitet diesen Befehl, um das Statusfenster für das IME eigenständig anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5cce3-115">An application processes this command to display the status window for the IME by itself.</span></span>

<span data-ttu-id="5cce3-116">Im IME-Fenster wird ein Statusfenster erstellt, wenn der Befehl verarbeitet wird, und die Zeichen folgen, die im Fenster angezeigt werden, werden im Eingabe Kontext festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5cce3-116">The IME window creates a status window when it processes this command and sets the strings to display in the window into the input context.</span></span> <span data-ttu-id="5cce3-117">Anwendungen können Informationen über das Statusfenster mithilfe der [**immgetdeversionstatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) -Funktion erhalten.</span><span class="sxs-lookup"><span data-stu-id="5cce3-117">Applications can get information about the status window by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cce3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5cce3-118">Requirements</span></span>



| <span data-ttu-id="5cce3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5cce3-119">Requirement</span></span> | <span data-ttu-id="5cce3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5cce3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cce3-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5cce3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5cce3-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5cce3-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5cce3-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5cce3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5cce3-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5cce3-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5cce3-125">Header</span><span class="sxs-lookup"><span data-stu-id="5cce3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cce3-126"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5cce3-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cce3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5cce3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cce3-128">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="5cce3-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="5cce3-129">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="5cce3-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="5cce3-130">**Immgetsystemversionstatus**</span><span class="sxs-lookup"><span data-stu-id="5cce3-130">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="5cce3-131">**WM- \_ IME \_ Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="5cce3-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




