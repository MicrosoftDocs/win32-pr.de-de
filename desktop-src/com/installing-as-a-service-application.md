---
title: Installieren von als Dienst Anwendung
description: Installieren von als Dienst Anwendung
ms.assetid: 0dd4b348-3d12-49ba-8098-4adb9df01a0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed5c474d73c74b3be40bae773c3d51eadf6c69a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039654"
---
# <a name="installing-as-a-service-application"></a>Installieren von als Dienst Anwendung

Zusätzlich zur Ausführung als ausführbare Datei des lokalen Servers (exe) kann sich ein COM-Objekt auch als Dienst Anwendung Verpacken, wenn es von einem lokalen oder Remote Client aktiviert wird. -Dienste unterstützen zahlreiche nützliche und Benutzer seitige integrierte Verwaltungsfunktionen, einschließlich lokaler und Remote Starts, beenden, anhalten und Neustarts sowie der Möglichkeit, den Server für die Ausführung unter einem bestimmten [Benutzerkonto](/windows/desktop/Services/service-user-accounts) und einer [Fenster Station](/windows/desktop/winstation/window-stations)einzurichten.

Ein Objekt, das als Dienst geschrieben wird, wird für die Verwendung durch com installiert, indem ein [LocalService](localservice.md) -Wert unter seinem [AppID](appid-key.md) -Schlüssel eingerichtet und eine Standard Dienst Installation durchgeführt wird.

Klassen können auch so konfiguriert werden, dass Sie unter einem bestimmten Benutzerkonto ausgeführt werden, wenn Sie von einem Remote Client aktiviert werden, ohne als Dienst Anwendung geschrieben zu werden. Zu diesem Zweck installiert die-Klasse einen Benutzernamen und ein Kennwort, das verwendet werden soll, wenn der SCM den lokalen Server Prozess gestartet.

Wenn eine Klasse auf diese Weise konfiguriert wird, können Aufrufe von [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) mit dieser CLSID nicht ausgeführt werden, es sei denn, der Prozess wurde von com im Auftrag einer tatsächlichen Aktivierungs Anforderung gestartet. Anders ausgedrückt: Klassen, die für die Verwendung als bestimmter Benutzer konfiguriert sind, werden möglicherweise nicht unter einer anderen Identität registriert.

Der Benutzername wird vom " [runas](runas.md) "-Wert mit dem Namen "-" unter dem Schlüssel "AppID" der Klasse entnommen. Wenn der Benutzername "Interactive User" lautet, wird der Klassen Code im Sicherheitskontext des aktuell angemeldeten Benutzers ausgeführt und mit der interaktiven Fenster Station verbunden.

Andernfalls wird das Kennwort aus einem ausgeblendeten Teil der Registrierung abgerufen, der nur für Administratoren des Computers und des Systems verfügbar ist. Der Benutzername und das Kennwort werden dann verwendet, um eine Anmelde Sitzung zu erstellen, in der der Klassen Code ausgeführt wird. Wenn der Klassen Code auf diese Weise gestartet wird, wird er mit einem eigenen Desktop und einer eigenen Fenster Station ausgeführt, und es werden keine Fenster Handles, die Zwischenablage oder andere Elemente der Benutzeroberfläche mit dem interaktiven Benutzer oder anderen Klassen, die in anderen Benutzerkonten ausgeführt werden, gemeinsam verwendet.

Ein Server, der entweder mit " **LocalService** " oder " **runas** " registriert ist, kann ein Objekt in der laufenden Objekttabelle registrieren, damit jeder Client eine Verbindung mit ihm herstellen kann. Zu diesem Zweck muss der Server-Aufrufe von " [**iriunningobjectamp;: Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) " das rotflags- \_ Flag "zugsclient" festlegen. Eine Servereinstellung dieses Bit muss den Namen der ausführbaren Datei im AppID-Abschnitt der Registrierung aufweisen, die auf die AppID für die ausführbare Datei verweist. Ein "als Activator-Server aktivieren" (nicht als " **LocalService** " oder " **runas**" registriert) registriert möglicherweise ein Objekt mit diesem Flag nicht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren einer Klasse bei der Installation](registering-a-class-at-installation.md)
</dt> <dt>

[Registrieren eines ausführenden exe-Servers](registering-a-running-exe-server.md)
</dt> <dt>

[Registrieren von Objekten in der rot](registering-objects-in-the-rot.md)
</dt> <dt>

[Selbstregistrierung](self-registration.md)
</dt> </dl>

 

 