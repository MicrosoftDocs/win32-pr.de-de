---
title: Abrufen der Funktionen eines Erfassungs Treibers
description: Abrufen der Funktionen eines Erfassungs Treibers
ms.assetid: 17e90ca6-3646-41cb-8d7a-a2102bc16cc5
keywords:
- WM_CAP_DRIVER_GET_CAPS Meldung
- capdrivergetcaps-Makro
- Capdrivercaps-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d15a3b1e01ccff738494f287126b7e1ab033056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337398"
---
# <a name="obtaining-the-capabilities-of-a-capture-driver"></a>Abrufen der Funktionen eines Erfassungs Treibers

Die Meldung " [**WM- \_ Cap- \_ Treiber \_ get \_ Caps**](wm-cap-driver-get-caps.md) " gibt die Funktionen des Aufzeichnungs Treibers und der zugrunde liegenden Hardware in der [**capdrivercaps**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) -Struktur zurück. Jedes Mal, wenn eine Anwendung einen neuen Aufzeichnungs Treiber mit dem Erfassungsfenster verbindet, sollte Sie die **capdrivercaps** -Struktur aktualisieren. Im folgenden Beispiel wird das [**capdrivergetcaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) -Makro verwendet, um die Aufzeichnungs Treiberfunktionen zu erhalten.


```C++
CAPDRIVERCAPS CapDrvCaps; 

SendMessage (hWndC, WM_CAP_DRIVER_GET_CAPS, 
    sizeof (CAPDRIVERCAPS), (LONG) (LPVOID) &CapDrvCaps); 

// Or, use the macro to retrieve the driver capabilities. 
// capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Video Erfassung](using-video-capture.md)
</dt> </dl>

 

 




