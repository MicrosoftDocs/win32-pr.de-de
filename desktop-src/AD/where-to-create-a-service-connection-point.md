---
title: Erstellen eines Dienst Verbindungs Punkts
description: Wenn eine Instanz von Active Directory Domain Services installiert ist, erstellt das Dienst Installationsprogramm Dienst Verbindungspunkt-Objekte (SCP) in Active Directory Domain Services.
ms.assetid: a90566d9-dd68-43e2-be9e-300d57a7fbf4
ms.tgt_platform: multiple
keywords:
- Erstellen eines Dienst Verbindungs Punkts (AD)
- Active Directory, in dem ein Dienst Verbindungspunkt erstellt werden soll
- Erstellen eines Dienst Verbindungs Punkts (AD)
- Erstellen eines Dienst Verbindungspunkt-AD
- Dienst Verbindungspunkt-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf122ebabcfd8085ebad46314ffd1c09f827e783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036333"
---
# <a name="where-to-create-a-service-connection-point"></a>Erstellen eines Dienst Verbindungs Punkts

Wenn eine Instanz von Active Directory Domain Services installiert ist, erstellt das Dienst Installationsprogramm Dienst Verbindungspunkt-Objekte (SCP) in Active Directory Domain Services. Das Hauptziel sollte darin bestehen, den Replikations Datenverkehr zu minimieren und eine effiziente Verwaltung und Wartung von Objekten zu ermöglichen.

Beachten Sie, dass Client Anwendungen SCPs suchen, indem Sie im Verzeichnis nach Schlüsselwörtern im SCP suchen. Das **Schlüssel** Wort Attribut eines SCP ist im globalen Katalog enthalten. Clients können den globalen Katalog durchsuchen, um SCPs in der Gesamtstruktur zu finden. Aus diesem Grund hat der Client keinen Einfluss darauf, wo SCPs veröffentlicht werden soll.

## <a name="minimize-replication-traffic"></a>Minimierung des Replikations

Um den Replikations Datenverkehr zu minimieren, erstellen Sie SCPs in der Domänen Partition der Domäne des Dienst Host Computers. Beispielsweise können Sie SCPs als untergeordnete Objekte des Computer Objekts erstellen, auf dem der Dienst installiert ist. Eine Domänen Partition von Active Directory Domain Services, die manchmal als Domänen namens Kontext bezeichnet wird, enthält domänenspezifische Objekte, z. b. die Objekte für die Benutzer und Computer der Domäne. Ein vollständiges Replikat aller Objekte in der Domänen Partition wird auf jedem Domänen Controller (DC) für die Domäne repliziert, aber nicht an DCS anderer Domänen repliziert.

Erstellen Sie SCPs nicht in der Konfigurations Partition (auch als Konfigurations namens Kontext bezeichnet), da Änderungen an der Konfigurations Partition an alle Domänen Controller in der Gesamtstruktur repliziert werden. Wie bereits erwähnt, können Clients in der Gesamtstruktur den globalen Katalog Abfragen, um die SCPS überall in der Gesamtstruktur zu finden, sodass das Erstellen von SCPs in der Konfigurations Partition nicht mehr für Clients sichtbar ist. Es wird nur mehr Replikations Datenverkehr generiert.

## <a name="ease-of-administration"></a>Einfache Verwaltung

Beachten Sie die folgenden Richtlinien für die Objekt Verwaltung:

-   Platzieren Sie Dienst spezifische Objekte, in denen Administratoren den Zugriff auf diese Objekte mithilfe von Richtlinien und geerbten Zugriffsberechtigungen steuern können.
-   Platzieren Sie die Objekte in, wo Sie von einem Administrator leicht gefunden werden können.

Ein guter Standard Speicherort, der beide Ziele erfüllt, besteht darin, SCP und andere Dienst spezifische Objekte unter dem Computer Objekt des Host Computers jeder Dienst Instanz zu erstellen. Weitere Informationen finden Sie [unter Veröffentlichen unter einem Computer Objekt](publishing-under-a-computer-object.md).

