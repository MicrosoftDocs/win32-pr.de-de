---
title: IDispatch-Schnittstelle und Barrierefreiheit
description: Die IDispatch-Schnittstelle wurde ursprünglich zur Unterstützung von Automation entwickelt.
ms.assetid: 5a95f002-4fd5-43d3-9b50-7b3f7790300a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710fb0bc8142dfa863967114d3841506c220b3c058db042b867607ffe56cd5e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052708"
---
# <a name="idispatch-interface-and-accessibility"></a>IDispatch-Schnittstelle und Barrierefreiheit

Die [**IDispatch-Schnittstelle**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) wurde ursprünglich zur Unterstützung von Automation entwickelt. Sie stellt einen Mechanismus für die späte Bindung zum Zugreifen auf und Abrufen von Informationen über die Methoden und Eigenschaften eines Objekts zur Verfügung. Zuvor mussten Serverentwickler sowohl die **IDispatch-** als auch [**die IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für ihre barrierefreien Objekte implementieren. Das heißt, sie mussten eine [duale Schnittstelle bereitstellen.](dual-interfaces--iaccessible-and-idispatch.md) Mit Microsoft Active Accessibility 2.0 können Server **E \_ NOTIMPL** von **IDispatch-Methoden** zurückgeben, und Microsoft Active Accessibility implementiert die **IAccessible-Schnittstelle** für sie.

Zusätzlich zu den von [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)geerbten Methoden müssen Serverentwickler die folgenden Methoden innerhalb der Klassendefinition jedes verfügbar gemachten Objekts implementieren:

-   [**GetTypeInfoCount gibt**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) die Anzahl der Typbeschreibungen für das Objekt zurück. Für Objekte, die [**IDispatch unterstützen,**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)ist die Anzahl der Typinformationen immer 1.
-   [**GetTypeInfo**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfo) ruft eine Beschreibung der programmierbaren Schnittstelle des Objekts ab.
-   [**GetIDsOfNames ordnet**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) den Namen einer Methode oder Eigenschaft einer **DISPID** zu, die später zum Aufrufen der Methode oder Eigenschaft verwendet wird.
-   [**Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) ruft eine der Methoden des Objekts auf oder ruft eine seiner Eigenschaften ab oder legt sie fest.

 

 