---
title: Verfügbar machen von Active Accessibility Benutzeroberflächen Elemente
description: Microsoft Active Accessibility erstellt ein Proxy Objekt für jedes Benutzeroberflächen Element, das es verfügbar macht.
ms.assetid: 64aa8fac-cea7-4466-ae34-2760956c296b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b450ebe79aa467100fe9b6fb3bc4cdfb5540b60c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206746"
---
# <a name="how-active-accessibility-exposes-user-interface-elements"></a>Verfügbar machen von Active Accessibility Benutzeroberflächen Elemente

Microsoft Active Accessibility erstellt ein *Proxy* Objekt für jedes Benutzeroberflächen Element, das es verfügbar macht. Ein Proxy Objekt fungiert als Vermittler zwischen dem Client Hilfsprogramm und dem UI-Element. Der Zweck des Proxy Objekts ist die Überwachung der Lebensdauer des Benutzeroberflächen Elements und die Implementierung der Eigenschaften und Methoden von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) im Namen des Benutzeroberflächen Elements. Server Entwickler, die benutzerdefinierte Steuerelemente oder andere benutzerdefinierte Benutzeroberflächen Elemente erstellen, sollten ebenfalls Proxy Objekte erstellen. Weitere Informationen finden Sie unter [Erstellen von Proxy Objekten](creating-proxy-objects.md).

Wenn Microsoft Active Accessibility ein Objekt erstellt, um ein vordefiniertes oder gängiges Steuerelement verfügbar zu machen, erstellt es tatsächlich mindestens zwei Objekte: eine für das Steuerelement und eine für das Fenster, das das Steuerelement umgibt. In den meisten Fällen verfügen diese übergeordneten Fenster über die [Role-Eigenschaft](role-property.md) des [**Rollen \_ System \_ Fensters**](object-roles.md) und haben die gleiche [Name-Eigenschaft](name-property.md) und den Fenster Klassennamen wie das Steuerelement. Die Informationen über das Steuerelement, das von Clients an Endbenutzer übermittelt wird, sind im-Objekt enthalten, das von Microsoft Active Accessibility erstellt wird, um das Steuerelement verfügbar zu machen, nicht für das übergeordnete Objekt, das das Fenster verfügbar macht

Weitere Informationen finden Sie in den nachfolgenden Themen.

-   [Auschecken unnötiger Objekte](screening-out-unnecessary-objects.md)
-   [Bereitstellen der Name-Eigenschaft](providing-the-name-property.md)
-   [Sicherstellen, dass Benutzeroberflächen Elemente ordnungsgemäß benannt sind](ensure-that-ui-elements-are-named-correctly.md)
-   [Nicht unterstützte Elemente der Benutzeroberfläche](unsupported-user-interface-elements.md)

 

 




