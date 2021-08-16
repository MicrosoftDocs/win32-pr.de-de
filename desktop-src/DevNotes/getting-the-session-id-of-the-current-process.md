---
description: Der folgende x86-Beispielassemblycode ruft die Terminal services-Sitzungs-ID ab, die dem aktuellen Prozess zugeordnet ist.
ms.assetid: 9fcb35cb-6813-46a5-aa38-e102f1b6b7dc
title: Abrufen der Sitzungs-ID des aktuellen Prozesses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4326020f145c98544132703611fbd783edac9ae9eb89a5c69f44b67dc997ca30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955979"
---
# <a name="getting-the-session-id-of-the-current-process"></a>Abrufen der Sitzungs-ID des aktuellen Prozesses

\[Die in diesem Beispielcode angegebenen Speicheradressen können sich in zukünftigen Releases von Windows ändern. Um sicherzustellen, dass Ihre Anwendung in Zukunft weiterhin ordnungsgemäß ausgeführt wird, muss Ihre Anwendung [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) und dann [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) anstelle des folgenden Beispielcodes aufrufen.\]

Der folgende x86-Beispielassemblycode ruft die Terminal services-Sitzungs-ID ab, die dem aktuellen Prozess zugeordnet ist.

``` syntax
mov     eax,fs:[00000018]
mov     eax,[eax+0x30]
mov     eax,[eax+0x1d4]
```

 

 
