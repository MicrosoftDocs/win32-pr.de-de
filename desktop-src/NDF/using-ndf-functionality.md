---
title: Verwenden der NDF-Funktionalität
description: Microsoft ermöglicht den Zugriff auf NDF-Funktionen über eine öffentliche API. Wenn ein Problem auftritt, kann die Anwendung diese API verwenden, um diese Funktionalität im Kontext einer bestimmten Anwendung zu nutzen.
ms.assetid: db06b9a9-a64a-43ff-9b77-95230208cfd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d85d1386971207330579f5395989e14c4b2315dc578f5bb3509695b99d6e215a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133227"
---
# <a name="using-ndf-functionality"></a>Verwenden der NDF-Funktionalität

Microsoft ermöglicht den Zugriff auf NDF-Funktionen über eine öffentliche API. Wenn ein Problem auftritt, kann die Anwendung diese API verwenden, um diese Funktionalität im Kontext einer bestimmten Anwendung zu nutzen.

Es gibt drei Phasen der Diagnose mit NDF: Erstellen eines Incidents, Ausführen von Diagnosen und Reparaturen und Schließen des Incidents. Diese Übersicht gibt an, welche NDF-Funktionen für ein bestimmtes Szenario relevant sein können. Ausführliche Informationen zu den einzelnen Funktionen finden Sie im [Abschnitt NDF-Referenz.](ndf-reference.md)

## <a name="creating-an-incident"></a>Erstellen eines Incidents

Für eine NDF-Diagnosesitzung ist für die Diagnose ein bestimmter Vorfall erforderlich. Es gibt mehrere Funktionen, die zum Erstellen eines Incidents verwendet werden können. Wählen Sie die Funktion aus, die am besten mit dem entspricht, was die Anwendung versucht hat, als der Fehler aufgetreten ist.

-   [**NdfCreateConnectivityIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateconnectivityincident)Allgemeine Probleme mit der Internetverbindung, die keine zusätzlichen Informationen benötigen.
-   [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) / [**NdfCreateWebIncidentEx:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincidentex)Herstellen einer Verbindung mit einer HTTP- oder HTTPS-URL.
-   [**NdfCreateSharingIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatesharingincident)Zugriff auf einen UNC-Pfad oder eine Dateifreigabe.
-   [**NdfCreateDNSIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident)Auflösen eines DNS-Hostnamens.
-   [**NdfCreatePnrpIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatepnrpincident)Auflösen eines PNRP-Peernamens.
-   [**NdfCreateGroupingIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreategroupingincident)Beitritt zu einer Peer-zu-Peer-Gruppe.
-   [**NdfCreateWinSockIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident)Herstellen einer Verbindung mit einem Ziel mithilfe eines Sockets (wenn keine der anderen Funktionen speziell angewendet wird).
-   [**NdfCreateIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateincident)Wird verwendet, wenn kein anderes Szenario geeignet ist und die spezifische NDF-Hilfsklasse, die aufgerufen werden soll, bekannt ist (zusammen mit den dafür benötigten Argumenten). Wird hauptsächlich zu Testzwecken von Anwendungsentwicklern verwendet, die ihre eigene Hilfsklasse geschrieben haben.

## <a name="running-diagnosis-and-repairs"></a>Ausführen von Diagnosen und Reparaturen

Es gibt zwei Möglichkeiten, die Diagnose- und Reparaturfunktionen zu starten.

-   Verwenden des Windows Benutzeroberfläche (empfohlen)

    Wenn Sie in der Standard-Windows-Benutzeroberfläche ausführen, können Sie einfach die [**NdfExecuteDia pivot-Funktion**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) aufrufen. Der NDF-Assistent wird gestartet und hilft dem Benutzer, das Problem zu identifizieren (und wenn möglich) zu beheben. Die Funktion gibt zurück, nachdem dieser Prozess abgeschlossen wurde. Die Benutzeroberfläche ist optional modal für Ihre Anwendung.

