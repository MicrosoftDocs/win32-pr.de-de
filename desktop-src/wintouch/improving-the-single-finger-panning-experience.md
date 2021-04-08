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
# <a name="improving-the-single-finger-panning-experience"></a>Verbessern der Single-Finger schwenken

Wenn Sie eine Anwendung erstellen, die sich auf Windows-Finger Eingaben bezieht, bietet Sie automatisch grundlegende Unterstützung für das Schwenken Allerdings können Sie die [**WM- \_ Gesten**](wm-gesture.md) Nachricht verwenden, um erweiterte Unterstützung für Single-Finger-Panning bereitzustellen.

## <a name="overview"></a>Übersicht

Gehen Sie wie in den nachfolgenden Abschnitten in diesem Thema beschrieben vor, um die Einzel Fingerbewegung zu verbessern:

-   Erstellen Sie eine Anwendung mit Bild Lauf leisten und deaktivierten schnelle Stift Bewegungen.
-   Unterstützung für Gesten Schwenk Nachrichten hinzufügen.
-   Aktivieren von Bounce.

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a>Erstellen einer Anwendung mit Bild Lauf leisten und deaktivierten Flicks

Bevor Sie beginnen, müssen Sie eine Anwendung mit Bild Lauf leisten erstellen. Dieser Prozess wird im Abschnitt [Legacy Unterstützung für das Schwenken mit Scrollleisten](legacy-support-for-panning-with-scrollbars.md) erläutert. Wenn Sie mit dem Beispiel Inhalt beginnen möchten, wechseln Sie zu diesem Abschnitt, und erstellen Sie eine Anwendung mit Bild Lauf leisten, und deaktivieren Sie dann die Flicks. Wenn Sie bereits über eine Anwendung mit funktionierenden Bild Lauf leisten verfügen, deaktivieren Sie schnelle Stift Bewegungen wie in diesem Abschnitt beschrieben.

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a>Benutzerdefinierte Unterstützung für Gesten schwenken hinzufügen

Um Gesten Schwenk Nachrichten zu unterstützen, müssen Sie Sie in der **WndProc** -Methode behandeln. Die Gesten Meldungen werden verwendet, um horizontale und vertikale Delta für Schwenken-Nachrichten zu bestimmen. Die Delta Steuer Objekte werden verwendet, um das ScrollBar-Objekt zu aktualisieren, das die Benutzeroberfläche aktualisiert.

Aktualisieren Sie zunächst die Windows-Versions Einstellungen in der Datei "targetver. h", um Windows-Fingereingabe zu aktivieren. Der folgende Code zeigt die verschiedenen Einstellungen der Windows-Version, die diese in "targetver. h" ersetzen sollen.


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



Fügen Sie dem Projekt anschließend die Datei "uxtheme. h" hinzu, und fügen Sie die Bibliothek "uxtheme. lib" den zusätzlichen Abhängigkeiten Ihres Projekts hinzu.


```C++
#include <uxtheme.h>
```



Fügen Sie als nächstes die folgenden Variablen am Anfang der **WndProc** -Funktion hinzu. Diese werden in Berechnungen zum Schwenken verwendet.


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



Fügen Sie als nächstes den Handler für [**die \_ WM**](wm-gesture.md) -Gesten Nachricht hinzu, damit die Bild Lauf leisten mit Delta-Gesten aktualisiert werden. Dadurch erhalten Sie eine wesentlich präzisere Steuerung des schwenken.

Der folgende Code Ruft die [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) -Struktur aus dem *LPARAM* ab, speichert die letzte y-Koordinate aus der-Struktur und bestimmt die Änderung an der Position, an der das Bild Lauf leisten Objekt aktualisiert wird. Der folgende Code sollte in der **WndProc** Switch-Anweisung abgelegt werden.


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



Wenn Sie nun die Schwenkbewegung im Fenster ausführen, wird der Text mit Trägheit angezeigt. An diesem Punkt können Sie den Text so ändern, dass er mehr Zeilen hat, damit Sie das Schwenken von großen Textabschnitten durchsuchen können.

## <a name="boundary-feedback-in-wndproc"></a>Begrenzungs Feedback in WndProc

Das Feedback von Grenzen ist eine Art visuelles Feedback, das Benutzern bereitgestellt wird, wenn Sie das Ende eines Platz alisier baren Bereichs erreichen. Sie wird von der Anwendung ausgelöst, wenn eine Grenze erreicht wird. In der vorherigen Beispiel Implementierung der [**WM- \_ Gesten**](wm-gesture.md) Nachricht wird die Endbedingung `(si.nPos == si.yPos)` aus dem Fall der **WM- \_ Geste** verwendet, um zu testen, ob Sie das Ende eines Bare-Bereichs erreicht haben. Die folgenden Variablen werden verwendet, um Werte und Test Fehler zu verfolgen.


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



Die Groß-/Kleinschreibung wird aktualisiert, um das Feedback zu Grenzen zu initiieren Der folgende Code veranschaulicht die Groß-/Kleinschreibung der **gid \_** aus dem [**WM- \_ Gesten**](wm-gesture.md) Nachrichten Handler.


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



Das Fenster der Anwendung sollte nun über ein Begrenzungs Feedback verfügen, wenn sich ein Benutzer hinter dem unteren Rand des Bild Lauf leisten Bereichs befindet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Touchgesten](guide-multi-touch-gestures.md)
</dt> <dt>

[**Beginpanningfeedback**](/windows/win32/api/uxtheme/nf-uxtheme-beginpanningfeedback)
</dt> <dt>

[**Endpanningfeedback**](/windows/win32/api/uxtheme/nf-uxtheme-endpanningfeedback)
</dt> <dt>

[**Updatepanningfeedback**](/windows/win32/api/uxtheme/nf-uxtheme-updatepanningfeedback)
</dt> </dl>

 

 