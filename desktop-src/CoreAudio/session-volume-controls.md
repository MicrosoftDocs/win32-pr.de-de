---
description: Sitzungs Volume-Steuerelemente
ms.assetid: e6d112f9-08c9-4d95-b37b-267beebd0d7f
title: Sitzungs Volume-Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add29b18b39c942c54926190ef9c0f85e447bb88
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861300"
---
# <a name="session-volume-controls"></a>Sitzungs Volume-Steuerelemente

Wie bereits erläutert, können WASAPI-Clients die Volumeebene jeder [Audiositzung](audio-sessions.md)einzeln steuern. WASAPI wendet die volumeeinstellung für eine Sitzung einheitlich auf alle Streams in der Sitzung an. Jede Volumeebene ist ein Wert im Bereich von 0,0 bis 1,0, wobei 0,0 auf Stille und 1,0 auf vollständiges Volume (keine Dämpfung) hinweist.

Ein Client erstellt implizit eine Sitzung, indem er der Sitzung den ersten Stream zuweist. Die Standard Volume-Ebene der neuen Sitzung ist 1,0. Wie bereits erläutert, kann der Benutzer die Volumeebene der Sitzung über die Benutzeroberfläche eines Steuerungsprogramms (z. b. sndvol) anpassen, bei dem es sich um einen WASAPI-Client handelt. Die Steuerelement Einstellungen sind persistent.

Zusätzlich zu den vom Client kontrollierten Volumeeinstellungen wendet das System seine eigenen Volumeeinstellungen auf Sitzungen an. Diese Einstellungen basieren auf der audiorichtlinie und ändern sich dynamisch als Reaktion auf Änderungen in den Streams, die die globale Audiomischung bilden. Weitere Informationen zu Audiorichtlinien finden Sie unter [benutzermodusaudiokomponenten](user-mode-audio-components.md).

Die Systemsoftware, die das volumensteuerelement für jeden Stream implementiert, multipliziert die PCM-Beispiele im Stream mit der effektiven Volumeebene. Die effektive Volumeebene ist das Ergebnis der Multiplikation der Client-und systemvolumeeinstellungen. Folglich ist die resultierende Änderung in Signal Amplitude eine lineare Kombination der Client-und System Volume-Ebenen. Wenn die Client Volume-Ebene beispielsweise 0,8 und die System Volume-Ebene 0,5 ist, ist die effektive Volumeebene (0,8)<sup>.</sup> (0,5) = 0,4.

Beachten Sie, dass die wahrgenommene Lautstärke in Bezug auf Signal Amplitude nicht linear ist. Stattdessen variiert die Lautstärke ungefähr wie der Logarithmus der Volumeebene v:

Lautstärke in Dezibel = 20<sup>.</sup> Log ₁ ₀ (v)

Durch das Festlegen von v = 0,5 wird die Lautstärke des ursprünglichen Signals (das Signal vor dem Anwenden der Volumeebene) um 6 Dezimalstellen abgeschwächt. durch das Festlegen von v = 0,25 wird das Signal um 12 Dezimalstellen verringert usw. Eine Volumeebene v = 1,0, die 0 Dezimalstellen entspricht, ändert nicht die ursprüngliche Signalebene.

Audioanwendungen mit Benutzeroberflächen zum Steuern der Volumeebene zeigen normalerweise Schieberegler an, die Änderungen an der wahrgenommenen Lautstärke generieren, die linear proportional zu Änderungen an der Schieberegler-Position sind. Um eine lineare Beziehung zwischen der wahrgenommenen Lautstärke und der Schieberegler-Position zu schaffen, muss die Anwendung eine nichtlineare Beziehung zwischen der Volumeebene v und der Position des Schiebereglers definieren. Weitere Informationen finden Sie unter Steuer [Elemente für audiotaktvolumes](audio-tapered-volume-controls.md).

Wie bereits erläutert, zeigt das System Volume-Control-Programm, sndvol, volumeschiebe Regler für die audiositzungen an, die auf jedem audiorenderinggerät abgespielt werden. Diese Schieberegler werden im Gruppenfeld mit der Bezeichnung **Anwendungen** im sndvol-Fenster angezeigt. In der Regel enthält jede Sitzung alle Wiedergabe Datenströme eines bestimmten Anwendungsfensters. Durch die Schieberegler im sndvol-Fenster steuern die Benutzer die volumeebenen einzelner Audioanwendungen.

Als allgemeine Regel sollte eine Anwendung alle Wiedergabe Datenströme derselben Audiositzung zuweisen. WASAPI verhindert nicht, dass eine Anwendung ihre Wiedergabe Datenströme auf mehrere Sitzungen verteilt. Die resultierende Verbreitung von volumeschiebe Reglern in sndvol kann jedoch Benutzer verwirren.

Als Option kann ein Anwendungsfenster einen volumeschiebe Regler anzeigen. Der Schieberegler der Anwendung sollte den Status des entsprechenden sndvol-Schiebereglers jederzeit widerspiegeln. Wenn der Benutzer die Volumeebene durch Verschieben des Schiebereglers im Anwendungsfenster ändert, sollte der entsprechende Schieberegler im sndvol-Fenster in gemeinsamen mit dem anwendungsschiebe Regler verschoben werden. Ebenso sollte der Schieberegler der Anwendung in gemeinsamen mit dem Schieberegler sndvol verschoben werden, wenn der Benutzer den Schieberegler sndvol verschiebt.

