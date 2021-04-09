---
title: Abrufen eines Benutzers (SDO)
description: Abrufen eines Benutzers (SDO)
ms.assetid: 440628f8-081b-4e7f-bdb2-760ff9bd0d77
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c1d6320398afb4eed22f72f0c5e12495010323
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948920"
---
# <a name="retrieving-a-user-sdo"></a><span data-ttu-id="3d19e-103">Abrufen eines Benutzers (SDO)</span><span class="sxs-lookup"><span data-stu-id="3d19e-103">Retrieving a User SDO</span></span>

<span data-ttu-id="3d19e-104">Mit dem folgenden Code wird ein Server Datenobjekt (SDO) für den Administrator abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3d19e-104">The following code retrieves a Server Data Object (SDO) for the Administrator.</span></span>


```C++
   HRESULT  hr;
   _bstr_t bstrUserName = L"Administrator";
   CComPtr<IUnknown> pUserUnknown;

   hr = pSdoMachine->GetUserSDO(
      DATA_STORE_LOCAL,
      bstrUserName,
      (IUnknown**) &pUserUnknown
   );
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pUserSDO;
   hr = pUserUnknown->QueryInterface(
      __uuidof(ISdo),
      (void**) &pUserSDO
   );
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="related-topics"></a><span data-ttu-id="3d19e-105">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3d19e-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d19e-106">Anfügen an einen SDO-Enabled Computer</span><span class="sxs-lookup"><span data-stu-id="3d19e-106">Attaching to an SDO-Enabled Computer</span></span>](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[<span data-ttu-id="3d19e-107">**Isdo**</span><span class="sxs-lookup"><span data-stu-id="3d19e-107">**ISdo**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[<span data-ttu-id="3d19e-108">**Isdomachine**</span><span class="sxs-lookup"><span data-stu-id="3d19e-108">**ISdoMachine**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdomachine)
</dt> <dt>

[<span data-ttu-id="3d19e-109">**Isdomachine:: getusersdo**</span><span class="sxs-lookup"><span data-stu-id="3d19e-109">**ISdoMachine::GetUserSDO**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo)
</dt> <dt>

[<span data-ttu-id="3d19e-110">**SysAllocString**</span><span class="sxs-lookup"><span data-stu-id="3d19e-110">**SysAllocString**</span></span>](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)
</dt> <dt>

[<span data-ttu-id="3d19e-111">**SysFreeString**</span><span class="sxs-lookup"><span data-stu-id="3d19e-111">**SysFreeString**</span></span>](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)
</dt> </dl>

 

 