Eine gute Alternative für Dienste, die nicht an einen einzelnen Host gebunden sind, besteht darin, einen Container für die Dienst Objekte unter dem System Container in einer Domänen Partition zu erstellen. Weitere Informationen finden Sie unter [Veröffentlichen in einem Domänen System Container](publishing-in-a-domain-system-container.md).

Das folgende Diagramm zeigt einen Teil der Standardcontainer Hierarchie für eine Domänen Partition.

![Standard Domänen Partitions-Container Hierarchie](images/domain-container-heirarchy.png)

Das Diagramm zeigt die Standard Domänen Hierarchie, die in Active Directory Domain Services enthalten ist. Viele Unternehmen erstellen jedoch eine Hierarchie von Organisationseinheiten-Containern, um Objektklassen, wie z. b. Benutzer und Computer, zum Zweck der Verwaltung zu gruppieren. Administratoren können dann Richtlinien und vererbbare Zugriffs Steuerungs Einträge (ACEs) auf eine Organisationseinheit anwenden, um die administrative Autorität für Objekte in der Organisationseinheit zu delegieren. Dies ermöglicht es Administratoren, ein Unternehmen effizient zu verwalten, aber es hat einige Folgen für Dienst Programmierer:

-   Das Computer Objekt für einen Dienst Host ist möglicherweise nicht unter dem Container "Computer", wie im Diagramm dargestellt. Weitere Informationen zum Suchen des Computer Objekts für den lokalen Computer finden Sie [unter Veröffentlichen unter einem Computer Objekt](publishing-under-a-computer-object.md).
-   Administratoren können Objekte verschieben, wenn sich Ihre Organisations Anforderungen ändern. Dies bedeutet, dass Sie nicht von ihren Objekten abhängig sind, die an einem festgelegten Speicherort verbleiben. Das heißt, dass der Dienst nicht von einem anderen Objekt definierten Namen abhängig ist. Verwenden Sie stattdessen das **objectGUID** -Attribut eines Objekts, das sich nicht ändert, wenn das Objekt verschoben oder umbenannt wird. Weitere Informationen und ein Codebeispiel, in dem ein SCP erstellt wird, speichert seine **objectGUID** und ruft später die **objectGUID** ab, um eine Bindung an den SCP herzustellen, finden Sie unter [Erstellen und Verwalten eines Dienst Verbindungs Punkts](creating-and-maintaining-a-service-connection-point.md).
-   Alle Dienst bezogenen Standard Objektklassen sowie alle Unterklassen dieser Klassen sind gültige untergeordnete Elemente der Klassen " **Computer** " und " **OrganizationalUnit** ". Wenn Sie das Schema erweitern, um eine eigene Dienst spezifische Klasse zu definieren, stellen Sie sicher, dass die **Computer** -und **OrganizationalUnit** -Klassen in den möglichen Vorgesetzten enthalten sind.
-   Das Dienst Installationsprogramm bestimmt den Standard Speicherort für das Erstellen von SCPs. Sie können zulassen, dass der Administrator, der den Dienst installiert, einen alternativen Installationspfad angibt.

Dienst spezifische Objekte sollten nicht in den folgenden Bereichen erstellt werden:

-   Dienste sollten Objekte nicht direkt in den Benutzern oder Computern einer Domänen Partition veröffentlichen, und Sie sollten auch keine neuen Container in diesen Containern erstellen. Allerdings können-Dienste Objekte als untergeordnete Objekte eines Computer Objekts veröffentlichen, unabhängig davon, ob das Computer Objekt im Container Computer gespeichert ist.
-   Dienste, die die APIs für die Registrierung und Auflösung von Windows Sockets (RNR) oder RPC Name Service (RpcNs) verwenden, erstellen die richtigen Objekte in den Containern winsockservices und rpcservices unter dem System Container einer Domänen Partition. Erstellen Sie Objekte in diesen Containern nicht explizit. Dies führt nicht zu direkten Schäden, kann aber für Administratoren verwirrend sein.

 

 




