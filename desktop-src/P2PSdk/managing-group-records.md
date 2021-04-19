---
description: Bei einem Gruppendaten Satz handelt es sich um spezifische Daten, die für alle aktiven Mitglieder einer Peer Gruppe veröffentlicht werden, z. b. eine Chat Nachricht oder eine anwendungsspezifische Statusaktualisierung.
ms.assetid: 073ee4e9-0e97-451a-a808-8265575d073c
title: Verwalten von Gruppendaten Sätzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b6d9e3257cc597b715dc9c65eb5945c00c15286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362477"
---
# <a name="managing-group-records"></a>Verwalten von Gruppendaten Sätzen

Bei einem Gruppendaten Satz handelt es sich um spezifische Daten, die für alle aktiven Mitglieder einer Peer Gruppe veröffentlicht werden, z. b. eine Chat Nachricht oder eine anwendungsspezifische Statusaktualisierung. Ein Datensatz wird durch die [**Peer \_ Daten Satz**](/windows/desktop/api/P2P/ns-p2p-peer_record) Struktur dargestellt und enthält die folgenden Informationen zu einem Peer:

-   Die Datensatz-ID ist ein Wert, der einen Datensatz in der Peer Gruppe eindeutig identifiziert.
-   Eine GUID, die den Daten Satz Typ angibt. Anwendungen können unterschiedliche Daten Satz Typen unterstützen. Eine Anwendung interpretiert das **Datenfeld eines Daten** Satzes auf der Grundlage des Daten Satz Typs. Einige GUIDs sind reserviert, und der API-Rückruf gibt **Peer \_ E \_ nicht \_ autorisiert** zurück, wenn die Anwendung versucht, Sie zu verwenden.
-   Ein Satz von Daten Satz Attributen, die als XML-Zeichenfolge beschrieben werden. Die Attribute werden beim Durchsuchen von Datensätzen verwendet. Weitere Informationen zu Attributen finden Sie unter [Datensatz Attribute Schema](record-attribute-schema.md).
-   Die Peer Zeit, zu der ein Datensatz erstellt wird.
-   Die Peer Zeit, zu der ein Datensatz abläuft.
-   Die Peer Zeit, zu der ein Datensatz geändert wird.
-   Der Ersteller eines Datensatzes.
-   Der Member, der einen Datensatz ändert.
-   Eine [**Peer \_ Daten**](/windows/desktop/api/P2P/ns-p2p-peer_data) Struktur, die die kryptografische Signatur für alle Felder in dieser Peer Daten [**\_ Satz**](/windows/desktop/api/P2P/ns-p2p-peer_record) Struktur enthält. Dieses Feld kann nicht direkt von einem Peer aktualisiert oder geändert werden.
-   Eine [**Peer \_ Daten**](/windows/desktop/api/P2P/ns-p2p-peer_data) Struktur, die die anwendungsspezifischen Daten enthält, die diesem Datensatz als Bytearray zugeordnet sind. Der Datentyp, der in diesem Feld vorhanden ist, wird durch einen Anwendungs definierten Daten Satz Typen bestimmt.

## <a name="obtaining-peer-group-records"></a>Abrufen von Peer Gruppendaten Sätzen

Einzelne Datensätze werden abgerufen, indem " [**Peer groupgetrecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) " mit der ID des Datensatzes aufgerufen wird. Wenn alle Datensätze eines bestimmten Typs verarbeitet werden, wird der aufgelistete Satz aller aktuellen Peer Gruppendaten Sätze abgerufen, indem zuerst [**peergroupumrecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords) aufgerufen wird, um die Enumeration zu öffnen und anschließend [**peergetnextitem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) aufzurufen, bis alle Datensätze abgerufen wurden. Wenn Sie fertig sind, schließen Sie die-Enumeration, und geben Sie den zugeordneten Arbeitsspeicher frei, indem Sie " [**Peer Enumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration)" aufrufen.

Wenn ein Datensatz von einem Peer erstellt, gelöscht oder aktualisiert wird, wird der betroffene Datensatz über das Änderungs Ereignis des **Peer \_ Gruppen \_ Ereignis \_ Datensatzes \_** für alle Mitglieder der Peer Gruppe veröffentlicht. Beachten Sie Folgendes: Wenn ein Peer nicht mit der Gruppe verbunden ist, wird der aktualisierte Datensatz empfangen, wenn er das nächste Mal eine Verbindung herstellt. Es ist wichtig, sich mit "Peer Group [**pregisterevent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) " für dieses Ereignis zu registrieren, wenn Ihre Anwendung Datensätze auf sinnvolle Weise verwaltet oder verwaltet. Alternativ kann die Anwendung die datensatzdatenbank Bedarfs gesteuert mithilfe von " [**Peer Group searchrecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords)" Abfragen.

