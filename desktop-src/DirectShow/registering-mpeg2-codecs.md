---
description: Registrieren von MPEG2-Codecs
ms.assetid: f730a7df-af8f-4dce-9bfe-6ee1eca8fd90
title: Registrieren von MPEG2-Codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de007cebdd0a911f6b43f21003ed3ede0bc1723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124135"
---
# <a name="registering-mpeg2-codecs"></a>Registrieren von MPEG2-Codecs

Dieses Thema gilt nur für Windows XP Media Center Edition.

Windows XP Media Center Edition verwaltet zwei Registrierungsschlüssel, die verwendet werden, um zu bestimmen, welcher Codec zum Wiedergeben von Video-und Audiodateien für das Video verwendet werden soll. Der erste Registrierungsschlüssel gibt den bevorzugten MPEG2-Codec des Computerherstellers an, der zweite listet alle mit Media Center kompatiblen Codecs auf, die derzeit auf dem Computer installiert sind. Wenn Media Center eine MPEG2-Datei wiedergeben muss, wird der bevorzugte Codec des Herstellers verwendet, sofern ein solcher angegeben ist. Wenn dies nicht der Fall ist, wird der erste in der Registrierung aufgeführte Media Center-kompatible Codec verwendet. Wenn in der Registrierung keine bevorzugten oder kompatiblen Codecs angegeben sind, verwendet Media Center das standardmäßige DirectShow-Filter Verdienst, um einen Codec auszuwählen.

Um sicherzustellen, dass Media Center immer einen kompatiblen MPEG2-Codec verwendet, sollten Hersteller von Media Center-Computern den bevorzugten MPEG2-Codec am folgenden Registrierungs Speicherort angeben:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Media Center\Service\Video
```



Die Schlüsseldaten sollten wie folgt lauten:


```C++
PreferredMPEG2VideoDecoder=REG_SZ "{MPEG2 Video CLSID GUID}"
PreferredMPEG2AudioDecoder=REG_SZ "{MPEG2 Audio CLSID GUID}"
```



Das Setup Programm für einen mit Media Center kompatiblen MPEG2-Codec sollte den Codec registrieren, indem zwei Instanzen des folgenden Registrierungsschlüssels erstellt werden – eine für den Videocodec und eine für den Audiocodec:


```C++
[HKEY_CLASSES_ROOT\CLSID\{083863F1-70DE-11d0-BD40-00A0C911CE86}\Instance\<Your Codec CLSID here>\Capabilities]
```



Die Schlüsseldaten sollten wie folgt lauten:


```C++
"{374ac4df-7c98-4257-b13d-36087dbee458}"=dword:00000001
```



 

 



