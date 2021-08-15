---
description: Veranschaulicht, welcher Registrierungsschlüssel festgelegt werden muss, um die automatische Wiedergabe zu verhindern.
ms.assetid: E0A25DC2-0991-45D6-9185-019DB4C040AD
title: Verhindern der automatischen Wiedergabe für eine Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3b44817f6803c25bbf506a5f76c8b068c683af4b5d4c7536482c30cd3aee2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859687"
---
# <a name="how-to-prevent-autoplay-for-a-component"></a>Verhindern der automatischen Wiedergabe für eine Komponente

Veranschaulicht, welcher Registrierungsschlüssel festgelegt werden muss, um die automatische Wiedergabe zu verhindern.

## <a name="instructions"></a>Anweisungen


Um zu verhindern, dass AutoPlay als Reaktion auf ein Ereignis gestartet wird, fügen Sie den folgenden **REG \_ SZ-Wert** hinzu, wie in diesem Beispiel gezeigt.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     CancelAutoplay
                        CLSID
                           00000000-0000-0000-0000-000000000000
```

Der Wert ist der Klassenbezeichner (CLSID), von dem die Komponente, die das Ereignis generiert, in der ausgeführten Objekttabelle (ROT) bekannt ist. Der Wert verfügt über keine Daten.

> [!IMPORTANT]
> Unter diesem Schlüssel sind die CLSIDs nicht in geschweifte Klammern () {} eingeschlossen.

 

 

 



