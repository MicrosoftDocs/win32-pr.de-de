---
description: XAudio2 ist eine audioapi auf niedriger Ebene. Es bietet eine Signalverarbeitung und eine Mischung für Spiele, die den Vorgänger, DirectSound und xaudio ähneln.
ms.assetid: c87be63a-58b5-9cd1-1f03-f32b5a858b2e
title: XAudio2-Einführung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7cde958256d9126746a07764dc0c792e88289c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362988"
---
# <a name="xaudio2-introduction"></a>XAudio2-Einführung

XAudio2 ist eine audioapi auf niedriger Ebene. Es bietet eine Signalverarbeitung und eine Mischung für Spiele, die den Vorgänger, DirectSound und xaudio ähneln.

XAudio2 ist die lang erwartete Ersetzung für DirectSound. Es werden mehrere ausstehende Probleme und Featureanforderungen behandelt.

## <a name="xaudio2-features"></a>XAudio2-Funktionen

Im folgenden finden Sie eine Liste der XAudio2 Features und neuen Funktionen, mit denen Entwickler die Leistung Ihrer Spiele verbessern können.

-   DSP-Effekte und sprach Filterung

    Die Auswirkungen digitaler Signal Verarbeitung (DSP) sind die Pixel-Shader von Audiodaten. Sie behandeln alles von der Transformation eines Sounds – das Umwandeln eines Pig-Klangs in ein niedriges, beängstigendes Monster – zum Platzieren von Sounds in der Spielumgebung mithilfe von Hall-und Okklusions-oder Hindernis filtern. XAudio2 bietet ein flexibles und leistungsfähiges DSP-Framework. Außerdem bietet es einen integrierten Filter für jede Stimme, um Filter Effekte mit geringem/hohem/banddurchlauf zu ermöglichen.

    Weitere Informationen zu DSP-Effekten und zum Filtern pro Sprache finden Sie unter [XAudio2-Audioeffekte](xaudio2-audio-effects.md) und [**IXAudio2Voice:: setfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) .

-   Submischen

    Bei der submischung werden mehrere Sounds in einem einzelnen Audiostream kombiniert, z. –. ein Engine-Ton, der aus zusammengesetzten Teilen besteht, die alle gleichzeitig abgespielt werden. Außerdem können Sie die unter Mischung verwenden, um ähnliche Teile eines Spiels zu verarbeiten und zu kombinieren. Beispielsweise können Sie alle Spiel Soundeffekte kombinieren, damit eine Einstellung für das Benutzer Volume angewendet werden kann, während eine separate Einstellung das Musik Volume steuert. In Kombination mit DSP bietet die submischung den Typ der Datenweiterleitung und-Verarbeitung, die für die heutigen Spiele benötigt werden. XAudio2 ermöglicht das Erstellen komplexer Sounds und Spiel Mischungen und ermöglicht so die unter Mischung beliebiger Ebenen.

    Weitere Informationen zur unter Mischung finden Sie unter [XAudio2 audiograph](xaudio2-audio-graph.md) und [XAudio2 Voices](xaudio2-voices.md) .

-   Komprimierte Audiounterstützung

    Eine der wichtigsten Funktionsanforderungen für DirectSound ist für komprimierte Audiounterstützung vorgesehen. XAudio2 unterstützt komprimierte Formate – ADPCM – nativ mit Lauf Zeit Komprimierung.

-   Erweiterte Unterstützung für Multichannel und Surround Sound

    Die Unterstützung für Multichannel, 3D und Surround Sound ist erweitert. 3D-und umschließende Sounds sind nun viel flexibler und transparenter. XAudio2 entfernt das 6-Kanal-Limit für Multichannel-Sounds und unterstützt Multichannel-Audiodaten auf einer beliebigen Multichannel-fähigen Audiokarte. Die Karte muss nicht Hardware beschleunigt werden.

-   Mehrstufige Verarbeitung

    Um die CPU-Auslastung zu minimieren, bietet XAudio2 die Technologie zum Erstellen mehrerer Audioverarbeitungs Diagramme mit geringem Geschwindigkeit. Dies kann die CPU-Auslastung erheblich verringern, indem es einem Spiel ermöglicht, Audiodaten mit der Geschwindigkeit des Quellmaterials zu verarbeiten, wenn die Rate kleiner als 48 kHz ist.

-   Nicht blockierendes API-Modell

    Mit wenigen Ausnahmen wird die Audioverarbeitungs-Engine durch einen XAudio2-Methoden aufrufnicht blockiert. Dies bedeutet, dass ein Client jederzeit sicher einen Satz von Methoden aufrufen ausführen kann, ohne dass Aufrufe mit langer Ausführungszeit blockiert werden, die Verzögerungen verursachen. Ausnahmen sind die [**IXAudio2Voice::D estroyvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-destroyvoice) -Methode (die die Engine blockieren kann, bis die Wiederherstellung der Stimme abgeschlossen ist) und die Methoden, die den audiothread beenden: [**IXAudio2:: stopengine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) und [**IXAudio2:: Release**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-release). Beachten Sie, dass die XAudio2-Methodenaufrufe die Audioverarbeitungs-Engine nicht blockieren, dass die XAudio2-Methoden kritische Abschnitte enthalten und in einigen Fällen blockiert werden können.

## <a name="when-to-use-xaudio2"></a>Verwendungszwecke von XAudio2

XAudio2 ist hauptsächlich für die Entwicklung Hochleistungs-audioengines für Spiele gedacht. Spieleentwicklern, die Soundeffekte und Hintergrundmusik zu ihren modernen Spielen hinzufügen möchten, bietet XAudio2 ein Modul für Audiodiagramme und zum Mischen mit geringer Latenz und Unterstützung für dynamische Puffer, synchrone Wiedergabe genau nach Beispiel und implizite Quellratenumwandlung. Im Vergleich zu WASAPI erfordert XAudio2 nur eine minimale Menge an Code, auch für komplexe Audiolösungen. Im Vergleich zur Media Foundation-Engine ist XAudio2 eine C++-API auf niedriger Ebene, die für die Verwendung in Spielen konzipiert ist.

Für Anwendungen, die nur eine reguläre Musikwiedergabe benötigen, ist die Media Foundation-Engine möglicherweise besser mit den Anforderungen der Anwendung zu vergleichen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> <dt>

[Erste Schritte](getting-started.md)
</dt> <dt>

[XAudio2-Programmierreferenz](programming-reference.md)
</dt> </dl>

 

 
