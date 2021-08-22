---
title: Gerätesteuerung (Windows Multimedia)
description: Gerätesteuerung
ms.assetid: b4479803-f1da-4646-909e-c4ef412ebdcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6878e5e759f3eddb5e98d241d9a8d081005e3545dc2f0054b46630619eaa06fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497240"
---
# <a name="device-control-windows-multimedia"></a>Gerätesteuerung (Windows Multimedia)

Um ein MCI-Gerät zu steuern, öffnen Sie das Gerät, senden die erforderlichen Befehle an es und schließen dann das Gerät. Die Befehle können sehr ähnlich sein, auch für vollständig unterschiedliche MCI-Geräte. Die folgende Reihe von MCI-Befehlen gibt beispielsweise den sechsten Titel einer Audio-CD mithilfe der [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) wieder:


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



Das nächste Beispiel zeigt eine ähnliche Reihe von MCI-Befehlen, die die ersten 10.000 Beispiele einer Waveform-Audiodatei wieder geben:


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



Diese Beispiele veranschaulichen einige interessante Fakten zu MCI-Befehlen:

-   Die gleichen grundlegenden Befehle ([**öffnen**](open.md), [**festlegen,**](set.md) [**wiederverspielen**](play.md)und schließen [**)**](close.md)werden für CD-Audio- und Waveform-Audiogeräte verwendet. Die gleichen MCI-Befehle werden für alle MCI-Geräte verwendet.
-   Der Open-Befehl für das Waveform-Audio-Gerät enthält eine Dateinamenspezifikation. Das Waveform-Audio-Gerät ist ein zusammengesetztes Gerät *(das* einer Datendatei zugeordnet ist), während das CD-Audiogerät ein einfaches Gerät *(ein* Gerät ohne zugeordnete Datendatei) ist.
-   Der Set-Befehl gibt in jedem Fall Zeitformate an, aber das Zeitformatflag für das CD-Audiogerät gibt das TMSF-Format (tracks/minutes/seconds/frames) an, während das Zeitformat, das mit dem Waveform-Audio-Gerät verwendet wird, "Samples" angibt.
-   Die Variablen, die mit den Flags "from" und "to" verwendet werden, sind für das jeweilige Zeitformat geeignet. Für das CD-Audiogerät geben die Variablen beispielsweise einen Bereich von Spuren an, aber für das Waveform-Audio-Gerät geben die Variablen einen Bereich von Stichproben an.

 

 
