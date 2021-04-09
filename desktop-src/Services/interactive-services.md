---
description: In der Regel sind Dienste Konsolen Anwendungen, die ohne grafische Benutzeroberfläche (GUI) unbeaufsichtigt ausgeführt werden sollen.
ms.assetid: 3d6e090a-00b1-47d8-a4fb-620f3db8ba9c
title: Interaktive Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dda3018b4b37e8c5ee56d67cd1db2c56da9b67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867611"
---
# <a name="interactive-services"></a>Interaktive Dienste

In der Regel sind Dienste Konsolen Anwendungen, die ohne grafische Benutzeroberfläche (GUI) unbeaufsichtigt ausgeführt werden sollen. Einige Dienste erfordern jedoch möglicherweise gelegentliche Interaktionen mit einem Benutzer. Auf dieser Seite werden die besten Möglichkeiten zur Interaktion mit dem Benutzer von einem Dienst erläutert.

> [!IMPORTANT]
> Dienste können nicht direkt mit einem Benutzer in Windows Vista interagieren. Daher sollten die im Abschnitt mit einem interaktiven Dienst erwähnten Verfahren nicht in neuem Code verwendet werden.

 

## <a name="interacting-with-a-user-from-a-service-indirectly"></a>Indirekte Interaktion mit einem Benutzer von einem Dienst

Sie können die folgenden Verfahren verwenden, um mit dem Benutzer von einem Dienst auf allen unterstützten Versionen von Windows zu interagieren:

-   Zeigt ein Dialogfeld in der Benutzersitzung mithilfe der [**wtssendmessage**](/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssendmessagea) -Funktion an.
-   Erstellen Sie eine separate ausgeblendete GUI-Anwendung, und verwenden Sie die Funktion "Funktion", [**um die Anwendung**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) im Kontext des interaktiven Benutzers auszuführen. Entwerfen Sie die GUI-Anwendung für die Kommunikation mit dem Dienst über eine Methode der prozessübergreifenden Kommunikation (prozessübergreifende Communication, IPC), z. b. Named Pipes. Der Dienst kommuniziert mit der GUI-Anwendung, um ihm mitzuteilen, wann die GUI angezeigt werden soll. Die Anwendung kommuniziert die Ergebnisse der Benutzerinteraktion zurück an den Dienst, sodass der Dienst die geeignete Aktion ausführen kann. Beachten Sie, dass IPC Ihre Dienst Schnittstellen über das Netzwerk verfügbar machen kann, es sei denn, Sie verwenden eine geeignete Zugriffs Steuerungs Liste (ACL).

    Wenn dieser Dienst auf einem System mit mehreren Benutzern ausgeführt wird, fügen Sie die Anwendung dem folgenden Schlüssel hinzu, damit Sie in jeder Sitzung ausgeführt wird: **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run**. Wenn die Anwendung Named Pipes für IPC verwendet, kann der Server zwischen mehreren Benutzer Prozessen unterscheiden, indem jeder Pipe basierend auf der Sitzungs-ID ein eindeutiger Name übergeben wird.

Die folgende Technik ist auch für Windows Server 2003 und Windows XP verfügbar:

-   Zeigen Sie ein Meldungs Feld an, indem Sie die [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) -Funktion mit **MB \_ Dienst \_ Benachrichtigung** aufrufen. Dies wird empfohlen, um einfache Statusmeldungen anzuzeigen. Sie können **MessageBox** während der Dienst Initialisierung oder der [**handlerex**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) -Routine nicht aufrufen, es sei denn, Sie nennen Sie von einem separaten Thread aus, sodass Sie schnell zum SCM zurückkehren.

## <a name="using-an-interactive-service"></a>Verwenden eines interaktiven Dienstanbieter

Standardmäßig verwenden Dienste eine nicht interaktive [Fenster Station](/windows/desktop/winstation/window-stations) und können nicht mit dem Benutzer interagieren. Ein *interaktiver Dienst* kann jedoch eine Benutzeroberfläche anzeigen und Benutzereingaben erhalten.

> [!Caution]  
> Dienste, die in einem Sicherheitskontext mit erhöhten Rechten ausgeführt werden, z. b. das LocalSystem-Konto, sollten auf dem interaktiven Desktop kein Fenster erstellen, da jede andere Anwendung, die auf dem interaktiven Desktop ausgeführt wird, mit diesem Fenster interagieren kann. Dadurch wird der Dienst für jede Anwendung verfügbar gemacht, die von einem angemeldeten Benutzer ausgeführt wird. Außerdem sollten Dienste, die als "LocalSystem" ausgeführt werden, nicht durch Aufrufen der [**openwindowstation**](/windows/desktop/api/winuser/nf-winuser-openwindowstationa) -oder [**getthreaddesktop-**](/windows/desktop/api/winuser/nf-winuser-getthreaddesktop) Funktion auf den interaktiven Desktop zugreifen.

 

Um einen interaktiven Dienst zu erstellen, führen Sie die folgenden Schritte aus, wenn Sie die [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) -Funktion aufrufen:

1.  Geben Sie NULL für den *lpservicestartname* -Parameter an, um den Dienst im Kontext des [Kontos "LocalSystem](localsystem-account.md)" auszuführen.
2.  Geben Sie das **Dienst \_ interaktive \_ prozessflag** an.

Um zu ermitteln, ob ein Dienst als interaktiver Dienst ausgeführt wird, rufen Sie die [**getprocesswindowstation**](/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation) -Funktion auf, um ein Handle für die Fenster Station abzurufen, und die [**getuserobjectinformation**](/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa) -Funktion, um zu testen, ob die Fenster Station über das **\_ sichtbare WSF** -Attribut verfügt.

Beachten Sie jedoch, dass der folgende Registrierungsschlüssel den Wert " **nointeractiveservices**" enthält, der die Auswirkung des \_ interaktiven Dienst \_ Vorgangs steuert:

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Windows**

Der **nointeractiveservices** -Wert ist standardmäßig auf 1 festgelegt. Dies bedeutet, dass kein Dienst interaktiv ausgeführt werden darf, unabhängig davon, ob der **Dienst \_ interaktiv \_ verarbeitet** wird. Wenn **nointeractiveservices** auf "0" festgelegt ist, können Dienste mit **\_ interaktivem Dienst \_ Prozess** interaktiv ausgeführt werden.

**Windows 7, Windows Server 2008 R2, Windows XP und Windows Server 2003:** Der **nointeractiveservices** -Wert ist standardmäßig auf 0 festgelegt. Dies bedeutet, dass Dienste mit **\_ interaktivem Dienst \_ Prozess** interaktiv ausgeführt werden können. Wenn **nointeractiveservices** auf einen Wert ungleich 0 (null) festgelegt ist, kann kein Dienst, der danach gestartet wird, interaktiv ausgeführt werden, unabhängig davon, ob der **Dienst \_ interaktiv \_ verarbeitet** wird.

> [!IMPORTANT]
> Alle-Dienste werden in Terminal Dienste-Sitzung 0 ausgeführt. Wenn ein interaktiver Dienst also eine Benutzeroberfläche anzeigt, wird er nur für den Benutzer angezeigt, der eine Verbindung mit Sitzung 0 hergestellt hat. Da es nicht möglich ist, sicherzustellen, dass der interaktive Benutzer mit Sitzung 0 verbunden ist, sollten Sie einen Dienst nicht so konfigurieren, dass er als interaktiver Dienst unter Terminal Diensten oder auf einem System ausgeführt wird, das die schnelle Benutzerumschaltung unterstützt (schnelle Benutzerumschaltung wird mithilfe von Terminal Diensten implementiert).

 

 

 
