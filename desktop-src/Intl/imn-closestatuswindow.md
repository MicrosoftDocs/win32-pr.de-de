---
description: Benachrichtigt eine Anwendung, wenn ein IME im Begriff ist, das Statusfenster zu schließen. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Benachrichtigungs Meldung mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: d59fdf76-50e7-4a59-b1bd-a12cdb0026f6
title: IMN_CLOSESTATUSWINDOW Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0347fb4b0d83a9e3891b9aea59d82ab81e2183
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368782"
---
# <a name="imn_closestatuswindow-notification-code"></a><span data-ttu-id="d2a58-104">IMN \_ closestatus Window-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="d2a58-104">IMN\_CLOSESTATUSWINDOW notification code</span></span>

<span data-ttu-id="d2a58-105">Benachrichtigt eine Anwendung, wenn ein IME im Begriff ist, das Statusfenster zu schließen.</span><span class="sxs-lookup"><span data-stu-id="d2a58-105">Notifies an application when an IME is about to close the status window.</span></span> <span data-ttu-id="d2a58-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Benachrichtigungs**](wm-ime-notify.md) Meldung mit den Parametereinstellungen, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2a58-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CLOSESTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="d2a58-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2a58-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a58-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2a58-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="d2a58-109">Legen Sie auf IMN \_ closestatus Window fest.</span><span class="sxs-lookup"><span data-stu-id="d2a58-109">Set to IMN\_CLOSESTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="d2a58-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="d2a58-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d2a58-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2a58-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2a58-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2a58-112">Return Value</span></span>

<span data-ttu-id="d2a58-113">Dieser Befehl weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="d2a58-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2a58-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2a58-114">Remarks</span></span>

<span data-ttu-id="d2a58-115">Eine Anwendung sollte diesen Befehl verarbeiten, wenn Sie das Statusfenster für den IME anzeigt.</span><span class="sxs-lookup"><span data-stu-id="d2a58-115">An application should process this command if it displays the status window for the IME.</span></span>

<span data-ttu-id="d2a58-116">Das Fenster IME schließt das Fenster Status, wenn es diesen Befehl verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d2a58-116">The IME window closes the status window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2a58-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2a58-117">Requirements</span></span>



| <span data-ttu-id="d2a58-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2a58-118">Requirement</span></span> | <span data-ttu-id="d2a58-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d2a58-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a58-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2a58-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d2a58-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2a58-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d2a58-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2a58-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d2a58-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2a58-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d2a58-124">Header</span><span class="sxs-lookup"><span data-stu-id="d2a58-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2a58-125"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2a58-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2a58-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2a58-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a58-127">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="d2a58-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d2a58-128">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="d2a58-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="d2a58-129">**WM- \_ IME \_ Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="d2a58-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




