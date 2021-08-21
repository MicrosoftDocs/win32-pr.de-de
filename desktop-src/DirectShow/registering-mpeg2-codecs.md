---
description: Registrieren von MPEG2-Codecs
ms.assetid: f730a7df-af8f-4dce-9bfe-6ee1eca8fd90
title: Registrieren von MPEG2-Codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7aaf683d03f529e394fe7e01af8ccae0e0fd009ad7a90b608c8bbebf834c5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952139"
---
# <a name="registering-mpeg2-codecs"></a>Registrieren von MPEG2-Codecs

Dieses Thema gilt nur für Windows XP Media Center Edition.

Windows Xp Media Center Edition verwaltet zwei Registrierungsschlüssel, mit denen bestimmt wird, welcher Codec zum Wiedergeben von MPEG2-Video- und Audiodateien verwendet werden soll. Der erste Registrierungsschlüssel gibt den bevorzugten MPEG2-Codec des Computerherstellers an, und der zweite listet alle Media Center-kompatiblen Codecs auf, die derzeit auf dem Computer installiert sind. Wenn Media Center eine MPEG2-Datei wiedergeben muss, verwendet es den bevorzugten Codec des Herstellers, sofern angegeben. Falls nicht, wird der erste Media Center-kompatible Codec verwendet, der in der Registrierung aufgeführt ist. Wenn die Registrierung keine bevorzugten oder kompatiblen Codecs angibt, verwendet Media Center den DirectShow-Standardfilter, um einen Codec auszuwählen.

Um sicherzustellen, dass Media Center immer einen kompatiblen MPEG2-Codec verwendet, sollten Hersteller von Media Center-Computern den bevorzugten MPEG2-Codec am folgenden Registrierungsspeicherort angeben:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Media Center\Service\Video
```



Die Schlüsseldaten sollten wie folgt aussehen:


```C++
PreferredMPEG2VideoDecoder=REG_SZ "{MPEG2 Video CLSID GUID}"
PreferredMPEG2AudioDecoder=REG_SZ "{MPEG2 Audio CLSID GUID}"
```



Das Setupprogramm für einen Mit Media Center kompatiblen MPEG2-Codec sollte den Codec registrieren, indem zwei Instanzen des folgenden Registrierungsschlüssels erstellt werden: eine für den Videocodec und eine für den Audiocodec:


```C++
[HKEY_CLASSES_ROOT\CLSID\{083863F1-70DE-11d0-BD40-00A0C911CE86}\Instance\<Your Codec CLSID here>\Capabilities]
```



Die Schlüsseldaten sollten wie folgt aussehen:


```C++
"{374ac4df-7c98-4257-b13d-36087dbee458}"=dword:00000001
```



 

 



