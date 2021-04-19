---
description: Markiert eine Anwendung, wenn eine ausgewählte IME Informationen zum Kandidaten Fenster benötigt. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Anforderungs Nachricht mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: 35849290-a5be-406f-82f5-4a7e2af48586
title: IMR_CANDIDATEWINDOW Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb905acace27cc9bb04ce2b14dc6a685b7c4f8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362210"
---
# <a name="imr_candidatewindow-notification-code"></a><span data-ttu-id="c60f7-104">IMR \_ candidatewindow-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="c60f7-104">IMR\_CANDIDATEWINDOW notification code</span></span>

<span data-ttu-id="c60f7-105">Markiert eine Anwendung, wenn eine ausgewählte IME Informationen zum Kandidaten Fenster benötigt.</span><span class="sxs-lookup"><span data-stu-id="c60f7-105">Notfies an application when a selected IME needs information about the candidate window.</span></span> <span data-ttu-id="c60f7-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Anforderungs**](wm-ime-request.md) Nachricht mit den Parametereinstellungen, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c60f7-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_CANDIDATEWINDOW
```



## <a name="parameters"></a><span data-ttu-id="c60f7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c60f7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c60f7-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="c60f7-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="c60f7-109">Legen Sie auf IMR \_ candidatewindow fest.</span><span class="sxs-lookup"><span data-stu-id="c60f7-109">Set to IMR\_CANDIDATEWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="c60f7-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="c60f7-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="c60f7-111">Zeiger auf einen Puffer, der eine [**candidateform**](/windows/win32/api/imm/ns-imm-candidateform) -Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="c60f7-111">Pointer to a buffer containing a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure.</span></span> <span data-ttu-id="c60f7-112">Der zugehörige **dwIndex** -Member enthält den Index des Kandidaten Fensters, auf das verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c60f7-112">Its **dwIndex** member contains the index to the candidate window referenced.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c60f7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c60f7-113">Return Value</span></span>

<span data-ttu-id="c60f7-114">Gibt einen Wert ungleich 0 (null) zurück, wenn die Anwendung die [**candidateform**](/windows/win32/api/imm/ns-imm-candidateform) -Struktur füllt.</span><span class="sxs-lookup"><span data-stu-id="c60f7-114">Returns a nonzero value if the application fills in the [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure.</span></span> <span data-ttu-id="c60f7-115">Andernfalls gibt der Befehl 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="c60f7-115">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="c60f7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c60f7-116">Remarks</span></span>

<span data-ttu-id="c60f7-117">Dieser Befehl kann vom IME an ein Fenster gesendet werden, das das ISC \_ showuicandidatewindow-Flag im [**WM \_ IME \_ SetContext**](wm-ime-setcontext.md) -Nachrichten Handler gelöscht hat.</span><span class="sxs-lookup"><span data-stu-id="c60f7-117">This command can be sent by the IME to a window that has cleared the ISC\_SHOWUICANDIDATEWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="c60f7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c60f7-118">Requirements</span></span>



| <span data-ttu-id="c60f7-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c60f7-119">Requirement</span></span> | <span data-ttu-id="c60f7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c60f7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c60f7-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c60f7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c60f7-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c60f7-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c60f7-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c60f7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c60f7-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c60f7-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c60f7-125">Header</span><span class="sxs-lookup"><span data-stu-id="c60f7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c60f7-126"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c60f7-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c60f7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c60f7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c60f7-128">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="c60f7-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="c60f7-129">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="c60f7-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="c60f7-130">**Candidateform**</span><span class="sxs-lookup"><span data-stu-id="c60f7-130">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[<span data-ttu-id="c60f7-131">**WM- \_ IME- \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="c60f7-131">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="c60f7-132">**WM \_ IME \_ SetContext**</span><span class="sxs-lookup"><span data-stu-id="c60f7-132">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 




