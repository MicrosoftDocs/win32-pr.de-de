---
description: Eine Anwendung, die als Standardbenutzer ausgeführt wird, kommuniziert mithilfe eines Remote Prozedur Aufrufs (RPC) mit einem Dienst, der als System ausgeführt wird.
ms.assetid: c0bcebe3-f7eb-471f-a21d-5840d2e26729
title: Betriebs System-Dienstmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce545c60da8e480247c8fc8b02cfc01e4487340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960139"
---
# <a name="operating-system-service-model"></a>Betriebs System-Dienstmodell

Im Betriebssystem-Dienstmodell kommuniziert eine Anwendung, die als Standardbenutzer ausgeführt wird, mit einem Dienst, der als **System** ausgeführt wird, mithilfe des [Remote Prozedur Aufrufs](/windows/desktop/Rpc/rpc-start-page) (RPC).

Die Standardbenutzer Anwendung wird im Anwendungs Manifest mit dem **requestedExecutionLevel-Wert** " **asInvoker**" gekennzeichnet. Um einen Vorgang auszuführen, für den Administratorrechte erforderlich sind, stellt die Standardbenutzer Anwendung eine Anforderung an den Dienst.

Eine Verwendung für das Dienstmodell des Betriebssystems besteht darin, Anwendungen zu verwalten, die sich auf das System auswirken können, z. b. Antivirensoftware oder andere unerwünschte Software und Spyware. Mit der Standardbenutzer Anwendung kann der angemeldete Benutzer einige Aspekte des dienstanwendungs-Dienstanbieter steuern. Der Dienst ist verantwortlich für die Bestimmung der Vorgänge, die er für eine Standardbenutzer Anwendung ausführt. Beispielsweise kann ein Antivirendienst einem Standardbenutzer ermöglichen, eine Überprüfung des Systems zu starten, aber es ist nicht möglich, dass ein Standardbenutzer die Echt Zeit Viren Überprüfung deaktiviert.

Ein wesentlicher Vorteil der Verwendung des Betriebssystem-Dienst Modells ist, dass keine Eingabeaufforderung zur Rechte Erweiterung erforderlich ist.

Ein Nachteil bei der Verwendung des Betriebssystem-Dienst Modells besteht darin, dass ein auf dem System ausgeführt Dienst mehr Ressourcen als eine Aufgabe verwendet und ein Dienst nicht von einem Standardbenutzer angehalten werden kann. Verwenden Sie ggf. das [Modell mit erhöhten](elevated-task-model.md) rechten.

Um das Betriebssystem-Dienstmodell zu implementieren, erstellen Sie eine Standardbenutzer-Client Anwendung und einen Betriebssystem Dienst. Installieren Sie den Dienst während der Installation des Produkts im Betriebssystem.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von Anwendungen, für die Administrator Rechte erforderlich sind](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Administrator Broker Modell](administrator-broker-model.md)
</dt> <dt>

[COM-Objektmodell für Administratoren](administrator-com-object-model.md)
</dt> <dt>

[Modell mit erhöhten Rechten](elevated-task-model.md)
</dt> </dl>

 

 
