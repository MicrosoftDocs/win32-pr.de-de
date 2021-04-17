---
description: Die Peer-zu-Peer-Gruppierung ist eine Technologie, die es Entwicklern ermöglicht, schnell und effektiv ein sicheres Peer Netzwerk zu erstellen.
ms.assetid: ee72f60b-1e5b-4b69-bda0-2ae80734c144
title: Arbeiten mit Gruppen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7bebf958d0c3fdee6ad0dc400d495c54ec2e6fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529126"
---
# <a name="how-to-work-with-groups"></a>Arbeiten mit Gruppen

Die Peer-zu-Peer-Gruppierung ist eine Technologie, die es Entwicklern ermöglicht, schnell und effektiv ein sicheres Peer Netzwerk zu erstellen. In der folgenden Liste sind die wichtigsten Aspekte beim Erstellen einer Peer Gruppierungs Anwendung aufgeführt.

-   [Abrufen einer Peer Identität](#obtaining-a-peer-identity)
-   [Starten einer Peer Gruppe](#starting-up-the-peer-grouping-infrastructure)
-   [Registrieren für Gruppierungs Ereignisse](#registering-for-peer-grouping-events)
-   [Herstellen einer Verbindung mit einer Gruppe](#obtaining-a-group-handle)
-   [Erstellen von Administrator-und Mitglieds Rollen](#creating-administrator-and-member-roles)
-   [Suchen eines Peers](#finding-a-peer)
-   [Direkte Verbindung mit einem Peer](#connecting-directly-to-a-peer)
-   [Schließen und Herunterfahren einer Gruppe](#closing-and-shutting-down-a-peer-group)

## <a name="obtaining-a-peer-identity"></a>Abrufen einer Peer Identität

Vor dem Erstellen oder Herstellen einer Verbindung mit einer Gruppe muss ein Peer eine Peer Identität abrufen. dabei handelt es sich um einen Namen, der zum eindeutigen Identifizieren eines Peers für eine Gruppe verwendet wird. Rufen Sie zum Abrufen einer Aufzählungs Liste aller Peer Identitäten, die auf dem Peer definiert sind, [**peerenumidentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities)auf, das ein Handle für die-Enumeration zurückgibt. Rufen Sie zum Abrufen der Peer Identitäten [**peergetnextitem mit dem enumerationshandle**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) und der Anzahl der abzurufenden Member auf. Setzen Sie **peergetnextitem** fort, bis der *pcount* -Parameter einen Wert zurückgibt, der kleiner ist als die Anzahl der angeforderten Peer Identitäten.

Wenn keine Peer Identität für den Peer vorhanden ist, kann er durch Aufrufen von [**peeridentitycreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)erstellt werden. Nach dem Erstellen einer Peer Identität generiert der Peer ein XML-Identitäts-XML-BLOB, das den ihm zugewiesenen öffentlichen Schlüssel enthält.

Die Peer-Identitätsinformationen werden abgerufen, indem [**peeridentitygetxml**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml)aufgerufen wird. Diese Peer Identitätsinformationen werden vom Gruppen Ersteller oder einem Administrator verwendet, um die Anmelde Informationen, die für den Beitritt zur Gruppe erforderlich sind, als Einladungs-XML-BLOB auszugeben.

Weitere Informationen zu Peer Identitäten finden Sie in der Dokumentation zur [Identity Manager-API](identity-manager-api.md) .

## <a name="starting-up-the-peer-grouping-infrastructure"></a>Starten der Peer Gruppierungs Infrastruktur

Bevor eine Funktion in der Peer Gruppierungs-API von einer Anwendung aufgerufen wird, muss [**peergroupstartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) aufgerufen werden. Diese Funktion initialisiert die Peer Gruppierungs Infrastruktur für die Anwendung und legt die unterstützte Version fest.

## <a name="obtaining-a-group-handle"></a>Abrufen eines Gruppen Handles

Um eine Verbindung mit einer Gruppe herzustellen und mit der Teilnahme zu beginnen, muss ein Handle für eine Peer Gruppe abgerufen werden. In der folgenden Liste werden die drei Möglichkeiten zum Herstellen einer Verbindung mit einer Peer Gruppe beschrieben:

-   Erstellen einer Peer Gruppe durch Aufrufen von " [**peergroupcreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)", die eine neue Peer Gruppe initialisiert und ein gültiges Handle mit dem Peer als Besitzer und als alleinige Administrator zurückgibt.
-   Beitreten zu einer Peer Gruppe durch Aufrufen von [**peergroupjoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin). Zum beitreten zu einer Peer Gruppe muss ein Peer eine Einladung von einem Peer Gruppenadministrator erhalten. Um eine Einladung zu erhalten, senden Sie das XML-BLOB mit den Identitätsinformationen an den Administrator, der eine Einladung erstellt, und sendet Sie über einen externen Mechanismus, z. b. e-Mail oder FTP, an Sie. Die Einladung und Peer Identität werden an **peergroupjoin** übermittelt, wodurch ein gültiges Handle an die Gruppe zurückgegeben wird.
-   Öffnen einer Peer Gruppe, der ein Peer zuvor durch Aufrufen von [**peergroupopen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)beigetreten ist. In dieser Situation ist das Abrufen einer Einladung nicht erforderlich.

Nachdem Sie ein gültiges Peer Gruppen Handle von einer der oben genannten Funktionen erhalten haben, können Sie eine Verbindung mit einer Peer Gruppe herstellen, indem Sie [**peergroupconnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) mit dem neuen Handle aufrufen.

> [!Note]  
> Wenn bei der Verbindung mit einer Peer Gruppe ein Fehler auftritt, tritt das Ereignis der Peer \_ Gruppen \_ Ereignis \_ Verbindung \_ fehl. Der Handler kann versuchen, die Verbindung mit der Peer Gruppe wiederherzustellen.

 

## <a name="registering-for-peer-grouping-events"></a>Registrieren für Peer Gruppierungs Ereignisse

Bevor ein Peer an einer Peer Gruppe teilnimmt, muss sich der Peer für Peer Gruppen Ereignisse registrieren. Rufen Sie zum Registrieren für bestimmte Peer Ereignisse [**peergroupregisterevent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)auf, und übergeben Sie einen oder mehrere der in Peer \_ Group \_ Event Type definierten Peer Ereignis Typen \_ . Sie müssen für jedes Peer Ereignis, das für Ihre Anwendung gilt, registrieren. Wenn Sie z. b. Daten über eine direkte Verbindung empfangen möchten, registrieren Sie sich für die \_ \_ Ereignisdaten Ereignisse der Peer Gruppe Ereignis \_ Direct \_ Connection und Peer \_ Group \_ Event \_ eingehende \_ Daten. Jeder-Rückruf nimmt ein Ereignis Handle an und gibt ein **hpeerevent** -Handle für dieses Peer Ereignis zurück.

Ereignishandler können die einem Peer Ereignis zugeordneten Daten abrufen, indem Sie das Handle an die registrierten Peer Ereignisse an [**peergroupgeteventdata**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)übergeben. Diese Peer Ereignisdaten werden als Peer Gruppen- \_ \_ Ereignis \_ Daten Union zurückgegeben. Wenn die Peer-Ereignis Warteschlange leer ist, gibt diese Funktion \_ Peers \_ keine \_ Ereignis \_ Daten zurück.

Sie können die Registrierung für Peer Ereignisse aufheben, indem Sie [**peergroupunregisterevent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) aufrufen und das Handle für das Peer Ereignis bereitstellen, dessen Registrierung Sie aufheben möchten. Nachdem die Funktion aufgerufen wurde, werden die dem Handle zugeordneten Peer Ereignisse nicht mehr registriert.

## <a name="creating-administrator-and-member-roles"></a>Erstellen von Administrator-und Mitglieds Rollen

Der Peer, der die Peer Gruppe erstellt, wird als Peer Gruppen Ersteller bezeichnet und verfügt standardmäßig über die Administrator Rolle. Die Gruppen Eigenschaften können nur vom Ersteller der Peer Gruppe festgelegt werden.

Peers, die in die Peer Gruppe eingeladen werden, können entweder ein Administrator oder ein Mitglied sein. Wenn dem Administrator, der die Einladung ausgibt, eine Administrator Rolle zugewiesen wird, können Sie neue Mitglieder zur Peer Gruppe einladen und gleichermaßen anderen Mitgliedern die Administrator Rolle zuweisen.

Die Rollen der Peer Gruppenmitglieder werden in den Einladungen festgelegt, die der Administrator an ein Mitglied übergibt. Wenn Sie weitere Administratoren hinzufügen möchten, legen Sie den Wert des *proles* -Parameters von [**peergroupforateinvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) \_ bei der \_ Erstellung einer Einladung auf Peer Group role \_ Admin fest.

Mitglieder können an einer Peer Gruppe teilnehmen, aber keine neuen Mitglieder einladen und autorisieren, Gruppen Eigenschaften festlegen oder Gruppendaten Sätze aktualisieren oder löschen, die nicht speziell erstellt werden. Legen Sie zum Zuweisen eines Mitgliedsstatus zu einem teilnehmenden Peer den Wert des **proles** -Parameters von [**peergroupkreateinvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) auf Peer \_ Group \_ Role Member fest, \_ Wenn Sie eine Einladung für diesen Peer erstellen.

Um die Rolle eines Mitglieds zu ändern, müssen neue Anmelde Informationen, die die neue Rolle enthalten, an dieses Mitglied ausgegeben werden. Um dies zu erreichen, rufen Sie die [**Peer \_ Credential \_ Info**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) -Struktur für dieses Element aus der Peer Elementstruktur ab, die \_ von [**peergroupumschlag Members**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)zurückgegeben wurde. Ändern Sie das Feld " **proles** " in **Peer \_ Credential \_ Info** in die neue Rolle, und übergeben Sie die Struktur an [**peergroupissuecredential**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials).

Die neuen Anmelde Informationen werden erst dann für den Peer wirksam, wenn Sie eine Verbindung mit der Peer Gruppe herstellen. Wenn Sie derzeit verbunden sind, müssen Sie die Gruppe schließen und die Verbindung wiederherstellen, um die aktualisierten Anmelde Informationen abzurufen.

## <a name="finding-a-peer"></a>Suchen eines Peers

Rufen Sie zum Abrufen einer Aufzählungs Liste aller Peers, die an der Peer Gruppe teilnehmen, [**peergroupummembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) mit dem Gruppen Handle auf, das ein Handle für die-Enumeration zurückgibt. Rufen Sie zum Abrufen der Member " [**Peer GetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) " mit dem enumerationshandle und der Anzahl der abzurufenden Member auf. Fahren Sie mit dem Aufrufen von " **Peer GetNextItem** " fort, bis der Parameter " *pcount* " einen niedrigeren Wert als die Anzahl der angeforderten Member zurückgibt Beachten Sie, dass die komplette Liste der verfügbaren Mitglieder möglicherweise nicht zurückgegeben wird.

Jeder Member wird als Peer Element [**Struktur \_**](/windows/desktop/api/P2P/ns-p2p-peer_member) dargestellt, die die Identität des Peers, der Knoten-IDs und der IP-Adressen für aktive Peers enthält.

Wenn Sie fertig sind, schließen Sie die Enumeration, und geben Sie den zugeordneten Speicher frei, indem Sie " [**Peer Enumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration)" aufrufen.

## <a name="connecting-directly-to-a-peer"></a>Direkte Verbindung mit einem Peer

Wenn ein Peer mit einer Peer Gruppe verbunden ist, wird der direkte Austausch mit anderen verbundenen Mitgliedern initiiert, indem [**peergroupopendirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) aufgerufen und die Identität des anderen Peers bereitgestellt wird. Dieser Rückruf ist asynchron und gibt eine 64-Bit-Verbindungs-ID zurück. Wenn der-Vorgang erfolgreich ist, erhalten Sie das Peer \_ Group \_ Event \_ Direct Connection- \_ \_ Ereignis Peer Ereignis, um anzuzeigen, dass die Verbindung erfolgreich hergestellt wurde. Wenn die Verbindung erfolgreich ist, ist die Verbindungs-ID gültig und kann zum Senden und empfangen von Daten über die direkte Verbindung verwendet werden.

Damit direkte Verbindungen empfangen werden können, muss sich der andere Peer auch zuvor für das Peer \_ Group \_ Event \_ Direct \_ Connection Peer-Ereignis registriert haben.

Um Daten an einen Peer zu senden, nennen Sie [**peergroupsenddata**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) mit einer gültigen Verbindungs-ID. Zum Empfangen von Daten muss der andere Peer für das \_ \_ Ereignis \_ eingehender Daten Peer Gruppen Ereignis \_ für Peer Gruppen registriert werden. Wenn der sendende Peer wiederum Daten empfangen möchte, muss er auch für das \_ \_ Ereignis für \_ eingehende \_ Daten Peer Gruppen Ereignisse registriert werden.

Um den Gesamtsatz der derzeit aktiven direkten Verbindungen mit anderen Peers in einer Gruppe zu empfangen, können Sie [**peergroupumconnections**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections) aufrufen, um die Enumeration zu öffnen und die Liste der Verbindungen mithilfe von [**peergetnextitem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem)zu durchlaufen.

Um eine direkte Verbindung zu schließen, nennen Sie " [**Peer groupclosedirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) ", und übergeben Sie die Verbindungs-ID.

## <a name="closing-and-shutting-down-a-peer-group"></a>Schließen und Herunterfahren einer Peer Gruppe

Um eine Verbindung mit einer Peer Gruppe zu schließen, können Sie [**peergroupclose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose)aufrufen, wodurch das Gruppen Handle ungültig wird, aber die Peer Gruppierungs Infrastruktur nicht heruntergefahren wird. Peer-zu-Peer-Gruppendaten werden durch Aufrufen von [**peergroupdelete**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)gelöscht.

Wenn die Anwendung mit der Peer Gruppierungs Infrastruktur fertig ist, muss Sie [**peergroupshutdown**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown)aufrufen.

 

 



