---
title: Abrufen von Änderungen mithilfe des Dirsync-Steuer Elements
description: Die Active Directory Directory-Synchronisierung (Dirsync) ist eine LDAP-Server Erweiterung, die es einer Anwendung ermöglicht, eine Verzeichnis Partition nach Objekten zu durchsuchen, die sich seit einem früheren Zustand geändert haben.
ms.assetid: f77caeb3-bfc9-4ae6-8d1d-73f4ee554336
ms.tgt_platform: multiple
keywords:
- Abrufen von Änderungen mithilfe des DirSync-Steuerelement-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3d105757d39bc25bd10df21ab68c4d1d1202be
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724472"
---
# <a name="polling-for-changes-using-the-dirsync-control"></a>Abrufen von Änderungen mithilfe des Dirsync-Steuer Elements

Die Active Directory Directory-Synchronisierung (Dirsync) ist eine LDAP-Server Erweiterung, die es einer Anwendung ermöglicht, eine Verzeichnis Partition nach Objekten zu durchsuchen, die sich seit einem früheren Zustand geändert haben.

Verwenden Sie das DirSync-Steuerelement über ADSI, indem Sie die Such Einstellung **ADS \_ searchpref \_ Dirsync** bei Verwendung von [**idirector ysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch)angeben. Weitere Informationen und ein Codebeispiel finden Sie unter [Beispielcode mit ADS \_ searchpref \_ Dirsync](example-code-using-ads-searchpref-dirsync.md). Sie können auch eine Dirsync-Suche mit der LDAP-API durchführen. Im folgenden wird die ADSI-Implementierung beschrieben. die meisten davon gelten auch für die direkte Verwendung von LDAP, außer wie am Ende dieses Themas erläutert.

Wenn Sie eine Dirsync-Suche durchführen, übergeben Sie ein Anbieter spezifisches Datenelement (Cookie), das den Verzeichnis Zustand zum Zeitpunkt der vorherigen Dirsync-Suche identifiziert. Bei der ersten Suche übergeben Sie ein NULL-Cookie, und die Suche gibt alle Objekte zurück, die dem Filter entsprechen. Die Suche gibt auch ein gültiges Cookie zurück. Speichern Sie das Cookie im gleichen Speicher, den Sie mit dem Active Directory-Server synchronisieren. Bei nachfolgenden Such Vorgängen wird das Cookie aus dem Speicher abgeraten und mit der Such Anforderung übergeben. Die Suchergebnisse enthalten jetzt nur die Objekte und Attribute, die sich seit dem vorherigen Zustand, der durch das Cookie identifiziert wurde, geändert haben. Die Suche gibt auch ein neues Cookie zurück, das für die nächste Suche gespeichert werden soll.

In der folgenden Tabelle werden die Suchparameter aufgelistet, die von der Client Such Anforderung angegeben werden können.



| Parameter          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Basis der Suche | Die Basis einer Dirsync-Suche muss der Stamm einer Verzeichnis Partition sein, bei der es sich um eine Domänen Partition, die Konfigurations Partition oder die Schema Partition handeln kann.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Bereich              | Der Gültigkeitsbereich einer Dirsync-Suche muss eine **Werbe \_ Bereichs \_ Unterstruktur** sein, d. h. die gesamte Unterstruktur der Partition. Beachten Sie, dass die Teilstruktur bei einer Suche nach einer Domänen Partition die Köpfe, aber nicht den Inhalt der Konfigurations-und Schema Partitionen enthält. Um Änderungen in einem kleineren Bereich abzurufen, verwenden Sie anstelle von DirSync die Methode "nicht **geändert** ".                                                                                                                                                                                                                                                                                                                                                                                 |
| Filter             | Sie können einen beliebigen gültigen Suchfilter angeben. Bei einer ersten Suche mit einem NULL-Cookie enthalten die Ergebnisse alle Objekte, die dem Filter entsprechen. Bei nachfolgenden Such Vorgängen mit einem gültigen Cookie enthalten die Suchergebnisse nur Daten für Objekte, die dem Filter entsprechen und sich seit dem durch das Cookie festgelegten Status geändert haben. Weitere Informationen zu Suchfiltern finden Sie unter [Erstellen eines Abfrage Filters](creating-a-query-filter.md).                                                                                                                                                                                                                                                                                                                |
| Attribute         | Sie können eine Liste von Attributen angeben, die zurückgegeben werden sollen, wenn eine Änderung auftritt. Für jedes Objekt enthalten die anfänglichen Ergebnisse alle angeforderten Attribute, die für das Objekt festgelegt wurden. Nachfolgende Suchergebnisse enthalten nur die angegebenen Attribute, die geändert wurden. Unveränderte Attribute sind nicht in den Suchergebnissen enthalten. In der ADSI-Implementierung enthalten die Suchergebnisse immer die **objectGUID** und **instanceType** jedes Objekts. Außerdem fungiert die angegebene Attribut Liste als zusätzlicher Filter: in den ersten Suchergebnissen sind nur Objekte enthalten, für die mindestens eines der angegebenen Attribute festgelegt ist. bei nachfolgenden Such Vorgängen werden nur Objekte angezeigt, für die ein oder mehrere Attribute geändert wurden (hinzugefügte oder gelöschte Werte). |



 

