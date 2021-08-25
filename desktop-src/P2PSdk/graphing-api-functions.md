---
description: 'Die Peergraphing-API verwendet die folgenden Funktionen:'
ms.assetid: cd05d4da-ca65-471b-bb97-82885f22e6f9
title: Graphing-API-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26c40770e8fcbc18b08ccb73dcfea5f1f6c4eab65be615ed76d8088ddc90954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776220"
---
# <a name="graphing-api-functions"></a>Graphing-API-Funktionen

Die Peergraphing-API verwendet die folgenden Funktionen:

## <a name="initialization-and-cleanup-functions"></a>Initialisierungs- und Bereinigungsfunktionen



| Funktion                                       | Beschreibung                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphShutdown**](/windows/desktop/api/P2P/nf-p2p-peergraphshutdown) | Bereinigt alle Ressourcen, die durch den Aufruf von [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup)zugeordnet werden.                     |
| [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup)   | Gibt der Peerdiagramminfrastruktur an, welche Version der Peerprotokolle für die aufrufende Anwendung erforderlich ist. |



 

## <a name="graph-creation-and-access-functions"></a>Graph Erstellungs- und Zugriffsfunktionen



| Funktion                                   | Beschreibung                                                                                                                                                                                                           |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)   | Macht das Peerdiagrammhandle ungültig, das durch einen Aufruf von [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) oder [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)zurückgegeben wird, und schließt alle Netzwerkverbindungen für das angegebene Peerdiagramm. |
| [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) | Erstellt ein neues Peerdiagramm.                                                                                                                                                                                             |
| [**PeerGraphDelete**](/windows/desktop/api/P2P/nf-p2p-peergraphdelete) | Löscht die einem angegebenen Peerdiagramm zugeordneten Daten.                                                                                                                                                              |
| [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) | Gibt an, dass ein Peerdiagramm auf eingehende Verbindungen lauschen soll.                                                                                                                                          |
| [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)     | Öffnet ein Peerdiagramm, das zuvor entweder vom lokalen Knoten oder einem Remoteknoten erstellt wurde.                                                                                                                              |



 

## <a name="graph-and-node-information-functions"></a>Graph- und Knoteninformationsfunktionen



| Funktion                                                         | Beschreibung                                                                                                                                                        |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphEnumNodes**](/windows/desktop/api/P2P/nf-p2p-peergraphenumnodes)                 | Erstellt ein Enumerationshandle, das zum Aufzählen der Knoten in einem Peerdiagramm verwendet wird, und gibt dieses zurück.                                                                             |
| [**PeerGraphGetNodeInfo**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnodeinfo)             | Ruft Informationen zu einem bestimmten Knoten ab.                                                                                                                       |
| [**PeerGraphGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties)         | Ruft die aktuellen Peerdiagrammeigenschaften ab.                                                                                                                       |
| [**PeerGraphGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergraphgetstatus)                 | Gibt den aktuellen Status des Peerdiagramms zurück.                                                                                                                      |
| [**PeerGraphSetNodeAttributes**](/windows/desktop/api/P2P/nf-p2p-peergraphsetnodeattributes) | Legt die Attribute der [**PEER \_ NODE \_ INFO-Struktur**](/windows/desktop/api/P2P/ns-p2p-peer_node_info) für den lokalen Knoten fest.                                                                |
| [**PeerGraphSetPresence**](/windows/desktop/api/P2P/nf-p2p-peergraphsetpresence)             | Aktiviert oder deaktiviert explizit die Veröffentlichung von Anwesenheitsdatensätzen für einen bestimmten Knoten. Diese Funktion kann die Anwesenheitseinstellungen in den Peerdiagrammeigenschaften überschreiben. |
| [**PeerGraphSetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphsetproperties)         | Legt die Peerdiagrammeigenschaften fest.                                                                                                                                    |



 

## <a name="record-management-functions"></a>Funktionen für die Datensatzverwaltung



