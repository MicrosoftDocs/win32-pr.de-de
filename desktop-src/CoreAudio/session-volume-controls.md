---
description: Steuerelemente für Sitzungsvolumen
ms.assetid: e6d112f9-08c9-4d95-b37b-267beebd0d7f
title: Steuerelemente für Sitzungsvolumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe45dce825dedd116c8f9c65684ac665eb6483f95dec3d247071f66408e8ed2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758890"
---
# <a name="session-volume-controls"></a>Steuerelemente für Sitzungsvolumen

Wie bereits erläutert, können WASAPI-Clients die Lautstärke jeder [Audiositzung einzeln steuern.](audio-sessions.md) WASAPI wendet die Volumeeinstellung für eine Sitzung einheitlich auf alle Streams in der Sitzung an. Jede Volumeebene ist ein Wert im Bereich von 0,0 bis 1,0, wobei 0,0 für Stille und 1,0 für vollständige Lautstärke (keine Dämpfung) steht.

Ein Client erstellt implizit eine Sitzung, indem dieser Sitzung der erste Stream zugewiesen wird. Die Standard-Volumeebene der neuen Sitzung ist 1.0. Wie bereits erwähnt, kann der Benutzer die Volumeebene der Sitzung über die Benutzeroberfläche eines Steuerungsprogramms (z. B. Sndvol) anpassen, bei dem es sich um einen WASAPI-Client handelt. Die Steuerelementeinstellungen sind persistent.

Zusätzlich zu den clientgesteuerten Volumeeinstellungen wendet das System seine eigenen Volumeeinstellungen auf Sitzungen an. Diese Einstellungen basieren auf einer Audiorichtlinie und ändern sich dynamisch als Reaktion auf Änderungen in den Streams, aus denen die globale Audiomischung erstellt wird. Weitere Informationen zur Audiorichtlinie finden Sie unter [Audiokomponenten im Benutzermodus.](user-mode-audio-components.md)

Die Systemsoftware, die die Volumesteuerung für jeden Stream implementiert, multipliziert die PCM-Stichproben im Stream mit der effektiven Volumeebene. Die effektive Volumeebene ist das Ergebnis der Multiplikation der Client- und System-Volumeeinstellungen. Daher ist die resultierende Änderung der Signalamplitude eine lineare Kombination der Client- und Systemvolumenebenen. Wenn die Client-Volumeebene beispielsweise 0,8 und die Systemvolumenebene 0,5 ist, ist die<sup></sup> effektive Volumeebene (0,8). (0,5) = 0,4.

Beachten Sie, dass die wahrgenommene Lautheit in Bezug auf die Signalamplitude nicht linear ist. Stattdessen variiert die Lautheit ungefähr wie der Logarithmus der Volumeebene v:

Lautheit in Dezibel = 20<sup>.</sup> log₁₀(v)

Daher dämpft das Festlegen von v = 0,5 die Lautstärke des ursprünglichen Signals (das Signal, bevor die Lautstärkestufe angewendet wird) um 6 Dezibel, v = 0,25 dämpft das Signal um 12 Dezibel und so weiter. Eine Volumeebene v = 1,0, die 0 Dezibel entspricht, ändert nicht die ursprüngliche Signalebene.

Audioanwendungen mit Benutzeroberflächen zum Steuern der Lautstärke zeigen in der Regel Schieberegler an, die Änderungen an wahrgenommener Lautheit generieren, die linear proportional zu Änderungen der Schiebereglerposition sind. Um eine lineare Beziehung zwischen wahrgenommener Lautheit und Schiebereglerposition zu erzeugen, muss die Anwendung eine nicht lineare Beziehung zwischen der Lautstärkestufe v und der Position des Schiebereglers definieren. Weitere Informationen finden Sie unter [Audio-Tapered Volume Controls](audio-tapered-volume-controls.md).

Wie bereits erläutert, zeigt das Systemprogramm zur Volumesteuerung (Sndvol) Volumeschieberegler für die Audiositzungen an, die auf jedem Audiorenderinggerät abspielt werden. Diese Schieberegler werden im Gruppenfeld Anwendungen **im** Fenster SndVol angezeigt. In der Regel enthält jede Sitzung alle Wiedergabestreams aus einem bestimmten Anwendungsfenster. Über die Schieberegler im Sndvol-Fenster steuern Benutzer die Lautstärkeebenen einzelner Audioanwendungen.

Im Allgemeinen sollte eine Anwendung alle Wiedergabestreams derselben Audiositzung zuweisen. WASAPI verhindert nicht, dass eine Anwendung ihre Wiedergabestreams auf mehrere Sitzungen verteilt. Die daraus resultierende Verbreitung von Volumeschiebereglern in Sndvol kann jedoch benutzerverwirrend sein.

Optional kann in einem Anwendungsfenster ein Volumeschieberegler angezeigt werden. Der Anwendungsschieberegler sollte jederzeit den Zustand des entsprechenden Sndvol-Schiebereglers widerspiegeln. Wenn der Benutzer also die Lautstärke durch Bewegen des Schiebereglers im Anwendungsfenster ändert, sollte der entsprechende Schieberegler im Sndvol-Fenster zusammen mit dem Schieberegler der Anwendung bewegt werden. Wenn der Benutzer den Sndvol-Schieberegler verschiebt, sollte der Schieberegler der Anwendung zusammen mit dem Sndvol-Schieberegler bewegt werden.

