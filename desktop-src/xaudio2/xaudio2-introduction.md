---
description: XAudio2 ist eine Low-Level-Audio-API. Es bietet eine Signalverarbeitungs- und Mischungs-Grundlage für Spiele, die den Vorgängern DirectSound und XAudio ähnelt.
ms.assetid: c87be63a-58b5-9cd1-1f03-f32b5a858b2e
title: XAudio2-Einführung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a966e9682a7f605864c0374a588d4b7eb3724036fe284bd6d92c64080e9225
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589900"
---
# <a name="xaudio2-introduction"></a>XAudio2-Einführung

XAudio2 ist eine Low-Level-Audio-API. Es bietet eine Signalverarbeitungs- und Mischungs-Grundlage für Spiele, die den Vorgängern DirectSound und XAudio ähnelt.

XAudio2 ist der lange erwartete Ersatz für DirectSound. Es werden mehrere ausstehende Probleme und Featureanforderungen behandelt.

## <a name="xaudio2-features"></a>XAudio2-Funktionen

Im Folgenden finden Sie eine Liste mit XAudio2-Features und neuen Funktionen, mit denen Entwickler die Leistung in ihren Spielen verbessern können.

-   DSP-Effekte und Filterung pro Stimme

    DSP-Effekte (Digital Signal Processing) sind die Pixel-Shader von Audio. Sie verarbeiten alles, von der Transformation eines Sounds – von der Umwandlung einer Pig-Queal in einen niedrigen, beängstigenden Sound bis hin zum Platzieren von Sounds in der Spielumgebung mit Hall und Okklusion oder Sperrfilterung. XAudio2 bietet ein flexibles und leistungsstarkes DSP-Framework. Außerdem bietet sie einen integrierten Filter für jede Stimme, um effiziente Filtereffekte für niedrige/hohe/Bandpassfilterung zu erzielen.

    Weitere Informationen zu DSP-Effekten und zum Filtern pro Stimme finden Sie unter [XAudio2 Audio Effects](xaudio2-audio-effects.md) und [**IXAudio2Voice::SetFilterParameters.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)

-   Untermischung

    Bei der Untermischung werden mehrere Sounds zu einem einzelnen Audiostream kombiniert, z. B. ein Engine-Sound, der aus zusammengesetzten Teilen besteht, die alle gleichzeitig abspielt. Außerdem können Sie mithilfe von Untermischung ähnliche Teile eines Spiels verarbeiten und kombinieren. Beispielsweise können Sie alle Spielklangeffekte kombinieren, um die Anwendung einer Benutzer-Volumeeinstellung zu ermöglichen, während eine separate Einstellung die Musikvolumen steuert. In Kombination mit DSP bietet die Untermischung die Art des Datenroutings und der Verarbeitung, die für heutige Spiele erforderlich ist. XAudio2 ermöglicht eine beliebige Untermischung, sodass komplexe Sounds und Spielmischungen erstellt werden können.

    Weitere [Informationen zum Untermixen finden](xaudio2-audio-graph.md) Graph XAudio2 Audio Graph und [XAudio2-Stimmen.](xaudio2-voices.md)

-   Unterstützung komprimierter Audiodaten

    Eine der wichtigsten Featureanforderungen für DirectSound war die Unterstützung komprimierter Audiodaten. XAudio2 unterstützt komprimierte Formate – ADPCM – nativ mit Laufzeitdekomprimierung.

-   Erweiterte Multichannel- und Surround Sound-Unterstützung

    Die Unterstützung für Multichannel-, 3D- und Surround-Sound wird erweitert. 3D- und Umschließen-Sound sind jetzt viel flexibler und transparenter. XAudio2 entfernt die 6-Kanal-Grenze für Multichannel-Sounds und unterstützt Multichannel-Audio auf jeder Multichannel-fähigen Audiokarte. Die Karte muss nicht hardwarebeschleunigt sein.

-   Multirate Processing

    Um die CPU-Auslastung zu minimieren, stellt XAudio2 die Technologie zum Erstellen mehrerer Audioverarbeitungsdiagramme mit niedriger Rate zur Anwendung. Dies kann die CPU-Auslastung erheblich reduzieren, indem ein Spiel audio mit der Rate des Quellmaterials verarbeiten kann, wenn die Rate kleiner als 48 kHz ist.

-   API-Modell ohne Blockierung

    Mit wenigen Ausnahmen blockiert ein XAudio2-Methodenaufruf die Audioverarbeitungs-Engine nicht. Dies bedeutet, dass ein Client jederzeit sicher eine Reihe von Methodenaufrufen ausführen kann, ohne bei Aufrufen mit langer Ausführungszeit zu blockieren, was zu Verzögerungen führt. Ausnahmen sind die [**IXAudio2Voice::D esticeVoice-Methode**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-destroyvoice) (die die Engine blockieren kann, bis die zerstörte Stimme verarbeitet ist) und die Methoden, die den Audiothread beenden: [**IXAudio2::StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) und [**IXAudio2::Release**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-release). Beachten Sie, dass XAudio2-Methodenaufrufe zwar die Audioverarbeitungs-Engine nicht blockieren, die XAudio2-Methoden jedoch kritische Abschnitte enthalten und unter bestimmten Umständen selbst blockiert werden können.

## <a name="when-to-use-xaudio2"></a>Verwendung von XAudio2

XAudio2 ist hauptsächlich für die Entwicklung leistungsstarker Audio-Engines für Spiele vorgesehen. Spieleentwicklern, die Soundeffekte und Hintergrundmusik zu ihren modernen Spielen hinzufügen möchten, bietet XAudio2 ein Modul für Audiodiagramme und zum Mischen mit geringer Latenz und Unterstützung für dynamische Puffer, synchrone Wiedergabe genau nach Beispiel und implizite Quellratenumwandlung. Im Vergleich zu WASAPI erfordert XAudio2 nur eine minimale Menge an Code, auch für komplexe Audiolösungen. Im Vergleich zur Media Foundation-Engine ist XAudio2 eine C++-API mit niedriger Latenz, die für die Verwendung in Spielen entwickelt wurde.

Für Anwendungen, die einfach reguläre Musikwiedergabe benötigen, ist die Media Foundation-Engine möglicherweise eine bessere Übereinstimmung mit den Anforderungen der Anwendung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> <dt>

[Erste Schritte](getting-started.md)
</dt> <dt>

[XAudio2-Programmierreferenz](programming-reference.md)
</dt> </dl>

 

 
