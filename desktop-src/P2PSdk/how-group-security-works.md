---
description: Für Peer Gruppen ist es erforderlich, dass jedes Mitglied über ein bestimmtes Zertifikat verfügt, das als Gruppenmitglieds Zertifikat (GMC) bezeichnet wird.
ms.assetid: 3966d4eb-4504-4b1e-9c9f-6eab7751d7ed
title: Funktionsweise der Gruppen Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d272e9a0567c6edc300a52cfa206305253ec5a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865155"
---
# <a name="how-group-security-works"></a>Funktionsweise der Gruppen Sicherheit

Für Peer Gruppen ist es erforderlich, dass jedes Mitglied über ein bestimmtes Zertifikat verfügt, das als Gruppenmitglieds Zertifikat (GMC) bezeichnet wird. Mit dem GMC-Zertifikat wird sichergestellt, dass alle zwischen Peers ausgetauschten Datensätze digital signiert sind. Der öffentliche Schlüssel eines Peers ist in den Strukturen enthalten, die als Teil der Kommunikation zwischen Peers – einschließlich Peer-Anmelde [**\_ \_ Informationen**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info), übermittelt werden.

Eine GMC kann in einer Kette ausgestellt werden. Ein Ersteller kann z. B. eine GMC an Administrator a ausstellen, der eine GMC für Administrator B ausstellen kann, der eine GMC für das Mitglied M ausgeben kann. Die resultierende GMC-Kette ist: Creator->A->B->M, das eine Länge von 4 hat. Die Kettenlänge ist wichtig, da Sie nicht länger als 24 sein darf. Wenn der 24. Administrator in einer Kette versucht, eine GMC an einen Member auszugeben, gibt [**peergroupissuecredenseins**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) oder [**peergroupkreateinvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) eine Peer- \_ E- \_ Kette \_ zu lang zurück \_ .

Eine GMC kann auch durch Aufrufen von " [**Peer groupissuecredenseins**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)" ausgegeben werden. Eine GMC impliziert eine Benutzer Mitgliedschaft in der Gruppe, für die die GMC ausgestellt wird, und kann eine begrenzte oder unbegrenzte Lebensdauer aufweisen. Die Aktivität "Gruppenmitglied" darf nicht länger als die in der GMC angegebene Gültigkeitsdauer sein.

> [!Note]  
> Die unbegrenzte Lebensdauer der GMC ist zurzeit auf 1000 Jahre festgelegt.

 

Die Gruppenmitglieder Aktivität wird durch die GMC-Lebensdauer beschränkt und umfasst Folgendes:

-   Daten **Satz Vorgänge** : ein Peer kann keine Informationen in einer Gruppe veröffentlichen, nachdem die Gruppenmitgliedschaft abgelaufen ist, oder Datensätze veröffentlichen, deren Lebensdauer länger als die Lebensdauer der Peer Mitgliedschaft ist.
-   **Mitgliedschafts Vorgänge** : ein Gruppenadministrator kann keine Mitgliedschaft ausstellen, die über das in der Gruppenadministrator Mitgliedschaft angegebene Datum hinausgeht. Wenn ein Administrator beispielsweise 500 Stunden für die GMC-Lebensdauer verbleiben, müssen alle ausgegebenen Mitgliedschaften weniger als 500 Stunden betragen.

Da für ein Gruppenmitglied nicht länger als für den Administrator, der das Mitglied der Gruppe ist, eine Gültigkeitsdauer festgelegt werden kann, empfiehlt es sich, die GMC-Lebensdauer eines Administrators als unendlich oder für eine sehr lange Lebensdauer festzulegen. Der Ersteller der Gruppe weist standardmäßig eine unbegrenzte Lebensdauer auf.

## <a name="renewing-group-membership"></a>Erneuern der Gruppenmitgliedschaft

Zum Erneuern der Anmelde Informationen eines Administrators oder Mitglieds, dessen GMC-Lebensdauer bereit ist, stehen Ihnen die folgenden beiden Optionen zur folgenden zur Folge:

-   Aufrufen von " [**Peer groupissuecredenseins**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) " und übergeben der Identität des Members, dessen Lebensdauer bereit ist, ablaufen zu lassen. Wenn die Anmelde Informationen als **null** angegeben werden und die Mitgliedschafts Informationen des Peers der Gruppe zur Verfügung stehen, wird die Erneuerungszeit auf dieselbe Dauer festgelegt, die in den zuvor veröffentlichten Anmelde Informationen für das Mitglied angegeben ist. Wenn ein anderer Zeitraum angegeben werden muss, muss eine neue [**Peer \_ Credential \_ Info**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) -Struktur bereitgestellt werden, die die neue Lebensdauer enthält. Anschließend wird eine neue GMC für das Element veröffentlicht.

    Die [**peergroupissuecredenseins**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) -Funktion übernimmt optional das Kennzeichen für die Peer \_ Gruppen- \_ Anmelde Informationen \_ , mit dem die neuen Anmelde Informationen des Mitglieds in der Gruppen Datenbank automatisch veröffentlicht werden. Wenn der Member zum nächsten Mal eine Verbindung mit der Gruppe herstellt, erhält das Mitglied zum ersten Mal oder nach dem Offline schalten die aktualisierte GMC aus der Datenbank.

-   Aufrufen von " [**Peer groupkreateinvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) " zum übergeben der Identität des Members, dessen GMC-Lebensdauer bereit zum ablaufen ist. Wenn die in der Einladung angegebene Ablaufzeit **null** ist, entspricht die Gültigkeitsdauer der GMC dem Administrator-GMC, der die Mitgliedschaft ausgibt. Wenn der Ersteller den Ablauf als **null** angibt, wird eine GMC mit einer unendlichen Lebensdauer ausgegeben.

    Wenn für einen Peer eine GMC ausgegeben wird, die vor dem Anwesenheits Lebensdauer-Wert abläuft, sind die Adressen des Peers nicht in den [**\_ peermember**](/windows/desktop/api/P2P/ns-p2p-peer_member) -Strukturen verfügbar, die in der durch einen [**peergroupummembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)-Aufrufe initiierten Enumeration zurückgegeben werden. Dies liegt daran, dass Anwesenheits Informationen in diesem Fall nicht veröffentlicht werden, auch wenn das Flag zum Deaktivieren des Peers \_ \_ nicht festgelegt ist.

 

 



