---
description: Benachrichtigt eine Anwendung, wenn eine ausgewählte IME Informationen zum Kompositionsfenster benötigt. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Anforderungs Nachricht mit den festgelegten Parametern, wie unten gezeigt.
ms.assetid: 08fd7119-d225-4a78-b2cd-8b58887c9139
title: IMR_COMPOSITIONWINDOW Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af0481ccebc59968fe85a489c856388a04dbece
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358876"
---
# <a name="imr_compositionwindow-notification-code"></a><span data-ttu-id="f4667-104">IMR \_ compositionwindow-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="f4667-104">IMR\_COMPOSITIONWINDOW notification code</span></span>

<span data-ttu-id="f4667-105">Benachrichtigt eine Anwendung, wenn eine ausgewählte IME Informationen zum Kompositionsfenster benötigt.</span><span class="sxs-lookup"><span data-stu-id="f4667-105">Notifies an application when a selected IME needs information about the composition window.</span></span> <span data-ttu-id="f4667-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Anforderungs**](wm-ime-request.md) Nachricht mit den festgelegten Parametern, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f4667-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters set as shown below.</span></span>


```C++
LRESULT IMR_COMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="f4667-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4667-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4667-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4667-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="f4667-109">Legen Sie auf IMR \_ compositionwindow fest.</span><span class="sxs-lookup"><span data-stu-id="f4667-109">Set to IMR\_COMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="f4667-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="f4667-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f4667-111">Zeiger auf einen Puffer, der eine [**compositionform**](/windows/win32/api/imm/ns-imm-compositionform) -Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="f4667-111">Pointer to a buffer containing a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4667-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4667-112">Return Value</span></span>

<span data-ttu-id="f4667-113">Gibt einen Wert ungleich 0 (null) zurück, wenn die Anwendung die [**compositionform**](/windows/win32/api/imm/ns-imm-compositionform) -Struktur füllt.</span><span class="sxs-lookup"><span data-stu-id="f4667-113">Returns a nonzero value if the application fills in the [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure.</span></span> <span data-ttu-id="f4667-114">Andernfalls gibt der Befehl 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="f4667-114">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4667-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4667-115">Remarks</span></span>

<span data-ttu-id="f4667-116">Dieser Befehl kann von der IME an ein Fenster gesendet werden, das das ISC \_ showuicompositionwindow-Flag im [**WM \_ IME \_ SetContext**](wm-ime-setcontext.md) -Nachrichten Handler gelöscht hat.</span><span class="sxs-lookup"><span data-stu-id="f4667-116">This command can be sent by the IME to a window that has cleared the ISC\_SHOWUICOMPOSITIONWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4667-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4667-117">Requirements</span></span>



| <span data-ttu-id="f4667-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4667-118">Requirement</span></span> | <span data-ttu-id="f4667-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f4667-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4667-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4667-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f4667-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4667-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f4667-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4667-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f4667-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4667-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f4667-124">Header</span><span class="sxs-lookup"><span data-stu-id="f4667-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4667-125"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4667-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4667-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4667-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4667-127">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="f4667-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="f4667-128">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="f4667-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="f4667-129">**Compositionform**</span><span class="sxs-lookup"><span data-stu-id="f4667-129">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[<span data-ttu-id="f4667-130">**WM- \_ IME- \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="f4667-130">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="f4667-131">**WM \_ IME \_ SetContext**</span><span class="sxs-lookup"><span data-stu-id="f4667-131">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 




