---
description: Weist ein IME-Fenster an, den Stil des Kompositions Fensters festzulegen. Um diesen Befehl zu senden, verwendet die Anwendung die WM- \_ IME- \_ Steuerungs Meldung mit den unten gezeigten Parametereinstellungen.
ms.assetid: 19b99228-a1fc-4cd5-8f37-5462bf767f85
title: IMC_SETCOMPOSITIONWINDOW Befehl (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b06c53b1ff2ec343d6382dd48d0d4108cf403c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345142"
---
# <a name="imc_setcompositionwindow-command"></a><span data-ttu-id="bda30-104">IMC \_ setcompositionwindow-Befehl</span><span class="sxs-lookup"><span data-stu-id="bda30-104">IMC\_SETCOMPOSITIONWINDOW command</span></span>

<span data-ttu-id="bda30-105">Weist ein IME-Fenster an, den Stil des Kompositions Fensters festzulegen.</span><span class="sxs-lookup"><span data-stu-id="bda30-105">Instructs an IME window to set the style of the composition window.</span></span> <span data-ttu-id="bda30-106">Um diesen Befehl zu senden, verwendet die Anwendung die [**WM- \_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung mit den unten gezeigten Parametereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="bda30-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="bda30-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bda30-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bda30-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="bda30-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="bda30-109">Legen Sie auf IMC \_ setcompositionwindow fest.</span><span class="sxs-lookup"><span data-stu-id="bda30-109">Set to IMC\_SETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="bda30-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="bda30-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="bda30-111">Zeiger auf eine [**compositionform**](/windows/win32/api/imm/ns-imm-compositionform) -Struktur, die die Stil Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="bda30-111">Pointer to a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure that contains the style information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bda30-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bda30-112">Return Value</span></span>

<span data-ttu-id="bda30-113">Gibt bei Erfolg 0 zurück oder andernfalls einen Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="bda30-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bda30-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bda30-114">Remarks</span></span>

<span data-ttu-id="bda30-115">Mit diesem Befehl wird der Stil im aktuellen Eingabe Kontext festgelegt, und anschließend wird der Stil auf jedes IME-Fenster angewendet, das diesen Eingabe Kontext empfängt.</span><span class="sxs-lookup"><span data-stu-id="bda30-115">This command sets the style in the current input context, and the style is subsequently applied to each IME window that receives that input context.</span></span>

<span data-ttu-id="bda30-116">Standardmäßig verfügt das IME-Fenster über die Art des CFS- \_ Punkts.</span><span class="sxs-lookup"><span data-stu-id="bda30-116">By default, the IME window has the CFS\_POINT style.</span></span> <span data-ttu-id="bda30-117">Bei diesem Stil verwendet das IME-Fenster die aktuelle Position der Einfügemarke und den Fenster Client Bereich, wenn ein Kompositionsfenster geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="bda30-117">With this style, the IME window uses the current caret position and window client area when it opens any composition window.</span></span>

## <a name="requirements"></a><span data-ttu-id="bda30-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bda30-118">Requirements</span></span>



| <span data-ttu-id="bda30-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bda30-119">Requirement</span></span> | <span data-ttu-id="bda30-120">Wert</span><span class="sxs-lookup"><span data-stu-id="bda30-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bda30-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bda30-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bda30-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bda30-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bda30-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bda30-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bda30-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bda30-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bda30-125">Header</span><span class="sxs-lookup"><span data-stu-id="bda30-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bda30-126"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bda30-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bda30-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bda30-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bda30-128">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="bda30-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="bda30-129">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="bda30-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="bda30-130">**Compositionform**</span><span class="sxs-lookup"><span data-stu-id="bda30-130">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[<span data-ttu-id="bda30-131">**WM \_ IME- \_ Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="bda30-131">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




