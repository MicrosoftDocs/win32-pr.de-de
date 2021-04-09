---
title: Video Aufzeichnung eines minimalen Ansatzes
description: Video Aufzeichnung eines minimalen Ansatzes
ms.assetid: e39ff590-69c0-4927-90c2-786c6082068f
keywords:
- Video für Windows (Vfw), Video Erfassung
- VFW (Video für Windows), Video Erfassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a65d5d5bbdc00dfd947c5d917e514d72e3ac069
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858194"
---
# <a name="video-capture-a-minimal-approach"></a>Video Erfassung: ein minimaler Ansatz

Die Video Erfassung digitalisiert einen Stream von Video-und Audiodaten und speichert Sie auf einer Festplatte oder einem anderen Typ von persistenten Speichergeräten. In diesem Abschnitt wird beschrieben, wie einer Anwendung mithilfe von drei Code Anweisungen eine einfache Form der Videoaufzeichnung hinzugefügt wird. Außerdem wird beschrieben, wie Sie eine Aufzeichnungs Sitzung beenden oder Abbrechen, indem Sie Nachrichten an das Aufzeichnungs Fenster senden.

Ein avicap-Erfassungsfenster behandelt die Details der Streaming-Audiodaten und Video Erfassung an AVI-Dateien. Dadurch kann Ihre Anwendung nicht mehr in das AVI-Dateiformat, die Video-und audiopufferverwaltung und den Zugriff auf Low-Level-Gerätetreiber einbezogen werden. Avicap bietet eine flexible Oberfläche für Anwendungen. Sie können Ihrer Anwendung Video Erfassung hinzufügen, indem Sie nur die folgenden Codezeilen verwenden:


```C++
hWndC = capCreateCaptureWindow ( "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE , 0, 0, 160, 120, hwndParent, nID);

SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0 /* wIndex */, 0L);

SendMessage (hWndC, WM_CAP_SEQUENCE, 0, 0L);
 
```



Es ist auch eine Makro Schnittstelle verfügbar, die eine Alternative zur Verwendung der [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion und zur Verbesserung der Lesbarkeit einer Anwendung bietet. Im folgenden Beispiel wird die Makro Schnittstelle verwendet, um eine Video Erfassung zu einer Anwendung hinzuzufügen.


```C++
hWndC = capCreateCaptureWindow (   "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE ,   0, 0, 160, 120, hwndParent, nID);

capDriverConnect (hWndC, 0);

capCaptureSequence (hWndC); 
 
```



Nachdem Ihre Anwendung ein Aufzeichnungs Fenster der avicap-Fenster Klasse erstellt und eine Verbindung mit einem Videotreiber hergestellt hat, ist das Erfassungsfenster zum Erfassen von Daten bereit. An diesem Punkt kann die Anwendung einfach die WM- [**\_ Cap- \_ Sequenz**](wm-cap-sequence.md) Nachricht (oder das [**capcapturesequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) -Makro) senden, um die Erfassung zu beginnen.

Mithilfe der Standardeinstellungen \_ \_ initiiert die WM-Cap-Sequenz die Erfassung von Video-und Audioeingaben in eine Datei mit dem Namen CAPTURE.AVI. Die Erfassung wird fortgesetzt, bis eines der folgenden Ereignisse eintritt:

-   Der Benutzer drückt die ESC-Taste oder eine Maustaste.
-   Die Anwendung beendet den Aufzeichnungs Vorgang oder bricht ihn ab.
-   Der Datenträger wird voll.

In einer Anwendung können Sie das Streaming erfasster Daten in eine Datei beenden, indem Sie die "WM Cap"-Meldung " [**\_ \_ Beenden**](wm-cap-stop.md) " (oder die " [**capcapturestoppt**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) "-Makro) an ein Aufzeichnungs Fenster senden Sie können den Aufzeichnungs Vorgang auch abbrechen, indem Sie die [**WM- \_ Cap- \_ Abbruch**](wm-cap-abort.md) Nachricht (oder das " [**capcaptureabort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) "-Makro) an ein Aufzeichnungs Fenster senden.

 

 