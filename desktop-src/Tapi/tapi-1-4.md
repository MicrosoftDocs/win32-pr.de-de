---
description: TAPI 1,4 hat der 1,3-Spezifikation eine Reihe von APIs, Nachrichten, Konstanten und Strukturelementen hinzugefügt.
ms.assetid: 293f732f-0288-46d1-b542-d948c6179158
title: TAPI 1,4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32f4320043ada2e2ae5477a698bde63f28d2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959709"
---
# <a name="tapi-14"></a>TAPI 1,4

TAPI 1,4 hat der 1,3-Spezifikation eine Reihe von APIs, Nachrichten, Konstanten und Strukturelementen hinzugefügt. TAPI 1,4 unterstützt nur 16-Bit-TSPS. Allerdings können 32-Bit-Anwendungen entwickelt werden, ohne sich Gedanken über die Einschränkungen von 16-Bit-Fenstern machen zu müssen.

Die TAPI-und TSPI-Header Dateien werden verwendet, um beide Anwendungen sowohl für TAPI 1,4 als auch für TAPI 2. x zu entwickeln. Es gab zwar nicht viele Änderungen an den Strukturen zwischen diesen beiden Spezifikationen, aber es gab Änderungen an der API (insbesondere Unicode-Unterstützung), die es sehr wichtig zu beachten, dass die Header in Abhängigkeit von der aktuellen TAPI-Versions Konstante anders kompiliert werden \_ \_ . Beispiel:

``` syntax
#define TAPI_CURRENT_VERSION 0x00010004
#include <tapi.h>
```

> [!Note]  
> Die \_ aktuelle TAPI- \_ Version muss für alle TAPI-Anwendungen definiert werden. Obwohl es für die TAPI 2. x-Entwicklung nicht unbedingt notwendig ist, können zukünftige Änderungen auftreten, um dies zu erfordern.

 

 

 



