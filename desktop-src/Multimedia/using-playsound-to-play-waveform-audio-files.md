---
title: Verwenden von PlaySound zum Wiedergeben Waveform-Audio Dateien
description: Verwenden von PlaySound zum Wiedergeben Waveform-Audio Dateien
ms.assetid: 8b7d191b-6b0c-4dff-84de-cb3a5c314b80
keywords:
- Waveform-Audio, PlaySound-Funktion
- Waveformaudio, Wiedergeben von Dateien
- Waveform-Audio, WAV-Dateinamenerweiterung
- PlaySound-Funktion, Wiedergeben von Waveform-Audiodateien
- Wiedergeben von Waveform-Audiodateien, PlaySound-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa83125665e2a99cc0f47da0893cbc113c0be7a251d62eb66a91e7a1218dac5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687850"
---
# <a name="using-playsound-to-play-waveform-audio-files"></a>Verwenden von PlaySound zum Wiedergeben Waveform-Audio Dateien

Die meisten Waveform-Audiodateien verwenden . WAV-Dateinamenerweiterung.

Die folgende Anweisung gibt C: \\ SOUNDS \\ BELLS wieder. WAV-Datei:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC); 
```



Wenn die angegebene Datei nicht vorhanden ist oder die Datei nicht in den verfügbaren Arbeitsspeicher passt, gibt [**PlaySound**](/previous-versions//dd743680(v=vs.85)) den Standardsystemsound wieder. Wenn kein Standardsystemsound definiert wurde, erzeugt **PlaySound** keinen Sound. Wenn der Standardsystemsound nicht wiedergegeben werden soll, geben Sie das \_ SND-NODEFAULT-Flag an, wie im folgenden Beispiel gezeigt:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC | SND_NODEFAULT); 
```



 

 