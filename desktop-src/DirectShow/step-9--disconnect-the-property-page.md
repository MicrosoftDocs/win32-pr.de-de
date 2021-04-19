---
description: Schritt 9
ms.assetid: 3e476422-ab76-4a2b-af9b-d9d065d79e5b
title: Schritt 9 Trennen der Eigenschaften Seite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59c620179e95afa3f1b949ed40cbfc3a2bca11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356963"
---
# <a name="step-9-disconnect-the-property-page"></a><span data-ttu-id="81301-104">Schritt 9</span><span class="sxs-lookup"><span data-stu-id="81301-104">Step 9.</span></span> <span data-ttu-id="81301-105">Trennen der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="81301-105">Disconnect the Property Page</span></span>

<span data-ttu-id="81301-106">Überschreiben Sie die [**cbasepropertypage:: OnDisconnect**](cbasepropertypage-ondisconnect.md) -Methode, um alle Schnittstellen freizugeben, die Sie in der **OnConnect** -Methode abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="81301-106">Override the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method to release any interfaces that you obtained in the **OnConnect** method.</span></span> <span data-ttu-id="81301-107">Wenn der Benutzer das Eigenschaften Blatt schließt, ohne die Änderungen zu übernehmen, sollten Sie außerdem die ursprünglichen Werte wiederherstellen, wenn Sie sich geändert haben.</span><span class="sxs-lookup"><span data-stu-id="81301-107">Also, if the user dismisses the property sheet without committing the changes, you should restore the original values if they have changed.</span></span> <span data-ttu-id="81301-108">Es gibt keine "OnCancel"-Methode, die aufgerufen wird, wenn der Benutzer abbricht, sodass Sie nachverfolgen müssen, ob der Benutzer " **onapplychanges**" aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="81301-108">There is no "OnCancel" method that gets called when the user cancels, so you need to keep track of whether the user has called **OnApplyChanges**.</span></span> <span data-ttu-id="81301-109">In diesem Beispiel wird die oben \_ beschriebene m LVAL-Variable verwendet:</span><span class="sxs-lookup"><span data-stu-id="81301-109">This example uses the m\_lVal variable, described earlier:</span></span>


```C++
HRESULT CGrayProp::OnDisconnect(void)
{
    if (m_pGray)
    {
        // If the user clicked OK, m_lVal holds the new value.
        // Otherwise, if the user clicked Cancel, m_lVal is the old value.
        m_pGray->SetSaturation(m_lVal);  
        m_pGray->Release();
        m_pGray = NULL;
    }
    return S_OK;
}
```



<span data-ttu-id="81301-110">Weiter: [Schritt 10. COM-Registrierung unterstützen](step-10--support-com-registration.md)</span><span class="sxs-lookup"><span data-stu-id="81301-110">Next: [Step 10. Support COM Registration](step-10--support-com-registration.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="81301-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="81301-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81301-112">Erstellen einer Filter Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="81301-112">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



