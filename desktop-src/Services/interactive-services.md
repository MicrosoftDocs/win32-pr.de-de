---
description: In der Regel handelt es sich bei Diensten um Konsolenanwendungen, die für die unbeaufsichtigte Ausführung ohne grafische Benutzeroberfläche (GUI) konzipiert sind.
ms.assetid: 3d6e090a-00b1-47d8-a4fb-620f3db8ba9c
title: Interactive Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6b99eb41d26d6740a30a314654d92fdd4522f5597ea6e4cbb2a3d443de8120
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889468"
---
# <a name="interactive-services"></a>Interactive Services

In der Regel handelt es sich bei Diensten um Konsolenanwendungen, die für die unbeaufsichtigte Ausführung ohne grafische Benutzeroberfläche (GUI) konzipiert sind. Einige Dienste erfordern jedoch möglicherweise eine gelegentliche Interaktion mit einem Benutzer. Auf dieser Seite werden die besten Möglichkeiten für die Interaktion mit dem Benutzer aus einem Dienst erläutert.

> [!IMPORTANT]
> Dienste können ab Windows Vista nicht direkt mit einem Benutzer interagieren. Daher sollten die im Abschnitt Using an Interactive Service (Verwenden eines interaktiven Diensts) erwähnten Techniken nicht in neuem Code verwendet werden.

 

## <a name="interacting-with-a-user-from-a-service-indirectly"></a>Indirekte Interaktion mit einem Benutzer aus einem Dienst

Sie können die folgenden Techniken verwenden, um mit dem Benutzer über einen Dienst in allen unterstützten Versionen von Windows zu interagieren:

-   Zeigen Sie ein Dialogfeld in der Sitzung des Benutzers mithilfe der [**WTSSendMessage-Funktion**](/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssendmessagea) an.
-   Erstellen Sie eine separate ausgeblendete GUI-Anwendung, und verwenden Sie die [**CreateProcessAsUser-Funktion,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) um die Anwendung im Kontext des interaktiven Benutzers auszuführen. Entwerfen Sie die GUI-Anwendung so, dass sie mit dem Dienst über eine Methode der prozessübergreifenden Kommunikation (Interprocess Communication, IPC) kommuniziert, z. B. Named Pipes. Der Dienst kommuniziert mit der GUI-Anwendung, um ihm mitzuteilen, wann die GUI angezeigt werden soll. Die Anwendung gibt die Ergebnisse der Benutzerinteraktion an den Dienst zurück, damit der Dienst die entsprechende Aktion ergreifen kann. Beachten Sie, dass IPC Ihre Dienstschnittstellen über das Netzwerk verfügbar machen kann, es sei denn, Sie verwenden eine entsprechende Zugriffssteuerungsliste (Access Control List, ACL).

    Wenn dieser Dienst auf einem Multiusersystem ausgeführt wird, fügen Sie die Anwendung dem folgenden Schlüssel hinzu, damit sie in jeder Sitzung ausgeführt wird: **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Run**. Wenn die Anwendung Named Pipes für IPC verwendet, kann der Server zwischen mehreren Benutzerprozessen unterscheiden, indem jeder Pipe basierend auf der Sitzungs-ID ein eindeutiger Name gegeben wird.

Das folgende Verfahren ist auch für Windows Server 2003 und Windows XP verfügbar:

-   Zeigen Sie ein Meldungsfeld an, indem Sie die [**MessageBox-Funktion**](/windows/win32/api/winuser/nf-winuser-messagebox) mit **MB SERVICE \_ \_ NOTIFICATION** aufrufen. Dies wird empfohlen, um einfache Statusmeldungen anzuzeigen. Rufen Sie **MessageBox** nicht während der Dienstinitialisierung oder über die [**HandlerEx-Routine**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) auf, es sei denn, Sie rufen sie aus einem separaten Thread auf, sodass Sie rechtzeitig zum SCM zurückkehren.

## <a name="using-an-interactive-service"></a>Verwenden eines interaktiven Diensts

