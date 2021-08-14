---
description: Die Anwendung ist in zwei Programme unterteilt. Eines der Programme wird als Standardbenutzer ausgeführt, das andere mit Administratorrechten.
ms.assetid: 1e661915-5797-421d-b96f-72949f441aba
title: Administrator Broker-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c67a68c823221226f56d01b750ab74a70ca30530f44cd174e333c3e4d7cbaa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784941"
---
# <a name="administrator-broker-model"></a>Administrator Broker-Modell

Im Administratorbrokermodell ist die Anwendung in zwei Programme unterteilt. Eines der Programme wird als Standardbenutzer ausgeführt, das andere mit Administratorrechten.

Markieren Sie mithilfe eines Anwendungsmanifests das Standardbenutzerprogramm mit **requestedExecutionLevel** von **asInvoker,** und markieren Sie das Verwaltungsprogramm mit **requestedExecutionLevel** von **requireAdministrator**. Ein Benutzer startet zuerst das Standardbenutzerprogramm. Wenn der Benutzer versucht, einen Vorgang auszuführen, der ein vollständiges Administratorzugriffstoken erfordert, ruft das Standardbenutzerprogramm die [**ShellExecute-Funktion**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) auf, um das Verwaltungsprogramm zu starten. Die **ShellExecute-Funktion** fordert den Benutzer zur Genehmigung auf, bevor die Anwendung mit dem vollständigen Administratorzugriffstoken des Benutzers ausgeführt wird. Das Administratorprogramm kann dann Aufgaben ausführen, die Administratorberechtigungen erfordern.

Das Verwaltungsprogramm ist nicht vollständig vom Standardbenutzerprogramm isoliert. Das Verwaltungsprogramm kann die prozessübergreifende Kommunikation mit dem Standardbenutzerprogramm aktivieren. Diese Kommunikation ist jedoch durch die standardmäßige obligatorische Integritätsrichtlinie beschränkt. Informationen zu obligatorischen Integritätsüberlegungen finden Sie unter [Entwerfen von Anwendungen für die Ausführung auf niedriger Integritätsebene.](/previous-versions/dotnet/articles/bb625960(v=msdn.10))

Im Folgenden werden mögliche Verwendungsmöglichkeiten für das Administratorbrokermodell verwendet:

-   Entwickeln von Assistenten. Wenn ein Hardware-Assistent feststellt, dass ein erforderlicher Treiber nicht auf dem Computer installiert ist oder sich am genehmigten Standort des Unternehmens befindet, wird eine Anwendung mit erhöhten Rechten aufgerufen, die die Möglichkeit bietet, einen Treiber in den Computerspeicher zu verschieben.
-   Autorun.exe aufrufende Setup.exe. Wenn ein Benutzer Software von einer CD aus ausführt, startet Autorun.exe, der als Standardbenutzer ausgeführt wird, Setup.exe, der als Administrator ausgeführt wird, um die Software auf dem Computer zu installieren.

Die verwendung des Administratorbrokermodells hat folgende Nachteile:

-   Die Übergänge von Anwendung zu Anwendung können für den Benutzer verwirrend sein. Es kann schwierig sein, den Benutzer darüber zu informieren, warum eine neue Anwendung auf dem Monitor angezeigt wird.
-   Es kann schwierig sein, Zustandsinformationen zwischen den beiden Anwendungen zu übergeben. Beispielsweise würden Sie dieses Modell nicht verwenden, um Zustandsinformationen zwischen einer Standard-Benutzersteuerung (User Control Panel, CPL) und ihrer Administratorentsprechung zu übergeben, um derselben CPL einfach administrative und Standardbenutzerfunktionen zu ermöglichen. Die CPL des Standardbenutzers müsste seinen Zustand an einem ortsüblichen Ort speichern.
-   Beim Aufteilen der Funktionalität auf zwei Programme kann viel replizierter Code vorhanden sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von Anwendungen, die Administratorrechte erfordern](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[COM-Objektmodell des Administrators](administrator-com-object-model.md)
</dt> <dt>

[Betriebssystemdienstmodell](operating-system-service-model.md)
</dt> <dt>

[Aufgabenmodell mit erhöhten Rechten](elevated-task-model.md)
</dt> </dl>

 

 
