---
description: In diesem Thema wird erläutert, wie Sie einen Peer zum beitreten zu einer Peer Gruppe mithilfe der Peer Gruppierungs-APIs einladen.
ms.assetid: 6afcbfec-b1df-45cd-8a43-221dfe5d8c33
title: Einladen eines Peers zu einer Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68b1e8852f58387d424944d4a8821f56b5e11e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959784"
---
# <a name="inviting-a-peer-to-a-group"></a>Einladen eines Peers zu einer Gruppe

In diesem Thema wird erläutert, wie Sie einen Peer zum beitreten zu einer Peer Gruppe mithilfe der Peer Gruppierungs-APIs einladen.

Eine Peer Gruppe benötigt gültige Anmelde Informationen, um teilnehmen zu können. Anmelde Informationen werden von außerhalb einer Gruppe in Form von Einladungen oder direkt an Mitglieder innerhalb einer Gruppe ausgegeben, wenn Aktualisierungen von Anmelde Informationen benötigt werden.

## <a name="group-member-certificates"></a>Gruppenmitglieder Zertifikate

Eine Peer Gruppe wird erstellt, wenn eine Anwendung [**peergroupcreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)aufruft.

Um an einer Peer Gruppe teilnehmen zu können, muss jeder Peer über eine Peer Identität verfügen. Nennen Sie [**peertenumidentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) , bis alle für den Peer definierten Peer Identitäten zurückgegeben wurden, und wählen Sie die zu verwendende. Wenn keine Peer Identität vorhanden ist, erstellen Sie eine, indem Sie [**peeridentitycreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)aufrufen.

Jede Peer Identität ist einem bestimmten Satz von Anmelde Informationen zugeordnet, die verwendet werden können, um die Peer Gruppenmitgliedschaft beim Herstellen einer Verbindung zu beweisen, sowie zum Veröffentlichen von Datensätzen oder zum einladen zusätzlicher Mitglieder. Diese Anmelde Informationen werden als Ketten von [X. 509-Zertifikaten](https://www.ietf.org/rfc/rfc2511.txt) dargestellt, die Gruppen Mitgliedschafts Zertifikate (GMC) genannt werden.

Um die GMC für eine Peer Identität zu erstellen, müssen Sie zuerst Ihren öffentlichen Schlüssel abrufen. Dieser Schlüssel wird abgerufen, indem [**peeridentitygetxml**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) für den potenziellen einladenden Empfänger aufgerufen und seine Peer Identität übergeben wird. Diese Funktion gibt ein Base-64-codiertes Zertifikat (IDC) zurück, das den öffentlichen RSA-Schlüssel enthält, der zum Erstellen der GMC für die Peer Identität (unter anderem) in einem XML-BLOB in folgendem Format verwendet wird:

``` syntax
<PEERIDENTITYINFO VERSION="1.0">
     <IDC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
          <!-- Base-64 encoded certificate  -->
     </IDC>
</PEERIDENTITYINFO>
```

Diese Zeichenfolge kann an [**peergroupkreateinvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)übergeben werden, die eine Einladung zurückgibt, die die GMC für diese Peer Identität enthält. Die Einladung muss an den einladenden Empfänger mit einem anderen Prozess, z. b. e-Mail, FTP oder einer sicheren Dateifreigabe, weitergeleitet werden.

Alternativ kann das IDC selbst in einer neuen [**Peer \_ Credential \_ Info**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) -Struktur abgelegt und an [**peergroupissuecredential**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)weitergeleitet werden, wodurch entsprechend eine Einladung generiert wird.

Beachten Sie, dass Anwendungen keine Tags innerhalb des " **Peer Identity tyinfo** "-Tags hinzufügen oder dieses XML-Fragment in irgendeiner Weise ändern dürfen. Anwendungen dürfen dieses XML-Fragment in andere XML-Dokumente einbinden, müssen jedoch alle anwendungsspezifischen XML-Daten entfernen, bevor Sie dieses Fragment an die Funktionen " [**Peer groupkreateinvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) " oder " [**Peer groupissuecredential**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) " übergeben.

Mitglied-gmcs werden von Administratoren und dem Ersteller der Peer Gruppe ausgegeben. Mitglieder müssen neue gmcs mit den erweiterten Lebens dauern ihrer gmcs abrufen, bevor die Ablaufzeit abgelaufen ist. Der Peer Gruppenadministrator gibt aktualisierte Anmelde Informationen durch Aufrufen von [**peergroupissuecredenseins**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) mit den vorhandenen Anmelde Informationen für diesen Peer aus.

Die [**Peer \_ Credential \_ Info**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) -Struktur enthält die grundlegenden Daten zum Mitgliedschaftsstatus eines Peers, einschließlich des öffentlichen Schlüssels für die zugehörige GMC. Neu ausgestellte Anmelde Informationen können in der Peer Gruppe veröffentlicht werden, indem das Flag für die Peer \_ Gruppen- \_ Anmelde Informationen \_ im [**peergroupissuecreden-**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)Befehl festgelegt wird. Wenn der Empfänger der neuen Anmelde Informationen der Peer Gruppe Beitritt, werden vorhandene Anmelde Informationen von der Peer Gruppierungs Infrastruktur aktualisiert.

## <a name="issuing-an-invitation"></a>Ausstellen einer Einladung

Ein Mitglied wird mit einer der beiden folgenden Methoden eingeladen, der Peer Gruppe beizutreten:

-   Ein Peer Gruppenadministrator ruft [**peergroupkreateinvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)auf und übergibt dabei die XML-Zeichenfolge mit den Identitätsinformationen, die der potenzielle einladende Empfänger über einen gemeinsamen out-of-Band-Mechanismus erhält, z. b. e-Mail oder eine im-Sitzung. Die Einladung wird auch über einen externen Prozess oder Mechanismus an den Peer übermittelt, der Sie schließlich als XML-Zeichenfolge oder Textdatei empfängt.
-   Ein Peer Gruppenadministrator ruft [**peergroupissuecredensts**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)auf. Um diese Funktion verwenden zu können, muss der Peer bereits Mitgliedschafts Informationen für die Peer Gruppe [**( \_ peermember**](/windows/desktop/api/P2P/ns-p2p-peer_member)) veröffentlicht haben oder über einen verfügbaren öffentlichen Schlüssel verfügen (dem RSA-Schlüsselpaar, das zum Erstellen der betreffidentität verwendet wurde). Im ersten Fall kann die für **peergroupissuecredential** erforderliche [**Peer \_ Credential \_ Info**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) -Struktur aus der peermember **- \_** Struktur abgerufen werden. in letzterem Fall kann eine neue **Peer \_ Credential \_ Info** -Struktur mit dem öffentlichen Schlüssel aufgefüllt werden.

Nach dem Empfang der Einladungs Zeichenfolge übergibt der Peer ihn an [**peergroupjoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) , um der Peer Gruppe beizutreten. Wenn der Aufruf von **peergroupjoin** erfolgreich ist, kann der Peer die Peer Gruppe später durch Aufrufen von [**peergroupopen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)öffnen.

## <a name="parsing-an-invitation"></a>Eine Einladung wird verarbeitet.

Optional kann eine Einladung analysiert werden, indem [**peergroupparamevitation**](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)aufgerufen wird, die eine [**Peer \_ Einladungs \_ Informations**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) Struktur zurückgibt. Die Felder in der Struktur können problemlos zu Anzeige Zwecken abgerufen werden.

 

 



