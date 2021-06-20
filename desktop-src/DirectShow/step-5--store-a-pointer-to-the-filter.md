---
description: Speichern Sie einen Zeiger auf einen Filter als Teil der Erstellung einer Filtereigenschaftenseite für einen benutzerdefinierten DirectShow-Filter.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: 'Schritt 5: Speichern eines Zeigers auf den Filter'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa1e98e98fcc0f41d07774b8a2d1ab93dea8d0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406793"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a><span data-ttu-id="a21e2-104">Schritt 5:</span><span class="sxs-lookup"><span data-stu-id="a21e2-104">Step 5.</span></span> <span data-ttu-id="a21e2-105">Speichern eines Zeigers auf den Filter</span><span class="sxs-lookup"><span data-stu-id="a21e2-105">Store a Pointer to the Filter</span></span>

<span data-ttu-id="a21e2-106">Überschreiben Sie die [**CBasePropertyPage::OnConnect-Methode,**](cbasepropertypage-onconnect.md) um einen Zeiger auf den Filter zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a21e2-106">Override the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to store a pointer to the filter.</span></span> <span data-ttu-id="a21e2-107">Im folgenden Beispiel wird der *pUnk-Parameter* für die benutzerdefinierte ISaturation-Schnittstelle des Filters abgefragt:</span><span class="sxs-lookup"><span data-stu-id="a21e2-107">The following example queries the *pUnk* parameter for the filter's custom ISaturation interface:</span></span>


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



<span data-ttu-id="a21e2-108">Weiter: [Schritt 6. Initialisieren Sie das Dialogfeld](step-6--initialize-the-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="a21e2-108">Next: [Step 6. Initialize the Dialog](step-6--initialize-the-dialog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a21e2-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a21e2-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a21e2-110">Erstellen einer Filtereigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="a21e2-110">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



