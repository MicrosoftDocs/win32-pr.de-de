---
title: Abrufen einer Dienst-SDO
description: Abrufen einer Dienst-SDO
ms.assetid: bac95c42-8f7e-4011-960c-8f18b4b7c088
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51f1ec3f8537cbf6e9a7be82f8152bc764a263093fe0ebeee46ed1499abfd346
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618956"
---
# <a name="retrieving-a-service-sdo"></a>Abrufen einer Dienst-SDO

> [!Note]  
> Der Internetauthentifizierungsdienst (INTERNET Authentication Service, IAS) wurde ab Windows Server 2008 in Netzwerkrichtlinienserver (Network Policy Server, NPS) umbenannt.

 

Der folgende Code ruft ein Serverdatenobjekt (SDO) für den Netzwerkrichtlinienserver ab.


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



## <a name="remarks"></a>Hinweise

Sie müssen an einen Computer [anfügen,](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) bevor Sie eine der [**ISdoMachine-Methoden**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) aufrufen können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anfügen an einen SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo)
</dt> <dt>

[**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol)
</dt> </dl>

 

 