---
title: How Active Accessibility Exposes Benutzeroberfläche Elements
description: Microsoft Active Accessibility erstellt ein Proxyobjekt für jedes Verfügbar machende Benutzeroberflächenelement.
ms.assetid: 64aa8fac-cea7-4466-ae34-2760956c296b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4260788cc37aa6d4a33fcccb68a51fb61833d753c98ba4ae5dcff89f0d18cec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994160"
---
# <a name="how-active-accessibility-exposes-user-interface-elements"></a>How Active Accessibility Exposes Benutzeroberfläche Elements

Microsoft Active Accessibility erstellt ein *Proxyobjekt* für jedes benutzeroberflächenelement, das es verfügbar macht. Ein Proxyobjekt fungiert als Vermittler zwischen dem Clientprogramm und dem Benutzeroberflächenelement. Der Zweck des Proxyobjekts besteht in der Überwachung der Lebensdauer des Ui-Elements und der Implementierung der [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und -Methoden im Namen des UI-Elements. Serverentwickler, die benutzerdefinierte Steuerelemente oder andere benutzerdefinierte Benutzeroberflächenelemente erstellen, sollten auch Proxyobjekte erstellen. Weitere Informationen finden Sie unter [Erstellen von Proxyobjekten.](creating-proxy-objects.md)

Wenn Microsoft Active Accessibility objekt erstellt, um ein vordefiniertes oder allgemeines Steuerelement verfügbar zu machen, werden tatsächlich mindestens zwei Objekte erstellt: eines für das Steuerelement und eines für das Fenster, das das Steuerelement umgibt. In den meisten Fällen verfügen diese übergeordneten Fenster über die [Role-Eigenschaft](role-property.md) [**von ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) und haben die gleiche [Name-Eigenschaft](name-property.md) und den gleichen Fensterklassennamen wie das -Steuerelement. Die Informationen über das Steuerelement, das Clients Endbenutzern vermitteln, sind in dem Objekt enthalten, das Microsoft Active Accessibility erstellt, um das Steuerelement verfügbar zu machen, nicht das übergeordnete Objekt, das das Fenster verfügbar macht, das das Steuerelement umgibt.

Weitere Informationen finden Sie in den folgenden Themen.

-   [Aufsparen unnötiger Objekte](screening-out-unnecessary-objects.md)
-   [Bereitstellen der Name-Eigenschaft](providing-the-name-property.md)
-   [Sicherstellen, dass Benutzeroberflächenelemente ordnungsgemäß benannt sind](ensure-that-ui-elements-are-named-correctly.md)
-   [Nicht unterstützte Benutzeroberfläche Elements](unsupported-user-interface-elements.md)

 

 