Zur Unterstützung dieses Verhaltens implementiert WASAPI die [**ISimpleAudioVolume-Schnittstelle.**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) Wenn der Benutzer den Anwendungsschieberegler verschiebt, ruft die Anwendung die [**ISimpleAudioVolume::SetMasterVolume-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume) auf, um die Sitzungsvolumeebene entsprechend anzupassen. Sndvol überwacht Volumeänderungen, die mit dieser Methode vorgenommen wurden, und spiegelt die Änderungen an den angezeigten Volumeschiebereglern wider. Darüber hinaus kann eine Anwendung Benachrichtigungen über Änderungen des Sitzungsvolumes empfangen, die der Benutzer über Sndvol vor sich geht. Zu diesem Zweck implementiert die Anwendung eine [**IAudioSessionEvents-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) und registriert die Schnittstelle bei WASAPI. Danach empfängt die Anwendung jedes Mal, wenn der Benutzer die Sitzungsvolumeebene über Sndvol ändert, einen Benachrichtigungsaufruf über die [**IAudioSessionEvents::OnSimpleVolumeChanged-Methode.**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) Ein Codebeispiel, das eine **IAudioSessionEvents-Schnittstelle** implementiert, finden Sie unter [AudioSitzungsereignisse](audio-session-events.md). Ein Codebeispiel, das eine **IAudioSessionEvents-Schnittstelle** registriert, finden Sie unter [Audioereignisse für Ältere Audioanwendungen.](audio-events-for-legacy-audio-applications.md)

Die **ISimpleAudioVolume-Schnittstelle** wendet dieselbe Lautstärkeebene gleichmäßig auf alle Kanäle in einer Audiositzung an. Obwohl diese Schnittstelle die Volumesteuerungsanforderungen der meisten Anwendungen erfüllen sollte, erfordern einige Anwendungen möglicherweise speziellere Volumesteuerungsfunktionen. Die [**IAudioStreamVolume-Schnittstelle**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) steuert das Volume eines einzelnen Streams in einer Sitzung relativ zu den anderen Streams in der Sitzung. **IAudioStreamVolume ermöglicht** es einem Client auch, die Volumeebenen aller Kanäle im Stream einzeln zu steuern. Beispielsweise kann eine Anwendung diese Funktion verwenden, um Audioeffekte zu erzielen, z. B. das Simulieren der räumlichen Bewegung einer Audioquelle durch Schwenken von links nach rechts. Eine weitere spezialisierte Schnittstelle, [**IChannelAudioVolume,**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)steuert die Volumeebenen der einzelnen Kanäle in einer Sitzung. Beispielsweise könnte eine Anwendung **IChannelAudioVolume** verwenden, um Ausgleichssteuerelemente für ein stereophones Soundsystem zu implementieren.

Die Volumeschieberegler im Feld **Anwendungen** in Sndvol spiegeln nur Volumeänderungen wider, die über die **ISimpleAudioVolume-Schnittstelle vorgenommen** werden. Sie spiegeln keine Volumeänderungen wider, die über die **Schnittstellen IAudioStreamVolume** und **IChannelAudioVolume vorgenommen** werden. Obwohl einige Anwendungen es Benutzern ermöglichen, Volumeeinstellungen direkt oder indirekt über **IAudioStreamVolume** und **IChannelAudioVolume** zu steuern, sollten Entwickler vermeiden, Anwendungsschieberegler für diese Volumeeinstellungen zu präsentieren, die Benutzer wahrscheinlich mit den Volumeschiebereglern in Sndvol verwechseln. Andernfalls kann ein Benutzer einen Anwendungsschieberegler verschieben, der erwartet, dass die Änderung in einem Sndvol-Schieberegler widergespiegelt wird, und verwirrend werden, wenn keine solche Änderung auftritt. Entwickler können dieses Problem durch einen sorgfältigen Entwurf der Benutzeroberfläche vermeiden.

Die effektive Lautstärke jedes Kanals im Sitzungsuntermix, wie von den Sprechern gehört, ist das Produkt der folgenden vier Faktoren auf Volumeebene:

-   Die Pro-Kanal-Volumeebenen der Streams in der Sitzung, die Clients über die Methoden in der **IAudioStreamVolume-Schnittstelle steuern** können.
-   Die Pro-Kanal-Volumeebene der Sitzung, die Clients über die Methoden in der **IChannelAudioVolume-Schnittstelle steuern** können.
-   Die Mastervolumeebene der Sitzung, die Clients über die Methoden in der **ISimpleAudioVolume-Schnittstelle steuern** können.
-   Die richtlinienbasierte Volumeebene der Sitzung, die das System dynamisch ändert, wenn sich die globale Mischung ändert.

Jeder der vier Faktoren auf Volumeebene in der vorangehenden Liste ist ein Wert im Bereich von 0,0 bis 1,0, wobei 0,0 für Stille und 1,0 für vollständige Lautstärke (keine Dämpfung) steht. Die effektive Volumeebene ist auch ein Wert im Bereich von 0,0 bis 1,0.

Die Audio-Engine wendet die effektive Volumeebene für jeden Kanal auf die Kanäle in einem Stream an, bevor der Stream mit den anderen Streams in der Audiositzung gemischt wird. Wenn Beispielwerte in einem Kanal 0 Dezibel überschreiten, nachdem sie von der Audio-Engine mit der effektiven Lautstärkeebene multipliziert wurden, schneide die Engine die Beispiele aus, bevor sie dem Sitzungsuntermix hinzugefügt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lautstärkeregler](volume-controls.md)
</dt> </dl>

 

 



