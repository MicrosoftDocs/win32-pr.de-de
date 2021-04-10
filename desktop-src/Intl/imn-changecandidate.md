---
description: Benachrichtigt die Anwendung, wenn ein IME im Begriff ist, den Inhalt des Kandidaten Fensters zu ändern. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Benachrichtigungs Meldung mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: 0a276f9c-cece-4fa6-b71a-ba0daad5ca05
title: IMN_CHANGECANDIDATE Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 197380c3cf6369e0dbfd7dbca76bb3b84334eb6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131740"
---
# <a name="imn_changecandidate-notification-code"></a><span data-ttu-id="2b257-104">IMN \_ changecandidate-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="2b257-104">IMN\_CHANGECANDIDATE notification code</span></span>

<span data-ttu-id="2b257-105">Benachrichtigt die Anwendung, wenn ein IME im Begriff ist, den Inhalt des Kandidaten Fensters zu ändern.</span><span class="sxs-lookup"><span data-stu-id="2b257-105">Notifies the application when an IME is about to change the content of the candidate window.</span></span> <span data-ttu-id="2b257-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Benachrichtigungs**](wm-ime-notify.md) Meldung mit den Parametereinstellungen, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2b257-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CHANGECANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="2b257-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b257-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b257-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b257-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="2b257-109">Legen Sie auf IMN \_ changecandidate fest.</span><span class="sxs-lookup"><span data-stu-id="2b257-109">Set to IMN\_CHANGECANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="2b257-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="2b257-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="2b257-111">Flag der Kandidatenliste.</span><span class="sxs-lookup"><span data-stu-id="2b257-111">Candidate list flag.</span></span> <span data-ttu-id="2b257-112">Jedes Bit entspricht einer Kandidatenliste: Bit 0 bis zur ersten Liste, Bit 1 zur zweiten Liste usw.</span><span class="sxs-lookup"><span data-stu-id="2b257-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second list, and so on.</span></span> <span data-ttu-id="2b257-113">Wenn ein angegebenes Bit 1 ist, wird das entsprechende Kandidaten Fenster geändert.</span><span class="sxs-lookup"><span data-stu-id="2b257-113">If a specified bit is 1, the corresponding candidate window is about to be changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b257-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b257-114">Return Value</span></span>

<span data-ttu-id="2b257-115">Dieser Befehl weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="2b257-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b257-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b257-116">Remarks</span></span>

<span data-ttu-id="2b257-117">Eine Anwendung sollte diesen Befehl verarbeiten, wenn Sie Kandidaten selbst anzeigt.</span><span class="sxs-lookup"><span data-stu-id="2b257-117">An application should process this command if it displays candidates itself.</span></span>

<span data-ttu-id="2b257-118">Das IME-Fenster ändert die Darstellung des Kandidaten Fensters, wenn es diesen Befehl verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="2b257-118">The IME window changes the appearance of the candidate window when it processes this command.</span></span> <span data-ttu-id="2b257-119">Eine Anwendung kann Informationen über das System Fenster mit " [**immgetcandidatelistcount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) " und " [**immgetcandidatelist**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) " erhalten.</span><span class="sxs-lookup"><span data-stu-id="2b257-119">An application can get information about the system window with the [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) and [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)</span></span>

## <a name="requirements"></a><span data-ttu-id="2b257-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b257-120">Requirements</span></span>



| <span data-ttu-id="2b257-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b257-121">Requirement</span></span> | <span data-ttu-id="2b257-122">Wert</span><span class="sxs-lookup"><span data-stu-id="2b257-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b257-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b257-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2b257-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b257-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2b257-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b257-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2b257-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b257-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2b257-127">Header</span><span class="sxs-lookup"><span data-stu-id="2b257-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b257-128"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b257-128"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b257-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b257-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b257-130">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="2b257-130">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="2b257-131">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="2b257-131">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="2b257-132">**Immgetcandidatelist**</span><span class="sxs-lookup"><span data-stu-id="2b257-132">**ImmGetCandidateList**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[<span data-ttu-id="2b257-133">**Immgetcandidatelistcount**</span><span class="sxs-lookup"><span data-stu-id="2b257-133">**ImmGetCandidateListCount**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)
</dt> <dt>

[<span data-ttu-id="2b257-134">**WM- \_ IME \_ Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="2b257-134">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




