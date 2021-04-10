---
title: Value-Eigenschaft
description: Die Value-Eigenschaft stellt eine Textdarstellung der visuellen Informationen dar, die in einem-Objekt enthalten sind. Die Value-Eigenschaft wird nicht von allen Objekten unterstützt.
ms.assetid: 89b99645-31f5-458a-ae61-a72bf1338195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6cd3ad86b9ce3a4fcc917fc4f49792adf432bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310152"
---
# <a name="value-property"></a><span data-ttu-id="85da5-104">Value-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="85da5-104">Value Property</span></span>

<span data-ttu-id="85da5-105">Die **value** -Eigenschaft stellt eine Textdarstellung der visuellen Informationen dar, die in einem-Objekt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="85da5-105">The **Value** property provides a textual representation of the visual information contained in an object.</span></span> <span data-ttu-id="85da5-106">Die **value** -Eigenschaft wird nicht von allen Objekten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="85da5-106">Not all objects support the **Value** property.</span></span>

<span data-ttu-id="85da5-107">Die **value** -Eigenschaft wird durch Aufrufen von [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="85da5-107">The **Value** property is retrieved by calling [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span></span>

<span data-ttu-id="85da5-108">Die **value** -Eigenschaft teilt dem Client Informationen zu den visuellen Informationen zu, die in einem-Objekt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="85da5-108">The **Value** property tells the client about the visual information contained in an object.</span></span> <span data-ttu-id="85da5-109">Beispielsweise ist der Wert eines Bearbeitungs Steuer Elements der enthaltene Text, während ein Menü Element keinen Wert besitzt.</span><span class="sxs-lookup"><span data-stu-id="85da5-109">For example, an edit control's value is the text it contains, whereas a menu item has no value.</span></span>

## <a name="providing-hierarchical-information"></a><span data-ttu-id="85da5-110">Bereitstellen hierarchischer Informationen</span><span class="sxs-lookup"><span data-stu-id="85da5-110">Providing Hierarchical Information</span></span>

<span data-ttu-id="85da5-111">Die **value** -Eigenschaft stellt hierarchische Informationen in Fällen wie einem Strukturansicht-Steuerelement bereit.</span><span class="sxs-lookup"><span data-stu-id="85da5-111">The **Value** property provides hierarchical information in cases such as a tree view control.</span></span> <span data-ttu-id="85da5-112">Obwohl das übergeordnete Objekt im Strukturansicht-Steuerelement keine Informationen in der **value** -Eigenschaft bereitstellt, verfügt jedes Element im Steuerelement über einen NULL basierten Wert, der die Ebene innerhalb der Hierarchie darstellt.</span><span class="sxs-lookup"><span data-stu-id="85da5-112">Although the parent object in the tree view control does not provide information in the **Value** property, each item within the control has a zero-based value that represents its level within the hierarchy.</span></span> <span data-ttu-id="85da5-113">Elemente der obersten Ebene haben den Wert 0 (null), Elemente der zweiten Ebene haben den Wert 1 usw.</span><span class="sxs-lookup"><span data-stu-id="85da5-113">Top-level items have a value of zero, second-level items have a value of one, and so on.</span></span>

 

 




