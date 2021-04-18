---
UID: ''
title: Shellproc-Rückruffunktion
description: Die Funktion empfängt Benachrichtigungen von shellereignissen vom System.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 4add84011745aeb61659c39775b94fed91028d83
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2020
ms.locfileid: "106341295"
---
# <a name="shellproc-function"></a><span data-ttu-id="b901a-103">Shellproc-Funktion</span><span class="sxs-lookup"><span data-stu-id="b901a-103">ShellProc function</span></span>

## <a name="description"></a><span data-ttu-id="b901a-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b901a-104">Description</span></span>

<span data-ttu-id="b901a-105">Eine von der Anwendung definierte oder Bibliotheks definierte Rückruffunktion, die mit der [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b901a-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="b901a-106">Die Funktion empfängt Benachrichtigungen von shellereignissen vom System.</span><span class="sxs-lookup"><span data-stu-id="b901a-106">The function receives notifications of Shell events from the system.</span></span>

<span data-ttu-id="b901a-107">Der **HookProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="b901a-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="b901a-108">**Shellproc** ist ein Platzhalter für den Anwendungs definierten oder Bibliotheks definierten Funktionsnamen.</span><span class="sxs-lookup"><span data-stu-id="b901a-108">**ShellProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK ShellProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="b901a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b901a-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="b901a-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="b901a-110">nCode [in]</span></span>

<span data-ttu-id="b901a-111">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="b901a-111">Type: **int**</span></span>

<span data-ttu-id="b901a-112">Der Hook-Code.</span><span class="sxs-lookup"><span data-stu-id="b901a-112">The hook code.</span></span>
<span data-ttu-id="b901a-113">Wenn *nCode* kleiner als 0 (null) ist, muss die Hook-Prozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b901a-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="b901a-114">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="b901a-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="b901a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b901a-115">Value</span></span> | <span data-ttu-id="b901a-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b901a-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="b901a-117">**HSHELL_ACCESSIBILITYSTATE** 11</span><span class="sxs-lookup"><span data-stu-id="b901a-117">**HSHELL_ACCESSIBILITYSTATE** 11</span></span> | <span data-ttu-id="b901a-118">Der Barrierefreiheits Zustand hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="b901a-118">The accessibility state has changed.</span></span> |
| <span data-ttu-id="b901a-119">**HSHELL_ACTIVATESHELLWINDOW** 3</span><span class="sxs-lookup"><span data-stu-id="b901a-119">**HSHELL_ACTIVATESHELLWINDOW** 3</span></span> | <span data-ttu-id="b901a-120">Das Hauptfenster muss von der Shell aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="b901a-120">The shell should activate its main window.</span></span> |
| <span data-ttu-id="b901a-121">**HSHELL_APPCOMMAND** 12</span><span class="sxs-lookup"><span data-stu-id="b901a-121">**HSHELL_APPCOMMAND** 12</span></span> | <span data-ttu-id="b901a-122">Der Benutzer hat ein Eingabe Ereignis abgeschlossen (z. b. eine Anwendungs Befehlsschaltfläche auf der Maus oder eine Anwendungs Befehlstaste auf der Tastatur gedrückt), und die Anwendung hat die von dieser Eingabe generierte [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) Nachricht nicht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b901a-122">The user completed an input event (for example, pressed an application command button on the mouse or an application command key on the keyboard), and the application did not handle the [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) message generated by that input.</span></span> <span data-ttu-id="b901a-123">Wenn die shellprozedur die [WM_COMMAND](/windows/desktop/menurc/wm-command) Nachricht behandelt, sollte Sie **CallNextHookEx** nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b901a-123">If the Shell procedure handles the [WM_COMMAND](/windows/desktop/menurc/wm-command) message, it should not call **CallNextHookEx**.</span></span> <span data-ttu-id="b901a-124">Weitere Informationen finden Sie im Abschnitt "Rückgabewert".</span><span class="sxs-lookup"><span data-stu-id="b901a-124">See the Return Value section for more information.</span></span> |
| <span data-ttu-id="b901a-125">**HSHELL_GETMINRECT** 5</span><span class="sxs-lookup"><span data-stu-id="b901a-125">**HSHELL_GETMINRECT** 5</span></span> | <span data-ttu-id="b901a-126">Ein Fenster wird minimiert oder maximiert.</span><span class="sxs-lookup"><span data-stu-id="b901a-126">A window is being minimized or maximized.</span></span> <span data-ttu-id="b901a-127">Das System benötigt die Koordinaten des minimierten Rechtecks für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="b901a-127">The system needs the coordinates of the minimized rectangle for the window.</span></span> |
| <span data-ttu-id="b901a-128">**HSHELL_LANGUAGE** 8</span><span class="sxs-lookup"><span data-stu-id="b901a-128">**HSHELL_LANGUAGE** 8</span></span> | <span data-ttu-id="b901a-129">Die Tastatur Sprache wurde geändert, oder ein neues Tastaturlayout wurde geladen.</span><span class="sxs-lookup"><span data-stu-id="b901a-129">Keyboard language was changed or a new keyboard layout was loaded.</span></span> |
| <span data-ttu-id="b901a-130">**HSHELL_REDRAW** 6</span><span class="sxs-lookup"><span data-stu-id="b901a-130">**HSHELL_REDRAW** 6</span></span> | <span data-ttu-id="b901a-131">Der Titel eines Fensters in der Taskleiste wurde neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b901a-131">The title of a window in the task bar has been redrawn.</span></span> |
| <span data-ttu-id="b901a-132">**HSHELL_TASKMAN** 7</span><span class="sxs-lookup"><span data-stu-id="b901a-132">**HSHELL_TASKMAN** 7</span></span> | <span data-ttu-id="b901a-133">Der Benutzer hat die Aufgabenliste ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="b901a-133">The user has selected the task list.</span></span> <span data-ttu-id="b901a-134">Eine Shellanwendung, die eine Aufgabenliste bereitstellt, sollte **true** zurückgeben, um zu verhindern, dass Windows Ihre Aufgabenliste startet.</span><span class="sxs-lookup"><span data-stu-id="b901a-134">A shell application that provides a task list should return **TRUE** to prevent Windows from starting its task list.</span></span> |
| <span data-ttu-id="b901a-135">**HSHELL_WINDOWACTIVATED** 4</span><span class="sxs-lookup"><span data-stu-id="b901a-135">**HSHELL_WINDOWACTIVATED** 4</span></span> | <span data-ttu-id="b901a-136">Die Aktivierung wurde in ein anderes Fenster der obersten Ebene (nicht im Besitz) geändert.</span><span class="sxs-lookup"><span data-stu-id="b901a-136">The activation has changed to a different top-level, unowned window.</span></span> |
| <span data-ttu-id="b901a-137">**HSHELL_WINDOWCREATED** 1</span><span class="sxs-lookup"><span data-stu-id="b901a-137">**HSHELL_WINDOWCREATED** 1</span></span> | <span data-ttu-id="b901a-138">Es wurde ein nicht eigenes Fenster der obersten Ebene erstellt.</span><span class="sxs-lookup"><span data-stu-id="b901a-138">A top-level, unowned window has been created.</span></span> <span data-ttu-id="b901a-139">Das Fenster ist vorhanden, wenn das System diesen Hook aufruft.</span><span class="sxs-lookup"><span data-stu-id="b901a-139">The window exists when the system calls this hook.</span></span> |
| <span data-ttu-id="b901a-140">**HSHELL_WINDOWDESTROYED** 2</span><span class="sxs-lookup"><span data-stu-id="b901a-140">**HSHELL_WINDOWDESTROYED** 2</span></span> | <span data-ttu-id="b901a-141">Ein Fenster der obersten Ebene, das nicht im Besitz ist, wird zerstört.</span><span class="sxs-lookup"><span data-stu-id="b901a-141">A top-level, unowned window is about to be destroyed.</span></span> <span data-ttu-id="b901a-142">Das Fenster ist weiterhin vorhanden, wenn das System diesen Hook aufruft.</span><span class="sxs-lookup"><span data-stu-id="b901a-142">The window still exists when the system calls this hook.</span></span> |
| <span data-ttu-id="b901a-143">**HSHELL_WINDOWREPLACED** 13</span><span class="sxs-lookup"><span data-stu-id="b901a-143">**HSHELL_WINDOWREPLACED** 13</span></span> | <span data-ttu-id="b901a-144">Ein Fenster der obersten Ebene wird ersetzt.</span><span class="sxs-lookup"><span data-stu-id="b901a-144">A top-level window is being replaced.</span></span> <span data-ttu-id="b901a-145">Das Fenster ist vorhanden, wenn das System diesen Hook aufruft.</span><span class="sxs-lookup"><span data-stu-id="b901a-145">The window exists when the system calls this hook.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="b901a-146">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="b901a-146">wParam [in]</span></span>

<span data-ttu-id="b901a-147">Typ: **wParam**</span><span class="sxs-lookup"><span data-stu-id="b901a-147">Type: **WPARAM**</span></span>

<span data-ttu-id="b901a-148">Dieser Parameter hängt vom Wert des *nCode* -Parameters ab, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b901a-148">This parameter depends on the value of the *nCode* parameter, as shown in the following table.</span></span>

| <span data-ttu-id="b901a-149">nCode</span><span class="sxs-lookup"><span data-stu-id="b901a-149">nCode</span></span> | <span data-ttu-id="b901a-150">wParam</span><span class="sxs-lookup"><span data-stu-id="b901a-150">wParam</span></span> |
|-------|---------|
| <span data-ttu-id="b901a-151">**HSHELL_ACCESSIBILITYSTATE**</span><span class="sxs-lookup"><span data-stu-id="b901a-151">**HSHELL_ACCESSIBILITYSTATE**</span></span> | <span data-ttu-id="b901a-152">Gibt an, welche Barrierefreiheits Funktion den Zustand geändert hat.</span><span class="sxs-lookup"><span data-stu-id="b901a-152">Indicates which accessibility feature has changed state.</span></span> <span data-ttu-id="b901a-153">Dieser Wert ist einer der folgenden Werte: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS** oder **ACCESS_STICKYKEYS**.</span><span class="sxs-lookup"><span data-stu-id="b901a-153">This value is one of the following: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS**, or **ACCESS_STICKYKEYS**.</span></span> |
| <span data-ttu-id="b901a-154">**HSHELL_APPCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="b901a-154">**HSHELL_APPCOMMAND**</span></span> | <span data-ttu-id="b901a-155">Gibt an, an welcher Stelle die **WM_APPCOMMAND** Nachricht ursprünglich gesendet wurde. beispielsweise das Handle für ein Fenster.</span><span class="sxs-lookup"><span data-stu-id="b901a-155">Indicates where the **WM_APPCOMMAND** message was originally sent; for example, the handle to a window.</span></span> <span data-ttu-id="b901a-156">Weitere Informationen finden Sie unter cmd-Parameter in **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="b901a-156">For more information, see cmd parameter in **WM_APPCOMMAND**.</span></span> |
| <span data-ttu-id="b901a-157">**HSHELL_GETMINRECT**</span><span class="sxs-lookup"><span data-stu-id="b901a-157">**HSHELL_GETMINRECT**</span></span> | <span data-ttu-id="b901a-158">Ein Handle für das minimierte oder maximierte Fenster.</span><span class="sxs-lookup"><span data-stu-id="b901a-158">A handle to the minimized or maximized window.</span></span> |
| <span data-ttu-id="b901a-159">**HSHELL_LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="b901a-159">**HSHELL_LANGUAGE**</span></span> | <span data-ttu-id="b901a-160">Ein Handle für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="b901a-160">A handle to the window.</span></span> |
| <span data-ttu-id="b901a-161">**HSHELL_REDRAW**</span><span class="sxs-lookup"><span data-stu-id="b901a-161">**HSHELL_REDRAW**</span></span> | <span data-ttu-id="b901a-162">Ein Handle für das neu erstellte Fenster.</span><span class="sxs-lookup"><span data-stu-id="b901a-162">A handle to the redrawn window.</span></span> |
| <span data-ttu-id="b901a-163">**HSHELL_WINDOWACTIVATED**</span><span class="sxs-lookup"><span data-stu-id="b901a-163">**HSHELL_WINDOWACTIVATED**</span></span> | <span data-ttu-id="b901a-164">Ein Handle für das aktivierte Fenster.</span><span class="sxs-lookup"><span data-stu-id="b901a-164">A handle to the activated window.</span></span> |
| <span data-ttu-id="b901a-165">**HSHELL_WINDOWCREATED**</span><span class="sxs-lookup"><span data-stu-id="b901a-165">**HSHELL_WINDOWCREATED**</span></span> | <span data-ttu-id="b901a-166">Ein Handle für das erstellte Fenster.</span><span class="sxs-lookup"><span data-stu-id="b901a-166">A handle to the created window.</span></span> |
| <span data-ttu-id="b901a-167">**HSHELL_WINDOWDESTROYED**</span><span class="sxs-lookup"><span data-stu-id="b901a-167">**HSHELL_WINDOWDESTROYED**</span></span> | <span data-ttu-id="b901a-168">Ein Handle für das zerstörte Fenster.</span><span class="sxs-lookup"><span data-stu-id="b901a-168">A handle to the destroyed window.</span></span> |
| <span data-ttu-id="b901a-169">**HSHELL_WINDOWREPLACED**</span><span class="sxs-lookup"><span data-stu-id="b901a-169">**HSHELL_WINDOWREPLACED**</span></span> | <span data-ttu-id="b901a-170">Ein Handle für das Fenster, das ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b901a-170">A handle to the window being replaced.</span></span> <span data-ttu-id="b901a-171">Windows 2000: nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b901a-171">Windows 2000:  Not supported.</span></span> |

### <a name="lparam-in"></a><span data-ttu-id="b901a-172">LParam [in]</span><span class="sxs-lookup"><span data-stu-id="b901a-172">lParam [in]</span></span>

<span data-ttu-id="b901a-173">Typ: **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="b901a-173">Type: **LPARAM**</span></span>

<span data-ttu-id="b901a-174">Dieser Parameter hängt vom Wert des *nCode* -Parameters ab, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b901a-174">This parameter depends on the value of the *nCode* parameter, as shown in the following table.</span></span>

| <span data-ttu-id="b901a-175">nCode</span><span class="sxs-lookup"><span data-stu-id="b901a-175">nCode</span></span> | <span data-ttu-id="b901a-176">lParam</span><span class="sxs-lookup"><span data-stu-id="b901a-176">lParam</span></span> |
|-------|---------|
| <span data-ttu-id="b901a-177">**HSHELL_APPCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="b901a-177">**HSHELL_APPCOMMAND**</span></span> | <span data-ttu-id="b901a-178">`GET_APPCOMMAND_LPARAM(lParam)` der Anwendungs Befehl, der dem Eingabe Ereignis entspricht.</span><span class="sxs-lookup"><span data-stu-id="b901a-178">`GET_APPCOMMAND_LPARAM(lParam)` is the application command corresponding to the input event.</span></span> <span data-ttu-id="b901a-179">`GET_DEVICE_LPARAM(lParam)` Gibt an, was das Eingabe Ereignis generiert hat. beispielsweise die Maus oder die Tastatur.</span><span class="sxs-lookup"><span data-stu-id="b901a-179">`GET_DEVICE_LPARAM(lParam)` indicates what generated the input event; for example, the mouse or keyboard.</span></span> <span data-ttu-id="b901a-180">Weitere Informationen finden Sie in der Beschreibung des Parameters " *udevice* " unter **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="b901a-180">For more information, see the *uDevice* parameter description under **WM_APPCOMMAND**.</span></span> <span data-ttu-id="b901a-181">`GET_FLAGS_LPARAM(lParam)` hängt vom Wert von *cmd* in **WM_APPCOMMAND** ab.</span><span class="sxs-lookup"><span data-stu-id="b901a-181">`GET_FLAGS_LPARAM(lParam)` depends on the value of *cmd* in **WM_APPCOMMAND**.</span></span> <span data-ttu-id="b901a-182">So kann beispielsweise angegeben werden, welche virtuellen Schlüssel beim ursprünglichen Senden der **WM_APPCOMMAND** Nachricht gedrückt gehalten wurden.</span><span class="sxs-lookup"><span data-stu-id="b901a-182">For example, it might indicate which virtual keys were held down when the **WM_APPCOMMAND** message was originally sent.</span></span> <span data-ttu-id="b901a-183">Weitere Informationen finden Sie unter dem Parameter " *dwcmdflags* Description" unter **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="b901a-183">For more information, see the *dwCmdFlags* description parameter under **WM_APPCOMMAND**.</span></span> |
| <span data-ttu-id="b901a-184">**HSHELL_GETMINRECT**</span><span class="sxs-lookup"><span data-stu-id="b901a-184">**HSHELL_GETMINRECT**</span></span> | <span data-ttu-id="b901a-185">Ein Zeiger auf eine [Rect](/previous-versions/dd162897(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b901a-185">A pointer to a [RECT](/previous-versions/dd162897(v=vs.85)) structure.</span></span> |
| <span data-ttu-id="b901a-186">**HSHELL_LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="b901a-186">**HSHELL_LANGUAGE**</span></span> | <span data-ttu-id="b901a-187">Ein Handle für ein Tastaturlayout.</span><span class="sxs-lookup"><span data-stu-id="b901a-187">A handle to a keyboard layout.</span></span> |
| <span data-ttu-id="b901a-188">**HSHELL_MONITORCHANGED**</span><span class="sxs-lookup"><span data-stu-id="b901a-188">**HSHELL_MONITORCHANGED**</span></span> | <span data-ttu-id="b901a-189">Ein Handle für das Fenster, das auf einen anderen Monitor verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="b901a-189">A handle to the window that moved to a different monitor.</span></span> |
| <span data-ttu-id="b901a-190">**HSHELL_REDRAW**</span><span class="sxs-lookup"><span data-stu-id="b901a-190">**HSHELL_REDRAW**</span></span> | <span data-ttu-id="b901a-191">Der Wert ist " **true** ", wenn das Fenster blinkt, andernfalls " **false** ".</span><span class="sxs-lookup"><span data-stu-id="b901a-191">The value is **TRUE** if the window is flashing, or **FALSE** otherwise.</span></span> |
| <span data-ttu-id="b901a-192">**HSHELL_WINDOWACTIVATED**</span><span class="sxs-lookup"><span data-stu-id="b901a-192">**HSHELL_WINDOWACTIVATED**</span></span> | <span data-ttu-id="b901a-193">Der Wert ist "true", wenn sich das Fenster im Vollbildmodus befindet, andernfalls " **false** ".</span><span class="sxs-lookup"><span data-stu-id="b901a-193">The value is TRUE if the window is in full-screen mode, or **FALSE** otherwise.</span></span> |
| <span data-ttu-id="b901a-194">**HSHELL_WINDOWREPLACED**</span><span class="sxs-lookup"><span data-stu-id="b901a-194">**HSHELL_WINDOWREPLACED**</span></span> | <span data-ttu-id="b901a-195">Ein Handle für das neue Fenster.</span><span class="sxs-lookup"><span data-stu-id="b901a-195">A handle to the new window.</span></span> <span data-ttu-id="b901a-196">Windows 2000: nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b901a-196">Windows 2000:  Not supported.</span></span> |

## <a name="returns"></a><span data-ttu-id="b901a-197">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="b901a-197">Returns</span></span>

<span data-ttu-id="b901a-198">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="b901a-198">Type: **LRESULT**</span></span>

<span data-ttu-id="b901a-199">Der Rückgabewert sollte NULL sein, es sei denn, der Wert von nCode ist **HSHELL_APPCOMMAND** , und die shellprozedur verarbeitet die **WM_COMMAND** -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b901a-199">The return value should be zero unless the value of nCode is **HSHELL_APPCOMMAND** and the shell procedure handles the **WM_COMMAND** message.</span></span>
<span data-ttu-id="b901a-200">In diesem Fall sollte die Rückgabe nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b901a-200">In this case, the return should be nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b901a-201">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b901a-201">Remarks</span></span>

<span data-ttu-id="b901a-202">Installieren Sie diese Hook-Prozedur, indem Sie den [WH_SHELL](about-hooks.md) Hooktyp und einen Zeiger auf die Hook-Prozedur in einem Aufrufen der **SetWindowsHookEx** -Funktion angeben.</span><span class="sxs-lookup"><span data-stu-id="b901a-202">Install this hook procedure by specifying the [WH_SHELL](about-hooks.md) hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="b901a-203">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b901a-203">See also</span></span>

[<span data-ttu-id="b901a-204">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="b901a-204">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="b901a-205">SendMessage</span><span class="sxs-lookup"><span data-stu-id="b901a-205">SendMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)

[<span data-ttu-id="b901a-206">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="b901a-206">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="b901a-207">WM_APPCOMMAND</span><span class="sxs-lookup"><span data-stu-id="b901a-207">WM_APPCOMMAND</span></span>](/windows/desktop/inputdev/wm-appcommand)

[<span data-ttu-id="b901a-208">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="b901a-208">WM_COMMAND</span></span>](/windows/desktop/menurc/wm-command)

[<span data-ttu-id="b901a-209">Hooks</span><span class="sxs-lookup"><span data-stu-id="b901a-209">Hooks</span></span>](hooks.md)
