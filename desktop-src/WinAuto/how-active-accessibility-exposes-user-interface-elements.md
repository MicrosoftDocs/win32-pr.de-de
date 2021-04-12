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
# <a name="how-active-accessibility-exposes-user-interface-elements"></a><span data-ttu-id="6c647-103">Verfügbar machen von Active Accessibility Benutzeroberflächen Elemente</span><span class="sxs-lookup"><span data-stu-id="6c647-103">How Active Accessibility Exposes User Interface Elements</span></span>

<span data-ttu-id="6c647-104">Microsoft Active Accessibility erstellt ein *Proxy* Objekt für jedes Benutzeroberflächen Element, das es verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="6c647-104">Microsoft Active Accessibility creates a *proxy* object for each user interface element that it exposes.</span></span> <span data-ttu-id="6c647-105">Ein Proxy Objekt fungiert als Vermittler zwischen dem Client Hilfsprogramm und dem UI-Element.</span><span class="sxs-lookup"><span data-stu-id="6c647-105">A proxy object acts as an intermediary between the client utility and the UI element.</span></span> <span data-ttu-id="6c647-106">Der Zweck des Proxy Objekts ist die Überwachung der Lebensdauer des Benutzeroberflächen Elements und die Implementierung der Eigenschaften und Methoden von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) im Namen des Benutzeroberflächen Elements.</span><span class="sxs-lookup"><span data-stu-id="6c647-106">The purpose of the proxy object is to monitor the life span of the UI element and to implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods on behalf of the UI element.</span></span> <span data-ttu-id="6c647-107">Server Entwickler, die benutzerdefinierte Steuerelemente oder andere benutzerdefinierte Benutzeroberflächen Elemente erstellen, sollten ebenfalls Proxy Objekte erstellen.</span><span class="sxs-lookup"><span data-stu-id="6c647-107">Server developers who create custom controls or other custom UI elements should also create proxy objects.</span></span> <span data-ttu-id="6c647-108">Weitere Informationen finden Sie unter [Erstellen von Proxy Objekten](creating-proxy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6c647-108">For more information, see [Creating Proxy Objects](creating-proxy-objects.md).</span></span>

<span data-ttu-id="6c647-109">Wenn Microsoft Active Accessibility ein Objekt erstellt, um ein vordefiniertes oder gängiges Steuerelement verfügbar zu machen, erstellt es tatsächlich mindestens zwei Objekte: eine für das Steuerelement und eine für das Fenster, das das Steuerelement umgibt.</span><span class="sxs-lookup"><span data-stu-id="6c647-109">When Microsoft Active Accessibility creates an object to expose a predefined or common control, it actually creates at least two objects: one for the control and one for the window that surrounds the control.</span></span> <span data-ttu-id="6c647-110">In den meisten Fällen verfügen diese übergeordneten Fenster über die [Role-Eigenschaft](role-property.md) des [**Rollen \_ System \_ Fensters**](object-roles.md) und haben die gleiche [Name-Eigenschaft](name-property.md) und den Fenster Klassennamen wie das Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="6c647-110">In most cases, these parent windows have the [Role property](role-property.md) of [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) and have the same [Name property](name-property.md) and window class name as the control.</span></span> <span data-ttu-id="6c647-111">Die Informationen über das Steuerelement, das von Clients an Endbenutzer übermittelt wird, sind im-Objekt enthalten, das von Microsoft Active Accessibility erstellt wird, um das Steuerelement verfügbar zu machen, nicht für das übergeordnete Objekt, das das Fenster verfügbar macht</span><span class="sxs-lookup"><span data-stu-id="6c647-111">The information about the control that clients convey to end users is contained in the object that Microsoft Active Accessibility creates to expose the control, not the parent object that exposes the window that surrounds the control.</span></span>

<span data-ttu-id="6c647-112">Weitere Informationen finden Sie in den nachfolgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="6c647-112">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="6c647-113">Auschecken unnötiger Objekte</span><span class="sxs-lookup"><span data-stu-id="6c647-113">Screening Out Unnecessary Objects</span></span>](screening-out-unnecessary-objects.md)
-   [<span data-ttu-id="6c647-114">Bereitstellen der Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6c647-114">Providing the Name Property</span></span>](providing-the-name-property.md)
-   [<span data-ttu-id="6c647-115">Sicherstellen, dass Benutzeroberflächen Elemente ordnungsgemäß benannt sind</span><span class="sxs-lookup"><span data-stu-id="6c647-115">Ensuring that UI Elements are Correctly Named</span></span>](ensure-that-ui-elements-are-named-correctly.md)
-   [<span data-ttu-id="6c647-116">Nicht unterstützte Elemente der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="6c647-116">Unsupported User Interface Elements</span></span>](unsupported-user-interface-elements.md)

 

 




