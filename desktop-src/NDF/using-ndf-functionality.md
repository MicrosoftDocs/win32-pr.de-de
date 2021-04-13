---
title: Verwenden der NDF-Funktionalität
description: Microsoft ermöglicht den Zugriff auf die NDF-Funktionalität über eine öffentliche API. Wenn ein Problem auftritt, kann die Anwendung diese API verwenden, um diese Funktionalität innerhalb des Kontexts einer bestimmten Anwendung zu nutzen.
ms.assetid: db06b9a9-a64a-43ff-9b77-95230208cfd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca74a8a80f7babca75182625ec71dc1ec47cbc7
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/10/2020
ms.locfileid: "104390120"
---
# <a name="using-ndf-functionality"></a>Verwenden der NDF-Funktionalität

Microsoft ermöglicht den Zugriff auf die NDF-Funktionalität über eine öffentliche API. Wenn ein Problem auftritt, kann die Anwendung diese API verwenden, um diese Funktionalität innerhalb des Kontexts einer bestimmten Anwendung zu nutzen.

Es gibt drei Phasen der Diagnose mit NDF: Erstellen eines Vorfalls, Ausführen von Diagnosen und Reparaturen und Schließen des Vorfalls. Diese Übersicht gibt an, welche NDF-Funktionen für ein bestimmtes Szenario relevant sein können. Ausführliche Informationen zu den einzelnen Funktionen finden Sie im Abschnitt [NDF-Referenz](ndf-reference.md) .

## <a name="creating-an-incident"></a>Erstellen eines Vorfalls

Eine NDF-Diagnose Sitzung erfordert einen bestimmten Incident für die Diagnose. Es gibt mehrere Funktionen, die verwendet werden können, um einen Vorfall zu erstellen. Wählen Sie die Funktion aus, die der Anwendung am ehesten entspricht, als der Fehler aufgetreten ist.

-   [**Ndfkreateconnectivityincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateconnectivityincident): allgemeine Probleme mit der Internet Verbindung, die keine zusätzlichen Informationen benötigen.
-   [**Ndfkreatewebincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) / [**Ndfkreatewebincidentex**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincidentex): Herstellen einer Verbindung mit einer HTTP-oder HTTPS-URL.
-   [**Ndfkreatesharingincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatesharingincident): Zugriff auf einen UNC-Pfad oder eine Dateifreigabe.
-   [**Ndfkreatednsincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident): Auflösen eines DNS-Host namens.
-   [**Ndfkreatepnrpincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatepnrpincident): Auflösen eines PNRP-Peer namens.
-   [**Ndfkreategroupingincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreategroupingincident): Beitritt zu einer Peer-zu-Peer-Gruppe.
-   [**Ndfkreatewinsockincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident): Herstellen einer Verbindung mit einem Ziel mithilfe eines Sockets (wenn keine der anderen Funktionen spezifisch ist).
-   [**Ndfkreatabcident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateincident): wird verwendet, wenn kein anderes Szenario geeignet ist und die spezifische NDF-Hilfsklasse, die aufgerufen werden soll, bekannt ist (zusammen mit den Argumenten, die Sie benötigt). Wird hauptsächlich zu Testzwecken von Anwendungsentwicklern verwendet, die ihre eigene Hilfsklasse geschrieben haben.

## <a name="running-diagnosis-and-repairs"></a>Ausführen von Diagnosen und Reparaturen

Es gibt zwei Möglichkeiten, die Diagnose-und Reparaturfunktionen zu starten.

-   Verwenden der Windows-Benutzeroberfläche (empfohlen)

    Wenn Sie auf der Windows-Standardbenutzer Oberfläche ausführen, können Sie einfach die [**ndfexecutediagnose**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) -Funktion aufrufen. Der NDF-Assistent wird gestartet und unterstützt den Benutzer beim identifizieren (und nach Möglichkeit und beheben) des Problems. Die Funktion gibt zurück, nachdem dieser Prozess abgeschlossen wurde. Die Benutzeroberfläche ist optional für Ihre Anwendung modal.