Beachten Sie auch Folgendes:

-   Bei inkrementellen suchen empfiehlt es sich, an denselben Domänen Controller (DC) zu binden, der in der vorherigen Suche verwendet wurde, d. h. an den Domänen Controller, der das Cookie generiert hat. Wenn derselbe DC nicht verfügbar ist, warten Sie, bis er ist, oder binden Sie an einen neuen Domänen Controller, und führen Sie eine vollständige Synchronisierung durch. Speichern Sie den DNS-Namen des Domänen Controllers im sekundären Speicher mit dem Cookie.

    Sie können ein von einem Domänen Controller generiertes Cookie an einen anderen Domänen Controller übergeben, der ein Replikat derselben Verzeichnis Partition hostet. Es ist nicht möglich, dass ein Client Änderungen durch Verwendung eines Cookies von einem Domänen Controller auf einem anderen DC verpasst. Es ist jedoch möglich, dass die Suchergebnisse des neuen Domänen Controllers gemeldete Änderungen des alten Domänen Controllers einschließen. in einigen Fällen gibt der neue DC möglicherweise alle Objekte und Attribute zurück, wie bei einer vollständigen Synchronisierung. Der Client sollte seine Datenbank lediglich mit den gemeldeten Suchergebnissen für einen beliebigen Dirsync-Befehl konsistent machen, d. h., alle inkrementellen Ergebnisse werden so behandelt, als wären Sie der aktuelle Zustand. Es spielt keine Rolle, ob Sie die Änderung schon vor oder nach einem früheren Zustand erkannt haben, da sich die wiederholten inkrementellen Synchronisierung bei Konsistenz annähern.

-   Wenn ein Objekt umbenannt oder verschoben wird, sind seine untergeordneten Objekte, sofern vorhanden, nicht in den Suchergebnissen enthalten, auch wenn sich die Distinguished Names der untergeordneten Objekte geändert haben. Ebenso, wenn ein vererbbarer ACE in einem Objekt Sicherheits Deskriptor geändert wird, sind die untergeordneten Objekte des-Objekts nicht in den Suchergebnissen enthalten, auch wenn sich die Sicherheits Deskriptoren der untergeordneten-Objekte geändert haben.
-   Verwenden Sie das **objectGUID** -Attribut, um die nach verfolgten Objekte zu identifizieren. Die **objectGUID** jedes Objekts bleibt unverändert, unabhängig davon, wo das Objekt innerhalb der Gesamtstruktur verschoben wird.
-   Beachten Sie, dass die Suchergebnisse einer Dirsync-Suche den Zustand der Objekte auf einem Replikat der Verzeichnis Partition zum Zeitpunkt der Suche angeben. Dies bedeutet, dass Änderungen an anderen DCS nicht eingeschlossen werden, wenn Sie nicht auf den Ziel-DC repliziert wurden. Dies bedeutet auch, dass sich die Attribute eines Objekts seit der vorherigen Dirsync-Suche mehrmals geändert haben können. bei der Suche wird jedoch nur der endgültige Zustand angezeigt, nicht die Abfolge der Änderungen.
-   In der ADSI-Implementierung muss die Anwendung das Cookie als nicht transparent behandeln und keine Annahmen über die interne Organisation oder den Wert machen.
-   Beachten Sie, dass der Client das Cookie, die Cookie-Länge und den DNS-Namen des Domänen Controllers im gleichen Speicher speichert, der die synchronisierten Objektdaten enthält. Dadurch wird sichergestellt, dass das Cookie und andere Parameter mit den Objektdaten synchron bleiben, wenn der Speicher jemals aus einer Sicherung wieder hergestellt wird.
-   Um das für das DirSync-Steuerelement erstellte Attribut " [**arguid**](/windows/desktop/ADSchema/a-parentguid) " abzurufen, muss auch das [**namens**](/windows/desktop/ADSchema/a-name) Attribut angefordert werden.

