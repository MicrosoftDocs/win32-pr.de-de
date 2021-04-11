---
title: Verwenden der IAccessible-Schnittstelle
description: Die IAccessible-Schnittstelle ist eine Auflistung von Methoden, die die gängigsten Attribute und Verhaltensweisen einer Breite Palette von Benutzeroberflächen Elementen verfügbar machen.
ms.assetid: 82f6e934-58ea-47f2-98a3-2ab1c20f24c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218d009793dc1bebac2a7e5caeba8fa140ac0d96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310255"
---
# <a name="using-the-iaccessible-interface"></a><span data-ttu-id="b54ff-103">Verwenden der IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b54ff-103">Using the IAccessible Interface</span></span>

<span data-ttu-id="b54ff-104">Die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle ist eine Auflistung von Methoden, die die gängigsten Attribute und Verhaltensweisen einer Breite Palette von Benutzeroberflächen Elementen verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="b54ff-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is a collection of methods that expose the most common attributes and behaviors of a wide range of UI elements.</span></span> <span data-ttu-id="b54ff-105">Ein Benutzeroberflächen Element ist ein Steuerelement, z. b. ein Menü oder eine Schaltfläche, das Teil der Benutzeroberfläche ist.</span><span class="sxs-lookup"><span data-stu-id="b54ff-105">A UI element is a control, such as a menu or push button, that is part of the user interface.</span></span> <span data-ttu-id="b54ff-106">Ein Barrierefreies Objekt ist ein UI-Element, das über eine sinnvolle **IAccessible** -Schnittstelle verfügt.</span><span class="sxs-lookup"><span data-stu-id="b54ff-106">An accessible object is a UI element that has a meaningful **IAccessible** interface.</span></span>

<span data-ttu-id="b54ff-107">Einige der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften können nicht auf jede Art von Benutzeroberflächen Element angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b54ff-107">Some of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties are not applicable to every kind of user interface element.</span></span> <span data-ttu-id="b54ff-108">Außerdem variiert die Implementierung von **IAccessible** von der Anwendung bis zur Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b54ff-108">Also, the implementation of **IAccessible** varies from application to application.</span></span>

<span data-ttu-id="b54ff-109">Obwohl die Parameter und Rückgabewerte für die Eigenschaften und Methoden von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) vollständig angegeben sind, wird die Art und Weise, wie ein Client eine Eigenschaft verwenden sollte oder wie ein Server eine Eigenschaft implementieren soll, manchmal interpretiert.</span><span class="sxs-lookup"><span data-stu-id="b54ff-109">Although the parameters and return values for the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods are fully specified, how a client should use a property or how a server should implement a property is sometimes subject to interpretation.</span></span>

<span data-ttu-id="b54ff-110">Dieser Abschnitt enthält Vorschläge, Richtlinien und Beispiele für die Unterstützung von Client Anwendungen beim Abrufen von Informationen zu Benutzeroberflächen Elementen und zur Unterstützung von Server Anwendungen bei der Bereitstellung geeigneter</span><span class="sxs-lookup"><span data-stu-id="b54ff-110">This section provides suggestions, guidelines, and examples for helping client applications obtain information about UI elements and for helping server applications provide appropriate information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b54ff-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="b54ff-111">In this section</span></span>

-   [<span data-ttu-id="b54ff-112">Inhalt von beschreibenden Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b54ff-112">Content of Descriptive Properties</span></span>](content-of-descriptive-properties.md)
-   [<span data-ttu-id="b54ff-113">Auswahl-und Fokus Eigenschaften und-Methoden</span><span class="sxs-lookup"><span data-stu-id="b54ff-113">Selection and Focus Properties and Methods</span></span>](selection-and-focus-properties-and-methods.md)
-   [<span data-ttu-id="b54ff-114">Objekt Navigations Eigenschaften und-Methoden</span><span class="sxs-lookup"><span data-stu-id="b54ff-114">Object Navigation Properties and Methods</span></span>](object-navigation-properties-and-methods.md)

 

 




