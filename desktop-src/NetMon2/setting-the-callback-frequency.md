---
description: Verwenden Sie den folgenden Code, um die Rückruf Häufigkeit festzulegen.
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: Festlegen der Rückruf Häufigkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e03c260b6d289e473f27bb3ae6b84a3f42d0878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343868"
---
# <a name="setting-the-callback-frequency"></a>Festlegen der Rückruf Häufigkeit

Verwenden Sie den folgenden Code, um die Rückruf Häufigkeit festzulegen:

**DWORD** Wert = 1;


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



Dieses Code Fragment legt die Rückruf Häufigkeit auf 1 Sekunde (Minimalwert) fest. Der maximale Wert muss viel größer als 1 sein. Wenn der NPP-Puffer (Network Packet Provider) voll ist, ruft der NPP den Monitor früher wieder auf.

 

 



