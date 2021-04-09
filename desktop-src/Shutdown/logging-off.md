---
description: Die exitwindows-Funktion meldet den aktuellen Benutzer ab. Sie können auch die ExitWindowsEx-Funktion mit dem Flag für die EXW-Abmeldung aufzurufen \_ .
ms.assetid: 906d92f1-7cbe-454e-9c71-34b4383aebab
title: Abmelden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0571c0522c494acd763d57dcae8d200125cd53d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869232"
---
# <a name="logging-off"></a><span data-ttu-id="73eac-104">Abmelden</span><span class="sxs-lookup"><span data-stu-id="73eac-104">Logging Off</span></span>

<span data-ttu-id="73eac-105">Die [**exitwindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) -Funktion meldet den aktuellen Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="73eac-105">The [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) function logs off the current user.</span></span> <span data-ttu-id="73eac-106">Sie können auch die [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) -Funktion mit dem Flag für die EXW-Abmeldung aufzurufen \_ .</span><span class="sxs-lookup"><span data-stu-id="73eac-106">You can also call the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) function with the EXW\_LOGOFF flag.</span></span>

<span data-ttu-id="73eac-107">Wenn eine Anwendung [**exitwindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) oder [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) verwendet, um sich abzumelden, sendet das System standardmäßig die [**WM-Abfrage " \_ queryendsession**](wm-queryendsession.md) " an jedes Fenster.</span><span class="sxs-lookup"><span data-stu-id="73eac-107">By default, when an application uses [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) or [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) to log off, the system sends the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message to each window.</span></span> <span data-ttu-id="73eac-108">Anwendungen Stimmen zu beenden, indem Sie " **true** " zurückgeben, wenn diese Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="73eac-108">Applications agree to terminate by returning **TRUE** when they receive this message.</span></span> <span data-ttu-id="73eac-109">Wenn eine Anwendung bei der Verarbeitung dieser Nachricht **false** zurückgibt, wird der Abmeldevorgang abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="73eac-109">If any application returns **FALSE** when processing this message, the log-off operation is canceled.</span></span> <span data-ttu-id="73eac-110">Wenn Ihre Anwendung die **WM- \_ queryendsession** -Nachricht behandelt, können Sie zulassen, dass der Benutzer den Abmeldevorgang abbrechen kann, auch wenn eine andere Anwendung oder das System die Anforderung der Endsitzung verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="73eac-110">If your application handles the **WM\_QUERYENDSESSION** message, you can allow the user to cancel the log-off operation, even if another application or the system originated the end-session request.</span></span> <span data-ttu-id="73eac-111">Ein Beispiel finden Sie unter [Abmelden des aktuellen Benutzers](how-to-log-off-the-current-user.md).</span><span class="sxs-lookup"><span data-stu-id="73eac-111">For an example, see [How to Log Off the Current User](how-to-log-off-the-current-user.md).</span></span>

<span data-ttu-id="73eac-112">Wenn eine Anwendung **true** für [**WM \_ queryendsession**](wm-queryendsession.md)zurückgibt, empfängt Sie die [**WM- \_ endsitzungs**](wm-endsession.md) Nachricht und wird beendet, unabhängig davon, wie die anderen Anwendungen auf die **WM- \_ queryendsession** -Nachricht reagieren.</span><span class="sxs-lookup"><span data-stu-id="73eac-112">When an application returns **TRUE** for [**WM\_QUERYENDSESSION**](wm-queryendsession.md), it receives the [**WM\_ENDSESSION**](wm-endsession.md) message and it is terminated, regardless of how the other applications respond to the **WM\_QUERYENDSESSION** message.</span></span>

<span data-ttu-id="73eac-113">Um das Beenden aller Anwendungen zu erzwingen, verwenden Sie [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex), und geben Sie das EXW \_ Force-Flag an.</span><span class="sxs-lookup"><span data-stu-id="73eac-113">To force all applications to terminate, use [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex), and specify the EXW\_FORCE flag.</span></span> <span data-ttu-id="73eac-114">Dadurch wird verhindert, dass das System [**WM- \_ queryendsession**](wm-queryendsession.md) -Nachrichten sendet.</span><span class="sxs-lookup"><span data-stu-id="73eac-114">This prevents the system from sending [**WM\_QUERYENDSESSION**](wm-queryendsession.md) messages.</span></span>

<span data-ttu-id="73eac-115">Das System sendet \_ \_ während eines Abmelde Vorgangs auch das STRG-Abmelde Ereignis-Steuerungs Signal an jeden Prozess.</span><span class="sxs-lookup"><span data-stu-id="73eac-115">The system also sends the CTRL\_LOGOFF\_EVENT control signal to every process during a log-off operation.</span></span> <span data-ttu-id="73eac-116">Eine Konsolenanwendung kann eine [**Handlerroutine**](/windows/console/handlerroutine) registrieren, um diese Nachrichten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="73eac-116">A console application can register a [**HandlerRoutine**](/windows/console/handlerroutine) to process these messages.</span></span>

<span data-ttu-id="73eac-117">Wenn der Prozess, der [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) aufgerufen hat, in der Anmelde Sitzung des interaktiven Benutzers ausgeführt wird, werden alle Prozesse in der Anmelde Sitzung beendet.</span><span class="sxs-lookup"><span data-stu-id="73eac-117">If the process that called [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) is running in the logon session of the interactive user, all processes in the logon session are terminated.</span></span> <span data-ttu-id="73eac-118">Wenn sich der Prozess, der **ExitWindowsEx** aufgerufen hat, in einer anderen Anmelde Sitzung befindet, werden nur die Benachrichtigungen durchgeführt. keine Prozesse werden beendet.</span><span class="sxs-lookup"><span data-stu-id="73eac-118">If the process calling **ExitWindowsEx** is in some other logon session, only the notifications are made; no processes are terminated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73eac-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="73eac-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73eac-120">Abmelden des aktuellen Benutzers</span><span class="sxs-lookup"><span data-stu-id="73eac-120">How to Log Off the Current User</span></span>](how-to-log-off-the-current-user.md)
</dt> </dl>

 

 
