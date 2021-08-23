---
description: 'Die Gruppierungs-API verwendet die folgenden Funktionen:'
ms.assetid: 56ea2880-b468-4816-b6c9-5780c807b3f1
title: Gruppieren von API-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 888a64096f66a9adf048d91c2d577d71203a03da6d1b698f2ea305396c4be0db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776170"
---
# <a name="grouping-api-functions"></a>Gruppieren von API-Funktionen

Die Gruppierungs-API verwendet die folgenden Funktionen:

## <a name="group-initialization-and-cleanup-functions"></a>Gruppenin initialisierungs- und Bereinigungsfunktionen



| Funktion                                       | Beschreibung                                                                                                            |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupShutdown**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown) | Schließt eine Peergruppe, die mit [**PeerGroupStartup erstellt**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) wurde, und gibt alle zugeordneten Ressourcen zurück. |
| [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup)   | Initiiert eine Peergruppe mithilfe einer angeforderten Version der Peerinfrastruktur.                                        |



 

## <a name="group-creation-and-access-functions"></a>Gruppenerstellungs- und Zugriffsfunktionen



| Funktion                                                                       | Beschreibung                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose)                                       | Erklärt das Peergruppenhandl für ungültig, das durch einen vorherigen Aufruf der [**PeerGroupCreate-,**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) [**PeerGroupJoin-**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)oder [**PeerGroupOpen-Funktion ermittelt**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) wurde. |
| [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)                                   | Initiiert eine PNRP-Suche nach einer Peergruppe und versucht, eine Verbindung damit herzustellen. Nachdem diese Funktion erfolgreich aufgerufen wurde, kann ein Peer mit anderen Mitgliedern der Peergruppe kommunizieren.                             |
| [**PeerGroupConnectByAddress**](/windows/desktop/api/P2P/nf-p2p-peergroupconnectbyaddress)                 | Versucht, eine Verbindung mit der Peergruppe herzustellen, an der andere Peers mit bekannten IPv6-Adressen teilnehmen.                                                                                                       |
| [**PeerGroupErzeugen**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)                                     | Erstellt eine neue Peergruppe.                                                                                                                                                                                    |
| [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)                 | Gibt eine XML-Zeichenfolge zurück, die vom angegebenen Peer zum Beitreten zu einer Gruppe verwendet werden kann.                                                                                                                                |
| [**PeerGroupCreatePasswordInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreatepasswordinvitation) | Gibt eine XML-Zeichenfolge zurück, die vom angegebenen Peer verwendet werden kann, um einer Gruppe mit einem übereinstimmenden Kennwort beizugeben.                                                                                                       |
| [**PeerGroupDelete**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)                                     | Löscht die lokalen Daten und das Zertifikat, die einer Peergruppe zugeordnet sind.                                                                                                                                         |
| [**PeerGroupGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus)                               | Ruft den aktuellen Status einer Gruppe ab.                                                                                                                                                                     |
| [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)                 | Gibt Anmeldeinformationen, einschließlich gmc, an eine bestimmte Identität aus und gibt optional eine EINLADUNGS-XML-Zeichenfolge zurück, die der eingeladene Peer zum Beitreten zu einer Peergruppe verwenden kann.                                                  |
| [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)                                         | Ermöglicht einem Peer mit einer Einladung den Beitritt zu einer vorhandenen Peergruppe.                                                                                                                                             |
| [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)                                         | Öffnet eine Peergruppe, die ein Peer erstellt oder beigetreten ist.                                                                                                                                                        |
| [**PeerGroupParseInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)                   | Gibt eine [**PEER \_ INVITATION \_ INFO-Struktur**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) mit den Details einer bestimmten Einladung zurück.                                                                                        |
| [**PeerGroupPasswordJoin**](/windows/desktop/api/P2P/nf-p2p-peergrouppasswordjoin)                         | Ermöglicht einem Peer mit einer Einladung und dem richtigen Kennwort das Beitreten zu einer kennwortgeschützten Peergruppe.                                                                                                           |



 

## <a name="group-and-member-information-functions"></a>Gruppen- und Memberinformationsfunktionen



