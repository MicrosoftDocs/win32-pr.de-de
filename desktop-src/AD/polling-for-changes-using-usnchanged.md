---
title: Abrufen von Änderungen mithilfe von ""
description: Änderungen von Active Directory können auch durch Abfragen des Attributs "Attribut" abgerufen werden, wodurch die Einschränkungen des Dirsync-Steuer Elements vermieden werden.
ms.assetid: 83bda359-09e5-4abf-8f60-9c63bccfcdd1
ms.tgt_platform: multiple
keywords:
- Abrufen von Änderungen mithilfe von "US-Changed AD"
- Über geändertes AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e062c84fae575f837f45d78be7c92e5e284c1e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858132"
---
# <a name="polling-for-changes-using-usnchanged"></a>Abrufen von Änderungen mithilfe von ""

Das DirSync-Steuerelement ist leistungsfähig und effizient, hat jedoch zwei bedeutende Einschränkungen:

-   Nur für Anwendungen mit hohen Berechtigungen: um das DirSync-Steuerelement zu verwenden, muss eine Anwendung unter einem Konto ausgeführt werden, das über die Berechtigung " **SE \_ Sync \_ Agent \_ Name** " auf dem Domänen Controller verfügt. Wenige Konten sind so stark privilegiert, sodass eine Anwendung, die das DirSync-Steuerelement verwendet, nicht von normalen Benutzern ausgeführt werden kann.
-   Keine Unterstruktur Bereich: das DirSync-Steuerelement gibt alle Änderungen zurück, die innerhalb eines Namens Kontexts auftreten. Eine Anwendung, die nur an Änderungen interessiert ist, die in einer kleinen Teilstruktur eines Namens Kontexts auftreten, muss viele irrelevante Änderungen durchlaufen, was sowohl für die Anwendung als auch für den Domänen Controller ineffizient ist.

Änderungen von Active Directory können auch durch Abfragen [**des Attributs**](/windows/desktop/ADSchema/a-usnchanged) "Attribut" abgerufen werden, wodurch die Einschränkungen des Dirsync-Steuer Elements vermieden werden. Diese Alternative ist nicht besser geeignet als das DirSync-Steuerelement, da es das Übertragen aller Attribute erfordert, wenn sich ein beliebiges Attribut ändert, und es mehr Arbeit vom Anwendungsentwickler erfordert, um bestimmte Fehler Szenarios ordnungsgemäß zu verarbeiten. Derzeit ist dies die beste Möglichkeit, bestimmte Anwendungen für die Änderungs Nachverfolgung zu schreiben.

Wenn ein Objekt von einem Domänen [**Controller geändert wird**](/windows/desktop/ADSchema/a-usnchanged) , wird das Attribut "-Attribut" für dieses Objekt auf einen Wert festgelegt, der größer ist als der vorherige Wert des Attributs "Attribut" für dieses Objekt und größer als der aktuelle Wert **des Attributs** **"Attribut"** für alle anderen auf diesem Domänen Controller gespeicherten Objekte. Folglich kann eine Anwendung das zuletzt geänderte Objekt auf einem Domänen Controller suchen, indem Sie das-Objekt mit dem **größten Wert von** "von der Größe" gefunden hat. Das zweite zuletzt geänderte Objekt auf einem Domänen Controller verfügt über den **zweitgrößten Wert** für "Wert", usw.

Das Attribut [**"Attribut"**](/windows/desktop/ADSchema/a-usnchanged) wird nicht repliziert, daher werden in der Regel unterschiedliche Werte durch das Lesen des Attributs " **" von "** " für ein Objekt auf zwei verschiedenen Domänen Controllern

