---
title: Herstellen einer Verbindung mit einem Erfassungstreiber
description: Herstellen einer Verbindung mit einem Erfassungstreiber
ms.assetid: ce83329f-de5a-4428-bc0d-be5f3d35ff1a
keywords:
- capDriverDisconnect-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34e606c439143400f1ea1845db37e7faf93009350254c173c4003400c3996f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144863"
---
# <a name="connecting-to-a-capture-driver"></a>Herstellen einer Verbindung mit einem Erfassungstreiber

Im folgenden Beispiel wird das Erfassungsfenster mit dem Handle *hWndC* mit dem MSVIDEO-Treiber verbunden und dann mithilfe des Makros [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) getrennt:


```C++
fOK = SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0, 0L); 
// 
// Or, use the macro to connect to the MSVIDEO driver: 
// fOK = capDriverConnect(hWndC, 0); 
// 
// Place code to set up and capture video here. 
// 
capDriverDisconnect (hWndC); 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Video capture](using-video-capture.md)
</dt> </dl>

 

 




