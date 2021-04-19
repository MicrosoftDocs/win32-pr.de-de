---
description: In diesem Thema wird erläutert, wie eine Anwendung mithilfe der Peer Gruppierungs-APIs eine Verbindung mit einer Peer Gruppe herstellt.
ms.assetid: 56fa28d8-3b3a-4cd5-8448-c8c4ce8d0b2c
title: Vorgehensweise beim Herstellen einer Verbindung mit einer Peer Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bb3f41342573742e634a6e7ebce283188f3ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358903"
---
# <a name="how-to-connect-to-a-peer-group"></a>Vorgehensweise beim Herstellen einer Verbindung mit einer Peer Gruppe

In diesem Thema wird erläutert, wie eine Anwendung mithilfe der Peer Gruppierungs-APIs eine Verbindung mit einer Peer Gruppe herstellt.

## <a name="joining-a-peer-group"></a>Beitreten zu einer Peer Gruppe

Wenn Sie einer Peer Gruppe beitreten möchten, nennen Sie [**peergroupjoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), und übergeben Sie dabei den Identitäts Namen des Peers und die Einladung (und einen optionalen PNRP-cloudnamen, wenn der cloudName in der Einladung mehrdeutig ist).

Wenn der Vorgang erfolgreich ist, gibt [**peergroupjoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) ein Handle für die Peer Gruppe zurück.

Wenn der Peer zuvor der Peer Gruppe beigetreten ist und dann das Handle geschlossen hat, sollte die Peer Gruppe durch Aufrufen von [**peergroupopen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) und übergeben des Namens der Peer Gruppe erneut geöffnet werden. Dieser Rückruf gibt ein neues Peer Gruppen Handle zurück.

Nachdem die Peer Gruppe erfolgreich verknüpft wurde, kann der Peer eine direkte Verbindung mit der Peer Gruppe herstellen und mit der Interaktion beginnen, indem [**peergroupconnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)aufgerufen wird. Nachdem die Verbindung hergestellt wurde, wird der Peer als "Online" betrachtet.

Wenn eine Anwendung zu diesem Zeitpunkt nicht mit der Gruppe interagiert, kann Sie "Offline" bleiben. Wenn die Teilnahme an einer späteren Instanz direkt an der Peer Gruppe teilnimmt, wird Sie durch einen nachfolgenden [**peergroupconnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) -Befehl online geschaltet. Nachdem ein Peer der Peer Gruppe beigetreten ist, muss er mindestens einmal eine Verbindung herstellen, bevor er Datensätze in der Peer Gruppe veröffentlichen kann.

## <a name="opening-a-peer-group-without-connecting-offline"></a>Öffnen einer Peer Gruppe ohne Verbindung (offline)

Häufig möchten Sie, dass eine Anwendung eine Verbindung mit einer Peer Gruppe herstellt, Sie jedoch nicht direkt daran beteiligt, Daten Satz Aktualisierungen empfängt und veröffentlicht, aber keine Daten Nachrichten sendet oder empfängt. Eine Anwendung befindet sich unmittelbar nach dem Aufrufen von " [**Peer groupcreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)", " [**Peer GroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)" oder " [**Peer groupopen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) " in diesem Status "Offline".

Eine Offline Anwendung kann jederzeit online geschaltet werden, indem " [**Peer groupconnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)" aufgerufen wird. Nachdem die Verbindung hergestellt wurde, kann eine Peer Gruppe erst offline geschaltet werden, wenn alle anderen Anwendungen, die dieser Identität zugeordnet sind und die diese Gruppe freigeben, ebenfalls über geschlossene Verbindungen verfügen.

Eine Peer Gruppe ist eine freigegebene Ressource mit der gleichen Peer Gruppe, die für mehrere Anwendungen verfügbar ist. Wenn mehr als eine Anwendung für die gleiche Identität und den Windows-Benutzer dieselbe Peer Gruppe verwendet, nutzen Sie auch die gleiche zugrunde liegende Datenbank und die gleichen Verbindungen (Nachbar und direkt). Wenn eine dieser Anwendungen [**peergroupconnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)aufruft, stellen alle anderen Anwendungen für diese Identität bzw. diesen Benutzer, die an der Gruppe teilnehmen, auch eine Verbindung mit der Gruppe her. Wenn ein Datensatz von einer Anwendung hinzugefügt wird, während die Gruppe offline ist, können andere Anwendungen Sie sehen. Daher muss eine Anwendung jederzeit online geschaltet werden können.

## <a name="connecting-to-a-peer-group-online"></a>Herstellen einer Verbindung mit einer Peer Gruppe (Online)

