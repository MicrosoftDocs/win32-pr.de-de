---
title: InprocHandler
description: InprocHandler gibt an, ob eine Anwendung einen benutzerdefinierten Handler im HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID verwendet.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- InprocHandler-Registrierungsschlüssel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aea1ca0d5eb5dec58a36578d268d7020a963a95e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404733"
---
# <a name="inprochandler"></a><span data-ttu-id="5a8d3-104">InprocHandler</span><span class="sxs-lookup"><span data-stu-id="5a8d3-104">InprocHandler</span></span>

<span data-ttu-id="5a8d3-105">Gibt an, ob eine Anwendung einen benutzerdefinierten Handler verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a8d3-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="5a8d3-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="5a8d3-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="5a8d3-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a8d3-107">Remarks</span></span>

<span data-ttu-id="5a8d3-108">Dies ist ein **REG \_ SZ-Wert,** der den benutzerdefinierten Handler angibt, der von der Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a8d3-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="5a8d3-109">Wenn kein benutzerdefinierter Handler verwendet wird, sollte der Eintrag auf Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="5a8d3-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="5a8d3-110">Wenn ein Container in der Registrierung nach einem benutzerdefinierten Handler sucht, hat die 16-Bit-Version Priorität mit einem 16-Bit-Container, und die 32-Bit-Version hat Priorität mit einem 32-Bit-Container.</span><span class="sxs-lookup"><span data-stu-id="5a8d3-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a8d3-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5a8d3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a8d3-112">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="5a8d3-112">**InprocHandler32**</span></span>](inprochandler32.md)
</dt> </dl>

 

 




