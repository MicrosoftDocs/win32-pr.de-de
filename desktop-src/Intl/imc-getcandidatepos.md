---
description: Weist ein IME-Fenster an, die Position des Kandidaten Fensters zu erhalten. Um diesen Befehl zu senden, verwendet die Anwendung die WM- \_ IME- \_ Steuerungs Meldung mit den unten gezeigten Parametereinstellungen.
ms.assetid: e582dbc2-8081-424c-a972-1a182a477293
title: IMC_GETCANDIDATEPOS Befehl (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb5cd143bf45f9bdb37be4cbe3078a483f53db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366522"
---
# <a name="imc_getcandidatepos-command"></a><span data-ttu-id="b29a4-104">Befehl "IMC \_ getcandidatepos"</span><span class="sxs-lookup"><span data-stu-id="b29a4-104">IMC\_GETCANDIDATEPOS command</span></span>

<span data-ttu-id="b29a4-105">Weist ein IME-Fenster an, die Position des Kandidaten Fensters zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b29a4-105">Instructs an IME window to get the position of the candidate window.</span></span> <span data-ttu-id="b29a4-106">Um diesen Befehl zu senden, verwendet die Anwendung die [**WM- \_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung mit den unten gezeigten Parametereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="b29a4-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="b29a4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b29a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b29a4-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="b29a4-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="b29a4-109">Legen Sie auf "IMC \_ getcandidatepos" fest.</span><span class="sxs-lookup"><span data-stu-id="b29a4-109">Set to IMC\_GETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="b29a4-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="b29a4-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b29a4-111">Zeiger auf eine [**candidateform**](/windows/win32/api/imm/ns-imm-candidateform) -Struktur, die die Position des Kandidaten Fensters enthält.</span><span class="sxs-lookup"><span data-stu-id="b29a4-111">Pointer to a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure that contains the position of the candidate window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b29a4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b29a4-112">Return Value</span></span>

<span data-ttu-id="b29a4-113">Gibt bei Erfolg 0 zurück oder andernfalls einen Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b29a4-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b29a4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b29a4-114">Remarks</span></span>

<span data-ttu-id="b29a4-115">Da der IME die Position eines Kandidaten Fensters anpassen kann, verwendet eine Anwendung diesen Befehl, um die tatsächliche Position zu ermitteln, um zu entscheiden, ob das Fenster neu positioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b29a4-115">Because the IME might adjust the position of a candidate window, an application uses this command to get the actual position to decide whether to reposition the window.</span></span> <span data-ttu-id="b29a4-116">Die abgerufene Position befindet sich in Fenster Koordinaten relativ zu dem Fenster, das den aktuellen Eingabefokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="b29a4-116">The retrieved position is in window coordinates relative to the window having the current input focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="b29a4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b29a4-117">Requirements</span></span>



| <span data-ttu-id="b29a4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b29a4-118">Requirement</span></span> | <span data-ttu-id="b29a4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b29a4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b29a4-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b29a4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b29a4-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b29a4-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b29a4-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b29a4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b29a4-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b29a4-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b29a4-124">Header</span><span class="sxs-lookup"><span data-stu-id="b29a4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b29a4-125"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b29a4-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b29a4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b29a4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b29a4-127">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="b29a4-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="b29a4-128">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="b29a4-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="b29a4-129">**Candidateform**</span><span class="sxs-lookup"><span data-stu-id="b29a4-129">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> </dl>

 

 




