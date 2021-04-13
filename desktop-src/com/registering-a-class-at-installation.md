---
title: Registrieren einer Klasse bei der Installation
description: Wenn eine Klasse für Clients jederzeit verfügbar sein soll, wie es bei den meisten Anwendungen der Fall ist, registrieren Sie Sie in der Regel über ein Installations-und Setup Programm.
ms.assetid: 6d78c2ce-56d8-4866-9801-35125ec9cac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4253c40cb3feb7e737368c947c0b20715f5becbd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316551"
---
# <a name="registering-a-class-at-installation"></a>Registrieren einer Klasse bei der Installation

Wenn eine Klasse für Clients jederzeit verfügbar sein soll, wie es bei den meisten Anwendungen der Fall ist, registrieren Sie Sie in der Regel über ein Installations-und Setup Programm. Dies bedeutet, dass Sie Informationen über die Anwendung in die Registrierung einfügen, einschließlich der Art und Weise, in der die Objekte instanziiert werden. Diese Informationen müssen für alle CLSIDs registriert werden. Weitere Informationen sind optional. Tools wie regsvr32 vereinfachen das Schreiben eines Setup Programms, mit dem Server bei der Installation registriert werden.

Wenn Sie nicht auf die System Standardwerte Vertrauen, gibt es zwei wichtige Schlüssel in der Registrierung: die CLSID und die AppID. Zu den wichtigen Informationen unter diesen Schlüsseln gehört, wie das Objekt instanziiert werden soll. Objekte können als Prozess interne, out-of-Process-oder out-of-Process-Remote festgelegt werden.

Unter dem Schlüssel "AppID" sind mehrere Werte, die für diese Anwendung spezifische Informationen definieren. Dabei handelt es sich um [Remoteservername](remoteservername.md) und [activateatstorage](activateatstorage.md). beide können verwendet werden, um einem Client das Erstellen eines Objekts zu gestatten, wobei der Client nicht über das integrierte Wissen zum Speicherort des Servers verfügt. (Weitere Informationen zur Remote Instanziierung finden Sie untersuchen [eines Remote Objekts](locating-a-remote-object.md) und [Hilfsfunktionen zum Erstellen von Instanzen](instance-creation-helper-functions.md).)

Ein Server kann auch als Dienst installiert werden oder unter einem bestimmten Benutzerkonto ausgeführt werden. Weitere Informationen finden Sie unter [Installieren von as-a-Service-Anwendungen](installing-as-a-service-application.md).

Ein Server-oder ein rot-Objekt, das kein-Dienst ist oder unter einem bestimmten Benutzerkonto ausgeführt wird, kann als Server "aktivieren als Aktivator" bezeichnet werden. Für diese Server müssen der Sicherheitskontext und die Fenster Station/der Desktop des Clients mit dem des Servers identisch sein. Ein Client, der versucht, eine Verbindung mit einem Remote Server herzustellen, wird als **null** -Fenster Station/Desktop betrachtet, sodass nur der Server Sicherheitskontext in dieser Instanz verglichen wird. (Weitere Informationen zu SIDs finden Sie unter [Sicherheit in com](security-in-com.md).) COM speichert die Fenster Station/den Desktop eines Prozesses zwischen, wenn der Prozess zum ersten Mal eine Verbindung mit dem verteilten com-Dienst herstellt. Daher sollten com-Clients und-Server die Fenster Station oder die Thread Desktops des Prozesses nicht ändern, nachdem [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) oder [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)aufgerufen wurde.

Wenn eine Klasse als Prozess interne Registrierung registriert wird, wird ein Aufruf von [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) zum Erstellen des Klassen Objekts automatisch von com an die [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) -Funktion übergeben, die von der Klasse implementiert werden muss, um dem aufrufenden Objekt einen Zeiger auf das zugehörige Klassenobjekt zu verleihen.

Klassen, die in ausführbaren Dateien implementiert werden, können angeben, dass com Ihren Prozess ausführen soll, und warten, bis der Prozess die [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) -Schnittstelle Ihres Klassen Objekts über einen Aufrufen der [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) -Funktion registriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Registrierungsschlüssel](com-registry-keys.md)
</dt> <dt>

[Installieren von als Dienst Anwendung](installing-as-a-service-application.md)
</dt> <dt>

[Registrieren eines ausführenden exe-Servers](registering-a-running-exe-server.md)
</dt> <dt>

[Registrieren von Komponenten](registering-components.md)
</dt> <dt>

[Registrieren von Objekten in der rot](registering-objects-in-the-rot.md)
</dt> <dt>

[Selbstregistrierung](self-registration.md)
</dt> </dl>

 

 