-   Verwenden einer benutzerdefinierten Benutzeroberfläche (nur Windows 7 und höher)

    Verschiedene Funktionen stehen zur Verwendung in Szenarios zur Verfügung, in denen keine Benutzeroberfläche angezeigt wird oder wenn die standardmäßige Windows-Benutzeroberfläche nicht verwendet wird (z. b. Media Center, Embedded Applications und die Eingabeaufforderung). Mit dieser Option wird die Funktionalität der Benutzer Funktionalität umgangen, die im NDF-Assistenten bereitgestellt wird. dazu gehören das Einschränken der Ergebnisse auf vollständig unterstützte Hauptursachen sowie die Heuristik, um dem Benutzer die Reparaturen in der empfohlenen Reihenfolge zu präsentieren. Wenn Sie diese Funktionen verwenden, müssen Sie selbst diese Funktionen bereitstellen. Außerdem müssen Sie sicherstellen, dass der von den Diagnoseergebnissen verwendete Arbeitsspeicher freigegeben wird.

    Um die Diagnose zu starten, wenden Sie die [**ndfdiagnoseincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) -Funktion an. Alle gefundenen Probleme werden an die Anwendung als eine Auflistung von [**rootkauseinfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) -Strukturen zurückgegeben, in denen identifizierte Ursachen und mögliche Reparaturen beschrieben werden.

    Nachdem Sie eine Reparatur ausgewählt (oder den Benutzer zur Auswahl einer Reparatur aufgefordert haben), sollte [**ndfreanincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) aufgerufen werden, um die Reparatur zu versuchen und zu ermitteln, ob das Problem behoben wurde.

    In einigen Fällen kann eine Reparatur erfolgreich ausgeführt werden, aber das Problem nicht beheben. In solchen Fällen wird empfohlen, den vorhandenen Incident zu schließen und dann einen neuen zu öffnen. Dadurch wird sichergestellt, dass alle neuen Probleme, die durch die anfängliche Reparatur nicht maskiert werden, identifiziert werden. Nehmen Sie z. b. an, dass keine Drahtlos Netzwerke sichtbar sind. Nach dem Zurücksetzen des Adapters werden drahtlose Netzwerke angezeigt, aber keine von Ihnen finden Sie in der bevorzugten Liste. Dabei handelt es sich um ein neues Problem, das eine neue Diagnose zur Identifizierung erfordern würde. Wenn bei einem solchen zweiten Diagnose Versuch keine zusätzlichen Probleme identifiziert werden, kann versucht werden, das ursprüngliche Problem zu beheben, oder der Benutzer kann darüber informiert werden, dass das Problem nicht gelöst werden konnte.

    [**Ndfdiagnoseincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) und [**ndfrepaar Incident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) sind synchrone APIs. Wenn Sie die von diesen Funktionen initiierte Aktivität abbrechen möchten, rufen Sie [**ndfcancelincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcancelincident) von einem anderen Thread auf. Die Funktion wird beim nächsten verfügbaren Endpunkt im Diagnose-oder Reparaturprozess zurückgegeben.

    An jedem Punkt können Sie optional [**ndfgettracefile**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfgettracefile) aufrufen, um eine Kopie des NDF-Protokolls für die aktuelle Diagnose Sitzung abzurufen und in die Anwendungsprotokolle einzubeziehen. Das Protokoll wird nach dem Abrufen geleert, und nachfolgende Aufrufe rufen nur Ereignisse ab, die nach dem letzten Aufruf dieser Funktion aufgetreten sind.

## <a name="closing-an-incident"></a>Schließen eines Vorfalls

Wenn die Diagnose eines Vorfalls abgeschlossen ist, können Sie [**ndfcloseincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident) abrufen, um Systemressourcen freizugeben, die mit dem Ausführen der Diagnose bei diesem Vorfall verknüpft sind. (Beachten Sie, dass dies keine von [**ndfdiagnoseincident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident)erstellten Objekte freigibt.
