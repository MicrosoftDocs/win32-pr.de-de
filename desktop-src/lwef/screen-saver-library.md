---
title: Behandeln von Bildschirm Schonern
description: Die Microsoft Win32-API unterstützt spezielle Anwendungen namens Bildschirmschoner.
ms.assetid: cda5e690-71fe-4df7-b8a2-3a2ad65b1bfb
keywords:
- Bildschirmschoner
- Systemsteuerung, Bildschirmschoner
- Screensaverkonfiguriredialog
- Modul Definitions Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b7e0d0c177af2798b041fa12b4cc5793bf9be0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473020"
---
# <a name="handling-screen-savers"></a><span data-ttu-id="4fc17-107">Behandeln von Bildschirm Schonern</span><span class="sxs-lookup"><span data-stu-id="4fc17-107">Handling Screen Savers</span></span>

<span data-ttu-id="4fc17-108">Die Microsoft Win32-API unterstützt spezielle Anwendungen namens *Bildschirmschoner*.</span><span class="sxs-lookup"><span data-stu-id="4fc17-108">The Microsoft Win32 API supports special applications called *screen savers*.</span></span> <span data-ttu-id="4fc17-109">Bildschirmschoner beginnen, wenn sich die Maus und die Tastatur für einen angegebenen Zeitraum im Leerlauf befanden.</span><span class="sxs-lookup"><span data-stu-id="4fc17-109">Screen savers start when the mouse and keyboard have been idle for a specified period of time.</span></span> <span data-ttu-id="4fc17-110">Sie werden aus zwei Gründen verwendet:</span><span class="sxs-lookup"><span data-stu-id="4fc17-110">They are used for these two reasons:</span></span>

-   <span data-ttu-id="4fc17-111">Zum Schützen eines Bildschirms vor der durch statische Bilder verursachten Phosphor Verbrennung.</span><span class="sxs-lookup"><span data-stu-id="4fc17-111">To protect a screen from phosphor burn caused by static images.</span></span>
-   <span data-ttu-id="4fc17-112">, Um vertrauliche Informationen auf einem Bildschirm zu verbergen.</span><span class="sxs-lookup"><span data-stu-id="4fc17-112">To conceal sensitive information left on a screen.</span></span>

<span data-ttu-id="4fc17-113">Dieses Thema ist in die folgenden Abschnitte unterteilt.</span><span class="sxs-lookup"><span data-stu-id="4fc17-113">This topic is divided into the following sections.</span></span>

