---
title: Abfragen von Änderungen mit USNChanged
description: Änderungen aus Active Directory können auch durch Abfragen des uSNChanged-Attributs abgerufen werden, wodurch die Einschränkungen des DirSync-Steuerelements vermieden werden.
ms.assetid: 83bda359-09e5-4abf-8f60-9c63bccfcdd1
ms.tgt_platform: multiple
keywords:
- Abfragen von Änderungen mitHILFE von USNChanged AD
- USNChanged AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c665d536eb3dcb0e3265a2e3abb87808ddf630510e5d0600f6185007c72bc28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025528"
---
# <a name="polling-for-changes-using-usnchanged"></a>Abfragen von Änderungen mit USNChanged

Das DirSync-Steuerelement ist leistungsstark und effizient, weist jedoch zwei wesentliche Einschränkungen auf:

-   Nur für Anwendungen mit hohen Berechtigungen: Um das DirSync-Steuerelement verwenden zu können, muss eine Anwendung unter einem Konto ausgeführt werden, das über die **Berechtigung SE SYNC AGENT \_ \_ \_ NAME** auf dem Domänencontroller verfügt. Einige Konten sind so stark privilegiert, sodass eine Anwendung, die das DirSync-Steuerelement verwendet, nicht von normalen Benutzern ausgeführt werden kann.
-   Keine Unterstruktur: Das DirSync-Steuerelement gibt alle Änderungen zurück, die innerhalb eines Namenskontexts auftreten. Eine Anwendung, die nur an Änderungen interessiert ist, die in einer kleinen Teilstruktur eines Namenskontexts auftreten, muss viele irrelevante Änderungen durchlaufen, was sowohl für die Anwendung als auch für den Domänencontroller ineffizient ist.

Änderungen aus Active Directory können auch durch Abfragen des [**uSNChanged-Attributs**](/windows/desktop/ADSchema/a-usnchanged) abgerufen werden, wodurch die Einschränkungen des DirSync-Steuerelements vermieden werden. Diese Alternative ist nicht in jeder Hinsicht besser als das DirSync-Steuerelement, da es die Übertragung aller Attribute umfasst, wenn sich Attribute ändern, und es mehr Arbeit vom Anwendungsentwickler erfordert, um bestimmte Fehlerszenarien ordnungsgemäß zu behandeln. Es ist derzeit die beste Möglichkeit, bestimmte Anwendungen zur Änderungsnachverfolgung zu schreiben.

Wenn ein Domänencontroller ein Objekt ändert, legt er das [**uSNChanged-Attribut**](/windows/desktop/ADSchema/a-usnchanged) dieses Objekts auf einen Wert fest, der größer als der vorherige Wert des **uSNChanged-Attributs** für dieses Objekt und größer als der aktuelle Wert des **uSNChanged-Attributs** für alle anderen Objekte ist, die auf diesem Domänencontroller enthalten sind. Infolgedessen kann eine Anwendung das zuletzt geänderte Objekt auf einem Domänencontroller finden, indem sie das Objekt mit dem größten **uSNChanged-Wert** sucht. Das zweite zuletzt geänderte Objekt auf einem Domänencontroller weist den zweiten größten **uSNChanged-Wert** auf usw.

Das [**uSNChanged-Attribut**](/windows/desktop/ADSchema/a-usnchanged) wird nicht repliziert, weshalb das Lesen des **uSNChanged-Attributs** eines Objekts auf zwei verschiedenen Domänencontrollern in der Regel unterschiedliche Werte ergibt.

Beispielsweise kann das [**uSNChanged-Attribut**](/windows/desktop/ADSchema/a-usnchanged) verwendet werden, um Änderungen in einer Teilstruktur S nachzuverfolgen. Führen Sie zunächst eine "vollständige Synchronisierung" der Teilstruktur S aus. Angenommen, der größte **uSNChanged-Wert** für jedes Objekt in S ist U. Fragen Sie in regelmäßigen Abständen nach allen Objekten in Teilstruktur S ab, deren **uSNChanged-Wert** größer als U ist. Die Abfrage gibt alle Objekte zurück, die sich seit der vollständigen Synchronisierung geändert haben. Legen Sie den größten **uSNChanged** unter diesen geänderten Objekten fest, und Sie können erneut abfragen.

