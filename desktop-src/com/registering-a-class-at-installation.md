---
title: Registrieren einer Klasse bei der Installation
description: Wenn eine Klasse wie die meisten Anwendungen jederzeit für Clients verfügbar sein soll, registrieren Sie sie in der Regel über ein Installations- und Setupprogramm.
ms.assetid: 6d78c2ce-56d8-4866-9801-35125ec9cac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017e4393a4c5422157c8f9b9e9b7f366c2fafc8cfe6af5722e451a3d1b9fa069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047858"
---
# <a name="registering-a-class-at-installation"></a>Registrieren einer Klasse bei der Installation

Wenn eine Klasse wie die meisten Anwendungen jederzeit für Clients verfügbar sein soll, registrieren Sie sie in der Regel über ein Installations- und Setupprogramm. Dies bedeutet, informationen über die Anwendung in die Registrierung zu stellen, einschließlich der Art und Stelle, an der die Objekte instanziiert werden sollen. Diese Informationen müssen für alle CLSIDs registriert werden. Andere Informationen sind optional. Tools wie Regsvr32 machen es einfach, ein Setupprogramm zu schreiben, das Server bei der Installation registriert.

Wenn Sie sich nicht auf die Systemeinstellungen verlassen, gibt es zwei wichtige Schlüssel in der Registrierung: die CLSID und die AppID. Zu den wichtigen Informationen unter diesen Schlüsseln gehört, wie das Objekt instanziiert werden soll. Objekte können als in-process, out-of-process local oder out-of-process remote festgelegt werden.

Unter dem AppID-Schlüssel befinden sich mehrere Werte, die spezifische Informationen für diese Anwendung definieren. Dazu gehören [RemoteServerName](remoteservername.md) und [ActivateAtStorage,](activateatstorage.md)die beide verwendet werden können, um einem Client das Erstellen eines Objekts zu ermöglichen, ohne dass der Client über integrierte Kenntnisse des Standorts des Servers verfing. (Weitere Informationen zur Remoteinstanziierung finden Sie unter [Locating a Remote Object](locating-a-remote-object.md) and [Instance Creation Helper Functions](instance-creation-helper-functions.md).)

Ein Server kann auch als Dienst installiert oder unter einem bestimmten Benutzerkonto ausgeführt werden. Weitere Informationen finden Sie unter [Installieren als Dienstanwendung.](installing-as-a-service-application.md)

Ein Server oder ROT-Objekt, das kein Dienst ist oder unter einem bestimmten Benutzerkonto ausgeführt wird, kann als "Activate as activator"-Server bezeichnet werden. Für diese Server müssen der Sicherheitskontext und die Fensterstation/der Desktop des Clients mit dem des Servers übereinstimmen. Ein Client, der versucht, eine Verbindung mit  einem Remoteserver herzustellen, wird als NULL-Fensterstation/Desktop angesehen, sodass in dieser Instanz nur der Serversicherheitskontext verglichen wird. (Weitere Informationen zu SIDs finden Sie unter [Sicherheit in COM](security-in-com.md).) COM speichert die Fensterstation/den Desktop eines Prozesses zwischen, wenn der Prozess zum ersten Mal eine Verbindung mit dem verteilten COM-Dienst herstellt. Daher sollten COM-Clients und -Server ihre Fensterstation oder Threaddesktops des Prozesses nach dem Aufruf von [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) oder [**CoInitializeEx nicht ändern.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)

Wenn eine Klasse als in-process registriert wird, wird ein Aufruf von [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) zum Erstellen des Klassenobjekts automatisch von COM an die [**DllGetClassObject-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) übergeben, die die Klasse implementieren muss, um dem aufrufenden Objekt einen Zeiger auf sein Klassenobjekt zu geben.

In ausführbaren Dateien implementierte Klassen können angeben, dass COM ihren Prozess ausführen und warten soll, bis der Prozess die [**IClassFactory-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) ihres Klassenobjekts über einen Aufruf der [**CoRegisterClassObject-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) registriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Registrierungsschlüssel](com-registry-keys.md)
</dt> <dt>

[Installieren einer As-a-Service-Anwendung](installing-as-a-service-application.md)
</dt> <dt>

[Registrieren eines ausgeführten EXE-Servers](registering-a-running-exe-server.md)
</dt> <dt>

[Registrieren von Komponenten](registering-components.md)
</dt> <dt>

[Registrieren von Objekten in rot](registering-objects-in-the-rot.md)
</dt> <dt>

[Selbstregistrierung](self-registration.md)
</dt> </dl>

 

 