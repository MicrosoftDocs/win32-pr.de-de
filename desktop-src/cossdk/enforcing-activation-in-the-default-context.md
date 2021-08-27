---
description: Eine konfigurierte COM-Komponente wird in der Regel in ihrem eigenen Kontext aktiviert. Das heißt, COM+ verweist auf die Komponentenkataloginformationen, um konfigurierte Dienste zur Verfügung zu stellen.
ms.assetid: 09dc7165-22b1-4eca-9591-d83e85556f3f
title: Erzwingen der Aktivierung im Standardkontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d188fb50521e09c88a9c61136e33928176faa1f70a94680b31cf0cc1e75cb8eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070760"
---
# <a name="enforcing-activation-in-the-default-context"></a>Erzwingen der Aktivierung im Standardkontext

Eine konfigurierte COM-Komponente wird in der Regel in ihrem eigenen Kontext aktiviert. Das heißt, COM+ verweist auf die Kataloginformationen der Komponente, um konfigurierte Dienste zur Verfügung zu stellen. Sie können jedoch eine konfigurierte Komponente im Standardkontext aktivieren. Eine COM-Basiskomponente – eine registrierte Komponente ohne COM+-Kataloginformationen – wird in der Regel im Standardkontext aktiviert.

Das Aktivieren einer COM-Komponente im Standardkontext bietet drei wesentliche Leistungsvorteile:

-   Sie speichern Systemressourcen, indem Sie die Anzahl der erstellten Kontexte begrenzen.
-   Sie erhöhen die Leistung, indem Sie die Anzahl kontextübergreifender Aufrufe begrenzen. Da Aufrufe über Kontexte hinweg Marshalling erfordern, ist es viel schneller, wenn ein COM-Objekt, das im Standardkontext aktiviert ist, Aufrufe an andere Objekte im Standardkontext senden kann. Die Leistung in diesem Fall (von Aufrufen innerhalb desselben Kontexts) ähnelt der des Aufrufs einer Unterroutine.
-   Sie können ältere COM-Anwendungen in COM+ importieren und problemlos ausführen. Beispielsweise können Sie mehrere ältere COM-Anwendungen unter der Annahme implementiert haben, dass objektverweise innerhalb eines Apartments übergeben werden können, ohne die Verweise zu marshallen. Diese COM-Anwendungen funktionieren nicht, wenn sie in COM+ importiert werden, da die Objektverweise über Kontextgrenzen hinweg übergeben werden. Sie können diese Art von COM-Anwendung jedoch beim Importieren ausführen, wenn Sie das Verwaltungstool komponentendienste verwenden, um alle Klassen in der Anwendung als Muss im Standardkontext aktiviert **werden zu markieren.**

Der Hauptnachteil der Aktivierung einer konfigurierten Komponente im Standardkontext ist, dass COM+ keine der konfigurierten Dienste der Komponente bietet. Es gibt einen Abkniff zwischen der verbesserten Leistung und der Möglichkeit, COM+-Dienste zu verwenden.

Angenommen, eine COM-Komponente erfordert keine COM+-Dienste (z. B. Transaktionen [,](com--transactions.md) [Just-in-Time-Aktivierung](com--just-in-time-activation.md), [Ereignisse](com--events.md) [,](com--queued-components.md)Warteschlangenkomponenten, [Synchronisierung](com--synchronization.md)oder [Objektpooling](com--object-pooling.md)), und dass die Komponente eine Reihe von Aufrufen an andere COM-Komponenten vorsendet, die im Standardkontext aktiviert werden können. In diesem Fall ist es eine gute Idee, die aufrufende Komponente im Standardkontext zu aktivieren.

Wenn die COM-Komponente COM+-Dienste erfordert, kann sie nicht als **Muss im Standardkontext aktiviert werden markiert werden.** Darüber hinaus gibt es keinen echten Leistungsgewinn, wenn ein im Standardkontext aktiviertes COM-Objekt eine Reihe von Aufrufen von Objekten in anderen Kontexten vor sich geht. (Weitere Informationen finden Sie unter [Kontexte](com--contexts.md).)

**So erzwingen Sie die Aktivierung im Standardkontext**

1.  Klicken Sie im Detailbereich des Komponentendienste-Verwaltungstools mit der  rechten Maustaste auf die Komponente (die sich im Ordner Komponenten einer beliebigen ausgewählten COM+-Anwendung befindet), die Sie im Standardkontext aktivieren möchten, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Komponenteneigenschaften auf die **Registerkarte Aktivierung.**

3.  Aktivieren Sie **das Kontrollkästchen Muss im Standardkontext** aktiviert werden.

4.  Klicken Sie auf **OK**.

> [!Note]  
> Wenn Sie eine konfigurierte Komponente im Standardkontext ausführen, aktiviert COM+ keine der konfigurierten Dienste für diese Komponente. Diese Dienste sind wieder verfügbar, wenn Sie das Kontrollkästchen Muss im Standardkontext aktiviert sein deaktivieren und anschließend die konfigurierte Komponente in ihrem eigenen Kontext ausführen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte der COM+-Just-In-Time-Aktivierung](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Erzwingen der Aktivierung im Kontext des Aufrufers](enforcing-activation-in-the-caller-s-context.md)
</dt> </dl>

 

 



