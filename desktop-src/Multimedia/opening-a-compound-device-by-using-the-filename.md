---
title: Öffnen eines Verbundgeräts mithilfe des Dateinamens
description: Öffnen eines Verbundgeräts mithilfe des Dateinamens
ms.assetid: 5199bb68-44be-4fad-af5b-8fe89f27caee
keywords:
- mciSendCommand-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5ef021c283337c0cea2085d79fefa91667ce1dac095ff7ae17fcc448c9461c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806360"
---
# <a name="opening-a-compound-device-by-using-the-filename"></a>Öffnen eines Verbundgeräts mithilfe des Dateinamens

Im folgenden Beispiel wird das Waveform-Audio-Gerät geöffnet, indem eine Waveform-Audiodatei mit dem Namen "TIM SINUS" angegeben wird. WAV" mithilfe der [**mciSendCommand-Funktion.**](/previous-versions//dd757160(v=vs.85))


```C++
UINT wDeviceID;
DWORD dwReturn;
MCI_OPEN_PARMS mciOpenParms;
 
// Opens a waveform-audio device by specifying the device and 
// file name.

mciOpenParms.lpstrDeviceType = "waveaudio";
mciOpenParms.lpstrElementName = "timpani.wav";

if (dwReturn = mciSendCommand(NULL, MCI_OPEN,
    MCI_OPEN_TYPE | MCI_OPEN_ELEMENT, (DWORD)(LPVOID) &mciOpenParms))
{
    
    // Error, unable to open device.
    
}

// The device opened successfully; get the device ID.
wDeviceID = mciOpenParms.wDeviceID;
```



 

 