---
title: Öffnen des Wiedergabefensters
description: Öffnen des Wiedergabefensters
ms.assetid: 180f3fb9-cdcb-49ec-a708-84a597295b2f
keywords:
- MCI_OPEN Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11aed7802a3536beb069c1fd7048b66be217d21f0dd3e47fa21caaad80d854e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806170"
---
# <a name="opening-the-playback-window"></a>Öffnen des Wiedergabefensters

Das folgende Beispiel zeigt, wie Sie mit dem [**MCI \_ OPEN-Befehl**](mci-open.md) ein übergeordnetes Fenster festlegen und ein untergeordnetes Element dieses Fensters erstellen.


```C++
MCI_DGV_OPEN_PARMS    mciOpen; 
 
mciOpen.lpstrElementName = lpstrFile;  // Set the filename.
mciOpen.dwStyle = WS_CHILD;            // Set the style. 
mciOpen.hWndParent = hWnd;             // Give a window handle. 
 
if (mciSendCommand(0, MCI_OPEN, 
   (DWORD)(MCI_OPEN_ELEMENT|MCI_DGV_OPEN_PARENT|MCI_DGV_OPEN), 
   (DWORD)(LPSTR)&mciOpen) == 0)
{ 
    // Open operation is successful. Continue. 
} 
```



 

 




