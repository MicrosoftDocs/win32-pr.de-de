---
title: Öffnen eines einfachen Geräts mithilfe der Device-Type Konstante
description: Öffnen eines einfachen Geräts mithilfe der Device-Type Konstante
ms.assetid: 6ed5fd4b-534a-4e03-8130-07f831403a8e
keywords:
- mciSendCommand-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 810915331fc00f72f4ab705cd01c91ecabf5d190efca4f4a9c786a36d7880103
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806330"
---
# <a name="opening-a-simple-device-by-using-the-device-type-constant"></a>Öffnen eines einfachen Geräts mithilfe der Device-Type Konstante

Im folgenden Beispiel wird ein CD-Audiogerät geöffnet, indem eine Gerätetypkonstante mithilfe der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) angegeben wird.


```C++
UINT wDeviceID;
DWORD dwReturn;
MCI_OPEN_PARMS mciOpenParms;

// Opens a CD audio device by specifying a device-type constant.

mciOpenParms.lpstrDeviceType = (LPCSTR) MCI_DEVTYPE_CD_AUDIO;

if (dwReturn = mciSendCommand(NULL, MCI_OPEN,
    MCI_OPEN_TYPE | MCI_OPEN_TYPE_ID, (DWORD)(LPVOID) &mciOpenParms))
{
    
    // Error, unable to open device.
    
}

// The device opened successfully; get the device ID.
wDeviceID = mciOpenParms.wDeviceID;
```



 

 