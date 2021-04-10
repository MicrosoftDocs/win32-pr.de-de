---
description: Benachrichtigt eine Anwendung, wenn ein IME im Begriff ist, das Kandidaten Fenster zu öffnen. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Benachrichtigungs Meldung mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: 439ff125-2731-4eb1-8287-4ca8ace7d8ec
title: IMN_OPENCANDIDATE-Ereignis (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f8f412c60cc6b62904e562d450479af642de0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865492"
---
# <a name="imn_opencandidate-event"></a><span data-ttu-id="5b1ca-104">IMN \_ opencandidate-Ereignis</span><span class="sxs-lookup"><span data-stu-id="5b1ca-104">IMN\_OPENCANDIDATE event</span></span>

<span data-ttu-id="5b1ca-105">Benachrichtigt eine Anwendung, wenn ein IME im Begriff ist, das Kandidaten Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-105">Notifies an application when an IME is about to open the candidate window.</span></span> <span data-ttu-id="5b1ca-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Benachrichtigungs**](wm-ime-notify.md) Meldung mit den Parametereinstellungen, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_OPENCANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="5b1ca-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b1ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b1ca-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b1ca-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="5b1ca-109">Legen Sie auf IMN \_ opencandidate fest.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-109">Set to IMN\_OPENCANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="5b1ca-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="5b1ca-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="5b1ca-111">Flag der Kandidatenliste.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-111">Candidate list flag.</span></span> <span data-ttu-id="5b1ca-112">Jedes Bit entspricht einer Kandidatenliste: Bit 0 bis zur ersten Liste, Bit 1 bis zum zweiten usw.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="5b1ca-113">Wenn ein angegebenes Bit 1 ist, wird das entsprechende Kandidaten Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-113">If a specified bit is 1, the corresponding candidate window is about to be opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b1ca-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b1ca-114">Return Value</span></span>

<span data-ttu-id="5b1ca-115">Dieser Befehl weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b1ca-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b1ca-116">Remarks</span></span>

<span data-ttu-id="5b1ca-117">Eine Anwendung sollte diesen Befehl verarbeiten, wenn Sie Kandidaten selbst anzeigt.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-117">An application should process this command if it displays candidates itself.</span></span> <span data-ttu-id="5b1ca-118">Die Anwendung kann eine Liste der anzuzeigenden Kandidaten mithilfe der [**immgetcandidatelist**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-118">The application can retrieve a list of candidates to display by using the [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) function.</span></span>

<span data-ttu-id="5b1ca-119">Standardmäßig erstellt das IME-Fenster ein Kandidaten Fenster, wenn es diesen Befehl verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="5b1ca-119">By default, the IME window creates a candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b1ca-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b1ca-120">Requirements</span></span>



| <span data-ttu-id="5b1ca-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b1ca-121">Requirement</span></span> | <span data-ttu-id="5b1ca-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5b1ca-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b1ca-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b1ca-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5b1ca-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b1ca-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5b1ca-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b1ca-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5b1ca-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b1ca-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5b1ca-127">Header</span><span class="sxs-lookup"><span data-stu-id="5b1ca-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b1ca-128"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b1ca-128"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b1ca-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b1ca-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b1ca-130">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="5b1ca-130">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="5b1ca-131">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="5b1ca-131">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="5b1ca-132">**Immgetcandidatelist**</span><span class="sxs-lookup"><span data-stu-id="5b1ca-132">**ImmGetCandidateList**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[<span data-ttu-id="5b1ca-133">**WM- \_ IME \_ Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="5b1ca-133">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