Zu den Feinheiten der Implementierung einer [**uSNChanged-Synchronisierungsanwendung**](/windows/desktop/ADSchema/a-usnchanged) gehören:

-   Verwenden Sie das **attribut highestCommittedUSN** von rootDSE, um Ihre [**uSNChanged-Filter**](/windows/desktop/ADSchema/a-usnchanged) zu binden. Lesen Sie also vor dem Starten einer vollständigen Synchronisierung den **höchstenCommittedUSN-Wert** Ihres zugeordneten Domänencontrollers. Führen Sie dann eine vollständige Synchronisierungsabfrage aus (mit ausgelagerungen Ergebnissen), um die Datenbank zu initialisieren. Speichern Sie nach Abschluss dieses Vorgangs den **höchstenCommittedUSN-Wert,** der vor der vollständigen Synchronisierungsabfrage gelesen wurde. , um als untere Grenze des **uSNChanged-Attributs** für die nächste Synchronisierung zu verwenden. Um später eine inkrementelle Synchronisierung durchzuführen, lesen Sie das rootDSE-Attribut **highestCommittedUSN** erneut. Fragen Sie dann relevante Objekte ab, indem Sie ausgelagerungte Ergebnisse verwenden, deren **uSNChanged** größer als die unteren Grenzen des **uSNChanged-Attributwerts** ist, der aus der vorherigen Synchronisierung gespeichert wurde. Aktualisieren Sie die Datenbank mithilfe dieser Informationen. Aktualisieren Sie nach Abschluss des Vorgangs die Untergrenzen des **uSNChanged-Attributs** vom **höchstenCommittedUSN-Wert,** der vor der Abfrage der inkrementellen Synchronisierung gelesen wurde. Speichern Sie immer die Untergrenzen des **uSNChanged-Attributwerts** im gleichen Speicher, in dem die Anwendung mit dem Domänencontrollerinhalt synchronisiert wird.

    Wenn Sie dieses Verfahren befolgen und nicht auf [**uSNChanged-Werten**](/windows/desktop/ADSchema/a-usnchanged) für abgerufene Objekte basieren, vermeiden Sie, dass der Server aktualisierte Objekte erneut untersucht, die außerhalb des Satzes liegen, der für die Anwendung gilt.

-   Da [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) ein nicht repliziertes Attribut ist, muss die Anwendung bei jeder Ausführung an denselben Domänencontroller gebunden werden. Wenn er nicht an diesen Domänencontroller gebunden werden kann, muss er entweder warten, bis dies möglich ist, oder mit einem neuen Domänencontroller verbunden sein und eine vollständige Synchronisierung mit diesem Domänencontroller durchführen. Wenn die Anwendung mit einem Domänencontroller verbunden ist, zeichnet sie den DNS-Namen dieses Domänencontrollers in stabilem Speicher auf. Dabei handelt es sich um denselben Speicher, der mit dem Domänencontrollerinhalt konsistent bleibt. Anschließend wird der gespeicherte DNS-Name verwendet, um für nachfolgende Synchronisierungen eine Bindung an den gleichen Domänencontroller durchzuführen.
-   Die Anwendung muss erkennen, wann der Domänencontroller, dem sie derzeit zugeordnet ist, aus der Sicherung wiederhergestellt wurde, da dies zu Inkonsistenzen führen kann. Wenn die Anwendung mit einem Domänencontroller verbunden ist, speichert sie die "Aufruf-ID" dieses Domänencontrollers im stabilen Speicher zwischen, d. h. denselben Speicher, der mit dem Domänencontrollerinhalt konsistent bleibt. Die "Aufruf-ID" eines Domänencontrollers ist eine GUID, die im **invocationID-Attribut** des Dienstobjekts des Domänencontrollers gespeichert ist. Um den Distinguished Name des Dienstobjekts eines Domänencontrollers abzurufen, lesen Sie das **dsServiceName-Attribut** der rootDSE.

    Beachten Sie, dass beim Wiederherstellen des stabilen Speichers der Anwendung aus der Sicherung keine Konsistenzprobleme auftreten, da der Domänencontrollername, die Aufruf-ID und die unteren Grenzen des [**uSNChanged-Attributwerts**](/windows/desktop/ADSchema/a-usnchanged) mit den Daten gespeichert werden, die mit dem Domänencontrollerinhalt synchronisiert werden.

