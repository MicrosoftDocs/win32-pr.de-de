---
title: DEFAULTACTION (Eigenschaft)
description: Die DEFAULTACTION-Eigenschaft eines Objekts beschreibt die primäre Manipulations Methode des Objekts aus der Sicht des Benutzers. Die DEFAULTACTION-Eigenschaft eines Objekts sollte ein Verb oder ein kurzes Verb-Ausdruck sein.
ms.assetid: 8242c0af-b42e-44a4-8807-d6740fa1a24a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc032037c331a2022f227cb8e8547dd8bce9d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309464"
---
# <a name="defaultaction-property"></a><span data-ttu-id="3b994-104">DEFAULTACTION (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3b994-104">DefaultAction Property</span></span>

<span data-ttu-id="3b994-105">Die **DEFAULTACTION** -Eigenschaft eines Objekts beschreibt die primäre Manipulations Methode des Objekts aus der Sicht des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="3b994-105">An object's **DefaultAction** property describes the object's primary method of manipulation from the user's viewpoint.</span></span> <span data-ttu-id="3b994-106">Die **DEFAULTACTION** -Eigenschaft eines Objekts sollte ein Verb oder ein kurzes Verb-Ausdruck sein.</span><span class="sxs-lookup"><span data-stu-id="3b994-106">An object's **DefaultAction** property should be a verb or a short verb phrase.</span></span>

<span data-ttu-id="3b994-107">Die **DEFAULTACTION** -Eigenschaft wird durch Aufrufen von " [**IAccessible:: get \_ accdefaultaction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3b994-107">The **DefaultAction** property is retrieved by calling [**IAccessible::get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).</span></span>

<span data-ttu-id="3b994-108">Um die Standardaktion eines Objekts auszuführen, wird " [**IAccessible:: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)" aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3b994-108">To perform an object's default action, clients call [**IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).</span></span>

<span data-ttu-id="3b994-109">Nicht alle Objekte haben Standard Aktionen, und einige Objekte verfügen über eine Standardaktion, die sich auf Ihre [**Wert**](value-property.md) Eigenschaft bezieht, z. b. in den folgenden Beispielen:</span><span class="sxs-lookup"><span data-stu-id="3b994-109">Not all objects have default actions, and some objects have a default action that is related to its [**Value**](value-property.md) property, such as in the following examples:</span></span>

-   <span data-ttu-id="3b994-110">Ein ausgewähltes Kontrollkästchen hat die Standardaktion "uncheck" und den Wert "aktiviert".</span><span class="sxs-lookup"><span data-stu-id="3b994-110">A selected check box has a default action of "Uncheck" and a value of "Checked."</span></span>
-   <span data-ttu-id="3b994-111">Ein gelöschtes Kontrollkästchen hat die Standardaktion "Check" und den Wert "deaktiviert".</span><span class="sxs-lookup"><span data-stu-id="3b994-111">A cleared check box has a default action of "Check" and a value of "Unchecked."</span></span>
-   <span data-ttu-id="3b994-112">Eine Schaltfläche mit der Bezeichnung "Print" hat die Standardaktion "Press" ohne Wert.</span><span class="sxs-lookup"><span data-stu-id="3b994-112">A button labeled "Print" has a default action of "Press," with no value.</span></span>
-   <span data-ttu-id="3b994-113">Ein statisches Text Steuerelement oder ein Bearbeitungs Steuerelement, das "Printer" anzeigt, hat keine Standardaktion, hat jedoch den Wert "Printer".</span><span class="sxs-lookup"><span data-stu-id="3b994-113">A static text control or an edit control that shows "Printer" has no default action, but has a value of "Printer."</span></span>

 

 




