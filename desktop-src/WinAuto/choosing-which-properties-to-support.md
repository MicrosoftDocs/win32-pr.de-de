---
title: Auswählen der zu unterstützten Eigenschaften
description: Die IAccessible-Eigenschaften bieten Server Entwicklern die Möglichkeit, eine Vielzahl von Benutzeroberflächen Elementen zu beschreiben.
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c88a808889403f88d414f7ad950b3e431c00e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310500"
---
# <a name="choosing-which-properties-to-support"></a><span data-ttu-id="2bcd9-103">Auswählen der zu unterstützten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2bcd9-103">Choosing Which Properties to Support</span></span>

<span data-ttu-id="2bcd9-104">Die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften bieten Server Entwicklern die Möglichkeit, eine Vielzahl von Benutzeroberflächen Elementen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="2bcd9-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties provide a way for server developers to describe a wide variety of user interface elements.</span></span> <span data-ttu-id="2bcd9-105">Allerdings sind nicht alle Eigenschaften für jede Art von Benutzeroberflächen Element anwendbar.</span><span class="sxs-lookup"><span data-stu-id="2bcd9-105">But not all of the properties are applicable for every kind of user interface element.</span></span> <span data-ttu-id="2bcd9-106">Außerdem bieten einige Eigenschaften beschreibende Informationen, die hilfreich, aber nicht unbedingt erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="2bcd9-106">Additionally, some properties provide descriptive information that is useful but not essential.</span></span>

<span data-ttu-id="2bcd9-107">Server müssen für jedes Objekt die folgenden Eigenschaften und Methoden unterstützen:</span><span class="sxs-lookup"><span data-stu-id="2bcd9-107">Servers must support the following properties and methods for every object:</span></span>

-   [<span data-ttu-id="2bcd9-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2bcd9-108">**Name**</span></span>](name-property.md)
-   [<span data-ttu-id="2bcd9-109">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="2bcd9-109">**Role**</span></span>](role-property.md)
-   [<span data-ttu-id="2bcd9-110">**State**</span><span class="sxs-lookup"><span data-stu-id="2bcd9-110">**State**</span></span>](state-property.md)
-   <span data-ttu-id="2bcd9-111">[**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) und [ **IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)</span><span class="sxs-lookup"><span data-stu-id="2bcd9-111">[**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) and [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)</span></span>
-   <span data-ttu-id="2bcd9-112">[**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) und [ **IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)</span><span class="sxs-lookup"><span data-stu-id="2bcd9-112">[**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) and [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)</span></span>

<span data-ttu-id="2bcd9-113">Die folgenden Eigenschaften und Methoden müssen unterstützt werden, wenn Sie auf das Objekt anwendbar sind:</span><span class="sxs-lookup"><span data-stu-id="2bcd9-113">The following properties and method must be supported if they are applicable to the object:</span></span>

-   [<span data-ttu-id="2bcd9-114">**KeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="2bcd9-114">**KeyboardShortcut**</span></span>](keyboardshortcut-property.md)
-   [<span data-ttu-id="2bcd9-115">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2bcd9-115">**Value**</span></span>](value-property.md)

<span data-ttu-id="2bcd9-116">Die folgenden Eigenschaften und Methoden müssen unterstützt werden, wenn das-Objekt über untergeordnete Elemente verfügt:</span><span class="sxs-lookup"><span data-stu-id="2bcd9-116">The following properties and method must be supported if the object has children:</span></span>

-   <span data-ttu-id="2bcd9-117">[**Child**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) und [ **childCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)</span><span class="sxs-lookup"><span data-stu-id="2bcd9-117">[**Child**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) and [**ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)</span></span>
-   <span data-ttu-id="2bcd9-118">[**Fokus, Auswahl**](selection-and-focus-properties-and-methods.md)und [ **IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)</span><span class="sxs-lookup"><span data-stu-id="2bcd9-118">[**Focus, Selection**](selection-and-focus-properties-and-methods.md), and [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)</span></span>

<span data-ttu-id="2bcd9-119">Die folgenden Eigenschaften sind optional, bieten jedoch nützliche beschreibende Informationen über das Objekt.</span><span class="sxs-lookup"><span data-stu-id="2bcd9-119">The following properties are optional, but provide useful descriptive information about the object.</span></span> <span data-ttu-id="2bcd9-120">Die [**Description**](description-property.md) -Eigenschaft wird implementiert, um Bitmaps und andere Bilder zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="2bcd9-120">The [**Description**](description-property.md) property is implemented to describe bitmaps and other images.</span></span>

-   [<span data-ttu-id="2bcd9-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2bcd9-121">**Description**</span></span>](description-property.md)
-   <span data-ttu-id="2bcd9-122">[**DEFAULTACTION**](defaultaction-property.md) und [ **IAccessible:: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)</span><span class="sxs-lookup"><span data-stu-id="2bcd9-122">[**DefaultAction**](defaultaction-property.md) and [**IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)</span></span>
-   [<span data-ttu-id="2bcd9-123">**Hilfe**</span><span class="sxs-lookup"><span data-stu-id="2bcd9-123">**Help**</span></span>](help-property.md)
-   [<span data-ttu-id="2bcd9-124">**HelpTopic**</span><span class="sxs-lookup"><span data-stu-id="2bcd9-124">**HelpTopic**</span></span>](helptopic-property.md)

 

 




