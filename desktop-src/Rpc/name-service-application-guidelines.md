---
title: Richtlinien für die Namensdienstanwendung
description: Wenn Sie Ihre verteilte Anwendung entwickeln, müssen Sie den Anwendungsbenutzern eine Methode zum Angeben des Namens bereitstellen, unter dem sie die Anwendung in der Namensdienstdatenbank registrieren können.
ms.assetid: cda997b3-6031-4c0f-affc-c766ba4b7fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e0e79f8ddb9e2076da8d7b8d2c275cb1b1941f6867bfea68dd46bc6c352d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927829"
---
# <a name="name-service-application-guidelines"></a>Richtlinien für die Namensdienstanwendung

Wenn Sie Ihre verteilte Anwendung entwickeln, müssen Sie den Anwendungsbenutzern eine Methode zum Angeben des Namens bereitstellen, unter dem sie die Anwendung in der Namensdienstdatenbank registrieren können. Diese Methode kann aus einer Datendatei, einer Befehlszeileneingabe oder einem Dialogfeld bestehen.

Obwohl die Architektur des RPC-Namensdiensts verschiedene Methoden zum Organisieren der Servereinträge einer Anwendung unterstützt, ist sie für Nachschlageverfahren optimiert. Daher können häufige Updates die Leistung des Namensdiensts und der Anwendung beeinträchtigen. Um das unnötige Exportieren von Informationen zu vermeiden, wählen Sie einen Entwurf aus, mit dem der Server bestimmen kann, ob seine Informationen in der Namensdienstdatenbank enthalten sind. Darüber hinaus sollte jede Serverinstanz in ihren eigenen Eintragsnamen exportieren. Andernfalls ist es für eine Instanz schwierig, ihre unterstützten Objekt-UUIDs oder Protokollsequenzen zu ändern, ohne die Informationen einer anderen Instanz zu stören.

Die folgende Methode vermeidet diese Fallstricke und bietet eine gute Leistung, unabhängig davon, welchen Namensdienst Ihr Netzwerk verwendet.

Entwerfen Sie zunächst Ihre Anwendung so, dass sie beim ersten Start einer bestimmten Serverinstanz einen eindeutigen Servereintragsnamen auswählt und diesen Namen zusammen mit den anderen Konfigurationsinformationen der Anwendung in der Registrierung speichert. Anschließend muss er seine Bindungshandles und Objekt-UUIDs (sofern dies der Fall ist) in seinen Namensdiensteintrag exportieren.

Nachfolgende Aufrufe der Serverinstanz sollten überprüfen, ob der Name-Diensteintrag vorhanden ist und den richtigen Satz von Objekt-UUIDs und Bindungshandles enthält. Ein fehlender Eintrag kann bedeuten, dass ein Administrator ihn entfernt hat oder dass ein Stromausfall dazu führte, dass die Namensdienstinformationen verloren gegangen sind. Es ist wichtig zu überprüfen, ob die Bindungshandles im Eintrag richtig sind. Wenn ein Administrator einem Computer beispielsweise TCP/IP-Unterstützung hinzufügt, lauschen RPC-Server beim Aufrufen von [**RpcServerUseAllProtseqs auf diese Protokollsequenz.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs) Wenn der Server den Namensdiensteintrag jedoch nicht aktualisiert, werden Clients nicht darüber informiert, dass TCP unterstützt wird.

Wenn der Client importiert, sollte er **NULL** als Eintragsnamen angeben. Die Angabe **von NULL** bewirkt, dass die Microsoft RPC-Bibliotheksfunktionen in allen Namensdiensteinträgen in der Domäne oder Arbeitsgruppe des Clientcomputers nach der Schnittstelle suchen und so die Informationen für jede Instanz finden.

Wenn Sie Objekt-UUIDs verwenden, um bekannte Objekte wie Drucker darstellen, können Sie eine Variante dieser Methode verwenden. Anstatt Bindungen in einen Eintrag zu exportieren, entwerfen Sie Ihre Anwendung so, dass jede Instanz einen Eintrag für jedes unterstützte Objekt erstellt, z. B. "/.:/". printer/Scanner1" und "/.:/ printer/Scanner2." Anschließend muss der Server seine Bindungshandles zusammen mit der für diesen Eintrag relevanten Objekt-UUID in jeden Servereintrag exportieren.

In diesem Fall kann ein Client eine Ressource nach Namen suchen, indem er aus dem relevanten Servereintrag importiert. Die Objekt-UUID der Ressource ist nicht erforderlich. Wenn sie über die Ressourcen-UUID, aber nicht über den Namen verfügt, kann sie aus dem **NULL-Eintrag importieren.**

 

 




