---
description: Benachrichtigt eine Anwendung, wenn der ausgewählte IME Informationen zu den Koordinaten eines Zeichens in der Kompositions Zeichenfolge benötigt. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Anforderungs Nachricht mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: cae7e5b3-8aaf-452d-80df-fb0ae04a342c
title: IMR_QUERYCHARPOSITION Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947eec9b3dd1f678d9266bb795214cf392629193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358434"
---
# <a name="imr_querycharposition-notification-code"></a><span data-ttu-id="aac12-104">IMR \_ querycharposition-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="aac12-104">IMR\_QUERYCHARPOSITION notification code</span></span>

<span data-ttu-id="aac12-105">Benachrichtigt eine Anwendung, wenn der ausgewählte IME Informationen zu den Koordinaten eines Zeichens in der Kompositions Zeichenfolge benötigt.</span><span class="sxs-lookup"><span data-stu-id="aac12-105">Notifies an application when the selected IME needs information about the coordinates of a character in the composition string.</span></span> <span data-ttu-id="aac12-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Anforderungs**](wm-ime-request.md) Nachricht mit den Parametereinstellungen, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="aac12-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_QUERYCHARPOSITION
```



## <a name="parameters"></a><span data-ttu-id="aac12-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="aac12-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aac12-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="aac12-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="aac12-109">Legen Sie auf IMR \_ querycharposition fest.</span><span class="sxs-lookup"><span data-stu-id="aac12-109">Set to IMR\_QUERYCHARPOSITION.</span></span>

</dd> <dt>

<span data-ttu-id="aac12-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="aac12-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="aac12-111">Zeiger auf eine [**imecharposition**](/windows/win32/api/imm/ns-imm-imecharposition) -Struktur, die die Position des Zeichens im Kompositionsfenster enthält.</span><span class="sxs-lookup"><span data-stu-id="aac12-111">Pointer to an [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure that contains the position of the character in the composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aac12-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aac12-112">Return Value</span></span>

<span data-ttu-id="aac12-113">Gibt einen Wert ungleich 0 (null) zurück, wenn die Anwendung die [**imecharposition**](/windows/win32/api/imm/ns-imm-imecharposition) -Struktur füllt.</span><span class="sxs-lookup"><span data-stu-id="aac12-113">Returns a nonzero value if the application fills the [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure.</span></span> <span data-ttu-id="aac12-114">Andernfalls gibt der Befehl 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="aac12-114">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="aac12-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aac12-115">Remarks</span></span>

<span data-ttu-id="aac12-116">Eine Anwendung, die die Kompositions Zeichenfolge selbst zeichnet, anstatt sich auf den IME zu verlassen, ist für das Ausfüllen aller Member der [**imecharposition**](/windows/win32/api/imm/ns-imm-imecharposition) -Struktur verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="aac12-116">An application that draws the composition string itself, instead of relying on the IME, is responsible for filling in all the members of the [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure.</span></span> <span data-ttu-id="aac12-117">Andernfalls sollte die Anwendung den Befehl an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) oder [**immisuimess**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) übergeben, wenn Sie über ein eigenes IME-Benutzeroberflächen Fenster verfügt.</span><span class="sxs-lookup"><span data-stu-id="aac12-117">Otherwise, the application should pass the command to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) if it has its own IME user interface window.</span></span>

## <a name="requirements"></a><span data-ttu-id="aac12-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aac12-118">Requirements</span></span>



| <span data-ttu-id="aac12-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aac12-119">Requirement</span></span> | <span data-ttu-id="aac12-120">Wert</span><span class="sxs-lookup"><span data-stu-id="aac12-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aac12-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aac12-121">Minimum supported client</span></span><br/> | <span data-ttu-id="aac12-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aac12-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="aac12-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aac12-123">Minimum supported server</span></span><br/> | <span data-ttu-id="aac12-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aac12-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="aac12-125">Header</span><span class="sxs-lookup"><span data-stu-id="aac12-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="aac12-126"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aac12-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aac12-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aac12-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aac12-128">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="aac12-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="aac12-129">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="aac12-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="aac12-130">**Imecharposition**</span><span class="sxs-lookup"><span data-stu-id="aac12-130">**IMECHARPOSITION**</span></span>](/windows/win32/api/imm/ns-imm-imecharposition)
</dt> <dt>

[<span data-ttu-id="aac12-131">**Immisuimess Age**</span><span class="sxs-lookup"><span data-stu-id="aac12-131">**ImmIsUIMessage**</span></span>](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> <dt>

[<span data-ttu-id="aac12-132">**WM- \_ IME- \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="aac12-132">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 
