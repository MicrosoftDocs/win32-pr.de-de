---
title: ProxyStubClsid32
description: Ordnet eine IID einer CLSID in 32-Bit-Proxy-DLLs zu.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- ProxyStubClsid32 Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d1d70ad2deb4f747ecf57fd12f0707ac8b2b9d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316556"
---
# <a name="proxystubclsid32"></a><span data-ttu-id="59b7f-104">ProxyStubClsid32</span><span class="sxs-lookup"><span data-stu-id="59b7f-104">ProxyStubClsid32</span></span>

<span data-ttu-id="59b7f-105">Ordnet eine IID einer CLSID in 32-Bit-Proxy-DLLs zu.</span><span class="sxs-lookup"><span data-stu-id="59b7f-105">Maps an IID to a CLSID in 32-bit proxy DLLs.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="59b7f-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="59b7f-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a><span data-ttu-id="59b7f-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59b7f-107">Remarks</span></span>

<span data-ttu-id="59b7f-108">Dies ist ein **reg \_ SZ** -Wert, der die CLSID für die IID angibt.</span><span class="sxs-lookup"><span data-stu-id="59b7f-108">This is a **REG\_SZ** value that specifies the CLSID for the IID.</span></span>

<span data-ttu-id="59b7f-109">Dies ist ein erforderlicher Eintrag, da die Zuordnung zwischen IID und CLSID für 16-Bit-und 32-Bit-Schnittstellen unterschiedlich sein kann.</span><span class="sxs-lookup"><span data-stu-id="59b7f-109">This is a required entry since the IID-to-CLSID mapping may be different for 16-bit and 32-bit interfaces.</span></span> <span data-ttu-id="59b7f-110">Die Zuordnung zwischen IID und CLSID hängt davon ab, wie die Schnittstellen Proxys in einen Satz von Proxy-DLLs gepackt werden.</span><span class="sxs-lookup"><span data-stu-id="59b7f-110">The IID-to-CLSID mapping depends on the way the interface proxies are packaged into a set of proxy DLLs.</span></span>

<span data-ttu-id="59b7f-111">Wenn Sie Schnittstellen hinzufügen, müssen Sie diesen Eintrag verwenden, um Sie zu registrieren (32-Bit-Systeme), damit OLE den entsprechenden remotingcode finden kann, um prozessübergreifende Kommunikation herzustellen.</span><span class="sxs-lookup"><span data-stu-id="59b7f-111">If you add interfaces, you must use this entry to register them (32-bit systems) so that OLE can find the appropriate remoting code to establish interprocess communication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59b7f-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="59b7f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59b7f-113">**Von IMarshal**</span><span class="sxs-lookup"><span data-stu-id="59b7f-113">**IMarshal**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[<span data-ttu-id="59b7f-114">**Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="59b7f-114">**Interface**</span></span>](interface-key.md)
</dt> <dt>

[<span data-ttu-id="59b7f-115">**Proxystubclsid**</span><span class="sxs-lookup"><span data-stu-id="59b7f-115">**ProxyStubClsid**</span></span>](proxystubclsid.md)
</dt> </dl>

 

 