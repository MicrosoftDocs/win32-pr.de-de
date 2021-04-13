---
title: Abrufen von Informationen zu einem Film
description: Abrufen von Informationen zu einem Film
ms.assetid: 678272e0-67fe-4ec1-88a8-924a773445a7
keywords:
- mciSendCommand-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711fb56164a9dc440240f12c16b9adff1210db71
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314678"
---
# <a name="retrieving-information-about-a-movie"></a><span data-ttu-id="7f605-104">Abrufen von Informationen zu einem Film</span><span class="sxs-lookup"><span data-stu-id="7f605-104">Retrieving Information About a Movie</span></span>

<span data-ttu-id="7f605-105">Im folgenden Beispiel wird das Zeitformat auf Frames festgelegt, und die aktuelle Position wird abgerufen, wenn das Gerät mit der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7f605-105">The following example sets the time format to frames and obtains the current position if the device is playing using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


```C++
MCI_DGV_SET_PARMS mciSet; 
MCI_DGV_STATUS_PARMS mciStatus; 
 
// Put in frame mode. 
mciSet.dwTimeFormat = MCI_FORMAT_FRAMES; 
mciSendCommand(wDeviceID, MCI_SET, 
    MCI_SET_TIME_FORMAT, 
    (DWORD)(LPSTR)&mciSet); 
 
mciStatus.dwItem = MCI_STATUS_MODE; 
mciSendCommand(wDeviceID, MCI_STATUS, 
    MCI_STATUS_ITEM, 
    (DWORD)(LPSTR)&mciStatus); 
 
// If device is playing, get the position. 
if (mciStatus.dwReturn == MCI_MODE_PLAY)
{ 
    mciStatus.dwItem = MCI_STATUS_POSITION; 
    mciSendCommand(wDeviceID, MCI_STATUS, MCI_STATUS_ITEM, 
        (DWORD)(LPSTR)&mciStatus); 
 
    // Update the position from mciStatus.dwReturn. 
} 
```



 

 