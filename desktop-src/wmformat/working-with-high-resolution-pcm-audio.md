---
title: Arbeiten mit High-Resolution PCM-Audiodatei
description: Arbeiten mit High-Resolution PCM-Audiodatei
ms.assetid: 422a78f9-0f43-4edb-acaf-7f6e3f4a1cb8
keywords:
- Advanced Systems Format (ASF), hochauflösende PCM-Audiodaten
- ASF (Advanced Systems Format), hochauflösende PCM-Audiodaten
- Profile, hochauflösende PCM-Audiodaten
- Codecs, hochauflösende PCM-Audiodaten
- Advanced Systems Format (ASF), PCM-Audiodatei
- ASF (Advanced Systems Format), PCM-Audiodatei
- Profile, PCM-Audiodaten
- Codecs, PCM-Audiodaten
- hochauflösende PCM-Audiodaten
- PCM-Audiodatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a45904072307e915065ba3a5946d5ef774c73b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948856"
---
# <a name="working-with-high-resolution-pcm-audio"></a>Arbeiten mit High-Resolution PCM-Audiodatei

Einige der Eingabeformate für den Windows Media Audio 9 Professional-Codec und den Windows Media Audio 9 verlustfreien Codec sind hochauflösende PCM-Formate. Dabei handelt es sich um PCM-Formate mit mehr als zwei Kanälen oder mehr als 16 Bits pro Stichprobe (Audiodaten mit mehr als zwei Kanälen werden auch als Multichannel-Audiodaten bezeichnet).

Diese Formate werden mit einer strukturierten Erweiterung der [**WaveFormatEx**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) -Struktur konfiguriert, die als [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85))bezeichnet wird. Die **WAVEFORMATEXTENSIBLE** -Struktur enthält Informationen zu den Kanälen, die in der Audiodatei enthalten sind. Diese Struktur ist erforderlich, wenn hochauflösende PCM-Audiodaten verwendet werden, da einige Windows-APIs keine **WaveFormatEx** -Strukturen akzeptieren, die Werte mit hoher Auflösung enthalten.

Hochauflösende PCM-Formate verfügen über 22 Byte erweiterte Daten, die im **CBSIZE** -Member der **WaveFormatEx** -Struktur angegeben werden. Bei Windows Media-Audioformaten mit hoher Auflösung wird die **WAVEFORMATEXTENSIBLE** -Struktur nicht verwendet, aber es werden erweiterte Daten an die **WaveFormatEx** -Struktur angehängt.

Die Windows Media-Audiocodecs unterstützen nur das Decodieren in hochauflösende PCM-Formate, wenn die Anwendung unter Windows XP oder höher ausgeführt wird. In früheren Versionen von Microsoft Windows decodieren die Codecs in ein Format mit maximal 16 Bits pro Stichprobe und 2 Kanälen. Außerdem müssen Sie angeben, dass der Codec in High-Definition PCM decodiert werden soll, indem Sie die \_ Ausgabe Einstellung g wszene ablediskreteoutput mithilfe der [**IWMReaderAdvanced2:: setoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) -Methode auf " **true** " festlegen. Nach dem Ausführen dieses Aufrufes werden die vom Reader aufgelisteten Ausgaben zu hoch Definitions Formaten.

Multichannel-Audiodaten erfordern mehr Konfiguration. Weitere Informationen finden Sie unter [Lesen von Multichannel-Audioinformationen](reading-multichannel-audio.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Eingaben**](working-with-inputs.md)
</dt> </dl>

 

 