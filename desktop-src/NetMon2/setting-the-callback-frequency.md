---
description: Verwenden Sie den folgenden Code, um die Rückrufhäufigkeit zu festlegen.
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: Festlegen der Rückrufhäufigkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f235377865583e48d6a4b9c16abce4209e6449f74ed3cf42688dfa417287bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363246"
---
# <a name="setting-the-callback-frequency"></a>Festlegen der Rückrufhäufigkeit

Verwenden Sie den folgenden Code, um die Rückrufhäufigkeit fest zu legen:

**DWORD** Wert = 1;


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



Dieses Codefragment legt die Rückrufhäufigkeit auf 1 Sekunde (mindestwert) fest. Der Höchstwert muss viel größer als 1 sein. Wenn der Puffer des Netzwerkpaketanbieters (Network Packet Provider, NPP) voll ist, ruft der NPP den Monitor früher zurück.

 

 



