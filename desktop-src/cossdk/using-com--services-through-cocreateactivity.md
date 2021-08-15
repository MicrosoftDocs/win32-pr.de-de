---
description: Die CoCreateActivity-Funktion wird verwendet, um Batcharbeit an das COM+-System zu übermitteln. Es ermöglicht skriptbasierten Anwendungen die Unterstützung einer anwendungsweiten COM+-Dienstkonfiguration.
ms.assetid: af734507-516c-43f1-9c5e-c77cde1b8008
title: Verwenden von COM+-Diensten über CoCreateActivity
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b5452c99fa431e7c1927646eec7ad9b5e5fa930f3ba7d0bf242df7690325db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128662"
---
# <a name="using-com-services-through-cocreateactivity"></a>Verwenden von COM+-Diensten über CoCreateActivity

Die [**CoCreateActivity-Funktion**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) wird verwendet, um Batcharbeit an das COM+-System zu übermitteln. Es ermöglicht skriptbasierten Anwendungen die Unterstützung einer anwendungsweiten COM+-Dienstkonfiguration.

Die gewünschten COM+-Dienste werden über ein [**CServiceConfig-Objekt**](cserviceconfig.md) konfiguriert, das an die Funktion übergeben wird. Die Funktion erstellt ein Aktivitätsobjekt und gibt die [**IServiceActivity-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) dieses Objekts zurück. Die Batchverarbeitung kann entweder synchron oder asynchron übermittelt werden, indem die [**SynchronousCall-**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) bzw. [**AsynchronousCall-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) von **IServiceActivity** verwendet wird. Ein Zeiger auf eine [**IServiceCall-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) wird an jede dieser Methoden übergeben, und die Batchverarbeitung wird vom Entwickler in der [**OnCall-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) der **IServiceCall-Schnittstelle** implementiert.

## <a name="component-services-administrative-tool"></a>Verwaltungstool für Komponentendienste

Nicht anwendbar.

## <a name="visual-basic"></a>Visual Basic

Nicht anwendbar.

## <a name="cc"></a>C/C++

Das folgende Codefragment veranschaulicht die Verwendung von COM+-Diensten über [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity). Die Fehlerbehandlung wurde weggelassen, um die Komplexität gering zu halten. Dieses Codefragment verwendet das [**CServiceConfig-Objekt,**](cserviceconfig.md) das in Configuring COM+ Services with CServiceConfig (Konfigurieren von [COM+-Diensten mit CServiceConfig) erstellt und konfiguriert wurde.](configuring-com--services-with-cserviceconfig.md)


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER,
//   IID_IUnknown, (void**)&pUnknownCSC);

// Create the activity for our services.
HRESULT hr = CoCreateActivity(pUnknownCSC, IID_IServiceActivity, (void**)&pActivity);
if (FAILED(hr)) throw(hr);

// Do the batch work synchronously.
// The batch work is implemented in pServiceCall->OnCall().
hr = pActivity->SynchronousCall(pServiceCall);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[Konfigurieren von COM+-Diensten mit CServiceConfig](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[**CServiceConfig**](cserviceconfig.md)
</dt> <dt>

[Verwenden von COM+-Diensten über CoEnterServiceDomain und CoLeaveServiceDomain](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

 



