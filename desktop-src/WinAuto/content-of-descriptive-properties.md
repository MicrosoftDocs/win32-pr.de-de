---
title: Inhalt von beschreibenden Eigenschaften
description: Die IAccessible-Schnittstelle stellt beschreibende Eigenschaften zur Verfügung, die verschiedene Aspekte eines Objekts beschreiben.
ms.assetid: e6c1d1a3-417d-4aea-abac-f84a55f666b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271dc920034802b87afd4c76ab7ede6bb9476d99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515800"
---
# <a name="content-of-descriptive-properties"></a><span data-ttu-id="f18a4-103">Inhalt von beschreibenden Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f18a4-103">Content of Descriptive Properties</span></span>

<span data-ttu-id="f18a4-104">Die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle stellt beschreibende Eigenschaften zur Verfügung, die verschiedene Aspekte eines Objekts beschreiben.</span><span class="sxs-lookup"><span data-stu-id="f18a4-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface provides descriptive properties, which describe various aspects of an object.</span></span> <span data-ttu-id="f18a4-105">Einige dieser Eigenschaften sind inhaltsspezifisch. andere Eigenschaften verfügen über Inhalte, die aus beschreibenden Text bestehen, der vom Server bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f18a4-105">Some of these properties are content specific; other properties have content consisting of descriptive text that is provided by the server.</span></span> <span data-ttu-id="f18a4-106">Der Typ der Informationen für jede Eigenschaft variiert abhängig vom Objekt.</span><span class="sxs-lookup"><span data-stu-id="f18a4-106">The type of information for each property varies depending on the object.</span></span>

<span data-ttu-id="f18a4-107">In den folgenden Themen werden Informationen beschrieben, die von-Clients aus diesen Eigenschaften abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f18a4-107">The following topics describe information that clients obtain from these properties.</span></span> <span data-ttu-id="f18a4-108">Außerdem bieten Sie den Servern Vorschläge zum Auswählen von Inhalt.</span><span class="sxs-lookup"><span data-stu-id="f18a4-108">They also provide servers with suggestions for choosing content.</span></span>

-   [<span data-ttu-id="f18a4-109">Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f18a4-109">Name Property</span></span>](name-property.md)
-   [<span data-ttu-id="f18a4-110">Role-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f18a4-110">Role Property</span></span>](role-property.md)
-   [<span data-ttu-id="f18a4-111">State-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f18a4-111">State Property</span></span>](state-property.md)
-   [<span data-ttu-id="f18a4-112">Value-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f18a4-112">Value Property</span></span>](value-property.md)
-   [<span data-ttu-id="f18a4-113">Description-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f18a4-113">Description Property</span></span>](description-property.md)
-   [<span data-ttu-id="f18a4-114">Hilfe (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f18a4-114">Help Property</span></span>](help-property.md)
-   [<span data-ttu-id="f18a4-115">HelpTopic-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f18a4-115">HelpTopic Property</span></span>](helptopic-property.md)
-   [<span data-ttu-id="f18a4-116">KeyboardShortcut (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f18a4-116">KeyboardShortcut Property</span></span>](keyboardshortcut-property.md)
-   [<span data-ttu-id="f18a4-117">DEFAULTACTION (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f18a4-117">DefaultAction Property</span></span>](defaultaction-property.md)

<span data-ttu-id="f18a4-118">Beim Entwerfen von zugänglichen Objekten sollten Server Entwickler auch die folgenden Themen lesen:</span><span class="sxs-lookup"><span data-stu-id="f18a4-118">When designing accessible objects, server developers should also refer to the following topics:</span></span>

-   [<span data-ttu-id="f18a4-119">Auswählen der zu unterstützten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f18a4-119">Choosing Which Properties to Support</span></span>](choosing-which-properties-to-support.md)
-   [<span data-ttu-id="f18a4-120">Auswählen des Inhalts für beschreibende Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f18a4-120">Choosing the Content for Descriptive Properties</span></span>](choosing-the-content-for-descriptive-properties.md)

<span data-ttu-id="f18a4-121">Informationen zu den Parametern und Rückgabe Werten dieser Eigenschaften finden Sie im Abschnitt [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) der Referenz zu Microsoft Active Accessibility [C/C++](c-c---reference.md).</span><span class="sxs-lookup"><span data-stu-id="f18a4-121">For information about the parameters and return values of these properties, see the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) section of the Microsoft Active Accessibility[C/C++ Reference](c-c---reference.md).</span></span>

 

 




