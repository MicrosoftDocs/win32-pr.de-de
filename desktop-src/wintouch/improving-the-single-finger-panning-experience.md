---
title: Verbessern der Single-Finger schwenken
description: Wenn Sie eine Anwendung erstellen, die sich auf Windows-Finger Eingaben bezieht, bietet Sie automatisch grundlegende Unterstützung für das Schwenken Allerdings können Sie die WM- \_ Gesten Nachricht verwenden, um erweiterte Unterstützung für Single-Finger-Panning bereitzustellen.
ms.assetid: eb01a6df-9969-44d1-a657-4f83fb0b67cb
keywords:
- Windows Touch, Einfinger schwenken
- Windows-Fingereingabe, Schwenken
- Windows-Fingereingabe, Scrollleisten
- Windows-Fingereingabe, Flicks
- Windows-Toucheingabe, Gesten schwenken Nachrichten
- Windows-Toucheingabe, Begrenzungs Feedback
- Schwenken mit einem Finger
- Schwenken, mit einem Finger
- Schwenken, Grenzen von Feedback
- Bild Lauf leisten, Einfinger schwenken
- Flicks, Einfinger schwenken
- Bild Lauf leisten, deaktivieren
- Flicks, deaktivieren
- Gesten, Gesten Schwenk Meldungen
- Schwenken, Gesten schwenken Nachrichten
- Begrenzungs Feedback, Einfinger schwenken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9081903600918485f1e3241a02c01b5438c1aae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728017"
---
# <a name="improving-the-single-finger-panning-experience"></a><span data-ttu-id="51a10-120">Verbessern der Single-Finger schwenken</span><span class="sxs-lookup"><span data-stu-id="51a10-120">Improving the Single-Finger Panning Experience</span></span>

<span data-ttu-id="51a10-121">Wenn Sie eine Anwendung erstellen, die sich auf Windows-Finger Eingaben bezieht, bietet Sie automatisch grundlegende Unterstützung für das Schwenken</span><span class="sxs-lookup"><span data-stu-id="51a10-121">If you build an application that targets Windows Touch, it automatically provides basic panning support.</span></span> <span data-ttu-id="51a10-122">Allerdings können Sie die [**WM- \_ Gesten**](wm-gesture.md) Nachricht verwenden, um erweiterte Unterstützung für Single-Finger-Panning bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="51a10-122">However, you can use the [**WM\_GESTURE**](wm-gesture.md) message to provide enhanced support for single-finger panning.</span></span>

## <a name="overview"></a><span data-ttu-id="51a10-123">Übersicht</span><span class="sxs-lookup"><span data-stu-id="51a10-123">Overview</span></span>

<span data-ttu-id="51a10-124">Gehen Sie wie in den nachfolgenden Abschnitten in diesem Thema beschrieben vor, um die Einzel Fingerbewegung zu verbessern:</span><span class="sxs-lookup"><span data-stu-id="51a10-124">To improve the single-finger panning experience, use these steps, as explained in subsequent sections of this topic:</span></span>

-   <span data-ttu-id="51a10-125">Erstellen Sie eine Anwendung mit Bild Lauf leisten und deaktivierten schnelle Stift Bewegungen.</span><span class="sxs-lookup"><span data-stu-id="51a10-125">Create an application with scroll bars and with flicks disabled.</span></span>
-   <span data-ttu-id="51a10-126">Unterstützung für Gesten Schwenk Nachrichten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="51a10-126">Add support for gesture pan messages.</span></span>
-   <span data-ttu-id="51a10-127">Aktivieren von Bounce.</span><span class="sxs-lookup"><span data-stu-id="51a10-127">Enable bounce.</span></span>

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a><span data-ttu-id="51a10-128">Erstellen einer Anwendung mit Bild Lauf leisten und deaktivierten Flicks</span><span class="sxs-lookup"><span data-stu-id="51a10-128">Create an Application with Scroll Bars and with Flicks Disabled</span></span>

<span data-ttu-id="51a10-129">Bevor Sie beginnen, müssen Sie eine Anwendung mit Bild Lauf leisten erstellen.</span><span class="sxs-lookup"><span data-stu-id="51a10-129">Before you begin, you must create an application with scroll bars.</span></span> <span data-ttu-id="51a10-130">Dieser Prozess wird im Abschnitt [Legacy Unterstützung für das Schwenken mit Scrollleisten](legacy-support-for-panning-with-scrollbars.md) erläutert.</span><span class="sxs-lookup"><span data-stu-id="51a10-130">The section [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) explains this process.</span></span> <span data-ttu-id="51a10-131">Wenn Sie mit dem Beispiel Inhalt beginnen möchten, wechseln Sie zu diesem Abschnitt, und erstellen Sie eine Anwendung mit Bild Lauf leisten, und deaktivieren Sie dann die Flicks.</span><span class="sxs-lookup"><span data-stu-id="51a10-131">If you want to start with the example content, go to that section and create an application with scroll bars and then disable flicks.</span></span> <span data-ttu-id="51a10-132">Wenn Sie bereits über eine Anwendung mit funktionierenden Bild Lauf leisten verfügen, deaktivieren Sie schnelle Stift Bewegungen wie in diesem Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="51a10-132">If you already have an application with functioning scroll bars, disable flicks as described in that section.</span></span>

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a><span data-ttu-id="51a10-133">Benutzerdefinierte Unterstützung für Gesten schwenken hinzufügen</span><span class="sxs-lookup"><span data-stu-id="51a10-133">Add Custom Panning Support for Gesture Pan Messages</span></span>

