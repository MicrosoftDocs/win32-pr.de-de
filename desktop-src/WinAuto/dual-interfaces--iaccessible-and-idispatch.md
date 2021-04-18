---
title: Duale Schnittstellen IAccessible und IDispatch
description: Server Entwickler müssen die IDispatch-Schnittstelle der Standard-Component Object Model (com) für Ihre barrierefreien Objekte bereitstellen.
ms.assetid: 043d6777-6f9a-4e93-aadc-9cbe9a9119c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bbe19e35a04414253dc8f22c4edbc19a041b27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340492"
---
# <a name="dual-interfaces-iaccessible-and-idispatch"></a><span data-ttu-id="aa03c-103">Duale Schnittstellen: IAccessible und IDispatch</span><span class="sxs-lookup"><span data-stu-id="aa03c-103">Dual Interfaces: IAccessible and IDispatch</span></span>

<span data-ttu-id="aa03c-104">Server Entwickler müssen die [**IDispatch**](idispatch-interface.md) -Schnittstelle der Standard-Component Object Model (com) für Ihre barrierefreien Objekte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="aa03c-104">Server developers must provide the standard Component Object Model (COM) interface [**IDispatch**](idispatch-interface.md) for their accessible objects.</span></span> <span data-ttu-id="aa03c-105">Die IDispatch-Schnittstelle ermöglicht es Client Anwendungen, die in Microsoft Visual Basic und verschiedenen Skriptsprachen geschrieben wurden, die von [**IAccessible verfügbar**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)gemachten Methoden und Eigenschaften zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="aa03c-105">The IDispatch interface allows client applications written in Microsoft Visual Basic and various scripting languages to use the methods and properties exposed by [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="aa03c-106">Da ein Barrierefreies Objekt entweder indirekt über [IDispatch:: Aufrufen]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) oder direkt mit **IAccessible** Zugriff auf ein Objekt bietet, wird es als duale Schnittstelle bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="aa03c-106">Because an accessible object provides access to an object either indirectly through [IDispatch::Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) or directly with **IAccessible**, it is said to have a dual interface.</span></span>

<span data-ttu-id="aa03c-107">Wenn C/C++-Clients einen IDispatch-Schnittstellen Zeiger zurückerhalten, können Clients [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) abrufen, um zu versuchen, den IDispatch-Schnittstellen Zeiger in einen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="aa03c-107">When C/C++ clients get back an IDispatch interface pointer, clients can call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to try converting the IDispatch interface pointer to an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span> <span data-ttu-id="aa03c-108">Um die **IAccessible** -Methoden indirekt aufzurufen, rufen C/C++-Clients IDispatch:: Aufrufen auf.</span><span class="sxs-lookup"><span data-stu-id="aa03c-108">To call the **IAccessible** methods indirectly, C/C++ clients call IDispatch::Invoke.</span></span> <span data-ttu-id="aa03c-109">Um die Leistung zu verbessern, müssen Sie die **IAccessible** -Methoden zur direkten Verwendung des-Objekts abrufen.</span><span class="sxs-lookup"><span data-stu-id="aa03c-109">For improved performance, call the **IAccessible** methods to use the object directly.</span></span>

<span data-ttu-id="aa03c-110">Eine Liste der dispatchids (DispIds), die **IDispatch** verwendet, um die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden und-Eigenschaften zu identifizieren, finden Sie in [Anhang C: IAccessible-DispIds](appendix-c--iaccessible-dispids.md).</span><span class="sxs-lookup"><span data-stu-id="aa03c-110">For a list of the dispatch IDs (DISPIDs) that **IDispatch** uses to identify the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties, see [Appendix C: IAccessible DISPIDs](appendix-c--iaccessible-dispids.md).</span></span>

> [!Note]  
> <span data-ttu-id="aa03c-111">Unter Version 2,0 und höher von Microsoft Active Accessibility müssen Server die Methoden von [**IDispatch**](idispatch-interface.md) nicht vollständig implementieren, aber \_ Sie können nach dem Initialisieren von out-Parametern einfach E notimpl zurückgeben, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="aa03c-111">Under version 2.0 and later of Microsoft Active Accessibility, servers do not have to fully implement the methods of [**IDispatch**](idispatch-interface.md) but can simply return E\_NOTIMPL after initializing any out parameters, as shown in the following example.</span></span>

 


```C++
HRESULT STDMETHODCALLTYPE AccServer::GetTypeInfoCount(UINT* pctinfo)
{
    *pctinfo = 0;
    return E_NOTIMPL;
};
```



 

 