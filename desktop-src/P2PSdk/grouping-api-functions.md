---
description: 'Die Gruppierungs-API verwendet die folgenden Funktionen:'
ms.assetid: 56ea2880-b468-4816-b6c9-5780c807b3f1
title: Gruppieren von API-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d2970ca68d69b16a32cf7a6d546a5852b07dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350232"
---
# <a name="grouping-api-functions"></a>Gruppieren von API-Funktionen

Die Gruppierungs-API verwendet die folgenden Funktionen:

## <a name="group-initialization-and-cleanup-functions"></a>Initialisierungs-und Bereinigungs Funktionen für Gruppen



| Funktion                                       | BESCHREIBUNG                                                                                                            |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**"Peer groupshutdown"**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown) | Schließt eine Peer Gruppe, die mit [**peergroupstartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) erstellt wurde, und gibt alle zugeordneten Ressourcen frei. |
| [**Peer groupstartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup)   | Initiiert eine Peer Gruppe mithilfe einer angeforderten Version der Peer Infrastruktur.                                        |



 

## <a name="group-creation-and-access-functions"></a>Gruppen Erstellungs-und Zugriffs Funktionen



| Funktion                                                                       | BESCHREIBUNG                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Peer groupclose"**](/windows/desktop/api/P2P/nf-p2p-peergroupclose)                                       | Erklärt das Peer Gruppen Handle für ungültig, das durch einen vorherigen Aufrufen der [**peergroupcreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)-, [**peergroupjoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)-oder [**peergroupopen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) -Funktion abgerufen wurde. |
| [**Peer groupconnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)                                   | Initiiert eine PNRP-Suche für eine Peer Gruppe und versucht, eine Verbindung damit herzustellen. Nachdem diese Funktion erfolgreich aufgerufen wurde, kann ein Peer mit anderen Mitgliedern der Peer Gruppe kommunizieren.                             |
| [**"Peer groupconnectbyaddress"**](/windows/desktop/api/P2P/nf-p2p-peergroupconnectbyaddress)                 | Versucht, eine Verbindung mit der Peer Gruppe herzustellen, an der andere Peers mit bekannten IPv6-Adressen teilnehmen.                                                                                                       |
| [**Peer groupcreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)                                     | Erstellt eine neue Peer Gruppe.                                                                                                                                                                                    |
| [**"Peer groupkreateinvitation"**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)                 | Gibt eine XML-Zeichenfolge zurück, die vom angegebenen Peer zum beitreten zu einer Gruppe verwendet werden kann.                                                                                                                                |
| [**Peer groupkreatepasswordinvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreatepasswordinvitation) | Gibt eine XML-Zeichenfolge zurück, die vom angegebenen Peer verwendet werden kann, um eine Gruppe mit einem übereinstimmenden Kennwort zu verknüpfen.                                                                                                       |
| [**"Peer groupdelete"**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)                                     | Löscht die lokalen Daten und das Zertifikat, die einer Peer Gruppe zugeordnet sind.                                                                                                                                         |
| [**Peergroupgetstatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus)                               | Ruft den aktuellen Status einer Gruppe ab.                                                                                                                                                                     |
| [**Peer groupissuecredenseins**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)                 | Gibt Anmelde Informationen, einschließlich einer GMC, für eine bestimmte Identität aus und gibt optional eine Einladungs-XML-Zeichenfolge zurück, mit der der eingeladene Peer einer Peer Gruppe beitreten kann.                                                  |
| [**Peer GroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)                                         | Ermöglicht einem Peer mit einer Einladung, einer vorhandenen Peer Gruppe beizutreten.                                                                                                                                             |
| [**Peer groupopen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)                                         | Öffnet eine Peer Gruppe, die ein Peer erstellt oder verknüpft hat.                                                                                                                                                        |
| [**"Peer groupparamevitation"**](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)                   | Gibt eine [**Peer \_ Einladungs \_ Informations**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) Struktur mit den Details einer bestimmten Einladung zurück.                                                                                        |
| [**Peer-grouppasswordjoin**](/windows/desktop/api/P2P/nf-p2p-peergrouppasswordjoin)                         | Ermöglicht einem Peer mit einer Einladung und dem richtigen Kennwort, um einer Kenn Wort geschützten Peer Gruppe beizutreten.                                                                                                           |



 

## <a name="group-and-member-information-functions"></a>Gruppen-und Element Informationsfunktionen



| Funktion                                                 | BESCHREIBUNG                                                                                                                        |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**"Peer groupenummembers"**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)     | Erstellt eine Enumeration der verfügbaren Peer Gruppenmitglieder und der zugehörigen Mitgliedschafts Informationen.                                  |
| [**"Peer groupgetproperties"**](/windows/desktop/api/P2P/nf-p2p-peergroupgetproperties) | Ruft Informationen zu den Eigenschaften einer angegebenen Gruppe ab.                                                                      |
| [**"Peer groupsetproperties"**](/windows/desktop/api/P2P/nf-p2p-peergroupsetproperties) | Legt die aktuellen Peer Gruppen Eigenschaften fest. In Version 1,0 dieser API kann dieser Vorgang nur vom Ersteller der Peer Gruppe durchgeführt werden. |



 

