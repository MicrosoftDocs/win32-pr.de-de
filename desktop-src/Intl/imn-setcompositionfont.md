---
description: Benachrichtigt eine Anwendung, wenn die Schriftart des Eingabe Kontexts aktualisiert wird. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Benachrichtigungs Meldung mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: 946bee83-91af-4647-9b22-96d42466352c
title: IMN_SETCOMPOSITIONFONT Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8373954e80e420004b347bf1b40021c86ddbb876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359490"
---
# <a name="imn_setcompositionfont-notification-code"></a><span data-ttu-id="923c4-104">IMN \_ setcompositionfont-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="923c4-104">IMN\_SETCOMPOSITIONFONT notification code</span></span>

<span data-ttu-id="923c4-105">Benachrichtigt eine Anwendung, wenn die Schriftart des Eingabe Kontexts aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="923c4-105">Notifies an application when the font of the input context is updated.</span></span> <span data-ttu-id="923c4-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Benachrichtigungs**](wm-ime-notify.md) Meldung mit den Parametereinstellungen, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="923c4-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="923c4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="923c4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="923c4-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="923c4-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="923c4-109">Legen Sie auf IMN \_ setcompositionfont fest.</span><span class="sxs-lookup"><span data-stu-id="923c4-109">Set to IMN\_SETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="923c4-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="923c4-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="923c4-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="923c4-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="923c4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="923c4-112">Return Value</span></span>

<span data-ttu-id="923c4-113">Dieser Befehl weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="923c4-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="923c4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="923c4-114">Remarks</span></span>

<span data-ttu-id="923c4-115">Die Anwendung kann Informationen über die Schriftart mithilfe der [**immgetcompositionfont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) -Funktion erhalten.</span><span class="sxs-lookup"><span data-stu-id="923c4-115">The application can get information about the font by using the [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) function.</span></span> <span data-ttu-id="923c4-116">Das IME-Fenster verwendet anschließend die Schriftart zum Zeichnen der Kompositions Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="923c4-116">The IME window subsequently uses the font to draw the composition string.</span></span>

## <a name="requirements"></a><span data-ttu-id="923c4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="923c4-117">Requirements</span></span>



| <span data-ttu-id="923c4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="923c4-118">Requirement</span></span> | <span data-ttu-id="923c4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="923c4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="923c4-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="923c4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="923c4-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="923c4-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="923c4-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="923c4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="923c4-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="923c4-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="923c4-124">Header</span><span class="sxs-lookup"><span data-stu-id="923c4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="923c4-125"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="923c4-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="923c4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="923c4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="923c4-127">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="923c4-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="923c4-128">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="923c4-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="923c4-129">**Immgetcompositionfont**</span><span class="sxs-lookup"><span data-stu-id="923c4-129">**ImmGetCompositionFont**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)
</dt> <dt>

[<span data-ttu-id="923c4-130">**WM- \_ IME \_ Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="923c4-130">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




