---
description: Mit dem Anstieg der Medienspeichergeräte, die komprimierte Audioformate erfordern, müssen Anwendungen eine Vielzahl von neuen codierten Audioinhalten identifizieren, beschreiben und verwenden, um Inhalte von PCs an Geräte wie DENCS- oder DisplayPort-Empfänger zu übertragen.
ms.assetid: 86f3396c-b32a-4d70-9f21-e38a745f78bf
title: Darstellen von Formaten für IEC 61937-Übertragungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0a607770a388a11978d0e4666b5046506b6698c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549295"
---
# <a name="representing-formats-for-iec-61937-transmissions"></a>Darstellen von Formaten für IEC 61937-Übertragungen

Mit dem Anstieg der Medienspeichergeräte, die komprimierte Audioformate erfordern, müssen Anwendungen eine Vielzahl von neuen codierten Audioinhalten identifizieren, beschreiben und verwenden, um Inhalte von PCs an Geräte wie DENCS- oder DisplayPort-Empfänger zu übertragen.

Um einen codierten Audiostream darzustellen, der über eine IEC 61937-kompatible Schnittstelle übertragen werden soll, muss eine Anwendung:

-   Die Merkmale eines codierten Audiodatenstroms, der übertragen werden soll.

-   Die Merkmale eines decodierten Audiodatenstroms auf dem Zielgerät.

Unter Windows Vista und früheren Windows-Betriebssystemen kann eine Anwendung die Qualitätsstufe eines Audioformats aus der Anzahl der Kanäle, der Stichprobengröße und der Datenrate eines Audiodatenstroms ableiten, der das Format verwendet. Für ein PCM-Format sind diese Informationen über die **Member nChannels**, **nSamplesPerSec** und **nAvgBytesPerSec** der **WAVEFORMATEX-Struktur** verfügbar, die das Format angibt. Für ein Nicht-PCM-Format wurden diese drei Member dazu aufgefordert, Informationen zu den komprimierten Daten im Audiostream zu speichern. Daher fehlen in der **WAVEFORMATEX-Struktur** Informationen über die effektive Anzahl von Kanälen, die Stichprobengröße und die Datenrate des Nicht-PCM-Audiodatenstroms, nachdem der Stream dekomprimiert und wiedergegeben wurde. Basierend auf den Informationen in dieser Struktur kann es für einen Benutzer oder eine Anwendung schwierig sein, den Qualitätsgrad des Nicht-PCM-Streams hergeleitet zu werden.

**WAVEFORMATEX** wurde auf die **WAVEFORMATEXTENSIBLE-Struktur** erweitert, um die zusätzlichen Streameigenschaften bereitzustellen. Diese Struktur ist jedoch auch nicht geeignet, um den Stream für IEC 61937-Übertragungen zu beschreiben, da sie einen einzelnen Satz von Merkmalen darstellen und für unkomprimierte MULTI-Channel-PCM-Daten verwendet werden sollte.

Unter Windows 7 löst das Betriebssystem dieses Problem, indem es unterstützung für eine neue Struktur bietet: **WAVEFORMATEXTENSIBLE \_ IEC61937,** die **die WAVEFORMATEXTENSIBLE-Struktur** erweitert, um zwei Sätze von Audiostreammerkmalen zu speichern: das codierte Audioformat vor der Übertragung und die Merkmale des Audiostreams nach der Decodierung. Die neue -Struktur gibt explizit die effektive Anzahl von Kanälen, die Stichprobengröße und die Datenrate eines Nicht-PCM-Formats an. Mit diesen Informationen kann eine Anwendung die Qualitätsstufe des Nicht-PCM-Streams nach dem Dekomprimieren und Abspielen abgeleitet.

