---
description: Weist ein IME-Fenster an, die Position des Kandidaten Fensters festzulegen. Um diesen Befehl zu senden, verwendet die Anwendung die WM- \_ IME- \_ Steuerungs Meldung mit den unten gezeigten Parametereinstellungen.
ms.assetid: 7a2f9958-4a4e-462a-9737-e7796fd90216
title: IMC_SETCANDIDATEPOS Befehl (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ac05890e4c720c5b671faa7f20a68a96b24a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752345"
---
# <a name="imc_setcandidatepos-command"></a><span data-ttu-id="4624a-104">IMC \_ setcandidatepos-Befehl</span><span class="sxs-lookup"><span data-stu-id="4624a-104">IMC\_SETCANDIDATEPOS command</span></span>

<span data-ttu-id="4624a-105">Weist ein IME-Fenster an, die Position des Kandidaten Fensters festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4624a-105">Instructs an IME window to set the position of the candidates window.</span></span> <span data-ttu-id="4624a-106">Um diesen Befehl zu senden, verwendet die Anwendung die [**WM- \_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung mit den unten gezeigten Parametereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="4624a-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="4624a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4624a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4624a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="4624a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="4624a-109">Legen Sie auf IMC \_ setcandidatepos fest.</span><span class="sxs-lookup"><span data-stu-id="4624a-109">Set to IMC\_SETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="4624a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="4624a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="4624a-111">Zeiger auf eine [**candidateform**](/windows/win32/api/imm/ns-imm-candidateform) -Struktur, die die x-Koordinate und die y-Koordinate für das Fenster Kandidaten enthält.</span><span class="sxs-lookup"><span data-stu-id="4624a-111">Pointer to a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure that contains the x coordinate and y coordinate for the candidates window.</span></span> <span data-ttu-id="4624a-112">Die Anwendung sollte den **dwIndex** -Member dieser Struktur festlegen.</span><span class="sxs-lookup"><span data-stu-id="4624a-112">The application should set the **dwIndex** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4624a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4624a-113">Return Value</span></span>

<span data-ttu-id="4624a-114">Gibt bei Erfolg 0 zurück oder andernfalls einen Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="4624a-114">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4624a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4624a-115">Remarks</span></span>

<span data-ttu-id="4624a-116">Dieser Befehl ist für Anwendungen vorgesehen, die eigen Kompositions Zeichen anzeigen, aber das IME-Fenster verwenden, um Kandidaten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4624a-116">This command is intended for applications that display composition characters on their own but use the IME window to display candidates.</span></span>

## <a name="requirements"></a><span data-ttu-id="4624a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4624a-117">Requirements</span></span>



| <span data-ttu-id="4624a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4624a-118">Requirement</span></span> | <span data-ttu-id="4624a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4624a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4624a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4624a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4624a-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4624a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4624a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4624a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4624a-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4624a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4624a-124">Header</span><span class="sxs-lookup"><span data-stu-id="4624a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4624a-125"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4624a-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4624a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4624a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4624a-127">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="4624a-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="4624a-128">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="4624a-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="4624a-129">**Candidateform**</span><span class="sxs-lookup"><span data-stu-id="4624a-129">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[<span data-ttu-id="4624a-130">**WM \_ IME- \_ Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="4624a-130">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




