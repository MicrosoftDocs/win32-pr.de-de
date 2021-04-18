---
description: Dank der Zunahme der Medien Speichergeräte, die komprimierte Audioformate erfordern, müssen Anwendungen eine Vielzahl von neuen codierten Audioinhalten für die Übertragung von Inhalten von PCs an Geräte wie z. b. den Empfänger "HDMI" oder "Display Port" identifizieren, beschreiben und verwenden.
ms.assetid: 86f3396c-b32a-4d70-9f21-e38a745f78bf
title: Darstellen von Formaten für IEC 61937-Übertragungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0700329aafe7e7bc0e09b532c1ac29b9957ca905
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344213"
---
# <a name="representing-formats-for-iec-61937-transmissions"></a>Darstellen von Formaten für IEC 61937-Übertragungen

Dank der Zunahme der Medien Speichergeräte, die komprimierte Audioformate erfordern, müssen Anwendungen eine Vielzahl von neuen codierten Audioinhalten für die Übertragung von Inhalten von PCs an Geräte wie z. b. den Empfänger "HDMI" oder "Display Port" identifizieren, beschreiben und verwenden.

Um einen codierten Audiostream darzustellen, der über eine mit IEC 61937 kompatible Schnittstelle übertragen werden soll, muss eine Anwendung Folgendes bereitstellen:

-   Die Eigenschaften eines codierten Audiostreams, der übertragen werden soll.

-   Die Merkmale eines decodierten Audiostreams auf dem Zielgerät.

In Windows Vista und früheren Windows-Betriebssystemen kann eine Anwendung die Qualitätsstufe eines Audioformats von der Anzahl der Kanäle, der Stichprobengröße und der Datenrate eines Audiostreams, der das Format verwendet, ableiten. Bei einem PCM-Format sind diese Informationen über die **nchannels**-, **nsamplespersec**-und **navgbytespersec** -Member der **WaveFormatEx** -Struktur verfügbar, die das Format angibt. Bei einem nicht-PCM-Format wurden diese drei Member für das Speichern von Informationen über die komprimierten Daten im Audiostream bereitstellt. Folglich fehlen in der **WaveFormatEx** -Strukturinformationen über die effektive Anzahl von Kanälen, die Stichprobengröße und die Datenrate des nicht-PCM-Audiostreams, nachdem der Stream dekomprimiert und wiedergegeben wurde. Basierend auf den Informationen in dieser Struktur hat ein Benutzer oder eine Anwendung möglicherweise Schwierigkeiten beim Ableiten der Qualitätsstufe des nicht-PCM-Streams.

**WaveFormatEx** wurde auf die **WAVEFORMATEXTENSIBLE** -Struktur erweitert, um die zusätzlichen Datenstrom Merkmale bereitzustellen. Diese Struktur ist jedoch auch nicht ausreichend, um den Stream für IEC 61937-Übertragungen zu beschreiben, da Sie einen einzelnen Satz von Merkmalen darstellen und für nicht komprimierte PCM-Daten mit mehreren Kanälen verwendet werden sollte.

In Windows 7 löst das Betriebssystem dieses Problem durch die Unterstützung einer neuen Struktur, **WAVEFORMATEXTENSIBLE \_ IEC61937** , die die **WAVEFORMATEXTENSIBLE** -Struktur erweitert, um zwei Sätze von audiostreammerkmalen zu speichern: das codierte Audioformat vor der Übertragung und die Eigenschaften des Audiostreams, nachdem er decodiert wurde. Die neue Struktur gibt explizit die effektive Anzahl von Kanälen, die Stichprobengröße und die Datenrate eines nicht-PCM-Formats an. Mit diesen Informationen kann eine Anwendung die Qualitätsstufe des nicht-PCM-Streams ableiten, nachdem Sie dekomprimiert und wiedergegeben wurde.

Die **WAVEFORMATEXTENSIBLE \_ IEC61937** -Struktur wird im "ksmedia. h"-Header deklariert, der im Windows 7 SDK enthalten ist. Der **formatext** -Member ist die **WAVEFORMATEXTENSIBLE** -Struktur, die die Merkmale des zu übertragenden Datenstroms speichert. Der **formatmember der** **WAVEFORMATEXTENSIBLE** -Struktur ist die **WaveFormatEx** -Struktur. Der Inhalt dieser **WaveFormatEx** und **WAVEFORMATEXTENSIBLE** gibt einer Anwendung an, ob die Struktur als **WAVEFORMATEXTENSIBLE \_ IEC61937** -Struktur interpretiert werden kann. Für eine **WAVEFORMATEXTENSIBLE \_ IEC61937** -Struktur:

