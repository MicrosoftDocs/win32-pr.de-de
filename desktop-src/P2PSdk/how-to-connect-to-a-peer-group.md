---
description: In diesem Thema wird erläutert, wie eine Anwendung mithilfe der Peer grouping-APIs eine Verbindung mit einer Peergruppe herstellt.
ms.assetid: 56fa28d8-3b3a-4cd5-8448-c8c4ce8d0b2c
title: How to Verbinden to a Peer Group
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb1cfd08fde0fc733873648dfae1ffb4f86b713b3ed790430686b641a893d23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612766"
---
# <a name="how-to-connect-to-a-peer-group"></a>How to Verbinden to a Peer Group

In diesem Thema wird erläutert, wie eine Anwendung mithilfe der Peer grouping-APIs eine Verbindung mit einer Peergruppe herstellt.

## <a name="joining-a-peer-group"></a>Beitreten zu einer Peergruppe

Rufen Sie zum Beitreten zu einer Peergruppe [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)auf, und übergeben Sie dabei den Identitätsnamen des Peers und die Einladung (und einen optionalen PNRP-Cloudnamen, wenn der Cloudname in der Einladung mehrdeutig ist).

Bei Erfolg gibt [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) ein Handle an die Peergruppe zurück.

Wenn der Peer zuvor der Peergruppe beigetreten ist und dann das Handle geschlossen hat, sollte die Peergruppe erneut geöffnet werden, indem [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) aufruft und der Name der Peergruppe übergeben wird. Dieser Aufruf gibt ein neues Peergruppenhand handle zurück.

Nachdem die Peergruppe erfolgreich beigetreten ist, kann der Peer eine direkte Verbindung mit der Peergruppe herstellen und mit der Interaktion beginnen, indem [**PeerGroupConnect aufruft.**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) Nach dem Herstellen der Verbindung gilt der Peer als "online".

Wenn eine Anwendung zu diesem Zeitpunkt nicht mit der Gruppe interagiert, kann sie "offline" bleiben. Wenn sie sich für eine direkte Teilnahme an der Peergruppe in einer späteren Instanz entscheidet, wird sie durch einen nachfolgenden Aufruf von [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) online wiederherstellen. Nachdem ein Peer der Peergruppe beigetreten ist, muss er mindestens einmal eine Verbindung herstellen, bevor er Datensätze in der Peergruppe veröffentlichen kann.

## <a name="opening-a-peer-group-without-connecting-offline"></a>Öffnen einer Peergruppe ohne Verbindung (offline)

Häufig möchten Sie eine Anwendung eine Verbindung mit einer Peergruppe herstellen, aber nicht direkt daran teilnehmen, d. b. Aktualisierungen von Datensatzdaten empfangen und veröffentlichen, aber keine Datennachrichten senden oder empfangen. Eine Anwendung befindet sich unmittelbar nach dem Aufgerufenen [**von PeerGroupCreate,**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)oder [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) in diesem Offlinezustand.

Eine Offlineanwendung kann jederzeit durch Aufrufen von [**PeerGroupConnect online geschaltet werden.**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) Sobald die Verbindung besteht, kann eine Peergruppe erst offline geschaltet werden, wenn alle anderen Anwendungen, die dieser Identität zugeordnet sind und diese Gruppe freigeben, auch über geschlossene Verbindungen verfügen.

Eine Peergruppe ist eine freigegebene Ressource, bei der dieselbe Peergruppe für mehrere Anwendungen verfügbar ist. Wenn mehr als eine Anwendung für dieselbe Identität und Windows benutzer dieselbe Peergruppe verwendet, verwenden sie auch die gleiche zugrunde liegende Datenbank und die gleichen Verbindungen (Nachbar und direkt). Wenn eine dieser Anwendungen [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)aufruft, stellen alle anderen Anwendungen für diese Identität/diesen Benutzer, die an der Gruppe teilnehmen, ebenfalls eine Verbindung mit der Gruppe her. Wenn ein Datensatz von einer Anwendung hinzugefügt wird, während die Gruppe offline ist, können andere Anwendungen ihn auch sehen. Daher muss eine Anwendung jederzeit online gehen können.

## <a name="connecting-to-a-peer-group-online"></a>Herstellen einer Verbindung mit einer Peergruppe (Online)

