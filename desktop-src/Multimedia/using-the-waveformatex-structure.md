---
title: Verwenden der WaveFormatEx-Struktur
description: Verwenden der WaveFormatEx-Struktur
ms.assetid: 9b668e1e-cb5f-4065-802b-23974925eacf
keywords:
- Wellenform-Audiostruktur, WaveFormatEx-Struktur
- hilfsaudiostruktur, WaveFormatEx-Struktur
- WaveFormatEx-Struktur
- PCM-Audiodaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1534cf660c2f2423dc526c3d29f8eca06878fc0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472885"
---
# <a name="using-the-waveformatex-structure"></a>Verwenden der WaveFormatEx-Struktur

Verwenden Sie für PCM-Audiodaten, die nicht mehr als zwei Kanäle und 8-Bit-oder 16-Bit-Beispiele aufweisen, die [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -Struktur, um das Datenformat anzugeben.

Im folgenden Beispiel wird gezeigt, wie Sie eine **WaveFormatEx** -Struktur für 11,025 Kilohertz (kHz) 8-Bit Mono und für 44,1 kHz 16-Bit-Stereo einrichten. Nach dem Einrichten von **WaveFormatEx** Ruft das Beispiel die isformatsupported-Funktion auf, um zu überprüfen, ob das PCM Wellenform-Ausgabegerät das-Format unterstützt. Der Quellcode für isformatsupported wird in einem Beispiel unter Bestimmen der [nicht standardmäßigen Format Unterstützung](determining-nonstandard-format-support.md)gezeigt.


```C++
UINT wReturn; 
WAVEFORMATEX pcmWaveFormat; 
 
// Set up WAVEFORMATEX for 11 kHz 8-bit mono. 
 
pcmWaveFormat.wFormatTag = WAVE_FORMAT_PCM; 
pcmWaveFormat.nChannels = 1; 
pcmWaveFormat.nSamplesPerSec = 11025L; 
pcmWaveFormat.nAvgBytesPerSec = 11025L; 
pcmWaveFormat.nBlockAlign = 1; 
pcmWaveFormat.wBitsPerSample = 8; 
pcmWaveFormat.cbSize = 0;
 
// See if format is supported by any device in system. 
 
wReturn = IsFormatSupported(&pcmWaveFormat, WAVE_MAPPER); 
 
// Report results. 
 
if (wReturn == 0) 
     MessageBox(hMainWnd, "11 kHz 8-bit mono is supported.", 
       "", MB_ICONINFORMATION); 
else if (wReturn == WAVERR_BADFORMAT) 
     MessageBox(hMainWnd, "11 kHz 8-bit mono NOT supported.", 
       "", MB_ICONINFORMATION); 
else 
     MessageBox(hMainWnd, "Error opening waveform device.", 
       "Error", MB_ICONEXCLAMATION); 
 
// Set up WAVEFORMATEX for 44.1 kHz 16-bit stereo. 
 
pcmWaveFormat.wFormatTag = WAVE_FORMAT_PCM; 
pcmWaveFormat.nChannels = 2; 
pcmWaveFormat.nSamplesPerSec = 44100L; 
pcmWaveFormat.nAvgBytesPerSec = 176400L; 
pcmWaveFormat.nBlockAlign = 4; 
pcmWaveFormat.wBitsPerSample = 16; 
pcmWaveFormat.cbSize = 0;
 
// See if format is supported by any device in the system. 
 
wReturn = IsFormatSupported(&pcmWaveFormat, WAVE_MAPPER); 
 
// Report results. 
 
if (wReturn == 0) 
    MessageBox(hMainWnd, "44.1 kHz 16-bit stereo is supported.", 
      "", MB_ICONINFORMATION); 
else if (wReturn == WAVERR_BADFORMAT) 
    MessageBox(hMainWnd, "44.1 kHz 16-bit stereo NOT supported.", 
      "", MB_ICONINFORMATION); 
else 
    MessageBox(hMainWnd, "Error opening waveform device.", 
      "Error", MB_ICONEXCLAMATION); 

```



 

 