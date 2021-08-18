---
description: Ein Gruppendatensatz sind bestimmte Daten, die für alle aktiven Mitglieder einer Peergruppe veröffentlicht werden, z. B. eine Chatnachricht oder eine anwendungsspezifische Statusaktualisierung.
ms.assetid: 073ee4e9-0e97-451a-a808-8265575d073c
title: Verwalten von Gruppendatensätzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d2d0ba77a315043e638ddaa28615cf84654852a13e73347ee36ee4c7d66a6e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061398"
---
# <a name="managing-group-records"></a>Verwalten von Gruppendatensätzen

Ein Gruppendatensatz sind bestimmte Daten, die für alle aktiven Mitglieder einer Peergruppe veröffentlicht werden, z. B. eine Chatnachricht oder eine anwendungsspezifische Statusaktualisierung. Ein Datensatz wird durch die [**PEER \_ RECORD-Struktur**](/windows/desktop/api/P2P/ns-p2p-peer_record) dargestellt und enthält die folgenden Informationen zu einem Peer:

-   Die Datensatz-ID ist ein Wert, der einen Datensatz in der Peergruppe eindeutig identifiziert.
-   Eine GUID, die den Datensatztyp angibt. Anwendungen können verschiedene Datensatztypen unterstützen. Eine Anwendung interpretiert das **Datenfeld** eines Datensatzes basierend auf dem Datensatztyp. Einige GUIDs sind reserviert, und der API-Aufruf gibt **PEER E NOT AUTHORIZED \_ \_ \_ zurück,** wenn die Anwendung versucht, sie zu verwenden.
-   Ein Satz von Datensatzattributen, die als XML-Zeichenfolge beschrieben werden. Die Attribute werden beim Durchsuchen von Datensätzen verwendet. Weitere Informationen zu Attributen finden Sie unter [Datensatzattributschema](record-attribute-schema.md).
-   Die Peerzeit, zu der ein Datensatz erstellt wird.
-   Die Peerzeit, zu der ein Datensatz abläuft.
-   Die Peerzeit, zu der ein Datensatz geändert wird.
-   Der Ersteller eines Datensatzes.
-   Der Member, der einen Datensatz ändert.
-   Eine [**PEER \_ DATA-Struktur,**](/windows/desktop/api/P2P/ns-p2p-peer_data) die die kryptografische Signatur für alle Felder in dieser [**PEER \_ RECORD-Struktur**](/windows/desktop/api/P2P/ns-p2p-peer_record) enthält. Dieses Feld kann nicht direkt von einem Peer aktualisiert oder geändert werden.
-   Eine [**PEER \_ DATA-Struktur,**](/windows/desktop/api/P2P/ns-p2p-peer_data) die die anwendungsspezifischen Daten enthält, die diesem Datensatz als Bytearray zugeordnet sind. Der Datentyp in diesem Feld wird durch den anwendungsdefinierten Datensatztyp bestimmt.

## <a name="obtaining-peer-group-records"></a>Abrufen von Peergruppendatensätzen

Einzelne Datensätze werden durch Aufrufen von [**PeerGroupGetRecord mit**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) der ID des Datensatzes ermittelt. Wenn alle Datensätze eines bestimmten Typs verarbeitet werden, wird der aufzählte Satz aller aktuellen Peergruppendatensätze abgerufen, indem zuerst [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords) aufgerufen wird, um die Enumeration zu öffnen, und anschließend [**iterativ PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) aufgerufen wird, bis alle Datensätze abgerufen werden. Schließen Sie die Enumeration, und geben Sie den ihr zugeordneten Arbeitsspeicher frei, indem Sie [**PeerEndEnumeration aufrufen.**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration)

Wenn ein Datensatz von einem Peer erstellt, gelöscht oder aktualisiert wird, wird der betroffene Datensatz über das **PEER GROUP EVENT RECORD \_ \_ \_ \_ CHANGE-Ereignis** für alle Mitglieder der Peergruppe veröffentlicht. Beachten Sie, dass ein Peer, der nicht mit der Gruppe verbunden ist, den aktualisierten Datensatz erhält, wenn er das nächste Mal eine Verbindung herstellt. Es ist wichtig, sich für dieses Ereignis mit [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) zu registrieren, wenn Ihre Anwendung Datensätze auf sinnvolle Weise verwaltet oder verwaltet. Alternativ kann die Anwendung die Datensatzdatenbank bei Bedarf mit [**peerGroupSearchRecords abfragen.**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords)