Die **WAVEFORMATEXTENSIBLE \_ IEC61937-Struktur** wird im KsMedia.h-Header deklariert, der im Windows 7 SDK enthalten ist. Der **FormatExt-Member** ist die **WAVEFORMATEXTENSIBLE-Struktur,** die die Merkmale des zu übertragenden Streams speichert. Der **Format-Member** der **WAVEFORMATEXTENSIBLE-Struktur** ist die **WAVEFORMATEX-Struktur.** Der Inhalt dieses **WAVEFORMATEX-** und **WAVEFORMATEXTENSIBLE-Steuerelements** gibt für eine Anwendung an, ob die Struktur als **WAVEFORMATEXTENSIBLE \_ IEC61937-Struktur interpretiert werden** kann. Für eine **WAVEFORMATEXTENSIBLE \_ IEC61937-Struktur:**

-   Das **wFormatTag-Member** von **WAVEFORMATEX** muss WAVE \_ FORMAT \_ EXTENSIBLE ( ) `FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE` enthalten.

-   Der **SubFormat-Member** der **WAVEFORMATEXTENSIBLE-Struktur** gibt die GUID des zu übertragenden codierten Formats an. Beispielsweise gibt das `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` Dolby Digital Plus-Format an. Informationen zu den unterstützten GUIDs finden Sie unter SubFormat-GUIDs.

-   Die vom **cbSize-Member** des WAVEFORMATEX-Steuerelements angegebene Größe beträgt 34 Bytes. (`FormatExt.Format.cbSize = 34`). Die Gesamtgröße von **WAVEFORMATEXTENSIBLE \_ IEC61937** beträgt 52 Bytes.

Die Member **dwEncodedSamplesPerSec,** **dwEncodedChannelCount** und **dwAverageBytesPerSec** von **WAVEFORMATEXTENSIBLE \_ IEC61937** beschreiben die Samplingrate, die Anzahl der Kanäle und die Bitrate in Bytes des Streams des Audiostreams, nachdem er decodiert wurde.

## <a name="subformat-guids"></a>SubFormat-GUIDs

In Windows 7 enthält der KsMedia.h-Header Definitionen für die SubFormat-GUIDs für die komprimierten Audioformate, die von CEA-861-D definiert werden. Die GUIDs werden im SubFormat-Element von **WAVEFORMATEXTENSIBLE** angegeben, angegeben im **FormatExt-Member** der **WAVEFORMATEXTENSIBLE \_ IEC61937-Struktur** ( `WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat` ).

Die GUIDs für die komprimierten Audioformate, die als IEC 61937-codierte Standardaudioformate verfügbar sind, sind in der folgenden Tabelle aufgeführt. Diese Formate ähneln den vorhandenen Darstellungen von Active Coding 3 (AC-3) und DtS -Formaten in Windows.



| CEA 861-Typ | SubFormat-GUID                                                                                                          | Beschreibung                                  |
|--------------|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| 0x00         |                                                                                                                         | Weitere Informationen finden Sie im Stream.                         |
| 0x01         | 00000000-0000-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ WAVEFORMATEX<br/>                          | IEC 60958 PCM                                |
| 0x02         | 00000092-0000-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ DOLBY \_ DIGITAL<br/>              | AC-3                                         |
| 0x03         | 00000003-0cea-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ MPEG1<br/>                       | MPEG-1 (Layer 1 & 2)                         |
| 0x04         | 00000004-0cea-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ MPEG3<br/>                       | MPEG-3 (Ebene 3)                             |
| 0x05         | 00000005-0cea-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ MPEG2 <br/>                      | MPEG-2(multichannel)                         |
| 0x06         | 00000006-0cea-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ AAC<br/>                         | Erweiterte Audiocodierung (MPEG-2/4 AAC in ADTS) |
| 0x07         | 00000008-0000-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ DTS<br/>                         | DTS                                          |
| 0x0a         | 0000000a-0cea-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ DOLBY DIGITAL \_ \_ PLUS<br/>        | Dolby Digital Plus                           |
| 0x0a         | 0000010a-0cea-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ DOLBY DIGITAL PLUS \_ \_ \_ ATMOS<br/> | Dolby Atmos-codiert mit Dolby Digital Plus  |
| 0x0b         | 0000000b-0cea-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ DTS \_ HD<br/> | DTS HD  |
| 0x0b         | 0000010b-0cea-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ DTSX \_ E1<br/> | DTS:X E1  |
| 0x0b         | 0000030b-0cea-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ DTSX \_ E2<br/> | DTS:X E2  |
| 0x0f         |                                                                                                                         | Nicht verwendet reserviert                              |



 

