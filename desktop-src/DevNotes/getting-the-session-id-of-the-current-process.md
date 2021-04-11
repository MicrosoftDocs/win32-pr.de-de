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
# <a name="getting-the-session-id-of-the-current-process"></a><span data-ttu-id="b2516-103">Die Sitzungs-ID des aktuellen Prozesses wird erhalten.</span><span class="sxs-lookup"><span data-stu-id="b2516-103">Getting the Session ID of the Current Process</span></span>

<span data-ttu-id="b2516-104">\[Die in diesem Beispielcode angegebenen Speicheradressen können sich in zukünftigen Versionen von Windows ändern.</span><span class="sxs-lookup"><span data-stu-id="b2516-104">\[The memory addresses specified by this example code may change in future releases of Windows.</span></span> <span data-ttu-id="b2516-105">Um sicherzustellen, dass Ihre Anwendung in Zukunft weiterhin ordnungsgemäß ausgeführt wird, muss Ihre Anwendung [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) und dann [**processidtosessionid**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) anstelle des folgenden Beispielcodes aufrufen.\]</span><span class="sxs-lookup"><span data-stu-id="b2516-105">To ensure that your application will continue to run correctly in the future, your application must call [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) and then [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) instead of the following sample code.\]</span></span>

<span data-ttu-id="b2516-106">Der folgende Beispielcode der x86-Assembly Ruft die Terminal Dienste-Sitzungs-ID ab, die dem aktuellen Prozess zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b2516-106">The following example x86 assembly code gets the Terminal Services session ID associated with the current process.</span></span>

``` syntax
mov     eax,fs:[00000018]
mov     eax,[eax+0x30]
mov     eax,[eax+0x1d4]
```

 

 