So kann z. b [**. das Attribut**](/windows/desktop/ADSchema/a-usnchanged) "-Attribut" verwendet werden, um Änderungen in einer Teilstruktur zu verfolgen. Führen Sie zunächst eine "vollständige Synchronisierung" der Teilstruktur "s" aus. angenommen, **der größte Wert** für "Wert" für ein Objekt in S ist U. führen Sie in Regel  mäßigen Abständen Abfragen für alle Objekte in der Teilstruktur aus Die Abfrage gibt alle Objekte zurück, die seit der vollständigen Synchronisierung geändert wurden. Legen Sie auf die größte **Änderung** der geänderten Objekte fest, und wiederholen Sie den Abruf Vorgang.

Die folgenden Feinheiten der Implementierung einer Anwendungs [**geänderten**](/windows/desktop/ADSchema/a-usnchanged) Synchronisierungs Anwendung sind:

-   Verwenden Sie das **highestCommittedUSN** -Attribut von RootDSE, um die von der Anwendung [**geänderten**](/windows/desktop/ADSchema/a-usnchanged) Filter zu binden. Das heißt, bevor Sie eine vollständige Synchronisierung starten, lesen Sie die **highestCommittedUSN** Ihres zugehörigen Domänen Controllers. Führen Sie dann eine vollständige Synchronisierungs Abfrage (mithilfe von Auslagerungs Ergebnissen) aus, um die Datenbank zu initialisieren. Speichern Sie nach Abschluss des Vorgangs den Wert **highestCommittedUSN** , der vor der vollständigen Synchronisierungs Abfrage gelesen wurde. , wenn für die nächste Synchronisierung als untere Grenze **des Attributs** "-Attribut" verwendet werden soll. Um später eine inkrementelle Synchronisierung durchzuführen, müssen Sie das rootDSE-Attribut **highestCommittedUSN** erneut registrieren. Fragen Sie dann relevante Objekte ab, indem Sie auslagerbare Ergebnisse verwenden, deren " **enchanged** " größer ist als die Untergrenze des von der vorherigen Synchronisierung **gespeicherten Attributs** von "Wert". Aktualisieren Sie die Datenbank mit diesen Informationen. Aktualisieren Sie nach Abschluss des Vorgangs die unteren Begrenzungen **des Attributs** "" von " **highestCommittedUSN** ", die vor der inkrementellen Synchronisierungs Abfrage gelesen wurden. Speichern Sie immer die unteren Begrenzungen des Werts für den Wert **des Attributs** in demselben Speicher, den die Anwendung mit dem Domänen Controller Inhalt synchronisiert.

    Wenn Sie diese Prozedur befolgen, anstatt Sie basierend auf den von der Anwendung [**geänderten**](/windows/desktop/ADSchema/a-usnchanged) Werten für abgerufene Objekte zu überprüfen, wird verhindert, dass der Server aktualisierte Objekte erneut untersucht, die außerhalb des für die Anwendung anwendbaren Satzes liegen.

-   Da es sich bei " [**US Changed**](/windows/desktop/ADSchema/a-usnchanged) " um ein nicht repliziertes Attribut handelt, muss die Anwendung bei jeder Ausführung eine Bindung an denselben Domänen Controller herstellen. Wenn eine Bindung an diesen Domänen Controller nicht möglich ist, muss er entweder warten, bis dies möglich ist, oder einem neuen Domänen Controller zuordnen und eine vollständige Synchronisierung mit diesem Domänen Controller durchführen. Wenn die Anwendung mit einem Domänen Controller in Betrieb ist, wird der DNS-Name des Domänen Controllers in einem stabilen Speicher aufgezeichnet, bei dem es sich um denselben Speicher handelt wie der Inhalt des Domänen Controllers. Anschließend verwendet er den gespeicherten DNS-Namen, um für nachfolgende Synchronisierung eine Bindung an denselben Domänen Controller herzustellen.
-   Die Anwendung muss erkennen, wenn der Domänen Controller, dem er derzeit angehört, von der Sicherung wieder hergestellt wurde, da dies zu Inkonsistenzen führen kann. Wenn die Anwendung mit einem Domänen Controller mit einem Domänen Controller ausgeführt wird, wird die Aufruf-ID des Domänen Controllers im stabilen Speicher zwischengespeichert, d. h. der gleiche Speicher, der dem Domänen Controller Inhalt entspricht. Die Aufruf-ID eines Domänen Controllers ist eine GUID, die im **invocationID** -Attribut des Dienst Objekts des Domänen Controllers gespeichert ist. Um den Distinguished Name des Dienst Objekts eines Domänen Controllers zu erhalten, lesen Sie das Attribut **dsservicename** von RootDSE.

    Beachten Sie, dass wenn der stabile Speicher der Anwendung aus der Sicherung wieder hergestellt wird, keine Konsistenzprobleme auftreten, da der Name des Domänen Controllers, die Aufruf-ID [**und die unteren Grenzen des Attributs**](/windows/desktop/ADSchema/a-usnchanged) "Wert des Attributs" mit den Daten gespeichert werden, die mit dem Domänen Controller Inhalt synchronisiert werden.