Standardmäßig verwenden Dienste eine nicht interaktive [Fensterstation](/windows/desktop/winstation/window-stations) und können nicht mit dem Benutzer interagieren. Ein *interaktiver Dienst* kann jedoch eine Benutzeroberfläche anzeigen und Benutzereingaben empfangen.

> [!Caution]  
> Dienste, die in einem Sicherheitskontext mit erhöhten Rechten ausgeführt werden, z. B. das LocalSystem-Konto, sollten kein Fenster auf dem interaktiven Desktop erstellen, da jede andere Anwendung, die auf dem interaktiven Desktop ausgeführt wird, mit diesem Fenster interagieren kann. Dadurch wird der Dienst für jede Anwendung verfügbar gemacht, die ein angemeldeter Benutzer ausführt. Außerdem sollten Dienste, die als LocalSystem ausgeführt werden, nicht auf den interaktiven Desktop zugreifen, indem sie die [**Funktion OpenWindowStation**](/windows/desktop/api/winuser/nf-winuser-openwindowstationa) oder [**GetThreadDesktop**](/windows/desktop/api/winuser/nf-winuser-getthreaddesktop) aufrufen.

 

Um einen interaktiven Dienst zu erstellen, gehen Sie wie folgt vor, wenn Sie die [**CreateService-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) aufrufen:

1.  Geben Sie NULL für den *lpServiceStartName-Parameter* an, um den Dienst im Kontext des [LocalSystem-Kontos](localsystem-account.md)auszuführen.
2.  Geben Sie das **SERVICE \_ INTERACTIVE \_ PROCESS-Flag** an.

Um zu bestimmen, ob ein Dienst als interaktiver Dienst ausgeführt wird, rufen Sie die [**GetProcessWindowStation-Funktion**](/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation) auf, um ein Handle für die Fensterstation abzurufen, und die [**GetUserObjectInformation-Funktion,**](/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa) um zu testen, ob die Fensterstation über das **WSF \_ VISIBLE-Attribut** verfügt.

Beachten Sie jedoch, dass der folgende Registrierungsschlüssel den Wert **NoInteractiveServices** enthält, der die Auswirkung von SERVICE \_ INTERACTIVE PROCESS \_ steuert:

**HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Control \\ Windows**

Der **NoInteractiveServices-Wert** ist standardmäßig auf 1 eingestellt. Dies bedeutet, dass kein Dienst interaktiv ausgeführt werden darf, unabhängig davon, ob er **über SERVICE INTERACTIVE PROCESS \_ \_ verfügt.** Wenn **NoInteractiveServices** auf 0 festgelegt ist, dürfen Dienste mit **SERVICE INTERACTIVE \_ \_ PROCESS** interaktiv ausgeführt werden.

**Windows 7, Windows Server 2008 R2, Windows XP und Windows Server 2003:** Der **NoInteractiveServices-Wert** ist standardmäßig auf 0 (0) eingestellt. Dies bedeutet, dass Dienste mit **SERVICE INTERACTIVE \_ \_ PROCESS** interaktiv ausgeführt werden dürfen. Wenn **NoInteractiveServices** auf einen Wert ungleich 0 (null) festgelegt ist, kann kein danach gestarteter Dienst interaktiv ausgeführt werden, unabhängig davon, ob er **über SERVICE INTERACTIVE PROCESS \_ \_ verfügt.**

> [!IMPORTANT]
> Alle Dienste werden in der Terminaldienstesitzung 0 ausgeführt. Wenn ein interaktiver Dienst eine Benutzeroberfläche anzeigt, ist er daher nur für den Benutzer sichtbar, der eine Verbindung mit Sitzung 0 hergestellt hat. Da es keine Möglichkeit gibt, sicherzustellen, dass der interaktive Benutzer mit Sitzung 0 verbunden ist, konfigurieren Sie keinen Dienst so, dass er als interaktiver Dienst unter Terminaldienste oder auf einem System ausgeführt wird, das schnelles Wechseln von Benutzern unterstützt (schneller Benutzerwechsel wird mithilfe von Terminaldiensten implementiert).

 

 

 
