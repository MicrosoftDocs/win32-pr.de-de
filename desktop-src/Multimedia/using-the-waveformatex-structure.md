---
title: Verwenden der WAVEFORMATEX-Struktur
description: Verwenden der WAVEFORMATEX-Struktur
ms.assetid: 9b668e1e-cb5f-4065-802b-23974925eacf
keywords:
- Waveform-Audio, WAVEFORMATEX-Struktur
- Hilfsaudio, WAVEFORMATEX-Struktur
- WAVEFORMATEX-Struktur
- PCM-Audiodaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3831d9760580f294573a4bc1bec3aef1d42cf345b2d714a897b22940a89a0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136054"
---
# <a name="using-the-waveformatex-structure"></a>Verwenden der WAVEFORMATEX-Struktur

Verwenden Sie für PCM-Audiodaten auf nicht mehr als zwei Kanälen und mit 8-Bit- oder 16-Bit-Stichproben die [**WAVEFORMATEX-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) um das Datenformat anzugeben.

Das folgende Beispiel zeigt, wie Sie eine **WAVEFORMATEX-Struktur** für 8-Bit-Mono mit 11,025 Kilohertz (kHz) und für 16-Bit-Stereo mit 44,1 kHz einrichten. Nach dem Einrichten **von WAVEFORMATEX** ruft das Beispiel die IsFormatSupported-Funktion auf, um zu überprüfen, ob das PCM Waveform-Ausgabegerät das Format unterstützt. Der Quellcode für IsFormatSupported wird in einem Beispiel unter [Determining Nonstandard Format Support (Bestimmen der Nichtstandardformatunterstützung) gezeigt.](determining-nonstandard-format-support.md)


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



 

 