---
description: 'Schritt 6:'
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: 'Schritt 6: Initialisieren des Dialog Felds'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 282eb03db38c543678fb2c4ef1155e1150b419bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350032"
---
# <a name="step-6-initialize-the-dialog"></a><span data-ttu-id="97920-104">Schritt 6:</span><span class="sxs-lookup"><span data-stu-id="97920-104">Step 6.</span></span> <span data-ttu-id="97920-105">Initialisieren des Dialog Felds</span><span class="sxs-lookup"><span data-stu-id="97920-105">Initialize the Dialog</span></span>

<span data-ttu-id="97920-106">Überschreiben Sie die [**cbasepropertypage:: onaktivierungs**](cbasepropertypage-onactivate.md) -Methode, um das Dialogfeld zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="97920-106">Override the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method to initialize the dialog.</span></span> <span data-ttu-id="97920-107">In diesem Beispiel verwendet die Eigenschaften Seite ein Schieberegler-Steuerelement, sodass der erste Schritt in **onreaktivierungs** die Initialisierung der allgemeinen Steuerelement Bibliothek ist.</span><span class="sxs-lookup"><span data-stu-id="97920-107">In this example, the property page uses a slider control, so the first step in **OnActivate** is to initialize the common control library.</span></span> <span data-ttu-id="97920-108">Die Methode initialisiert dann das Schieberegler-Steuerelement mit dem aktuellen Wert der Eigenschaft Sättigung des Filters:</span><span class="sxs-lookup"><span data-stu-id="97920-108">The method then initializes the slider control using the current value of the filter's saturation property:</span></span>


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



<span data-ttu-id="97920-109">Nächste [Schritte: Schritt 7. Fenster Meldungen behandeln](step-7--handle-window-messages.md)</span><span class="sxs-lookup"><span data-stu-id="97920-109">Next: [Step 7. Handle Window Messages](step-7--handle-window-messages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="97920-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97920-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97920-111">Erstellen einer Filter Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="97920-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



