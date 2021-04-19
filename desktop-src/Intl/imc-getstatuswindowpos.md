---
description: Weist ein IME-Fenster an, die Position des Status Fensters zu erhalten. Um diesen Befehl zu senden, verwendet die Anwendung die WM- \_ IME- \_ Steuerungs Meldung mit den unten gezeigten Parametereinstellungen.
ms.assetid: 59c7baae-1b8a-4761-9814-31afd8d39691
title: IMC_GETSTATUSWINDOWPOS Befehl (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd17c5787d9ef8c787e62a556afa2f136bd65c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356800"
---
# <a name="imc_getstatuswindowpos-command"></a><span data-ttu-id="e0161-104">Befehl "IMC \_ GetStatus-WINDOWPOS"</span><span class="sxs-lookup"><span data-stu-id="e0161-104">IMC\_GETSTATUSWINDOWPOS command</span></span>

<span data-ttu-id="e0161-105">Weist ein IME-Fenster an, die Position des Status Fensters zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e0161-105">Instructs an IME window to get the position of the status window.</span></span> <span data-ttu-id="e0161-106">Um diesen Befehl zu senden, verwendet die Anwendung die [**WM- \_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung mit den unten gezeigten Parametereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="e0161-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="e0161-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0161-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0161-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0161-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="e0161-109">Legen Sie auf "IMC \_ GetStatus-WINDOWPOS" fest.</span><span class="sxs-lookup"><span data-stu-id="e0161-109">Set to IMC\_GETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="e0161-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="e0161-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="e0161-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0161-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0161-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0161-112">Return Value</span></span>

<span data-ttu-id="e0161-113">Gibt eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur zurück, die die x-Koordinate und die y-Koordinate der Statusfenster Position in Bildschirm Koordinaten relativ zur oberen linken Ecke des Bildschirms enthält.</span><span class="sxs-lookup"><span data-stu-id="e0161-113">Returns a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x coordinate and y coordinate of the status window position in screen coordinates, relative to the upper left corner of the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0161-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0161-114">Requirements</span></span>



| <span data-ttu-id="e0161-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0161-115">Requirement</span></span> | <span data-ttu-id="e0161-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e0161-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0161-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0161-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e0161-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0161-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e0161-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0161-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e0161-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0161-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e0161-121">Header</span><span class="sxs-lookup"><span data-stu-id="e0161-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0161-122"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0161-122"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0161-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0161-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0161-124">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="e0161-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="e0161-125">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="e0161-125">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="e0161-126">**WM \_ IME- \_ Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="e0161-126">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
