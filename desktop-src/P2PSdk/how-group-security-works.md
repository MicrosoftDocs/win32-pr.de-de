---
description: Peergruppen erfordern, dass jedes Mitglied über ein bestimmtes Zertifikat verfügt, das als Gruppenmitgliedszertifikat (Group Member Certificate, GMC) bezeichnet wird.
ms.assetid: 3966d4eb-4504-4b1e-9c9f-6eab7751d7ed
title: Funktionsweise der Gruppensicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0941b4bded19b914218d5c011e8696cdd9c92612a493954dc5dd45d91e59006a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675210"
---
# <a name="how-group-security-works"></a>Funktionsweise der Gruppensicherheit

Peergruppen erfordern, dass jedes Mitglied über ein bestimmtes Zertifikat verfügt, das als Gruppenmitgliedszertifikat (Group Member Certificate, GMC) bezeichnet wird. Das GMC-Zertifikat stellt sicher, dass alle zwischen Peers ausgetauschten Datensätze digital signiert sind. Der öffentliche Schlüssel eines Peers ist in den Strukturen enthalten, die als Teil der Kommunikation zwischen Peers übergeben werden, einschließlich [**PEER \_ CREDENTIAL \_ INFO.**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info)

Ein GMC kann in einer Kette ausgegeben werden. Beispielsweise kann ein Ersteller ein GMC für Administrator A ausstellen, der ein GMC an Administrator B ausstellen kann, der ein GMC für Mitglied M ausstellen kann. Die resultierende GMC-Kette ist: Creator->A->B->M, die eine Länge von 4 hat. Die Kettenlänge ist wichtig, da sie nicht länger als 24 sein darf. Wenn der 24. Administrator in einer Kette versucht, ein GMC für ein Mitglied auszugeben, gibt [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) oder [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) PEER \_ E CHAIN TOO LONG \_ \_ \_ zurück.

Ein GMC kann auch durch Aufrufen von [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)ausgegeben werden. Ein GMC impliziert die Benutzermitgliedschaft in der Gruppe, für die der GMC ausgestellt wird, und kann eine begrenzte oder unendliche Lebensdauer aufweisen. Die Gruppenmitgliedsaktivität darf nicht länger als die im GMC angegebene Lebensdauer sein.

> [!Note]  
> Die unbegrenzte GMC-Lebensdauer ist derzeit auf 1.000 Jahre festgelegt.

 

Die Gruppenmitgliedsaktivität ist durch die GMC-Lebensdauer beschränkt und umfasst Folgendes:

-   **Datensatzvorgänge:** Ein Peer kann keine Informationen in einer Gruppe veröffentlichen, nachdem die Gruppenmitgliedschaft abgelaufen ist, oder Datensätze veröffentlichen, deren Lebensdauer länger ist als die Gruppenmitgliedschaftsdauer des Peers.
-   **Mitgliedschaftsvorgänge:** Ein Gruppenadministrator kann keine Mitgliedschaft ausstellen, deren Lebensdauer über das in der Gruppenadministratormitgliedschaft angegebene Datum hinausgeht. Wenn ein Administrator beispielsweise 500 Stunden für seine GMC-Lebensdauer übrig hat, müssen alle ausgestellten Mitgliedschaften weniger als 500 Stunden betragen.

Da ein Gruppenmitglied keine längere Lebensdauer als der Administrator haben kann, der dieses Gruppenmitglied einlädt, wird empfohlen, die GMC-Lebensdauer eines Administrators als unendlich oder für eine sehr lange Lebensdauer festzulegen. Der Gruppenersteller verfügt standardmäßig über eine unbegrenzte Lebensdauer.

## <a name="renewing-group-membership"></a>Erneuern der Gruppenmitgliedschaft

Zum Erneuern der Anmeldeinformationen eines Administrators oder Mitglieds, dessen GMC-Lebensdauer läuft, haben Sie die folgenden beiden Optionen:

-   Rufen Sie [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) auf, und übergeben Sie die Identität des Members, dessen Lebensdauer läuft. Wenn die Anmeldeinformationen als **NULL** angegeben sind und die Mitgliedschaftsinformationen des Peers für die Gruppe verfügbar sind, wird die Verlängerungszeit auf die gleiche Dauer festgelegt, die in den zuvor veröffentlichten Anmeldeinformationen des Mitglieds angegeben ist. Wenn ein anderer Zeitraum angegeben werden muss, muss eine neue [**PEER \_ CREDENTIAL \_ INFO-Struktur**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) bereitgestellt werden, die die neue Lebensdauerdauer enthält, und dann wird ein neues GMC für den Member veröffentlicht.

    Die [**PeerGroupIssueCredentials-Funktion**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) verwendet optional das Flag PEER \_ GROUP STORE \_ \_ CREDENTIALS, das automatisch die neuen Anmeldeinformationen des Mitglieds in der Gruppendatenbank veröffentlicht. Wenn das Mitglied das nächste Mal eine Verbindung mit der Gruppe herstellt , entweder zum ersten Mal oder nach dem Offlineschalten, erhält das Mitglied die aktualisierte GMC aus der Datenbank.

-   Rufen Sie [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) auf, um die Identität des Members zu übergeben, dessen GMC-Lebensdauer läuft. Wenn der in der Einladung angegebene Ablauf **NULL** ist, entspricht die Lebensdauer des GMC dem Gmc-Administrator, der die Mitgliedschaft ausgibt. Wenn der Ersteller den Ablauf als **NULL** angibt, wird ein GMC mit einer unbegrenzten Lebensdauer ausgegeben.

    Wenn einem Peer ein GMC ausgestellt wird, der vor dem Wert für die Anwesenheitslebensdauer abläuft, sind die Adressen des Peers nicht in den [**PEER \_ MEMBER-Strukturen**](/windows/desktop/api/P2P/ns-p2p-peer_member) verfügbar, die in der Enumeration zurückgegeben werden, die durch einen Aufruf von [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)initiiert wurde. Dies liegt daran, dass in diesem Fall keine Anwesenheitsinformationen veröffentlicht werden, auch wenn das FLAG PEER \_ DISABLE PRESENCE nicht festgelegt \_ ist.

 

 