Wenn das **Änderungs Ereignis des Peer \_ Gruppen \_ Ereignis \_ Datensatzes \_** ausgelöst wird, werden die jeweilige Datensatz-ID und der Typ sowie der Typ der Änderung (hinzufügen, aktualisieren, löschen) als [**Änderungs Datenstruktur des Peer \_ Ereignis \_ Datensatzes \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_event_record_change_data) empfangen. Diese Struktur wird durch einen Aufrufen von " [**Peer groupgeteventdata**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)" abgerufen. Wenn es sich bei der Änderung um ein Add-oder Update-Update handelt, sollten Sie den Datensatz mit der angegebenen ID mithilfe von " [**Peer groupgetrecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) " abrufen. Die lokale datensatzdatenbank für die Infrastruktur wird automatisch aktualisiert.

Sie können auch nach bestimmten Datensätzen suchen, die auf bestimmten benutzerdefinierten Attributen basieren, die im Feld **pwzattribute** des [**Peer \_ Datensatzes**](/windows/desktop/api/P2P/ns-p2p-peer_record)bereitgestellt werden, sowie auf allen vordefinierten Attributen. Verwenden Sie hierzu die Funktion " [**Peer groupsearchrecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) " mit einer XML-Suchabfrage, die im Thema [Datensatz-Suchabfrage Format](record-search-query-format.md) angegeben ist.

Weitere Informationen zum Arbeiten mit Datensätzen in der Peer Infrastruktur finden Sie im Thema " [Datensätze](records.md) " unter [Verwenden der Peer Infrastruktur](using-the-peer-infrastructure.md).

## <a name="administration-of-peer-group-records"></a>Verwaltung von Peer Gruppen-Datensätzen

Wenn die anfänglichen Einladungen vom Ersteller der Peer Gruppe ausgegeben werden, können Sie angeben, dass bestimmte Mitglieder in einer administrativen Rolle (Peer \_ Gruppen- \_ Rollen \_ Administrator) fungieren, wenn Sie dem Benutzer neue Anmelde Informationen (entweder über [**peergroupkreateinvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) oder [**peergroupissuecredenseins**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)) ausgibt. Ein Administrator kann beliebige Peer Gruppendaten Sätze direkt hinzufügen, löschen und aktualisieren. Umgekehrt kann ein Peer Gruppenmitglied, dessen Rolle entweder auf ein Mitglied der **Peer \_ Gruppen \_ Rolle \_** oder auf ein **\_ \_ \_ einladender \_ Mitglied der Peer Gruppen Rolle** festgelegt ist, nur eigene Datensätze hinzufügen, aktualisieren und löschen.

Der Ersteller verfügt standardmäßig über die Administrator Rolle.

Um einen Datensatz zu aktualisieren, rufen Sie den Datensatz mit " [**Peer groupgetrecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) " oder " [**Peer-groupumrecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)" ab, nehmen Sie die Änderungen vor, und übergeben Sie den aktualisierten Datensatz an " [**Peer-groupupdaterecord**](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)".

Um einen Datensatz zu löschen, übergeben Sie die Datensatz-ID zum Löschen an " [**Peer groupdeleterecord**](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)".

Um einen Datensatz hinzuzufügen, erstellen Sie eine neue [**Peer \_ Daten Satz**](/windows/desktop/api/P2P/ns-p2p-peer_record) Struktur, und füllen Sie die folgenden Felder aus:

-   **dwSize**. Dieses Feld enthält den Wert von **sizeof**([**Peer \_ Datensatz**](/windows/desktop/api/P2P/ns-p2p-peer_record)).
-   **ftexpiration**. Dieses Feld enthält das Ablaufdatum und die Ablaufzeit dieses Datensatzes, ausgedrückt als Peer Zeit als **FILETIME** -Struktur.
-   **geben** Sie ein. Dieses Feld enthält einen **GUID** -Wert, der den Daten Satz Typen für die Anwendung identifiziert. Wenn dieser Typ für Ihre Anwendungs Infrastruktur Benutzer definiert ist, sollten Sie auch das **Datenfeld** auffüllen.

Die folgenden Felder werden von der-Infrastruktur aufgefüllt und werden ignoriert, wenn Sie von der Anwendung festgelegt werden:

-   **id**
-   **pwzkreatorid**
-   **pwzlastmodifiedbyid**
-   **ftcreation**
-   **ftlastmodified**
-   **securitydata**

Die restlichen Felder sind optional. Um diesen neuen Datensatz der Peer Gruppe hinzuzufügen, übergeben Sie ihn an [**peergroupaddrecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord).

## <a name="importing-and-exporting-records"></a>Importieren und Exportieren von Datensätzen

Peer-zu-Peer-Gruppendaten Sätze werden lokal als Datenbank verwaltet. Um eine aktuelle Momentaufnahme der datensatzdatenbank der Peer Gruppe in einer lokalen Datei zu speichern, nennen Sie [**peergroupexportdatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase), und übergeben Sie das Handle an die Peer Gruppe. Diese Datei kann dann auf einen anderen Computer oder eine andere Anwendung übertragen werden, wodurch diese datensatzdatenbank durch Aufrufen von " [**Peer groupimportdatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)" extrahiert und verwendet werden kann.

 

 



