---
description: Audiofunktionen
ms.assetid: de96f6ee-b526-4ac2-93ac-a731f86ef5d5
title: Audiofunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2cf02927b69d807f400c4185a7d4ddbdd14322
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522528"
---
# <a name="audio-capabilities"></a>Audiofunktionen

Für Audiofunktionen gibt [**iamstreamconfig:: getstreamcaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) ein Array von Paaren von " [**am \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) " und " [**\_ Audiostream \_ config \_ "-**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) Strukturen zurück. Wie bei Video können Sie damit auch alle Arten von Audiofunktionen auf der PIN verfügbar machen, wie z. b. die Daten Rate und ob Mono oder Stereo unterstützt wird.

Video bezogene Beispiele in Bezug auf getstreamcaps finden Sie unter [Videofunktionen](video-capabilities.md).

Angenommen, Sie unterstützen das PCM (Pulse Code Modulation)-wellenformat (wie von der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur dargestellt) bei der Stichprobenentnahme von 11.025, 22.050 und 44.100 Stichproben pro Sekunde, alles bei 8-oder 16-Bit-Mono oder Stereo. In diesem Fall würden Sie zwei Struktur Paare anbieten. Das erste Paar hätte eine **\_ Audiostream \_ config \_ -** Funktionsstruktur, die besagt, dass Sie mindestens 11.025 bis maximal 22.050 Samplings pro Sekunde mit einer Granularität von 11.025 Stichproben pro Sekunde unterstützen (die Granularität ist der Unterschied zwischen unterstützten Werten); ein 8-Bit-minimal-zu-16-Bit-Bit pro Stichprobe mit einer Granularität von 8 Bits pro Stichprobe und einem minimal-und zwei Kanal Maximum. Der Medientyp des ersten Paars wäre das standardmäßige PCM-Format in diesem Bereich, vielleicht 22 Kilohertz (kHz), 16-Bit-Stereo. Ihr zweites Paar wäre eine Funktion, die 44.100 für die Mindest-und höchst Anzahl von Samplings pro Sekunde anzeigt. 8-Bit-(minimal) und 16-Bit-Bits (max) pro Stichprobe mit einer Granularität von 8 Bits pro Beispiel; und das minimal-und zwei-Kanal-Maximum mit einem Kanal. Der Medientyp wäre das standardmäßige 44 kHz-Format, vielleicht 44 kHz 16-Bit-Stereo.

Wenn Sie nicht-PCM-Wellen Formate unterstützen, kann der Medientyp, der von dieser Methode zurückgegeben wird, anzeigen, welche nicht-PCM-Formate unterstützt werden (mit einer standardmäßigen Samplingrate, Bitrate und Kanälen), und die Funktionsstruktur, die den Medientyp begleitet, kann beschreiben, welche anderen Stichproben Raten, Bitraten und Kanäle

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verfügbar machen von Erfassung und Komprimierungs Formaten](exposing-capture-and-compression-formats.md)
</dt> </dl>

 

 