| Funktion                                                 | Beschreibung                                                                                                                        |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)     | Erstellt eine Enumeration der verfügbaren Peergruppenmitglieder und der zugehörigen Mitgliedschaftsinformationen.                                  |
| [**PeerGroupGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergroupgetproperties) | Ruft Informationen zu den Eigenschaften einer angegebenen Gruppe ab.                                                                      |
| [**PeerGroupSetProperties**](/windows/desktop/api/P2P/nf-p2p-peergroupsetproperties) | Legt die aktuellen Peergruppeneigenschaften fest. In Version 1.0 dieser API kann nur der Ersteller der Peergruppe diesen Vorgang ausführen. |



 

## <a name="records-and-record-management-functions"></a>Funktionen für die Datensatz- und Datensatzverwaltung



| Funktion                                                 | Beschreibung                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)         | Fügt der Peergruppe einen neuen Datensatz hinzu, der an alle beteiligten Peers propagiert wird. |
| [**PeerGroupDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)   | Löscht einen Datensatz aus einer Peergruppe. Nur der Ersteller eines Datensatzes kann ihn löschen.      |
| [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)     | Erstellt eine Enumeration von Peergruppendatensätzen.                                        |
| [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord)         | Ruft einen bestimmten Gruppendatensatz ab.                                                   |
| [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) | Durchsucht die lokale Peergruppendatenbank nach Datensätzen, die den angegebenen Kriterien entsprechen. |
| [**PeerGroupUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)   | Aktualisiert einen Datensatz innerhalb einer bestimmten Peergruppe.                                       |



 

## <a name="group-database-importexport-functions"></a>Gruppendatenbank-Import/Export Funktionen



| Funktion                                                   | Beschreibung                                                                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase) | Exportiert eine Peergruppendatenbank in eine bestimmte Datei, die auf einen anderen Computer übertragen und mit der [**PeerGroupImportDatabase-Funktion importiert werden**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) kann. |
| [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) | Importiert eine Peergruppendatenbank aus einer lokalen Datei.                                                                                                                                          |



 

## <a name="direct-connection-functions"></a>Funktionen für direkte Verbindungen



| Funktion                                                                 | Beschreibung                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) | Schließt eine bestimmte direkte Verbindung zwischen zwei Peers.              |
| [**PeerGroupEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections)             | Erstellt eine Enumeration von Verbindungen, die derzeit auf dem Peer aktiv sind. |
| [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)   | Stellt eine direkte Verbindung mit einem anderen Peer in einer Peergruppe ein.  |
| [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)                           | Sendet Daten über eine benachbarte oder direkte Verbindung an ein Mitglied.        |



 

## <a name="group-events-infrastructure"></a>Infrastruktur für Gruppenereignisse



| Funktion                                                     | Beschreibung                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)       | Ermöglicht es einer Anwendung, die von einem Gruppierungsereignis zurückgegebenen Daten abzurufen.                       |
| [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)     | Registriert einen Peer für bestimmte Peergruppenereignisse.                                               |
| [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) | Aufheben der Registrierung eines Peers bei der Benachrichtigung von Peerereignissen, die dem angegebenen Ereignishand handle zugeordnet sind. |



 

## <a name="group-time-conversion-functions"></a>Funktionen für die Gruppenzeitkonvertierung



| Funktion                                                                     | Beschreibung                                                                                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupPeerTimeToUniversalTime**](/windows/desktop/api/P2P/nf-p2p-peergrouppeertimetouniversaltime) | Konvertiert den von der Peergruppe verwalteten Verweiszeitwert in einen lokalisierten Zeitwert, der für die Anzeige auf einem Peercomputer geeignet ist. |
| [**PeerGroupUniversalTimeToPeerTime**](/windows/desktop/api/P2P/nf-p2p-peergroupuniversaltimetopeertime) | Konvertiert einen lokalen Zeitwert vom Computer eines Peers in einen gemeinsamen Peergruppenzeitwert.                                         |



 

## <a name="group-configuration-functions"></a>Gruppenkonfigurationsfunktionen



| Funktion                                               | Beschreibung                                                                                                                       |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig) | Exportiert die Gruppenkonfiguration für einen Peer als XML-Zeichenfolge, die die Identität, den Gruppennamen und den GMC für die Identität enthält. |
| [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) | Importiert eine Peergruppenkonfiguration für eine Identität basierend auf den spezifischen Einstellungen in einer angegebenen XML-Konfigurationszeichenfolge.         |



 

 

 



