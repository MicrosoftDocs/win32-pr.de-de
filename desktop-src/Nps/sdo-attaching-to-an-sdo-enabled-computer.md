---
title: Anfügen an einen SDO-Enabled Computer
description: Anfügen an einen SDO-Enabled Computer
ms.assetid: 434e2e0c-075e-48a9-9617-bbe75716380d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729d8c5609691f1d51598701953c795225c08e4b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390392"
---
# <a name="attaching-to-an-sdo-enabled-computer"></a>Anfügen an einen SDO-Enabled Computer

Der folgende Code wird als SDO-Computer an den lokalen Computer angefügt.


```C++
   HRESULT  hr;
   CComPtr<ISdoMachine> pSdoMachine;
   CLSID    clsid;

   hr = CLSIDFromProgID(TEXT("IAS.SdoMachine"), &clsid);
   if (FAILED(hr))
   {
      return hr;
   }

   hr = CoCreateInstance(
      clsid,
      NULL,
      CLSCTX_INPROC_SERVER,
      __uuidof(ISdoMachine),
      (void**)&pSdoMachine
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Pass NULL to specify local computer.
   //
   hr = pSdoMachine->Attach(NULL); 
   if (FAILED(hr))
   {
      return hr;
   }

```



Das Anfügen an einen Computer als SDO-Computer ist der erste Schritt bei der Verwaltung des Computers über SDO.

Weitere Informationen finden Sie unter [**isdomachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine), [**isdomachine:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach).

 

 