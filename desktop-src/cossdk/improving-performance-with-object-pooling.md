---
description: Verbessern der Leistung durch Objekt Pooling
ms.assetid: 7a8a38d8-6549-4686-a298-f3b427b380e3
title: Verbessern der Leistung durch Objekt Pooling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398b9140080d3a439293b5152b4da7251978e800
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338912"
---
# <a name="improving-performance-with-object-pooling"></a>Verbessern der Leistung durch Objekt Pooling

Das Objekt Pooling kann unter bestimmten Umständen äußerst effektiv sein, was zu einer erheblichen Leistungssteigerung bei der Leistung. Die allgemeine Idee für die Wiederverwendung von Objekten, die am besten genutzt werden sollten, besteht darin, so viele Ressourcen wie möglich zu bündeln, die Initialisierung von der eigentlichen ausgeführten Arbeit zu gestalten und dann die Pool Merkmale zum Zeitpunkt der Bereitstellung administrativ an die tatsächliche Hardware anzupassen. Das heißt, Sie sollten gemäß den folgenden Schritten fortfahren:

1.  Schreiben Sie das-Objekt, um die teure Initialisierung und Ressourcen Erfassung zu berücksichtigen, die für jeden Client als Voraussetzung für die tatsächliche Arbeit im Auftrag des Clients ausgeführt wird. Schreiben Sie große Objektkonstruktoren, um so viele Ressourcen wie möglich zu bündeln, damit diese vom Objekt aufbewahrt werden und sofort verfügbar sind, wenn Clients ein Objekt aus dem Pool erhalten.
2.  Konfigurieren Sie den Pool administrativ, um das beste Gleichgewicht in verfügbaren Hardware Ressourcen zu erzielen. verwenden Sie in der Regel den Arbeitsspeicher, der für die Verwaltung eines Pools mit einer bestimmten Größe in Exchange reserviert ist, um den Client Zugriff zu beschleunigen und An einem bestimmten Punkt erzielt das Pooling abnehmende Rückgaben, und Sie können eine gute Leistung erzielen, während Sie mögliche Ressourcennutzung durch eine bestimmte Komponente begrenzen.

## <a name="doing-actual-work-or-acquiring-resources"></a>Tatsächliche Arbeit oder Ressourcenbeschaffung

Wenn Sie über eine-Komponente verfügen, die von Clients kurz und in schneller Folge verwendet wird, in der ein erheblicher Teil der Objekt Verwendung für den Ressourcen Abruf oder die Initialisierung aufgewendet wird, bevor bestimmte Aufgaben für den Client ausgeführt werden, ist es wahrscheinlich, dass das Schreiben der Komponente zur Verwendung von Objekt Pooling ein großer Gewinn ist.

Sie können die Komponente so schreiben, dass Sie im Konstruktor des Objekts den zeitaufwändigen Arbeitsaufwand ausführen, der für alle Clients möglichst einheitlich ist – das Abrufen von einer oder mehreren Verbindungen, das Ausführen von Skripts, das Abrufen von Initialisierungs Daten aus Dateien oder über ein Netzwerk usw. Dies hat Auswirkungen auf das Pooling der einzelnen Ressourcen. Sie bündeln die Kombination von Ressourcen und dem generischen Zustand, der für die Durchführung einiger Aufgaben erforderlich ist.

Wenn Clients ein Objekt aus dem Pool erhalten, sind diese Ressourcen in dieser Situation sofort verfügbar. Normalerweise verwenden Sie das-Objekt, um eine kleine Arbeitseinheit auszuführen, Daten zu übertragen oder zu übertragen. Anschließend ruft das Objekt [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) oder [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) auf und gibt zurück. Mit schnell Feuer-Verwendungs Mustern wie diesem führt das Pooling zu hervorragenden Leistungsvorteilen. Sie können die Einfachheit des Zustands losen automatischen Transaktions Programmierungs Modells voll ausschöpfen und gleichzeitig die Leistung der herkömmlichen Zustands behafteten Komponenten steigern.

