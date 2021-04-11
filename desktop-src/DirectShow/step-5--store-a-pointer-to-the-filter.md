---
description: 'Schritt 5:'
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: 'Schritt 5: Speichern eines Zeigers auf den Filter'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eff096c6afcf830494ef02920176d8f80a3b9569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217481"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a><span data-ttu-id="9ee85-104">Schritt 5:</span><span class="sxs-lookup"><span data-stu-id="9ee85-104">Step 5.</span></span> <span data-ttu-id="9ee85-105">Speichern eines Zeigers auf den Filter</span><span class="sxs-lookup"><span data-stu-id="9ee85-105">Store a Pointer to the Filter</span></span>

<span data-ttu-id="9ee85-106">Überschreiben Sie die [**cbasepropertypage:: OnConnect**](cbasepropertypage-onconnect.md) -Methode, um einen Zeiger auf den Filter zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9ee85-106">Override the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to store a pointer to the filter.</span></span> <span data-ttu-id="9ee85-107">Im folgenden Beispiel wird der- *Punk* -Parameter für die benutzerdefinierte isationinterface des Filters abgefragt:</span><span class="sxs-lookup"><span data-stu-id="9ee85-107">The following example queries the *pUnk* parameter for the filter's custom ISaturation interface:</span></span>


```C++
HRESULT CGrayProp::OnConnect(IUnknown *pUnk)
{
    if (pUnk == NULL)
    {
        return E_POINTER;
    }
    ASSERT(m_pGray == NULL);
    return pUnk->QueryInterface(IID_ISaturation, 
        reinterpret_cast<void**>(&m_pGray));
}
```



<span data-ttu-id="9ee85-108">Weiter: [Schritt 6. Initialisieren Sie das Dialog](step-6--initialize-the-dialog.md)Feld.</span><span class="sxs-lookup"><span data-stu-id="9ee85-108">Next: [Step 6. Initialize the Dialog](step-6--initialize-the-dialog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ee85-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9ee85-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ee85-110">Erstellen einer Filter Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="9ee85-110">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



