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
# <a name="retrieving-a-collection"></a>Abrufen einer Sammlung

> [!Note]  
> Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

Mit dem folgenden Code wird die-Client Sammlung für den Netzwerk Richtlinien Server abgerufen.


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



## <a name="remarks"></a>Bemerkungen

Die psdoservicecontrol-Variable enthält einen Zeiger auf ein Server Datenobjekt für NPS. Weitere Informationen finden Sie im Thema [Abrufen eines SDO-diensdo](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).

Die vtclientscollection-Variable ist vom Typ [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)). Ein \_ Variant- \_ t-Objekt kapselt bzw. schließt den [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Datentyp ein. Die-Klasse verwaltet die Zuordnung und Aufhebung der Zuordnung von Ressourcen und führt Funktionsaufrufe an [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) und [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) entsprechend aus.

Nach dem Aufrufen von "psdo->GetProperty ()" gibt die vtprotocolscollection-Variable ein Objekt an. Der **pdispVal** -Member von vtprotocolscollection enthält einen Zeiger auf die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle für das Objekt.

Der obige Beispielcode kann angepasst werden, um andere NPS-Auflistungen abzurufen, z. b. die NPS-Anforderungs Handler-Auflistungen. Der [**iasproperties**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) -Enumerationstyp listet Werte auf, die den verfügbaren NPS-Auflistungen entsprechen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[\_Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))
</dt> <dt>

[**Iasproperties**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[**Isdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[**Isdocollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[Abrufen eines SDO-diensdo](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[**Variantit**](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[**Konfigur**](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 