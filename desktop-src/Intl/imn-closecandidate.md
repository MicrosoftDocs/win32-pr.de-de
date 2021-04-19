---
description: Benachrichtigt eine Anwendung, wenn ein IME im Begriff ist, das Fenster Kandidaten zu schließen. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Benachrichtigungs Meldung mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: d96cea0a-1fc4-4ba7-bb96-7e9c0b67ce5b
title: IMN_CLOSECANDIDATE Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3414d2aa37a50b7f35f0dfb936b641b7c86a932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368784"
---
# <a name="imn_closecandidate-notification-code"></a><span data-ttu-id="00aab-104">IMN \_ closecandidate-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="00aab-104">IMN\_CLOSECANDIDATE notification code</span></span>

<span data-ttu-id="00aab-105">Benachrichtigt eine Anwendung, wenn ein IME im Begriff ist, das Fenster Kandidaten zu schließen.</span><span class="sxs-lookup"><span data-stu-id="00aab-105">Notifies an application when an IME is about to close the candidates window.</span></span> <span data-ttu-id="00aab-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Benachrichtigungs**](wm-ime-notify.md) Meldung mit den Parametereinstellungen, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="00aab-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CLOSECANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="00aab-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="00aab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00aab-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="00aab-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="00aab-109">Legen Sie auf IMN \_ closecandidate fest.</span><span class="sxs-lookup"><span data-stu-id="00aab-109">Set to IMN\_CLOSECANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="00aab-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="00aab-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="00aab-111">Flag der Kandidatenliste.</span><span class="sxs-lookup"><span data-stu-id="00aab-111">Candidate list flag.</span></span> <span data-ttu-id="00aab-112">Jedes Bit entspricht einer Kandidatenliste: Bit 0 bis zur ersten Liste, Bit 1 bis zum zweiten usw.</span><span class="sxs-lookup"><span data-stu-id="00aab-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="00aab-113">Wenn ein angegebenes Bit 1 ist, wird das entsprechende Kandidaten Fenster geschlossen.</span><span class="sxs-lookup"><span data-stu-id="00aab-113">If a specified bit is 1, the corresponding candidates window is about to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00aab-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00aab-114">Return Value</span></span>

<span data-ttu-id="00aab-115">Dieser Befehl weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="00aab-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00aab-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00aab-116">Remarks</span></span>

<span data-ttu-id="00aab-117">Eine Anwendung sollte diesen Befehl verarbeiten, wenn Sie Kandidaten selbst anzeigt.</span><span class="sxs-lookup"><span data-stu-id="00aab-117">An application should process this command if it displays candidates itself.</span></span>

<span data-ttu-id="00aab-118">Standardmäßig zerstört das IME-Fenster ein Kandidaten Fenster, wenn es diesen Befehl verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="00aab-118">By default, the IME window destroys a candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="00aab-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00aab-119">Requirements</span></span>



| <span data-ttu-id="00aab-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00aab-120">Requirement</span></span> | <span data-ttu-id="00aab-121">Wert</span><span class="sxs-lookup"><span data-stu-id="00aab-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00aab-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00aab-122">Minimum supported client</span></span><br/> | <span data-ttu-id="00aab-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00aab-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="00aab-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00aab-124">Minimum supported server</span></span><br/> | <span data-ttu-id="00aab-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00aab-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="00aab-126">Header</span><span class="sxs-lookup"><span data-stu-id="00aab-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="00aab-127"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00aab-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00aab-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00aab-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00aab-129">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="00aab-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="00aab-130">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="00aab-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="00aab-131">**WM- \_ IME \_ Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="00aab-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




