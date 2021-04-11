---
description: Der folgende Beispielcode der x86-Assembly Ruft die Terminal Dienste-Sitzungs-ID ab, die dem aktuellen Prozess zugeordnet ist.
ms.assetid: 9fcb35cb-6813-46a5-aa38-e102f1b6b7dc
title: Die Sitzungs-ID des aktuellen Prozesses wird erhalten.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac76865bcfe9144e8b95d4642385804aaf1af8fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126619"
---
# <a name="getting-the-session-id-of-the-current-process"></a>Die Sitzungs-ID des aktuellen Prozesses wird erhalten.

\[Die in diesem Beispielcode angegebenen Speicheradressen können sich in zukünftigen Versionen von Windows ändern. Um sicherzustellen, dass Ihre Anwendung in Zukunft weiterhin ordnungsgemäß ausgeführt wird, muss Ihre Anwendung [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) und dann [**processidtosessionid**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) anstelle des folgenden Beispielcodes aufrufen.\]

Der folgende Beispielcode der x86-Assembly Ruft die Terminal Dienste-Sitzungs-ID ab, die dem aktuellen Prozess zugeordnet ist.

``` syntax
mov     eax,fs:[00000018]
mov     eax,[eax+0x30]
mov     eax,[eax+0x1d4]
```

 

 
