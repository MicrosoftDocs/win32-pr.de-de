---
description: Eine konfigurierte COM-Komponente wird normalerweise in einem eigenen Kontext aktiviert; Das heißt, com+ verweist auf die Komponenten Katalog Informationen, um konfigurierte Dienste bereitzustellen.
ms.assetid: 09dc7165-22b1-4eca-9591-d83e85556f3f
title: Erzwingen der Aktivierung im Standardkontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41599f71dc37c37c1a9a574d274ca2858835e2df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524363"
---
# <a name="enforcing-activation-in-the-default-context"></a>Erzwingen der Aktivierung im Standardkontext

Eine konfigurierte COM-Komponente wird normalerweise in einem eigenen Kontext aktiviert; Das heißt, com+ verweist auf die Katalog Informationen der Komponente, um konfigurierte Dienste bereitzustellen. Sie können jedoch festlegen, dass eine konfigurierte Komponente im Standardkontext aktiviert werden soll. Eine Basis-COM-Komponente – eine registrierte Komponente ohne com+-Katalog Informationen – wird normalerweise im Standardkontext aktiviert.

Das Aktivieren einer COM-Komponente im Standardkontext bietet wie folgt drei wichtige Leistungsvorteile:

-   Sie speichern Systemressourcen, indem Sie die Anzahl der erstellten Kontexte begrenzen.
-   Sie erhöhen die Leistung, indem Sie die Anzahl von Kontext übergreifenden aufrufen einschränken. Da Aufrufe zwischen Kontexten Marshalling erfordern, ist es für ein COM-Objekt, das im Standardkontext aktiviert ist, viel schneller, Aufrufe an andere Objekte im Standardkontext vorzunehmen. Die Leistung in diesem Fall (von aufrufen innerhalb desselben Kontexts) ähnelt der des Aufrufs einer Unterroutine.
-   Ältere COM-Anwendungen können in com+ importiert und ohne Probleme ausgeführt werden. Beispielsweise können mehrere ältere COM-Anwendungen unter der Annahme implementiert werden, dass es zulässig ist, Objekt Verweise innerhalb eines Apartment zu übergeben, ohne dass die Verweise gemarshallt werden. Diese com-Anwendungen funktionieren nicht, wenn Sie in com+ importiert werden, da die Objekt Verweise über Kontext Grenzen hinweg übermittelt werden. Sie können diese Art von COM-Anwendung jedoch beim Importieren ausführen, wenn Sie das Verwaltungs Programmkomponenten Dienste verwenden, um alle Klassen in der Anwendung zu markieren, die **im Standardkontext aktiviert werden müssen**.

Der größte Nachteil beim Aktivieren einer konfigurierten Komponente im Standardkontext ist, dass com+ keinen der konfigurierten Dienste der Komponente bereitstellt. Es gibt einen Kompromiss zwischen verbesserter Leistung und der Möglichkeit, com+-Dienste zu verwenden.

Nehmen Sie beispielsweise an, dass für eine COM-Komponente keine COM+-Dienste erforderlich sind (z. b. [Transaktionen](com--transactions.md), [Just-in-Time-Aktivierung](com--just-in-time-activation.md), [Ereignisse](com--events.md), in der [Warteschlange befindliche Komponenten](com--queued-components.md), [Synchronisierung](com--synchronization.md)oder [Objekt Pooling](com--object-pooling.md)) und dass die Komponente eine Reihe von Aufrufen an andere COM-Komponenten ausführt, die möglicherweise im Standardkontext aktiviert werden. In diesem Fall empfiehlt es sich, die aufrufende Komponente im Standardkontext zu aktivieren.

Wenn für die COM-Komponente com+-Dienste erforderlich sind, kann Sie nicht als markiert werden, da Sie **im Standardkontext aktiviert werden muss**. Außerdem gibt es keine wirkliche Leistungssteigerung, wenn ein im Standardkontext aktiviertes com-Objekt eine Reihe von Aufrufen an Objekte in anderen Kontexten ausführt. (Ausführlichere Informationen finden Sie unter [Kontexte](com--contexts.md).)

**So erzwingen Sie die Aktivierung im Standardkontext**

1.  Klicken Sie im Detailbereich des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die Komponente (befindet sich im Ordner **Komponenten** der ausgewählten COM+-Anwendung), die Sie im Standardkontext aktivieren möchten, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Aktivierung** .

3.  Aktivieren Sie das Kontrollkästchen **muss im Standardkontext aktiviert werden**.

4.  Klicken Sie auf **OK**.

> [!Note]  
> Wenn Sie eine konfigurierte Komponente im Standardkontext ausführen, aktiviert com+ keinen der konfigurierten Dienste für diese Komponente. Diese Dienste sind erneut verfügbar, wenn Sie das Kontrollkästchen **muss im Standardkontext aktiviert werden aktiviert** deaktivieren und anschließend die konfigurierte Komponente in einem eigenen Kontext ausführen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte für die Just-in-Time-Aktivierung in com+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Erzwingen der Aktivierung im Kontext des Aufrufers](enforcing-activation-in-the-caller-s-context.md)
</dt> </dl>

 

 



