---
description: Die Anwendung ist in zwei Programme unterteilt. Eines der Programme wird als Standardbenutzer ausgeführt, und die andere wird mit Administrator Berechtigungen ausgeführt.
ms.assetid: 1e661915-5797-421d-b96f-72949f441aba
title: Administrator Broker Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299d35c995fb56f969fc5983864cfc93b25b6c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865999"
---
# <a name="administrator-broker-model"></a>Administrator Broker Modell

Im Administrator Broker Modell ist die Anwendung in zwei Programme unterteilt. Eines der Programme wird als Standardbenutzer ausgeführt, und die andere wird mit Administrator Berechtigungen ausgeführt.

Markieren Sie mithilfe eines Anwendungs Manifests das Standardbenutzer Programm mit dem **requestedExecutionLevel-Wert** **asInvoker** , und markieren Sie das administrative Programm mit dem **requestedExecutionLevel-Wert** " **requilesministrator**". Ein Benutzer wird zuerst das Standardbenutzer Programm starten. Wenn der Benutzer versucht, einen Vorgang auszuführen, der ein vollständiges Administrator Zugriffs Token erfordert, ruft das Standardbenutzer Programm die [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) -Funktion auf, um das administrative Programm zu starten. Die **ShellExecute** -Funktion fordert den Benutzer zur Genehmigung auf, bevor die Anwendung mit dem vollständigen Administrator Zugriffs Token des Benutzers ausgeführt wird. Das administrative Programm kann dann Aufgaben ausführen, für die Administratorrechte erforderlich sind.

Das administrative Programm ist nicht vollständig vom Standardbenutzer Programm isoliert. Das administrative Programm kann die prozessübergreifende Kommunikation mit dem Standardbenutzer Programm aktivieren. Diese Kommunikation wird jedoch durch die standardmäßige obligatorische Integritätsrichtlinie eingeschränkt. Informationen zu obligatorischen Integritäts Überlegungen finden [Sie unter Entwerfen von Anwendungen für die Durchführung mit niedriger Integritäts Stufe](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).

Für das Modell des Administrator Brokers können folgende Verwendungsmöglichkeiten verwendet werden:

-   Entwickeln von Assistenten. Wenn ein Hardware-Assistent feststellt, dass ein erforderlicher Treiber nicht auf dem Computer installiert ist oder sich am genehmigten Standort des Unternehmens befindet, wird eine Anwendung mit erhöhten Rechten aufgerufen, die die Möglichkeit zum Verschieben eines Treibers in den Computerspeicher hat.
-   Autorun.exe Aufrufen von Setup.exe. Wenn ein Benutzer die Software von einer CD ausführt, wird Autorun.exe, der als Standardbenutzer ausgeführt wird, Setup.exe, der als Administrator ausgeführt wird, gestartet, um die Software auf dem Computer zu installieren.

Die Verwendung des Administrator Broker Modells hat folgende Nachteile:

-   Die Übergänge von Anwendung zu Anwendung können für den Benutzer verwirrend sein. Es kann schwierig sein, den Benutzer zu informieren, warum eine neue Anwendung auf dem Monitor angezeigt wird.
-   Es kann schwierig sein, Zustandsinformationen zwischen den beiden Anwendungen zu übergeben. Beispielsweise können Sie dieses Modell nicht verwenden, um Zustandsinformationen zwischen einer Standardbenutzer-Systemsteuerung (CPL) und Ihrem Administrator Pendant zu übergeben, um der gleichen cpl die Administrator-und Standardbenutzer Funktionalität zu ermöglichen. Der Standardbenutzer-cpl muss seinen Zustand irgendwo speichern.
-   Beim Aufteilen der Funktionalität zwischen zwei Programmen kann viel replizierter Code vorhanden sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von Anwendungen, für die Administrator Rechte erforderlich sind](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[COM-Objektmodell für Administratoren](administrator-com-object-model.md)
</dt> <dt>

[Betriebs System-Dienstmodell](operating-system-service-model.md)
</dt> <dt>

[Modell mit erhöhten Rechten](elevated-task-model.md)
</dt> </dl>

 

 
