---
title: Abruf von Änderungen mithilfe des DirSync-Steuerelements
description: Das Active Directory-Verzeichnissynchronisierungs-Steuerelement (DirSync) ist eine LDAP-Servererweiterung, mit der eine Anwendung eine Verzeichnispartition nach Objekten durchsuchen kann, die sich seit einem früheren Zustand geändert haben.
ms.assetid: f77caeb3-bfc9-4ae6-8d1d-73f4ee554336
ms.tgt_platform: multiple
keywords:
- Abruf von Änderungen mithilfe des DirSync-Steuerelements AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b95e9fed93a962ef95e8cdbe08c202bd8e46df21959d9e1fcabe8eac033b6ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185407"
---
# <a name="polling-for-changes-using-the-dirsync-control"></a>Abruf von Änderungen mithilfe des DirSync-Steuerelements

Das Active Directory-Verzeichnissynchronisierungs-Steuerelement (DirSync) ist eine LDAP-Servererweiterung, mit der eine Anwendung eine Verzeichnispartition nach Objekten durchsuchen kann, die sich seit einem früheren Zustand geändert haben.

Verwenden Sie das DirSync-Steuerelement über ADSI, indem Sie bei Verwendung von [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch)die **Sucheinstellung ADS \_ SEARCHPREF \_ DIRSYNC** angeben. Weitere Informationen und ein Codebeispiel finden Sie unter [Beispielcode mit ADS \_ SEARCHPREF \_ DIRSYNC](example-code-using-ads-searchpref-dirsync.md). Sie können auch eine DirSync-Suche mithilfe der LDAP-API ausführen. Im Folgenden wird die ADSI-Implementierung beschrieben, von denen die meisten auch für die direkte Verwendung von LDAP gelten, außer wie am Ende dieses Themas erläutert.

Wenn Sie eine DirSync-Suche durchführen, übergeben Sie ein anbieterspezifisches Datenelement (Cookie), das den Verzeichniszustand zum Zeitpunkt der vorherigen DirSync-Suche identifiziert. Bei der ersten Suche übergeben Sie ein NULL-Cookie, und die Suche gibt alle Objekte zurück, die mit dem Filter übereinstimmen. Die Suche gibt auch ein gültiges Cookie zurück. Store Cookie in demselben Speicher ab, den Sie mit dem Active Directory-Server synchronisieren. Bei nachfolgenden Suchvorgängen müssen Sie das Cookie aus dem Speicher erhalten und mit der Suchanforderung übergeben. Die Suchergebnisse enthalten jetzt nur die Objekte und Attribute, die sich seit dem vorherigen durch das Cookie identifizierten Zustand geändert haben. Die Suche gibt auch ein neues Cookie zurück, das für die nächste Suche gespeichert werden soll.

In der folgenden Tabelle sind die Suchparameter aufgeführt, die von der Clientsuchanforderung angegeben werden können.



| Parameter          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Basis der Suche | Die Basis für eine DirSync-Suche muss der Stamm einer Verzeichnispartition sein, bei der es sich um eine Domänenpartition, die Konfigurationspartition oder die Schemapartitionen geben kann.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Bereich              | Der Bereich einer DirSync-Suche muss **ADS \_ SCOPE \_ SUBTREE** sein, also die gesamte Teilstruktur der Partition. Beachten Sie, dass bei der Suche nach einer Domänenpartition die Teilstruktur die Kopf- und nicht den Inhalt der Konfigurations- und Schemapartitionen enthält. Verwenden Sie anstelle von DirSync das **USNChanged-Verfahren,** um Änderungen in einem kleineren Bereich zu überprüfen.                                                                                                                                                                                                                                                                                                                                                                                 |
| Filtern             | Sie können einen beliebigen gültigen Suchfilter angeben. Bei einer ersten Suche mit einem NULL-Cookie enthalten die Ergebnisse alle Objekte, die mit dem Filter übereinstimmen. Bei nachfolgenden Suchvorgängen mit einem gültigen Cookie enthalten die Suchergebnisse nur Daten für Objekte, die mit dem Filter übereinstimmen und sich seit dem durch das Cookie angegebenen Zustand geändert haben. Weitere Informationen zu Suchfiltern finden Sie unter [Erstellen eines Abfragefilters.](creating-a-query-filter.md)                                                                                                                                                                                                                                                                                                                |
| Attribute         | Sie können eine Liste von Attributen angeben, die bei einer Änderung zurückgegeben werden sollen. Für jedes Objekt enthalten die ersten Ergebnisse alle angeforderten Attribute, die für das Objekt festgelegt wurden. Nachfolgende Suchergebnisse enthalten nur die angegebenen Attribute, die sich geändert haben. Unveränderte Attribute sind nicht in den Suchergebnissen enthalten. In der ADSI-Implementierung enthalten die Suchergebnisse immer **objectGUID** und **instanceType** jedes Objekts. Außerdem fungiert die angegebene Attributliste als zusätzlicher Filter: Die ersten Suchergebnisse enthalten nur Objekte, für die mindestens eines der angegebenen Attribute festgelegt ist. Nachfolgende Suchvorgänge enthalten nur Objekte, für die eines oder mehrere attribute geändert wurden (Werte hinzugefügt oder gelöscht). |



 

