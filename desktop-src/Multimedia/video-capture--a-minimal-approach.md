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
# <a name="video-capture-a-minimal-approach"></a><span data-ttu-id="cc3cd-105">Video Erfassung: ein minimaler Ansatz</span><span class="sxs-lookup"><span data-stu-id="cc3cd-105">Video Capture: A Minimal Approach</span></span>

<span data-ttu-id="cc3cd-106">Die Video Erfassung digitalisiert einen Stream von Video-und Audiodaten und speichert Sie auf einer Festplatte oder einem anderen Typ von persistenten Speichergeräten.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-106">Video capture digitizes a stream of video and audio data, and stores it on a hard disk or some other type of persistent storage device.</span></span> <span data-ttu-id="cc3cd-107">In diesem Abschnitt wird beschrieben, wie einer Anwendung mithilfe von drei Code Anweisungen eine einfache Form der Videoaufzeichnung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-107">This section describes how to add a simple form of video capture to an application using three statements of code.</span></span> <span data-ttu-id="cc3cd-108">Außerdem wird beschrieben, wie Sie eine Aufzeichnungs Sitzung beenden oder Abbrechen, indem Sie Nachrichten an das Aufzeichnungs Fenster senden.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-108">It also describes how to end or abort a capture session by sending messages to the capture window.</span></span>

<span data-ttu-id="cc3cd-109">Ein avicap-Erfassungsfenster behandelt die Details der Streaming-Audiodaten und Video Erfassung an AVI-Dateien.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-109">An AVICap capture window handles the details of streaming audio and video capture to AVI files.</span></span> <span data-ttu-id="cc3cd-110">Dadurch kann Ihre Anwendung nicht mehr in das AVI-Dateiformat, die Video-und audiopufferverwaltung und den Zugriff auf Low-Level-Gerätetreiber einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-110">This frees your application from involvement in the AVI file format, video and audio buffer management, and the low-level access of video and audio device drivers.</span></span> <span data-ttu-id="cc3cd-111">Avicap bietet eine flexible Oberfläche für Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-111">AVICap provides a flexible interface for applications.</span></span> <span data-ttu-id="cc3cd-112">Sie können Ihrer Anwendung Video Erfassung hinzufügen, indem Sie nur die folgenden Codezeilen verwenden:</span><span class="sxs-lookup"><span data-stu-id="cc3cd-112">You can add video capture to your application, using only the following lines of code:</span></span>


```C++
hWndC = capCreateCaptureWindow ( "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE , 0, 0, 160, 120, hwndParent, nID);

SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0 /* wIndex */, 0L);

SendMessage (hWndC, WM_CAP_SEQUENCE, 0, 0L);
 
```



<span data-ttu-id="cc3cd-113">Es ist auch eine Makro Schnittstelle verfügbar, die eine Alternative zur Verwendung der [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion und zur Verbesserung der Lesbarkeit einer Anwendung bietet.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-113">A macro interface is also available that provides an alternative to using the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function and improves the readability of an application.</span></span> <span data-ttu-id="cc3cd-114">Im folgenden Beispiel wird die Makro Schnittstelle verwendet, um eine Video Erfassung zu einer Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-114">The following example uses the macro interface to add video capture to an application.</span></span>


```C++
hWndC = capCreateCaptureWindow (   "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE ,   0, 0, 160, 120, hwndParent, nID);

capDriverConnect (hWndC, 0);

capCaptureSequence (hWndC); 
 
```



<span data-ttu-id="cc3cd-115">Nachdem Ihre Anwendung ein Aufzeichnungs Fenster der avicap-Fenster Klasse erstellt und eine Verbindung mit einem Videotreiber hergestellt hat, ist das Erfassungsfenster zum Erfassen von Daten bereit.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-115">After your application creates a capture window of the AVICap window class and connects it to a video driver, the capture window is ready to capture data.</span></span> <span data-ttu-id="cc3cd-116">An diesem Punkt kann die Anwendung einfach die WM- [**\_ Cap- \_ Sequenz**](wm-cap-sequence.md) Nachricht (oder das [**capcapturesequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) -Makro) senden, um die Erfassung zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-116">At this point, your application can simply send the [**WM\_CAP\_SEQUENCE**](wm-cap-sequence.md) message (or the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro) to begin capturing.</span></span>

<span data-ttu-id="cc3cd-117">Mithilfe der Standardeinstellungen \_ \_ initiiert die WM-Cap-Sequenz die Erfassung von Video-und Audioeingaben in eine Datei mit dem Namen CAPTURE.AVI.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-117">Using default settings, WM\_CAP\_SEQUENCE initiates the capture of video and audio input to a file named CAPTURE.AVI.</span></span> <span data-ttu-id="cc3cd-118">Die Erfassung wird fortgesetzt, bis eines der folgenden Ereignisse eintritt:</span><span class="sxs-lookup"><span data-stu-id="cc3cd-118">Capture continues until one of the following events occurs:</span></span>

-   <span data-ttu-id="cc3cd-119">Der Benutzer drückt die ESC-Taste oder eine Maustaste.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-119">The user presses the ESC key or a mouse button.</span></span>
-   <span data-ttu-id="cc3cd-120">Die Anwendung beendet den Aufzeichnungs Vorgang oder bricht ihn ab.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-120">Your application stops or aborts capture operation.</span></span>
-   <span data-ttu-id="cc3cd-121">Der Datenträger wird voll.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-121">The disk becomes full.</span></span>

<span data-ttu-id="cc3cd-122">In einer Anwendung können Sie das Streaming erfasster Daten in eine Datei beenden, indem Sie die "WM Cap"-Meldung " [**\_ \_ Beenden**](wm-cap-stop.md) " (oder die " [**capcapturestoppt**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) "-Makro) an ein Aufzeichnungs Fenster senden</span><span class="sxs-lookup"><span data-stu-id="cc3cd-122">In an application, you can stop streaming captured data to a file by sending the [**WM\_CAP\_STOP**](wm-cap-stop.md) (or the [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) macro) message to a capture window.</span></span> <span data-ttu-id="cc3cd-123">Sie können den Aufzeichnungs Vorgang auch abbrechen, indem Sie die [**WM- \_ Cap- \_ Abbruch**](wm-cap-abort.md) Nachricht (oder das " [**capcaptureabort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) "-Makro) an ein Aufzeichnungs Fenster senden.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-123">You can also abort the capture operation by sending the [**WM\_CAP\_ABORT**](wm-cap-abort.md) message (or the [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) macro) to a capture window.</span></span>

 

 