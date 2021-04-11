---
description: Weist ein IME-Fenster an, die Position des Status Fensters festzulegen. Um diesen Befehl zu senden, verwendet die Anwendung die WM- \_ IME- \_ Steuerungs Meldung mit den Parametereinstellungen wie unten gezeigt.
ms.assetid: d77de7ab-1fbc-42f4-829e-e9fb51668d21
title: IMC_SETSTATUSWINDOWPOS Befehl (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99c57eef1a4748bb58018ee47aaee21eb677016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041805"
---
# <a name="imc_setstatuswindowpos-command"></a><span data-ttu-id="94896-104">Befehl "der \_ Befehl"</span><span class="sxs-lookup"><span data-stu-id="94896-104">IMC\_SETSTATUSWINDOWPOS command</span></span>

<span data-ttu-id="94896-105">Weist ein IME-Fenster an, die Position des Status Fensters festzulegen.</span><span class="sxs-lookup"><span data-stu-id="94896-105">Instructs an IME window to set the position of the status window.</span></span> <span data-ttu-id="94896-106">Um diesen Befehl zu senden, verwendet die Anwendung die [**WM- \_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung mit den Parametereinstellungen wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="94896-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMC_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="94896-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="94896-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94896-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="94896-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="94896-109">Legen Sie auf "IMC \_ SetStatus-WINDOWPOS" fest.</span><span class="sxs-lookup"><span data-stu-id="94896-109">Set to IMC\_SETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="94896-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="94896-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="94896-111">Zeiger auf eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur, die die x-Koordinate und die y-Koordinate der Position des Status Fensters enthält.</span><span class="sxs-lookup"><span data-stu-id="94896-111">Pointer to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x coordinate and y coordinate of the position of the status window.</span></span> <span data-ttu-id="94896-112">Die Koordinaten befinden sich in Bildschirm Koordinaten relativ zur oberen linken Ecke der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="94896-112">The coordinates are in screen coordinates, relative to the upper left corner of the display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94896-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94896-113">Return Value</span></span>

<span data-ttu-id="94896-114">Gibt bei Erfolg 0 zurück oder andernfalls einen Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="94896-114">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="94896-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94896-115">Requirements</span></span>



| <span data-ttu-id="94896-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94896-116">Requirement</span></span> | <span data-ttu-id="94896-117">Wert</span><span class="sxs-lookup"><span data-stu-id="94896-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94896-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94896-118">Minimum supported client</span></span><br/> | <span data-ttu-id="94896-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94896-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="94896-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94896-120">Minimum supported server</span></span><br/> | <span data-ttu-id="94896-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94896-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="94896-122">Header</span><span class="sxs-lookup"><span data-stu-id="94896-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="94896-123"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94896-123"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94896-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94896-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94896-125">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="94896-125">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="94896-126">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="94896-126">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="94896-127">**WM \_ IME- \_ Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="94896-127">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
