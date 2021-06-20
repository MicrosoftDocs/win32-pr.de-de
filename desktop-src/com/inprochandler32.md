---
title: InprocHandler32
description: InprocHandler32 gibt an, ob eine Anwendung einen benutzerdefinierten Handler im HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID verwendet.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- InprocHandler32-Registrierungsschlüssel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be73a8b2577a554b0bb8b5ba5a851e630edbf90a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406003"
---
# <a name="inprochandler32"></a><span data-ttu-id="2e12b-104">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="2e12b-104">InprocHandler32</span></span>

<span data-ttu-id="2e12b-105">Gibt an, ob eine Anwendung einen benutzerdefinierten Handler verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e12b-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="2e12b-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="2e12b-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="2e12b-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e12b-107">Remarks</span></span>

<span data-ttu-id="2e12b-108">Dies ist ein **REG \_ SZ-Wert,** der den benutzerdefinierten Handler angibt, der von der Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2e12b-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="2e12b-109">Wenn kein benutzerdefinierter Handler verwendet wird, sollte der Eintrag auf Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="2e12b-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="2e12b-110">Wenn ein Container in der Registrierung nach einem benutzerdefinierten Handler sucht, hat die 16-Bit-Version Priorität mit einem 16-Bit-Container, und die 32-Bit-Version hat Priorität mit einem 32-Bit-Container.</span><span class="sxs-lookup"><span data-stu-id="2e12b-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e12b-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2e12b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e12b-112">**InprocHandler**</span><span class="sxs-lookup"><span data-stu-id="2e12b-112">**InprocHandler**</span></span>](inprochandler.md)
</dt> </dl>

 

 




