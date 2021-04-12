---
description: Eine Meldung, die an alle Fenster der obersten Ebene gesendet wird, wenn die SystemParametersInfo-Funktion eine systemweite Einstellung ändert oder wenn sich die Richtlinien Einstellungen geändert haben.
ms.assetid: 77174e06-a25b-440a-9e9c-4fd5979c433c
title: WM_SETTINGCHANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c3d1360b5e4cc5de2dbd23b09b8f2ad034948f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218211"
---
# <a name="wm_settingchange-message"></a><span data-ttu-id="bfdac-103">WM- \_ settingchange-Meldung</span><span class="sxs-lookup"><span data-stu-id="bfdac-103">WM\_SETTINGCHANGE message</span></span>

<span data-ttu-id="bfdac-104">Eine Meldung, die an alle Fenster der obersten Ebene gesendet wird, wenn die [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Funktion eine systemweite Einstellung ändert oder wenn sich die Richtlinien Einstellungen geändert haben.</span><span class="sxs-lookup"><span data-stu-id="bfdac-104">A message that is sent to all top-level windows when the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function changes a system-wide setting or when policy settings have changed.</span></span>

<span data-ttu-id="bfdac-105">Anwendungen sollten **WM \_ settingchange** an alle Fenster der obersten Ebene senden, wenn Sie Änderungen an den Systemparametern vornehmen.</span><span class="sxs-lookup"><span data-stu-id="bfdac-105">Applications should send **WM\_SETTINGCHANGE** to all top-level windows when they make changes to system parameters.</span></span> <span data-ttu-id="bfdac-106">(Diese Nachricht kann nicht direkt an ein Fenster gesendet werden.) Um die **WM- \_ settingchange** -Nachricht an alle Fenster der obersten Ebene zu senden, verwenden Sie die [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) -Funktion mit dem *HWND* -Parameter, der auf **HWND- \_ Broadcast** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bfdac-106">(This message cannot be sent directly to a window.) To send the **WM\_SETTINGCHANGE** message to all top-level windows, use the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function with the *hwnd* parameter set to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="bfdac-107">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="bfdac-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WININICHANGE                 0x001A
#define WM_SETTINGCHANGE                WM_WININICHANGE
```



## <a name="parameters"></a><span data-ttu-id="bfdac-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfdac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfdac-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bfdac-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfdac-110">Wenn das System diese Nachricht als Ergebnis eines [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Aufrufes sendet, ist der *wParam* -Parameter der Wert des *uiaction* -Parameters, der an die **SystemParametersInfo** -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="bfdac-110">When the system sends this message as a result of a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) call, the *wParam* parameter is the value of the *uiAction* parameter passed to the **SystemParametersInfo** function.</span></span> <span data-ttu-id="bfdac-111">Eine Liste der Werte finden Sie unter **SystemParametersInfo**.</span><span class="sxs-lookup"><span data-stu-id="bfdac-111">For a list of values, see **SystemParametersInfo**.</span></span>

<span data-ttu-id="bfdac-112">Wenn das System diese Nachricht aufgrund einer Änderung der Richtlinien Einstellungen sendet, gibt dieser Parameter den Typ der angewendeten Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="bfdac-112">When the system sends this message as a result of a change in policy settings, this parameter indicates the type of policy that was applied.</span></span> <span data-ttu-id="bfdac-113">Dieser Wert ist 1, wenn die Computer Richtlinie angewendet wurde, oder NULL, wenn die Benutzer Richtlinie angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="bfdac-113">This value is 1 if computer policy was applied or zero if user policy was applied.</span></span>

<span data-ttu-id="bfdac-114">Wenn das System diese Nachricht aufgrund einer Änderung der Gebiets Schema Einstellungen sendet, ist dieser Parameter 0 (null).</span><span class="sxs-lookup"><span data-stu-id="bfdac-114">When the system sends this message as a result of a change in locale settings, this parameter is zero.</span></span>

<span data-ttu-id="bfdac-115">Wenn eine Anwendung diese Nachricht sendet, muss dieser Parameter **null** sein.</span><span class="sxs-lookup"><span data-stu-id="bfdac-115">When an application sends this message, this parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bfdac-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfdac-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfdac-117">Wenn das System diese Nachricht als Ergebnis eines [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Aufrufes sendet, ist *LPARAM* ein Zeiger auf eine Zeichenfolge, die den Bereich angibt, der den geänderten Systemparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="bfdac-117">When the system sends this message as a result of a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) call, *lParam* is a pointer to a string that indicates the area containing the system parameter that was changed.</span></span> <span data-ttu-id="bfdac-118">Dieser Parameter gibt in der Regel nicht an, welcher spezifische Systemparameter geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="bfdac-118">This parameter does not usually indicate which specific system parameter changed.</span></span> <span data-ttu-id="bfdac-119">(Beachten Sie, dass einige Anwendungen diese Nachricht senden, wobei *LPARAM* auf **null** festgelegt ist.) Wenn Sie diese Meldung erhalten, sollten Sie im Allgemeinen alle Systemparameter Einstellungen überprüfen und erneut laden, die von der Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfdac-119">(Note that some applications send this message with *lParam* set to **NULL**.) In general, when you receive this message, you should check and reload any system parameter settings that are used by your application.</span></span>

<span data-ttu-id="bfdac-120">Diese Zeichenfolge kann der Name eines Registrierungsschlüssels oder der Name eines Abschnitts in der Win.ini-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="bfdac-120">This string can be the name of a registry key or the name of a section in the Win.ini file.</span></span> <span data-ttu-id="bfdac-121">Wenn die Zeichenfolge ein Registrierungs Name ist, gibt Sie in der Regel nur den Endknoten in der Registrierung an, nicht den vollständigen Pfad.</span><span class="sxs-lookup"><span data-stu-id="bfdac-121">When the string is a registry name, it typically indicates only the leaf node in the registry, not the full path.</span></span>

<span data-ttu-id="bfdac-122">Wenn das System diese Nachricht aufgrund einer Änderung der Richtlinien Einstellungen sendet, verweist dieser Parameter auf die Zeichenfolge "Policy".</span><span class="sxs-lookup"><span data-stu-id="bfdac-122">When the system sends this message as a result of a change in policy settings, this parameter points to the string "Policy".</span></span>

<span data-ttu-id="bfdac-123">Wenn das System diese Nachricht aufgrund einer Änderung der Gebiets Schema Einstellungen sendet, verweist dieser Parameter auf die Zeichenfolge "Intl".</span><span class="sxs-lookup"><span data-stu-id="bfdac-123">When the system sends this message as a result of a change in locale settings, this parameter points to the string "intl".</span></span>

<span data-ttu-id="bfdac-124">Um eine Änderung in den Umgebungsvariablen für das System oder den Benutzer zu beeinflussen, senden Sie diese Meldung mit *LPARAM* , die auf die Zeichenfolge "Environment" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bfdac-124">To effect a change in the environment variables for the system or the user, broadcast this message with *lParam* set to the string "Environment".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfdac-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bfdac-125">Return value</span></span>

<span data-ttu-id="bfdac-126">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="bfdac-126">Type: **LRESULT**</span></span>

<span data-ttu-id="bfdac-127">Wenn Sie diese Meldung verarbeiten, wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bfdac-127">If you process this message, return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfdac-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfdac-128">Remarks</span></span>

<span data-ttu-id="bfdac-129">Der *LPARAM* -Parameter gibt an, welche Systemmetrik sich geändert hat, z. b. "cabriblelockemode", wenn der "konvertierte Indikator" geändert wurde, oder "systemdockmode", wenn der angedockte Indikator umgeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="bfdac-129">The *lParam* parameter indicates which system metric has changed, for example, "ConvertibleSlateMode" if the CONVERTIBLESLATEMODE indicator was toggled or "SystemDockMode" if the DOCKED indicator was toggled.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfdac-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfdac-130">Requirements</span></span>



| <span data-ttu-id="bfdac-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfdac-131">Requirement</span></span> | <span data-ttu-id="bfdac-132">Wert</span><span class="sxs-lookup"><span data-stu-id="bfdac-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfdac-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfdac-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bfdac-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfdac-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bfdac-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfdac-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bfdac-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfdac-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bfdac-137">Header</span><span class="sxs-lookup"><span data-stu-id="bfdac-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfdac-138"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="bfdac-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfdac-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfdac-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfdac-140">Richtlinien Ereignisse</span><span class="sxs-lookup"><span data-stu-id="bfdac-140">Policy Events</span></span>](/previous-versions/windows/desktop/Policy/policy-events)
</dt> <dt>

[<span data-ttu-id="bfdac-141">**Von SendMessageTimeout**</span><span class="sxs-lookup"><span data-stu-id="bfdac-141">**SendMessageTimeout**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
</dt> <dt>

[<span data-ttu-id="bfdac-142">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="bfdac-142">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
