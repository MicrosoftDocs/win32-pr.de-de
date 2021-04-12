---
title: Was sind Proxy Objekte?
description: Ein Proxy Objekt fungiert als Vermittler zwischen dem Client und einem barrierefreien Objekt. Das Proxy Objekt dient zum Überwachen der Lebensdauer des barrierefreien Objekts und zum Weiterleiten von Aufrufen an das barrierefreie Objekt nur, wenn es nicht zerstört wird.
ms.assetid: fdd5d44a-1797-47e6-8044-37dde926c18a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d54fb20d677f1a417d633242ddf40c704087f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316227"
---
# <a name="what-are-proxy-objects"></a>Was sind Proxy Objekte?

Ein *Proxy* Objekt fungiert als Vermittler zwischen dem Client und einem barrierefreien Objekt. Das Proxy Objekt dient zum Überwachen der Lebensdauer des barrierefreien Objekts und zum Weiterleiten von Aufrufen an das barrierefreie Objekt nur, wenn es nicht zerstört wird.

Wenn ein Client eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaft aufruft, um Informationen zu einem Objekt zu erhalten, muss das Proxy Objekt überprüfen, ob das barrierefreie Objekt weiterhin verfügbar ist. Wenn dies der Fall ist, übergibt das Proxy Objekt die Anforderung des Clients an das barrierefreie Objekt. Wenn das barrierefreie Objekt zerstört wird (z. b. Wenn ein Dialogfeld mit benutzerdefinierten Steuerelementen geschlossen wird), gibt das Proxy Objekt einen Fehler zurück. Um anzugeben, dass das Objekt zerstört wurde, wird empfohlen, dass Server den Fehlercode **Co \_ E \_ objnotconnected** zurückgeben, da dieser Fehler von Component Object Model (com) zurückgegeben wird, nachdem ein Server [CoDisconnectObject](/windows/win32/api/combaseapi/nf-combaseapi-codisconnectobject)aufgerufen hat.

Das Proxy Objekt ist für den Client transparent. Wenn der Client [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)oder [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)aufruft, empfängt er einen Zeiger auf eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle. Wenn der Client diesen Zeiger jedoch verwendet, um eine der Eigenschaften oder Methoden von **IAccessible** aufzurufen, wird der ausgeführte Code innerhalb des Proxy Objekts ausgeführt.

 

 