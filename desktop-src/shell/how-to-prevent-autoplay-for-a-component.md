---
description: Veranschaulicht, welcher Registrierungsschlüssel festgelegt werden muss, um eine automatische Wiedergabe zu verhindern.
ms.assetid: E0A25DC2-0991-45D6-9185-019DB4C040AD
title: Verhindern von AutoPlay für eine Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebe03473ce7c5eb441ec428cbe4d060dc62f042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979529"
---
# <a name="how-to-prevent-autoplay-for-a-component"></a>Verhindern von AutoPlay für eine Komponente

Veranschaulicht, welcher Registrierungsschlüssel festgelegt werden muss, um eine automatische Wiedergabe zu verhindern.

## <a name="instructions"></a>Instructions


Fügen Sie den folgenden **reg \_ SZ** -Wert hinzu, um zu verhindern, dass die Wiedergabe als Reaktion auf ein Ereignis gestartet wird, wie in diesem Beispiel gezeigt.

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

Der Wert ist der Klassen Bezeichner (CLSID), der von der Komponente, die das Ereignis erstellt, in der laufenden Objekttabelle (rot) bekannt ist. Der Wert enthält keine Daten.

> [!IMPORTANT]
> Unter diesem Schlüssel werden die CLSIDs nicht in geschweifte Klammern ( {} ) eingeschlossen.

 

 

 