Um mit der Teilnahme an einer Gruppe zu beginnen, können Sie [**peergroupconnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) aufrufen, nachdem Sie die Gruppe erstellt, beitreten oder geöffnet haben. In diesem Zustand können direkte Verbindungen mit anderen Peers geöffnet werden, die an derselben Gruppe teilnehmen, indem [**peergroupopendirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)aufgerufen wird.

Um zu ermitteln, ob bei einem Verbindungsversuch ein Fehler aufgetreten ist, registrieren Sie sich für das Ereignis Verbindungsfehler bei der Peer \_ Gruppe \_ \_ \_ . Dieses Ereignis wird ausgelöst, wenn die Gruppierungs Infrastruktur keinen anderen Member finden kann, mit dem eine Verbindung hergestellt werden kann, oder wenn die Verbindung fehlschlägt, bevor die Gruppen Datenbank synchronisiert wird und keine andere Verbindung hergestellt werden kann.

Obwohl mehrere Anwendungen, die auf dem Peer ausgeführt werden und an derselben Gruppe mit der gleichen Peer Identität beteiligt sind, möglicherweise offline sind, führt ein Aufrufen von [**peergroupconnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) durch eine der Anwendungen dazu, dass alle Anwendungen online werden.

Wenn eine Anwendung auf dem Peer eine Verbindung mit der Gruppe hergestellt hat, sind auch alle anderen Anwendungen, die [**peergroupjoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) oder [**peergroupopen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) aufrufen, sofort verbunden. Wenn eine Anwendung " [**Peer groupclose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose)" aufruft, wird das Handle nur für diese Anwendung geschlossen. Folglich gibt ein nachfolgende Aufrufen von **peergroupopen** durch die Anwendung ein neues Gruppen Handle zurück, und die Anwendung wird sofort online geschaltet, wenn andere Anwendungen, die an derselben Gruppe teilnehmen, weiterhin verbunden sind.

## <a name="sending-and-receiving-data"></a>Senden und empfangen von Daten

Zum Senden und empfangen von Daten zwischen bestimmten Mitglieds Knoten in der Gruppe müssen Direktverbindungen mit den Mitgliedern hergestellt werden, mit denen Sie interagieren möchten. Das Einrichten einer direkten Verbindung ist ein asynchroner [**peergroupopendirectconnection-Peering**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)und übergibt das Handle für eine verbundene Gruppe sowie die Identität des Peers innerhalb der Gruppe, mit der Sie eine Verbindung herstellen möchten. Diese Methode gibt eine Verbindungs-ID zurück. Wenn der-Vorgang erfolgreich ist, \_ \_ wird auf dem Peer ein Ereignis für eine Peer Gruppen Ereignis- \_ direkte \_ Verbindung ausgelöst, wobei die Verbindungs-ID überprüft wird.

Um direkte Verbindungen von anderen Online Peers zu empfangen, registrieren Sie sich \_ \_ \_ \_ mit einem [**peergroupregisterevent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)-Ereignis für das Peer Group Event Direct Connection-Ereignis.

Sobald eine direkte Verbindung hergestellt wurde, kann die Anwendung mit dem Senden von Daten mit Aufrufen von " [**Peer Group Data**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)" beginnen und dabei die gültige Verbindungs-ID übergeben. Die Reihenfolge von mehrteiligen Datenübertragungen wird von " **Peer Group**" verarbeitet. Anwendungen sollten jedoch einen ordnungsgemäßen Protokollstapel implementieren, um die nicht transparenten Daten zu verarbeiten, die von diesem API-Befehl zurückgegeben werden.

Um Daten über eine direkte Verbindung zu empfangen, muss sich die Anwendung \_ \_ \_ \_ mit [**peergroupregisterevent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)für das Ereignis eingehende Daten der Peer Gruppe registrieren. Der Ereignishandler ist für das Abrufen und Anordnen der nicht transparenten Daten und die Übergabe an die Anwendung zuständig. Diese Daten werden innerhalb des Ereignis Handlers abgerufen, indem " [**Peer groupgeteventdata**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) " mit dem Handle für die registrierten Ereignisse aufgerufen wird.

Eine direkte Verbindung wird geschlossen, indem [**peergroupclosedirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) aufgerufen und die Verbindungs-ID übergeben wird, die durch einen vorherigen Aufruf von [**peergroupopendirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) abgerufen oder in den Ereignisdaten für die \_ \_ \_ direkte Verbindung mit der Peer-Ereignis Gruppe empfangen wurde \_ .

 

 



