---
title: Verwenden des MCI_NOTIFY-Flags
description: Verwenden des MCI \_ NOTIFY-Flags
ms.assetid: 1d1803c8-f315-463e-ae0d-a258aa3af3c9
keywords:
- MCI_NOTIFY-Flag
- MCI_PLAY Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b0e7269ee7d80dd47372d9210fbdbc1332b3a88a96e2a17d6719c9945ab30aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136138"
---
# <a name="using-the-mci_notify-flag"></a>Verwenden des MCI \_ NOTIFY-Flags

Das folgende Beispiel zeigt, wie das MCI \_ NOTIFY-Flag mit dem [**MCI \_ PLAY-Befehl**](mci-play.md) verwendet wird. Das Handle für die Fensterprozedur, die die [**MM \_ MCINOTIFY-Nachricht**](mm-mcinotify.md) verarbeitet, wird in *hwnd* angegeben.


```C++
MCI_DGV_PLAY_PARMS mciPlay; 
DWORD dwFlags; 
 
mciPlay.dwCallback = MAKELONG(hwnd, 0); 
dwFlags = MCI_NOTIFY; 
 
mciSendCommand(wMCIDeviceID, MCI_PLAY, dwFlags, (DWORD)(LPSTR)&mciPlay); 
```



 

 




