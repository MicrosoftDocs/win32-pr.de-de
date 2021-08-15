---
title: Verbessern des Single-Finger Schwenkens
description: Wenn Sie eine Anwendung erstellen, die auf Windows Touch abzielt, bietet sie automatisch grundlegende Schwenkunterstützung. Sie können jedoch die WM GESTURE-Nachricht verwenden, \_ um erweiterte Unterstützung für das Einfinger-Schwenken bereitzustellen.
ms.assetid: eb01a6df-9969-44d1-a657-4f83fb0b67cb
keywords:
- Windows Toucheingabe, Einzelfinger-Schwenken
- Windows Toucheingabe, Schwenken
- Windows Toucheingabe, Scrollleisten
- Windows Toucheingabe, Fingereingaben
- Windows Toucheingabe, Gesten-Schwenknachrichten
- Windows Toucheingabe, Begrenzungsfeedback
- Schwenken mit einem Finger
- Schwenken, Einzelfinger
- Schwenken, Begrenzungsfeedback
- Scrollleisten, Schwenken mit einem Finger
- Flackern, Einfinger-Schwenken
- Scrollleisten, deaktivieren
- Flackern,Deaktivieren
- Gesten, Gesten schwenken Nachrichten
- Schwenken, Gesten-Schwenken-Nachrichten
- Begrenzungsfeedback, Einzelfinger-Schwenken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf740d673e8bd2d2711238902d3de6c89d21a01fe330524b910db050011872f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435443"
---
# <a name="improving-the-single-finger-panning-experience"></a>Verbessern des Single-Finger Schwenkens

Wenn Sie eine Anwendung erstellen, die auf Windows Touch abzielt, bietet sie automatisch grundlegende Schwenkunterstützung. Sie können jedoch die [**WM \_ GESTURE-Nachricht**](wm-gesture.md) verwenden, um erweiterte Unterstützung für das Einfinger-Schwenken bereitzustellen.

## <a name="overview"></a>Übersicht

Um das Einfinger-Schwenken zu verbessern, verwenden Sie diese Schritte, wie in den nachfolgenden Abschnitten dieses Themas erläutert:

-   Erstellen Sie eine Anwendung mit Scrollleisten und deaktivierten Flimmern.
-   Unterstützung für Gesten-Schwenknachrichten hinzugefügt.
-   Aktivieren Sie "bounce".

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a>Erstellen einer Anwendung mit Scrollleisten und deaktivierten Flicks

Bevor Sie beginnen, müssen Sie eine Anwendung mit Scrollleisten erstellen. Dieser Vorgang wird im Abschnitt [Legacyunterstützung für das Schwenken mit Scrollleisten](legacy-support-for-panning-with-scrollbars.md) erläutert. Wenn Sie mit dem Beispielinhalt beginnen möchten, wechseln Sie zu diesem Abschnitt, und erstellen Sie eine Anwendung mit Scrollleisten, und deaktivieren Sie dann Flattern. Wenn Sie bereits über eine Anwendung mit funktionierenden Scrollleisten verfügen, deaktivieren Sie Dies ist in diesem Abschnitt beschrieben.

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a>Hinzufügen benutzerdefinierter Schwenkunterstützung für Gesten-Schwenknachrichten

Um Gesten-Schwenknachrichten zu unterstützen, müssen Sie sie in der **WndProc-Methode** behandeln. Die Gestennachrichten werden verwendet, um horizontale und vertikale Deltas für Schwenknachrichten zu bestimmen. Die Deltas werden verwendet, um das Bildlaufleistenobjekt zu aktualisieren, das die Benutzeroberfläche aktualisiert.

Aktualisieren Sie zunächst die Windows Versionseinstellungen in der Datei targetver.h, um Windows Touch zu aktivieren. Der folgende Code zeigt die verschiedenen Windows Versionseinstellungen, die diese in targetver.h ersetzen sollten.


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



Fügen Sie als Nächstes die Datei UXTheme.h ihrem Projekt hinzu, und fügen Sie die Bibliothek uxtheme.lib den zusätzlichen Abhängigkeiten Ihres Projekts hinzu.


```C++
#include <uxtheme.h>
```



Fügen Sie als Nächstes die folgenden Variablen am Anfang der **WndProc-Funktion** hinzu. Diese werden in Berechnungen zum Schwenken verwendet.


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



Fügen Sie als Nächstes den Handler für die [**WM \_ GESTURE-Nachricht**](wm-gesture.md) hinzu, damit die Scrollleisten basierend auf Schwenkgesten mit Deltas aktualisiert werden. Dadurch erhalten Sie eine viel differenziertere Steuerung des Schwenkens.

Der folgende Code ruft die [**GESTUREINFO-Struktur**](/windows/win32/api/winuser/ns-winuser-gestureinfo) aus dem *lParam* ab, speichert die letzte y-Koordinate aus der -Struktur und bestimmt die Positionsänderung, um das Bildlaufleistenobjekt zu aktualisieren. Der folgende Code sollte in Ihrer **WndProc** switch-Anweisung platziert werden.


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



Wenn Sie nun die Schwenkbewegung in Ihrem Fenster ausführen, wird der Text mit Trägheit gescrollt. An diesem Punkt möchten Sie möglicherweise den Text so ändern, dass er mehr Zeilen enthält, damit Sie das Schwenken großer Textabschnitte untersuchen können.

## <a name="boundary-feedback-in-wndproc"></a>Begrenzungsfeedback in WndProc

Begrenzungsfeedback ist eine Art visuelles Feedback, das Benutzern gegeben wird, wenn sie das Ende eines schwenkbaren Bereichs erreichen. Sie wird von der Anwendung ausgelöst, wenn eine Grenze erreicht wird. In der vorherigen Beispielimplementierungen der [**WM \_ GESTURE-Nachricht**](wm-gesture.md) wird die Endbedingung `(si.nPos == si.yPos)` aus dem WM **\_ GESTURE-Fall** verwendet, um zu testen, ob Sie das Ende eines schwenkbaren Bereichs erreicht haben. Die folgenden Variablen werden verwendet, um Werte und Testfehler nachzuverfolgen.


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



Der Schwenkgestenfall wird aktualisiert, um Begrenzungsfeedback auszulösen. Der folgende Code veranschaulicht den **GID \_ PAN-Fall** aus dem [**WM \_ GESTURE-Meldungshandler.**](wm-gesture.md)


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



Nun sollte das Fenster Ihrer Anwendung Begrenzungsfeedback aufweisen, wenn ein Benutzer über den unteren Rand des Scrollleistenbereichs schwenkt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Touchgesten](guide-multi-touch-gestures.md)
</dt> <dt>

[**BeginPanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-beginpanningfeedback)
</dt> <dt>

[**EndPanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-endpanningfeedback)
</dt> <dt>

[**UpdatePanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-updatepanningfeedback)
</dt> </dl>

 

 