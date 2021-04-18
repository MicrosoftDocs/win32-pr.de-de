---
title: Auflisten von Objekten in einer Auflistung
description: Auflisten von Objekten in einer Auflistung
ms.assetid: 664e4d99-48ed-4948-b816-e92ad1ca3ece
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f3c543e01f3c8f154628c6e204aff53c6ad210
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338290"
---
# <a name="enumerating-objects-in-a-collection"></a><span data-ttu-id="b61e7-103">Auflisten von Objekten in einer Auflistung</span><span class="sxs-lookup"><span data-stu-id="b61e7-103">Enumerating Objects in a Collection</span></span>

> [!Note]  
> <span data-ttu-id="b61e7-104">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="b61e7-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="b61e7-105">Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS.</span><span class="sxs-lookup"><span data-stu-id="b61e7-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="b61e7-106">Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="b61e7-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="b61e7-107">Der folgende Code listet die Protokolle in der NPS-Protokoll Sammlung auf.</span><span class="sxs-lookup"><span data-stu-id="b61e7-107">The following code enumerates the protocols in the NPS protocols collection.</span></span>


```C++
   HRESULT hr;

   //
   // Retrieve the protocols collection object
   //
   _variant_t vtIASProtocolsCollection;
   hr = pSdo->GetProperty(
      PROPERTY_IAS_PROTOCOLS_COLLECTION,
      &vtIASProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the ISdoCollection interface 
   // for the object.
   //
   CComPtr<ISdoCollection> pIASProtocolsCollection;
   hr = vtIASProtocolsCollection.pdispVal->QueryInterface(
      __uuidof(ISdoCollection), 
      (void **) &pIASProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the enumeration interface, IEnumVARIANT
   //
   CComPtr<IUnknown> pUnknownProtocol;
   hr = pIASProtocolsCollection->get__NewEnum(&pUnknownProtocol);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<IEnumVARIANT> pEnumProtocols;
   hr = pUnknownProtocol->QueryInterface(
      __uuidof(IEnumVARIANT), 
      (void **) &pEnumProtocols
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the first protocol from the collection
   //
   DWORD      dwRetrieved = 1;
   _variant_t vtProtocol;
   hr = pEnumProtocols->Next(1, &vtProtocol, &dwRetrieved);
   if (FAILED(hr))
   {
      return hr;
   }

   while (hr != S_FALSE) {
      // 
      // Retrieve the name of the protocol
      //
      CComPtr<ISdo> pLocalSdo;
      hr = vtProtocol.pdispVal->QueryInterface(
         __uuidof(ISdo), 
         (void**)&pLocalSdo
      );
      if (FAILED(hr))
      {
         return hr;
      }

      _variant_t vtName;
      hr = pLocalSdo->GetProperty(PROPERTY_SDO_NAME, &vtName);
      if (FAILED(hr))
      {
         return hr;
      }

      vtProtocol.Clear();
      vtName.Clear();

      //
      // Retrieve the next protocol from the collection
      //
      dwRetrieved = 1;
      hr = pEnumProtocols->Next(1, &vtProtocol, &dwRetrieved);
      if (FAILED(hr))
      {
         return hr;
      }
   }

```



## <a name="remarks"></a><span data-ttu-id="b61e7-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b61e7-108">Remarks</span></span>

<span data-ttu-id="b61e7-109">Die vtname-und vtprotocol-Variablen sind vom Typ [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span><span class="sxs-lookup"><span data-stu-id="b61e7-109">The vtName and vtProtocol variables are of type [\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span></span> <span data-ttu-id="b61e7-110">Ein [ \_ Variant- \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)) -Objekt kapselt bzw. schließt den **Variant** -Datentyp ein.</span><span class="sxs-lookup"><span data-stu-id="b61e7-110">A [\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)) object encapsulates, or encloses, the **VARIANT** data type.</span></span> <span data-ttu-id="b61e7-111">Die-Klasse verwaltet die Zuordnung und Aufhebung der Zuordnung von Ressourcen und führt Funktionsaufrufe an [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) und [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) entsprechend aus.</span><span class="sxs-lookup"><span data-stu-id="b61e7-111">The class manages resource allocation and deallocation, and makes function calls to [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b61e7-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b61e7-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b61e7-113">[\_Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="b61e7-113">[\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span></span>
</dt> <dt>

[<span data-ttu-id="b61e7-114">Hinzufügen eines Clients</span><span class="sxs-lookup"><span data-stu-id="b61e7-114">Adding a Client</span></span>](/windows/desktop/Nps/sdo-adding-a-client)
</dt> <dt>

[<span data-ttu-id="b61e7-115">**Iascommonproperties**</span><span class="sxs-lookup"><span data-stu-id="b61e7-115">**IASCOMMONPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties)
</dt> <dt>

[<span data-ttu-id="b61e7-116">**IEnumVARIANT**</span><span class="sxs-lookup"><span data-stu-id="b61e7-116">**IEnumVARIANT**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)
</dt> <dt>

[<span data-ttu-id="b61e7-117">**Isdo:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="b61e7-117">**ISdo::GetProperty**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[<span data-ttu-id="b61e7-118">Abrufen eines SDO-diensdo</span><span class="sxs-lookup"><span data-stu-id="b61e7-118">Retrieving a Service SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[<span data-ttu-id="b61e7-119">**VariantClear**</span><span class="sxs-lookup"><span data-stu-id="b61e7-119">**VariantClear**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[<span data-ttu-id="b61e7-120">**Variantit**</span><span class="sxs-lookup"><span data-stu-id="b61e7-120">**VariantInit**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[<span data-ttu-id="b61e7-121">**Konfigur**</span><span class="sxs-lookup"><span data-stu-id="b61e7-121">**VARIANT**</span></span>](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 