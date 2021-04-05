---
title: Proxystubclsid
description: Ordnet eine IID einer CLSID in 16-Bit-Proxy-DLLs zu.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- Proxystubclsid-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adfbe319903b2e278be342d169a2e523c952693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037367"
---
# <a name="proxystubclsid"></a><span data-ttu-id="2d6ac-104">Proxystubclsid</span><span class="sxs-lookup"><span data-stu-id="2d6ac-104">ProxyStubClsid</span></span>

<span data-ttu-id="2d6ac-105">Ordnet eine IID einer CLSID in 16-Bit-Proxy-DLLs zu.</span><span class="sxs-lookup"><span data-stu-id="2d6ac-105">Maps an IID to a CLSID in 16-bit proxy DLLs.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="2d6ac-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="2d6ac-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a><span data-ttu-id="2d6ac-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d6ac-107">Remarks</span></span>

<span data-ttu-id="2d6ac-108">Dies ist ein **reg \_ SZ** -Wert, der die CLSID für die IID angibt.</span><span class="sxs-lookup"><span data-stu-id="2d6ac-108">This is a **REG\_SZ** value that specifies the CLSID for the IID.</span></span>

<span data-ttu-id="2d6ac-109">Wenn Sie Schnittstellen hinzufügen, müssen Sie diesen Eintrag verwenden, um Sie zu registrieren (16-Bit-Systeme), damit OLE den entsprechenden remotingcode finden kann, um prozessübergreifende Kommunikation herzustellen.</span><span class="sxs-lookup"><span data-stu-id="2d6ac-109">If you add interfaces, you must use this entry to register them (16-bit systems) so that OLE can find the appropriate remoting code to establish interprocess communication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d6ac-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2d6ac-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d6ac-111">**Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2d6ac-111">**Interface**</span></span>](interface-key.md)
</dt> <dt>

[<span data-ttu-id="2d6ac-112">**ProxyStubClsid32**</span><span class="sxs-lookup"><span data-stu-id="2d6ac-112">**ProxyStubClsid32**</span></span>](proxystubclsid32.md)
</dt> </dl>

 

 




