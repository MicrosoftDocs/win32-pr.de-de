---
description: Überschreiben Sie die CBasePropertyPage::OnActivate-Methode, um das Dialogfeld im Rahmen der Erstellung einer Filtereigenschaftenseite für einen benutzerdefinierten DirectShow-Filter zu initialisieren.
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: 'Schritt 6: Initialisieren des Dialogfelds'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcbdf18e272ac548227626bc9da4f992786a4ab3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404493"
---
# <a name="step-6-initialize-the-dialog"></a><span data-ttu-id="15a09-104">Schritt 6:</span><span class="sxs-lookup"><span data-stu-id="15a09-104">Step 6.</span></span> <span data-ttu-id="15a09-105">Initialisieren des Dialogfelds</span><span class="sxs-lookup"><span data-stu-id="15a09-105">Initialize the Dialog</span></span>

<span data-ttu-id="15a09-106">Überschreiben Sie die [**CBasePropertyPage::OnActivate-Methode,**](cbasepropertypage-onactivate.md) um das Dialogfeld zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="15a09-106">Override the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method to initialize the dialog.</span></span> <span data-ttu-id="15a09-107">In diesem Beispiel verwendet die Eigenschaftenseite ein Schieberegler-Steuerelement, sodass der erste Schritt in **OnActivate** darin besteht, die allgemeine Steuerelementbibliothek zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="15a09-107">In this example, the property page uses a slider control, so the first step in **OnActivate** is to initialize the common control library.</span></span> <span data-ttu-id="15a09-108">Die -Methode initialisiert dann das Schieberegler-Steuerelement unter Verwendung des aktuellen Werts der Sättigungseigenschaft des Filters:</span><span class="sxs-lookup"><span data-stu-id="15a09-108">The method then initializes the slider control using the current value of the filter's saturation property:</span></span>


```C++
HRESULT CGrayProp::OnActivate(void)
{
    INITCOMMONCONTROLSEX icc;
    icc.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icc.dwICC = ICC_BAR_CLASSES;
    if (InitCommonControlsEx(&icc) == FALSE)
    {
        return E_FAIL;
    }

    ASSERT(m_pGray != NULL);
    HRESULT hr = m_pGray->GetSaturation(&m_lVal);
    if (SUCCEEDED(hr))
    {
        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0,
            MAKELONG(SATURATION_MIN, SATURATION_MAX));

        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 
            (SATURATION_MAX - SATURATION_MIN) / 10, 0);

        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lVal);
    }
    return hr;
}
```



<span data-ttu-id="15a09-109">Weiter: [Schritt 7. Verarbeiten von Fenstermeldungen](step-7--handle-window-messages.md)</span><span class="sxs-lookup"><span data-stu-id="15a09-109">Next: [Step 7. Handle Window Messages](step-7--handle-window-messages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="15a09-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15a09-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15a09-111">Erstellen einer Filtereigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="15a09-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