Wenn das **PEER GROUP EVENT RECORD \_ \_ \_ \_ CHANGE-Ereignis** ausgelöst wird, werden die spezifische Datensatz-ID und der Typ sowie der Typ der Änderung (Hinzufügen, Aktualisieren, Löschen) als [**PEER EVENT RECORD CHANGE \_ \_ \_ \_ DATA-Struktur**](/windows/desktop/api/P2P/ns-p2p-peer_event_record_change_data) empfangen. Diese Struktur wird mit einem Aufruf von [**PeerGroupGetEventData erhalten.**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) Wenn die Änderung ein Hinzufügen oder Aktualisieren ist, sollten Sie [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) verwenden, um den Datensatz mit der angegebenen ID zu erhalten. Die lokale Datensatzdatenbank für die Infrastruktur wird automatisch aktualisiert.

Sie können auch nach bestimmten Datensätzen suchen, die auf bestimmten benutzerdefinierten Attributen basieren, die im **Feld pwzAttributes** von [**PEER \_ RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record)angegeben sind, sowie nach vordefinierten Attributen. Verwenden Sie hierzu die [**PeerGroupSearchRecords-Funktion**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) mit einer XML-Suchabfrage, die wie im Thema Suchabfrageformat für Datensätze [angegeben formatiert](record-search-query-format.md) ist.

Weitere Informationen zum Arbeiten mit Datensätzen in der [](records.md) Peerinfrastruktur finden Sie im Thema Datensätze unter [Verwenden der Peerinfrastruktur.](using-the-peer-infrastructure.md)

## <a name="administration-of-peer-group-records"></a>Verwaltung von Peergruppendatensätzen

Wenn die ersten Einladungen vom Ersteller der Peergruppe ausgegeben werden, kann sie angeben, dass bestimmte Mitglieder in einer Administratorrolle (PEER GROUP ROLE ADMIN) dienen, wenn neue Anmeldeinformationen für den Benutzer ausgegeben werden (entweder über \_ \_ \_ [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) oder [**PeerGroupIssueCredentials).**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) Ein Administrator kann Alle Peergruppendatensätze direkt hinzufügen, löschen und aktualisieren. Umgekehrt kann ein Peergruppenmitglied, dessen Rolle auf **PEER \_ GROUP ROLE \_ \_ MEMBER** oder **PEER GROUP ROLE INVITING \_ \_ \_ \_ MEMBER** festgelegt ist, nur eigene Datensätze hinzufügen, aktualisieren und löschen.

Der Ersteller verfügt standardmäßig über die Administratorrolle.

Um einen Datensatz zu aktualisieren, müssen Sie den Datensatz mit [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) oder [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)abrufen, die Änderungen vornehmen und den aktualisierten Datensatz [**an PeerGroupUpdateRecord übergeben.**](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)

Um einen Datensatz zu löschen, übergeben Sie die zu löschende Datensatz-ID an [**PeerGroupDeleteRecord.**](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)

Erstellen Sie zum Hinzufügen eines Datensatzes eine neue [**PEER \_ RECORD-Struktur,**](/windows/desktop/api/P2P/ns-p2p-peer_record) und füllen Sie die folgenden Felder aus:

-   **dwSize**. Dieses Feld enthält den Wert von **sizeof**([**PEER \_ RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record)).
-   **ftExpiration**. Dieses Feld enthält das Ablaufdatum und die Uhrzeit dieses Datensatzes, ausgedrückt als Peerzeit als **FILETIME-Struktur.**
-   **geben Sie ein.** Dieses Feld enthält einen **GUID-Wert,** der den Datensatztyp für die Anwendung identifiziert. Wenn dieser Typ für Ihre Anwendungsinfrastruktur benutzerdefiniert ist, sollten Sie auch das **Datenfeld** auffüllen.

Die folgenden Felder werden von der Infrastruktur aufgefüllt und ignoriert, wenn sie von der Anwendung festgelegt werden:

-   **id**
-   **pwzCreatorId**
-   **pwzLastModifiedById**
-   **ftCreation**
-   **ftLastModified**
-   **securityData**

Die restlichen Felder sind optional. Um diesen neuen Datensatz der Peergruppe hinzuzufügen, übergeben Sie ihn an [**PeerGroupAddRecord.**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)

## <a name="importing-and-exporting-records"></a>Importieren und Exportieren von Datensätzen

Peer-zu-Peer-Gruppendatensätze werden lokal als Datenbank verwaltet. Um eine aktuelle Momentaufnahme der Peergruppendatensatz-Datenbank in einer lokalen Datei zu speichern, rufen Sie [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)auf, und übergeben Sie es an die Peergruppe. Diese Datei kann dann auf einen anderen Computer oder eine andere Anwendung übertragen werden, die diese Datensatzdatenbank extrahieren und verwenden kann, indem [**PeerGroupImportDatabase aufruft.**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)

 

 



