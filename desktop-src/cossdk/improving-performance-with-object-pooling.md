---
description: Verbessern der Leistung mit Objektpooling
ms.assetid: 7a8a38d8-6549-4686-a298-f3b427b380e3
title: Verbessern der Leistung mit Objektpooling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ce6a86e76f7a97395973cc9cab4c4e9e81177f4312a389c2b01ec2d88eb7a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547847"
---
# <a name="improving-performance-with-object-pooling"></a>Verbessern der Leistung mit Objektpooling

Objektpooling kann unter bestimmten Umständen äußerst effektiv sein und zu erheblichen Leistungssteigerungen führen. Die allgemeine Idee, Objekte wiederzuverwenden, um den besten Vorteil zu bieten, besteht darin, so viele Ressourcen wie möglich zusammenzufassen, die Initialisierung aus der tatsächlich ausgeführten Arbeit herauszustützen und dann die Pooleigenschaften zur Bereitstellungszeit administrativ an die tatsächliche Hardware anzupassen. Das heißt, Sie sollten mit den folgenden Schritten fortfahren:

1.  Schreiben Sie das -Objekt, um die teure Initialisierung und den Ressourcenerwerb zu berücksichtigen, die für jeden Client als Voraussetzung für die tatsächliche Arbeit im Auftrag des Clients ausgeführt werden. Schreiben Sie umfangreiche Objektkonstruktoren in den Pool so viele Ressourcen wie möglich, damit diese vom Objekt gehalten werden und sofort verfügbar sind, wenn Clients ein Objekt aus dem Pool erhalten.
2.  Konfigurieren Sie den Pool administrativ, um ein optimales Gleichgewicht bei den verfügbaren Hardwareressourcen zu erzielen. In der Regel wird der Speicher, der für die Verwaltung eines Pools einer bestimmten Größe reserviert ist, im Austausch für einen schnelleren Clientzugriff und die Verwendung von Objekten getauscht. Zu einem bestimmten Zeitpunkt erzielt das Pooling eine abnehmende Rendite, und Sie können eine ausreichend gute Leistung erzielen und gleichzeitig die mögliche Ressourcennutzung durch eine bestimmte Komponente einschränken.

## <a name="doing-actual-work-or-acquiring-resources"></a>Durchführen tatsächlicher Arbeit oder Abrufen von Ressourcen

Wenn Sie über eine Komponente verfügen, die Clients kurz und in schneller Folge verwenden, wobei ein erheblicher Teil der Objektnutzungszeit für das Abrufen von Ressourcen oder die Initialisierung vor der spezifischen Arbeit für den Client aufgewendet wird, ist es wahrscheinlich, dass das Schreiben Ihrer Komponente zur Verwendung des Objektpoolings ein großer Gewinn für Sie ist.

Sie können die Komponente so schreiben, dass Sie im Konstruktor des Objekts so viel zeitaufwendige Arbeit ausführen, die für alle Clients wie möglich gleich ist: Abrufen einer oder mehrerer Verbindungen, Ausführen von Skripts, Abrufen von Initialisierungsdaten aus Dateien oder über ein Netzwerk usw. Dies hat den Effekt, dass jede solche Ressource in einem Pool zusammengefasst wird. Sie poolen die Kombination aus Ressourcen und dem generischen Zustand, die zum Ausführen einiger Aufgaben erforderlich sind.

Wenn Clients in diesem Fall ein Objekt aus dem Pool erhalten, stehen ihnen diese Ressourcen sofort zur Verfügung. In der Regel verwenden sie das -Objekt, um eine kleine Arbeitseinheit auszuführen, Daten zu pushen oder zu pullen, und dann ruft das Objekt [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) oder [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) auf und gibt zurück. Mit solchen Mustern für schnelles Fire-Fire-Einsatz bietet Pooling hervorragende Leistungsvorteile. Sie können die Einfachheit des zustandslosen automatischen Transaktionsprogrammiermodells voll nutzen und dennoch eine Leistung erzielen, die mit herkömmlichen zustandslosen Komponenten vergleichbar ist.

