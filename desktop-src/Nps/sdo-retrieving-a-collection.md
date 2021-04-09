---
title: Abrufen einer Sammlung
description: Abrufen einer Sammlung
ms.assetid: b9090ad5-564c-4f48-b7bd-24617d582d2e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517acfa320069f9c94ee291e9215459d27ba25ad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948921"
---
# <a name="retrieving-a-collection"></a><span data-ttu-id="62cb3-103">Abrufen einer Sammlung</span><span class="sxs-lookup"><span data-stu-id="62cb3-103">Retrieving a Collection</span></span>

> [!Note]  
> <span data-ttu-id="62cb3-104">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="62cb3-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="62cb3-105">Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS.</span><span class="sxs-lookup"><span data-stu-id="62cb3-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="62cb3-106">Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="62cb3-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="62cb3-107">Mit dem folgenden Code wird die-Client Sammlung für den Netzwerk Richtlinien Server abgerufen.</span><span class="sxs-lookup"><span data-stu-id="62cb3-107">The following code retrieves the clients collection for the Network Policy Server.</span></span>


```C++
// Retrieve the clients collection 
   HRESULT hr;
   CComPtr<ISdo>  pSdo;
   hr = pSdoServiceControl->QueryInterface(
      __uuidof(ISdo),
      (void**) &pSdo
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // First Retrieve the protocols collection
   //
   _variant_t  vtProtocolsCollection;
   hr = pSdo->GetProperty(
      PROPERTY_IAS_PROTOCOLS_COLLECTION,
      &vtProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Get the ISdoCollection interface 
   // for the object.
   //
   CComPtr<ISdoCollection>  pProtocolsCollection;
   hr = vtProtocolsCollection.pdispVal->QueryInterface(
      __uuidof(ISdoCollection), 
      (void **) &pProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Then retrieve the RADIUS protocol
   //
   CComPtr<IDispatch> pRadiusDispatch;
   _variant_t  vtProtocolName = L"Microsoft Radius Protocol";
   hr = pProtocolsCollection->Item(&vtProtocolName, &pRadiusDispatch);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pRadiusSdo;
   hr = pRadiusDispatch->QueryInterface(      
      __uuidof(ISdo), 
      (void **) &pRadiusSdo
   );

   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Then retrieve the clients collection
   //
   _variant_t  vtClientsCollection;
   hr = pRadiusSdo->GetProperty(PROPERTY_RADIUS_CLIENTS_COLLECTION, &vtClientsCollection);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdoCollection> pClientsCollection;
   hr = vtClientsCollection.pdispVal->QueryInterface(      
      __uuidof(ISdoCollection), 
      (void **) &pClientsCollection
   );

   if (FAILED(hr))
   {
      return hr;
   }

```



## <a name="remarks"></a><span data-ttu-id="62cb3-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62cb3-108">Remarks</span></span>

<span data-ttu-id="62cb3-109">Die psdoservicecontrol-Variable enthält einen Zeiger auf ein Server Datenobjekt für NPS.</span><span class="sxs-lookup"><span data-stu-id="62cb3-109">The pSdoServiceControl variable contains a pointer to a Server Data Object for NPS.</span></span> <span data-ttu-id="62cb3-110">Weitere Informationen finden Sie im Thema [Abrufen eines SDO-diensdo](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).</span><span class="sxs-lookup"><span data-stu-id="62cb3-110">For more information, see the topic [Retrieving a Service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).</span></span>

<span data-ttu-id="62cb3-111">Die vtclientscollection-Variable ist vom Typ [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span><span class="sxs-lookup"><span data-stu-id="62cb3-111">The vtClientsCollection variable is of type [\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span></span> <span data-ttu-id="62cb3-112">Ein \_ Variant- \_ t-Objekt kapselt bzw. schließt den [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Datentyp ein.</span><span class="sxs-lookup"><span data-stu-id="62cb3-112">A \_variant\_t object encapsulates, or encloses, the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) data type.</span></span> <span data-ttu-id="62cb3-113">Die-Klasse verwaltet die Zuordnung und Aufhebung der Zuordnung von Ressourcen und führt Funktionsaufrufe an [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) und [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) entsprechend aus.</span><span class="sxs-lookup"><span data-stu-id="62cb3-113">The class manages resource allocation and deallocation, and makes function calls to [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) as appropriate.</span></span>

<span data-ttu-id="62cb3-114">Nach dem Aufrufen von "psdo->GetProperty ()" gibt die vtprotocolscollection-Variable ein Objekt an.</span><span class="sxs-lookup"><span data-stu-id="62cb3-114">After the call to "pSdo->GetProperty()", the vtProtocolsCollection variable specifies an object.</span></span> <span data-ttu-id="62cb3-115">Der **pdispVal** -Member von vtprotocolscollection enthält einen Zeiger auf die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="62cb3-115">The **pdispVal** member of vtProtocolsCollection contains a pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface for the object.</span></span>

<span data-ttu-id="62cb3-116">Der obige Beispielcode kann angepasst werden, um andere NPS-Auflistungen abzurufen, z. b. die NPS-Anforderungs Handler-Auflistungen.</span><span class="sxs-lookup"><span data-stu-id="62cb3-116">The above sample code can be adapted to retrieve other NPS collections, for example the NPS Request Handlers collections.</span></span> <span data-ttu-id="62cb3-117">Der [**iasproperties**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) -Enumerationstyp listet Werte auf, die den verfügbaren NPS-Auflistungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62cb3-117">The [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) enumeration type enumerated values that correspond to the available NPS collections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62cb3-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="62cb3-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="62cb3-119">[\_Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="62cb3-119">[\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span></span>
</dt> <dt>

[<span data-ttu-id="62cb3-120">**Iasproperties**</span><span class="sxs-lookup"><span data-stu-id="62cb3-120">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[<span data-ttu-id="62cb3-121">**Isdo:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="62cb3-121">**ISdo::GetProperty**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[<span data-ttu-id="62cb3-122">**Isdocollection**</span><span class="sxs-lookup"><span data-stu-id="62cb3-122">**ISdoCollection**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[<span data-ttu-id="62cb3-123">Abrufen eines SDO-diensdo</span><span class="sxs-lookup"><span data-stu-id="62cb3-123">Retrieving a Service SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[<span data-ttu-id="62cb3-124">**VariantClear**</span><span class="sxs-lookup"><span data-stu-id="62cb3-124">**VariantClear**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[<span data-ttu-id="62cb3-125">**Variantit**</span><span class="sxs-lookup"><span data-stu-id="62cb3-125">**VariantInit**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[<span data-ttu-id="62cb3-126">**Konfigur**</span><span class="sxs-lookup"><span data-stu-id="62cb3-126">**VARIANT**</span></span>](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 