-   Verwenden Sie Paging bei der Abfrage des Servers, sowohl vollständige als auch inkrementelle Synchronisierung, um die Möglichkeit zu vermeiden, große Resultsets gleichzeitig abzurufen. Weitere Informationen finden Sie unter [Angeben anderer Suchoptionen](specifying-other-search-options.md).
-   Führen Sie indexbasierte Abfragen aus, um zu vermeiden, dass der Server beim Verwenden von ausgelagerten Ergebnissen große Zwischenergebnisse speichert. Weitere Informationen finden Sie unter [indizierte Attribute](indexed-attributes.md).
-   Verwenden Sie im Allgemeinen keine serverseitige Sortierung von Suchergebnissen, wodurch der Server große Zwischenergebnisse speichern und sortieren kann. Dies gilt für vollständige und inkrementelle Synchronisierung. Weitere Informationen finden Sie unter [Angeben anderer Suchoptionen](specifying-other-search-options.md).
-   Behandeln Sie keine übergeordneten Bedingungen ordnungsgemäß. Die Anwendung erkennt möglicherweise ein Objekt, bevor es das übergeordnete Objekt erkannt hat. Abhängig von der Anwendung ist dies möglicherweise ein Problem. Die Anwendung kann den aktuellen Status des übergeordneten Elements immer aus dem Verzeichnis lesen.
-   Speichern Sie das [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) -Attribut jedes überwachten Objekts, um verschockte oder gelöschte Objekte zu verarbeiten. Das **objectGUID** -Attribut eines Objekts bleibt unverändert, unabhängig davon, wo es in die Gesamtstruktur verschoben wird.
-   Um verschoderte Objekte zu verarbeiten, führen Sie entweder regelmäßige vollständige Synchronisierung durch, oder vergrößern Sie den Suchbereich, und Filtern Sie uninteressante Änderungen am Client Ende heraus.
-   Um gelöschte Objekte zu verarbeiten, führen Sie entweder regelmäßige vollständige Synchronisierungen durch, oder führen Sie bei der inkrementellen Synchronisierung eine separate Suche nach gelöschten Wenn Sie gelöschte Objekte Abfragen, rufen Sie die [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) der gelöschten Objekte ab, um zu bestimmen, welche Objekte aus der Datenbank gelöscht werden sollen. Weitere Informationen finden Sie unter [Abrufen von gelöschten Objekten](retrieving-deleted-objects.md).
-   Beachten Sie, dass die Suchergebnisse nur die Objekte und Attribute enthalten, für die der Aufrufer über Leseberechtigung verfügt (basierend auf den Sicherheits Beschreibungen und den DACLs für die verschiedenen Objekte). Weitere Informationen finden Sie unter [Auswirkungen der Sicherheit bei Abfragen](effects-of-security-on-queries.md).

Weitere Informationen und ein Codebeispiel, in dem die Grundlagen einer Anwendungs geänderten Synchronisierungs Anwendung veranschaulicht werden, finden Sie unter [Beispielcode zum Abrufen von Änderungen mithilfe von "US-nchanged](example-code-to-retrieve-changes-using-usnchanged.md)".

 

 