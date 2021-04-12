---
title: Abrufen eines SDO-diensdo
description: Abrufen eines SDO-diensdo
ms.assetid: bac95c42-8f7e-4011-960c-8f18b4b7c088
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afcea1885e0ed714587e99bc7c2dcd92f2fea422
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209289"
---
# <a name="retrieving-a-service-sdo"></a><span data-ttu-id="99ce7-103">Abrufen eines SDO-diensdo</span><span class="sxs-lookup"><span data-stu-id="99ce7-103">Retrieving a Service SDO</span></span>

> [!Note]  
> <span data-ttu-id="99ce7-104">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="99ce7-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

<span data-ttu-id="99ce7-105">Mit dem folgenden Code wird ein Server Datenobjekt (SDO) für den Netzwerk Richtlinien Server abgerufen.</span><span class="sxs-lookup"><span data-stu-id="99ce7-105">The following code retrieves a Server Data Object (SDO) for the Network Policy Server .</span></span>


```C++
   HRESULT hr;
   CComPtr<IUnknown> pServiceUnknown;
   _bstr_t bstrServiceName = L"IAS";

   hr = pSdoMachine->GetServiceSDO(
      DATA_STORE_LOCAL,
      bstrServiceName,
      (IUnknown**) &pServiceUnknown
   );
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdoServiceControl>  pSdoServiceControl;
   hr = pServiceUnknown->QueryInterface(
      __uuidof(ISdoServiceControl),
      (void**) &pSdoServiceControl
   );
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="remarks"></a><span data-ttu-id="99ce7-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99ce7-106">Remarks</span></span>

<span data-ttu-id="99ce7-107">Sie müssen an einen Computer [Anfügen](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) , bevor Sie eine der [**isdomachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) -Methoden ausführen können.</span><span class="sxs-lookup"><span data-stu-id="99ce7-107">You must [attach](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) to a computer before you can call any of the [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99ce7-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="99ce7-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99ce7-109">Anfügen an einen SDO-Enabled Computer</span><span class="sxs-lookup"><span data-stu-id="99ce7-109">Attaching to an SDO-Enabled Computer</span></span>](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[<span data-ttu-id="99ce7-110">**Isdomachine:: getservicesdo**</span><span class="sxs-lookup"><span data-stu-id="99ce7-110">**ISdoMachine::GetServiceSDO**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo)
</dt> <dt>

[<span data-ttu-id="99ce7-111">**Isdoservicecontrol**</span><span class="sxs-lookup"><span data-stu-id="99ce7-111">**ISdoServiceControl**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol)
</dt> </dl>

 

 