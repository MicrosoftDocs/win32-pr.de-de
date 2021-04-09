---
description: Weist das IME-Fenster an, das Statusfenster anzuzeigen. Um diesen Befehl zu senden, verwendet die Anwendung die WM- \_ IME- \_ Steuerungs Meldung mit den unten gezeigten Parametereinstellungen.
ms.assetid: 8c422592-ef59-4030-b684-81e4e552c6b0
title: IMC_OPENSTATUSWINDOW Befehl (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd0b5e19ef6a026459eedb050e9ac9587b5ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862924"
---
# <a name="imc_openstatuswindow-command"></a><span data-ttu-id="7b783-104">Befehl "- \_ openstatus Window" von IMC</span><span class="sxs-lookup"><span data-stu-id="7b783-104">IMC\_OPENSTATUSWINDOW command</span></span>

<span data-ttu-id="7b783-105">Weist das IME-Fenster an, das Statusfenster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7b783-105">Instructs the IME window to show the status window.</span></span> <span data-ttu-id="7b783-106">Um diesen Befehl zu senden, verwendet die Anwendung die [**WM- \_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung mit den unten gezeigten Parametereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="7b783-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_OPENSTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="7b783-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b783-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b783-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="7b783-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="7b783-109">Legen Sie auf "IMC \_ openstatus Window" fest.</span><span class="sxs-lookup"><span data-stu-id="7b783-109">Set to IMC\_OPENSTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="7b783-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="7b783-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="7b783-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7b783-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b783-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b783-112">Return Value</span></span>

<span data-ttu-id="7b783-113">Gibt bei Erfolg 0 zurück oder andernfalls einen Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="7b783-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b783-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b783-114">Remarks</span></span>

<span data-ttu-id="7b783-115">Dieser Befehl wird ignoriert, wenn sich das Betriebssystem nicht im Modus "IME-Status anzeigen" befindet.</span><span class="sxs-lookup"><span data-stu-id="7b783-115">This command is ignored if the operating system is not in the show IME status mode.</span></span> <span data-ttu-id="7b783-116">Der Benutzer kann den IME-Status Modus anzeigen auf der Taskleiste festlegen oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="7b783-116">The user can set or clear the show IME status mode from the task bar.</span></span>

<span data-ttu-id="7b783-117">Wenn das Statusfenster bereits angezeigt wird, führt dieser Befehl nichts aus.</span><span class="sxs-lookup"><span data-stu-id="7b783-117">If the status window is already shown, this command does nothing.</span></span> <span data-ttu-id="7b783-118">Obwohl die Anwendung diesen Befehl an das IME-Fenster senden kann, empfängt die Anwendung nicht den entsprechenden [**IMN \_ openstatus Window**](imn-openstatuswindow.md) -Befehl.</span><span class="sxs-lookup"><span data-stu-id="7b783-118">Although the application can send this command to the IME window, the application does not receive the corresponding [**IMN\_OPENSTATUSWINDOW**](imn-openstatuswindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b783-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b783-119">Requirements</span></span>



| <span data-ttu-id="7b783-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b783-120">Requirement</span></span> | <span data-ttu-id="7b783-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7b783-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b783-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b783-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7b783-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b783-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7b783-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b783-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7b783-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b783-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7b783-126">Header</span><span class="sxs-lookup"><span data-stu-id="7b783-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b783-127"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b783-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b783-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b783-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b783-129">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="7b783-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="7b783-130">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="7b783-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="7b783-131">**WM \_ IME- \_ Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="7b783-131">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




