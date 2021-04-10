---
description: Im folgenden Beispiel wird die exitwindows-Funktion verwendet, um den aktuellen Benutzer abzumelden.
ms.assetid: 74be3505-c4bd-4ae2-aaed-700382839006
title: Abmelden des aktuellen Benutzers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e59ce625ae7da8a2a4a901fbb1429ab0f9b638c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959721"
---
# <a name="how-to-log-off-the-current-user"></a><span data-ttu-id="375ce-103">Abmelden des aktuellen Benutzers</span><span class="sxs-lookup"><span data-stu-id="375ce-103">How to Log Off the Current User</span></span>

<span data-ttu-id="375ce-104">Im folgenden Beispiel wird die [**exitwindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) -Funktion verwendet, um den aktuellen Benutzer abzumelden.</span><span class="sxs-lookup"><span data-stu-id="375ce-104">The following example uses the [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) function to log off the current user.</span></span>

``` syntax
// Log off the current user. 

ExitWindows(0, 0);
```

<span data-ttu-id="375ce-105">Im folgenden Beispiel wird die [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) -Funktion verwendet, um den aktuellen Benutzer abzumelden.</span><span class="sxs-lookup"><span data-stu-id="375ce-105">The following example uses the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) function to log off the current user.</span></span>

``` syntax
// Log off the current user. 

ExitWindowsEx(EWX_LOGOFF, 0);
```

<span data-ttu-id="375ce-106">Die Anwendung empfängt die [**WM- \_ Abfrage "queryendsession**](wm-queryendsession.md) " und zeigt ein Dialogfeld an, in dem Sie gefragt werden, ob das Beenden der Sitzung in Ordnung ist.</span><span class="sxs-lookup"><span data-stu-id="375ce-106">The application receives the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message and displays a dialog box asking the whether it is OK to end the session.</span></span> <span data-ttu-id="375ce-107">Wenn der Benutzer auf **Ja** klickt, meldet das System den Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="375ce-107">If the user clicks **Yes**, the system logs off the user.</span></span> <span data-ttu-id="375ce-108">Wenn der Benutzer auf **Nein** klickt, wird die Abmeldung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="375ce-108">If the user clicks **No**, the logoff is canceled.</span></span>

``` syntax
// Process the message in the window procedure. 

case WM_QUERYENDSESSION:  
{ 
    int r; 
    r = MessageBox(NULL,(LPCWSTR)L"End the session?",(LPCWSTR)L"WM_QUERYENDSESSION",MB_YESNO);
 
    // Return TRUE to continue, FALSE to stop. 
 
    return r == IDYES; 
    break; 
}
```

## <a name="related-topics"></a><span data-ttu-id="375ce-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="375ce-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="375ce-110">Abmelden</span><span class="sxs-lookup"><span data-stu-id="375ce-110">Logging Off</span></span>](logging-off.md)
</dt> </dl>

 

 



