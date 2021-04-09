---
title: Übersicht über Windows-Animationen
description: Diese Übersicht bietet eine Einführung in den Windows-Animations-Manager und konzentriert sich auf die wichtigsten Komponenten und Konzepte.
ms.assetid: de1380c9-6801-4178-9281-a23af7d71d77
keywords:
- Windows Animation Windows Animation, Übersicht
- Animation Manager Objects Windows-Animation, beschrieben
- Animations Variablen Windows-Animation, beschrieben
- Animation Zeit Geber Objekte Windows-Animation, beschrieben
- Zeit Steuerungssystem-Windows-Animation
- Kontextabhängige Dauer der Windows-Animation
- der Windows-Animation entsprechende Geschwindigkeit
- Windows-Animation für Konflikt Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a60b02b29d8d434cc93420f36c3cdca4428f94c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039089"
---
# <a name="windows-animation-overview"></a>Übersicht über Windows-Animationen

Diese Übersicht bietet eine Einführung in den Windows-Animations-Manager und konzentriert sich auf die wichtigsten Komponenten und Konzepte. Weitere Informationen zu Storyboards und Übergängen finden Sie unter [Übersicht über Storyboards](storyboard-construction.md).

Dieses Thema enthält folgende Abschnitte:

-   [Grundlegende Konzepte](#basic-concepts)
-   [Komponenten der Windows-Animation](#components-of-windows-animation)
-   [Die Windows-Animations-API](#the-windows-animation-api)
-   [Konfigurationen](#configurations)
    -   [Anwendungs gesteuerte Animation](#application-driven-animation)
    -   [Zeit Geber gesteuerte Animation](#timer-driven-animation)
-   [Erweiterte Funktionen](#advanced-features)
    -   [Konflikt Verwaltung](#contention-management)
-   [Zugehörige Themen](#related-topics)

## <a name="basic-concepts"></a>Grundlegende Konzepte

*Animation* ist eine Sequenz von aufeinander folgenden Bildern, die eine Illusion der Bewegung erzeugt, wenn Sie wiedergegeben wird. Die Verwendung interaktiver Animationen in der Benutzeroberfläche kann eine Anwendung zu einer eindeutigen Persönlichkeit machen und die Benutzeroberfläche verbessern. Animation kann Ihnen helfen, wichtige Statusänderungen an der Benutzeroberfläche zu übermitteln und die Komplexität der Benutzeroberfläche zu verwalten. Animation kann dem Benutzer auch die Qualität einer Anwendung hinzufügen.

Als Beispiel wird die Windows-Animation in der Taskleiste verwendet, um Sie beim Verwalten von Dateien und Programmen zu unterstützen und die Bildschirmlupe zu vergrößern, um die Anzeige von Benutzern zu vereinfachen.

Die grundlegenden Einheiten einer Animation sind das Merkmal eines visuellen Elements, das animiert werden soll, und die Beschreibung, wie sich das Merkmal im Laufe der Zeit ändert. Eine Anwendung kann eine Vielzahl von Merkmalen animieren, wie z. b. Position, Farbe, Größe, Drehung, Kontrast und Deckkraft.

In der Windows-Animation stellt eine *Animations Variable* das zu animierende Merkmal dar. Bei einem *Übergang* wird beschrieben, wie sich der Wert dieser Animations Variablen ändert, wenn eine Animation auftritt. Ein visuelles Element kann z. b. eine Animations Variable aufweisen, die seine Deckkraft angibt, und eine Benutzeraktion generiert möglicherweise einen Übergang, der diese Deckkraft von einem Wert von 50 zu 100 übernimmt und eine Animation von semitransparent in vollständig nicht transparent darstellt.

Ein *Storyboard* ist eine Reihe von Übergängen, die im Laufe der Zeit auf eine oder mehrere Animations Variablen angewendet werden. Eine Anwendung zeigt Animationen an, indem Storyboards erstellt und abgespielt werden, und anschließend werden Sequenzen von diskreten Frames gezeichnet, wenn sich die Werte von Animations Variablen im Laufe der Zeit ändern.

## <a name="components-of-windows-animation"></a>Komponenten der Windows-Animation

Die Windows-Animation besteht aus den folgenden Komponenten:

<dl> <dt>

<span id="animation_manager"></span><span id="ANIMATION_MANAGER"></span>Animations-Manager
</dt> <dd>

Anwendungen verwenden ein Animations-Manager-Objekt, um Animations Variablen und Storyboards zu erstellen, Animationen zu planen und zu steuern und Zustandsinformationen zu aktualisieren, bevor die Anwendung jeden Frame zeichnet. Ein einzelnes Animations-Manager-Objekt verwaltet in der Regel alle Animationen in einer Anwendung und verfügt daher über eine globale Kontrolle über alle geplanten Storyboards.

</dd> <dt>

<span id="animation_variables"></span><span id="ANIMATION_VARIABLES"></span>Animations Variablen
</dt> <dd>

Vor dem Starten von Animationen muss eine Anwendung Animations Variablen Objekte erstellen. Eine Animations Variable stellt einen Aspekt eines visuellen Elements dar, das animiert werden soll. Die-Variable ist ein skalarer Gleit Komma Wert, obwohl der Wert auf einen ganzzahligen Wert gerundet werden kann.

Eine Animations Variable hat normalerweise die gleiche Lebensdauer wie das visuelle Element, das Sie animieren möchten. Der Anfangswert einer Animations Variablen wird beim Erstellen der Variablen angegeben. Danach kann der zugehörige Wert nicht direkt geändert werden. Es muss über den Animations-Manager aktualisiert werden.

Eine Animations Variable kann durch ein- *Tag* identifiziert werden, bei dem es sich um eine Kopplung eines ganzzahligen Bezeichners mit einem Zeiger auf ein COM-Objekt handelt. Ein Tag muss nicht eindeutig sein, es sei denn, die Anwendung verwendet es, um nach einer Variablen zu suchen. Standardmäßig weist eine Animations Variable kein-Tag auf, und alle Versuche, das zugehörige Tag zu lesen, schlagen fehl, bis eine solche festgelegt wurde.

</dd> <dt>

<span id="timing_system"></span><span id="TIMING_SYSTEM"></span>Zeit Steuerungssystem
</dt> <dd>

Windows-Animation umfasst ein Zeit Steuerungssystem, mit dem sichergestellt werden kann, dass Animationen mit einer nahtlos und konsistenten Framerate gerendert werden, während gleichzeitig die Verwendung von Systemressourcen für das Rendering reduziert wird, wenn das System ausgelastet ist. Ein *Timer* unterstützt das Rendern von Animationen, indem automatisch der Durchlauf einer kleinen Zeiteinheit, die als *Tick* bezeichnet wird, angegeben wird. Das Zeit Steuerungssystem überwacht die Gesamtleistung des System Renderings und *drosselt* Animationen durch dynamisches vergrößern oder Verkleinern der Ticks. Anwendungen können von einem Timer den Animations-Manager steuern und einen Handler registrieren, der vor und nach der Aktualisierung des Vorgesetzten für jeden Tick benachrichtigt werden soll. Anwendungen können die minimal zulässige Animations Frame Rate für einen Timer angeben und benachrichtigt werden, wenn die tatsächliche Framerate einer Animation unter diese Rate fällt.

Um Systemressourcen zu sparen, kann ein Timer so konfiguriert werden, dass er sich selbst deaktiviert, wenn keine Animation stattfindet.

</dd> </dl>

## <a name="the-windows-animation-api"></a>Die Windows-Animations-API

Die Windows-Animations-API ist eine COM-basierte Single Thread-API, die die folgenden Funktionen für Entwickler bereitstellt:

-   Ein Animations-Manager-Objekt, [**uianimationmanager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)), zum Erstellen von Animations Objekten und zum Steuern von Animationen
-   Animations Variablen und Storyboards
-   Eine grundlegende Bibliothek, [**uianimationtransitionlibrary**](/previous-versions/windows/desktop/legacy/dd317028(v=vs.85)), von sofort einsatzbereiten Übergängen
-   Ein Zeit Geber Objekt, [**uianimationtimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)), zum Bestimmen der aktuellen Uhrzeit und optional zum übertreiben der Animation
-   Ereignis Hooks zum Überwachen des Status und Fortschritts der Animation

Die komplette API-Referenz finden Sie unter [Referenz zur Windows-Animation](windows-animation-reference.md). Beispielcode finden Sie unter [Windows Animation Tasks](using-windows-animation.md) und [Windows Animation Samples](windows-animation-samples.md).

## <a name="configurations"></a>Configurations

Anwendungen müssen die aktuelle Zeit vor dem Planen einer neuen Animation erhalten. Die folgenden Zeit Steuerungsmechanismen werden von der Windows-Animation unterstützt:

-   [Anwendungs gesteuerte Animation](#application-driven-animation)
-   [Zeit Geber gesteuerte Animation](#timer-driven-animation)

### <a name="application-driven-animation"></a>Animation Application-Driven

Anwendungen, die eine hardwarebeschleunigte Grafik-API verwenden, können mit der Aktualisierungsrate des Monitors synchronisiert werden, um Smooth Animationen zu reneln Alternativ kann eine Anwendung einen eigenen Zeit Steuerungsmechanismus verwenden, um zu bestimmen, wann die einzelnen Frames einer Animation gezeichnet werden müssen. In beiden Fällen teilt die Anwendung dem Animations-Manager mit, wann der Status aktualisiert werden soll. Ein Animations Timer kann weiterhin verwendet werden, um die aktuelle Zeit mit hoher Genauigkeit in den für den Animations-Manager benötigten Einheiten zu bestimmen.

Das folgende Diagramm zeigt die Interaktionen zwischen einer Anwendung und den Windows-Animations Komponenten, wenn die Anwendung Animations Aktualisierungen direkt treibt.

![Diagramm, das die Interaktionen zwischen einer Anwendung und den Windows-Animations Komponenten anzeigt, wenn die Anwendung Animations Aktualisierungen direkt treibt.](images/animationupdates.png)

In der einfachsten Konfiguration zeichnet eine Anwendung jedes Mal, wenn der Bildschirm aktualisiert wird, alles neu, auch wenn keine Animationen abgespielt werden. Um die Arbeit zu vermeiden, kann eine Anwendung einen Manager-Ereignishandler registrieren, der benachrichtigt werden soll, wenn Animationen geplant sind, und erkennen kann, wenn der Zeitplan leer ist, sodass er das Neuzeichnen beenden kann.

### <a name="timer-driven-animation"></a>Animation Timer-Driven

Anstatt den Animations-Manager direkt zu aktualisieren, können Anwendungen den Animations-Manager darüber informieren, wann der Status aktualisiert werden soll, und einfach benachrichtigt werden, wenn jedes Update durchgeführt wurde. Diese Vorgehensweise wird für ältere Grafik-APIs empfohlen. Im Allgemeinen ist es besser, wenn es möglich ist, eine Synchronisierung mit der Aktualisierungsrate des Monitors durchzuführen und die Anwendungs gesteuerte Animation zu verwenden.

Das folgende Diagramm zeigt die Interaktionen zwischen einer Anwendung und den Windows-Animations Komponenten, wenn der Animations Zeit Geber Animations Aktualisierungen vorantreibt.

![Diagramm, das die Interaktionen zwischen einer Anwendung und den Windows-Animations Komponenten anzeigt, wenn der Animations Zeit Geber Animations Aktualisierungen vorantreibt.](images/animationtimerupdates.png)

Der Timer kann so konfiguriert werden, dass er nur ausgeführt wird, wenn die Animationen geplant sind. Dabei handelt es sich um eine einfache Übergabe eines bestimmten Parameters, wenn der Timer und der Animations-Manager verbunden sind.

## <a name="advanced-features"></a>Erweiterte Funktionen

Neben der grundlegenden Grundlage für die Unterstützung von Animationen bietet die Windows-Animation Unterstützung für mehrere erweiterte Animationstechniken, einschließlich:

<dl> <dt>

<span id="context-sensitive_duration"></span><span id="CONTEXT-SENSITIVE_DURATION"></span>*Kontextabhängige Dauer*
</dt> <dd>

Die Dauer eines Übergangs muss nicht korrigiert werden. Sie kann basierend auf dem Wert und der Geschwindigkeit der animierten Variablen bestimmt werden, wenn der Übergang beginnt.

</dd> <dt>

<span id="velocity_matching"></span><span id="VELOCITY_MATCHING"></span>*Geschwindigkeits Übereinstimmung*
</dt> <dd>

Bewegung ist im allgemeinen angenehmer, wenn die Position und Geschwindigkeit eines verschiebenden Objekts nicht unmittelbar zwischen den Werten springen. Wenn ein neues Storyboard eine derzeit wiedergegebene Unterbrechung durchläuft, kann das neue Storyboard das neue Storyboard reibungslos aufspielen, wenn das vorherige beendet wurde.

</dd> <dt>

<span id="contention_management"></span><span id="CONTENTION_MANAGEMENT"></span>*Konflikt Verwaltung*
</dt> <dd>

Wenn zwei Storyboards dieselbe Animations Variable gleichzeitig aktualisieren müssen, tritt ein Planungs Konflikt auf. Anstatt für jedes Storyboard eine bestimmte numerische Priorität zu erfordern, ermöglicht die Windows-Animation der Anwendung, die relativen Prioritäten von zwei Storyboards zu ermitteln.

</dd> </dl>

### <a name="contention-management"></a>Konflikt Verwaltung

Entwickler können einen *Prioritäts Vergleichs* Rückruf implementieren, um die Priorität des geplanten Storyboards und des Storyboards zu vergleichen, das bereits im Zeitplan vorhanden ist. Eine Anwendung, die einen Prioritäts Vergleich implementiert, kann jede bevorzugte Logik verwenden, um zu bestimmen, wann ein Storyboard eine andere vorzeitig entfernt. Um den Planungs Konflikt aufzulösen, fragt die Windows-Animation die Anwendung ab, welche dieser Aktionen ausgeführt werden kann, und zwar in der folgenden Reihenfolge:

-   **Brechen Sie das geplante Storyboard ab.** Wenn das geplante Storyboard noch nicht wiedergegeben wurde, wird es möglicherweise abgebrochen und sofort aus dem Zeitplan entfernt.
-   **Kürzen Sie das geplante Storyboard.** Wenn ein neues Storyboard ein geplantes Storyboard ausschneidet, wird die Variable vom geplanten Storyboard nicht mehr beeinflusst, sobald das neue Storyboard mit der Animation beginnt. Die Geschwindigkeiten werden abgeglichen, sodass das neue Storyboard reibungslos abgerufen werden kann, wenn das vorherige zurückgelassen wurde.
-   **Schließen Sie das geplante Storyboard.** Ein Storyboard kann nur beendet werden, wenn es eine Schleife enthält, die auf unbestimmte Zeit wiederholt wird. Wenn sich das Storyboard in einer solchen Schleife befindet, wenn es beendet wird, wird die aktuelle Wiederholung abgeschlossen, und der Rest des Storyboards wird wiedergegeben. Wenn die Schleife beim Abschluss eines Storyboards noch nicht gestartet wurde, wird die Schleife vollständig übersprungen.
-   **Komprimieren Sie das geplante Storyboard.** Wenn die Kürzung oder das Abbrechen des geplanten Storyboards nicht möglich ist, kann das Storyboard fertiggestellt werden. Mit der Windows-Animation wird die Möglichkeit eingeführt, die für das geplante Storyboard verfügbare Zeit (und alle zuvor geplanten Storyboards) zu komprimieren, sodass die Variablen den Endzustand schneller erreichen. Wenn die Komprimierung angewendet wird, wird die Zeit für betroffene Storyboards vorübergehend beschleunigt, sodass Sie schneller abgespielt werden.

Wenn keine der oben genannten Aktionen durch die registrierten Prioritäts Vergleichsobjekte zulässig ist, schlägt der Versuch fehl, das neue Storyboard zu planen. Standardmäßig können alle Storyboards gekürzt, abgeschlossen oder komprimiert werden, um Fehler zu verhindern, aber keine kann abgebrochen werden.

Das folgende Diagramm zeigt den Lebenszyklus eines Storyboards unter Verwendung der Zustände, die durch die Enumeration des [**\_ \_ Storyboards \_**](/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status) für die Benutzeroberflächen Animation definiert werden. Anwendungen verwenden die Windows-Animations-API, um ein Storyboard zu erstellen und für die Planung zu übermitteln. Der Animations-Manager plant das Storyboard und verwaltet die Animation.

![Diagramm, das zeigt, wie der Animations-Manager das Storyboard plant und die Animation verwaltet.](images/statediagram.png)

Weitere Informationen zum Planen und Verwalten von Storyboards finden Sie unter [Übersicht über Storyboards](storyboard-construction.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zur Windows-Animation](windows-animation-reference.md)
</dt> <dt>

[Beispiele für Windows-Animationen](windows-animation-samples.md)
</dt> <dt>

[Windows-Animations Aufgaben](using-windows-animation.md)
</dt> </dl>

 

 