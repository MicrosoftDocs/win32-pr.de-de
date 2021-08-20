---
title: Windows Übersicht über Animationen
description: Diese Übersicht bietet eine Einführung in den Windows Animation Manager und konzentriert sich auf wichtige Komponenten und Konzepte.
ms.assetid: de1380c9-6801-4178-9281-a23af7d71d77
keywords:
- Windows Animation Windows Animation , Übersicht
- Animation Manager-Objekte Windows Animation , beschrieben
- Animationsvariablen Windows Animation beschrieben
- Animation timer objects Windows Animation , beschrieben
- Zeitsteuerungssystem Windows Animation
- Kontextabhängige Dauer Windows Animation
- Geschwindigkeitsabgleich Windows Animation
- Contention Management Windows Animation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc0892cffa3e79428e19cbe5b1a3c27d7abda62365c4ceb15731101aa857f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348005"
---
# <a name="windows-animation-overview"></a>Windows Übersicht über Animationen

Diese Übersicht bietet eine Einführung in den Windows Animation Manager und konzentriert sich auf wichtige Komponenten und Konzepte. Weitere Informationen zu Storyboards und Übergängen finden Sie unter [Übersicht über Storyboards.](storyboard-construction.md)

Dieses Thema enthält folgende Abschnitte:

-   [Grundlegende Konzepte](#basic-concepts)
-   [Komponenten der Windows Animation](#components-of-windows-animation)
-   [Die Windows-Animations-API](#the-windows-animation-api)
-   [Konfigurationen](#configurations)
    -   [Anwendungsgesteuerte Animation](#application-driven-animation)
    -   [Zeitgebergesteuerte Animation](#timer-driven-animation)
-   [Erweiterte Features](#advanced-features)
    -   [Contention Management](#contention-management)
-   [Zugehörige Themen](#related-topics)

## <a name="basic-concepts"></a>Grundlegende Konzepte

*Animation* ist eine Sequenz aufeinander folgender Stillbilder, die eine Wiedergabe der Bewegung erzeugt. Die Verwendung interaktiver Animationen auf der Benutzeroberfläche kann einer Anwendung eine einzigartige Persönlichkeit verleihen und die Benutzerfreundlichkeit verbessern. Animationen können dabei helfen, wichtige Zustandsänderungen auf der Benutzeroberfläche zu kommunizieren und die Komplexität der Benutzeroberfläche zu verwalten. Animationen können auch die Wahrnehmung der Qualität einer Anwendung durch den Benutzer verbessern.

Als Beispiele wird Windows Animation in der Taskleiste verwendet, um Sie beim Verwalten von Dateien und Programmen zu unterstützen und darauf zuzugreifen, und Bildschirmlupe, um verschiedene Teile des Bildschirms zu vergrößern, damit sie benutzern leichter angezeigt werden können.

Die grundlegenden Einheiten einer Animation sind das Merkmal eines visuellen Elements, das animiert werden soll, und die Beschreibung, wie sich dieses Merkmal im Laufe der Zeit ändert. Eine Anwendung kann eine Vielzahl von Merkmalen animieren, z. B. Position, Farbe, Größe, Drehung, Kontrast und Deckkraft.

In Windows Animation stellt eine *Animationsvariable* das zu animierende Merkmal dar. Ein *Übergang* beschreibt, wie sich der Wert dieser Animationsvariablen ändert, wenn die Animation auftritt. Beispielsweise kann ein visuelles Element über eine Animationsvariable verfügen, die seine Deckkraft angibt, und eine Benutzeraktion generiert möglicherweise einen Übergang, der diese Deckkraft von einem Wert von 50 zu 100 übernimmt, der eine Animation von halbtransparent zu vollständig deckend darstellt.

Ein *Storyboard* ist ein Satz von Übergängen, die im Laufe der Zeit auf eine oder mehrere Animationsvariablen angewendet werden. Eine Anwendung zeigt Animationen an, indem Storyboards erstellt und wiedergegeben und dann Sequenzen diskreter Frames gezeichnet werden, wenn sich die Werte von Animationsvariablen im Laufe der Zeit ändern.

## <a name="components-of-windows-animation"></a>Komponenten der Windows Animation

Windows Animation besteht aus den folgenden Komponenten:

<dl> <dt>

<span id="animation_manager"></span><span id="ANIMATION_MANAGER"></span>Animations-Manager
</dt> <dd>

Anwendungen verwenden ein Animations-Manager-Objekt, um Animationsvariablen und Storyboards zu erstellen, Animationen zu planen und zu steuern und Zustandsinformationen zu aktualisieren, bevor die Anwendung jeden Frame zeichnet. Ein einzelnes Animations-Manager-Objekt verwaltet in der Regel alle Animationen in einer Anwendung und hat daher globale Kontrolle über alle geplanten Storyboards.

</dd> <dt>

<span id="animation_variables"></span><span id="ANIMATION_VARIABLES"></span>Animationsvariablen
</dt> <dd>

Vor dem Starten von Animationen muss eine Anwendung Animationsvariablenobjekte erstellen. Eine Animationsvariable stellt einen Aspekt eines visuellen Elements dar, das animiert werden soll. Die Variable ist ein skalarer Gleitkommawert, obwohl der Wert auf einen ganzzahligen Wert gerundet werden kann.

Eine Animationsvariable hat in der Regel die gleiche Lebensdauer wie das visuelle Element, das sie animieren soll. Der Anfangswert einer Animationsvariablen wird angegeben, wenn die Variable erstellt wird. Danach kann der Wert nicht direkt geändert werden. Sie muss über den Animations-Manager aktualisiert werden.

Eine Animationsvariable kann durch ein *Tag* identifiziert werden, bei dem es sich um eine Kopplung eines ganzzahligen Bezeichners mit einem Zeiger auf ein COM-Objekt handelt. Ein Tag muss nicht eindeutig sein, es sei denn, die Anwendung verwendet es, um nach einer Variablen zu suchen. Standardmäßig verfügt eine Animationsvariable nicht über ein Tag, und alle Versuche, ihr Tag zu lesen, schlagen fehl, bis ein Tag festgelegt wurde.

</dd> <dt>

<span id="timing_system"></span><span id="TIMING_SYSTEM"></span>Zeitsteuerungssystem
</dt> <dd>

Windows Animation umfasst ein Zeitsteuerungssystem, mit dem sichergestellt wird, dass Animationen mit einer gleichmäßigen und konsistenten Bildfrequenz gerendert werden, während gleichzeitig die Verwendung von Systemressourcen für das Rendering reduziert wird, wenn das System ausgelastet ist. Ein *Timer* hilft bei der Verwaltung des Animationsrenderings, indem er automatisch den Durchlauf einer kleinen Zeiteinheit angibt, die als *Teilstrich* bezeichnet wird. Das Zeitsteuerungssystem überwacht die Gesamtleistung des Systemrenderings und *drosselt* Animationen durch dynamisches Erhöhen oder Verringern der Takthäufigkeit. Anwendungen können mit einem Timer den Animations-Manager steuern und einen Handler registrieren, um benachrichtigt zu werden, bevor und nachdem der Manager für jeden Tick aktualisiert wurde. Anwendungen können die minimal zulässige Animationsrahmenrate für einen Timer angeben und benachrichtigt werden, wenn die tatsächliche Bildrate einer Animation unter diese Rate fällt.

Um Systemressourcen zu sparen, kann ein Timer so konfiguriert werden, dass er sich selbst deaktiviert, wenn keine Animation stattfindet.

</dd> </dl>

## <a name="the-windows-animation-api"></a>Die Windows-Animations-API

Die Windows Animation-API ist eine COM-basierte Singlethread-API, die Entwicklern die folgenden Features bietet:

-   Ein Animations-Manager-Objekt, [**UIAnimationManager,**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))zum Erstellen von Animationsobjekten und Steuern von Animationen
-   Animationsvariablen und Storyboards
-   Eine grundlegende Bibliothek, [**UIAnimationTransitionLibrary,**](/previous-versions/windows/desktop/legacy/dd317028(v=vs.85))mit einsatzbereiten Übergängen
-   Ein Timerobjekt, [**UIAnimationTimer,**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))zum Bestimmen der aktuellen Zeit und optional zum Ausführen von Animationen.
-   Ereignishooks zum Überwachen des Zustands und Fortschritts der Animation

Die vollständige API-Referenz finden Sie unter [Windows Animationsreferenz.](windows-animation-reference.md) Beispielcode finden Sie unter [Windows Animation Tasks](using-windows-animation.md) and Windows Animation [Samples](windows-animation-samples.md).

## <a name="configurations"></a>Konfigurationen

Anwendungen müssen die aktuelle Zeit abrufen, bevor sie eine neue Animation planen. Im Folgenden sind die Zeitsteuerungsmechanismen angegeben, die von Windows Animation unterstützt werden:

-   [Anwendungsgesteuerte Animation](#application-driven-animation)
-   [Zeitgebergesteuerte Animation](#timer-driven-animation)

### <a name="application-driven-animation"></a>Application-Driven Animation

Anwendungen, die eine hardwarebeschleunigte Grafik-API verwenden, können mit der Aktualisierungsrate des Monitors synchronisiert werden, um reibungslose Animationen zu rendern. Alternativ kann eine Anwendung einen eigenen Zeitsteuerungsmechanismus verwenden, um zu bestimmen, wann jeder Frame einer Animation gezeichnet werden soll. In beiden Fällen teilt die Anwendung dem Animations-Manager mit, wann der Zustand aktualisiert werden soll. Ein Animationstimer kann weiterhin verwendet werden, um die aktuelle Zeit mit hoher Genauigkeit in den vom Animations-Manager benötigten Einheiten zu bestimmen.

Das folgende Diagramm zeigt die Interaktionen zwischen einer Anwendung und den Windows Animationskomponenten, wenn die Anwendung Animationsupdates direkt antreibt.

![Diagramm, das die Interaktionen zwischen einer Anwendung und den Windows-Animationskomponenten zeigt, wenn die Anwendung Animationsupdates direkt antreibt.](images/animationupdates.png)

In der einfachsten Konfiguration zeichnet eine Anwendung jedes Mal, wenn der Bildschirm aktualisiert wird, alles neu, auch wenn keine Animationen wiedergegeben werden. Um unnötige Arbeit zu vermeiden, kann eine Anwendung einen Managerereignishandler registrieren, um benachrichtigt zu werden, wenn Animationen geplant sind, und erkennen, wann der Zeitplan leer ist, sodass das Neuzeichnen beendet werden kann.

### <a name="timer-driven-animation"></a>Timer-Driven Animation

Anstatt den Animations-Manager direkt zu aktualisieren, können Anwendungen den Animationszeitgeber dem Animations-Manager mitteilen, wann er seinen Zustand aktualisieren soll, und einfach benachrichtigt werden, wenn jedes Update durchgeführt wurde. Dieser Ansatz wird für ältere Grafik-APIs empfohlen. Wenn eine Synchronisierung mit der Aktualisierungsrate des Monitors möglich ist, ist es im Allgemeinen besser, dies zu tun und anwendungsgesteuerte Animationen zu verwenden.

Das folgende Diagramm zeigt die Interaktionen zwischen einer Anwendung und den Windows Animationskomponenten, wenn der Animationszeitgeber Animationsupdates antreibt.

![Diagramm, das die Interaktionen zwischen einer Anwendung und den Windows-Animationskomponenten zeigt, wenn der Animationszeitgeber Animationsupdates antreibt.](images/animationtimerupdates.png)

Der Timer kann so konfiguriert werden, dass er nur ausgeführt wird, wenn die Animationen geplant sind. Dies ist eine einfache Frage der Übergabe eines bestimmten Parameters, wenn der Timer und der Animations-Manager verbunden sind.

## <a name="advanced-features"></a>Erweiterte Funktionen

Neben einer grundlegenden Grundlage für die Unterstützung von Animationen umfasst Windows Animation unterstützung für verschiedene erweiterte Animationstechniken, einschließlich:

<dl> <dt>

<span id="context-sensitive_duration"></span><span id="CONTEXT-SENSITIVE_DURATION"></span>*Kontextabhängige Dauer*
</dt> <dd>

Die Dauer eines Übergangs muss nicht festgelegt werden. Sie kann basierend auf dem Wert und der Geschwindigkeit der animierten Variablen bestimmt werden, wenn der Übergang beginnt.

</dd> <dt>

<span id="velocity_matching"></span><span id="VELOCITY_MATCHING"></span>*Geschwindigkeitsabgleich*
</dt> <dd>

Die Bewegung ist in der Regel für das Auge anfälliger, wenn die Position und Geschwindigkeit eines bewegten Objekts nicht sofort zwischen den Werten springen. Wenn ein neues Storyboard unterbrochen wird, das gerade wiedergegeben wird, ermöglicht der Geschwindigkeitsabgleich, dass das neue Storyboard problemlos an der Stelle, an der das vorherige Storyboard beendet wurde, aufgenommen wird.

</dd> <dt>

<span id="contention_management"></span><span id="CONTENTION_MANAGEMENT"></span>*Contention Management*
</dt> <dd>

Wenn zwei Storyboards dieselbe Animationsvariable gleichzeitig aktualisieren müssen, tritt ein Planungskonflikt auf. Anstatt eine bestimmte numerische Priorität für jedes Storyboard zu erfordern, ermöglicht Windows Animation der Anwendung, die relativen Prioritäten von zwei Storyboards zu bestimmen.

</dd> </dl>

### <a name="contention-management"></a>Contention Management

Entwickler können einen *Prioritätsvergleichsrückruf* implementieren, um die Priorität des geplanten Storyboards und des Storyboards zu vergleichen, das sich bereits im Zeitplan befindet. Eine Anwendung, die einen Prioritätsvergleich implementiert, kann eine beliebige bevorzugte Logik verwenden, um zu bestimmen, wann ein Storyboard einem anderen voransetzt. Um den Planungskonflikt zu beheben, fragt Windows Animation die Anwendung, welche dieser Aktionen in der folgenden Reihenfolge ausgeführt werden können:

-   **Brechen Sie das geplante Storyboard ab.** Wenn die Wiedergabe des geplanten Storyboards noch nicht gestartet wurde, wird es möglicherweise abgebrochen und sofort aus dem Zeitplan entfernt.
-   **Kürzen Sie das geplante Storyboard.** Wenn ein neues Storyboard ein geplantes Storyboard kürzet, wird das geplante Storyboard die Variable nicht mehr beeinflussen, sobald das neue Storyboard damit beginnt, es zu animieren. Die Geschwindigkeiten werden abgeglichen, sodass das neue Storyboard problemlos an der Stelle, an der das vorherige Storyboard aufgehört hat, aufgenommen werden kann.
-   **Schließen Sie das geplante Storyboard ab.** Ein Storyboard kann nur dann abgeschlossen werden, wenn es eine Schleife enthält, die unbegrenzt wiederholt wird. Wenn sich das Storyboard nach Abschluss in einer solchen Schleife befindet, wird die aktuelle Wiederholung abgeschlossen, und der Rest des Storyboards wird dann wiedergegeben. Wenn die Schleife beim Abschluss eines Storyboards noch nicht begonnen hat, wird die Schleife vollständig übersprungen.
-   **Komprimieren Sie das geplante Storyboard.** Wenn das Kürzen oder Abbrechen des geplanten Storyboards keine Option ist, kann das Storyboard abgeschlossen werden. Windows Animation bietet die Möglichkeit, die für das geplante Storyboard (und alle zuvor geplanten Storyboards) verfügbare Zeit zu komprimieren, sodass die Variablen schneller ihren endgültigen Zustand erreichen. Wenn die Komprimierung angewendet wird, wird die Zeit für betroffene Storyboards vorübergehend beschleunigt, sodass sie schneller wiedergegeben werden.

Wenn keine der oben genannten Aktionen von den registrierten Prioritätsvergleichsobjekten zugelassen wird, schlägt der Versuch fehl, das neue Storyboard zu planen. Standardmäßig können alle Storyboards gekürzt, abgeschlossen oder komprimiert werden, um Fehler zu verhindern, aber keine können abgebrochen werden.

Das folgende Diagramm zeigt den Lebenszyklus eines Storyboards unter Verwendung der Durch die [**ANIMATION \_ \_ STORYBOARD \_ STATUS-Enumeration**](/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status) der Benutzeroberfläche definierten Zustände. Anwendungen verwenden die Windows Animation-API, um ein Storyboard zu erstellen und zur Planung zu übermitteln. Der Animations-Manager plant das Storyboard und verwaltet die Animation.

![Diagramm, das zeigt, wie der Animations-Manager das Storyboard plant und die Animation verwaltet.](images/statediagram.png)

Weitere Informationen zur Planung und Verwaltung von Storyboards finden Sie unter [Übersicht über Storyboards.](storyboard-construction.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Referenz zu Animationen](windows-animation-reference.md)
</dt> <dt>

[Windows Animationsbeispiele](windows-animation-samples.md)
</dt> <dt>

[Windows Animationsaufgaben](using-windows-animation.md)
</dt> </dl>

 

 