Wenn Clients jedoch für einen längeren Zeitraum ein Objekt verwenden, wird das Pooling weniger sinnvoll. Der Geschwindigkeitsvorteil, den Sie gewinnen, ist marginal, da die Anwendungszeit relativ zur Initialisierungs Zeit zunimmt. Sie erhalten abnehmende Rückgaben, die möglicherweise nicht die Kosten für den Arbeitsspeicher rechtfertigen, der zum Speichern eines Pools aktiver Objekte erforderlich ist.

## <a name="sharing-cost-across-multiple-clients"></a>Gemeinsame Nutzung von Kosten über mehrere Clients

Eine Variation bei der Umgestaltung der Initialisierung besteht darin, dass Sie das Pooling verwenden können, um die Kosten für den Erwerb kostspieliger Ressourcen statistisch amortisieren. Wenn Sie die Übernahme oder Initialisierung einmal durchführen und dann das Objekt wieder verwenden, teilen Sie diese Kosten für alle Clients, die das Objekt während ihrer Lebensdauer verwenden. Hohe Konstruktions Dauer wird nur einmal pro Objekt anfallen.

## <a name="preallocating-objects"></a>Vorab zuordnen von Objekten

Wenn Sie eine minimale Poolgröße ungleich NULL angeben, wird diese Mindestanzahl von Objekten erstellt und in einem Pool zusammengefasst, wenn die Anwendung gestartet wird. Dies ist für alle Clients bereit, die in der Anwendung aufgerufen werden.

## <a name="governing-resource-use-with-pool-management"></a>Steuern der Ressourcenverwendung mit der Pool Verwaltung

Sie können die maximale Poolgröße verwenden, um genau zu steuern, wie Sie Ressourcen verwenden. Wenn Sie z. b. eine bestimmte Anzahl von Datenbankverbindungen lizenziert haben, können Sie steuern, wie viele Verbindungen Sie jederzeit geöffnet haben.

Wenn Sie die Client Verwendungs Muster, Objekt Verwendungs Merkmale und physische Ressourcen wie z. b. Arbeitsspeicher und Verbindungen berücksichtigen, werden Sie bei der Leistungsoptimierung wahrscheinlich einen optimalen Saldo erzielen. Beim Pooling von Objekten ergeben sich nach einem bestimmten Punkt abnehmende Rückgaben. Sie können bestimmen, welche Leistungsstufe Sie benötigen, und wie Sie die Ressourcen abwägen, die für die Erreichung erforderlich sind.

Um die Leistungsoptimierung beim Konfigurieren des Objekt Pooling zu vereinfachen, können Sie Objekt Statistiken für die Komponenten in einer Anwendung überwachen. Weitere Informationen finden Sie unter über [Wachen von Objekt Statistiken](monitoring-object-statistics.md).

## <a name="improve-performance-of-jit-activated-components"></a>Verbessern der Leistung von JIT-Activated-Komponenten

Das Objekt Pooling funktioniert sehr gut mit dem [Just-in-Time-Aktivierungs Dienst von com+](com--just-in-time-activation.md) . Durch das Pooling von Objekten, die JIT-aktiviert sind, können Sie die Objekt Reaktivierung beschleunigen. Sie profitieren von den Vorteilen, dass der Kanal durch die JIT-Aktivierung geöffnet ist und gleichzeitig die Kosten der erneuten Aktivierung verringert werden. In diesem Fall können Sie das Pooling verwenden, um zu steuern, wie viel Arbeitsspeicher Sie Objekten zuordnen möchten, die über Verweise verfügen.

Es ist höchstwahrscheinlich, dass JIT-aktivierte Komponenten gebündelt werden, wenn diese transaktional sind. Das Objekt Pooling ist für die Verarbeitung von Transaktions Komponenten optimiert. Weitere Informationen finden Sie unter [Pooling von transaktionalen Objekten](pooling-transactional-objects.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-objektkonstruktorzeichenfolgen](com--object-constructor-strings.md)
</dt> <dt>

[Steuern der Objekt Lebensdauer und des Zustands](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Funktionsweise des Objekt Pooling](how-object-pooling-works.md)
</dt> <dt>

[Pooling von transaktionalen Objekten](pooling-transactional-objects.md)
</dt> <dt>

[Anforderungen für in einem Pool Bare Objekte](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



