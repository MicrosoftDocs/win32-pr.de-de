---
description: 'Schritt 8:'
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: 'Schritt 8: Anwenden von Eigenschafts Änderungen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46425613b8f23981a7b288121dc1a4ab0945452e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359450"
---
# <a name="step-8-apply-property-changes"></a><span data-ttu-id="99bc4-104">Schritt 8:</span><span class="sxs-lookup"><span data-stu-id="99bc4-104">Step 8.</span></span> <span data-ttu-id="99bc4-105">Anwenden von Eigenschafts Änderungen</span><span class="sxs-lookup"><span data-stu-id="99bc4-105">Apply Property Changes</span></span>

<span data-ttu-id="99bc4-106">Überschreiben Sie die [**cbasepropertypage:: onapplychanges**](cbasepropertypage-onapplychanges.md) -Methode, um einen Commit für alle Eigenschafts Änderungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="99bc4-106">Override the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method to commit any property changes.</span></span> <span data-ttu-id="99bc4-107">In diesem Beispiel wird die m \_ lnewval-Variable immer dann aktualisiert, wenn der Benutzer den Schieberegler durchläuft.</span><span class="sxs-lookup"><span data-stu-id="99bc4-107">In this example, the m\_lNewVal variable is updated whenever the user scrolls the slider bar.</span></span> <span data-ttu-id="99bc4-108">Die **onapplychanges** -Methode kopiert diesen Wert in die m \_ LVAL-Variable, wobei der ursprüngliche Wert überschrieben wird:</span><span class="sxs-lookup"><span data-stu-id="99bc4-108">The **OnApplyChanges** method copies this value into the m\_lVal variable, overwriting the original value:</span></span>


```C++
HRESULT CGrayProp::OnApplyChanges(void)
{
    m_lVal = m_lNewVal;
    return S_OK;
} 
```



<span data-ttu-id="99bc4-109">Weiter: [Schritt 9. Trennen Sie die Eigenschaften Seite](step-9--disconnect-the-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="99bc4-109">Next: [Step 9. Disconnect the Property Page](step-9--disconnect-the-property-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="99bc4-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="99bc4-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99bc4-111">Erstellen einer Filter Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="99bc4-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



