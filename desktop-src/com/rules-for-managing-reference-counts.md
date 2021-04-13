---
title: Regeln für die Verwaltung von Verweis Zählungen
description: Die Verwendung eines Verweis Zählers zum Verwalten der Lebensdauer eines Objekts ermöglicht es mehreren Clients, den Zugriff auf ein einzelnes Objekt zu erhalten und freizugeben, ohne einander bei der Verwaltung der Lebensdauer eines Objekts koordinieren zu müssen.
ms.assetid: bbe7d16c-fcb7-474d-a22d-5a3b33dd800e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9520cbbc88cb73c6e2abbd7908bed3754bb3945
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391046"
---
# <a name="rules-for-managing-reference-counts"></a>Regeln für die Verwaltung von Verweis Zählungen

Die Verwendung eines Verweis Zählers zum Verwalten der Lebensdauer eines Objekts ermöglicht es mehreren Clients, den Zugriff auf ein einzelnes Objekt zu erhalten und freizugeben, ohne einander bei der Verwaltung der Lebensdauer eines Objekts koordinieren zu müssen. Solange das Client Objekt bestimmten Verwendungs Regeln entspricht, stellt das-Objekt diese Verwaltung bereit. Diese Regeln geben an, wie Verweise zwischen Objekten verwaltet werden. (Com gibt keine internen Implementierungen von Objekten an, obwohl diese Regeln einen angemessenen Ausgangspunkt für eine Richtlinie innerhalb eines Objekts sind.)

Konzeptionell können Schnittstellen Zeiger als in Zeiger Variablen befindende betrachtet werden, die den gesamten internen Berechnungs Zustand enthalten, der einen Schnittstellen Zeiger enthält. Dazu zählen Variablen in Speicherpositionen, in internen Prozessor Registern und vom Programmierer generierte und vom Compiler generierte Variablen. Die Zuweisung zu oder Initialisierung einer Zeiger Variablen umfasst das Erstellen einer neuen Kopie eines bereits vorhandenen Zeigers. Wenn eine Kopie des Zeigers in einer Variablen vorhanden war (der Wert, der bei der Zuweisung/Initialisierung verwendet wird), gibt es jetzt zwei. Eine Zuweisung zu einer Zeiger Variablen zerstört die Zeiger Kopie, die aktuell in der Variablen ist, ebenso wie die Zerstörung der Variablen selbst. (Das heißt, der Bereich, in dem die Variable gefunden wird, z. b. der Stapel Rahmen, wird zerstört.)

Aus Sicht eines COM-Clients erfolgt die Verweis Zählung immer für jede Schnittstelle. Clients sollten niemals davon ausgehen, dass ein Objekt den gleichen Gegenstand für alle Schnittstellen verwendet.

Der Standardfall ist, dass [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) für jede neue Kopie eines Schnittstellen Zeigers aufgerufen werden muss und dass die [**Freigabe**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für jede Zerstörung eines Schnittstellen Zeigers aufgerufen werden muss, außer wenn die folgenden Regeln andernfalls zulässig sind:

-   **In-out-Parameter für Funktionen.** Der Aufrufer muss die [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) für den Parameter aufrufen, da er (mit einem Aufruf von [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)) im implementierenden Code freigegeben wird, wenn der Out-Wert darauf gespeichert wird.
-   **Eine globale Variable wird abgerufen.** Wenn Sie eine lokale Kopie eines Schnittstellen Zeigers aus einer vorhandenen Kopie des Zeigers in einer globalen Variablen erstellen, müssen Sie die [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) für die lokale Kopie abrufen, da eine andere Funktion die Kopie in der globalen Variablen zerstören kann, während die lokale Kopie noch gültig ist.
-   **Neue Zeiger, die aus "Thin Air" synthetisiert werden.** Eine Funktion, die einen Schnittstellen Zeiger mithilfe von besonderen internen Kenntnissen synthetisiert, anstatt ihn aus einer anderen Quelle abzurufen, muss zunächst die [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) auf dem neu synthetisierten Zeiger aufrufen. Wichtige Beispiele für derartige Routinen sind Instanzen Erstellungs Routinen, Implementierungen von [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))usw.
-   **Abrufen einer Kopie eines intern gespeicherten Zeigers.** Wenn eine Funktion eine Kopie eines Zeigers abruft, die intern vom Objekt mit dem Namen gespeichert wird, muss der Code dieses Objekts vor der Rückgabe der Funktion [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) für den Zeiger aufrufen. Nachdem der Zeiger abgerufen wurde, bietet das Ursprungs Objekt keine andere Möglichkeit, zu bestimmen, wie seine Lebensdauer mit der der intern gespeicherten Kopie des Zeigers zusammenhängt.

