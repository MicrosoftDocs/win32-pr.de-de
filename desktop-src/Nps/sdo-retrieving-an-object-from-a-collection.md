---
title: Abrufen eines Objekts aus einer Sammlung
description: Abrufen eines Objekts aus einer Sammlung
ms.assetid: df7cbff5-2d09-4031-8f41-3f4eea51598f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe8d5bfcba8a1671c7824a4b1356e9c8e1dd7567
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516934"
---
# <a name="retrieving-an-object-from-a-collection"></a><span data-ttu-id="f2849-103">Abrufen eines Objekts aus einer Sammlung</span><span class="sxs-lookup"><span data-stu-id="f2849-103">Retrieving an Object from a Collection</span></span>

<span data-ttu-id="f2849-104">Der folgende Code Ruft die IP-Adresse eines Clients aus einer Sammlung von Clients ab.</span><span class="sxs-lookup"><span data-stu-id="f2849-104">The following code retrieves the IP address of a client from a collection of clients.</span></span> <span data-ttu-id="f2849-105">Die Variable "pclientscollection" verweist auf eine [**isdocollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) -Schnittstelle für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="f2849-105">The variable pClientsCollection points to an [**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) interface for the collection.</span></span> <span data-ttu-id="f2849-106">Informationen zum Abrufen des Sammlungs Objekts finden Sie unter [Abrufen einer](/windows/desktop/Nps/sdo-retrieving-a-collection) Auflistung.</span><span class="sxs-lookup"><span data-stu-id="f2849-106">See [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection) for information on how to retrieve the collection object.</span></span>


```C++
   HRESULT hr
   _variant_t vtClientName = L"Test Client";
   
   //
   // Get the client "Test Client" from the collection of clients
   //
   CComPtr<IDispatch> pFoundClientDispatch;
   hr = pClientsCollection->Item(&vtClientName, &pFoundClientDispatch);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pFoundClientSdo;
   hr = pFoundClientDispatch->QueryInterface(
      __uuidof(ISdo),
      (void **) &pFoundClientSdo
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Get the IP address of that client 
   //
   _variant_t vtAddress;
   hr = pFoundClientSdo->GetProperty(PROPERTY_CLIENT_ADDRESS ,&vtAddress);
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="related-topics"></a><span data-ttu-id="f2849-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2849-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2849-108">**Isdocollection:: Item**</span><span class="sxs-lookup"><span data-stu-id="f2849-108">**ISdoCollection::Item**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdocollection-item)
</dt> <dt>

[<span data-ttu-id="f2849-109">Abrufen einer Sammlung</span><span class="sxs-lookup"><span data-stu-id="f2849-109">Retrieving a Collection</span></span>](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[<span data-ttu-id="f2849-110">**SysAllocString**</span><span class="sxs-lookup"><span data-stu-id="f2849-110">**SysAllocString**</span></span>](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)
</dt> <dt>

[<span data-ttu-id="f2849-111">**SysFreeString**</span><span class="sxs-lookup"><span data-stu-id="f2849-111">**SysFreeString**</span></span>](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)
</dt> <dt>

[<span data-ttu-id="f2849-112">**Konfigur**</span><span class="sxs-lookup"><span data-stu-id="f2849-112">**VARIANT**</span></span>](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 