---
title: Glossar für Windows-Animationen
description: Dieses Glossar enthält Begriffe und acronyme, die für Entwickler interessant sind, die den Windows-Animations-Manager verwenden.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 66e9cfb4-b9ae-4c21-9b1f-532c7d750903
keywords:
- Animation Windows Animation Windows Animation, Glossar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b7f276b0f20efc35057a9ee7c006c3cf170ac3
ms.sourcegitcommit: fdd00b445ee88366e9cdd1eed0cb3e42e2a73eca
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2019
ms.locfileid: "104516557"
---
# <a name="windows-animation-glossary"></a>Glossar für Windows-Animationen

Dieses Glossar enthält Begriffe und acronyme, die für Entwickler interessant sind, die den Windows-Animations-Manager verwenden.

<dl> <dt>

<span id="uianimation.term.animation"></span><span id="UIANIMATION.TERM.ANIMATION"></span>**Animation** 
</dt> <dd>

Eine Sequenz von synthetischen, aufeinander folgenden Bildern, die eine Illusion der Bewegung erzeugt, wenn Sie wiedergegeben wird.

</dd> <dt>

<span id="uianimation.term.animation_manager"></span><span id="UIANIMATION.TERM.ANIMATION_MANAGER"></span>**Animations-Manager** 
</dt> <dd>

Eine Kernkomponente der Windows-Animation und die zentrale programmgesteuerte Schnittstelle zum Verwalten (erstellen, planen und Steuern) von Animationen.

</dd> <dt>

<span id="uianimation.term.animation_timer"></span><span id="UIANIMATION.TERM.ANIMATION_TIMER"></span>**Animations Zeit Geber**
</dt> <dd>

Eine Komponente, die Zeit Steuerungs Dienste bereitstellt, die in Verbindung mit dem Animations-Manager verwendet werden können. Dadurch wird die Framerate basierend auf der Anwendungs-und System Auslastung oder im Modus für niedrige Energie dynamisch gedrosselt. Siehe auch: Drosselung.

</dd> <dt>

<span id="uianimation.term.animation_variable"></span><span id="UIANIMATION.TERM.ANIMATION_VARIABLE"></span>**Animations Variable** 
</dt> <dd>

Ein Wert, der animiert werden kann. Animations Variablen können verwendet werden, um Position, Größe, Drehung, Transparenz und andere Qualitäten von sichtbaren Objekten darzustellen.

</dd> <dt>

<span id="uianimation.term.cancellation"></span><span id="UIANIMATION.TERM.CANCELLATION"></span>**Streichung**
</dt> <dd>

Der Prozess, bei dem ein Storyboard aus dem Zeitplan entfernt wird, bevor die Wiedergabe gestartet wird.

</dd> <dt>

<span id="uianimation.term.compression"></span><span id="UIANIMATION.TERM.COMPRESSION"></span>**komprimi**
</dt> <dd>

Eine Aktualisierung der Zeit eines Storyboards. Das System erhöht die Rate, mit der das Storyboard fortschreitet, indem er Eingabe Zeitwerte übergibt, die schneller als die Systemuhr steigen.

</dd> <dt>

<span id="uianimation.term.conclusion"></span><span id="UIANIMATION.TERM.CONCLUSION"></span>**Abschluss**
</dt> <dd>

Der Prozess, bei dem ein Storyboard zum Beenden beliebiger Schleifen umgeleitet wird. Wenn die Schleife begonnen hat, wird die aktuelle Iterations Operation fertiggestellt, und der Rest des Storyboards wird wiedergegeben. Andernfalls wird der Schleifen Teil des Storyboards vollständig übersprungen.

</dd> <dt>

<span id="uianimation.term.frame"></span><span id="UIANIMATION.TERM.FRAME"></span>**Frame** 
</dt> <dd>

Ein einzelnes Bild in einem Film oder einer Animation.

</dd> <dt>

<span id="uianimation.term.frame_rate"></span><span id="UIANIMATION.TERM.FRAME_RATE"></span>**Framerate** 
</dt> <dd>

Die Anzahl der pro Sekunde angezeigten Frames. Höhere Frameraten führen in der Regel zu einer glatteren Bewegung des Bilds.

</dd> <dt>

<span id="uianimation.term.interpolator"></span><span id="UIANIMATION.TERM.INTERPOLATOR"></span>**interpolators**
</dt> <dd>