-   [<span data-ttu-id="4fc17-114">Informationen zu Bildschirmschoner</span><span class="sxs-lookup"><span data-stu-id="4fc17-114">About Screen Savers</span></span>](#about-screen-savers)
-   [<span data-ttu-id="4fc17-115">Verwenden der Bildschirmschoner-Funktionen</span><span class="sxs-lookup"><span data-stu-id="4fc17-115">Using the Screen Saver Functions</span></span>](#using-the-screen-saver-functions)
    -   [<span data-ttu-id="4fc17-116">Erstellen eines Bildschirmschoners</span><span class="sxs-lookup"><span data-stu-id="4fc17-116">Creating a Screen Saver</span></span>](#creating-a-screen-saver)
    -   [<span data-ttu-id="4fc17-117">Installieren neuer Bildschirmschoner</span><span class="sxs-lookup"><span data-stu-id="4fc17-117">Installing New Screen Savers</span></span>](#installing-new-screen-savers)
    -   [<span data-ttu-id="4fc17-118">Hinzufügen von Hilfe zum Dialog Feld "Bildschirmschoner-Konfiguration"</span><span class="sxs-lookup"><span data-stu-id="4fc17-118">Adding Help to the Screen Saver Configuration Dialog Box</span></span>](#adding-help-to-the-screen-saver-configuration-dialog-box)

## <a name="about-screen-savers"></a><span data-ttu-id="4fc17-119">Informationen zu Bildschirmschoner</span><span class="sxs-lookup"><span data-stu-id="4fc17-119">About Screen Savers</span></span>

<span data-ttu-id="4fc17-120">Mithilfe der Desktop Anwendung in der Windows-Systemsteuerung können Benutzer aus einer Liste von Bildschirm Schonern auswählen, wie viel Zeit vergehen muss, bevor der Bildschirmschoner beginnt, Bildschirmschoner konfigurieren und Bildschirmschoner in der Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4fc17-120">The Desktop application in the Windows Control Panel lets users select from a list of screen savers, specify how much time should elapse before the screen saver starts, configure screen savers, and preview screen savers.</span></span> <span data-ttu-id="4fc17-121">Bildschirmschoner werden automatisch geladen, wenn Windows gestartet wird oder wenn ein Benutzer den Bildschirmschoner über die Systemsteuerung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4fc17-121">Screen savers are loaded automatically when Windows starts or when a user activates the screen saver through the Control Panel.</span></span>

<span data-ttu-id="4fc17-122">Sobald ein Bildschirmschoner ausgewählt ist, überwacht Windows Tastatureingaben und Mausbewegungen und startet dann den Bildschirmschoner nach einer gewissen Zeit der Inaktivität.</span><span class="sxs-lookup"><span data-stu-id="4fc17-122">Once a screen saver is chosen, Windows monitors keystrokes and mouse movements and then starts the screen saver after a period of inactivity.</span></span> <span data-ttu-id="4fc17-123">Windows startet den Bildschirmschoner jedoch nicht, wenn eine der folgenden Bedingungen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="4fc17-123">However, Windows does not start the screen saver if any of the following conditions exist:</span></span>

-   <span data-ttu-id="4fc17-124">Bei der aktiven Anwendung handelt es sich nicht um eine Windows-basierte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4fc17-124">The active application is not a Windows-based application.</span></span>
-   <span data-ttu-id="4fc17-125">Es ist ein computerbasiertes Schulungs Fenster (CBT) vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4fc17-125">A computer-based training (CBT) window is present.</span></span>
-   <span data-ttu-id="4fc17-126">Die aktive Anwendung empfängt die [WM- \_ syscommand](../menurc/wm-syscommand.md) -Nachricht, bei der der *wParam* -Parameter auf den SC \_ Screensave-Wert festgelegt ist, übergibt die Nachricht jedoch nicht an die [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4fc17-126">The active application receives the [WM\_SYSCOMMAND](../menurc/wm-syscommand.md) message with the *wParam* parameter set to the SC\_SCREENSAVE value, but it does not pass the message to the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="4fc17-127">**Sicherheitskontext des Bildschirmschoners**</span><span class="sxs-lookup"><span data-stu-id="4fc17-127">**Security Context of the Screen Saver**</span></span>

<span data-ttu-id="4fc17-128">Der Sicherheitskontext des Bildschirmschoners ist davon abhängig, ob ein Benutzer interaktiv angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="4fc17-128">The security context of the screen saver is dependent on whether a user is interactively logged on.</span></span> <span data-ttu-id="4fc17-129">Wenn ein Benutzer beim Aufrufen des Bildschirmschoners interaktiv angemeldet ist, wird der Bildschirmschoner im Sicherheitskontext des interaktiven Benutzers ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4fc17-129">If a user is interactively logged on when the screen saver is invoked, the screen saver runs in the security context of the interactive user.</span></span> <span data-ttu-id="4fc17-130">Wenn kein Benutzer angemeldet ist, ist der Sicherheitskontext des Bildschirmschoners abhängig von der verwendeten Windows-Version.</span><span class="sxs-lookup"><span data-stu-id="4fc17-130">If no user is logged on, the security context of the screen saver is dependent on the version of Windows being used.</span></span>

-   <span data-ttu-id="4fc17-131">Windows XP und Windows 2000-Bildschirmschoner werden im Kontext von "LocalSystem" mit eingeschränkten Konten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4fc17-131">Windows XP and Windows 2000 - screen saver runs in the context of LocalSystem with accounts restricted.</span></span>
-   <span data-ttu-id="4fc17-132">Windows 2003: der Bildschirmschoner wird im Kontext von "LocalService" mit allen entfernten Berechtigungen und der Gruppe "Administratoren" ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4fc17-132">Windows 2003 - screen saver runs in the context of LocalService with all privileges removed and administrators group disabled.</span></span>
-   <span data-ttu-id="4fc17-133">Gilt nicht für Windows NT4.</span><span class="sxs-lookup"><span data-stu-id="4fc17-133">Does not apply to Windows NT4.</span></span>

<span data-ttu-id="4fc17-134">Der Sicherheitskontext bestimmt die Ebene privilegierter Vorgänge, die über einen Bildschirmschoner durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="4fc17-134">The security context determines the level of privileged operations which can be done from a screen saver.</span></span>

<span data-ttu-id="4fc17-135">**Windows Vista und höher:** Wenn der Kenn Wort Schutz durch eine Richtlinie aktiviert ist, wird der Bildschirmschoner unabhängig davon gestartet, was eine Anwendung mit der SC \_ Screensave-Benachrichtigung bewirkt.</span><span class="sxs-lookup"><span data-stu-id="4fc17-135">**Windows Vista and later:** If password protection is enabled by policy, the screen saver is started regardless of what an application does with the SC\_SCREENSAVE notification.</span></span>

<span data-ttu-id="4fc17-136">Bildschirmschoner enthalten bestimmte exportierte Funktionen, Ressourcen Definitionen und Variablen Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="4fc17-136">Screen savers contain specific exported functions, resource definitions, and variable declarations.</span></span> <span data-ttu-id="4fc17-137">Die Bildschirmschoner-Bibliothek enthält die **Main** -Funktion und anderen Startcode, der für einen Bildschirmschoner erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4fc17-137">The screen saver library contains the **main** function and other startup code required for a screen saver.</span></span> <span data-ttu-id="4fc17-138">Wenn ein Bildschirmschoner gestartet wird, erstellt der Startcode in der Bildschirmschoner-Bibliothek ein voll Bildfenster.</span><span class="sxs-lookup"><span data-stu-id="4fc17-138">When a screen saver starts, the startup code in the screen saver library creates a full-screen window.</span></span> <span data-ttu-id="4fc17-139">Die Fenster Klasse für dieses Fenster wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="4fc17-139">The window class for this window is declared as follows:</span></span>


```
WNDCLASS cls; 
cls.hCursor        = NULL; 
cls.hIcon          = LoadIcon(hInst, MAKEINTATOM(ID_APP)); 
cls.lpszMenuName   = NULL; 
cls.lpszClassName  = "WindowsScreenSaverClass"; 
cls.hbrBackground  = GetStockObject(BLACK_BRUSH); 
cls.hInstance      = hInst; 
cls.style          = CS_VREDRAW  | CS_HREDRAW | CS_SAVEBITS | CS_DBLCLKS; 
cls.lpfnWndProc    = (WNDPROC) ScreenSaverProc; 
cls.cbWndExtra     = 0; 
cls.cbClsExtra     = 0;
```



<span data-ttu-id="4fc17-140">Zum Erstellen eines Bildschirmschoners erstellen die meisten Entwickler ein Quell Code Modul, das drei erforderliche Funktionen enthält, und verknüpfen Sie mit der Bildschirmschoner-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="4fc17-140">To create a screen saver, most developers create a source code module containing three required functions and link them with the screen saver library.</span></span> <span data-ttu-id="4fc17-141">Ein Bildschirmschoner-Modul ist nur für die Konfiguration und das Bereitstellen von visuellen Effekten zuständig.</span><span class="sxs-lookup"><span data-stu-id="4fc17-141">A screen saver module is responsible only for configuring itself and for providing visual effects.</span></span>

<span data-ttu-id="4fc17-142">Eine der drei erforderlichen Funktionen in einem Bildschirmschoner-Modul ist [**screensaverproc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span><span class="sxs-lookup"><span data-stu-id="4fc17-142">One of the three required functions in a screen saver module is [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span></span> <span data-ttu-id="4fc17-143">Diese Funktion verarbeitet bestimmte Nachrichten und übergibt alle nicht verarbeiteten Nachrichten an die Bildschirmschoner-Bibliothek zurück.</span><span class="sxs-lookup"><span data-stu-id="4fc17-143">This function processes specific messages and passes any unprocessed messages back to the screen saver library.</span></span> <span data-ttu-id="4fc17-144">Im folgenden finden Sie einige der typischen Nachrichten, die von **screensaverproc** verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="4fc17-144">Following are some of the typical messages processed by **ScreenSaverProc**.</span></span>



| <span data-ttu-id="4fc17-145">Nachricht</span><span class="sxs-lookup"><span data-stu-id="4fc17-145">Message</span></span>        | <span data-ttu-id="4fc17-146">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4fc17-146">Meaning</span></span>                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc17-147">WM \_ Erstellen</span><span class="sxs-lookup"><span data-stu-id="4fc17-147">WM\_CREATE</span></span>     | <span data-ttu-id="4fc17-148">Abrufen von Initialisierungs Daten aus der Regedit.ini Datei.</span><span class="sxs-lookup"><span data-stu-id="4fc17-148">Retrieve any initialization data from the Regedit.ini file.</span></span> <span data-ttu-id="4fc17-149">Legen Sie einen Fenster Zeit Geber für das Fenster "Bildschirmschoner" fest.</span><span class="sxs-lookup"><span data-stu-id="4fc17-149">Set a window timer for the screen saver window.</span></span> <span data-ttu-id="4fc17-150">Führen Sie eine beliebige andere erforderliche Initialisierung aus.</span><span class="sxs-lookup"><span data-stu-id="4fc17-150">Perform any other required initialization.</span></span>                                     |
| <span data-ttu-id="4fc17-151">WM- \_ erasebkgnd</span><span class="sxs-lookup"><span data-stu-id="4fc17-151">WM\_ERASEBKGND</span></span> | <span data-ttu-id="4fc17-152">Löschen Sie das Fenster "Bildschirmschoner", und bereiten Sie nachfolgende Zeichnungsvorgänge vor.</span><span class="sxs-lookup"><span data-stu-id="4fc17-152">Erase the screen saver window and prepare for subsequent drawing operations.</span></span>                                                                                                               |
| <span data-ttu-id="4fc17-153">WM- \_ Timer</span><span class="sxs-lookup"><span data-stu-id="4fc17-153">WM\_TIMER</span></span>      | <span data-ttu-id="4fc17-154">Ausführen von Zeichnungs Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="4fc17-154">Perform drawing operations.</span></span>                                                                                                                                                                |
| <span data-ttu-id="4fc17-155">WM \_ zerstören</span><span class="sxs-lookup"><span data-stu-id="4fc17-155">WM\_DESTROY</span></span>    | <span data-ttu-id="4fc17-156">Die beim Verarbeiten der [WM \_ Create](../winmsg/wm-create.md) -Nachricht erstellten Timer werden zerstört</span><span class="sxs-lookup"><span data-stu-id="4fc17-156">Destroy the timers created when the application processed the [WM\_CREATE](../winmsg/wm-create.md) message.</span></span> <span data-ttu-id="4fc17-157">Führen Sie alle zusätzlichen erforderlichen Bereinigungs Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="4fc17-157">Perform any additional required cleanup.</span></span> |



 

<span data-ttu-id="4fc17-158">[**Screensaverproc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) übergibt nicht verarbeitete Nachrichten durch Aufrufen der [**defscreensaverproc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) -Funktion an die Bildschirmschoner-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="4fc17-158">[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) passes unprocessed messages to the screen saver library by calling the [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) function.</span></span> <span data-ttu-id="4fc17-159">In der folgenden Tabelle wird beschrieben, wie die Funktion verschiedene Nachrichten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="4fc17-159">The following table describes how this function processes various messages.</span></span>



| <span data-ttu-id="4fc17-160">`Message`</span><span class="sxs-lookup"><span data-stu-id="4fc17-160">Message</span></span>         | <span data-ttu-id="4fc17-161">Aktion</span><span class="sxs-lookup"><span data-stu-id="4fc17-161">Action</span></span>                                                                    |
|-----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="4fc17-162">WM- \_ SetCursor</span><span class="sxs-lookup"><span data-stu-id="4fc17-162">WM\_SETCURSOR</span></span>   | <span data-ttu-id="4fc17-163">Legen Sie den Cursor auf den NULL-Cursor fest, und entfernen Sie ihn aus dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="4fc17-163">Set the cursor to the null cursor, removing it from the screen.</span></span>           |
| <span data-ttu-id="4fc17-164">WM- \_ Paint</span><span class="sxs-lookup"><span data-stu-id="4fc17-164">WM\_PAINT</span></span>       | <span data-ttu-id="4fc17-165">Zeichnen Sie den Bildschirmhintergrund.</span><span class="sxs-lookup"><span data-stu-id="4fc17-165">Paint the screen background.</span></span>                                              |
| <span data-ttu-id="4fc17-166">WM \_ lbuttondown</span><span class="sxs-lookup"><span data-stu-id="4fc17-166">WM\_LBUTTONDOWN</span></span> | <span data-ttu-id="4fc17-167">Beenden Sie den Bildschirmschoner.</span><span class="sxs-lookup"><span data-stu-id="4fc17-167">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="4fc17-168">WM- \_ mbuttondown</span><span class="sxs-lookup"><span data-stu-id="4fc17-168">WM\_MBUTTONDOWN</span></span> | <span data-ttu-id="4fc17-169">Beenden Sie den Bildschirmschoner.</span><span class="sxs-lookup"><span data-stu-id="4fc17-169">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="4fc17-170">WM- \_ rbuttondown</span><span class="sxs-lookup"><span data-stu-id="4fc17-170">WM\_RBUTTONDOWN</span></span> | <span data-ttu-id="4fc17-171">Beenden Sie den Bildschirmschoner.</span><span class="sxs-lookup"><span data-stu-id="4fc17-171">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="4fc17-172">WM- \_ KeyDown</span><span class="sxs-lookup"><span data-stu-id="4fc17-172">WM\_KEYDOWN</span></span>     | <span data-ttu-id="4fc17-173">Beenden Sie den Bildschirmschoner.</span><span class="sxs-lookup"><span data-stu-id="4fc17-173">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="4fc17-174">WM- \_ mouseelmove</span><span class="sxs-lookup"><span data-stu-id="4fc17-174">WM\_MOUSEMOVE</span></span>   | <span data-ttu-id="4fc17-175">Beenden Sie den Bildschirmschoner.</span><span class="sxs-lookup"><span data-stu-id="4fc17-175">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="4fc17-176">WM \_ aktivieren</span><span class="sxs-lookup"><span data-stu-id="4fc17-176">WM\_ACTIVATE</span></span>    | <span data-ttu-id="4fc17-177">Beenden Sie den Bildschirmschoner, wenn der *wParam* -Parameter auf " **false**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4fc17-177">Terminate the screen saver if the *wParam* parameter is set to **FALSE**.</span></span> |



 

<span data-ttu-id="4fc17-178">Die zweite erforderliche Funktion in einem Bildschirmschoner-Modul ist [**screensaverkonfiguriredialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog).</span><span class="sxs-lookup"><span data-stu-id="4fc17-178">The second required function in a screen saver module is [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog).</span></span> <span data-ttu-id="4fc17-179">Diese Funktion zeigt ein Dialogfeld an, in dem der Benutzer den Bildschirmschoner konfigurieren kann (eine Anwendung muss eine entsprechende Dialogfeld Vorlage bereitstellen).</span><span class="sxs-lookup"><span data-stu-id="4fc17-179">This function displays a dialog box that enables the user to configure the screen saver (an application must provide a corresponding dialog box template).</span></span> <span data-ttu-id="4fc17-180">In Windows wird das Dialogfeld Konfiguration angezeigt, wenn der Benutzer die Schaltfläche **Setup** im Dialogfeld Bildschirmschoner der Systemsteuerung auswählt.</span><span class="sxs-lookup"><span data-stu-id="4fc17-180">Windows displays the configuration dialog box when the user selects the **Setup** button in the Control Panel's Screen Saver dialog box.</span></span>

<span data-ttu-id="4fc17-181">Die dritte erforderliche Funktion in einem Bildschirmschoner-Modul ist [**registerdialogclasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses).</span><span class="sxs-lookup"><span data-stu-id="4fc17-181">The third required function in a screen saver module is [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses).</span></span> <span data-ttu-id="4fc17-182">Diese Funktion muss von allen Bildschirmschoner-Anwendungen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4fc17-182">This function must be called by all screen saver applications.</span></span> <span data-ttu-id="4fc17-183">Anwendungen, für die keine speziellen Fenster oder benutzerdefinierten Steuerelemente im Konfigurations Dialogfeld erforderlich sind, können jedoch einfach " **true**" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4fc17-183">However, applications that do not require special windows or custom controls in the configuration dialog box can simply return **TRUE**.</span></span> <span data-ttu-id="4fc17-184">Anwendungen, die besondere Fenster oder benutzerdefinierte Steuerelemente erfordern, sollten diese Funktion verwenden, um die entsprechenden Fenster Klassen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="4fc17-184">Applications requiring special windows or custom controls should use this function to register the corresponding window classes.</span></span>

<span data-ttu-id="4fc17-185">Zusätzlich zum Erstellen eines Moduls, das die drei soeben beschriebenen Funktionen unterstützt, sollte ein Bildschirmschoner ein Symbol bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4fc17-185">In addition to creating a module that supports the three functions just described, a screen saver should supply an icon.</span></span> <span data-ttu-id="4fc17-186">Dieses Symbol ist nur sichtbar, wenn der Bildschirmschoner als eigenständige Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4fc17-186">This icon is visible only when the screen saver is run as a standalone application.</span></span> <span data-ttu-id="4fc17-187">(Um in der Systemsteuerung ausgeführt zu werden, muss ein Bildschirmschoner über die Dateinamenerweiterung. SCR verfügen, die als eigenständige Anwendung ausgeführt werden muss. exe muss die Dateinamenerweiterung. exe aufweisen.) Das Symbol muss in der Ressourcen Datei des Bildschirmschoners durch die Konstante-ID-App identifiziert werden \_ , die in der Header Datei "Scrnsave. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4fc17-187">(To be run by the Control Panel, a screen saver must have the .scr file name extension; to be run as a standalone application, it must have the .exe file name extension.) The icon must be identified in the screen saver's resource file by the constant ID\_APP, which is defined in the Scrnsave.h header file.</span></span>

<span data-ttu-id="4fc17-188">Eine abschließende Anforderung ist eine Bildschirmschoner-Beschreibungs Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4fc17-188">One final requirement is a screen saver description string.</span></span> <span data-ttu-id="4fc17-189">Die Ressourcen Datei für einen Bildschirmschoner muss eine Zeichenfolge enthalten, die in der Systemsteuerung als Bildschirmschoner Name angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4fc17-189">The resource file for a screen saver must contain a string that the Control Panel displays as the screen saver name.</span></span> <span data-ttu-id="4fc17-190">Die Beschreibungs Zeichenfolge muss die erste Zeichenfolge in der Zeichen folgen Tabelle der Ressourcen Datei (identifiziert durch den Ordinalwert 1) sein.</span><span class="sxs-lookup"><span data-stu-id="4fc17-190">The description string must be the first string in the resource file's string table (identified with the ordinal value 1).</span></span> <span data-ttu-id="4fc17-191">Die Beschreibungs Zeichenfolge wird jedoch von der Systemsteuerung ignoriert, wenn der Bildschirmschoner über einen langen Dateinamen verfügt.</span><span class="sxs-lookup"><span data-stu-id="4fc17-191">However, the description string is ignored by the Control Panel if the screen saver has a long filename.</span></span> <span data-ttu-id="4fc17-192">In diesem Fall wird der Dateiname als Beschreibungs Zeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="4fc17-192">In such case, the filename will be used as the description string.</span></span>

## <a name="using-the-screen-saver-functions"></a><span data-ttu-id="4fc17-193">Verwenden der Bildschirmschoner-Funktionen</span><span class="sxs-lookup"><span data-stu-id="4fc17-193">Using the Screen Saver Functions</span></span>

<span data-ttu-id="4fc17-194">In diesem Abschnitt wird ein Beispielcode aus einer Bildschirmschoner Anwendung verwendet, um die folgenden Aufgaben zu veranschaulichen:</span><span class="sxs-lookup"><span data-stu-id="4fc17-194">This section uses example code taken from a screen saver application to illustrate the following tasks:</span></span>

-   [<span data-ttu-id="4fc17-195">Erstellen eines Bildschirmschoners</span><span class="sxs-lookup"><span data-stu-id="4fc17-195">Creating a Screen Saver</span></span>](#creating-a-screen-saver)
-   [<span data-ttu-id="4fc17-196">Installieren neuer Bildschirmschoner</span><span class="sxs-lookup"><span data-stu-id="4fc17-196">Installing New Screen Savers</span></span>](#installing-new-screen-savers)
-   [<span data-ttu-id="4fc17-197">Hinzufügen von Hilfe zum Dialog Feld "Bildschirmschoner-Konfiguration"</span><span class="sxs-lookup"><span data-stu-id="4fc17-197">Adding Help to the Screen Saver Configuration Dialog Box</span></span>](#adding-help-to-the-screen-saver-configuration-dialog-box)

### <a name="creating-a-screen-saver"></a><span data-ttu-id="4fc17-198">Erstellen eines Bildschirmschoners</span><span class="sxs-lookup"><span data-stu-id="4fc17-198">Creating a Screen Saver</span></span>

<span data-ttu-id="4fc17-199">In Intervallen von 1 bis 10 Sekunden zeichnet die Anwendung in diesem Beispiel den Bildschirm mit einer von vier Farben auf: weiß, hellgrau, dunkelgrau und schwarz.</span><span class="sxs-lookup"><span data-stu-id="4fc17-199">At intervals ranging from 1 through 10 seconds, the application in this example repaints the screen with one of four colors: white, light gray, dark gray, and black.</span></span> <span data-ttu-id="4fc17-200">Die Anwendung zeichnet den Bildschirm jedes Mal, wenn [eine \_ WM](../winmsg/wm-timer.md) -Zeit Geber Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="4fc17-200">The application paints the screen each time it receives a [WM\_TIMER](../winmsg/wm-timer.md) message.</span></span> <span data-ttu-id="4fc17-201">Der Benutzer kann das Intervall, in dem diese Nachricht gesendet wird, anpassen, indem er das Konfigurations Dialogfeld der Anwendung auswählt und eine einzelne horizontale Schiebe Leiste anpasst.</span><span class="sxs-lookup"><span data-stu-id="4fc17-201">The user can adjust the interval at which this message is sent by selecting the application's configuration dialog box and adjusting a single horizontal scroll bar.</span></span>

### <a name="screen-saver-library"></a><span data-ttu-id="4fc17-202">Bildschirmschoner-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4fc17-202">Screen saver library</span></span>

<span data-ttu-id="4fc17-203">Die statischen Bildschirmschoner-Funktionen sind in der Bildschirmschoner-Bibliothek enthalten.</span><span class="sxs-lookup"><span data-stu-id="4fc17-203">The static screen saver functions are contained in the screen saver library.</span></span> <span data-ttu-id="4fc17-204">Es sind zwei Versionen der Bibliothek verfügbar: SCRNSAVE. lib und scrnsavw. lib.</span><span class="sxs-lookup"><span data-stu-id="4fc17-204">There are two versions of the library available, Scrnsave.lib and Scrnsavw.lib.</span></span> <span data-ttu-id="4fc17-205">Sie müssen Ihr Projekt mit einem dieser Verknüpfungen verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="4fc17-205">You must link your project with one of these.</span></span> <span data-ttu-id="4fc17-206">SCRNSAVE. lib wird für Bildschirmschoner verwendet, die ANSI-Zeichen verwenden, und scrnsavw. lib wird für Bildschirmschoner verwendet, die Unicode-Zeichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4fc17-206">Scrnsave.lib is used for screen savers that use ANSI characters, and Scrnsavw.lib is used for screen savers that use Unicode characters.</span></span> <span data-ttu-id="4fc17-207">Ein Bildschirmschoner, der mit scrnsavw. lib verknüpft ist, kann nur auf Windows-Plattformen ausgeführt werden, die Unicode unterstützen, während ein mit SCRNSAVE. lib verknüpfter Bildschirmschoner auf jeder Windows-Plattform ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4fc17-207">A screen saver that is linked with Scrnsavw.lib will only run on Windows platforms that support Unicode, while a screen saver linked with Scrnsave.lib will run on any Windows platform.</span></span>

### <a name="supporting-the-configuration-dialog-box"></a><span data-ttu-id="4fc17-208">Unterstützen des Konfigurations Dialogfelds</span><span class="sxs-lookup"><span data-stu-id="4fc17-208">Supporting the configuration dialog box</span></span>

<span data-ttu-id="4fc17-209">Die meisten Bildschirmschoner stellen ein Konfigurations Dialogfeld bereit, mit dem der Benutzer Anpassungsdaten, z. b. eindeutige Farben, Zeichen Geschwindigkeiten, Linienstärke, Schriftarten usw., angeben kann.</span><span class="sxs-lookup"><span data-stu-id="4fc17-209">Most screen savers provide a configuration dialog box to let the user specify customization data such as unique colors, drawing speeds, line thickness, fonts, and so on.</span></span> <span data-ttu-id="4fc17-210">Um das Dialogfeld "Konfiguration" zu unterstützen, muss die Anwendung eine Dialogfeld Vorlage bereitstellen. Außerdem muss die Funktion " [**screensaverkonfiguriredialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) " unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4fc17-210">To support the configuration dialog box, the application must provide a dialog box template and must also support the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function.</span></span> <span data-ttu-id="4fc17-211">Im folgenden finden Sie die Dialogfeld Vorlage für die Beispielanwendung.</span><span class="sxs-lookup"><span data-stu-id="4fc17-211">Following is the dialog box template for the sample application.</span></span>


```
DLG_SCRNSAVECONFIGURE DIALOG 6, 18, 160, 63
LANGUAGE LANG_NEUTRAL, SUBLANG_NEUTRAL
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION | WS_SYSMENU
CAPTION "Sample Screen-Saver Setup"
FONT 8, "MS Shell Dlg"
BEGIN
    GROUPBOX      "Redraw Speed", 101, 0, 6, 98, 40
    SCROLLBAR     ID_SPEED, 5, 31, 89, 10
    LTEXT         "Fast", 103, 6, 21, 20, 8
    LTEXT         "Slow", 104, 75, 21, 20, 8
    PUSHBUTTON    "OK", ID_OK, 117, 10, 40, 14
    PUSHBUTTON    "Cancel", ID_CANCEL, 117, 32, 40, 14
END
```



<span data-ttu-id="4fc17-212">Sie müssen die Konstante definieren, die zum Identifizieren der Dialogfeld Vorlage verwendet wird, indem Sie den Dezimalwert 2003 verwenden, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="4fc17-212">You must define the constant used to identify the dialog box template by using the decimal value 2003, as in the following example:</span></span>


```
#define  DLG_SCRNSAVECONFIGURE 2003
```



<span data-ttu-id="4fc17-213">Das folgende Beispiel zeigt die [**screensaverkonfiguriredialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) -Funktion, die in der Beispielanwendung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4fc17-213">The following example shows the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function found in the sample application.</span></span>


```
#define MINVEL  1                 // minimum redraw speed value     
#define MAXVEL  10                // maximum redraw speed value    
#define DEFVEL  5                 // default redraw speed value    
 
LONG    lSpeed = DEFVEL;          // redraw speed variable         
  
extern HINSTANCE hMainInstance;   // screen saver instance handle  
 
CHAR   szAppName[80];             // .ini section name             
CHAR   szTemp[20];                // temporary array of characters  
CHAR   szRedrawSpeed[ ] = "Redraw Speed";   // .ini speed entry 
CHAR   szIniFile[MAXFILELEN];     // .ini or registry file name  
 
BOOL WINAPI ScreenSaverConfigureDialog(hDlg, message, wParam, lParam) 
HWND     hDlg; 
UINT     message; 
DWORD    wParam; 
LONG     lParam; 
HRESULT  hr;
{ 
    static HWND hSpeed;   // handle to speed scroll bar 
    static HWND hOK;      // handle to OK push button  
 
    switch(message) 
    { 
        case WM_INITDIALOG: 
 
            // Retrieve the application name from the .rc file.  
            LoadString(hMainInstance, idsAppName, szAppName, 
                       80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, 
                       MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry. 
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // If the initialization file does not contain an entry 
            // for this screen saver, use the default value. 
            if(lSpeed > MAXVEL || lSpeed < MINVEL) 
                lSpeed = DEFVEL; 
 
            // Initialize the redraw speed scroll bar control.
            hSpeed = GetDlgItem(hDlg, ID_SPEED); 
            SetScrollRange(hSpeed, SB_CTL, MINVEL, MAXVEL, FALSE); 
            SetScrollPos(hSpeed, SB_CTL, lSpeed, TRUE); 
 
            // Retrieve a handle to the OK push button control.  
            hOK = GetDlgItem(hDlg, ID_OK); 
 
            return TRUE; 
 
        case WM_HSCROLL: 

            // Process scroll bar input, adjusting the lSpeed 
            // value as appropriate. 
            switch (LOWORD(wParam)) 
                { 
                    case SB_PAGEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_LINEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_PAGEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_LINEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_THUMBPOSITION: 
                        lSpeed = HIWORD(wParam); 
                    break; 
 
                    case SB_BOTTOM: 
                        lSpeed = MINVEL; 
                    break; 
 
                    case SB_TOP: 
                        lSpeed = MAXVEL; 
                    break; 
 
                    case SB_THUMBTRACK: 
                    case SB_ENDSCROLL: 
                        return TRUE; 
                    break; 
                } 

                if ((int) lSpeed <= MINVEL) 
                    lSpeed = MINVEL; 
                if ((int) lSpeed >= MAXVEL) 
                    lSpeed = MAXVEL; 
 
                SetScrollPos((HWND) lParam, SB_CTL, lSpeed, TRUE); 
            break; 
 
        case WM_COMMAND: 
            switch(LOWORD(wParam)) 
            { 
                case ID_OK: 
 
                    // Write the current redraw speed variable to
                    // the .ini file. 
                    hr = StringCchPrintf(szTemp, 20, "%ld", lSpeed);
                    if (SUCCEEDED(hr))
                        WritePrivateProfileString(szAppName, szRedrawSpeed, 
                                                  szTemp, szIniFile); 
 
                case ID_CANCEL: 
                    EndDialog(hDlg, LOWORD(wParam) == ID_OK); 

                return TRUE; 
            } 
    } 
    return FALSE; 
}
```



<span data-ttu-id="4fc17-214">Neben der Bereitstellung der Dialogfeld Vorlage und der Unterstützung der [**screensaverkonfiguriredialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) -Funktion muss eine Anwendung auch die [**registerdialogclasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) -Funktion unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4fc17-214">In addition to providing the dialog box template and supporting the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function, an application must also support the [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) function.</span></span> <span data-ttu-id="4fc17-215">Diese Funktion registriert alle nicht standardmäßigen Fenster Klassen, die für den Bildschirmschoner erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4fc17-215">This function registers any nonstandard window classes required by the screen saver.</span></span> <span data-ttu-id="4fc17-216">Da in der Beispielanwendung nur Standardfenster Klassen in der entsprechenden Dialogfeld Prozedur verwendet wurden, gibt diese Funktion einfach **true** zurück, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="4fc17-216">Because the sample application used only standard window classes in its dialog box procedure, this function simply returns **TRUE**, as in the following example:</span></span>


```
BOOL WINAPI RegisterDialogClasses(hInst) 
HANDLE  hInst; 
{ 
    return TRUE; 
}
```



### <a name="supporting-the-screen-saver-window-procedure"></a><span data-ttu-id="4fc17-217">Unterstützen der Prozedur für den Bildschirmschoner-Fenster</span><span class="sxs-lookup"><span data-stu-id="4fc17-217">Supporting the screen saver window procedure</span></span>

<span data-ttu-id="4fc17-218">Jeder Bildschirmschoner muss eine Fenster Prozedur mit dem Namen [**screensaverproc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc)unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4fc17-218">Each screen saver must support a window procedure named [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span></span> <span data-ttu-id="4fc17-219">Wie die meisten Fenster Prozeduren verarbeitet **screensaverproc** eine Reihe spezifischer Nachrichten und übergibt alle nicht verarbeiteten Nachrichten an eine Standardprozedur.</span><span class="sxs-lookup"><span data-stu-id="4fc17-219">Like most window procedures, **ScreenSaverProc** processes a set of specific messages and passes any unprocessed messages to a default procedure.</span></span> <span data-ttu-id="4fc17-220">Doch anstatt Sie an die [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca) -Funktion zu übergeben, übergibt **screensaverproc** nicht verarbeitete Nachrichten an die [**defscreensaverproc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4fc17-220">However, instead of passing them to the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function, **ScreenSaverProc** passes unprocessed messages to the [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) function.</span></span> <span data-ttu-id="4fc17-221">Ein weiterer Unterschied zwischen **screensaverproc** und einer normalen Fenster Prozedur besteht darin, dass das an **screensaverproc** übermittelte Handle den gesamten Desktop und nicht ein Client Fenster identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4fc17-221">Another difference between **ScreenSaverProc** and a normal window procedure is that the handle passed to **ScreenSaverProc** identifies the entire desktop rather than a client window.</span></span> <span data-ttu-id="4fc17-222">Das folgende Beispiel zeigt die Prozedur **screensaverproc** Window für den Beispiel Bildschirmschoner.</span><span class="sxs-lookup"><span data-stu-id="4fc17-222">The following example shows the **ScreenSaverProc** window procedure for the sample screen saver.</span></span>


```
LONG WINAPI ScreenSaverProc(hwnd, message, wParam, lParam) 
HWND  hwnd; 
UINT  message; 
DWORD wParam; 
LONG  lParam; 
{ 
    static HDC          hdc;      // device-context handle  
    static RECT         rc;       // RECT structure  
    static UINT         uTimer;   // timer identifier  
 
    switch(message) 
    { 
        case WM_CREATE: 
 
            // Retrieve the application name from the .rc file. 
            LoadString(hMainInstance, idsAppName, szAppName, 80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry.  
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // Set a timer for the screen saver window using the 
            // redraw rate stored in Regedit.ini. 
            uTimer = SetTimer(hwnd, 1, lSpeed * 1000, NULL); 
            break; 
 
        case WM_ERASEBKGND: 
 
            // The WM_ERASEBKGND message is issued before the 
            // WM_TIMER message, allowing the screen saver to 
            // paint the background as appropriate. 

            hdc = GetDC(hwnd); 
            GetClientRect (hwnd, &rc); 
            FillRect (hdc, &rc, GetStockObject(BLACK_BRUSH)); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_TIMER: 
 
            // The WM_TIMER message is issued at (lSpeed * 1000) 
            // intervals, where lSpeed == .001 seconds. This 
            // code repaints the entire desktop with a white, 
            // light gray, dark gray, or black brush each 
            // time a WM_TIMER message is issued. 

            hdc = GetDC(hwnd); 
            GetClientRect(hwnd, &rc); 
            if (i++ <= 4) 
                FillRect(hdc, &rc, GetStockObject(i)); 
            else 
                (i = 0); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_DESTROY: 
 
            // When the WM_DESTROY message is issued, the screen saver 
            // must destroy any of the timers that were set at WM_CREATE 
            // time. 

            if (uTimer) 
                KillTimer(hwnd, uTimer); 
            break; 
    } 
 
    // DefScreenSaverProc processes any messages ignored by ScreenSaverProc. 
    return DefScreenSaverProc(hwnd, message, wParam, lParam); 
}
```



### <a name="creating-a-module-definition-file"></a><span data-ttu-id="4fc17-223">Erstellen einer Modul Definitionsdatei</span><span class="sxs-lookup"><span data-stu-id="4fc17-223">Creating a module-definition file</span></span>

<span data-ttu-id="4fc17-224">Die Funktionen [**screensaverproc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) und [**screensaverkonfiguriredialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) müssen in der Modul Definitionsdatei der Anwendung exportiert werden. " [**Registerdialogclasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) " sollte jedoch nicht exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="4fc17-224">The [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) and [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) functions must be exported in the application's module-definition file; [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) should not be exported, however.</span></span> <span data-ttu-id="4fc17-225">Das folgende Beispiel zeigt die Modul Definitionsdatei für die Beispielanwendung.</span><span class="sxs-lookup"><span data-stu-id="4fc17-225">The following example shows the module-definition file for the sample application.</span></span>


```
NAME    SSTEST.SCR 

DESCRIPTION 'SCRNSAVE : Test' 
 
STUB    'WINSTUB.EXE' 
EXETYPE WINDOWS 
 
CODE    MOVEABLE 
DATA    MOVEABLE MULTIPLE 
 
HEAPSIZE  1024 
STACKSIZE 4096 
 
EXPORTS 
        ScreenSaverProc 
        ScreenSaverConfigureDialog
```



### <a name="installing-new-screen-savers"></a><span data-ttu-id="4fc17-226">Installieren neuer Bildschirmschoner</span><span class="sxs-lookup"><span data-stu-id="4fc17-226">Installing New Screen Savers</span></span>

<span data-ttu-id="4fc17-227">Beim Kompilieren der Liste der verfügbaren Bildschirmschoner durchsucht die Systemsteuerung das Windows-Start Verzeichnis nach Dateien mit der Erweiterung. scr.</span><span class="sxs-lookup"><span data-stu-id="4fc17-227">When compiling the list of available screen savers, the Control Panel searches the Windows Startup directory for files with the .scr extension.</span></span> <span data-ttu-id="4fc17-228">Da Bildschirmschoner standardmäßige ausführbare Windows-Dateien mit exe-Erweiterungen sind, müssen Sie diese so umbenennen, dass Sie über. SCR-Erweiterungen verfügen, und Sie in das richtige Verzeichnis kopieren.</span><span class="sxs-lookup"><span data-stu-id="4fc17-228">Because screen savers are standard Windows executable files with .exe extensions, you must rename them so they have .scr extensions and copy them to the correct directory.</span></span>

### <a name="adding-help-to-the-screen-saver-configuration-dialog-box"></a><span data-ttu-id="4fc17-229">Hinzufügen von Hilfe zum Dialog Feld "Bildschirmschoner-Konfiguration"</span><span class="sxs-lookup"><span data-stu-id="4fc17-229">Adding Help to the Screen Saver Configuration Dialog Box</span></span>

<span data-ttu-id="4fc17-230">Das Konfigurations Dialogfeld für einen Bildschirmschoner enthält in der Regel eine Schaltfläche **Hilfe** .</span><span class="sxs-lookup"><span data-stu-id="4fc17-230">The configuration dialog box for a screen saver typically includes a **Help** button.</span></span> <span data-ttu-id="4fc17-231">Bildschirmschoner-Anwendungen können den Bezeichner der Hilfe Schaltfläche Überprüfen und die [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) -Funktion auf die gleiche Weise wie in anderen Windows-basierten Anwendungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4fc17-231">Screen saver applications can check for the Help button identifier and call the [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) function in the same way Help is provided in other Windows-based applications.</span></span>

 

 