Die GUIDs für die komprimierten Audioformate, die in Audiobeispielpaketen mit hoher Bitrate übertragen werden, sind in der folgenden Tabelle aufgeführt.



| CEA 861-Typ | SubFormat-GUID                                                                                           | Beschreibung                                                                                                                     |
|--------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 0x0b         | 0000000b-0cea-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ DTS \_ HD<br/>      | DTS-HD (24-Bit, 96Khz)                                                                                                          |
| 0x0c         | 0000000c-0cea-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ DOLBY \_ MLP<br/>   | Dolby MAT 1.0:<br/> Dolby TrueHD (MLP – Verlustloses Packen von Meridianen) – 24-Bit-192KHz/bis zu 18 MBit/s, 8 Kanäle) <br/> |
| 0x0c         | 0000010c-0cea-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ DOLBY \_ MAT20<br/> | Dolby MAT 2.0: <br/> Dolby TrueHD – 24-Bit-192KHz/bis zu 18 MBit/s, 8 Kanäle oder LPCM bis zu 24 MBit/s. <br/>           |
| 0x0c         | 0000030c-0cea-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ DOLBY \_ MAT21<br/> | Dolby MAT 2.1: <br/> Dolby TrueHD – 24-Bit-192KHz/bis zu 18 MBit/s, 8 Kanäle oder LPCM bis zu 24 MBit/s. <br/>           |
| 0x0e         | 00000164-0000-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ WMA \_ PRO<br/>     | Windows Media Audio (WMA) Pro                                                                                                   |



 

Der von Microsoft bereitgestellte HD Audio-Klassentreiber unterstützt die Formate PCM, AC3, DTS, AAC, Dolby Digital Plus, WMA Pro und MAT (MLP). Die GUIDs für die komprimierten Audioformate, die vom HD-Audioklassentreiber nicht unterstützt werden und von Drittanbieterlösungen implementiert werden können, sind in der folgenden Tabelle aufgeführt.



| CEA 861-Typ | SubFormat-GUID                                                                                              | Beschreibung                                                                    |
|--------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| 0x08         | 00000008-0cea-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ ATRAC<br/>           | Adaptive Transformation Acoustic Coding (ATRAC)                                     |
| 0x09         | 00000009-0cea-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ \_ ONE-BIT-AUDIO \_<br/> | One-Bit Audio                                                                  |
| 0x0d         | 0000000d-0cea-0010-8000-00aa00389b71<br/> \_KSDATAFORMAT-UNTERTYP \_ IEC61937 \_ DST<br/>             | Direct Stream Transport (DST) – verlustfreie komprimierte DSD (Direct Stream Digital). |



 

## <a name="dolby-digital-plus-format"></a>Dolby Digital Plus-Format

Wenn Dolby Digital Plus-Inhalte über IEC 60958 übertragen werden, muss die Link-Samplingrate das Vierfache der Samplingrate des Inhalts sein. Dolby Digital Plus unterstützt Inhaltsbeispielraten von 32 KHz, 44,1 KHz und 48 KHz. Schnittstellen wie DIE -Schnittstelle unterstützen nicht 128 KHz (32 KHz x 4), sodass nur 44,1- und 48-KHz-Inhaltsstichprobenraten unterstützt werden können.

Die Werte, die von einer Anwendung in der WAVEFORMATEXTENSIBLE IEC61937-Struktur festgelegt wurden, um das Dolby Digital Plus-Format mit einer Inhaltsabtastrate von 48 KHz darstellen, werden im folgenden Beispiel \_ gezeigt.


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



## <a name="dolby-truehd-mat"></a>Dolby TrueHD (MAT)

Dolby TrueHD-Inhalt wird über IEC 60958 mit 176,4 kHz/8 Kanälen übertragen (erfordert eine IEC 60958 Framerate von 705,6 kHz) für Inhaltsstichprobenraten von 44,1, 88,2 und 176,4 kHz und 192 kHz/8 Kanäle (erfordert eine IEC 60958 Framerate von 768 kHz) für Inhaltsstichprobenraten von 48, 96 und 192 kHz.

