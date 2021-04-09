---
description: Weist ein IME-Fenster an, die logische Schriftart anzugeben, die zum Anzeigen von zwischen Zeichen im Kompositionsfenster verwendet werden soll. Um diesen Befehl zu senden, verwendet die Anwendung die WM- \_ IME- \_ Steuerungs Meldung mit den unten gezeigten Parametereinstellungen.
ms.assetid: 17b222e7-bf57-4cdd-8475-d9a8be03ab7f
title: IMC_SETCOMPOSITIONFONT Befehl (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb84c9e05ab19206064988a71b0ffc39b21a44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862923"
---
# <a name="imc_setcompositionfont-command"></a><span data-ttu-id="2d208-104">Befehl "IMC \_ setcompositionfont"</span><span class="sxs-lookup"><span data-stu-id="2d208-104">IMC\_SETCOMPOSITIONFONT command</span></span>

<span data-ttu-id="2d208-105">Weist ein IME-Fenster an, die logische Schriftart anzugeben, die zum Anzeigen von zwischen Zeichen im Kompositionsfenster verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d208-105">Instructs an IME window to specify the logical font to use for displaying intermediate characters in the composition window.</span></span> <span data-ttu-id="2d208-106">Um diesen Befehl zu senden, verwendet die Anwendung die [**WM- \_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung mit den unten gezeigten Parametereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="2d208-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="2d208-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d208-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d208-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d208-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="2d208-109">Legen Sie auf IMC \_ setcompositionfont fest.</span><span class="sxs-lookup"><span data-stu-id="2d208-109">Set to IMC\_SETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="2d208-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="2d208-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="2d208-111">Zeiger auf eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur, die Informationen über die logische Schriftart enthält.</span><span class="sxs-lookup"><span data-stu-id="2d208-111">Pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that contains information about the logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d208-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d208-112">Return Value</span></span>

<span data-ttu-id="2d208-113">Gibt bei Erfolg 0 zurück oder andernfalls einen Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2d208-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d208-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d208-114">Remarks</span></span>

<span data-ttu-id="2d208-115">Beim Verarbeiten dieses Befehls ändert das IME-Fenster die aktuell ausgewählte Schriftart im Eingabe Kontext.</span><span class="sxs-lookup"><span data-stu-id="2d208-115">When processing this command, the IME window changes the current selected font in the input context.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d208-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d208-116">Requirements</span></span>



| <span data-ttu-id="2d208-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d208-117">Requirement</span></span> | <span data-ttu-id="2d208-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2d208-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d208-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d208-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2d208-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d208-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2d208-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d208-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2d208-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d208-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2d208-123">Header</span><span class="sxs-lookup"><span data-stu-id="2d208-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d208-124"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d208-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d208-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d208-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d208-126">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="2d208-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="2d208-127">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="2d208-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="2d208-128">**WM \_ IME- \_ Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="2d208-128">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
