---
title: Windows Animationsglossar
description: Dieses Glossar enthält Begriffe und Akronyme, die für Entwickler von Interesse sind, die den Windows Animation Manager verwenden.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 66e9cfb4-b9ae-4c21-9b1f-532c7d750903
keywords:
- Windows Animation Windows Animation , Glossar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb477edcaa49aa8baff1bc628ca5d94c13dacc0e552137275ff1e92d8e4cfae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137393"
---
# <a name="windows-animation-glossary"></a>Windows Animationsglossar

Dieses Glossar enthält Begriffe und Akronyme, die für Entwickler von Interesse sind, die den Windows Animation Manager verwenden.

<dl> <dt>

<span id="uianimation.term.animation"></span><span id="UIANIMATION.TERM.ANIMATION"></span>**Animation** 
</dt> <dd>

Eine Sequenz synthetischer, aufeinander folgenden Stillbilder, die eine Bewegung erzeugen, wenn sie wiedergeben wird.

</dd> <dt>

<span id="uianimation.term.animation_manager"></span><span id="UIANIMATION.TERM.ANIMATION_MANAGER"></span>**Animations-Manager** 
</dt> <dd>

Eine Kernkomponente von Windows Animation und der zentralen programmgesteuerten Schnittstelle zum Verwalten (Erstellen, Planen und Steuern) von Animationen.

</dd> <dt>

<span id="uianimation.term.animation_timer"></span><span id="UIANIMATION.TERM.ANIMATION_TIMER"></span>**Animationszeitr**
</dt> <dd>

Eine Komponente zum Bereitstellen von Zeitsteuerungsdiensten, die in Verbindung mit dem Animations-Manager verwendet werden können. Sie drosselt die Bildfrequenz dynamisch basierend auf der Anwendungs- und Systemauslastung oder im Modus mit geringer Leistung. Siehe auch: Drosselung.

</dd> <dt>

<span id="uianimation.term.animation_variable"></span><span id="UIANIMATION.TERM.ANIMATION_VARIABLE"></span>**Animationsvariable** 
</dt> <dd>

Ein Wert, der animiert werden kann. Animationsvariablen können verwendet werden, um die Position, Größe, Drehung, Transparenz und andere Qualitäten sichtbarer Objekte zu darstellen.

</dd> <dt>

<span id="uianimation.term.cancellation"></span><span id="UIANIMATION.TERM.CANCELLATION"></span>**Stornierung**
</dt> <dd>

Der Prozess, bei dem ein Storyboard aus dem Zeitplan entfernt wird, bevor es mit der Wiedergabe begonnen hat.

</dd> <dt>

<span id="uianimation.term.compression"></span><span id="UIANIMATION.TERM.COMPRESSION"></span>**Komprimierung**
</dt> <dd>

Eine Verfingung der Zeitempfinden eines Storyboards. Das System erhöht die Geschwindigkeit, mit der das Storyboard fortschreitet, indem Eingabezeitwerte übergeben werden, die schneller als die Systemuhr steigen.

</dd> <dt>

<span id="uianimation.term.conclusion"></span><span id="UIANIMATION.TERM.CONCLUSION"></span>**Schlussfolgerung**
</dt> <dd>

Der Prozess, bei dem ein Storyboard an das Beenden unbestimmter Schleifen weiterverteilt wird. Wenn die Schleife begonnen hat, wird die aktuelle Iteration abgeschlossen, und der Rest des Storyboards wird dann wieder verwendet. Andernfalls wird der Schleifenteil des Storyboards vollständig übersprungen.

</dd> <dt>

<span id="uianimation.term.frame"></span><span id="UIANIMATION.TERM.FRAME"></span>**Frame** 
</dt> <dd>

Ein einzelnes Bild in einem Film oder einer Animation.

</dd> <dt>

<span id="uianimation.term.frame_rate"></span><span id="UIANIMATION.TERM.FRAME_RATE"></span>**Framerate** 
</dt> <dd>

Die Anzahl der pro Sekunde angezeigten Frames. Höhere Bildraten erzeugen im Allgemeinen eine reibungslosere Bewegung im Bild.

</dd> <dt>

<span id="uianimation.term.interpolator"></span><span id="UIANIMATION.TERM.INTERPOLATOR"></span>**Interpolator**
</dt> <dd>

