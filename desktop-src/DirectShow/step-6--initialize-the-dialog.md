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
# <a name="step-6-initialize-the-dialog"></a>Schritt 6: Initialisieren des Dialogfelds

Überschreiben Sie die [**CBasePropertyPage::OnActivate-Methode,**](cbasepropertypage-onactivate.md) um das Dialogfeld zu initialisieren. In diesem Beispiel verwendet die Eigenschaftenseite ein Schieberegler-Steuerelement, sodass der erste Schritt in **OnActivate** darin besteht, die allgemeine Steuerelementbibliothek zu initialisieren. Die -Methode initialisiert dann das Schieberegler-Steuerelement unter Verwendung des aktuellen Werts der Sättigungseigenschaft des Filters:


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



Weiter: [Schritt 7. Verarbeiten von Fenstermeldungen](step-7--handle-window-messages.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Filtereigenschaftenseite](creating-a-filter-property-page.md)
</dt> </dl>

 

 



