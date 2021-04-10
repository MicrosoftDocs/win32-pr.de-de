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
# <a name="device-control-windows-multimedia"></a>Geräte Steuerelement (Windows Multimedia)

Wenn Sie ein MCI-Gerät steuern möchten, öffnen Sie das Gerät, senden Sie die erforderlichen Befehle an das Gerät, und schließen Sie das Gerät. Die Befehle können auch bei vollkommen unterschiedlichen MCI-Geräten sehr ähnlich sein. Beispielsweise gibt die folgende Reihe von MCI-Befehlen die sechste Spur einer AudioCD mit der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion aus:


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



Das nächste Beispiel zeigt eine ähnliche Reihe von MCI-Befehlen, die die ersten 10.000-Beispiele einer Waveform-Audiodatei wiedergeben:


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

-   Die gleichen grundlegenden Befehle ([**Öffnen**](open.md), festlegen [**, wieder**](play.md) [**geben**](set.md)und [**Schließen**](close.md)) werden mit CD-Audiogeräten und Waveform-Audiogeräten verwendet. Die gleichen MCI-Befehle werden für alle MCI-Geräte verwendet.
-   Der Open-Befehl für das Waveform-Audiogerät enthält eine Datei namens Spezifikation. Das Waveform-Audiogerät ist ein *Verbund Gerät* (das einer Datendatei zugeordnet ist), während es sich bei dem CD-Audiogerät um ein *einfaches Gerät* handelt (eines ohne zugeordnete Datendatei).
-   Der SET-Befehl gibt in jedem Fall Zeitformate an, aber das Zeitformat Kennzeichen für das CD-Audiogerät gibt das TMSF-Format (Tracks/Minutes/seconds/Frames) an, während das mit dem Waveform-Audiogerät verwendete Zeitformat "Samples" angibt.
-   Die Variablen, die mit den Flags "from" und "to" verwendet werden, sind für das jeweilige Zeitformat geeignet. Beispielsweise geben die Variablen für das CD-Audiogerät einen Bereich von Spuren an, aber für das Waveform-Audiogerät geben die Variablen einen Bereich von Beispielen an.

 

 
