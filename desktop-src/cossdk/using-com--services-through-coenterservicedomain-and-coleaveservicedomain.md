---
description: Verwenden von COM+-Diensten über coenterservicedomain und coleaveservicedomain
ms.assetid: 763fb01e-5daf-4e9b-8ef1-9ae79c0a84cc
title: Verwenden von COM+-Diensten über coenterservicedomain und coleaveservicedomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d87931628e177374dd07b40e9917a56c168a81
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127133"
---
# <a name="using-com-services-through-coenterservicedomain-and-coleaveservicedomain"></a>Verwenden von COM+-Diensten über coenterservicedomain und coleaveservicedomain

[**Coenterservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) und [**coleaveservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) werden zusammen verwendet, um einen Code Bereich zu umschließen, der in einem eigenen Kontext ausgeführt wird und com+-Dienste verwenden kann, ohne dass COM+-Komponenten erforderlich sind. Die com+-Dienste, die in diesem Kontext verwendet werden, werden über das [**cserviceconfig**](cserviceconfig.md) -Objekt konfiguriert, das an **coenterservicedomain** übergeben wird. Der Code, der von **coenterservicedomain** und **coleaveservicedomain** umgeben ist, verhält sich so, als ob es sich um eine Methode handelt, die für ein in diesem Kontext erstelltes Objekt aufgerufen wird.

Eine Skript Anwendung kann dieses Funktions paar verwenden, um Laufzeitunterstützung für COM+-Dienste ohne Komponenten bereitzustellen. Beispielsweise kann eine Skript Anwendung so entwickelt werden, dass Sie Tags bereitstellt, mit denen die Skript Schreiber eine Dienst Domäne innerhalb des Skripts eingeben und verlassen können. Wenn die Skript-Engine das Skript verarbeitet und auf die Tags stößt, kann es [**coenterservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) mit einem vorkonfigurierten [**cserviceconfig**](cserviceconfig.md) -Objekt anrufen, den erforderlichen Code ausführen und dann [**coleaveservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)aufzurufen.

## <a name="component-services-administrative-tool"></a>Verwaltungs Tool für Komponenten Dienste

Nicht anwendbar.

## <a name="visual-basic"></a>Visual Basic

Nicht anwendbar.

## <a name="cc"></a>C/C++

Das folgende Code Fragment veranschaulicht, wie COM+-Dienste zwischen Aufrufen von [**coenterservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) und [**coleaveservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)verwendet werden. Die Fehlerbehandlung wurde weggelassen, um die Komplexität gering zu halten. Dieses Code Fragment verwendet das [**cserviceconfig**](cserviceconfig.md) -Objekt, das in [Konfigurieren von COM+-Diensten mit cserviceconfig](configuring-com--services-with-cserviceconfig.md)erstellt und konfiguriert wurde.


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
//   IID_IUnknown, (void**)&pUnknownCSC);

// Enter the Service Domain.
HRESULT hr = CoEnterServiceDomain(pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Do the work that uses COM+ services here.
//DoMyWork();

// Leave the Service Domain.
CoLeaveServiceDomain(NULL);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Coenterservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[**Coleaveservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[Konfigurieren von COM+-Diensten mit cserviceconfig](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[**Cserviceconfig**](cserviceconfig.md)
</dt> <dt>

[Verwenden von COM+-Diensten über cokreateactivity](using-com--services-through-cocreateactivity.md)
</dt> </dl>

 

 



