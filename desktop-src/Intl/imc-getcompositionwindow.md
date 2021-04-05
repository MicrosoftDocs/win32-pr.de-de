---
description: Weist ein IME-Fenster an, die Position des Kompositions Fensters zu erhalten. Um diesen Befehl zu senden, verwendet die Anwendung die WM- \_ IME- \_ Steuerungs Meldung mit den unten gezeigten Parametereinstellungen.
ms.assetid: d2c60974-a602-4a42-8a45-870ee39df001
title: IMC_GETCOMPOSITIONWINDOW Befehl (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b32b8f4414311d0727f622a1b552428cd31b0716
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752344"
---
# <a name="imc_getcompositionwindow-command"></a><span data-ttu-id="6bfc2-104">IMC \_ getcompositionwindow-Befehl</span><span class="sxs-lookup"><span data-stu-id="6bfc2-104">IMC\_GETCOMPOSITIONWINDOW command</span></span>

<span data-ttu-id="6bfc2-105">Weist ein IME-Fenster an, die Position des Kompositions Fensters zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6bfc2-105">Instructs an IME window to get the position of the composition window.</span></span> <span data-ttu-id="6bfc2-106">Um diesen Befehl zu senden, verwendet die Anwendung die [**WM- \_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung mit den unten gezeigten Parametereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="6bfc2-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="6bfc2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6bfc2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bfc2-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="6bfc2-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="6bfc2-109">Legen Sie auf "IMC \_ getcompositionwindow" fest.</span><span class="sxs-lookup"><span data-stu-id="6bfc2-109">Set to IMC\_GETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="6bfc2-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="6bfc2-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="6bfc2-111">Ein Zeiger auf eine [**compositionform**](/windows/win32/api/imm/ns-imm-compositionform) -Struktur, die die Position des Kompositions Fensters enthält.</span><span class="sxs-lookup"><span data-stu-id="6bfc2-111">Pointer to a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure that contains the position of the composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bfc2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6bfc2-112">Return Value</span></span>

<span data-ttu-id="6bfc2-113">Gibt bei Erfolg 0 zurück oder andernfalls einen Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6bfc2-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bfc2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6bfc2-114">Remarks</span></span>

<span data-ttu-id="6bfc2-115">Da der IME die Position eines Kompositions Fensters anpassen kann, verwendet eine Anwendung diesen Befehl, um die tatsächliche Position zu ermitteln, um zu entscheiden, ob das Fenster neu positioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6bfc2-115">Because the IME might adjust the position of a composition window, an application uses this command to get the actual position to decide whether to reposition the window.</span></span> <span data-ttu-id="6bfc2-116">Die abgerufene Position befindet sich in Fenster Koordinaten relativ zu dem Fenster, das den aktuellen Eingabefokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="6bfc2-116">The retrieved position is in window coordinates relative to the window having the current input focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bfc2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bfc2-117">Requirements</span></span>



| <span data-ttu-id="6bfc2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6bfc2-118">Requirement</span></span> | <span data-ttu-id="6bfc2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6bfc2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bfc2-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6bfc2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6bfc2-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bfc2-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6bfc2-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6bfc2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6bfc2-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bfc2-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6bfc2-124">Header</span><span class="sxs-lookup"><span data-stu-id="6bfc2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bfc2-125"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6bfc2-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bfc2-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6bfc2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bfc2-127">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="6bfc2-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="6bfc2-128">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="6bfc2-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="6bfc2-129">**Compositionform**</span><span class="sxs-lookup"><span data-stu-id="6bfc2-129">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> </dl>

 

 




