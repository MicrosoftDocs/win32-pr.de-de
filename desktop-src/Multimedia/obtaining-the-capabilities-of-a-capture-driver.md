---
title: Abrufen der Funktionen eines Erfassungstreibers
description: Abrufen der Funktionen eines Erfassungstreibers
ms.assetid: 17e90ca6-3646-41cb-8d7a-a2102bc16cc5
keywords:
- WM_CAP_DRIVER_GET_CAPS Meldung
- capDriverGetCaps-Makro
- CAPDRIVERCAPS-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6f717f1a7c19878ceeca2cccc2db309be3e62e0febf90dcb23376db73eed17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806570"
---
# <a name="obtaining-the-capabilities-of-a-capture-driver"></a>Abrufen der Funktionen eines Erfassungstreibers

Die [**MELDUNG WM CAP DRIVER GET \_ \_ \_ \_ CAPS**](wm-cap-driver-get-caps.md) gibt die Funktionen des Erfassungstreibers und der zugrunde liegenden Hardware in der [**CAPDRIVERCAPS-Struktur**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) zurück. Jedes Mal, wenn eine Anwendung einen neuen Erfassungstreiber mit dem Erfassungsfenster verbindet, sollte die **CAPDRIVERCAPS-Struktur** aktualisiert werden. Im folgenden Beispiel wird das [**CapDriverGetCaps-Makro**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) verwendet, um die Funktionen des Erfassungstreibers abzurufen.


```C++
CAPDRIVERCAPS CapDrvCaps; 

SendMessage (hWndC, WM_CAP_DRIVER_GET_CAPS, 
    sizeof (CAPDRIVERCAPS), (LONG) (LPVOID) &CapDrvCaps); 

// Or, use the macro to retrieve the driver capabilities. 
// capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Video capture](using-video-capture.md)
</dt> </dl>

 

 




