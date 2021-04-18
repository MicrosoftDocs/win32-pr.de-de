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
# <a name="dual-interfaces-iaccessible-and-idispatch"></a>Duale Schnittstellen: IAccessible und IDispatch

Server Entwickler müssen die [**IDispatch**](idispatch-interface.md) -Schnittstelle der Standard-Component Object Model (com) für Ihre barrierefreien Objekte bereitstellen. Die IDispatch-Schnittstelle ermöglicht es Client Anwendungen, die in Microsoft Visual Basic und verschiedenen Skriptsprachen geschrieben wurden, die von [**IAccessible verfügbar**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)gemachten Methoden und Eigenschaften zu verwenden. Da ein Barrierefreies Objekt entweder indirekt über [IDispatch:: Aufrufen]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) oder direkt mit **IAccessible** Zugriff auf ein Objekt bietet, wird es als duale Schnittstelle bezeichnet.

Wenn C/C++-Clients einen IDispatch-Schnittstellen Zeiger zurückerhalten, können Clients [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) abrufen, um zu versuchen, den IDispatch-Schnittstellen Zeiger in einen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger umzuwandeln. Um die **IAccessible** -Methoden indirekt aufzurufen, rufen C/C++-Clients IDispatch:: Aufrufen auf. Um die Leistung zu verbessern, müssen Sie die **IAccessible** -Methoden zur direkten Verwendung des-Objekts abrufen.

Eine Liste der dispatchids (DispIds), die **IDispatch** verwendet, um die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden und-Eigenschaften zu identifizieren, finden Sie in [Anhang C: IAccessible-DispIds](appendix-c--iaccessible-dispids.md).

> [!Note]  
> Unter Version 2,0 und höher von Microsoft Active Accessibility müssen Server die Methoden von [**IDispatch**](idispatch-interface.md) nicht vollständig implementieren, aber \_ Sie können nach dem Initialisieren von out-Parametern einfach E notimpl zurückgeben, wie im folgenden Beispiel gezeigt.

 


```C++
HRESULT STDMETHODCALLTYPE AccServer::GetTypeInfoCount(UINT* pctinfo)
{
    *pctinfo = 0;
    return E_NOTIMPL;
};
```



 

 