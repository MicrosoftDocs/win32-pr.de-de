---
title: Richtlinien für die Namensdienst Anwendung
description: Wenn Sie die verteilte Anwendung entwickeln, müssen Sie den Anwendungs Benutzern eine Methode zur Angabe des Namens bereitstellen, unter dem Sie die Anwendung in der Name Service-Datenbank registrieren können.
ms.assetid: cda997b3-6031-4c0f-affc-c766ba4b7fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c67af441da7a51917ae92751345e860e6b0fc92b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947900"
---
# <a name="name-service-application-guidelines"></a>Richtlinien für die Namensdienst Anwendung

Wenn Sie die verteilte Anwendung entwickeln, müssen Sie den Anwendungs Benutzern eine Methode zur Angabe des Namens bereitstellen, unter dem Sie die Anwendung in der Name Service-Datenbank registrieren können. Diese Methode kann aus einer Datendatei, einer Befehlszeilen Eingabe oder einem Dialogfeld bestehen.

Obwohl die RPC-Namensdienst Architektur verschiedene Methoden zum Organisieren der Server Einträge einer Anwendung unterstützt, ist Sie für Suchvorgänge optimiert. Demzufolge kann die Leistung des Namens Dienstanbieter und der Anwendung durch häufige Aktualisierungen beeinträchtigt werden. Um zu vermeiden, dass Informationen unnötig exportiert werden, wählen Sie einen Entwurf aus, mit dem der Server feststellen kann, ob seine Informationen in der Name Service-Datenbank Außerdem sollte jede Serverinstanz in ihren eigenen Eintrags Namen exportieren. Andernfalls ist es für eine Instanz schwierig, ihre unterstützten Objekt-UUIDs oder Protokoll Sequenzen zu ändern, ohne dass die Informationen einer anderen Instanz gestört werden.

Mit der folgenden Methode werden diese Fehlerquellen vermieden und eine gute Leistung erzielt, unabhängig davon, welchen Namen Dienst Ihr Netzwerk verwendet.

Entwerfen Sie zunächst Ihre Anwendung so, dass beim ersten Start einer bestimmten Serverinstanz ein eindeutiger Name für den Server Eintrag ausgewählt und dieser Name zusammen mit den anderen Konfigurationsinformationen der Anwendung in der Registrierung gespeichert wird. Exportieren Sie dann die Bindungs Handles und Objekt-UUIDs (sofern vorhanden) in den Namen des Namens Diensts.

Bei nachfolgenden Aufrufen der Serverinstanz sollte überprüft werden, ob der Name-Dienst Eintrag vorhanden ist und den richtigen Satz von Objekt-UUIDs und Bindungs Handles enthält. Ein fehlender Eintrag kann darauf hinweisen, dass ein Administrator ihn entfernt hat oder dass ein Stromausfall dazu geführt hat, dass die Namen Dienst Informationen verloren gegangen sind. Es ist wichtig, zu überprüfen, ob die Bindungs Handles im Eintrag korrekt sind. Wenn ein Administrator einem Computer TCP/IP-Unterstützung hinzufügt, lauschen die RPC-Server z. b. auf diese Protokoll Sequenz, wenn Sie [**rpcserveruseallprotsqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)aufrufen. Wenn der Server den Namensdienst Eintrag jedoch nicht aktualisiert, werden Clients nicht darüber informiert, dass TCP unterstützt wird.

Wenn der Client importiert, sollte **null** als Eintrags Name angegeben werden. Das Angeben von **null** bewirkt, dass die Microsoft RPC-Bibliotheksfunktionen in allen Namensdienst Einträgen in der Domäne oder Arbeitsgruppe des Client Computers nach der Schnittstelle suchen, sodass die Informationen für jede Instanz gefunden werden.

Wenn Sie Objekt-UUIDs verwenden, um bekannte Objekte (z. b. Drucker) darzustellen, können Sie eine Variation dieser Methode verwenden. Anstatt Bindungen in einen Eintrag zu exportieren, entwerfen Sie Ihre Anwendung so, dass jede Instanz einen Eintrag für jedes unterstützte Objekt erstellt, z. b. "/.:/ Printer/laser1 "and"/.:/ Drucker/Laser2. " Dann soll der Server seine Bindungs Handles in jeden Server Eintrag Exportieren, zusammen mit dem für diesen Eintrag relevanten Objekt UUID.

In diesem Fall kann ein Client eine Ressource anhand des Namens suchen, indem Sie den entsprechenden Server Eintrag importiert. die Objekt-UUID der Ressource ist nicht erforderlich. Wenn Sie über die Ressourcen-UUID, aber nicht über den Namen verfügt, kann Sie aus dem **null** -Eintrag importiert werden.

 

 




