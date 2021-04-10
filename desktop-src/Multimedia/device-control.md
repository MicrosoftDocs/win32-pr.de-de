---
title: Geräte Steuerelement (Windows Multimedia)
description: Gerätesteuerung
ms.assetid: b4479803-f1da-4646-909e-c4ef412ebdcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0e0b59127d160cc44418fd4bce1f9f670d13de
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039985"
---
# <a name="device-control-windows-multimedia"></a><span data-ttu-id="a7133-103">Geräte Steuerelement (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="a7133-103">Device Control (Windows Multimedia)</span></span>

<span data-ttu-id="a7133-104">Wenn Sie ein MCI-Gerät steuern möchten, öffnen Sie das Gerät, senden Sie die erforderlichen Befehle an das Gerät, und schließen Sie das Gerät.</span><span class="sxs-lookup"><span data-stu-id="a7133-104">To control an MCI device, you open the device, send the necessary commands to it, and then close the device.</span></span> <span data-ttu-id="a7133-105">Die Befehle können auch bei vollkommen unterschiedlichen MCI-Geräten sehr ähnlich sein.</span><span class="sxs-lookup"><span data-stu-id="a7133-105">The commands can be very similar, even for completely different MCI devices.</span></span> <span data-ttu-id="a7133-106">Beispielsweise gibt die folgende Reihe von MCI-Befehlen die sechste Spur einer AudioCD mit der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion aus:</span><span class="sxs-lookup"><span data-stu-id="a7133-106">For example, the following series of MCI commands plays the sixth track of an audio CD by using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function:</span></span>


```C++
mciSendString("open cdaudio", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("set cdaudio time format tmsf", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play cdaudio from 6 to 7", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close cdaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="a7133-107">Das nächste Beispiel zeigt eine ähnliche Reihe von MCI-Befehlen, die die ersten 10.000-Beispiele einer Waveform-Audiodatei wiedergeben:</span><span class="sxs-lookup"><span data-stu-id="a7133-107">The next example shows a similar series of MCI commands that plays the first 10,000 samples of a waveform-audio file:</span></span>


```C++
mciSendString(
    "open c:\mmdata\purplefi.wav type waveaudio alias finch", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
mciSendString("set finch time format samples", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play finch from 1 to 10000", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close finch", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="a7133-108">Diese Beispiele veranschaulichen einige interessante Fakten zu MCI-Befehlen:</span><span class="sxs-lookup"><span data-stu-id="a7133-108">These examples illustrate some interesting facts about MCI commands:</span></span>

-   <span data-ttu-id="a7133-109">Die gleichen grundlegenden Befehle ([**Öffnen**](open.md), festlegen [**, wieder**](play.md) [**geben**](set.md)und [**Schließen**](close.md)) werden mit CD-Audiogeräten und Waveform-Audiogeräten verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7133-109">The same basic commands ([**open**](open.md), [**set**](set.md), [**play**](play.md), and [**close**](close.md)) are used with CD audio and waveform-audio devices.</span></span> <span data-ttu-id="a7133-110">Die gleichen MCI-Befehle werden für alle MCI-Geräte verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7133-110">The same MCI commands are used with all MCI devices.</span></span>
-   <span data-ttu-id="a7133-111">Der Open-Befehl für das Waveform-Audiogerät enthält eine Datei namens Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="a7133-111">The open command for the waveform-audio device includes a filename specification.</span></span> <span data-ttu-id="a7133-112">Das Waveform-Audiogerät ist ein *Verbund Gerät* (das einer Datendatei zugeordnet ist), während es sich bei dem CD-Audiogerät um ein *einfaches Gerät* handelt (eines ohne zugeordnete Datendatei).</span><span class="sxs-lookup"><span data-stu-id="a7133-112">The waveform-audio device is a *compound device* (one associated with a data file), while the CD audio device is a *simple device* (one without an associated data file).</span></span>
-   <span data-ttu-id="a7133-113">Der SET-Befehl gibt in jedem Fall Zeitformate an, aber das Zeitformat Kennzeichen für das CD-Audiogerät gibt das TMSF-Format (Tracks/Minutes/seconds/Frames) an, während das mit dem Waveform-Audiogerät verwendete Zeitformat "Samples" angibt.</span><span class="sxs-lookup"><span data-stu-id="a7133-113">The set command specifies time formats in each case, but the time-format flag for the CD audio device specifies tracks/minutes/seconds/frames (TMSF) format, while the time format used with the waveform-audio device specifies "samples".</span></span>
-   <span data-ttu-id="a7133-114">Die Variablen, die mit den Flags "from" und "to" verwendet werden, sind für das jeweilige Zeitformat geeignet.</span><span class="sxs-lookup"><span data-stu-id="a7133-114">The variables used with the "from" and "to" flags are appropriate to the respective time format.</span></span> <span data-ttu-id="a7133-115">Beispielsweise geben die Variablen für das CD-Audiogerät einen Bereich von Spuren an, aber für das Waveform-Audiogerät geben die Variablen einen Bereich von Beispielen an.</span><span class="sxs-lookup"><span data-stu-id="a7133-115">For example, for the CD audio device, the variables specify a range of tracks, but for the waveform-audio device, the variables specify a range of samples.</span></span>

 

 
