---
description: Eine Anwendung, die als Standardbenutzer ausgeführt wird, kommuniziert mit einem Dienst, der als SYSTEM ausgeführt wird, mithilfe des Remoteprozeduraufrufs (Remote Procedure Call, RPC).
ms.assetid: c0bcebe3-f7eb-471f-a21d-5840d2e26729
title: Betriebssystemdienstmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af797a7baad8390b1b4bc79fd7723a518c587ed58cc2dab27ab2898845335ca3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907800"
---
# <a name="operating-system-service-model"></a>Betriebssystemdienstmodell

Im Betriebssystemdienstmodell kommuniziert eine Anwendung, die als Standardbenutzer ausgeführt wird, mit einem Dienst, der als **SYSTEM** ausgeführt wird, mithilfe des [Remoteprozeduraufrufs](/windows/desktop/Rpc/rpc-start-page) (Remote Procedure Call, RPC).

Die Standardbenutzeranwendung ist im Anwendungsmanifest mit **dem requestedExecutionLevel** von **asInvoker gekennzeichnet.** Um einen Vorgang durchzuführen, der Administratorrechte erfordert, stellt die Standardbenutzeranwendung eine Anforderung an den Dienst.

Eine Verwendung für das Betriebssystemdienstmodell besteht in der Verwaltung von Anwendungen, die sich auf das System auswirken können, z. B. Antivirensoftware oder andere unerwünschte Software und Spyware. Mit der Standardbenutzeranwendung kann der angemeldete Benutzer einige Aspekte des Diensts steuern. Der Dienst ist dafür verantwortlich, zu bestimmen, welche Vorgänge er für eine Standardbenutzeranwendung ausführt. Beispielsweise kann ein Antivirendienst es einem Standardbenutzer ermöglichen, eine Überprüfung des Systems zu starten, aber er lässt möglicherweise nicht zu, dass ein Standardbenutzer die Virenüberprüfung in Echtzeit deaktiviert.

Ein hauptvorteil der Verwendung des Betriebssystemdienstmodells ist, dass keine Eingabeaufforderung für rechte Rechte erforderlich ist.

Ein Nachteil der Verwendung des Betriebssystemdienstmodells ist, dass ein auf dem System ausgeführter Dienst mehr Ressourcen als eine Aufgabe verwendet und ein Dienst nicht von einem Standardbenutzer beendet werden kann. Erwägen Sie die [Verwendung des Aufgabenmodells mit erhöhten Rechten,](elevated-task-model.md) wenn es ausreicht.

Um das Betriebssystemdienstmodell zu implementieren, erstellen Sie eine Standardbenutzerclientanwendung und einen Betriebssystemdienst. Installieren Sie den Dienst während der Produktinstallation im Betriebssystem.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von Anwendungen, die Administratorrechte erfordern](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Administratorbrokermodell](administrator-broker-model.md)
</dt> <dt>

[COM-Objektmodell des Administrators](administrator-com-object-model.md)
</dt> <dt>

[Aufgabenmodell mit erhöhten Rechten](elevated-task-model.md)
</dt> </dl>

 

 
