---
title: XAudio2-Funktionen
description: Dieser Abschnitt enthält Informationen zu Funktionen, die von der Microsoft XAudio2-API bereitgestellt werden.
ms.assetid: 870a0425-3226-7848-bcc0-0ba7145135cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd8bcfdb00565d6f8bbc31ae0ee6a24f106dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351772"
---
# <a name="xaudio2-functions"></a>XAudio2-Funktionen

Dieser Abschnitt enthält Informationen zu Funktionen, die von der Microsoft XAudio2-API bereitgestellt werden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreatefx"**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx)<br/>                                                                     | Erstellt eine Instanz des angeforderten [xapofx](xapofx-overview.md) -Effekts.<br/>                                                                                                                                                         |
| [**"Kreatehrtfapo"**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo)<br/>                                                           | Erstellt eine Instanz der [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo) -Schnittstelle für die Verarbeitung von Head-Related Transfer Function (HRTF).<br/>                                                                                                                  |
| [**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative)<br/>                                 | Eine Inline Funktion, die die Parameter I3DL2 (Interactive 3D audiorendering Guidelines Level 2,0) in Native XAudio2-Parameter konvertiert.<br/>                                                                                                 |
| [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)<br/>                                                   | Berechnet DSP-Einstellungen in Bezug auf 3D-Parameter.<br/>                                                                                                                                                                             |
| [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)<br/>                                                 | Legt alle globalen 3D-audiokonstanten fest.<br/>                                                                                                                                                                                                |
| [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels)<br/>                       | Inline Funktion, die einen Wert für das Amplitude-Verhältnis in einen Dezibelskala-Wert konvertiert.<br/>                                                                                                                                                         |
| [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create)<br/>                                                           | Erstellt ein neues **XAudio2** -Objekt und gibt einen Zeiger auf die [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) -Schnittstelle zurück.<br/>                                                                                                                              |
| [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)<br/>                                               | Erstellt ein neues "Reverb-Audioverarbeitungs Objekt" (APO) und gibt einen Zeiger darauf zurück.<br/>                                                                                                                                                   |
| [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter)<br/>                                     | Erstellt ein neues Volume Meter-Audioverarbeitungs Objekt (APO) und gibt einen Zeiger darauf zurück.<br/>                                                                                                                                              |
| [**XAudio2CutoffFrequencyToOnePoleCoefficient**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoonepolecoefficient)<br/> | Inline Funktion, die von in Hertz ausgedrückten Filter Umstellungs Frequenzen in die Filterkoeffizienten konvertiert, die mit dem **Frequency** -Element der [**XAUDIO2 \_ Filter \_ Parameters**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) -Struktur verwendet werden.<br/>   |
| [**XAudio2CutoffFrequencyToRadians**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoradians)<br/>                       | Eine Inline Funktion, die von den in Hertz ausgedrückten Filtern von Umstellungs Frequenzen in die Bogenmaß Wert Frequency-Werte konvertiert, die im **Frequency** -Element der [**XAUDIO2 \_ Filter \_ Parameters**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) -Struktur verwendet werden.<br/> |
| [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio)<br/>                       | Inline Funktion, die einen Dezibelskala-Wert in einen Wert für das Amplitude-Verhältnis konvertiert.<br/>                                                                                                                                                         |
| [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones)<br/>                     | Inline Funktion, die einen Wert für das Frequency-Verhältnis in einen Wert vom Typ"Wert" konvertiert.<br/>                                                                                                                                                         |
| [**XAudio2RadiansToCutoffFrequency**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2radianstocutofffrequency)<br/>                       | Eine Inline Funktion, die von den in XAUDIO2 Filter-Parametern verwendeten radiin- [**\_ \_ Parametern**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) zurück zu absoluten Frequenzen in Hertz konvertiert.<br/>                                                          |
| [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio)<br/>                     | Inline Funktion, die einen Wert vom Typ"Wert" in einen Wert für das Frequency-Verhältnis konvertiert.<br/>                                                                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XAudio2::P-rogrammverweis](programming-reference.md)
</dt> </dl>

 

 