Das Programmier Objekt, das die mathematische interpolung des Werts und der Geschwindigkeit einer Variablen für einen Übergang durchführt.

</dd> <dt>

<span id="uianimation.term.keyframe"></span><span id="UIANIMATION.TERM.KEYFRAME"></span>**Keyframe**
</dt> <dd>

Ein Zeitpunkt innerhalb eines Storyboards, der relativ zum Anfang des Storyboards, relativ zu einem anderen Keyframe oder zum Endzeit eines Übergangs angegeben werden kann. er kann verwendet werden, um die Start-und Endzeit anderer Übergänge oder eines Zyklen innerhalb des Storyboards anzugeben.

</dd> <dt>

<span id="uianimation.term.loop"></span><span id="UIANIMATION.TERM.LOOP"></span>**ESE**
</dt> <dd>

Ein Abschnitt eines Storyboards zwischen zwei Keyframes, die wiederholt abgespielt werden. Eine-Schleife kann eine begrenzte Anzahl von Zeiten oder unbegrenzt wiedergeben.

</dd> <dt>

<span id="uianimation.term.priority_comparison"></span><span id="UIANIMATION.TERM.PRIORITY_COMPARISON"></span>**Prioritäts Vergleich** 
</dt> <dd>

Client definierter Code, der zwei Storyboards vergleicht, eine bereits geplante und die andere, die geplant werden soll, um deren relative Priorität zu bestimmen. Ein geplantes Storyboard kann gekürzt, komprimiert, abgebrochen oder abgeschlossen werden, um die Planung des Storyboards mit höherer Priorität zu aktivieren.

</dd> <dt>

<span id="uianimation.term.storyboard"></span><span id="UIANIMATION.TERM.STORYBOARD"></span>**Storyboard** 
</dt> <dd>

Eine Gruppe von Animations Übergängen, die relativ zueinander synchronisiert werden.

</dd> <dt>

<span id="uianimation.term.tag"></span><span id="UIANIMATION.TERM.TAG"></span>**Tag** 
</dt> <dd>

Ein paar aus einer ganzzahligen ID und einem COM-Objekt, das von einer Anwendung verwendet wird, um Animations Variablen und Storyboards innerhalb des Gültigkeits Bereichs eines bestimmten Animations-Managers zu identifizieren.

</dd> <dt>

<span id="uianimation.term.throttling"></span><span id="UIANIMATION.TERM.THROTTLING"></span>**Drosselung** 
</dt> <dd>

Dynamisches Anpassen der Framerate einer Animation an bestimmte Anforderungen. Durch die Drosselung wird sichergestellt, dass Animationen mit einer konsistenten Framerate gerendert werden, während gleichzeitig die Verwendung von Systemressourcen für das Rendern mit einer Rate minimiert wird

</dd> <dt>

<span id="uianimation.term.tick"></span><span id="UIANIMATION.TERM.TICK"></span>**Tick** 
</dt> <dd>

Ein Timer-Ereignis, das in der Regel das Rendering eines einzelnen Frames auslöst.

</dd> <dt>

<span id="uianimation.term.transition"></span><span id="UIANIMATION.TERM.TRANSITION"></span>**Übergang** 
</dt> <dd>

Ein Konstrukt, das Progressive Updates für eine Animations Variable über einen Zeitraum definiert.

</dd> <dt>

<span id="uianimation.term.trimming"></span><span id="UIANIMATION.TERM.TRIMMING"></span>**Kürzung**
</dt> <dd>

Vorab Entfernung eines Storyboards für eine Animations Variable mit einem Storyboard mit höherer Priorität. Wenn das Kürzen eines Storyboards auf eine oder mehrere Variablen bewirkt, dass das Storyboard vorzeitig beendet wird, gilt es als abgeschnitten. Siehe auch: abschneiden.

</dd> <dt>

<span id="uianimation.term.truncation"></span><span id="UIANIMATION.TERM.TRUNCATION"></span>**Kürzung**
</dt> <dd>

Das vorzeitige Beenden eines Storyboards durch die vorab Entfernung der Kontrolle über eine oder mehrere der Variablen, die mit einem oder mehreren Storyboards mit höherer Priorität animiert werden. Siehe auch: kürzen.

</dd> </dl>

 

 