Die Werte, die von einer Anwendung in der WAVEFORMATEXTENSIBLE IEC61937-Struktur festgelegt wurden, um Dolby TrueHD mit einer Inhaltsabtastrate von 96 KHz darstellen, werden in den folgenden Beispielen \_ gezeigt.

Dolby MAT 1.0


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



Dolby MAT 2.0


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



Dolby MAT 2.1


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
> Die Unterstützung für eine Version von Dolby MAT bedeutet nicht, dass Dolby MAT mit einer niedrigeren Versionsnummer unterstützt wird. Da Dolby MAT 2.1 abwärtskompatibel mit früheren Versionen von Dolby MAT ist, weist ein Klassentreiber, der die Unterstützung für Dolby MAT 2.1 angibt, in der Regel auch auf Unterstützung für Dolby MAT 2.0 und Dolby MAT 1.0 hin, indem für jede Version eine separate WAVEFORMATEXTENSIBLE \_ IEC61937-Struktur verwendet wird.

 

## <a name="wma-pro"></a>WMA Pro

WMA Pro-Audioinhalte können in einem der vier in der folgenden Tabelle aufgeführten Profile codiert werden.



| Profil | Eigenschaft – Wert                                                                                                                                                                                                                                                      | Beschreibung                                                                                                                         |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| M0      | Maximale Bitrate – 192.000 Bit/s <br/> Maximale Samplingrate – 48 KHz <br/> Maximale Kanalanzahl – 2 <br/> Maximale Puffergröße – 600 \* 1024 Bits <br/> Maximale Anzahl von Stichproben pro Frame – 2048 <br/> Maximale Bits pro Frame – 655536<br/>   | Empfohlen für Over-the-Air-Musik und Streaming.<br/> Die maximale Bitrate in einem Audioframe beträgt 1536.000 Bit/s.<br/>          |
| M1      | Maximale Bitrate – 385.000 Bps <br/> Maximale Samplingrate – 48 KHz <br/> Maximale Kanalanzahl – 6 <br/> Maximale Puffergröße – 600 \* 1024 Bits <br/> Maximale Anzahl von Stichproben pro Frame – 4096 <br/> Maximale Bits pro Frame – 131072<br/>   | Empfohlen für Surround-Sound-Standarddefinitionsvideos.<br/> Die maximale Bitrate in einem Audioframe beträgt 1536.000 Bit/s.<br/> |
| M2      | Maximale Bitrate – 769.000 Bps <br/> Maximale Samplingrate – 96 KHz <br/> Maximale Kanalanzahl – 6 <br/> Maximale Puffergröße – 1200 \* 1024 Bits <br/> Maximale Anzahl von Stichproben pro Frame – 4096 <br/> Maximale Bits pro Frame – 131072<br/>  | Empfohlen für High Definition-Filme mit Umschließen.<br/> Die maximale Rate in einem Audioframe beträgt 3072.000 Bit/s.<br/>         |
| M3      | Maximale Bitrate – 3000.000 Bit/s <br/> Maximale Samplingrate – 96 KHz <br/> Maximale Kanalanzahl – 8 <br/> Maximale Puffergröße – 2.400 \* 1.024 Bit <br/> Maximale Stichproben pro Frame – 4096 <br/> Maximale Bits pro Frame : 131072<br/> | Empfohlen für digitales Kinderspiel.<br/> Die maximale Rate in einem Audioframe beträgt 3072.000 Bit/s.<br/>                               |



 

Die Profile M0 und M1 passen in einen IEC 60958-Stream mit 48 KHz/16 Bit/Stereo (1536000 Bps). Die Profile M2 und M3 passen in einen IEC 60958-Stream mit 96 KHz/16 Bit/Stereo (3072000 Bps).

Die Werte, die von einer Anwendung in der WAVEFORMATEXTENSIBLE IEC61937-Struktur festgelegt werden, um \_ WMA Pro als M2-Profil zu darstellen, werden im folgenden Beispiel gezeigt.


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

[Geräteformate](device-formats.md)
</dt> </dl>

 

 




