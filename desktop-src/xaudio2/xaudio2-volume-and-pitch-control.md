---
description: In diesem Thema wird das XAudio2 Volume und die Steuerelement-Steuerelement
ms.assetid: dedc2d01-af83-d7d2-5b64-743dcebc83f7
title: XAudio2 Volume und Tonhöhe-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2526cfa50c0260e90e1aae9e2bce21d507dc2e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216949"
---
# <a name="xaudio2-volume-and-pitch-control"></a>XAudio2 Volume und Tonhöhe-Steuerelement

In diesem Thema wird das XAudio2 Volume und die Steuerelement-Steuerelement

## <a name="volume-control"></a>Volumesteuerung

Volumeebenen werden als Gleit Komma-Amplitude-multipangen zwischen-XAUDIO2 \_ Max \_ Volume \_ Level und XAUDIO2 \_ Max \_ Volume \_ Level (-224 bis 224) ausgedrückt, mit einem maximalen Gewinn von 144,5 DB. Ein Volume von 1,0 bedeutet, dass es keine Dämpfung oder einen Gewinn gibt. 0 bedeutet Stille. und negative Ebenen können verwendet werden, um die Audiophase umzukehren. In XAudio2. h werden zwei Inline Funktionen bereitgestellt, um zwischen den volumeeinheiten zu konvertieren: [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio) und [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels).

Sie können eine Volumeebene auf das Audiogerät an mehreren Punkten anwenden, während Sie durch das XAudio2 Graph fließt:

-   Alle Sprachtypen wenden eine gesamte Volumeebene auf die Eingabe an, die Sie mithilfe der [**IXAudio2Voice:: SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) -Methode steuern. In Submix-und Mastering-stimmen wird die gesamte Volumeebene direkt vor der integrierten Filter-und Wirkungskette der Stimme angewendet. In den Quell stimmen wird die gesamte Volumeebene nach dem integrierten Filter und der Wirkungskette der Stimme angewendet.
-   Stimmen wenden eine pro-Channel-Volumeebene auf die Ausgabe an, die Sie mithilfe der [**IXAudio2Voice:: setchannelvolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) -Methode steuern. Die Volumeebene pro Kanal wird unmittelbar nach der abschließenden Stichprobenrate der Stimme und vor dem Senden an andere Stimmen angewendet.
-   Jede Verbindung zwischen einer Sprache und einer anderen verfügt über eine Tabelle mit Ebenen, mit denen Audiodaten von jedem Quell Kanal an jeden Zielchannel gesendet werden, der mithilfe der [**IXAudio2Voice:: setoutputmatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) -Methode gesteuert wird.

Alle allgemeinen Volumes und kanalvolumes werden anfänglich standardmäßig auf 1,0 eingestellt. Alle Matrizen auf Sende Ebene werden standardmäßig auf geeignete Werte festgesetzt, die Signalleistung und Kanal Positionierung so genau wie möglich beibehalten. Ausführliche Informationen finden Sie in der Übersicht über die [XAudio2-Standard Kanal Zuordnung](xaudio2-default-channel-mapping.md) .

> [!Note]  
> XAudio2 passt volumeebenen automatisch basierend auf den Lautsprecher Einstellungen des Benutzers an, um eine konsistente Volumeebene über Konfigurationen hinweg beizubehalten. Wenn die Einstellungen des Benutzers nicht mit der physischen Konfiguration identisch sind, ist das Volume im Vergleich zu einem System mit exakten Einstellungen entweder zu laut oder zu weich. Ein System, das für 5,1-umschließende audioreferenten konfiguriert ist, für die nur zwei Sprecher verbunden sind, klingt beispielsweise zu weich. XAudio2 kann nicht erkennen, ob die Benutzer Sprechereinstellungen ordnungsgemäß mit dem physischen Setup in Einklang stehen.

 

## <a name="pitch-control"></a>Pitch-Steuerelement

Die Ziffern werden als Eingabe Raten-/ausgaberaten-Verhältnis zwischen 1/1024 und 1024/1 (einschließlich) ausgedrückt. Mit einem Verhältnis von 1/1024 wird die Tonhöhe um 10 Oktaven gesenkt, während ein Verhältnis von 1024/1 durch 10 Oktaven ausgelöst wird. Sie können nur die [**IXAudio2SourceVoice:: setfrequencyratio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) -Methode verwenden, um die Änderungen an den Quell Stimmen zu übernehmen. Dies gilt nur, wenn Sie nicht mit dem XAUDIO2 \_ Voice \_ nopitch-Flag erstellt wurden. Das standardmäßige Häufigkeits Verhältnis ist 1/1, d. h. keine Änderung der Tonhöhe. In XAudio2. h werden zwei Inline Funktionen bereitgestellt, um zwischen den Häufigkeits Verhältnissen und den folgenden Seiten zu konvertieren: [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones) und [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Volume und Steuerelement](volume-and-pitch-control.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[Vorgehensweise: Ändern der Stimm Schrift](how-to--change-voice-pitch.md)
</dt> <dt>

[Vorgehensweise: Ändern des sprach Volumens](how-to--change-voice-volume.md)
</dt> </dl>

 

 