-   Verwenden eines benutzerdefinierten Benutzeroberfläche (nur Windows 7 und höher)

    Es stehen verschiedene Funktionen zur Verfügung, die in Szenarien verwendet werden können, in denen keine Benutzeroberfläche angezeigt wird oder in denen die standardmäßige Windows-Benutzeroberfläche nicht verwendet wird (z. B. Media Center, eingebettete Anwendungen und die Eingabeaufforderung). Diese Option umgeht die Im NDF-Assistenten bereitgestellte Benutzeroberflächenfunktion, die das Beschränken der Ergebnisse auf vollständig unterstützte Grundursachen sowie heuristische Funktionen umfasst, um dem Benutzer Reparaturen in der empfohlenen Reihenfolge zu präsentieren. Wenn Sie diese Funktionen verwenden, müssen Sie diese Funktionen selbst bereitstellen. Sie müssen auch sicherstellen, dass der von den Diagnoseergebnissen verwendete Arbeitsspeicher frei wird.

    Um mit der Diagnose zu beginnen, rufen Sie die [**NdfDiagnoseIncident-Funktion**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) auf. Alle gefundenen Probleme werden als Sammlung von [**RootCauseInfo-Strukturen,**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) die identifizierte Ursachen und mögliche Reparaturen beschreiben, an die Anwendung zurückgegeben.

    Nachdem Sie eine Reparatur ausgewählt (oder den Benutzer aufgefordert haben, eine Reparatur auszuwählen), sollte [**NdfRepairIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) aufgerufen werden, um die Reparatur zu versuchen und zu ermitteln, ob das Problem behoben wurde.

    In einigen Fällen kann eine Reparatur erfolgreich durchgeführt werden, aber das Problem wird nicht behoben. In solchen Fällen wird empfohlen, den vorhandenen Incident zu schließen und dann einen neuen zu öffnen. Dadurch wird sichergestellt, dass alle neuen Probleme identifiziert werden, die bei der ersten Reparatur nicht maskiert wurden. Angenommen, es waren keine Drahtlosnetzwerke sichtbar. Nach dem Zurücksetzen des Adapters werden Funknetzwerke angezeigt, aber keines davon ist in der bevorzugten Liste enthalten. Dies ist ein neues Problem, für das eine neue Diagnose erforderlich wäre. Wenn bei einem solchen zweiten Diagnoseversuch keine zusätzlichen Probleme identifiziert werden, kann eine andere Reparatur versucht werden, um das ursprüngliche Problem zu beheben, oder der Benutzer kann darüber informiert werden, dass das Problem nicht behoben werden konnte.

    [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) und [**NdfRepairIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) sind synchrone APIs. Wenn Sie die von diesen Funktionen initiierte Aktivität abbrechen möchten, rufen Sie [**NdfCancelIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcancelincident) aus einem anderen Thread auf. Die Funktion gibt am nächsten verfügbaren Haltepunkt im Diagnose- oder Reparaturprozess zurück.

    Sie können optional jederzeit [**NdfGetTraceFile**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfgettracefile) aufrufen, um eine Kopie des NDF-Protokolls für die aktuelle Diagnosesitzung abzurufen und in Ihre Anwendungsprotokollen eineintragen. Das Protokoll wird nach dem Abrufen geleert, und nachfolgende Aufrufe rufen nur Ereignisse ab, die nach dem letzten Aufruf dieser Funktion aufgetreten sind.

## <a name="closing-an-incident"></a>Schließen eines Incidents

Wenn Sie die Diagnose eines Incidents abgeschlossen haben, rufen Sie [**NdfCloseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident) auf, um Systemressourcen frei zu geben, die mit der Diagnose dieses Incidents verknüpft sind. (Beachten Sie, dass dadurch keine objekte frei werden, die von [**NdfDiagnoseIncident erstellt wurden.**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident)
