---
title: Fehlermeldungen und Benachrichtigungen
description: Fehlermeldungen und Benachrichtigungen
ms.assetid: 7f804364-d8be-4e52-ab0e-fba05bcf76ce
keywords:
- Mciwndgeterror-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e40e78c72dc378baa37b56dbb2d5718ae2d85b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038886"
---
# <a name="error-messages-and-notifications"></a><span data-ttu-id="082cb-104">Fehlermeldungen und Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="082cb-104">Error Messages and Notifications</span></span>

<span data-ttu-id="082cb-105">Mciwnd verwendet MCI zum Steuern der Geräte, die Multimedia-Daten wiedergeben und aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="082cb-105">MCIWnd uses MCI to control the devices that play and record multimedia data.</span></span> <span data-ttu-id="082cb-106">Im Allgemeinen zeigt mciwnd MCI-Fehler in einem Fehler Dialogfeld an.</span><span class="sxs-lookup"><span data-stu-id="082cb-106">In general, MCIWnd displays MCI errors in an error dialog box.</span></span> <span data-ttu-id="082cb-107">Ein MCI-Fehler wird generiert, wenn ein MCI-Befehl fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="082cb-107">An MCI error is generated whenever an MCI command fails.</span></span> <span data-ttu-id="082cb-108">Wenn die Anwendung z. b. versucht, die angehaltene Wiedergabe mit dem [**mciwndresume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) -Makro fortzusetzen, und das aktuelle Gerät die Wiederaufnahme nicht unterstützt, wird dem Benutzer ein Fehler gemeldet.</span><span class="sxs-lookup"><span data-stu-id="082cb-108">For example, if your application tries to resume paused playback by using the [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) macro and the current device does not support resume, an error is reported to the user.</span></span>

<span data-ttu-id="082cb-109">Mciwnd ermöglicht Ihnen zwei Optionen für die Behandlung von Fehlermeldungen:</span><span class="sxs-lookup"><span data-stu-id="082cb-109">MCIWnd allows you two choices for handling error messages:</span></span>

-   <span data-ttu-id="082cb-110">Sie können verhindern, dass Fehlermeldungen den Benutzer erreichen.</span><span class="sxs-lookup"><span data-stu-id="082cb-110">You can prevent error messages from reaching the user.</span></span> <span data-ttu-id="082cb-111">Wenn Sie die Anzeige von MCI-Fehlermeldungen verhindern möchten, geben Sie das Fenster Format mciwndf \_ noerrordlg an, wenn Sie eine Instanz eines mciwnd-Fensters mithilfe der Funktion " [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) " oder " [deatewindowex](/windows/win32/api/winuser/nf-winuser-createwindowexa) " erstellen.</span><span class="sxs-lookup"><span data-stu-id="082cb-111">To prevent the display of MCI error messages, specify the MCIWNDF\_NOERRORDLG window style when you create an instance of an MCIWnd window by using the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) or [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span>
-   <span data-ttu-id="082cb-112">Sie können Sie zur Anzeige an Ihre Anwendung umleiten.</span><span class="sxs-lookup"><span data-stu-id="082cb-112">You can redirect them to your application for display.</span></span> <span data-ttu-id="082cb-113">Wenn Sie MCI-Fehlermeldungen an Ihre Anwendung umleiten möchten, geben Sie das Fenster Format mciwndf \_ notifyerror an, wenn Sie eine Instanz eines mciwnd-Fensters mithilfe von " **mciwndcreate** " oder " **kreatewindowex**" erstellen.</span><span class="sxs-lookup"><span data-stu-id="082cb-113">To redirect MCI error messages to your application, specify the MCIWNDF\_NOTIFYERROR window style when you create an instance of an MCIWnd window by using **MCIWndCreate** or **CreateWindowEx**.</span></span>

<span data-ttu-id="082cb-114">Wenn die Fehler Benachrichtigung aktiviert ist, sendet mciwnd jede Benachrichtigungs Meldung ([**mciwndm \_ notifyerror**](mciwndm-notifyerror.md)) an den Hauptnachrichten Handler des übergeordneten Elements des mciwnd-Fensters.</span><span class="sxs-lookup"><span data-stu-id="082cb-114">When error notification is enabled, MCIWnd sends each notification message ([**MCIWNDM\_NOTIFYERROR**](mciwndm-notifyerror.md)) to the main message handler of the parent of the MCIWnd window.</span></span> <span data-ttu-id="082cb-115">Die Anwendung muss über einen Nachrichten Handler verfügen, um die empfangenen Benachrichtigungs Meldungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="082cb-115">Your application must have a message handler to process the notification messages it receives.</span></span>

<span data-ttu-id="082cb-116">Eine Textbeschreibung der neuesten MCI-Fehlermeldung erhalten Sie, indem Sie das [**mciwndgeterror**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="082cb-116">You can obtain a textual description of the most recent MCI error message by using the [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) macro.</span></span> <span data-ttu-id="082cb-117">Dieses Makro gibt den Text in einem Anwendungs definierten Puffer zurück.</span><span class="sxs-lookup"><span data-stu-id="082cb-117">This macro returns the text in an application-defined buffer.</span></span> <span data-ttu-id="082cb-118">Wenn die Fehler Zeichenfolge länger als der Puffer ist, wird die Zeichenfolge von mciwnd abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="082cb-118">If the error string is longer than the buffer, MCIWnd truncates the string.</span></span>

<span data-ttu-id="082cb-119">Sie können alle Benachrichtigungen mithilfe des [**mciwndseetowner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) -Makros an ein anderes Fenster weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="082cb-119">You can route all notifications to another window by using the [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) macro.</span></span>

 

 