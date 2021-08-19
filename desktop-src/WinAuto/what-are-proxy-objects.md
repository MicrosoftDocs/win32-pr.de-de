---
title: Was sind Proxyobjekte?
description: Ein Proxyobjekt fungiert als Vermittler zwischen dem Client und einem zugänglichen Objekt. Der Zweck des Proxyobjekts besteht in der Überwachung der Lebensdauer des barrierefreien Objekts und dem Weitergeleitet von Aufrufen an das barrierefreie Objekt nur, wenn es nicht zerstört wird.
ms.assetid: fdd5d44a-1797-47e6-8044-37dde926c18a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf3625bf048241e4ef28163ed3b8ca7916ccc35cccc12e7eac05b2b9b9c96d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052188"
---
# <a name="what-are-proxy-objects"></a>Was sind Proxyobjekte?

Ein *Proxyobjekt* fungiert als Vermittler zwischen dem Client und einem zugänglichen Objekt. Der Zweck des Proxyobjekts besteht in der Überwachung der Lebensdauer des barrierefreien Objekts und dem Weitergeleitet von Aufrufen an das barrierefreie Objekt nur, wenn es nicht zerstört wird.

Wenn ein Client eine [**IAccessible-Eigenschaft aufruft,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) um Informationen zu einem Objekt zu erhalten, muss das Proxyobjekt überprüfen, ob das barrierefreie Objekt weiterhin verfügbar ist. Wenn dies der Derklang ist, übergibt das Proxyobjekt die Clientanforderung an das barrierefreie Objekt. Wenn das barrierefreie Objekt zerstört wird (z. B. wenn ein Dialogfeld mit benutzerdefinierten Steuerelementen geschlossen wird), gibt das Proxyobjekt einen Fehler zurück. Um anzugeben, dass das Objekt zerstört wurde, wird empfohlen, dass Server den Fehlercode **CO \_ E \_ OBJNOTCONNECTED** zurückgeben, da dieser Fehler von Component Object Model (COM) zurückgegeben wird, nachdem ein Server [CoDisconnectObject aufruft.](/windows/win32/api/combaseapi/nf-combaseapi-codisconnectobject)

Das Proxyobjekt ist für den Client transparent. Wenn der Client [**AccessibleObjectFromEvent,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)oder [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)aufruft, erhält er einen Zeiger auf eine [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) zurück. Wenn der Client diesen Zeiger jedoch zum Aufrufen einer der **IAccessible-Eigenschaften** oder -Methoden verwendet, befindet sich der ausgeführte Code innerhalb des Proxyobjekts.

 

 