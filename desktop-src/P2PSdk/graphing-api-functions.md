---
description: 'Die Peer graphende-API verwendet die folgenden Funktionen:'
ms.assetid: cd05d4da-ca65-471b-bb97-82885f22e6f9
title: Graphende von API-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e343f3f5ff1e53180cced98cbebbd66af1d28e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865167"
---
# <a name="graphing-api-functions"></a>Graphende von API-Funktionen

Die Peer graphende-API verwendet die folgenden Funktionen:

## <a name="initialization-and-cleanup-functions"></a>Initialisierungs-und Bereinigungs Funktionen



| Funktion                                       | BESCHREIBUNG                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**Peer Diagramm Shutdown**](/windows/desktop/api/P2P/nf-p2p-peergraphshutdown) | Bereinigt alle Ressourcen, die durch den [**callergraphstartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup)-Befehl zugeordnet werden.                     |
| [**Peer graphstartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup)   | Gibt an, welche Version der Peer Protokolle die aufrufende Anwendung erfordert. |



 

## <a name="graph-creation-and-access-functions"></a>Graph-Erstellungs-und Zugriffs Funktionen



| Funktion                                   | BESCHREIBUNG                                                                                                                                                                                                           |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Peer graphclose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)   | Erklärt das Peer Diagramm Handle für ungültig, das durch einen Aufruf von [**peergraphcreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) oder [**peergraphopen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)zurückgegeben wurde, und schließt alle Netzwerkverbindungen für das angegebene Peer Diagramm. |
| [**Peer graphcreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) | Erstellt ein neues Peer Diagramm.                                                                                                                                                                                             |
| [**Peer graphdelete**](/windows/desktop/api/P2P/nf-p2p-peergraphdelete) | Löscht die einem angegebenen Peer Diagramm zugeordneten Daten.                                                                                                                                                              |
| [**Peer Diagramm lauschen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) | Gibt an, dass ein Peer Diagramm mit dem lauschen auf eingehende Verbindungen beginnen soll.                                                                                                                                          |
| [**Peer graphopen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)     | Öffnet ein Peer Diagramm, das zuvor durch den lokalen Knoten oder einen Remote Knoten erstellt wurde.                                                                                                                              |



 

## <a name="graph-and-node-information-functions"></a>Graph-und Knoten Informationsfunktionen



| Funktion                                                         | BESCHREIBUNG                                                                                                                                                        |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Peer graphenumnodes"**](/windows/desktop/api/P2P/nf-p2p-peergraphenumnodes)                 | Erstellt ein enumerationshandle, das zum Aufzählen der Knoten in einem Peer Diagramm verwendet wird, und gibt es zurück.                                                                             |
| [**Peer graphgetnodeinfo**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnodeinfo)             | Ruft Informationen zu einem bestimmten Knoten ab.                                                                                                                       |
| [**"Peer graphgetproperties"**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties)         | Ruft die aktuellen Peer Diagramm Eigenschaften ab.                                                                                                                       |
| [**Peergraphgetstatus**](/windows/desktop/api/P2P/nf-p2p-peergraphgetstatus)                 | Gibt den aktuellen Status des Peer Diagramms zurück.                                                                                                                      |
| [**"Peer graphsetnodebug"-Attribute**](/windows/desktop/api/P2P/nf-p2p-peergraphsetnodeattributes) | Legt die Attribute der [**Peer \_ Knoten \_ Info**](/windows/desktop/api/P2P/ns-p2p-peer_node_info) -Struktur für den lokalen Knoten fest.                                                                |
| [**Peer graphsetpresence**](/windows/desktop/api/P2P/nf-p2p-peergraphsetpresence)             | Dient zum expliziten ein-oder Ausschalten der Veröffentlichung von Anwesenheitsdaten Sätzen für einen bestimmten Knoten. Diese Funktion kann die Anwesenheits Einstellungen in den Peer Diagramm Eigenschaften überschreiben. |
| [**"Peer graphsetproperties"**](/windows/desktop/api/P2P/nf-p2p-peergraphsetproperties)         | Legt die Eigenschaften des Peer Diagramms fest.                                                                                                                                    |



 

## <a name="record-management-functions"></a>Daten Satz Verwaltungsfunktionen



