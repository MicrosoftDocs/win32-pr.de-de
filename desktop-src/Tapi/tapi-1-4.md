---
description: TAPI 1.4 hat der Spezifikation 1.3 eine Reihe von APIs, Nachrichten, Konstanten und Strukturelementen hinzugefügt.
ms.assetid: 293f732f-0288-46d1-b542-d948c6179158
title: TAPI 1.4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f22833639813268420cc1ea202ef260964b42ce2e5119fafc8d0aa18593686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060358"
---
# <a name="tapi-14"></a>TAPI 1.4

TAPI 1.4 hat der Spezifikation 1.3 eine Reihe von APIs, Nachrichten, Konstanten und Strukturelementen hinzugefügt. TAPI 1.4 unterstützt nur 16-Bit-TSPs. Es ermöglicht jedoch die Entwicklung von 32-Bit-Anwendungen, ohne sich um die Einschränkungen der 16-Bit-Windows kümmern zu müssen.

Die TAPI- und TSPI-Headerdateien werden verwendet, um beide Anwendungen für TAPI 1.4 und TAPI 2.x zu entwickeln. Obwohl es nicht viele Änderungen an den Strukturen zwischen diesen beiden Spezifikationen gab, gab es Änderungen an der API (insbesondere Unicode-Unterstützung), die es sehr wichtig machen, zu beachten, dass die Header je nach TAPI CURRENT VERSION-Konstante unterschiedlich kompiliert \_ \_ werden. Beispiel:

``` syntax
#define TAPI_CURRENT_VERSION 0x00010004
#include <tapi.h>
```

> [!Note]  
> TAPI \_ CURRENT VERSION muss für alle \_ TAPI-Anwendungen definiert werden. Dies ist für die TAPI 2.x-Entwicklung zwar nicht unbedingt erforderlich, aber zukünftige Änderungen können dies erfordern.

 

 

 