Das Programmierobjekt, das die mathematische Interpolation des Werts und der Geschwindigkeit einer Variablen für einen Übergang übernimmt.

</dd> <dt>

<span id="uianimation.term.keyframe"></span><span id="UIANIMATION.TERM.KEYFRAME"></span>**Keyframe**
</dt> <dd>

Ein Zeitpunkt innerhalb eines Storyboards, der relativ zum Anfang des Storyboards, relativ zu einem anderen Keyframe oder zur Endzeit eines Übergangs angegeben werden kann, und zum Angeben der Start- und Endzeit anderer Übergänge oder eines Zyklus innerhalb des Storyboards verwendet werden kann.

</dd> <dt>

<span id="uianimation.term.loop"></span><span id="UIANIMATION.TERM.LOOP"></span>**Schleife**
</dt> <dd>

Ein Abschnitt eines Storyboards zwischen zwei Keyframes, der wiederholt abgespielt wird. Eine Schleife kann eine begrenzte Anzahl von Malen oder unbegrenzt spielen.

</dd> <dt>

<span id="uianimation.term.priority_comparison"></span><span id="UIANIMATION.TERM.PRIORITY_COMPARISON"></span>**Prioritätsvergleich** 
</dt> <dd>

Clientdefinierter Code, der zwei Storyboards vergleicht, von denen eines bereits geplant ist, und das andere, das geplant werden soll, um deren relative Priorität zu bestimmen. Ein geplantes Storyboard kann gekürzt, komprimiert, abgebrochen oder abgeschlossen werden, um die Planung des Storyboards mit höherer Priorität zu ermöglichen.

</dd> <dt>

<span id="uianimation.term.storyboard"></span><span id="UIANIMATION.TERM.STORYBOARD"></span>**Storyboard** 
</dt> <dd>

Eine Gruppe von Animationsübergängen, die relativ zueinander synchronisiert werden.

</dd> <dt>

<span id="uianimation.term.tag"></span><span id="UIANIMATION.TERM.TAG"></span>**Tag** 
</dt> <dd>

Ein Paar, das aus einer ganzzahligen ID und einem COM-Objekt besteht, das von einer Anwendung verwendet wird, um Animationsvariablen und Storyboards innerhalb des Bereichs eines bestimmten Animations-Managers zu identifizieren.

</dd> <dt>

<span id="uianimation.term.throttling"></span><span id="UIANIMATION.TERM.THROTTLING"></span>**Drosselung** 
</dt> <dd>

Dynamisches Anpassen der Bildfrequenz einer Animation, um bestimmte Anforderungen zu erfüllen. Durch die Drosselung wird sichergestellt, dass Animationen mit einer konsistenten Bildfrequenz gerendert werden, während gleichzeitig die Verwendung von Systemressourcen für das Rendering mit einer Rate minimiert wird, die über das hinaus geht, was erforderlich oder nützlich ist.

</dd> <dt>

<span id="uianimation.term.tick"></span><span id="UIANIMATION.TERM.TICK"></span>**tick** 
</dt> <dd>

Ein Timerereignis, das in der Regel das Rendern eines einzelnen Frames auslöst.

</dd> <dt>

<span id="uianimation.term.transition"></span><span id="UIANIMATION.TERM.TRANSITION"></span>**Übergang** 
</dt> <dd>

Ein Konstrukt, das progressive Aktualisierungen für eine Animationsvariable über einen bestimmten Zeitraum definiert.

</dd> <dt>

<span id="uianimation.term.trimming"></span><span id="UIANIMATION.TERM.TRIMMING"></span>**Trimmen**
</dt> <dd>

Das Steuerelement einer Animationsvariablen mit einem Storyboard mit höherer Priorität wird vorab aus dem Steuerelement des Storyboards. Wenn das Kürzen eines Storyboards für eine oder mehrere Variablen dazu führt, dass das Storyboard vorzeitig beendet wird, gilt es als abgeschnitten. Siehe auch: Abschneiden.

</dd> <dt>

<span id="uianimation.term.truncation"></span><span id="UIANIMATION.TERM.TRUNCATION"></span>**Abschneiden**
</dt> <dd>

Vorzeitiges Beenden eines Storyboards, indem die Steuerung einer oder mehrere der Variablen, die es animiert, mit einem oder mehr Storyboards mit höherer Priorität vorzeitig beendet wird. Siehe auch: Kürzen.

</dd> </dl>

 

 




