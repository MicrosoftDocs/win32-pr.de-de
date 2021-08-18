---
description: In diesem Thema wird die Lautstärke- und Tonhöhensteuerung von XAudio2 beschrieben.
ms.assetid: dedc2d01-af83-d7d2-5b64-743dcebc83f7
title: XAudio2-Steuerelement für Lautstärke und Tonhöhe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6376ad599b496a640b49d7eb539e1da774e31c71a3bf2a8e0c863fc140e19b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962489"
---
# <a name="xaudio2-volume-and-pitch-control"></a>XAudio2-Steuerelement für Lautstärke und Tonhöhe

In diesem Thema wird die Lautstärke- und Tonhöhensteuerung von XAudio2 beschrieben.

## <a name="volume-control"></a>Volumesteuerung

Volumeebenen werden als Gleitkomma-Amplitudenmultiplikatoren zwischen -XAUDIO2 MAX VOLUME LEVEL und \_ \_ \_ XAUDIO2 MAX VOLUME LEVEL (-224 bis 224) mit einem maximalen Gewinn von \_ \_ \_ 144,5 dB ausgedrückt. Ein Volume von 1,0 bedeutet, dass es keine Dämpfung oder keinen Gewinn gibt. 0 bedeutet Stille; und negative Ebenen können verwendet werden, um die Audiophase rückgängig zu machen. In XAudio2.h werden zwei Inlinefunktionen für die Konvertierung zwischen Volumeeinheiten bereitgestellt: [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio) und [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels).

Sie können eine Lautstärkeebene auf die Audiodaten an mehreren Punkten anwenden, während sie durch das XAudio2-Diagramm fließen:

-   Alle Stimmtypen wenden eine allgemeine Lautstärkeebene auf ihre Eingabe an, die sie mithilfe der [**IXAudio2Voice::SetVolume-Methode**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) steuern. Bei Untermischungs- und Masterstimmen wird die gesamte Lautstärke kurz vor der integrierten Filter- und Effektkette der Stimme angewendet. Bei Quellstimmen wird die gesamte Lautstärke nach der integrierten Filter- und Effektkette der Stimme angewendet.
-   Stimmen wenden eine Volumenebene pro Kanal auf ihre Ausgabe an, die sie mithilfe der [**IXAudio2Voice::SetChannelVolumes-Methode**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) steuern. Die Volumenebene pro Kanal wird direkt nach der endgültigen Umwandlung der Stichprobenrate der Stimme angewendet, und bevor sie an andere Stimmen gesendet wird.
-   Jede Verbindung zwischen einer Stimme und einer anderen verfügt über eine Tabelle mit Ebenen, die verwendet werden, um Audiodaten von jedem Quellkanal an jeden Zielkanal zu senden, der mithilfe der [**IXAudio2Voice::SetOutputMatrix-Methode**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) gesteuert wird.

Alle Gesamtvolumes und Kanalvolumes sind anfänglich standardmäßig auf 1.0 festgelegt. Alle Matrizen auf Sendeebene werden standardmäßig auf geeignete Werte festgelegt, die die Signalleistung und Kanalpositionierung so genau wie möglich beibehalten. Weitere Informationen finden Sie in der [Übersicht über die XAudio2-Standardkanalzuordnung.](xaudio2-default-channel-mapping.md)

> [!Note]  
> XAudio2 passt die Lautstärkeebenen automatisch basierend auf den Sprechereinstellungen des Benutzers an, um eine konsistente Volumeebene für alle Konfigurationen zu erhalten. Wenn die Einstellungen des Benutzers nicht mit der physischen Konfiguration übereinstimmen, ist das Volume im Vergleich zu einem System mit genauen Einstellungen entweder zu laut oder zu weich. Beispielsweise klingt ein für 5.1 konfiguriertes System, bei dem nur zwei Lautsprecher verbunden sind, zu weich. XAudio2 kann nicht erkennen, ob die Einstellungen des Benutzerlaut sprechers ordnungsgemäß mit der physischen Einrichtung übereinstimmen.

 

## <a name="pitch-control"></a>Pitch-Steuerelement

Tonhöhen werden als Verhältnisse zwischen Eingaberate und Ausgaberate zwischen 1/1.024 und 1.024/1 ausgedrückt, einschließlich. Ein Verhältnis von 1/1.024 senkt die Tonhöhe um 10 Oktaven, während ein Verhältnis von 1.024/1 die Tonhöhe um 10 Oktaven erhöht. Sie können die [**IXAudio2SourceVoice::SetFrequencyRatio-Methode**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) nur verwenden, um Tonhöhenanpassungen auf Quellstimmen anzuwenden, und nur, wenn sie nicht mit dem XAUDIO2 \_ VOICE \_ NOPITCH-Flag erstellt wurden. Das Standardfrequenzverhältnis ist 1/1, d.&a; keine Tonhöhenänderung. In XAudio2.h werden zwei Inlinefunktionen bereitgestellt, um zwischen Häufigkeitsverhältnisse und Semitonen zu konvertieren: [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones) und [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lautstärke- und Tonhöhensteuerung](volume-and-pitch-control.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[How to: Change Voice Pitch](how-to--change-voice-pitch.md)
</dt> <dt>

[How to: Change Voice Volume](how-to--change-voice-volume.md)
</dt> </dl>

 

 
