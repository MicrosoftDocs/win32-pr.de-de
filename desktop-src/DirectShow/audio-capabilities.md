---
description: Audiofunktionen
ms.assetid: de96f6ee-b526-4ac2-93ac-a731f86ef5d5
title: Audiofunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd12f3e151a73c2a297d10fec4233ac0e931e11d8bf16e1068f6335c781ed6da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824230"
---
# <a name="audio-capabilities"></a>Audiofunktionen

Für Audiofunktionen gibt [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) ein Array von Paaren von [**AM MEDIA \_ \_ TYPE-**](/windows/win32/api/strmif/ns-strmif-am_media_type) und [**AUDIO STREAM \_ \_ CONFIG \_ CAPS-Strukturen**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) zurück. Wie beim Video können Sie dies verwenden, um alle Arten von Audiofunktionen auf dem Pin verfügbar zu machen, z. B. die Datenrate und ob mono oder stereo unterstützt wird.

Videobezogene Beispiele im Zusammenhang mit GetStreamCaps finden Sie unter [Videofunktionen.](video-capabilities.md)

Angenommen, Sie unterstützen das PCM-Wellenformat (Pulse Code Europe) (dargestellt durch die [**WAVEFORMATEX-Struktur)**](/previous-versions/dd757713(v=vs.85)) mit Samplingraten von 11.025, 22.050 und 44.100 Stichproben pro Sekunde, alle mit 8- oder 16-Bit-Mono oder Stereo. In diesem Fall würden Sie zwei Paare von Strukturen anbieten. Das erste Paar verfügt über eine **AUDIO \_ STREAM \_ CONFIG \_ CAPS-Funktionsstruktur,** die besagt, dass Sie mindestens 11.025 bis maximal 22.050 Stichproben pro Sekunde mit einer Granularität von 11.025 Stichproben pro Sekunde unterstützen (Granularität ist der Unterschied zwischen den unterstützten Werten); ein 8-Bit-Minimum bis ein maximales 16-Bit-Bit pro Stichprobe mit einer Granularität von 8 Bits pro Stichprobe; und mindestens einen Kanal und maximal zwei Kanäle. Der Medientyp des ersten Paars wäre Ihr PCM-Standardformat in diesem Bereich, z. B. 22 Kilohertz (kHz), 16-Bit-Stereo. Ihr zweites Paar wäre eine Funktion, die 44.100 für minimale und maximale Stichproben pro Sekunde anzeigt. 8-Bit (minimum) und 16-Bit (maximum) bits pro Stichprobe mit einer Granularität von 8 Bits pro Stichprobe; und mindestens einen Kanal und maximal zwei Kanäle. Der Medientyp ist Ihr Standardformat von 44 kHz, möglicherweise 44 kHz, 16-Bit-Stereo.

Wenn Sie Nicht-PCM-Wellenformate unterstützen, kann der von dieser Methode zurückgegebene Medientyp anzeigen, welche Nicht-PCM-Formate Sie unterstützen (mit einer Standardabtastrate, Bitrate und Kanälen) und die mit diesem Medientyp verbundene Funktionenstruktur beschreiben können, welche anderen Abtastraten, Bitraten und Kanäle Sie unterstützen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verfügbarmachen von Erfassungs- und Komprimierungsformaten](exposing-capture-and-compression-formats.md)
</dt> </dl>

 

 
