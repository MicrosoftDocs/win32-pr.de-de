---
title: InprocServer
description: Gibt den Pfad zur Prozess internen Server-DLL an.
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- InprocServer-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5682693d711f734bbc60def8a711f11e2bad0ef9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947703"
---
# <a name="inprocserver"></a><span data-ttu-id="a0272-104">InprocServer</span><span class="sxs-lookup"><span data-stu-id="a0272-104">InprocServer</span></span>

<span data-ttu-id="a0272-105">Gibt den Pfad zur Prozess internen Server-DLL an.</span><span class="sxs-lookup"><span data-stu-id="a0272-105">Specifies the path to the in-process server DLL.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a0272-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="a0272-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer
         (Default) = path
```

## <a name="remarks"></a><span data-ttu-id="a0272-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0272-107">Remarks</span></span>

<span data-ttu-id="a0272-108">Der **InprocServer** -Eintrag ist für einfügbar-Klassen relativ selten.</span><span class="sxs-lookup"><span data-stu-id="a0272-108">The **InprocServer** entry is relatively rare for insertable classes.</span></span>

<span data-ttu-id="a0272-109">Prozess interne Server werden zurzeit mit dem Registrierungs Eintrag **InprocServer** registriert.</span><span class="sxs-lookup"><span data-stu-id="a0272-109">In-process servers are currently registered using the **InprocServer** registry entry.</span></span> <span data-ttu-id="a0272-110">Die 32-Bit-und 64-Bit-in-Process-Server sollten den [**InProcServer32**](inprocserver32.md) -Eintrag verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0272-110">The 32-bit and 64-bit in-process servers should use the [**InprocServer32**](inprocserver32.md) entry.</span></span> <span data-ttu-id="a0272-111">Wenn ein Container die Registrierung nach einem in-Process-Server durchsucht, hat die 16-Bit-Version eine Priorität mit einem 16-Bit-Container, und die 32-Bit-Version hat eine Priorität mit einem 32-Bit-Container.</span><span class="sxs-lookup"><span data-stu-id="a0272-111">If a container is searching the registry for an in-process server, the 16-bit version has priority with a 16-bit container and 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0272-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a0272-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0272-113">**InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="a0272-113">**InprocServer32**</span></span>](inprocserver32.md)
</dt> </dl>

 

 