-   Verwenden Sie paging beim Abfragen des Servers, sowohl vollständige als auch inkrementelle Synchronisierungen, um die Möglichkeit zu vermeiden, große Resultsets gleichzeitig abzurufen. Weitere Informationen finden Sie unter [Angeben anderer Suchoptionen.](specifying-other-search-options.md)
-   Führen Sie indexbasierte Abfragen durch, um zu vermeiden, dass der Server große Zwischenergebnisse speichert, wenn ausgelagerte Ergebnisse verwendet werden. Weitere Informationen finden Sie unter [Indizierte Attribute.](indexed-attributes.md)
-   Verwenden Sie im Allgemeinen keine serverseitige Sortierung von Suchergebnissen, die den Server zwingen können, große Zwischenergebnisse zu speichern und zu sortieren. Dies gilt sowohl für vollständige als auch für inkrementelle Synchronisierungen. Weitere Informationen finden Sie unter [Angeben anderer Suchoptionen.](specifying-other-search-options.md)
-   Behandeln Sie keine übergeordneten Bedingungen ordnungsgemäß. Die Anwendung erkennt möglicherweise ein Objekt, bevor das übergeordnete Objekt erkannt wurde. Je nach Anwendung kann dies ein Problem darstellen. Die Anwendung kann immer den aktuellen Zustand des übergeordneten Elements aus dem Verzeichnis lesen.
-   Um verschobene oder gelöschte Objekte zu verarbeiten, speichern Sie das [**objectGUID-Attribut**](/windows/desktop/ADSchema/a-objectguid) jedes nachverfolgten Objekts. Das **objectGUID-Attribut** eines Objekts bleibt unverändert, unabhängig davon, wo es in der Gesamtstruktur verschoben wird.
-   Um verschobene Objekte zu verarbeiten, führen Sie entweder regelmäßige vollständige Synchronisierungen durch, oder erhöhen Sie den Suchbereich, und filtern Sie uninteressierende Änderungen am Clientende heraus.
-   Um gelöschte Objekte zu verarbeiten, führen Sie entweder regelmäßige vollständige Synchronisierungen oder eine separate Suche nach gelöschten Objekten durch, wenn Sie eine inkrementelle Synchronisierung durchführen. Wenn Sie gelöschte Objekte abfragen, rufen Sie die [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) der gelöschten Objekte ab, um die Objekte zu bestimmen, die aus der Datenbank gelöscht werden sollen. Weitere Informationen finden Sie unter [Abrufen gelöschter Objekte.](retrieving-deleted-objects.md)
-   Beachten Sie, dass die Suchergebnisse nur die Objekte und Attribute enthalten, die der Aufrufer lesen darf (basierend auf den Sicherheitsbeschreibungen und DACLs für die verschiedenen Objekte). Weitere Informationen finden Sie unter [Auswirkungen der Sicherheit auf Abfragen.](effects-of-security-on-queries.md)

Weitere Informationen und ein Codebeispiel, das die Grundlagen einer USNChanged-Synchronisierungsanwendung zeigt, finden Sie unter [Beispielcode zum Abrufen von Änderungen mit USNChanged.](example-code-to-retrieve-changes-using-usnchanged.md)

 

 