---
description: Die Anwendung ist in zwei Programme unterteilt. Eines der Programme wird als Standardbenutzer ausgeführt, das andere mit Administratorrechten.
ms.assetid: 1e661915-5797-421d-b96f-72949f441aba
title: Administratorbrokermodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c67a68c823221226f56d01b750ab74a70ca30530f44cd174e333c3e4d7cbaa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784941"
---
# <a name="administrator-broker-model"></a>Administratorbrokermodell

Im Administratorbrokermodell ist die Anwendung in zwei Programme unterteilt. Eines der Programme wird als Standardbenutzer ausgeführt, das andere mit Administratorrechten.

Markieren Sie mithilfe eines Anwendungsmanifests das Standardbenutzerprogramm mit **dem requestedExecutionLevel** von **asInvoker,** und markieren Sie das Verwaltungsprogramm mit **dem requestedExecutionLevel** **von requireAdministrator**. Ein Benutzer startet zuerst das Standardbenutzerprogramm. Wenn der Benutzer versucht, einen Vorgang durchzuführen, der ein vollständiges Administratorzugriffstoken erfordert, ruft das Standardbenutzerprogramm die [**ShellExecute-Funktion**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) auf, um das Administrative Programm zu starten. Die **ShellExecute-Funktion** fordert den Benutzer zur Genehmigung auf, bevor die Anwendung mit dem Volladministrator-Zugriffstoken des Benutzers ausgeführt wird. Das Verwaltungsprogramm kann dann Aufgaben ausführen, die Administratorrechte erfordern.

Das Verwaltungsprogramm ist nicht vollständig vom Standardbenutzerprogramm isoliert. Das Verwaltungsprogramm kann die prozessübergreifende Kommunikation mit dem Standardbenutzerprogramm aktivieren. Diese Kommunikation wird jedoch durch die obligatorische Standardintegritätsrichtlinie eingeschränkt. Informationen zu obligatorischen Integritätsüberlegungen finden Sie unter [Entwerfen von Anwendungen, die auf niedriger Integritätsebene ausgeführt werden.](/previous-versions/dotnet/articles/bb625960(v=msdn.10))

Folgende Verwendungsmöglichkeiten sind für das Administratorbrokermodell möglich:

-   Entwickeln von Assistenten. Wenn ein Hardware-Assistent feststellt, dass ein erforderlicher Treiber nicht auf dem Computer installiert ist oder sich am genehmigten Speicherort des Unternehmens befindet, ruft er eine Anwendung mit erhöhten Rechten auf, die einen Treiber in den Computerspeicher verschieben kann.
-   Autorun.exe aufruft Setup.exe. Wenn ein Benutzer Software von einer CD aus ausgeführt, startet Autorun.exe, das als Standardbenutzer ausgeführt wird, Setup.exe, das als Administrator ausgeführt wird, um die Software auf dem Computer zu installieren.

Die Verwendung des Administratorbrokermodells hat folgende Nachteile:

-   Die Übergänge von der Anwendung zur Anwendung können für den Benutzer verwirrend sein. Es kann schwierig sein, den Benutzer darüber zu informieren, warum eine neue Anwendung auf dem Monitor angezeigt wird.
-   Es kann schwierig sein, Zustandsinformationen zwischen den beiden Anwendungen zu übergeben. Beispielsweise würden Sie dieses Modell nicht verwenden, um Zustandsinformationen zwischen einer Standardbenutzersteuerung (Standard User Control Panel, CPL) und deren Administratorentität zu übergeben, um der gleichen CPL lediglich verwaltungs- und standardbenutzerfunktionen zu ermöglichen. Die Standardbenutzer-CPL müsste ihren Zustand an einem anderen Ort speichern.
-   Es kann viel replizierten Code geben, wenn die Funktionalität auf zwei Programme aufgeteilt wird.

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

 

 
