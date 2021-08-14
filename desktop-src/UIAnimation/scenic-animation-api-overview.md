---
title: Windows Übersicht über Animationen
description: Diese Übersicht bietet eine Einführung in den animations Windows-Manager und konzentriert sich auf wichtige Komponenten und Konzepte.
ms.assetid: de1380c9-6801-4178-9281-a23af7d71d77
keywords:
- Windows Animation Windows Animation , Übersicht
- Animation Manager-Objekte Windows Animation , beschrieben
- Animationsvariablen Windows Animation , beschrieben
- Animation timer objects Windows Animation ,described
- Systemsteuerungs-Windows Animation
- kontextsensitive Dauer Windows Animation
- Geschwindigkeitsabgleich Windows Animation
- Animation für die Windows-Verwaltung
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

Diese Übersicht bietet eine Einführung in den animations Windows-Manager und konzentriert sich auf wichtige Komponenten und Konzepte. Weitere Informationen zu Storyboards und Übergängen finden Sie unter [Übersicht über Storyboards.](storyboard-construction.md)

Dieses Thema enthält folgende Abschnitte:

-   [Grundlegende Konzepte](#basic-concepts)
-   [Komponenten der Windows Animation](#components-of-windows-animation)
-   [Die Windows-Animations-API](#the-windows-animation-api)
-   [Konfigurationen](#configurations)
    -   [Anwendungsgesteuerte Animation](#application-driven-animation)
    -   [Timergesteuerte Animation](#timer-driven-animation)
-   [Erweiterte Funktionen](#advanced-features)
    -   [Contention Management](#contention-management)
-   [Zugehörige Themen](#related-topics)

## <a name="basic-concepts"></a>Grundlegende Konzepte

*Animation* ist eine Sequenz von aufeinander folgenden Stillbildern, die eine Bewegung erzeugen, wenn sie wiedergeben wird. Die Verwendung interaktiver Animationen in der Benutzeroberfläche kann einer Anwendung eine einzigartige Persönlichkeit verleihen und die Benutzerfreundlichkeit verbessern. Animationen können dabei helfen, wichtige Zustandsänderungen in der Benutzeroberfläche zu kommunizieren und die Komplexität der Benutzeroberfläche zu verwalten. Animationen können auch die Wahrnehmung der Qualität einer Anwendung durch den Benutzer verbessern.

Als Beispiel wird Windows Animation in der Taskleiste verwendet, um Dateien und Programme zu verwalten und darauf zu zugreifen, und die Bildschirmlupe, um verschiedene Teile des Bildschirms zu vergrößern, damit sie für Benutzer leichter angezeigt werden können.

Die grundlegenden Einheiten einer Animation sind das Merkmal eines animierten visuellen Elements und die Beschreibung, wie sich dieses Merkmal im Laufe der Zeit ändert. Eine Anwendung kann eine Vielzahl von Merkmalen animieren, z. B. Position, Farbe, Größe, Drehung, Kontrast und Deckkraft.

In Windows Animation stellt eine *Animationsvariable* das animierte Merkmal dar. Ein *Übergang* beschreibt, wie sich der Wert dieser Animationsvariablen ändert, wenn eine Animation auftritt. Beispielsweise kann ein visuelles Element über eine Animationsvariable verfügen, die seine Deckkraft angibt, und eine Benutzeraktion kann einen Übergang generieren, der diese Deckkraft von einem Wert von 50 bis 100 übernimmt, der eine Animation von halbtransparent zu vollständig deckend darstellt.

Ein *Storyboard* ist ein Satz von Übergängen, die im Laufe der Zeit auf eine oder mehrere Animationsvariablen angewendet werden. Eine Anwendung zeigt Animationen an, indem storyboards erstellt und abspielt und dann Sequenzen von diskreten Frames gezeichnen werden, wenn sich die Werte von Animationsvariablen im Laufe der Zeit ändern.

## <a name="components-of-windows-animation"></a>Komponenten der Windows Animation

Windows Die Animation besteht aus den folgenden Komponenten:

<dl> <dt>

<span id="animation_manager"></span><span id="ANIMATION_MANAGER"></span>Animations-Manager
</dt> <dd>

Anwendungen verwenden ein Animations-Manager-Objekt, um Animationsvariablen und Storyboards zu erstellen, Animationen zu planen und zu steuern und Statusinformationen zu aktualisieren, bevor die Anwendung jeden Frame zeichnet. Ein einzelnes Animations-Manager-Objekt verwaltet in der Regel alle Animationen in einer Anwendung und hat daher globale Kontrolle über alle geplanten Storyboards.

</dd> <dt>

<span id="animation_variables"></span><span id="ANIMATION_VARIABLES"></span>Animationsvariablen
</dt> <dd>

Vor dem Starten von Animationen muss eine Anwendung Animationsvariablenobjekte erstellen. Eine Animationsvariable stellt einen Aspekt eines visuellen Elements dar, das animiert werden soll. Die Variable ist ein skalarer Gleitkommawert, obwohl der Wert auf einen ganzzahligen Wert gerundet werden kann.

Eine Animationsvariable hat in der Regel die gleiche Lebensdauer wie das visuelle Element, das sie animieren soll. Der Anfangswert einer Animationsvariablen wird angegeben, wenn die Variable erstellt wird. Danach kann der Wert nicht direkt geändert werden. Sie muss über den Animations-Manager aktualisiert werden.

Eine Animationsvariable kann durch ein Tag identifiziert *werden,* bei dem es sich um eine Kopplung eines ganzzahligen Bezeichners mit einem Zeiger auf ein COM-Objekt handelt. Ein Tag muss nicht eindeutig sein, es sei denn, die Anwendung verwendet es, um nach einer Variablen zu suchen. Standardmäßig verfügt eine Animationsvariable nicht über ein -Tag, und alle Versuche, ihr Tag zu lesen, sind erst dann fehlgeschlagen, wenn eines festgelegt wurde.

</dd> <dt>

<span id="timing_system"></span><span id="TIMING_SYSTEM"></span>Zeitsteuerungssystem
</dt> <dd>

Windows Animationen umfassen ein Zeitsteuerungssystem, mit dem sichergestellt werden kann, dass Animationen mit einer gleichmäßigen und konsistenten Bildfrequenz gerendert werden, während gleichzeitig die Verwendung von Systemressourcen für das Rendering reduziert wird, wenn das System ausgelastet ist. Ein *Timer hilft* bei der Verwaltung des Animationsrenderings, indem er automatisch den Lauf einer kleinen Zeiteinheit angibt, die als Teilstrich *bezeichnet wird.* Das Zeitsteuerungssystem überwacht die  gesamte Systemrenderingleistung und drosselt Animationen, indem die Häufigkeit von Ticks dynamisch erhöht oder verringert wird. Anwendungen können es einem Timer ermöglichen, den Animations-Manager zu fahren, und einen Handler registrieren, um benachrichtigt zu werden, bevor und nachdem der Manager für jeden Tick aktualisiert wurde. Anwendungen können die minimale zulässige Animationsbildrate für einen Timer angeben und benachrichtigt werden, wenn die tatsächliche Bildfrequenz einer Animation unter diese Rate fällt.

Um Systemressourcen zu sparen, kann ein Timer so konfiguriert werden, dass er sich selbst deaktiviert, wenn keine Animation stattfindet.

</dd> </dl>

## <a name="the-windows-animation-api"></a>Die Windows-Animations-API

Die Windows-Animations-API ist eine COM-basierte Singlethread-API, die die folgenden Features für Entwickler bietet:

-   Ein Animations-Manager-Objekt, [**UIAnimationManager,**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))zum Erstellen von Animationsobjekten und Steuern von Animationen
-   Animationsvariablen und Storyboards
-   Eine grundlegende Bibliothek, [**UIAnimationTransitionLibrary,**](/previous-versions/windows/desktop/legacy/dd317028(v=vs.85))mit sofort einsatzbereiten Übergängen
-   Ein Timerobjekt, [**UIAnimationTimer,**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))zum Bestimmen der aktuellen Zeit und optional zum Fahren von Animationen
-   Ereignishooks zum Überwachen des Zustands und Fortschritts der Animation

Die vollständige API-Referenz finden Sie unter [Windows Animationsreferenz.](windows-animation-reference.md) Beispielcode finden Sie unter [Windows Animation Tasks (Animationsaufgaben)](using-windows-animation.md) [und Windows Animation Samples (Beispiele für Animationen).](windows-animation-samples.md)

## <a name="configurations"></a>Configurations

Anwendungen müssen die aktuelle Zeit erhalten, bevor sie eine neue Animation planen. Im Folgenden finden Sie die von der Animation Windows Zeitsteuerungsmechanismen:

-   [Anwendungsgesteuerte Animation](#application-driven-animation)
-   [Timergesteuerte Animation](#timer-driven-animation)

### <a name="application-driven-animation"></a>Application-Driven Animation

Anwendungen, die eine hardwarebeschleunigte Grafik-API verwenden, können mit der Aktualisierungsrate des Monitors synchronisiert werden, um reibungslose Animationen zu rendern. Alternativ kann eine Anwendung einen eigenen Zeitsteuerungsmechanismus verwenden, um zu bestimmen, wann die einzelnen Frames einer Animation ge zeichnen werden. In beiden Fällen gibt die Anwendung dem Animations-Manager an, wann der Zustand aktualisiert werden soll. Ein Animations-Timer kann weiterhin verwendet werden, um die aktuelle Zeit mit hoher Genauigkeit in den vom Animations-Manager benötigten Einheiten zu bestimmen.

Das folgende Diagramm zeigt die Interaktionen zwischen einer Anwendung und den Komponenten Windows Animation, wenn die Anwendung Animationsupdates direkt animiert.

![Diagramm, das die Interaktionen zwischen einer Anwendung und den Windows-Animationskomponenten zeigt, wenn die Anwendung Animationsupdates direkt animiert.](images/animationupdates.png)

In der einfachsten Konfiguration wird von einer Anwendung jedes Mal neu gezeichnet, wenn der Bildschirm aktualisiert wird, auch wenn keine Animationen abspielt werden. Um unnötige Arbeit zu vermeiden, kann eine Anwendung einen Manager-Ereignishandler registrieren, um benachrichtigt zu werden, wenn Animationen geplant sind, und erkennen, wenn der Zeitplan leer ist, sodass er die Neuzeichnung beenden kann.

### <a name="timer-driven-animation"></a>Timer-Driven Animation

Anstatt den Animations-Manager direkt zu aktualisieren, können Anwendungen es dem Animations-Manager ermöglichen, den Animations-Manager darüber zu informieren, wann der Zustand aktualisiert werden soll, und einfach benachrichtigt werden, wenn jedes Update erfolgt ist. Dieser Ansatz wird für ältere Grafik-APIs empfohlen. Wenn eine Synchronisierung mit der Aktualisierungsrate des Monitors möglich ist, ist es im Allgemeinen besser, dies zu tun und eine anwendungsgesteuerte Animation zu verwenden.

Das folgende Diagramm zeigt die Interaktionen zwischen einer Anwendung und den Komponenten Windows Animation, wenn der Animationszeitr Animationsupdates animiert.

![Diagramm, das die Interaktionen zwischen einer Anwendung und den Komponenten der Windows-Animation zeigt, wenn der Animationszeitr Animationsupdates animiert.](images/animationtimerupdates.png)

Der Timer kann so konfiguriert werden, dass er nur ausgeführt wird, wenn die Animationen geplant sind. Dies ist eine einfache Frage der Übergabe eines bestimmten Parameters, wenn der Timer und der Animations-Manager verbunden sind.

## <a name="advanced-features"></a>Erweiterte Funktionen

Neben einer grundlegenden Grundlage zur Unterstützung von Animationen bietet Windows Animation Unterstützung für verschiedene erweiterte Animationstechniken, darunter:

<dl> <dt>

<span id="context-sensitive_duration"></span><span id="CONTEXT-SENSITIVE_DURATION"></span>*Kontextorientierte Dauer*
</dt> <dd>

Die Dauer eines Übergangs muss nicht festgelegt werden. sie kann basierend auf dem Wert und der Geschwindigkeit der animierten Variable bestimmt werden, wenn der Übergang beginnt.

</dd> <dt>

<span id="velocity_matching"></span><span id="VELOCITY_MATCHING"></span>*Geschwindigkeitsabgleich*
</dt> <dd>

Die Bewegung ist in der Regel schwieriger für die Augen, wenn position und geschwindigkeit eines sich bewegenden Objekts nicht sofort zwischen Werten springen. Wenn ein neues Storyboard ein gerade abspielbares Storyboard unterbricht, ermöglicht der Geschwindigkeitsabgleich, dass das neue Storyboard reibungslos an der Stelle anfing, an der das vorherige beendet wurde.

</dd> <dt>

<span id="contention_management"></span><span id="CONTENTION_MANAGEMENT"></span>*Contention Management*
</dt> <dd>

Wenn zwei Storyboards dieselbe Animationsvariable gleichzeitig aktualisieren müssen, tritt ein Planungskonflikt auf. Anstatt eine bestimmte numerische Priorität für jedes Storyboard zu erfordern, ermöglicht Windows Animation der Anwendung, die relativen Prioritäten zweier Storyboards zu bestimmen.

</dd> </dl>

### <a name="contention-management"></a>Contention Management

Entwickler können einen Rückruf *für* einen Prioritätsvergleich implementieren, um die Priorität des geplanten Storyboards und des Storyboards zu vergleichen, das bereits im Zeitplan vorhanden ist. Eine Anwendung, die einen Prioritätsvergleich implementiert, kann eine beliebige bevorzugte Logik verwenden, um zu bestimmen, wann ein Storyboard einem anderen voransetzt. Um den Planungskonflikt zu beheben, fragt Windows Animation die Anwendung, welche dieser Aktionen in der folgenden Reihenfolge ausgeführt werden können:

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

 

 