Um mit der Teilnahme an einer Gruppe zu beginnen, rufen Sie [**PeerGroupConnect auf,**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) nachdem Sie die Gruppe erstellt, beitreten oder geöffnet haben. In diesem Zustand können direkte Verbindungen mit anderen Peers geöffnet werden, die an derselben Gruppe teilnehmen, indem [**PeerGroupOpenDirectConnection aufruft.**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)

Um zu ermitteln, ob ein Verbindungsversuch fehlgeschlagen ist, registrieren Sie sich für das PEER \_ GROUP \_ EVENT CONNECTION \_ \_ FAILED-Ereignis. Dieses Ereignis wird ausgelöst, wenn die Gruppierungsinfrastruktur kein anderes Mitglied finden kann, mit dem eine Verbindung hergestellt werden kann, oder wenn die Verbindung fehlschlägt, bevor die Gruppendatenbank synchronisiert wird und keine weitere Verbindung hergestellt werden kann.

Obwohl mehrere Anwendungen, die auf dem Peer ausgeführt werden und an derselben Gruppe mit derselben Peeridentität teilnehmen, offline sein können, führt ein Aufruf von [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) durch eine der Anwendungen dazu, dass alle Anwendungen online geschaltet werden.

Wenn eine Anwendung auf dem Peer mit der Gruppe verbunden ist, werden auch alle anderen Anwendungen, die [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) oder [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) aufrufen, sofort verbunden. Wenn eine Anwendung [**PeerGroupClose aufruft,**](/windows/desktop/api/P2P/nf-p2p-peergroupclose)wird das Handle nur für diese Anwendung geschlossen. Daher gibt ein nachfolgender Aufruf von **PeerGroupOpen** durch die Anwendung ein neues Gruppenhand handle zurück, und die Anwendung wird sofort online gestellt, wenn andere Anwendungen, die zur gleichen Gruppe gehören, weiterhin verbunden sind.

## <a name="sending-and-receiving-data"></a>Senden und Empfangen von Daten

Um Daten zwischen bestimmten Mitgliedsknoten in der Gruppe zu senden und zu empfangen, müssen direkte Verbindungen mit den Mitgliedern hergestellt werden, mit denen Sie interagieren möchten. Das Herstellen einer direkten Verbindung ist ein asynchroner Aufruf von [**PeerGroupOpenDirectConnection,**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)bei dem das Handle für eine verbundene Gruppe sowie die Identität des Peers innerhalb der Gruppe übergeben wird, mit der Sie eine Verbindung herstellen möchten. Diese Methode gibt eine Verbindungs-ID zurück. Wenn der Aufruf erfolgreich ist, wird ein PEER GROUP EVENT DIRECT CONNECTION-Ereignis auf dem Peer ausgelöst, um \_ \_ die \_ \_ Verbindungs-ID zu überprüfen.

Um direkte Verbindungen von anderen Online-Peers zu empfangen, registrieren Sie sich für das PEER GROUP EVENT DIRECT CONNECTION-Ereignis mit einem Aufruf \_ \_ von \_ \_ [**PeerGroupRegisterEvent.**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)

Nachdem eine direkte Verbindung erfolgreich hergestellt wurde, kann die Anwendung mit dem Senden von Daten mit Aufrufen von [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)beginnen und die gültige Verbindungs-ID übergeben. Die Reihenfolge der mehrteiligen Datenübertragungen wird von **PeerGroupSendData verarbeitet.** Anwendungen sollten jedoch einen geeigneten Protokollstapel für die Verarbeitung der nicht transparenten Daten implementieren, die von diesem API-Aufruf zurückgegeben werden.

Um Daten über eine direkte Verbindung zu empfangen, muss sich die Anwendung bei PeerGroupRegisterEvent für das PEER \_ GROUP \_ EVENT INCOMING \_ \_ [**DATA-Ereignis registrieren.**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) Der Ereignishandler ist dafür verantwortlich, die nicht transparenten Daten zu erhalten und zu ordnen und an die Anwendung zu übergeben. Diese Daten werden innerhalb des Ereignishandlers durch Aufrufen von [**PeerGroupGetEventData mit**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) dem Handle für die registrierten Ereignisse erhalten.

Eine direkte Verbindung wird durch Aufrufen von [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) und Übergeben der Verbindungs-ID geschlossen, die durch einen vorherigen Aufruf von [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) ermittelt oder in den Ereignisdaten für PEER EVENT GROUP DIRECT CONNECTION empfangen \_ \_ \_ \_ wurde.

 

 



