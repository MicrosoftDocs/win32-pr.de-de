---
title: InprocHandler32
description: Gibt an, ob eine Anwendung einen benutzerdefinierten Handler verwendet.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- InprocHandler32 Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c918669aa3de1c8cf2622e3caf4acc9ae18f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388083"
---
# <a name="inprochandler32"></a><span data-ttu-id="4a83e-104">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="4a83e-104">InprocHandler32</span></span>

<span data-ttu-id="4a83e-105">Gibt an, ob eine Anwendung einen benutzerdefinierten Handler verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a83e-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="4a83e-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="4a83e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="4a83e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a83e-107">Remarks</span></span>

<span data-ttu-id="4a83e-108">Dies ist ein **reg \_ SZ** -Wert, der den benutzerdefinierten Handler angibt, der von der Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4a83e-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="4a83e-109">Wenn kein benutzerdefinierter Handler verwendet wird, sollte der Eintrag auf Ole32.dll festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4a83e-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="4a83e-110">Wenn ein Container die Registrierung nach einem benutzerdefinierten Handler durchsucht, hat die 16-Bit-Version eine Priorität mit einem 16-Bit-Container, und die 32-Bit-Version hat eine Priorität mit einem 32-Bit-Container.</span><span class="sxs-lookup"><span data-stu-id="4a83e-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a83e-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a83e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a83e-112">**InprocHandler**</span><span class="sxs-lookup"><span data-stu-id="4a83e-112">**InprocHandler**</span></span>](inprochandler.md)
</dt> </dl>

 

 




