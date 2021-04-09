---
description: Die folgende "winternl. h"-Definition ist die statische Speicheradresse der aktiven Terminal Dienste-Konsolen Sitzungs-ID. Diese aktive Konsolen Sitzungs-ID ist nicht in Versionen des Microsoft Windows-Betriebssystems vor Windows XP definiert.
ms.assetid: f3022ab8-60ea-490b-a87d-cc1afc99d26f
title: Die ID der aktiven Konsolen Sitzung wird erhalten.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936db3f8038348864fc90fc55eeb4287a67c45d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860996"
---
# <a name="getting-the-active-console-session-id"></a><span data-ttu-id="811e0-104">Die ID der aktiven Konsolen Sitzung wird erhalten.</span><span class="sxs-lookup"><span data-stu-id="811e0-104">Getting the Active Console Session ID</span></span>

<span data-ttu-id="811e0-105">Die folgende "winternl. h"-Definition ist die statische Speicheradresse der aktiven Terminal Dienste-Konsolen Sitzungs-ID.</span><span class="sxs-lookup"><span data-stu-id="811e0-105">The following Winternl.h definition is the static memory address of the active Terminal Services console session ID.</span></span> <span data-ttu-id="811e0-106">Diese aktive Konsolen Sitzungs-ID ist nicht in Versionen des Microsoft Windows-Betriebssystems vor Windows XP definiert.</span><span class="sxs-lookup"><span data-stu-id="811e0-106">This active console session ID is not defined in versions of the Microsoft Windows operating system earlier than Windows XP.</span></span>

> [!Note]  
> <span data-ttu-id="811e0-107">Diese Definition kann sich in zukünftigen Versionen von Windows ändern.</span><span class="sxs-lookup"><span data-stu-id="811e0-107">This definition may change in future releases of Windows.</span></span> <span data-ttu-id="811e0-108">Um sicherzustellen, dass Ihre Anwendung in Zukunft weiterhin ordnungsgemäß ausgeführt wird, muss die Anwendung [**WFS getactiveconsolesessionid**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="811e0-108">To ensure that your application will continue to run correctly in the future, your application must call [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).</span></span>

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 
