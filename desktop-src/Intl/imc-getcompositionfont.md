---
description: Weist ein IME-Fenster an, die logische Schriftart zum Anzeigen von zwischen Zeichen im Kompositionsfenster abzurufen. Um diesen Befehl zu senden, verwendet die Anwendung die WM- \_ IME- \_ Steuerungs Meldung mit den unten gezeigten Parametereinstellungen.
ms.assetid: 43db70b6-f8bc-4241-9096-5d91fd1e332b
title: IMC_GETCOMPOSITIONFONT Befehl (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696d9809cadbe4f2c0e632719401e882777888dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214762"
---
# <a name="imc_getcompositionfont-command"></a><span data-ttu-id="18a05-104">IMC \_ getcompositionfont-Befehl</span><span class="sxs-lookup"><span data-stu-id="18a05-104">IMC\_GETCOMPOSITIONFONT command</span></span>

<span data-ttu-id="18a05-105">Weist ein IME-Fenster an, die logische Schriftart zum Anzeigen von zwischen Zeichen im Kompositionsfenster abzurufen.</span><span class="sxs-lookup"><span data-stu-id="18a05-105">Instructs an IME window to retrieve the logical font used for displaying intermediate characters in the composition window.</span></span> <span data-ttu-id="18a05-106">Um diesen Befehl zu senden, verwendet die Anwendung die [**WM- \_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung mit den unten gezeigten Parametereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="18a05-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="18a05-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="18a05-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18a05-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="18a05-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="18a05-109">Legen Sie auf "IMC \_ getcompositionfont" fest.</span><span class="sxs-lookup"><span data-stu-id="18a05-109">Set to IMC\_GETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="18a05-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="18a05-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="18a05-111">Ein Zeiger auf eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur, die Informationen über die logische Schriftart empfängt.</span><span class="sxs-lookup"><span data-stu-id="18a05-111">Pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that receives information about the logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18a05-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18a05-112">Return Value</span></span>

<span data-ttu-id="18a05-113">Gibt bei Erfolg 0 zurück oder andernfalls einen Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="18a05-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="18a05-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18a05-114">Requirements</span></span>



| <span data-ttu-id="18a05-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18a05-115">Requirement</span></span> | <span data-ttu-id="18a05-116">Wert</span><span class="sxs-lookup"><span data-stu-id="18a05-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18a05-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18a05-117">Minimum supported client</span></span><br/> | <span data-ttu-id="18a05-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18a05-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="18a05-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18a05-119">Minimum supported server</span></span><br/> | <span data-ttu-id="18a05-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18a05-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="18a05-121">Header</span><span class="sxs-lookup"><span data-stu-id="18a05-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="18a05-122"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18a05-122"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18a05-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18a05-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18a05-124">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="18a05-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="18a05-125">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="18a05-125">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> </dl>

 

 