<span data-ttu-id="51a10-134">Um Gesten Schwenk Nachrichten zu unterstützen, müssen Sie Sie in der **WndProc** -Methode behandeln.</span><span class="sxs-lookup"><span data-stu-id="51a10-134">To support gesture pan messages, you must handle them in the **WndProc** method.</span></span> <span data-ttu-id="51a10-135">Die Gesten Meldungen werden verwendet, um horizontale und vertikale Delta für Schwenken-Nachrichten zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="51a10-135">The gesture messages are used to determine horizontal and vertical deltas for pan messages.</span></span> <span data-ttu-id="51a10-136">Die Delta Steuer Objekte werden verwendet, um das ScrollBar-Objekt zu aktualisieren, das die Benutzeroberfläche aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="51a10-136">The deltas are used to update the scroll bar object, which updates the user interface.</span></span>

<span data-ttu-id="51a10-137">Aktualisieren Sie zunächst die Windows-Versions Einstellungen in der Datei "targetver. h", um Windows-Fingereingabe zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="51a10-137">First, update the Windows version settings in the targetver.h file to enable Windows Touch.</span></span> <span data-ttu-id="51a10-138">Der folgende Code zeigt die verschiedenen Einstellungen der Windows-Version, die diese in "targetver. h" ersetzen sollen.</span><span class="sxs-lookup"><span data-stu-id="51a10-138">The following code shows the various Windows version settings that should replace those in targetver.h.</span></span>


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



<span data-ttu-id="51a10-139">Fügen Sie dem Projekt anschließend die Datei "uxtheme. h" hinzu, und fügen Sie die Bibliothek "uxtheme. lib" den zusätzlichen Abhängigkeiten Ihres Projekts hinzu.</span><span class="sxs-lookup"><span data-stu-id="51a10-139">Next, add the UXTheme.h file to your project and add the uxtheme.lib library to the additional dependencies of your project.</span></span>


```C++
#include <uxtheme.h>
```



<span data-ttu-id="51a10-140">Fügen Sie als nächstes die folgenden Variablen am Anfang der **WndProc** -Funktion hinzu.</span><span class="sxs-lookup"><span data-stu-id="51a10-140">Next, add the following variables to the top of the **WndProc** function.</span></span> <span data-ttu-id="51a10-141">Diese werden in Berechnungen zum Schwenken verwendet.</span><span class="sxs-lookup"><span data-stu-id="51a10-141">These will be used in calculations for panning.</span></span>


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



<span data-ttu-id="51a10-142">Fügen Sie als nächstes den Handler für [**die \_ WM**](wm-gesture.md) -Gesten Nachricht hinzu, damit die Bild Lauf leisten mit Delta-Gesten aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="51a10-142">Next, add the handler for the [**WM\_GESTURE**](wm-gesture.md) message so that the scroll bars are updated with deltas based on panning gestures.</span></span> <span data-ttu-id="51a10-143">Dadurch erhalten Sie eine wesentlich präzisere Steuerung des schwenken.</span><span class="sxs-lookup"><span data-stu-id="51a10-143">This gives you a much finer-grained control of panning.</span></span>

<span data-ttu-id="51a10-144">Der folgende Code Ruft die [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) -Struktur aus dem *LPARAM* ab, speichert die letzte y-Koordinate aus der-Struktur und bestimmt die Änderung an der Position, an der das Bild Lauf leisten Objekt aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="51a10-144">The following code gets the [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) structure from the *lParam*, saves the last y-coordinate from the structure, and determines the change in position to update the scroll bar object.</span></span> <span data-ttu-id="51a10-145">Der folgende Code sollte in der **WndProc** Switch-Anweisung abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="51a10-145">The following code should be placed in your **WndProc** switch statement.</span></span>


```C++
    case WM_GESTURE:        
        // Get all the vertial scroll bar information
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;
        GetScrollInfo (hWnd, SB_VERT, &si);
        yPos = si.nPos;

        ZeroMemory(&gi, sizeof(GESTUREINFO));
        gi.cbSize = sizeof(GESTUREINFO);
        bResult = GetGestureInfo((HGESTUREINFO)lParam, &gi);

        if (bResult){
            // now interpret the gesture            
            switch (gi.dwID){
                case GID_BEGIN:
                   lastY = gi.ptsLocation.y;
                   CloseGestureInfoHandle((HGESTUREINFO)lParam);
                   break;                     
                // A CUSTOM PAN HANDLER
                // COMMENT THIS CASE OUT TO ENABLE DEFAULT HANDLER BEHAVIOR
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin || si.nPos >= (si.nMax - si.nPage)){                    
                        // we reached the bottom / top, pan
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
                case GID_ZOOM:
                   // Add Zoom handler 
                   return DefWindowProc(hWnd, message, lParam, wParam);
                default:
                   // You have encountered an unknown gesture
                   return DefWindowProc(hWnd, message, lParam, wParam);
             }          
        }else{
            DWORD dwErr = GetLastError();
            if (dwErr > 0){
                // something is wrong 
                // 87 indicates that you are probably using a bad
                // value for the gi.cbSize
            }
        } 
        return DefWindowProc (hWnd, message, wParam, lParam);
```