Beachten Sie außerdem, dass:

-   Bei inkrementellen Suchvorgängen besteht die bewährte Methode in der Bindung an den gleichen Domänencontroller (DC), der in der vorherigen Suche verwendet wurde, d. h. an den DC, der das Cookie generiert hat. Wenn derselbe DC nicht verfügbar ist, warten Sie entweder, bis er ist, oder binden Sie ihn an einen neuen DC, und führen Sie eine vollständige Synchronisierung durch. Store sie den DNS-Namen des Domänencontrollers im sekundären Speicher mit dem Cookie an.

    Sie können ein von einem DC generiertes Cookie an einen anderen Domänencontroller übergeben, der ein Replikat derselben Verzeichnispartition hostet. Es besteht keine Möglichkeit, dass ein Client Änderungen über ein Cookie von einem Domänencontroller auf einem anderen DC verpasst. Es ist jedoch möglich, dass die Suchergebnisse des neuen Domänencontrollers gemeldete Änderungen des alten Domänencontrollers enthalten. In einigen Fällen gibt der neue Domänencontroller möglicherweise alle Objekte und Attribute zurück, wie bei einer vollständigen Synchronisierung. Der Client sollte seine Datenbank nur mit den gemeldeten Suchergebnissen für jeden angegebenen DirSync-Aufruf konsistent machen, d.&a; alle inkrementellen Ergebnisse so behandeln, als ob sie den aktuellen Zustand hätten. Es spielt keine Rolle, ob Sie die Änderung bereits gesehen haben oder sogar in einen vorherigen Zustand zurückwechseln, da wiederholte inkrementelle Synchronisierungen auf Konsistenz konvergiert werden.

-   Wenn ein Objekt umbenannt oder verschoben wird, werden seine untergeordneten Objekte ( falls überhaupt ) nicht in die Suchergebnisse aufgenommen, obwohl sich die Distinguished Names der untergeordneten Objekte geändert haben. Wenn ein vererbbarer ACE in einem Objektsicherheitsdeskriptor geändert wird, werden die untergeordneten Objekte des Objekts auch dann nicht in die Suchergebnisse aufgenommen, wenn sich die Sicherheitsbeschreibungen der untergeordneten Objekte geändert haben.
-   Verwenden Sie das **objectGUID-Attribut,** um die nachverfolgten Objekte zu identifizieren. Die **objectGUID jedes** Objekts bleibt unverändert, unabhängig davon, wo das Objekt innerhalb der Gesamtstruktur verschoben wird.
-   Beachten Sie, dass die Suchergebnisse einer DirSync-Suche den Zustand der Objekte auf einem Replikat der Verzeichnispartition zum Zeitpunkt der Suche angeben. Dies bedeutet, dass Änderungen, die auf anderen Domänencontrollern vorgenommen werden, nicht eingeschlossen werden, wenn sie nicht auf den Ziel-DC repliziert wurden. Dies bedeutet auch, dass sich die Attribute eines Objekts seit der vorherigen DirSync-Suche möglicherweise mehrmals geändert haben, aber die Suche zeigt nur den endgültigen Zustand an, nicht die Sequenz der Änderungen.
-   In der ADSI-Implementierung muss die Anwendung das Cookie als nicht transparent behandeln und keine Annahmen über die interne Organisation oder den Wert treffen.
-   Beachten Sie, dass der Client das Cookie, die Cookielänge und den DNS-Namen des Domänencontrollers in demselben Speicher speichert, der die synchronisierten Objektdaten enthält. Dadurch wird sichergestellt, dass das Cookie und andere Parameter mit den Objektdaten synchron bleiben, wenn der Speicher jemals aus einer Sicherung wiederhergestellt wird.
-   Zum Abrufen des [**parentGUID-Attributs,**](/windows/desktop/ADSchema/a-parentguid) das für das DirSync-Steuerelement erstellt wird, ist es auch erforderlich, das [**Name-Attribut**](/windows/desktop/ADSchema/a-name) an fordern.