| Funktion                                                                     | Beschreibung                                                                                                                         |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphaddrecord)                             | Fügt einem Peerdiagramm einen neuen Datensatz hinzu. Ein mit dieser Funktion hinzugefügter Datensatz wird an jeden Knoten in einem Peerdiagramm gesendet.                          |
| [**PeerGraphDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphdeleterecord)                       | Markiert einen Datensatz in einem Peerdiagramm als gelöscht.                                                                                      |
| [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords)                         | Erstellt ein Enumerationshandle, das zum Auflisten von Datensätzen eines bestimmten Datensatztyps, Benutzers oder beider Typen verwendet wird, und gibt dieses zurück.                    |
| [**PeerGraphGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphgetrecord)                             | Ruft einen bestimmten Datensatz basierend auf der angegebenen Datensatz-ID ab.                                                                       |
| [**PeerGraphSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphsearchrecords)                     | Durchsucht das Peerdiagramm nach bestimmten Datensätzen.                                                                                       |
| [**PeerGraphUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphupdaterecord)                       | Aktualisiert einen Datensatz im Peerdiagramm und überflutet den Datensatz dann an jeden Knoten im Peerdiagramm.                                       |
| [**PeerGraphValidateDeferredRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphvalidatedeferredrecords) | Gibt der Peerdiagramminfrastruktur an, dass es an der Zeit ist, alle zurückgestellten Datensätze erneut zu übermitteln, die das Sicherheitsmodul überprüfen soll. |



 

## <a name="export-and-import-functions"></a>Export- und Importfunktionen



| Funktion                                                   | Beschreibung                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**PeerGraphExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase) | Exportiert eine Peergraphdatenbank in eine Datei, die Sie auf einen anderen Computer verschieben können. |
| [**PeerGraphImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase) | Importiert eine Datei, die die Informationen aus einer Peerdiagrammdatenbank enthält.             |



 

## <a name="utility-and-support-functions"></a>Hilfsprogramm- und Supportfunktionen



| Funktion                                                                     | Beschreibung                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration)                   | Gibt ein Enumerationshandle frei und gibt die einer Enumeration zugeordneten Ressourcen frei.                                           |
| [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata)                               | Gibt Ressourcen frei, die von mehreren Peer Graphing-API-Funktionen zurückgegeben werden.                                                           |
| [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount)                       | Ruft die Anzahl der Elemente in einer Enumeration ab.                                                                                  |
| [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem)                         | Ruft das nächste Element oder die nächsten Elemente in einer Enumeration ab, die durch einen Aufruf bestimmter Funktionen erstellt wurden, die eine Peerenumeration zurückgeben.        |
| [**PeerGraphPeerTimeToUniversalTime**](/windows/desktop/api/P2P/nf-p2p-peergraphpeertimetouniversaltime) | Konvertiert den vom Peerdiagramm verwalteten Verweiszeitwert in einen lokalisierten Zeitwert, der für die Anzeige auf dem Computer des Peers geeignet ist. |
| [**PeerGraphUniversalTimeToPeerTime**](/windows/desktop/api/P2P/nf-p2p-peergraphuniversaltimetopeertime) | Konvertiert einen universellen Zeitwert vom Computer des Peers in einen allgemeinen Peerdiagrammzeitwert.                                       |



 

## <a name="connection-functions"></a>Verbindungsfunktionen



| Funktion                                                                 | Beschreibung                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) | Schließt eine angegebene direkte Verbindung.                                                                                                                                                                                                          |
| [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)                             | Versucht, eine Verbindung mit einem angegebenen Knoten in einem Peerdiagramm herzustellen. Diese Funktion startet einen asynchronen Vorgang.                                                                                                                             |
| [**PeerGraphEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergraphenumconnections)             | Erstellt ein Enumerationshandle, das zum Aufzählen der Verbindungen eines lokalen Knotens verwendet wird, und gibt dieses zurück.                                                                                                                                                   |
| [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)   | Ermöglicht es einer Anwendung, eine direkte Verbindung mit einem Knoten in einem Peerdiagramm herzustellen. Die Verbindung kann nur hergestellt werden, wenn der Knoten, mit dem die Anwendung eine Verbindung herstellt, das **PEER GRAPH EVENT DIRECT \_ \_ \_ \_ CONNECTION-Ereignis** abonniert hat. |
| [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata)                           | Sendet Daten an einen benachbarten Knoten oder einen direkt verbundenen Knoten.                                                                                                                                                                                    |



 

## <a name="events-infrastructure-functions"></a>Ereignisinfrastrukturfunktionen



| Funktion                                                     | Beschreibung                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)       | Ruft Peerereignisse ab.                                                                                       |
| [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)     | Registriert die Anforderung eines Peers, über Änderungen benachrichtigt zu werden, die einem Peerdiagramm und einem Ereignistyp zugeordnet sind.            |
| [**PeerGraphUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent) | Fordert an, dass die Anwendung nicht mehr über Änderungen benachrichtigt wird, die einem Peerdiagramm und Datensatztyp zugeordnet sind. |



 

 

 



