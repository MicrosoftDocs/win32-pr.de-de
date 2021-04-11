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
# <a name="registering-mpeg2-codecs"></a><span data-ttu-id="3d1d4-103">Registrieren von MPEG2-Codecs</span><span class="sxs-lookup"><span data-stu-id="3d1d4-103">Registering MPEG2 Codecs</span></span>

<span data-ttu-id="3d1d4-104">Dieses Thema gilt nur für Windows XP Media Center Edition.</span><span class="sxs-lookup"><span data-stu-id="3d1d4-104">This topic applies to Windows XP Media Center Edition only.</span></span>

<span data-ttu-id="3d1d4-105">Windows XP Media Center Edition verwaltet zwei Registrierungsschlüssel, die verwendet werden, um zu bestimmen, welcher Codec zum Wiedergeben von Video-und Audiodateien für das Video verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d1d4-105">Windows XP Media Center Edition maintains two registry keys that it uses to determine which codec to use to play back MPEG2 video and audio files.</span></span> <span data-ttu-id="3d1d4-106">Der erste Registrierungsschlüssel gibt den bevorzugten MPEG2-Codec des Computerherstellers an, der zweite listet alle mit Media Center kompatiblen Codecs auf, die derzeit auf dem Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="3d1d4-106">The first registry key specifies the computer manufacturer's preferred MPEG2 codec, and the second lists all of the Media Center compatible codecs that are currently installed on the computer.</span></span> <span data-ttu-id="3d1d4-107">Wenn Media Center eine MPEG2-Datei wiedergeben muss, wird der bevorzugte Codec des Herstellers verwendet, sofern ein solcher angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3d1d4-107">When Media Center needs to play back an MPEG2 file, it uses the manufacturer's preferred codec, if one is specified.</span></span> <span data-ttu-id="3d1d4-108">Wenn dies nicht der Fall ist, wird der erste in der Registrierung aufgeführte Media Center-kompatible Codec verwendet.</span><span class="sxs-lookup"><span data-stu-id="3d1d4-108">If not, it uses the first Media Center compatible codec listed in the registry.</span></span> <span data-ttu-id="3d1d4-109">Wenn in der Registrierung keine bevorzugten oder kompatiblen Codecs angegeben sind, verwendet Media Center das standardmäßige DirectShow-Filter Verdienst, um einen Codec auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="3d1d4-109">If the registry specifies no preferred or compatible codecs, Media Center uses the standard DirectShow filter merit to choose a codec.</span></span>

<span data-ttu-id="3d1d4-110">Um sicherzustellen, dass Media Center immer einen kompatiblen MPEG2-Codec verwendet, sollten Hersteller von Media Center-Computern den bevorzugten MPEG2-Codec am folgenden Registrierungs Speicherort angeben:</span><span class="sxs-lookup"><span data-stu-id="3d1d4-110">To ensure that Media Center always uses a compatible MPEG2 codec, manufacturers of Media Center computers should specify the preferred MPEG2 codec at the following registry location:</span></span>


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Media Center\Service\Video
```



<span data-ttu-id="3d1d4-111">Die Schlüsseldaten sollten wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="3d1d4-111">The key data should be as follows:</span></span>


```C++
PreferredMPEG2VideoDecoder=REG_SZ "{MPEG2 Video CLSID GUID}"
PreferredMPEG2AudioDecoder=REG_SZ "{MPEG2 Audio CLSID GUID}"
```



<span data-ttu-id="3d1d4-112">Das Setup Programm für einen mit Media Center kompatiblen MPEG2-Codec sollte den Codec registrieren, indem zwei Instanzen des folgenden Registrierungsschlüssels erstellt werden – eine für den Videocodec und eine für den Audiocodec:</span><span class="sxs-lookup"><span data-stu-id="3d1d4-112">The setup program for a Media Center compatible MPEG2 codec should register the codec by creating two instances of the following registry key—one for the video codec and one for the audio codec:</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\{083863F1-70DE-11d0-BD40-00A0C911CE86}\Instance\<Your Codec CLSID here>\Capabilities]
```



<span data-ttu-id="3d1d4-113">Die Schlüsseldaten sollten wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="3d1d4-113">The key data should be as follows:</span></span>


```C++
"{374ac4df-7c98-4257-b13d-36087dbee458}"=dword:00000001
```



 

 



