---
description: In diesem Thema wird der Prozess zum Einladen eines Peers zum Beitreten zu einer Peergruppe mithilfe der Peer grouping-APIs erläutert.
ms.assetid: 6afcbfec-b1df-45cd-8a43-221dfe5d8c33
title: Einladen eines Peers in eine Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8760c2fb6023d5332da74402726669367fee4f5102c99269fa8e603653a1e2eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612650"
---
# <a name="inviting-a-peer-to-a-group"></a>Einladen eines Peers in eine Gruppe

In diesem Thema wird der Prozess zum Einladen eines Peers zum Beitreten zu einer Peergruppe mithilfe der Peer grouping-APIs erläutert.

Eine Peergruppe benötigt gültige Anmeldeinformationen, um teilnehmen zu können. Anmeldeinformationen werden von außerhalb einer Gruppe in Form von Einladungen oder direkt an Mitglieder innerhalb einer Gruppe ausgegeben, wenn Aktualisierungen der Anmeldeinformationen erforderlich sind.

## <a name="group-member-certificates"></a>Gruppenmitgliedszertifikate

Eine Peergruppe wird erstellt, wenn eine Anwendung [**PeerGroupCreate aufruft.**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)

Um an einer Peergruppe teilnehmen zu können, muss jeder Peer über eine Peeridentität verfügen. Rufen [**Sie PeerEnumIdentities auf,**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) bis alle für den Peer definierten Peeridentitäten zurückgegeben wurden, und wählen Sie die identität aus, die verwendet werden soll. Wenn keine Peeridentität vorhanden ist, erstellen Sie eine, indem Sie [**PeerIdentityCreate aufrufen.**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)

Jede Peeridentität ist einem bestimmten Satz von Anmeldeinformationen zugeordnet, die zum Nachweisen der Peergruppenmitgliedschaft beim Herstellen einer Verbindung sowie beim Veröffentlichen von Datensätzen oder Einladen zusätzlicher Mitglieder verwendet werden können. Diese Anmeldeinformationen werden als Ketten von [X.509-Zertifikaten dargestellt, die](https://www.ietf.org/rfc/rfc2511.txt) als Gruppenmitgliedschaftszertifikate (Group Membership Certificates, GMC) bezeichnet werden.

Um die GMC für eine Peeridentität zu erstellen, müssen Sie zuerst ihren öffentlichen Schlüssel abrufen. Dieser Schlüssel wird durch Aufrufen von [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) für den potenziellen Eingeladenen und Übergeben seiner Peeridentität ermittelt. Diese Funktion gibt ein Base64-codiertes Zertifikat (Base64-codiertes Zertifikat, IDC) zurück, das den öffentlichen RSA-Schlüssel enthält, der zum Erstellen des GMC für die Peeridentität (unter anderem) verwendet wird, gekapselt in einem XML-Blob im folgenden Format:

``` syntax
<PEERIDENTITYINFO VERSION="1.0">
     <IDC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
          <!-- Base-64 encoded certificate  -->
     </IDC>
</PEERIDENTITYINFO>
```

Diese Zeichenfolge kann an [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)übergeben werden, die eine Einladung zurückgibt, die die GMC für diese Peeridentität enthält. Die Einladung muss mit einem anderen Prozess wie E-Mail, FTP oder einer sicheren Dateifreigabe an den Eingeladenen übergeben werden.

Alternativ kann das IDC selbst in einer neuen [**PEER \_ CREDENTIAL \_ INFO-Struktur**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) platziert und an [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)übergeben werden, die ebenfalls eine Einladung generiert.

Beachten Sie, dass Anwendungen keine Tags innerhalb des **PEERIDENTITYINFO-Tags** hinzufügen oder dieses XML-Fragment in irgendeiner Weise ändern dürfen. Anwendungen dürfen dieses XML-Fragment in andere XML-Dokumente integrieren, müssen jedoch alle anwendungsspezifischen XML-Daten ausziehen, bevor sie dieses Fragment an die [**Funktionen PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) oder [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) übergeben.

Mitglieds-GMCs werden von Administratoren und dem Ersteller der Peergruppe ausgestellt. Mitglieder müssen neue GMCs mit erweiterter Lebensdauer ihrer GMCs abrufen, bevor die Ablaufzeit verstrichen ist. Der Peergruppenadministrator gibt aktualisierte Anmeldeinformationen aus, indem er [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) mit den vorhandenen Anmeldeinformationen für diesen Peer aufruft.

Die [**PEER \_ CREDENTIAL \_ INFO-Struktur**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) enthält die grundlegenden Daten zum Mitgliedschaftsstatus eines Peers, einschließlich des öffentlichen Schlüssels für seine GMC. Neu ausgestellte Anmeldeinformationen können in der Peergruppe veröffentlicht werden, indem im Aufruf von \_ \_ \_ [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)das Flag PEER GROUP STORE CREDENTIALS (PEER GROUP STORE CREDENTIALS) angegeben wird. Wenn der Empfänger der neuen Anmeldeinformationen der Peergruppe beitritt, werden die vorhandenen Anmeldeinformationen von der Peer grouping Infrastructure aktualisiert.

## <a name="issuing-an-invitation"></a>Ausstellen einer Einladung

Ein Mitglied wird auf eine der beiden folgenden Arten eingeladen, der Peergruppe bei beitritten:

-   Ein Peergruppenadministrator ruft [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)auf und übergibt die XML-Zeichenfolge für Identitätsinformationen, die vom potenziellen Eingeladenen über einen allgemeinen Out-of-Band-Mechanismus wie E-Mail oder EINE IM-Sitzung erhalten wurde. Die Einladung wird auch über einen externen Prozess oder Mechanismus an den Peer übergeben, der sie letztendlich als XML-Zeichenfolge oder Textdatei erhält.
-   Ein Peergruppenadministrator ruft [**PeerGroupIssueCredentials auf.**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) Um diese Funktion verwenden zu können, muss der Peer bereits Mitgliedschaftsinformationen für die Peergruppe [**\_ (PEERMITGLIED)**](/windows/desktop/api/P2P/ns-p2p-peer_member)veröffentlicht haben oder über einen verfügbaren öffentlichen Schlüssel (des RSA-Schlüsselpaars, das zum Erstellen der Subjektidentität verwendet wird) verfügen. Im ersten Fall kann die für **PeerGroupIssueCredentials** erforderliche [**PEER \_ CREDENTIAL \_ INFO-Struktur**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) aus der **PEER \_ MEMBER-Struktur** ermittelt werden. Im letzteren Fall kann eine neue **PEER \_ CREDENTIAL \_ INFO-Struktur** mit dem öffentlichen Schlüssel aufgefüllt werden.

Nachdem die Einladungszeichenfolge empfangen wurde, übergibt der Peer sie an [**PeerGroupJoin,**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) um der Peergruppe bei beitreten zu können. Wenn der Aufruf von **PeerGroupJoin** erfolgreich ist, kann der Peer die Peergruppe später öffnen, indem er [**PeerGroupOpen aufruft.**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)

## <a name="parsing-an-invitation"></a>Analyse einer Einladung

Optional kann eine Einladung durch Aufrufen von [**PeerGroupParseInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)analysiert werden, das eine [**PEER INVITATION \_ \_ INFO-Struktur**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) zurückgibt. Die Felder in der -Struktur können zu Anzeigezwecken leicht ermittelt werden.

 

 



