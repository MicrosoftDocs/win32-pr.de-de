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
# <a name="step-6-initialize-the-dialog"></a>Schritt 6: Initialisieren des Dialog Felds

Überschreiben Sie die [**cbasepropertypage:: onaktivierungs**](cbasepropertypage-onactivate.md) -Methode, um das Dialogfeld zu initialisieren. In diesem Beispiel verwendet die Eigenschaften Seite ein Schieberegler-Steuerelement, sodass der erste Schritt in **onreaktivierungs** die Initialisierung der allgemeinen Steuerelement Bibliothek ist. Die Methode initialisiert dann das Schieberegler-Steuerelement mit dem aktuellen Wert der Eigenschaft Sättigung des Filters:


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



Nächste [Schritte: Schritt 7. Fenster Meldungen behandeln](step-7--handle-window-messages.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Filter Eigenschaften Seite](creating-a-filter-property-page.md)
</dt> </dl>

 

 



