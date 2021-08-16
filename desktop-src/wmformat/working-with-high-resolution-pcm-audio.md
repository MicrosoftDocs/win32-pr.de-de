---
title: Arbeiten mit High-Resolution PCM Audio
description: Arbeiten mit High-Resolution PCM Audio
ms.assetid: 422a78f9-0f43-4edb-acaf-7f6e3f4a1cb8
keywords:
- Advanced Systems Format (ASF), pcm-Audio mit hoher Auflösung
- ASF (Advanced Systems Format), pcm-Audio mit hoher Auflösung
- Profile, pcm-Audio mit hoher Auflösung
- Codecs, pcm-Audio mit hoher Auflösung
- Advanced Systems Format (ASF), PCM-Audio
- ASF (Advanced Systems Format), PCM-Audio
- Profile, PCM-Audio
- Codecs, PCM-Audio
- Pcm-Audio mit hoher Auflösung
- PCM-Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a76cfb8397cacd6d39f62ea3594c8be655f4543e0b48b60cafbf15b9783c7fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194855"
---
# <a name="working-with-high-resolution-pcm-audio"></a>Arbeiten mit High-Resolution PCM Audio

Einige der Eingabeformate für den Windows Media Audio 9 Professional Codec und den Windows Media Audio 9 Lossless Codec sind PCM-Formate mit hoher Auflösung. Dies sind PCM-Formate mit mehr als zwei Kanälen oder mehr als 16 Bits pro Beispiel (Audio mit mehr als zwei Kanälen wird auch als Multichannelaudio bezeichnet).

Diese Formate werden mithilfe einer strukturierten Erweiterung der [**WAVEFORMATEX-Struktur**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) namens [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85))konfiguriert. Die **WAVEFORMATEXTENSIBLE-Struktur** enthält Informationen zu den in der Audiodatei enthaltenen Kanälen. Diese Struktur ist erforderlich, wenn PCM-Audio mit hoher Auflösung verwendet wird, da einige Windows-APIs keine **WAVEFORMATEX-Strukturen** akzeptieren, die werte mit hoher Auflösung enthalten.

PCM-Formate mit hoher Auflösung weisen 22 Bytes erweiterter Daten auf, die im **cbSize-Member** der **WAVEFORMATEX-Struktur** angegeben sind. Bei Windows Medienaudioformaten wird die **WAVEFORMATEXTENSIBLE-Struktur** nicht verwendet, es werden jedoch erweiterte Daten an die **WAVEFORMATEX-Struktur** angefügt.

Die Windows Media-Audiocodecs unterstützen nur die Decodierung in PCM-Formate mit hoher Auflösung, wenn die Anwendung auf Windows XP oder höher ausgeführt wird. In früheren Versionen von Microsoft Windows decodieren die Codecs in ein Format mit maximal 16 Bits pro Stichprobe und 2 Kanälen. Darüber hinaus müssen Sie angeben, dass der Codec in high-definition PCM decodiert werden soll, indem Sie die Ausgabeeinstellung g \_ wszEnableDiscreteOutput mithilfe der [**IWMReaderAdvanced2::SetOutputSetting-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) auf **TRUE** festlegen. Nach diesem Aufruf enthalten die vom Reader aufzählten Ausgaben High-Definition-Formate.

Multichannelaudio erfordert mehr Konfiguration. Weitere Informationen finden Sie unter [Lesen von Multichannelaudio.](reading-multichannel-audio.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Eingaben**](working-with-inputs.md)
</dt> </dl>

 

 