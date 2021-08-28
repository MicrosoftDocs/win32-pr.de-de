---
description: Peer-zu-Peer-Gruppierung ist eine Technologie, mit der Entwickler schnell und effektiv ein sicheres Peernetzwerk erstellen können.
ms.assetid: ee72f60b-1e5b-4b69-bda0-2ae80734c144
title: Arbeiten mit Gruppen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bce7280afe226fea20cde633a3971f62f606e1814ad4ab62bcc09025a125e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519390"
---
# <a name="how-to-work-with-groups"></a>Arbeiten mit Gruppen

Peer-zu-Peer-Gruppierung ist eine Technologie, mit der Entwickler schnell und effektiv ein sicheres Peernetzwerk erstellen können. In der folgenden Liste sind die wichtigsten Aspekte beim Erstellen einer Peergruppierungsanwendung aufgeführt.

-   [Abrufen einer Peeridentität](#obtaining-a-peer-identity)
-   [Starten einer Peergruppe](#starting-up-the-peer-grouping-infrastructure)
-   [Registrieren für Gruppierungsereignisse](#registering-for-peer-grouping-events)
-   [Herstellen einer Verbindung mit einer Gruppe](#obtaining-a-group-handle)
-   [Erstellen von Administrator- und Mitgliedsrollen](#creating-administrator-and-member-roles)
-   [Suchen eines Peers](#finding-a-peer)
-   [Direktes Herstellen einer Verbindung mit einem Peer](#connecting-directly-to-a-peer)
-   [Schließen und Herunterfahren einer Gruppe](#closing-and-shutting-down-a-peer-group)

## <a name="obtaining-a-peer-identity"></a>Abrufen einer Peeridentität

Vor dem Erstellen oder Herstellen einer Verbindung mit einer Gruppe muss ein Peer eine Peeridentität abrufen. Dabei handelt es sich um einen Namen, der verwendet wird, um einen Peer eindeutig mit einer Gruppe zu identifizieren. Um eine aufzählende Liste aller Peeridentitäten abzurufen, die für den Peer definiert sind, rufen Sie [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities)auf, der ein Handle für die Enumeration zurückgibt. Um die Peeridentitäten abzurufen, rufen [**Sie PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) mit dem Enumerationshandle und der Anzahl der abzurufenden Member auf. Fahren Sie mit dem Aufrufen von **PeerGetNextItem** fort, bis der *pCount-Parameter* einen Wert zurückgibt, der kleiner ist als die Anzahl der angeforderten Peeridentitäten.

Wenn keine Peeridentität für den Peer vorhanden ist, kann sie durch Aufrufen von [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)erstellt werden. Nach dem Erstellen einer Peeridentität generiert der Peer ein IDENTITÄTS-XML-Blob, das den ihm zugewiesenen öffentlichen Schlüssel enthält.

Die Peeridentitätsinformationen werden durch Aufrufen von [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml)abgerufen. Diese Peeridentitätsinformationen werden vom Ersteller der Gruppe oder einem Administrator verwendet, um die Anmeldeinformationen, die für den Beitritt zur Gruppe erforderlich sind, als XML-Einladungsblob auszugeben.

Weitere Informationen zu Peeridentitäten finden Sie in der [Identity Manager-API-Dokumentation.](identity-manager-api.md)

## <a name="starting-up-the-peer-grouping-infrastructure"></a>Starten der Peergruppierungsinfrastruktur

Bevor eine Funktion in der Peergruppierungs-API von einer Anwendung aufgerufen wird, muss [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) aufgerufen werden. Diese Funktion initialisiert die Peergruppierungsinfrastruktur für die Anwendung und legt die unterstützte Version fest.

## <a name="obtaining-a-group-handle"></a>Abrufen eines Gruppenhandle

Um eine Verbindung mit einer Gruppe herzustellen und mit der Teilnahme zu beginnen, muss ein Handle für eine Peergruppe abgerufen werden. In der folgenden Liste sind die drei Möglichkeiten zum Herstellen einer Verbindung mit einer Peergruppe aufgeführt:

-   Erstellen einer Peergruppe durch Aufrufen von [**PeerGroupCreate,**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)die eine neue Peergruppe initialisiert und ein gültiges Handle mit dem Peer als Besitzer und alleiniger Administrator zurückgibt.
-   Verknüpfen einer Peergruppe durch Aufrufen von [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin). Um einer Peergruppe beitreten zu können, muss ein Peer eine Einladung von einem Peergruppenadministrator erhalten. Um eine Einladung zu erhalten, senden Sie das XML-Blob für Identitätsinformationen an den Administrator, der eine Einladung erstellt, und sendet sie über einen externen Mechanismus wie E-Mail oder FTP an Sie. Die Einladungs- und Peeridentität werden an **PeerGroupJoin** übergeben, das ein gültiges Handle für die Gruppe zurückgibt.
-   Öffnen sie eine Peergruppe, der ein Peer zuvor beigetreten ist, indem [**Sie PeerGroupÖffnen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)aufrufen. In diesem Fall ist es nicht erforderlich, eine Einladung zu erhalten.

Nachdem Sie ein gültiges Peergruppenhandle aus einer der oben genannten Funktionen erhalten haben, können Sie eine Verbindung mit einer Peergruppe herstellen, indem Sie [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) mit dem neuen Handle aufrufen.

> [!Note]  
> Wenn die Verbindung mit einer Peergruppe fehlschlägt, tritt das \_ PEER GROUP EVENT CONNECTION \_ \_ \_ FAILED-Ereignis auf. Der Handler kann versuchen, die Verbindung mit der Peergruppe wiederherzustellen.

 

## <a name="registering-for-peer-grouping-events"></a>Registrieren für Peergruppierungsereignisse

Bevor ein Peer an einer Peergruppe teilnimmt, muss sich der Peer für Peergruppenereignisse registrieren. Um sich für bestimmte Peerereignisse zu registrieren, rufen Sie [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)auf, und übergeben Sie mindestens einen der in PEER GROUP EVENT TYPE definierten \_ Peerereignistypen. \_ \_ Sie müssen sich für jedes Peerereignis registrieren, das für Ihre Anwendung gilt. Registrieren Sie sich beispielsweise für die Ereignisse PEER GROUP EVENT DIRECT CONNECTION und PEER GROUP EVENT INCOMING DATA, um Daten über eine direkte Verbindung zu \_ \_ \_ \_ \_ \_ \_ \_ empfangen. Jeder Aufruf nimmt ein Ereignishandle entgegen und gibt ein **HPEEREVENT-Handle** für dieses Peerereignis zurück.

Ereignishandler können die einem Peerereignis zugeordneten Daten abrufen, indem sie das Handle an registrierte Peerereignisse an [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)übergeben. Diese Peerereignisdaten werden als PEER \_ GROUP \_ EVENT \_ DATA-Union zurückgegeben. Wenn die Peerereigniswarteschlange leer ist, gibt diese Funktion PEER \_ S NO EVENT DATA \_ \_ \_ zurück.

Sie können die Registrierung für Peerereignisse aufheben, indem Sie [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) aufrufen und das Handle für das Peerereignis bereitstellen, das Sie die Registrierung aufheben möchten. Nachdem die Funktion aufgerufen wurde, werden die peer-Ereignisse, die dem Handle zugeordnet sind, nicht mehr registriert.

## <a name="creating-administrator-and-member-roles"></a>Erstellen von Administrator- und Mitgliedsrollen

Der Peer, der die Peergruppe erstellt, wird als Ersteller der Peergruppe bezeichnet und verfügt standardmäßig über die Administratorrolle. Nur der Ersteller der Peergruppe kann die Gruppeneigenschaften festlegen.

Peers, die in die Peergruppe eingeladen werden, können entweder Administrator oder Mitglied sein. Wenn ihnen vom Administrator, der die Einladung ausgibt, eine Administratorrolle zugewiesen wird, können sie neue Mitglieder zur Peergruppe einladen und die Administratorrolle auch anderen Mitgliedern zuweisen.

Die Rollen von Peergruppenmitgliedern werden in den Einladungen festgelegt, die der Administrator einem Mitglied ausgibt. Um weitere Administratoren hinzuzufügen, legen Sie den Wert des *pRoles-Parameters* von [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) beim Erstellen einer Einladung auf PEER \_ GROUP ROLE ADMIN \_ \_ fest.

Mitglieder können an einer Peergruppe teilnehmen, aber keine neuen Mitglieder einladen und autorisieren, Gruppeneigenschaften festlegen oder Gruppendatensätze aktualisieren oder löschen, die sie nicht speziell erstellen. Legen Sie zum Zuweisen des Mitgliedsstatus zu einem teilnehmenden Peer den Wert des **pRoles-Parameters** von [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) auf PEER \_ GROUP ROLE MEMBER \_ \_ fest, wenn Sie eine Einladung für diesen Peer erstellen.

Um die Rolle eines Mitglieds zu ändern, müssen neue Anmeldeinformationen, die die neue Rolle enthalten, an dieses Mitglied ausgegeben werden. Rufen Sie hierzu die [**PEER \_ CREDENTIAL \_ INFO-Struktur**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) für diesen Member aus der PEER MEMBER-Struktur ab, die \_ von [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)zurückgegeben wird. Ändern Sie das Feld **pRoles** in **PEER CREDENTIAL \_ \_ INFO** in die neue Rolle, und übergeben Sie die Struktur an [**PeerGroupIssueCredentials.**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)

Die neuen Anmeldeinformationen werden für den Peer erst wirksam, wenn sie eine Verbindung mit der Peergruppe herstellen. Wenn sie derzeit verbunden sind, müssen sie die Gruppe schließen und erneut eine Verbindung herstellen, um die aktualisierten Anmeldeinformationen abzurufen.

## <a name="finding-a-peer"></a>Suchen eines Peers

Rufen Sie [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) mit dem Gruppenhandle auf, das ein Handle für die Enumeration zurückgibt, um eine aufzählende Liste aller Peers abzurufen, die an der Peergruppe teilnehmen. Rufen Sie [**peerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) mit dem Enumerationshandle und der Anzahl der abzurufenden Member auf, um die Member abzurufen. Fahren Sie mit dem Aufrufen von **PeerGetNextItem** fort, bis der *pCount-Parameter* einen Wert zurückgibt, der kleiner als die Anzahl der angeforderten Member ist. Beachten Sie, dass die vollständige Liste der verfügbaren Member möglicherweise nicht zurückgegeben wird.

Jedes Element wird als [**PEER \_ MEMBER-Struktur**](/windows/desktop/api/P2P/ns-p2p-peer_member) dargestellt, die die Identität des Peers, der Knoten-IDs und der IP-Adressen für aktive Peers enthält.

Schließen Sie abschließend die -Enumeration, und geben Sie den zugeordneten Arbeitsspeicher frei, indem Sie [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration)aufrufen.

## <a name="connecting-directly-to-a-peer"></a>Direktes Herstellen einer Verbindung mit einem Peer

Wenn ein Peer mit einer Peergruppe verbunden ist, werden direkte 1:1-Austauschvorgänge mit anderen verbundenen Mitgliedern initiiert, indem [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) aufgerufen und die Identität des anderen Peers zur Verfügung gestellt wird. Dieser Aufruf ist asynchron und gibt eine 64-Bit-Verbindungs-ID zurück. Wenn der Aufruf erfolgreich ist, erhalten Sie das Peerereignis PEER \_ GROUP EVENT DIRECT CONNECTION \_ \_ \_ \_ EVENT, um anzugeben, dass die Verbindung erfolgreich war. Wenn die Verbindung erfolgreich hergestellt wurde, ist die Verbindungs-ID gültig und kann zum Senden und Empfangen von Daten über die direkte Verbindung verwendet werden.

Um direkte Verbindungen empfangen zu können, muss sich der andere Peer zuvor auch für das Peerereignis PEER GROUP EVENT DIRECT CONNECTION registriert \_ \_ \_ \_ haben.

Um Daten an einen Peer zu senden, rufen Sie [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) mit einer gültigen Verbindungs-ID auf. Um Daten zu empfangen, muss der andere Peer für das Peerereignis PEER GROUP EVENT INCOMING DATA registriert \_ \_ \_ \_ sein. Wenn der sendende Peer wiederum Daten empfangen möchte, muss er auch für das \_ PEER GROUP EVENT INCOMING \_ \_ \_ DATA-Peerereignis registriert werden.

Um den Gesamtsatz der derzeit aktiven direkten Verbindungen mit anderen Peers in einer Gruppe zu empfangen, rufen Sie [**PeerGroupEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections) auf, um die Enumeration zu öffnen und die Liste der Verbindungen mithilfe von [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem)zu durchlaufen.

Um eine direkte Verbindung zu schließen, rufen Sie [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) auf, und übergeben Sie die Verbindungs-ID.

## <a name="closing-and-shutting-down-a-peer-group"></a>Schließen und Herunterfahren einer Peergruppe

Um eine Verbindung mit einer Peergruppe zu schließen, rufen Sie [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose)auf, wodurch das Gruppenhandle ungültig wird, aber die Peergruppierungsinfrastruktur nicht heruntergefahren wird. Peer-zu-Peer-Gruppendaten werden durch Aufrufen von [**PeerGroupDelete**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)gelöscht.

Wenn die Anwendung die Peergruppierungsinfrastruktur verwendet, muss sie [**PeerGroupShutdown**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown)aufrufen.

 

 



