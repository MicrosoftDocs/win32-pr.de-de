---
title: IDispatch-Schnittstelle und Barrierefreiheit
description: Die IDispatch-Schnittstelle wurde anfänglich zur Unterstützung der Automatisierung entworfen.
ms.assetid: 5a95f002-4fd5-43d3-9b50-7b3f7790300a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641ca3e4cc18b96441aefbbc46231e3f7753a94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340712"
---
# <a name="idispatch-interface-and-accessibility"></a>IDispatch-Schnittstelle und Barrierefreiheit

Die [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) -Schnittstelle wurde anfänglich zur Unterstützung der Automatisierung entworfen. Sie bietet einen Mechanismus für die späte Bindung, um auf Informationen über die Methoden und Eigenschaften eines Objekts zuzugreifen und diese abzurufen. Zuvor mussten Server Entwickler sowohl die **IDispatch** -Schnittstelle als auch die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle für Ihre zugänglichen Objekte implementieren. Das heißt, Sie mussten eine [duale Schnittstelle](dual-interfaces--iaccessible-and-idispatch.md)bereitstellen. Mit Microsoft Active Accessibility 2,0 können Server **E \_ notimpl** von **IDispatch** -Methoden zurückgeben, und Microsoft Active Accessibility implementiert die **IAccessible** -Schnittstelle für Sie.

Zusätzlich zu den von [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)geerbten Methoden müssen Server Entwickler die folgenden Methoden in der Klassendefinition jedes Objekts implementieren, das verfügbar gemacht wird:

-   [**GetTypeInfoCount**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) gibt die Anzahl der Typbeschreibungen für das-Objekt zurück. Bei Objekten, die [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)unterstützen, ist die Anzahl von Typinformationen immer 1.
-   [**GetTypeInfo**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfo) Ruft eine Beschreibung der programmierbaren Schnittstelle des Objekts ab.
-   [**GetIDsOfNames**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) ordnet den Namen einer Methode oder Eigenschaft einer **DISPID** zu, die später zum Aufrufen der Methode oder Eigenschaft verwendet wird.
-   Der [**Aufruf**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) Ruft eine der Methoden des Objekts auf oder ruft eine seiner Eigenschaften ab oder legt Sie fest.

 

 