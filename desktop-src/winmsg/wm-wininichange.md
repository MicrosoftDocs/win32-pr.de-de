---
description: Eine Anwendung sendet die WM- \_ wininichange-Nachricht an alle Fenster der obersten Ebene, nachdem eine Änderung an der WIN.INI Datei vorgenommen wurde. Die SystemParametersInfo-Funktion sendet diese Nachricht, nachdem eine Anwendung die-Funktion verwendet hat, um eine Einstellung in WIN.INI zu ändern.
ms.assetid: 402f8d71-ad52-486d-be26-8b41a3f22045
title: WM_WININICHANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b8db6c4794a8c1a572f61028d32eaeaf578d0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958893"
---
# <a name="wm_wininichange-message"></a><span data-ttu-id="80482-104">WM- \_ wininichange-Meldung</span><span class="sxs-lookup"><span data-stu-id="80482-104">WM\_WININICHANGE message</span></span>

<span data-ttu-id="80482-105">Eine Anwendung sendet die **WM- \_ wininichange** -Nachricht an alle Fenster der obersten Ebene, nachdem eine Änderung an der WIN.INI Datei vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="80482-105">An application sends the **WM\_WININICHANGE** message to all top-level windows after making a change to the WIN.INI file.</span></span> <span data-ttu-id="80482-106">Die [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Funktion sendet diese Nachricht, nachdem eine Anwendung die-Funktion verwendet hat, um eine Einstellung in WIN.INI zu ändern.</span><span class="sxs-lookup"><span data-stu-id="80482-106">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function sends this message after an application uses the function to change a setting in WIN.INI.</span></span>

> [!Note]  
> <span data-ttu-id="80482-107">Die **WM- \_ wininichange** -Nachricht wird nur aus Gründen der Kompatibilität mit früheren Versionen des Systems bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="80482-107">The **WM\_WININICHANGE** message is provided only for compatibility with earlier versions of the system.</span></span> <span data-ttu-id="80482-108">Anwendungen sollten die " [**WM \_ settingchange**](wm-settingchange.md) "-Meldung verwenden.</span><span class="sxs-lookup"><span data-stu-id="80482-108">Applications should use the [**WM\_SETTINGCHANGE**](wm-settingchange.md) message.</span></span>

 

<span data-ttu-id="80482-109">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="80482-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WININICHANGE                 0x001A
```



## <a name="parameters"></a><span data-ttu-id="80482-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="80482-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80482-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="80482-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80482-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="80482-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="80482-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="80482-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80482-114">Ein Zeiger auf eine Zeichenfolge, die den Namen des geänderten System Parameters enthält.</span><span class="sxs-lookup"><span data-stu-id="80482-114">A pointer to a string containing the name of the system parameter that was changed.</span></span> <span data-ttu-id="80482-115">Diese Zeichenfolge kann z. b. der Name eines Registrierungsschlüssels oder der Name eines Abschnitts in der Win.ini-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="80482-115">For example, this string can be the name of a registry key or the name of a section in the Win.ini file.</span></span> <span data-ttu-id="80482-116">Dieser Parameter ist nicht besonders nützlich, um zu bestimmen, welcher Systemparameter geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="80482-116">This parameter is not particularly useful in determining which system parameter changed.</span></span> <span data-ttu-id="80482-117">Wenn die Zeichenfolge z. b. ein Registrierungs Name ist, gibt Sie in der Regel nur den Endknoten in der Registrierung und nicht den gesamten Pfad an.</span><span class="sxs-lookup"><span data-stu-id="80482-117">For example, when the string is a registry name, it typically indicates only the leaf node in the registry, not the whole path.</span></span> <span data-ttu-id="80482-118">Außerdem senden einige Anwendungen diese Nachricht, wobei *LPARAM* auf **null** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="80482-118">In addition, some applications send this message with *lParam* set to **NULL**.</span></span> <span data-ttu-id="80482-119">Wenn Sie diese Meldung erhalten, sollten Sie im Allgemeinen alle Systemparameter Einstellungen überprüfen und erneut laden, die von der Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="80482-119">In general, when you receive this message, you should check and reload any system parameter settings that are used by your application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80482-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80482-120">Return value</span></span>

<span data-ttu-id="80482-121">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="80482-121">Type: **LRESULT**</span></span>

<span data-ttu-id="80482-122">Wenn Sie diese Meldung verarbeiten, wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="80482-122">If you process this message, return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="80482-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80482-123">Remarks</span></span>

<span data-ttu-id="80482-124">Um die **WM- \_ wininichange** -Nachricht an alle Fenster der obersten Ebene zu senden, verwenden Sie die [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion mit dem *HWND* -Parameter, der auf **HWND- \_ Broadcast** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="80482-124">To send the **WM\_WININICHANGE** message to all top-level windows, use the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the *hWnd* parameter set to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="80482-125">Aufrufe von Funktionen, die WIN.INI ändern, können stattdessen der Registrierung zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="80482-125">Calls to functions that change WIN.INI may be mapped to the registry instead.</span></span> <span data-ttu-id="80482-126">Diese Zuordnung tritt auf, wenn WIN.INI und der Abschnitt, der geändert wird, in der Registrierung unter dem folgenden Schlüssel angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="80482-126">This mapping occurs when WIN.INI and the section being changed are specified in the registry under the following key:</span></span>

<span data-ttu-id="80482-127">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ IniFileMapping**</span><span class="sxs-lookup"><span data-stu-id="80482-127">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\IniFileMapping**</span></span>

<span data-ttu-id="80482-128">Die Änderung am Speicherort hat keine Auswirkung auf das Verhalten dieser Nachricht.</span><span class="sxs-lookup"><span data-stu-id="80482-128">The change in the storage location has no effect on the behavior of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="80482-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80482-129">Requirements</span></span>



| <span data-ttu-id="80482-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80482-130">Requirement</span></span> | <span data-ttu-id="80482-131">Wert</span><span class="sxs-lookup"><span data-stu-id="80482-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80482-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80482-132">Minimum supported client</span></span><br/> | <span data-ttu-id="80482-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80482-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="80482-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80482-134">Minimum supported server</span></span><br/> | <span data-ttu-id="80482-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80482-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="80482-136">Header</span><span class="sxs-lookup"><span data-stu-id="80482-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="80482-137"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="80482-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80482-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80482-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80482-139">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="80482-139">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
