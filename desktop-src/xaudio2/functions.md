---
title: XAudio2-Funktionen
description: Dieser Abschnitt enthält Informationen zu Funktionen, die von der Microsoft XAudio2-API bereitgestellt werden.
ms.assetid: 870a0425-3226-7848-bcc0-0ba7145135cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b950ce33f55a4b834f3ee7a068f613e144c2e30633c67e887b8a24789140a618
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109650"
---
# <a name="xaudio2-functions"></a>XAudio2-Funktionen

Dieser Abschnitt enthält Informationen zu Funktionen, die von der Microsoft XAudio2-API bereitgestellt werden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                       | Beschreibung                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx)<br/>                                                                     | Erstellt eine Instanz des angeforderten [XAPOFX-Effekts.](xapofx-overview.md)<br/>                                                                                                                                                         |
| [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo)<br/>                                                           | Erstellt eine Instanz der [**IXAPO-Schnittstelle**](/windows/desktop/api/XAPO/nn-xapo-ixapo) für die Verarbeitung der Head-Related Transfer Function (HRTF).<br/>                                                                                                                  |
| [**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative)<br/>                                 | Inlinefunktion, die I3DL2-Parameter (Interactive 3D Audio Rendering Guidelines Level 2.0) in native XAudio2-Parameter konvertiert.<br/>                                                                                                 |
| [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)<br/>                                                   | Berechnet DSP-Einstellungen in Bezug auf 3D-Parameter.<br/>                                                                                                                                                                             |
| [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)<br/>                                                 | Legt alle globalen 3D-Audiokonstanten fest.<br/>                                                                                                                                                                                                |
| [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels)<br/>                       | Inlinefunktion, die einen Amplitudenverhältniswert in einen Dezibelwert konvertiert.<br/>                                                                                                                                                         |
| [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create)<br/>                                                           | Erstellt ein neues **XAudio2-Objekt** und gibt einen Zeiger auf seine [**IXAudio2-Schnittstelle**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) zurück.<br/>                                                                                                                              |
| [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)<br/>                                               | Erstellt ein neues Audioverarbeitungsobjekt (Audio Processing Object, APO) und gibt einen Zeiger darauf zurück.<br/>                                                                                                                                                   |
| [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter)<br/>                                     | Erstellt ein neues Audioverarbeitungsobjekt (Volume Meter Audio Processing Object, APO) und gibt einen Zeiger darauf zurück.<br/>                                                                                                                                              |
| [**XAudio2CutoffFrequencyToOnePoleCoefficient**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoonepolecoefficient)<br/> | Inlinefunktion, die von filter cutoff frequencys ausgedrückt in hertz in die Filterkoeffizienten konvertiert, die mit dem **Frequency-Member** der [**XAUDIO2 \_ FILTER \_ PARAMETERS-Struktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) verwendet werden.<br/>   |
| [**XAudio2CutoffFrequencyToRadians**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoradians)<br/>                       | Inlinefunktion, die von filter cutoff frequencys ausgedrückt in hertz in die Radianfrequenzwerte konvertiert, die im **Frequency-Member** der [**XAUDIO2 \_ FILTER \_ PARAMETERS-Struktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) verwendet werden.<br/> |
| [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio)<br/>                       | Inlinefunktion, die einen Dezibelwert in einen Amplitudenverhältniswert konvertiert.<br/>                                                                                                                                                         |
| [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones)<br/>                     | Inlinefunktion, die einen Frequency Ratio-Wert in einen Semitonwert konvertiert.<br/>                                                                                                                                                         |
| [**XAudio2RadiansToCutoffFrequency**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2radianstocutofffrequency)<br/>                       | Inlinefunktion, die von den in [**XAUDIO2 \_ FILTER \_ PARAMETERS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) verwendeten Radianfrequenzen zurück in absolute Frequenzen in Hertz konvertiert.<br/>                                                          |
| [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio)<br/>                     | Inlinefunktion, die einen Semitonwert in einen Frequency Ratio-Wert konvertiert.<br/>                                                                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XAudio2::P rogramming-Referenz](programming-reference.md)
</dt> </dl>

 

 




