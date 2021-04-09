---
description: Im folgenden Beispiel wird die Arbeitsstation mithilfe der Lock Workstation-Funktion gesperrt. Das System zeigt das Dialogfeld Arbeitsstation sperren an. Der Dialogfeld Text besagt, dass die Arbeitsstation verwendet wird und vom Benutzer gesperrt wurde.
ms.assetid: 7cbf9a0a-dfab-42e6-9a71-bb240121f59f
title: Vorgehensweise beim Sperren der Arbeitsstation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa6c198816613a13914c44a5a51f5317e2019f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865712"
---
# <a name="how-to-lock-the-workstation"></a><span data-ttu-id="42688-105">Vorgehensweise beim Sperren der Arbeitsstation</span><span class="sxs-lookup"><span data-stu-id="42688-105">How to Lock the Workstation</span></span>

<span data-ttu-id="42688-106">Im folgenden Beispiel wird die Arbeitsstation mithilfe der [**Lock Workstation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) -Funktion gesperrt.</span><span class="sxs-lookup"><span data-stu-id="42688-106">The following example locks the workstation using the [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) function.</span></span> <span data-ttu-id="42688-107">Das System zeigt das Dialogfeld **Arbeitsstation sperren** an.</span><span class="sxs-lookup"><span data-stu-id="42688-107">The system displays the **Lock Workstation** dialog box.</span></span> <span data-ttu-id="42688-108">Der Dialogfeld Text besagt, dass die Arbeitsstation verwendet wird und vom Benutzer gesperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="42688-108">The dialog box text says that the workstation is in use and has been locked by the user.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment( lib, "user32.lib" )

void main()
{
    // Lock the workstation.

    if( !LockWorkStation() )
        printf ("LockWorkStation failed with %d\n", GetLastError());
}
```



<span data-ttu-id="42688-109">Überprüfen Sie, ob das Fenster sichtbar ist, um zu bestimmen, ob die Arbeitsstation gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="42688-109">To determine whether the workstation is locked, test whether your window is visible.</span></span>

<span data-ttu-id="42688-110">Die Arbeitsstation kann vom Benutzer oder einem Administrator entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="42688-110">The workstation can be unlocked by the user or an administrator.</span></span> <span data-ttu-id="42688-111">Drücken Sie zum Entsperren des Systems STRG + ALT + ENTF, und melden Sie sich an.</span><span class="sxs-lookup"><span data-stu-id="42688-111">To unlock the system, press Ctrl+Alt+Del and log in.</span></span> <span data-ttu-id="42688-112">Um bei der Anmeldung des Benutzers eine Benachrichtigung zu erhalten, verwenden Sie die [**wzregistersessionnotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) -Funktion, um sich für den Empfang von [**WM- \_ \_ Änderungs**](../termserv/wm-wtssession-change.md) Nachrichten zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="42688-112">To receive notification when the user logs in, use the [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) function to register to receive [**WM\_WTSSESSION\_CHANGE**](../termserv/wm-wtssession-change.md) messages.</span></span> <span data-ttu-id="42688-113">Wenn diese Meldung empfangen wird, überprüfen Sie, ob der *wParam* -Parameter gleich der WTS- \_ Sitzungs \_ Sperre ist.</span><span class="sxs-lookup"><span data-stu-id="42688-113">When this message is received, check whether the *wParam* parameter is equal to WTS\_SESSION\_LOCK.</span></span>

 

 