-   Der **wformattag** -Member von **WaveFormatEx** muss das Wave- \_ Format \_ Extensible ( `FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE` ) enthalten.

-   Der **unter Format** -Member der **WAVEFORMATEXTENSIBLE** -Struktur gibt die GUID des codierten Formats an, das übertragen werden soll. Beispielsweise `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` gibt das Dolby Digital Plus-Format an. Informationen zu unterstützten GUIDs finden Sie unter unter Format-GUIDs.

-   Die Größe, die durch das **CBSIZE** -Element von WaveFormatEx angegeben wird, beträgt 34 Bytes. (`FormatExt.Format.cbSize = 34`). Die Gesamtgröße von **WAVEFORMATEXTENSIBLE \_ IEC61937** beträgt 52 bytes.

Die Member **dwencodedsamplespersec**, **dwencodedchannelcount** und **dwaveragebytespersec** von **WAVEFORMATEXTENSIBLE \_ IEC61937** beschreiben die Samplingrate, die Anzahl der Kanäle und die Bitrate in Bytes des Streams des Audiostreams, nachdem er decodiert wurde.

## <a name="subformat-guids"></a>Unter Format-GUIDs

In Windows 7 enthält der Header "ksmedia. h" Definitionen für die unter Format-GUIDs für die von CEA-861-D definierten komprimierten Audioformate. Die GUIDs werden im unter Format-Member von **WAVEFORMATEXTENSIBLE** angegeben, der im **formatext** -Member der **WAVEFORMATEXTENSIBLE \_ IEC61937** -Struktur () angegeben wird `WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat` .

Die GUIDs für die komprimierten Audioformate, die als standardmäßige IEC 61937-codierte Audioformate verfügbar sind, sind in der folgenden Tabelle aufgeführt. Diese Formate ähneln den vorhandenen aktiven Codierungs-3-Formaten (AC-3) und Digital Theater Sound (DTS)-Formaten in Windows.



| CEA 861-Typ | Unter Format-GUID                                                                                                          | BESCHREIBUNG                                  |
|--------------|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| 0x00         |                                                                                                                         | Verweisen Sie auf den Stream.                         |
| 0x01         | 00000000-0000-0010-8000-00aa00389b71<br/> ksdataformat- \_ Untertyp \_ WaveFormatEx<br/>                          | IEC 60958 PCM                                |
| 0x02         | 00000092-0000-0010-8000-00aa00389b71<br/> Ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ Digital<br/>              | AC-3                                         |
| 0x03         | 00000003-0cea-0010-8000-00aa00389b71<br/> Ksdataformat- \_ Untertyp \_ IEC61937 \_ MPEG1<br/>                       | MPEG-1 (Schicht 1 & 2)                         |
| 0x04         | 00000004-0cea-0010-8000-00aa00389b71<br/> Ksdataformat- \_ Untertyp \_ IEC61937 \_ mpeg3<br/>                       | MPEG-3 (Schicht 3)                             |
| 0x05         | 00000005-0cea-0010-8000-00aa00389b71<br/> Ksdataformat- \_ Untertyp \_ IEC61937 \_ MPEG2 <br/>                      | MPEG-2 (Multichannel)                         |
| 0x06         | 00000006-0cea-0010-8000-00aa00389b71<br/> Ksdataformat- \_ Untertyp \_ IEC61937 \_ AAC<br/>                         | Erweiterte Audiocodierung (MPEG-2/4 AAC in ADTs) |
| 0x07         | 00000008-0000-0010-8000-00aa00389b71<br/> Ksdataformat- \_ Untertyp \_ IEC61937 \_ DTS<br/>                         | DTS                                          |
| 0x0A         | 0000000A-0cea-0010-8000-00aa00389b71<br/> Ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ Digital \_ Plus<br/>        | Dolby Digital Plus                           |
| 0x0A         | 0000010a-0cea-0010-8000-00aa00389b71<br/> Ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ Digital \_ Plus \_ Atmos<br/> | Dolby Atmos, codiert mit Dolby Digital Plus  |
| 0x0f         |                                                                                                                         | Nicht verwendet reserviert                              |



 

In der folgenden Tabelle sind die GUIDs für die komprimierten Audioformate aufgeführt, die in den audiobeispielpaketen mit hoher Bitrate übertragen werden.



