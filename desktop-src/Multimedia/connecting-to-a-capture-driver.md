---
title: Herstellen einer Verbindung mit einem Aufzeichnungs Treiber
description: Herstellen einer Verbindung mit einem Aufzeichnungs Treiber
ms.assetid: ce83329f-de5a-4428-bc0d-be5f3d35ff1a
keywords:
- capdriverdisconnect-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2161279f5b8b8dc528ee548d0a6a8ad6e9b397f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342051"
---
# <a name="connecting-to-a-capture-driver"></a>Herstellen einer Verbindung mit einem Aufzeichnungs Treiber

Im folgenden Beispiel wird die Verbindung zwischen dem Erfassungsfenster und dem *hwndc* -Handle mit dem MSVIDEO-Treiber hergestellt, und die Verbindung wird dann mit dem-Makro [**capdriverdisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) getrennt:


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

[Verwenden der Video Erfassung](using-video-capture.md)
</dt> </dl>

 

 