<span data-ttu-id="51a10-146">Wenn Sie nun die Schwenkbewegung im Fenster ausführen, wird der Text mit Trägheit angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51a10-146">Now, when you perform the pan gesture on your window, you will see the text scroll with inertia.</span></span> <span data-ttu-id="51a10-147">An diesem Punkt können Sie den Text so ändern, dass er mehr Zeilen hat, damit Sie das Schwenken von großen Textabschnitten durchsuchen können.</span><span class="sxs-lookup"><span data-stu-id="51a10-147">At this point, you might want to change the text to have more lines so that you can explore panning large sections of text.</span></span>

## <a name="boundary-feedback-in-wndproc"></a><span data-ttu-id="51a10-148">Begrenzungs Feedback in WndProc</span><span class="sxs-lookup"><span data-stu-id="51a10-148">Boundary Feedback in WndProc</span></span>

<span data-ttu-id="51a10-149">Das Feedback von Grenzen ist eine Art visuelles Feedback, das Benutzern bereitgestellt wird, wenn Sie das Ende eines Platz alisier baren Bereichs erreichen.</span><span class="sxs-lookup"><span data-stu-id="51a10-149">Boundary feedback is a type of visual feedback given to users when they reach the end of a pannable area.</span></span> <span data-ttu-id="51a10-150">Sie wird von der Anwendung ausgelöst, wenn eine Grenze erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="51a10-150">It is triggered by the application when a boundary is reached.</span></span> <span data-ttu-id="51a10-151">In der vorherigen Beispiel Implementierung der [**WM- \_ Gesten**](wm-gesture.md) Nachricht wird die Endbedingung `(si.nPos == si.yPos)` aus dem Fall der **WM- \_ Geste** verwendet, um zu testen, ob Sie das Ende eines Bare-Bereichs erreicht haben.</span><span class="sxs-lookup"><span data-stu-id="51a10-151">In the previous example implementation of the [**WM\_GESTURE**](wm-gesture.md) message, the end condition `(si.nPos == si.yPos)` from the **WM\_GESTURE** case is used to test that you have reached the end of a pannable region.</span></span> <span data-ttu-id="51a10-152">Die folgenden Variablen werden verwendet, um Werte und Test Fehler zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="51a10-152">The following variables are used to track values and test errors.</span></span>


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



<span data-ttu-id="51a10-153">Die Groß-/Kleinschreibung wird aktualisiert, um das Feedback zu Grenzen zu initiieren</span><span class="sxs-lookup"><span data-stu-id="51a10-153">The pan gesture case is updated to trigger boundary feedback.</span></span> <span data-ttu-id="51a10-154">Der folgende Code veranschaulicht die Groß-/Kleinschreibung der **gid \_** aus dem [**WM- \_ Gesten**](wm-gesture.md) Nachrichten Handler.</span><span class="sxs-lookup"><span data-stu-id="51a10-154">The following code illustrates the **GID\_PAN** case from the [**WM\_GESTURE**](wm-gesture.md) message handler.</span></span>


```C++
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin){                    
                        // we reached the top, pan upwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }else if (si.nPos >= (si.nMax - si.nPage)){
                        // we reached the bottom, pan downwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
  
```



<span data-ttu-id="51a10-155">Das Fenster der Anwendung sollte nun über ein Begrenzungs Feedback verfügen, wenn sich ein Benutzer hinter dem unteren Rand des Bild Lauf leisten Bereichs befindet.</span><span class="sxs-lookup"><span data-stu-id="51a10-155">Now your application's window should have boundary feedback when a user pans past the bottom of the scroll bar region.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51a10-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51a10-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51a10-157">Windows-Touchgesten</span><span class="sxs-lookup"><span data-stu-id="51a10-157">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> <dt>

[<span data-ttu-id="51a10-158">**Beginpanningfeedback**</span><span class="sxs-lookup"><span data-stu-id="51a10-158">**BeginPanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-beginpanningfeedback)
</dt> <dt>

[<span data-ttu-id="51a10-159">**Endpanningfeedback**</span><span class="sxs-lookup"><span data-stu-id="51a10-159">**EndPanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-endpanningfeedback)
</dt> <dt>

[<span data-ttu-id="51a10-160">**Updatepanningfeedback**</span><span class="sxs-lookup"><span data-stu-id="51a10-160">**UpdatePanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-updatepanningfeedback)
</dt> </dl>

 

 