| CEA 861-Typ | Unter Format-GUID                                                                                           | BESCHREIBUNG                                                                                                                     |
|--------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 0x0B         | 0000000b-0cea-0010-8000-00aa00389b71<br/> Ksdataformat- \_ Untertyp \_ IEC61937 \_ DTS \_ HD<br/>      | DTS-HD (24-Bit, 96kHz)                                                                                                          |
| 0x0c         | 0000000c-0cea-0010-8000-00aa00389b71<br/> Ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ MLP<br/>   | Dolby Mat 1,0:<br/> Dolby TrueHD (MLP – Verlust lose Verpackung) – 24-Bit-192 kHz/bis zu 18 Mbit/s, 8 Kanäle) <br/> |
| 0x0c         | 0000010c-0cea-0010-8000-00aa00389b71<br/> Ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ MAT20<br/> | Dolby Mat 2,0: <br/> Dolby TrueHD – 24-Bit-192 kHz/bis zu 18 Mbit/s, 8 Kanäle oder LPCM bis zu 24 Mbit/s. <br/>           |
| 0x0c         | 0000030c-0cea-0010-8000-00aa00389b71<br/> Ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ MAT21<br/> | Dolby Mat 2,1: <br/> Dolby TrueHD – 24-Bit-192 kHz/bis zu 18 Mbit/s, 8 Kanäle oder LPCM bis zu 24 Mbit/s. <br/>           |
| 0x0E         | 00000164-0000-0010-8000-00aa00389b71<br/> Ksdataformat- \_ Untertyp \_ IEC61937 \_ WMA \_ pro<br/>     | Windows Media Audio (WMA) pro                                                                                                   |



 

Der von Microsoft bereitgestellte HD-audioklassen-Treiber unterstützt PCM, AC3, DTS, AAC, Dolby Digital Plus, WMA Pro, Matt Die GUIDs für die komprimierten Audioformate, die nicht vom Treiber der HD-audioklasse unterstützt werden und von Drittanbieter Lösungen implementiert werden können, sind in der folgenden Tabelle aufgeführt.



| CEA 861-Typ | Unter Format-GUID                                                                                              | BESCHREIBUNG                                                                    |
|--------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| 0x08         | 00000008-0cea-0010-8000-00aa00389b71<br/> Ksdataformat- \_ Untertyp \_ IEC61937 \_ ATRAC<br/>           | Adaptive Transform-akustische Codierung (ATRAC)                                     |
| 0x09         | 00000009-0cea-0010-8000-00aa00389b71<br/> Ksdataformat \_ \_ -Untertyp \_ IEC61937 \_ One \_ -Bit-Audiodatei<br/> | One-Bit Audiodaten                                                                  |
| 0x0D         | 0000000D-0cea-0010-8000-00aa00389b71<br/> Ksdataformat- \_ Untertyp \_ IEC61937 \_ DST<br/>             | Direct Stream Transport (DST) – Verlust lose komprimierte DSD (Direct Stream Digital). |



 

## <a name="dolby-digital-plus-format"></a>Dolby Digital Plus-Format

Wenn Dolby Digital Plus-Inhalt über IEC 60958 übertragen wird, muss die linksamplingrate viermal so oft wie die Samplingrate des Inhalts sein. Dolby Digital Plus unterstützt die Inhalts Stichproben Raten 32 kHz, 44,1 kHz und 48 kHz. Schnittstellen wie z. b. "HDMI" unterstützen 128 kHz (32 kHz x 4) nicht. Daher können nur die Samplingrate für 44,1 und 48 kHz unterstützt werden.

Die Werte, die von einer Anwendung in der WAVEFORMATEXTENSIBLE IEC61937-Struktur festgelegt \_ werden, um Dolby Digital Plus-Format mit einer Inhalts Stichproben Rate von 48 kHz darzustellen, werden im folgenden Beispiel gezeigt.


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;              // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 192000;    // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 768000;   // 192 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;            // 16 bits * 2 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;        // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                // Indicates that Format is part of a 
                                                   // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // Dolby 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL_PLUS;
wfext.dwEncodedSamplesPerSec = 48000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="dolby-truehd-mat"></a>Dolby TrueHD (Matt)

Der Dolby TrueHD-Inhalt wird über IEC 60958 auf 176,4 kHz/8-Kanälen übertragen (die IEC 60958-Frame Rate von 705,6 kHz erfordert), um die Inhalts Stichproben Raten von 44,1, 88,2 und 176,4 kHz und 192 kHz/8-Kanälen (die eine IEC 60958-Frame Rate von 768 kHz erfordert) für die Inhalts Stichprobenrate von 48, 96 und 192.

