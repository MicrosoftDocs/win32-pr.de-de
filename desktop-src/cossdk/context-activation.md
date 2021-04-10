---
description: In com+ wird jedes COM-Objekt mit einem zugeordneten Kontext erstellt.
ms.assetid: e5602af2-5852-4c34-a792-6742e90b7d41
title: Kontext Aktivierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a652615d6c1288887085c857817e32e3a3b4081c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127149"
---
# <a name="context-activation"></a>Kontext Aktivierung

In com+ wird jedes COM-Objekt mit einem zugeordneten Kontext erstellt. Dies bedeutet, dass entweder ein neuer Kontext erstellt und initialisiert werden muss oder ein entsprechender vorhandener Kontext verwendet wird. Dieser Prozess wird als *Aktivierung* bezeichnet. In com+ wird ein Objekt entweder in einem eigenen Kontext oder in dessen Ersteller (ein Objekt, das die Aktivierung des Objekts angefordert hat – z. b. durch Aufrufen von [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) aktiviert.

In einigen Fällen, wie z. b. beim [Objekt Pooling](com--object-pooling.md), wird ein Objekt aktiviert, ohne dass es von Grund auf neu erstellt wird. In diesem Fall wird eine laufende Instanz innerhalb eines Kontexts aktiviert. Während der Lebensdauer kann Sie in unterschiedlichen Kontexten wiederholt aktiviert werden.

Der grundlegende Mechanismus ist in beiden Fällen identisch – ein Objekt ist einem Kontext zugeordnet, und dieser Kontext wird ordnungsgemäß initialisiert, um die Lauf Zeitanforderungen des Objekts darzustellen.

## <a name="flowing-of-context-properties"></a>Fluss von Kontexteigenschaften

Wenn ein Objekt als Antwort auf eine Erstellungs Anforderung von einem anderen Objekt aktiviert wird, muss com+ zwischen Ihnen vermitteln, um das Downstream-Objekt ordnungsgemäß zu aktivieren. Com+ muss den Kontext des Aufrufers mit der Konfiguration der aufgerufenen Komponente vergleichen und dann entscheiden, wo die Downstreamkomponente aktiviert werden soll und wie deren Kontexteigenschaften initialisiert werden.

Um die Konfiguration der Komponente zu ermitteln, sucht com+ Sie in der com+-Klassen Registrierungsdatenbank, die für extrem schnelle Lauf Zeit Suchvorgänge optimiert ist. (Dies wird dadurch bestimmt, wie Sie eine Komponente bei der Installation in einer COM+-Anwendung konfiguriert haben.) Die Konfiguration der Komponente wird dann anhand des Status der Kontexteigenschaften des Aufrufers überprüft.

In einigen Fällen ist die Konfiguration mit dem Kontext des Aufrufers konsistent, und die Komponente kann im Kontext des Aufrufers aktiviert werden. Dies ist nur möglich, wenn der Kontext des Aufrufers alle Lauf Zeitanforderungen des neuen Objekts erfüllt.

Wenn die Downstreamkomponente nicht innerhalb des Aufrufers des Aufrufers aktiviert werden kann, wird Sie in einem eigenen Kontext in einem entsprechenden Apartment aktiviert. Wenn dies auftritt, können bestimmte Kontexteigenschaften vom Aufrufer zum aufgerufenen weitergeleitet werden. Wenn der Aufrufer z. b. einer Transaktion zugeordnet ist und der aufgerufene Transaktionen unterstützt, erhält das neue-Objekt seinen eigenen Kontext (für die Stimme in der Transaktion, er muss über ein eigenes konsistentes Flag verfügen) und erbt die Transaktions-ID und die Aktivitäts-ID des Aufrufers (die sich innerhalb derselben Transaktion und Synchronisierungs Domäne befinden).

## <a name="ignored-context-properties"></a>Ignorierte Kontexteigenschaften

Abhängig von der Konfiguration einer Komponente können einige Kontexteigenschaften keine Rolle spielen, um zu bestimmen, ob Sie im Kontext des Erstellers oder in Ihrem eigenen Kontext aktiviert ist. Beispielsweise werden die Einstellungen deaktivierte Transaktionen und Synchronisierung deaktiviert, was darauf hinweist, dass eine Transaktion oder Synchronisierungs Domäne vorhanden ist, bei der Aktivierung der Komponente keine Rolle spielen. Diese Eigenschaften werden grundsätzlich ignoriert, wenn der Kontext übertragen wird. Wenn eine Komponente nur die Zugriffs Überprüfung auf Prozessebene verwendet, wird die zugehörige Sicherheitskontext Eigenschaft ignoriert – die Sicherheitskonfiguration der Komponente spielt nie eine Rolle bei der Aktivierung.

## <a name="forcing-activation-in-the-callers-context"></a>Erzwingen der Aktivierung im Kontext des Aufrufers

Unter bestimmten Umständen möchten Sie möglicherweise, dass ein Objekt nur im Kontext seines Aufrufers aktiviert wird – das heißt, es wird nie in seinem eigenen Kontext aktiviert. Beispielsweise können Sie das Verhalten des Objekts steuern, wenn es über eine Kontext Grenze aufgerufen wird.

Mithilfe des Verwaltungs Programms Komponenten Dienste können Sie sicherstellen, dass ein Objekt nicht in einem eigenen Kontext aktiviert werden kann, indem Sie die **Kontext Option muss in** Aufrufer aktivieren auf der Registerkarte **Aktivierung** der Seite Komponenten **Eigenschaften** auswählen. (Eine Schritt-für-Schritt-Anleitung finden Sie [unter Erzwingen der Aktivierung im Kontext des Aufrufers](enforcing-activation-in-the-caller-s-context.md) .) Wenn Sie diese Option auswählen und das Objekt nicht im Kontext des Aufrufers aktiviert werden kann, schlägt [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fehl, und es wird ein Co \_ E- \_ Versuch \_ zur \_ Erstellung \_ außerhalb des \_ Client \_ Kontexts zurückgegeben.

## <a name="default-context"></a>Standardkontext

Standard Kontexte können nicht konfigurierte Komponenten unterstützt werden, d. –. com-Komponenten, die nicht in com+-Anwendungen installiert sind und nicht in der com+-Klassen Registrierungsdatenbank registriert sind. Wenn nicht konfigurierte Komponenten über ein kompatibles Threading Modell verfügen, werden Sie im Kontext des Aufrufers aktiviert. Andernfalls werden Sie in einem Standardkontext im entsprechenden Apartment aktiviert. Jedes Apartment verfügt über einen Standardkontext zur Unterstützung von COM-Objekten, die keine COM+-Dienste verwenden.

## <a name="hooking-activation"></a>Aktivieren der Aktivierung

Durch Implementieren von [**IObjectControl::**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) Activation und [**IObjectControl::D eaktivierung**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)können Sie die Aktivierung und Deaktivierung verknüpfen, um eine spezielle Initialisierung im neuen Kontext auszuführen. Diese Methoden werden von com+ an bestimmten Punkten im Lebenszyklus eines Objekts aufgerufen, wenn das Objekt für die Verwendung der JIT-Aktivierung oder des Objekt Pooling konfiguriert ist. Ausführlichere Informationen finden Sie unter [com+ Just-in-Time-Aktivierung](com--just-in-time-activation.md) und [com+-Objekt Pooling](com--object-pooling.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abfangen von Kontext übergreifenden aufrufen](interception-of-cross-context-calls.md)
</dt> </dl>

 

 