| Funktion                                                                     | BESCHREIBUNG                                                                                                                         |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**Peer-graphaddrecord**](/windows/desktop/api/P2P/nf-p2p-peergraphaddrecord)                             | Fügt einem Peer Diagramm einen neuen Datensatz hinzu. Ein mit dieser Funktion hinzugefügter Datensatz wird an jeden Knoten in einem Peer Diagramm gesendet.                          |
| [**Peer graphdeleterecord**](/windows/desktop/api/P2P/nf-p2p-peergraphdeleterecord)                       | Markiert einen Datensatz als gelöscht innerhalb eines Peer Diagramms.                                                                                      |
| [**"Peer graphenumrecords"**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords)                         | Erstellt ein enumerationshandle und gibt es zurück, das zum Auflisten von Datensätzen eines bestimmten Typs von Datensatz, Benutzer oder beides verwendet wird.                    |
| [**"Peer graphgetrecord"**](/windows/desktop/api/P2P/nf-p2p-peergraphgetrecord)                             | Ruft einen bestimmten Datensatz auf der Grundlage der angegebenen Datensatz-ID ab.                                                                       |
| [**Peer Diagramm searchrecords**](/windows/desktop/api/P2P/nf-p2p-peergraphsearchrecords)                     | Durchsucht das Peer Diagramm nach bestimmten Datensätzen.                                                                                       |
| [**Peer graphupdaterecord**](/windows/desktop/api/P2P/nf-p2p-peergraphupdaterecord)                       | Aktualisiert einen Datensatz im Peer Diagramm und überflutet den Datensatz auf jeden Knoten im Peer Diagramm.                                       |
| [**Peer graphvalidatedeferredrecords**](/windows/desktop/api/P2P/nf-p2p-peergraphvalidatedeferredrecords) | Gibt an, dass die Peer-graphinginfrastruktur Zeit ist, alle verzögerten Datensätze erneut zu übermitteln, die vom Sicherheitsmodul überprüft werden sollen. |



 

## <a name="export-and-import-functions"></a>Export-und Import Funktionen



| Funktion                                                   | BESCHREIBUNG                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**Peer graphexportdatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase) | Exportiert eine Peer Graph-Datenbank in eine Datei, die Sie auf einen anderen Computer verschieben können. |
| [**Peer graphimportdatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase) | Importiert eine Datei, die die Informationen aus einer Peer Graph-Datenbank enthält.             |



 

## <a name="utility-and-support-functions"></a>Dienstprogramm-und Unterstützungsfunktionen



| Funktion                                                                     | BESCHREIBUNG                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**"Peer graphenumeration"**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration)                   | Gibt ein enumerationshandle frei und gibt die einer Enumeration zugeordneten Ressourcen frei.                                           |
| [**Peer graphfredata**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata)                               | Gibt Ressourcen frei, die von einigen der Peer graphende-API-Funktionen zurückgegeben werden.                                                           |
| [**Peer graphgetitemcount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount)                       | Ruft die Anzahl der Elemente in einer Enumeration ab.                                                                                  |
| [**Peer graphgetnextitem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem)                         | Ruft das nächste Element oder die Elemente in einer Enumeration ab, die durch einen-Rückruf für bestimmte Funktionen erstellt werden, die eine peerenumeration zurückgeben.        |
| [**"Peer Diagramm"-Zeitfenster**](/windows/desktop/api/P2P/nf-p2p-peergraphpeertimetouniversaltime) | Konvertiert den Wert des Peer Graph-beibegenten Verweises in einen lokalisierten Uhrzeitwert, der für die Anzeige auf dem Computer des Peers geeignet ist. |
| [**Peer graphuniversaltimetopeertime**](/windows/desktop/api/P2P/nf-p2p-peergraphuniversaltimetopeertime) | Konvertiert einen universellen Uhrzeitwert vom Computer des Peers in einen gemeinsamen Peer Graph-Zeitwert.                                       |



 

## <a name="connection-functions"></a>Verbindungsfunktionen



| Funktion                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Peer Diagramm closedirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) | Schließt eine angegebene direkte Verbindung.                                                                                                                                                                                                          |
| [**Peer graphconnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)                             | Versucht, eine Verbindung mit einem angegebenen Knoten in einem Peer Diagramm herzustellen. Diese Funktion startet einen asynchronen Vorgang.                                                                                                                             |
| [**Peergraphenumconnections**](/windows/desktop/api/P2P/nf-p2p-peergraphenumconnections)             | Erstellt ein enumerationshandle, das zum Auflisten der Verbindungen eines lokalen Knotens verwendet wird, und gibt es zurück.                                                                                                                                                   |
| [**Peer graphopendirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)   | Ermöglicht es einer Anwendung, eine direkte Verbindung mit einem Knoten in einem Peer Diagramm herzustellen. Die Verbindung kann nur hergestellt werden, wenn der Knoten, mit dem die Anwendung eine Verbindung herstellt, das **Peer \_ Graph \_ Event \_ Direct \_ Connection** -Ereignis abonniert hat. |
| [**Peer Diagramm Daten**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata)                           | Sendet Daten an einen Nachbar Knoten oder einen direkt verbundenen Knoten.                                                                                                                                                                                    |



 

## <a name="events-infrastructure-functions"></a>Ereignisse Infrastrukturfunktionen



| Funktion                                                     | BESCHREIBUNG                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Peer graphgeteventdata**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)       | Ruft Peer Ereignisse ab.                                                                                       |
| [**Peer Diagramm Register Event**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)     | Registriert die Anforderung eines Peers, um über Änderungen benachrichtigt zu werden, die einem Peer Diagramm und einem Ereignistyp zugeordnet sind.            |
| [**"Peer Diagramm"**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent) | Fordert an, dass die Anwendung nicht mehr über Änderungen benachrichtigt wird, die einem Peer Graph und einem Daten Satz Typen zugeordnet sind. |



 

 

 