Die Werte, die von einer Anwendung in der WAVEFORMATEXTENSIBLE IEC61937-Struktur festgelegt \_ werden, um Dolby TrueHD mit einer Inhalts Stichproben Rate von 96 kHz darzustellen, werden in den folgenden Beispielen gezeigt.

Dolby Mat 1,0


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MLP; // This structure indicates MLP (MAT 1.0) support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



Dolby Mat 2,0


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT20; // This structure indicates MAT 2.0 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



Dolby Mat 2,1


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT21; // This structure indicates MAT 2.1 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



> [!Note]  
> Die Unterstützung für eine Version von Dolby Mat impliziert keine Unterstützung für Dolby Mat mit einer niedrigeren Versionsnummer. Da Dolby Mat 2,1 abwärts kompatibel mit früheren Versionen von Dolby Mat ist, gibt ein Klassen Treiber, der Unterstützung für Dolby Mat 2,1 angibt, in der Regel auch die Unterstützung für Dolby Matt 2,0 und Dolby Matt 1,0 an, wobei für jede Version eine separate WAVEFORMATEXTENSIBLE IEC61937-Struktur verwendet wird \_ .

 

## <a name="wma-pro"></a>WMA Pro

Der WMA pro-Audioinhalt kann in einem der vier profile codiert werden, die in der folgenden Tabelle aufgeführt sind.



| Profil | Eigenschafts Wert                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                         |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| M0      | Maximale Bitrate – 192000 Bit/s <br/> Maximale Samplingrate – 48 kHz <br/> Maximale Anzahl von Kanälen – 2 <br/> Maximale Puffergröße – 600 \* 1024 Bits <br/> Maximale Anzahl von Samplings pro Frame – 2048 <br/> Maximale Anzahl von Bits pro Frame-655536<br/>   | Empfohlen für die Musik und das Streaming per Funk.<br/> Die maximale Bitrate in einem audioframe beträgt 1536000 Bit/s.<br/>          |
| M1      | Maximale Bitrate – 385000 Bit/s <br/> Maximale Samplingrate – 48 kHz <br/> Maximale Anzahl von Kanälen – 6 <br/> Maximale Puffergröße – 600 \* 1024 Bits <br/> Maximale Anzahl von Samplings pro Frame – 4096 <br/> Maximale Anzahl von Bits pro Frame-131072<br/>   | Empfohlen für Filme mit Standarddefinitionen für umschließende Sounds.<br/> Die maximale Bitrate in einem audioframe beträgt 1536000 Bit/s.<br/> |
| M2      | Maximale Bitrate – 769000 Bit/s <br/> Maximale Samplingrate – 96 kHz <br/> Maximale Anzahl von Kanälen – 6 <br/> Maximale Puffergröße – 1200 \* 1024 Bits <br/> Maximale Anzahl von Samplings pro Frame – 4096 <br/> Maximale Anzahl von Bits pro Frame-131072<br/>  | Empfohlen für umschließende High Definition-Filme.<br/> Die maximale Rate in einem audioframe beträgt 3072000 Bit/s.<br/>         |
| M3      | Maximale Bitrate – 3 Millionen Bit/s <br/> Maximale Samplingrate – 96 kHz <br/> Maximale Anzahl von Kanälen – 8 <br/> Maximale Puffergröße – 2400 \* 1024 Bits <br/> Maximale Anzahl von Samplings pro Frame – 4096 <br/> Maximale Anzahl von Bits pro Frame-131072<br/> | Empfohlen für digitales Theater.<br/> Die maximale Rate in einem audioframe beträgt 3072000 Bit/s.<br/>                               |



 

Die M0-und M1-profile passen in einen 48 kHz/16 Bit/Stereo (1536000 Bit/s) IEC 60958-Datenstrom. Die Profile m2 und M3 passen in einen IEC 60958-Stream mit 96 kHz/16 Bit/Stereo (3072000 Bit/s) an.

Die Werte, die von einer Anwendung in der WAVEFORMATEXTENSIBLE IEC61937-Struktur festgelegt \_ werden, um WMA Pro als ein m2-Profil darzustellen, werden im folgenden Beispiel gezeigt.


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;             // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 96000;    // Link runs at 96 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 384000;  // 96 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;           // 16 bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;       // Always at 16 bits over link.
wfext.FormatExt.Format.cbSize = 34;               // Indicates that Format is part of a 
                                                  // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_WMA_PRO;
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte Formate](device-formats.md)
</dt> </dl>

 

 