Wenn Clients jedoch jedes Mal, wenn sie es aufrufen, ein Objekt für lange Zeit verwenden, ist das Pooling weniger sinnvoll. Der Geschwindigkeitsvorteil, den Sie erhalten, ist geringfügig, da die Nutzungszeit relativ zur Initialisierungszeit zunimmt. Sie erhalten abnehmende Rückgaben, die möglicherweise nicht die Kosten des Arbeitsspeichers rechtfertigen, der zum Speichern eines Pools aktiver Objekte erforderlich ist.

## <a name="sharing-cost-across-multiple-clients"></a>Gemeinsame Nutzung von Kosten auf mehrere Clients

Eine Variation bei der Out-Initialisierung besteht darin, dass Sie pooling verwenden können, um die Kosten für den Erwerb teurer Ressourcen statistisch zu amortisieren. Wenn Sie den Treffer für den Erwerb oder die Initialisierung einmal verwenden und dann das Objekt wiederverwenden, teilen Sie diese Kosten für alle Clients, die das Objekt während seiner Lebensdauer verwenden. Eine hohe Konstruktionszeit fällt nur einmal pro Objekt an.

## <a name="preallocating-objects"></a>Vorabverlegung von Objekten

Wenn Sie eine Minimale Poolgröße ungleich 0 (null) angeben, wird diese Mindestanzahl von Objekten erstellt und beim Starten der Anwendung in einem Pool zusammengefasst, der für alle Clients bereit ist, die die Anwendung aufrufen.

## <a name="governing-resource-use-with-pool-management"></a>Verwalten der Ressourcenverwendung mit der Poolverwaltung

Sie können die maximale Poolgröße verwenden, um sehr genau zu steuern, wie Ressourcen verwendet werden. Wenn Sie beispielsweise eine bestimmte Anzahl von Datenbankverbindungen lizenziert haben, können Sie steuern, wie viele Verbindungen Sie jederzeit geöffnet haben.

Wenn Sie Die Clientnutzungsmuster, Objektverwendungsmerkmale und physische Ressourcen wie Arbeitsspeicher und Verbindungen berücksichtigen, werden Sie wahrscheinlich einen optimalen Balancepunkt finden, wenn Sie eine Leistungsoptimierung durchführen. Poolingobjekte führen zu abnehmenden Rückgaben nach einem bestimmten Punkt. Sie können bestimmen, welche Leistungsstufe Sie benötigen, und dies mit den Ressourcen abwägen, die erforderlich sind, um dies zu erreichen.

Um die Leistungsoptimierung beim Konfigurieren des Objektpoolings zu vereinfachen, können Sie Objektstatistiken für die Komponenten in einer Anwendung überwachen. Weitere Informationen finden Sie unter Überwachen von [Objektstatistiken.](monitoring-object-statistics.md)

## <a name="improve-performance-of-jit-activated-components"></a>Verbessern der Leistung von JIT-Activated-Komponenten

Objektpooling funktioniert sehr gut mit dem [COM+-Just-In-Time-Aktivierungsdienst.](com--just-in-time-activation.md) Durch das Pooling von Objekten, die JIT-aktiviert werden, können Sie die Objektreaktivierung beschleunigen. Sie profitieren von den Vorteilen, den Kanal durch JIT-Aktivierung geöffnet zu halten und gleichzeitig die Kosten für die Reaktivierung zu verringern. Sie können pooling in diesem Fall verwenden, um zu steuern, wie viel Arbeitsspeicher Sie Objekten zuordnen möchten, für die Verweise aktiv sind.

Es ist sehr wahrscheinlich, dass Jit-aktivierte Komponenten in einem Pool zusammengefasst werden, wenn sie transaktional sind. Objektpooling ist für die Verarbeitung von Transaktionskomponenten optimiert. Weitere Informationen finden Sie unter [Pooling Transactional Objects](pooling-transactional-objects.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Objektkonstruktorzeichenfolgen](com--object-constructor-strings.md)
</dt> <dt>

[Steuern der Lebensdauer und des Zustands von Objekten](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Funktionsweise von Objektpooling](how-object-pooling-works.md)
</dt> <dt>

[Pooling von Transaktionsobjekten](pooling-transactional-objects.md)
</dt> <dt>

[Anforderungen für poolfähige Objekte](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



