---
description: Die cokreateactivity-Funktion wird verwendet, um Batch Arbeit an das com+-System zu übermitteln. Dadurch können skriptbasierte Anwendungen eine Anwendungs weite com+-Dienst Konfiguration unterstützen.
ms.assetid: af734507-516c-43f1-9c5e-c77cde1b8008
title: Verwenden von COM+-Diensten über cokreateactivity
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b3296756b91d0f8ea29b1d67c11c78c431cfcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341156"
---
# <a name="using-com-services-through-cocreateactivity"></a>Verwenden von COM+-Diensten über cokreateactivity

Die [**cokreateactivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) -Funktion wird verwendet, um Batch Arbeit an das com+-System zu übermitteln. Dadurch können skriptbasierte Anwendungen eine Anwendungs weite com+-Dienst Konfiguration unterstützen.

Die gewünschten com+-Dienste werden über ein [**cserviceconfig**](cserviceconfig.md) -Objekt konfiguriert, das an die Funktion übergeben wird. Die-Funktion erstellt ein Aktivitäts Objekt und gibt die [**iserviceactivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) -Schnittstelle des Objekts zurück. Die Batch Verarbeitung kann entweder synchron oder asynchron übermittelt werden, indem die [**synchouscall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) -Methode oder die [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) -Methode von **iserviceactivity** verwendet wird. Ein Zeiger auf eine [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) -Schnittstelle wird an jede dieser Methoden übergeben, und die Batch Arbeit wird vom Entwickler in der [**OnCall-**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) Methode der **IServiceCall** -Schnittstelle implementiert.

## <a name="component-services-administrative-tool"></a>Verwaltungs Tool für Komponenten Dienste

Nicht anwendbar.

## <a name="visual-basic"></a>Visual Basic

Nicht anwendbar.

## <a name="cc"></a>C/C++

Das folgende Code Fragment veranschaulicht, wie COM+-Dienste über [**cokreateactivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)verwendet werden. Die Fehlerbehandlung wurde weggelassen, um die Komplexität gering zu halten. Dieses Code Fragment verwendet das [**cserviceconfig**](cserviceconfig.md) -Objekt, das in [Konfigurieren von COM+-Diensten mit cserviceconfig](configuring-com--services-with-cserviceconfig.md)erstellt und konfiguriert wurde.


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

[**Cokreateactivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[Konfigurieren von COM+-Diensten mit cserviceconfig](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[**Cserviceconfig**](cserviceconfig.md)
</dt> <dt>

[Verwenden von COM+-Diensten über coenterservicedomain und coleaveservicedomain](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

 