Um dieses Verhalten zu unterstützen, implementiert WASAPI die [**isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) -Schnittstelle. Wenn der Benutzer den Schieberegler für die Anwendung verschiebt, ruft die Anwendung die [**isimpleaudiovolume:: setmastervolume**](/windows/desktop/api/Audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume) -Methode auf, um die Sitzungs Volume-Ebene entsprechend anzupassen. Sndvol überwacht volumeänderungen, die durch diese Methode vorgenommen wurden, und spiegelt die Änderungen in den angezeigten volumeschiebe Regler wider. Außerdem kann eine Anwendung Benachrichtigungen über Änderungen des Sitzungs Volumens empfangen, die der Benutzer über sndvol vornimmt. Zu diesem Zweck implementiert die Anwendung eine [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle und registriert die Schnittstelle bei WASAPI. Danach empfängt die Anwendung jedes Mal, wenn der Benutzer die Sitzungs Volume-Ebene über sndvol ändert, einen Benachrichtigungs Aufruf über die [**iaudiosessionevents:: onsimplevolumechanout**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) -Methode. Ein Codebeispiel, in dem eine **iaudiosessionevents** -Schnittstelle implementiert wird, finden Sie unter [audiositzungsereignisse](audio-session-events.md). Ein Codebeispiel, in dem eine **iaudiosessionevents** -Schnittstelle registriert wird, finden Sie unter [Audioereignisse für Legacy-Audioanwendungen](audio-events-for-legacy-audio-applications.md).

Die **isimpleaudiovolume** -Schnittstelle wendet dieselbe Volumeebene auf alle Kanäle in einer Audiositzung gleichmäßig an. Obwohl diese Schnittstelle die Anforderungen an die volumesteuerung der meisten Anwendungen erfüllen sollte, benötigen einige Anwendungen möglicherweise speziellere Volumen Steuerungsfunktionen. Die [**iaudiostreamvolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) -Schnittstelle steuert das Volume eines einzelnen Streams in einer Sitzung in Relation zu den anderen Datenströmen in der Sitzung. **Iaudiostreamvolume** ermöglicht außerdem einem Client, die volumeebenen aller Kanäle im Stream einzeln zu steuern. Beispielsweise kann eine Anwendung diese Funktion verwenden, um Audioeffekte zu erzielen, z. b. das Simulieren der räumlichen Bewegung einer Audioquelle durch Schwenken von links nach rechts. Eine weitere spezialisierte Schnittstelle, [**ichannelaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), steuert die volumeebenen der einzelnen Kanäle in einer Sitzung. Beispielsweise kann eine Anwendung **ichannelaudiovolume** verwenden, um die Balance-Steuerelemente für ein stereophonisches Soundsystem zu implementieren.

Die volumeschiebe Regler im Feld **Anwendungen** in sndvol spiegeln nur volumeänderungen wider, die über die Schnittstelle **isimpleaudiovolume** vorgenommen werden. Die volumeänderungen, die über die Schnittstellen **iaudiostreamvolume** und **ichannelaudiovolume** vorgenommen werden, werden nicht widerspiegelt. Obwohl einige Anwendungen möglicherweise das direkte oder indirekte Steuern der Volumeeinstellungen über **iaudiostreamvolume** und **ichannelaudiovolume** ermöglichen, sollten Entwickler keine Anwendungs Schieberegler für diese Volumeeinstellungen präsentieren, die Benutzer mit den volumeschiebe Reglern in sndvol wahrscheinlich verwechseln. Andernfalls kann ein Benutzer einen anwendungsslider verschieben, der erwartet, dass die Änderung in einem sndvol-Schieberegler reflektiert wird und verwirrt wird, wenn keine solche Änderung auftritt. Entwickler können dieses Problem durch das Design der Benutzeroberfläche vermeiden.

Die effektive Volumeebene eines beliebigen Kanals in der Sitzungs teilmischung, wie er bei den Referenten gehört, ist das Produkt der folgenden vier volumeebenenfaktoren:

-   Die volumeebenen pro Kanal der Datenströme in der Sitzung, die Clients durch die Methoden in der **iaudiostreamvolume** -Schnittstelle steuern können.
-   Die Volumeebene pro Kanal der Sitzung, die Clients durch die Methoden in der **ichannelaudiovolume** -Schnittstelle steuern können.
-   Die Master Volume-Ebene der Sitzung, die Clients durch die Methoden in der **isimpleaudiovolume** -Schnittstelle steuern können.
-   Die Richtlinien basierte Volumeebene der Sitzung, die das System dynamisch ändert, wenn die globale Mischung geändert wird.

Jede der vier volumeebenenfaktoren in der vorangehenden Liste ist ein Wert im Bereich von 0,0 bis 1,0, wobei 0,0 auf Stille und 1,0 auf vollständiges Volume (keine Dämpfung) hinweist. Die effektive Volumeebene ist auch ein Wert im Bereich von 0,0 bis 1,0.

Die Audioengine wendet die effektive Volumeebene für jeden Kanal auf die Kanäle in einem Stream an, bevor der Stream mit den anderen Streams in der Audiositzung gemischt wird. Wenn Stichprobenwerte in einem Kanal den Wert von 0 (null) überschreiten, nachdem die Audioengine Sie mit der effektiven Volumeebene multipliziert hat, schneidet die Engine die Beispiele ab, bevor Sie Sie der Sitzungs teilmischung hinzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lautstärkeregler](volume-controls.md)
</dt> </dl>

 

 