## <a name="records-and-record-management-functions"></a>Datensätze und Daten Satz Verwaltungsfunktionen



| Funktion                                                 | BESCHREIBUNG                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**"Peer groupaddrecord"**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)         | Fügt der Peer Gruppe einen neuen Datensatz hinzu, der an alle teilnehmenden Peers weitergegeben wird. |
| [**Peer groupdeleterecord**](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)   | Löscht einen Datensatz aus einer Peer Gruppe. Nur der Ersteller eines Datensatzes kann ihn löschen.      |
| [**Peer groupumschlag**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)     | Erstellt eine Enumeration von Peer Gruppen-Datensätzen.                                        |
| [**"Peer groupgetrecord"**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord)         | Ruft einen bestimmten Gruppendaten Satz ab.                                                   |
| [**"Peer groupsearchrecords"**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) | Durchsucht die lokale Peer Gruppen Datenbank nach Datensätzen, die den angegebenen Kriterien entsprechen. |
| [**Peer-groupupdaterecord**](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)   | Aktualisiert einen Datensatz innerhalb einer bestimmten Peer Gruppe.                                       |



 

## <a name="group-database-importexport-functions"></a>Importieren/Exportieren von Datenbankfunktionen



| Funktion                                                   | BESCHREIBUNG                                                                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Peer groupexportdatabase"**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase) | Exportiert eine Peer Gruppen Datenbank in eine bestimmte Datei, die auf einen anderen Computer übertragen und mit der [**peergroupimportdatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) -Funktion importiert werden kann. |
| [**"Peer groupimportdatabase"**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) | Importiert eine Peer Gruppen Datenbank aus einer lokalen Datei.                                                                                                                                          |



 

## <a name="direct-connection-functions"></a>Direkte Verbindungsfunktionen



| Funktion                                                                 | BESCHREIBUNG                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**"Peer groupclosedirectconnection"**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) | Schließt eine bestimmte direkte Verbindung zwischen zwei Peers.              |
| [**Peergroupumschlag-Verbindungen**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections)             | Erstellt eine Enumeration der derzeit auf dem Peer aktiven Verbindungen. |
| [**"Peer groupopendirectconnection"**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)   | Stellt eine direkte Verbindung mit einem anderen Peer in einer Peer Gruppe her.  |
| [**"Peer Group"-Daten**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)                           | Sendet Daten über eine Nachbar-oder direkte Verbindung an einen Member.        |



 

## <a name="group-events-infrastructure"></a>Infrastruktur für Gruppen Ereignisse



| Funktion                                                     | BESCHREIBUNG                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**"Peer groupgeteventdata"**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)       | Ermöglicht einer Anwendung das Abrufen der Daten, die von einem Gruppierungs Ereignis zurückgegeben werden.                       |
| [**"Peer-groupregisterevent"**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)     | Registriert einen Peer für bestimmte Peer Gruppen Ereignisse.                                               |
| [**"Peer Register Event"**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) | Hebt die Registrierung eines Peers von der Benachrichtigung über Peer Ereignisse auf, die dem angegebenen Ereignis Handle zugeordnet sind. |



 

## <a name="group-time-conversion-functions"></a>Gruppen Zeit Konvertierungs Funktionen



| Funktion                                                                     | BESCHREIBUNG                                                                                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**"Peer grouppeer Timeto universaltime"**](/windows/desktop/api/P2P/nf-p2p-peergrouppeertimetouniversaltime) | Konvertiert den von der Peer Gruppe verwalteten Verweis Zeitwert in einen lokalisierten Uhrzeitwert, der für die Anzeige auf einem Peer Computer geeignet ist. |
| [**"Peer groupuniversaltimetopeertime"**](/windows/desktop/api/P2P/nf-p2p-peergroupuniversaltimetopeertime) | Konvertiert einen lokalen Uhrzeitwert vom Computer eines Peers in einen gemeinsamen Peer Gruppen-Uhrzeitwert.                                         |



 

## <a name="group-configuration-functions"></a>Gruppen Konfigurationsfunktionen



| Funktion                                               | BESCHREIBUNG                                                                                                                       |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**"Peer groupexportconfig"**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig) | Exportiert die Gruppenkonfiguration für einen Peer als XML-Zeichenfolge, die die Identität, den Gruppennamen und die GMC für die Identität enthält. |
| [**"Peer groupimportconfig"**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) | Importiert eine Peer Gruppenkonfiguration für eine Identität basierend auf den spezifischen Einstellungen in einer angegebenen XML-Konfigurations Zeichenfolge.         |



 

 

 