Die einzige Ausnahme für den Standardfall ist, dass der Verwaltungs Code die Beziehungen zwischen den Lebens dauern von mindestens zwei Kopien eines Zeigers auf die gleiche Schnittstelle in einem Objekt kennt und einfach sicherstellt, dass das Objekt nicht zerstört wird, indem der Verweis Zähler auf 0 (null) zurückgesetzt wird. Im Allgemeinen gibt es zwei Fälle:

-   Wenn eine Kopie eines Zeigers bereits vorhanden ist und anschließend eine zweite Kopie erstellt und dann zerstört wird, während die erste Kopie noch vorhanden ist, können Aufrufe von [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)für die zweite Kopie ausgelassen werden.
-   Wenn eine Kopie eines Zeigers vorhanden ist und ein zweiter erstellt wird und der erste Vorgang vor dem zweiten zerstört wird, können die Aufrufe von [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)für die zweite Kopie und die [**Freigabe**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für die erste Kopie ausgelassen werden.

Im folgenden finden Sie spezifische Beispiele für diese Situationen: die ersten beiden sind besonders häufig.

-   **In den Parametern für Funktionen.** Die Lebensdauer der Kopie eines Schnittstellen Zeigers, der als Parameter an eine Funktion übergeben wird, wird in der des Zeigers, der zum Initialisieren des Werts verwendet wird, eingefügt, sodass für den Parameter kein separater Verweis Zähler erforderlich ist.
-   **Out-Parameter aus Funktionen, einschließlich der Rückgabewerte.** Um den out-Parameter festzulegen, muss die Funktion über eine stabile Kopie des Schnittstellen Zeigers verfügen. Bei der Rückgabe ist der Aufrufer für die Freigabe des Zeigers verantwortlich. Der Out-Parameter benötigt daher keinen separaten Verweis Zähler.
-   **Lokale Variablen.** Eine Methoden Implementierung hat die Kontrolle über die Lebensdauer der einzelnen Zeiger Variablen, die im Stapel Rahmen zugeordnet sind, und kann dies verwenden, um zu bestimmen, wie redundante [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)- / [**releasepaare**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) ausgelassen werden.
-   **Backpointer.** Einige Datenstrukturen enthalten zwei-Objekte, von denen jeder einen Zeiger auf den anderen hat. Wenn die Lebensdauer des ersten Objekts bekannt ist, dass die Lebensdauer des zweiten Objekts enthalten ist, ist es nicht erforderlich, einen Verweis Zähler für den Zeiger des zweiten Objekts auf das erste Objekt zu haben. Häufig ist es wichtig, diesen Schleifen zu vermeiden, wenn das entsprechende Verhalten beim Aufheben der Zuordnung beibehalten wird. Nicht abgezählte Zeiger sollten jedoch mit äußerster Vorsicht verwendet werden, da der Teil des Betriebssystems, der die Remote Verarbeitung verarbeitet, keine Möglichkeit hat, über diese Beziehung zu informieren. Daher ist in fast allen Fällen, dass der Rück Zeiger ein zweites, "Friend"-Objekt des ersten Zeigers (wodurch die Zirkularität vermieden wird) die bevorzugte Lösung. Beispielsweise verwendet die Verbindungs fähigen Objects-Architektur von com diese Vorgehensweise.

Beim implementieren oder Verwenden von Objekten mit Verweis Zählung kann es hilfreich sein, *künstliche Verweis Zähler* anzuwenden, die die Objekt Stabilität während der Verarbeitung einer Funktion garantieren. Beim Implementieren einer Methode einer Schnittstelle können Sie Funktionen aufzurufen, die die Möglichkeit haben, den Verweis Zähler auf ein Objekt zu dekrementieren, wodurch eine Vorzeitige Freigabe des Objekts und ein Fehler der Implementierung verursacht wird. Ein robuster Weg, dies zu vermeiden, besteht darin, am Anfang der Methoden Implementierung einen [**callf-Adressaten**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) einzufügen und ihn mit einem [**Freigabe Freigabe**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) paar kurz vor der Rückgabe der Methode zu koppeln.

In einigen Situationen sind die Rückgabewerte von [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) möglicherweise instabil und sollten nicht darauf basieren. Sie sollten nur zu Debuggingzwecken oder zu Diagnose Zwecken verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten von Objekt Lebensdauern durch Verweis Zählung](managing-object-lifetimes-through-reference-counting.md)
</dt> </dl>

 

 