Um das DirSync-Steuerelement zu verwenden, muss dem Aufrufer im Stamm der überwachten Partition das Recht "Verzeichnis Get Changes" zugewiesen sein. Dieses Recht wird standardmäßig den Konten "Administrator" und "LocalSystem" auf Domänen Controllern zugewiesen. Der Aufrufer muss auch über das Zugriffsrecht " [**DS-Replication-Get-Changes**](/windows/desktop/ADSchema/r-ds-replication-get-changes) Extended Control" verfügen. Weitere Informationen zum Implementieren eines Mechanismus zur Änderungs Nachverfolgung für Anwendungen, die unter einem Konto ausgeführt werden müssen, das nicht über dieses Recht verfügt, finden Sie unter Abrufen [von Änderungen mithilfe von "US-nchanged](polling-for-changes-using-usnchanged.md)". Weitere Informationen zu Berechtigungen finden Sie unter [Berechtigungen](/windows/desktop/SecAuthZ/privileges).

## <a name="retrieving-deleted-objects-with-a-dirsync-search"></a>Abrufen von gelöschten Objekten mit einer Dirsync-Suche

Die **\_ \_ Dirsync-Suchergebnisse von ADS searchpref** enthalten automatisch gelöschte Objekte (Tombstones), die dem angegebenen Suchfilter entsprechen. Ein Suchfilter, der mit einem Objekt verglichen wird, wenn es aktiv ist, stimmt jedoch möglicherweise nicht mit dem Objekt ab, nachdem es gelöscht wurde. Dies liegt daran, dass Tombstones nur eine Teilmenge der Attribute beibehalten, die für das ursprüngliche Objekt vorhanden sind. Beispielsweise verwenden Sie in der Regel den folgenden Filter für Benutzer Objekte.


```C++
(&(objectClass=user)(objectCategory=person))
```



Das **objectCategory** -Attribut wird entfernt, wenn ein Objekt gelöscht wird. Daher stimmt der Filter oben nicht mit den Tombstone-Objekten aus. Umgekehrt wird das **objectClass** -Attribut in Tombstone-Objekten aufbewahrt, sodass ein Filter von "(objectClass = User)" gelöschten Benutzer Objekten entspricht.

Die Attribut Liste, die Sie mit einer Dirsync-Suche angeben, fungiert auch als Filter. die Suchergebnisse enthalten nur Objekte, bei denen mindestens eines der angegebenen Attribute seit der vorherigen Dirsync-Suche geändert wurde. Wenn die Attribut Liste keine Attribute enthält, die auf Tombstones aufbewahrt werden, enthalten die Suchergebnisse keine Tombstones. Um dies zu behandeln, fordern Sie alle Attribute an, indem Sie eine NULL-Attribut Liste angeben. Sie können auch das **isDeleted** -Attribut anfordern und für alle Tombstones auf " **true** " festlegen. Bei Tombstone-Attributen ist das 0x8-Bit im **searchFlags** -Attribut der **attributeSchema** -Definition festgelegt.

Weitere Informationen finden Sie unter [Abrufen von gelöschten Objekten](retrieving-deleted-objects.md).

## <a name="ldap-implementation-of-the-dirsync-control"></a>LDAP-Implementierung des Dirsync-Steuer Elements

Sie können auch eine Dirsync-Suche durchführen, indem Sie die LDAP-API mit dem [LDAP- \_ Server \_ Dirsync \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-dirsync-oid) -Steuerelement verwenden. Wenn Sie die LDAP-API verwenden, geben Sie auch die [ \_ \_ Erweiterte \_ DN- \_ OID des LDAP-Servers](/previous-versions/windows/desktop/ldap/ldap-server-extended-dn-oid) und LDAP-Server mit [ \_ \_ \_ gelöschten \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) -Steuerelementen anzeigen Das \_ \_ Erweiterte DN-OID des LDAP-Servers \_ \_ bewirkt, dass eine LDAP-Suche eine erweiterte Form des Distinguished Name zurückgibt, die **objectGUID** und **objectSID** für Sicherheits Prinzipal Objekte wie z. b. Benutzer, Gruppen und Computer enthält. Der LDAP- \_ Server " \_ \_ gelöschtes OID" anzeigen \_ bewirkt, dass die Suchergebnisse Daten für gelöschte Objekte enthalten. Beachten Sie, dass diese Steuerelemente automatisch in der ADSI-Implementierung enthalten sind.

 

 