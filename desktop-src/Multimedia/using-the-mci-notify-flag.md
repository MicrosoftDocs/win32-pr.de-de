---
title: Verwenden des MCI_NOTIFY-Flags
description: Verwenden des MCI- \_ Benachrichtigungs Flags
ms.assetid: 1d1803c8-f315-463e-ae0d-a258aa3af3c9
keywords:
- MCI_NOTIFY-Flag
- MCI_PLAY-Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472613d2e6efcd6b30c88ed64dfa7875b4742527
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855687"
---
# <a name="using-the-mci_notify-flag"></a><span data-ttu-id="6b6ba-105">Verwenden des MCI- \_ Benachrichtigungs Flags</span><span class="sxs-lookup"><span data-stu-id="6b6ba-105">Using the MCI\_NOTIFY Flag</span></span>

<span data-ttu-id="6b6ba-106">Das folgende Beispiel zeigt, wie das MCI- \_ Benachrichtigungs Kennzeichen mit dem MCI-Befehl " [**\_ Play**](mci-play.md) " verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b6ba-106">The following example shows how the MCI\_NOTIFY flag is used with the [**MCI\_PLAY**](mci-play.md) command.</span></span> <span data-ttu-id="6b6ba-107">Das Handle für die Fenster Prozedur, die die [**mm- \_**](mm-mcinotify.md) Meldung mit dem Fehlercode verarbeitet, wird in *HWND* angegeben.</span><span class="sxs-lookup"><span data-stu-id="6b6ba-107">The handle to the window procedure that will process the [**MM\_MCINOTIFY**](mm-mcinotify.md) message is specified in *hwnd*.</span></span>


```C++
MCI_DGV_PLAY_PARMS mciPlay; 
DWORD dwFlags; 
 
mciPlay.dwCallback = MAKELONG(hwnd, 0); 
dwFlags = MCI_NOTIFY; 
 
mciSendCommand(wMCIDeviceID, MCI_PLAY, dwFlags, (DWORD)(LPSTR)&mciPlay); 
```



 

 