Um das DirSync-Steuerelement verwenden zu können, muss dem Aufrufer das Recht "Verzeichnisänderungen erhalten" im Stammverzeichnis der überwachten Partition zugewiesen sein. Standardmäßig wird dieses Recht den Konten Administrator und LocalSystem auf Domänencontrollern zugewiesen. Der Aufrufer muss außerdem über das erweiterte [**Steuerelementzugriffsrecht DS-Replication-Get-Changes**](/windows/desktop/ADSchema/r-ds-replication-get-changes) verfügen. Weitere Informationen zum Implementieren eines Änderungsnachverfolgungsmechanismus für Anwendungen, die unter einem Konto ausgeführt werden müssen, das nicht über dieses Recht verfügt, finden Sie unter [Polling for Changes Using USNChanged](polling-for-changes-using-usnchanged.md). Weitere Informationen zu Berechtigungen finden Sie unter [Berechtigungen.](/windows/desktop/SecAuthZ/privileges)

## <a name="retrieving-deleted-objects-with-a-dirsync-search"></a>Abrufen gelöschter Objekte mit einer DirSync-Suche

Die **ADS \_ SEARCHPREF \_ DIRSYNC-Suchergebnisse** enthalten automatisch gelöschte Objekte (Tombstones), die mit dem angegebenen Suchfilter übereinstimmen. Ein Suchfilter, der einem Objekt bei Live-1-0-000-Entität zusingt, kann jedoch nicht mit dem Objekt übereinstimmen, nachdem es gelöscht wurde. Dies liegt daran, dass Tombstones nur eine Teilmenge der Attribute beibehalten, die im ursprünglichen Objekt vorhanden sind. Beispielsweise würden Sie in der Regel den folgenden Filter für Benutzerobjekte verwenden.


```C++
(&(objectClass=user)(objectCategory=person))
```



Das **objectCategory-Attribut** wird entfernt, wenn ein Objekt gelöscht wird, sodass der obige Filter nicht mit Tombstoneobjekten übereinstimmen würde. Im Gegensatz dazu wird das **objectClass-Attribut** für Tombstoneobjekte beibehalten, sodass ein Filter von "(objectClass=user)" mit gelöschten Benutzerobjekten übereinstimmen würde.

Die Attributliste, die Sie mit einer DirSync-Suche angeben, fungiert auch als Filter. -Suchergebnisse enthalten nur Objekte, für die sich mindestens eines der angegebenen Attribute seit der vorherigen DirSync-Suche geändert hat. Wenn die Attributliste keine Attribute enthält, die für Tombstones beibehalten werden, enthalten die Suchergebnisse keine Tombstones. Um dies zu behandeln, fordern Sie alle Attribute an, indem Sie eine NULL-Attributliste angeben. Oder Sie können das **IsDeleted-Attribut** anfordern, das für alle Tombstones auf **TRUE** festgelegt ist. Bei Tombstoneattributen ist 0x8 Bit im **searchFlags-Attribut** der **AttributeSchema-Definition** festgelegt.

Weitere Informationen finden Sie unter [Abrufen gelöschter Objekte.](retrieving-deleted-objects.md)

## <a name="ldap-implementation-of-the-dirsync-control"></a>LDAP-Implementierung des DirSync-Steuerelements

Sie können auch eine DirSync-Suche durchführen, indem Sie die LDAP-API mit dem [LDAP \_ SERVER \_ DIRSYNC \_ OID-Steuerelement](/previous-versions/windows/desktop/ldap/ldap-server-dirsync-oid) verwenden. Wenn Sie die LDAP-API verwenden, geben Sie auch die [STEUERELEMENTE LDAP SERVER EXTENDED \_ \_ \_ DN \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-extended-dn-oid) und [LDAP SERVER SHOW \_ \_ \_ DELETED \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) an. Das LDAP \_ SERVER \_ EXTENDED \_ \_ DN-OID-Steuerelement  bewirkt, dass eine LDAP-Suche eine erweiterte Form des Distinguished Name zurücksendet, die objectGUID und **objectSID** für Sicherheitsprinzipalobjekte wie Benutzer, Gruppen und Computer enthält. Das OID-Steuerelement LDAP SERVER SHOW DELETED bewirkt, dass die Suchergebnisse \_ \_ Daten für \_ \_ gelöschte Objekte enthalten. Beachten Sie, dass diese Steuerelemente automatisch in die ADSI-Implementierung einbezogen werden.

 

 