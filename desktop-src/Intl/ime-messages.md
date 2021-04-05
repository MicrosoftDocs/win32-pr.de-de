---
description: Das Betriebssystem sendet IME-Fenster Meldungen an die Fenster Prozedur einer Anwendung, wenn bestimmte Ereignisse auftreten, die sich auf die IME-Fenster auswirken.
ms.assetid: 7eac1ab7-d04b-4e1b-9e2c-fa9a778756cd
title: IME-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f30baa01081e0aca1423f3384926938e6fdc07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041802"
---
# <a name="ime-messages"></a><span data-ttu-id="52f01-103">IME-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="52f01-103">IME Messages</span></span>

<span data-ttu-id="52f01-104">Das Betriebssystem sendet IME-Fenster Meldungen an die Fenster Prozedur einer Anwendung, wenn bestimmte Ereignisse auftreten, die sich auf die IME-Fenster auswirken.</span><span class="sxs-lookup"><span data-stu-id="52f01-104">The operating system sends IME window messages to the window procedure of an application when certain events occur that affect the IME windows.</span></span> <span data-ttu-id="52f01-105">Beispielsweise sendet das Betriebssystem die " [**WM \_ IME \_ SetContext**](wm-ime-setcontext.md) "-Meldung an die Anwendung, wenn ein Fenster aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="52f01-105">For example, the operating system sends the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message to the application when a window is activated.</span></span> <span data-ttu-id="52f01-106">IME-unbekannte Anwendungen übergeben diese Nachrichten an die [defwindowproc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion, die Sie an das entsprechende Standard-IME-Fenster sendet.</span><span class="sxs-lookup"><span data-stu-id="52f01-106">IME-unaware applications pass these messages to the [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which sends them to the corresponding default IME window.</span></span> <span data-ttu-id="52f01-107">IME-fähige Anwendungen verarbeiten diese Nachrichten oder leiten Sie an Ihre eigenen IME-Fenster weiter.</span><span class="sxs-lookup"><span data-stu-id="52f01-107">IME-aware applications either process these messages or forward them to their own IME windows.</span></span>

<span data-ttu-id="52f01-108">Die Anwendung kann ein IME-Fenster anweisen, einen Befehl auszuführen, z. b. die Position eines Kompositions Fensters mithilfe der WM- [**\_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="52f01-108">Your application can direct an IME window to carry out a command, for example, change the position of a composition window, by using the [**WM\_IME\_CONTROL**](wm-ime-control.md) message.</span></span> <span data-ttu-id="52f01-109">Der IME benachrichtigt die Anwendung über Änderungen an der Kompositions Zeichenfolge unter Verwendung der [**WM \_ IME- \_ Kompositions**](wm-ime-composition.md) Nachricht und über allgemeine Änderungen am Status der IME-Fenster durch Senden der [**WM-IME- \_ \_ Benachrichtigungs**](wm-ime-notify.md) Meldung.</span><span class="sxs-lookup"><span data-stu-id="52f01-109">The IME notifies the application about changes to the composition string by using the [**WM\_IME\_COMPOSITION**](wm-ime-composition.md) message, and about general changes to the status of the IME windows by sending the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52f01-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="52f01-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52f01-111">Informationen über den Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="52f01-111">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 
