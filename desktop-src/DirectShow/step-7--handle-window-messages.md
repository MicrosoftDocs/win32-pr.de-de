---
description: Schritt 7.
ms.assetid: 12bb1288-e764-4bc1-bea5-196e17cf3557
title: Schritt 7. Fenster Meldungen behandeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd1c44dd65a4f9f430b4223f0a5a0e4763af981
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353870"
---
# <a name="step-7-handle-window-messages"></a>Schritt 7. Fenster Meldungen behandeln

Überschreiben Sie die [**cbasepropertypage:: onreceivemess**](cbasepropertypage-onreceivemessage.md) -Methode, um die Dialogfeld Steuerelemente als Reaktion auf Benutzereingaben zu aktualisieren. Wenn Sie eine bestimmte Nachricht nicht verarbeiten, müssen Sie die Methode **onreceivemess** für die übergeordnete Klasse aufzurufen. Wenn der Benutzer eine Eigenschaft ändert, gehen Sie folgendermaßen vor:

-   Legen Sie die Variable **m \_ bdirty** der Eigenschaften Seite auf **true** fest.
-   Aufrufen der **ipropertypagesite:: OnStatusChange** -Methode des Eigenschaften Frames mit dem proppagestatus- \_ Flag "Dirty". Dieses Flag informiert den Eigenschaften Rahmen darüber, dass die Schaltfläche **anwenden** aktiviert werden soll. Der [**cbasepropertypage:: m \_ ppagesite**](cbasepropertypage-m-ppagesite.md) -Member enthält einen Zeiger auf die **ipropertypagesite** -Schnittstelle.

Um diesen Schritt zu vereinfachen, können Sie der Eigenschaften Seite die folgende Hilfsfunktion hinzufügen:


```C++
private:
    void SetDirty()
    {
        m_bDirty = TRUE;
        if (m_pPageSite)
        {
            m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
        }
    }
```



Diese private Methode wird in **onreceivemess** aufgerufen, wenn eine Benutzeraktion eine Eigenschaft ändert, wie im folgenden Beispiel gezeigt:


```C++
BOOL CGrayProp::OnReceiveMessage(HWND hwnd,
    UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_DEFAULT)
        {
            // User clicked the 'Revert to Default' button.
            m_lNewVal = SATURATION_DEFAULT;
            m_pGray->SetSaturation(m_lNewVal);

            // Update the slider control.
            SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1,
                m_lNewVal);
            SetDirty();
            return (LRESULT) 1;
        }
        break;

    case WM_HSCROLL:
        {
            // User moved the slider.
            switch(LOWORD(wParam))
            {
            case TB_PAGEDOWN:
            case SB_THUMBTRACK:
            case TB_PAGEUP:
                m_lNewVal = SendDlgItemMessage(m_Dlg, IDC_SLIDER1,
                    TBM_GETPOS, 0, 0);
                m_pGray->SetSaturation(m_lNewVal);
                SetDirty();
            }
            return (LRESULT) 1;
        }
    } // Switch.
    
    // Let the parent class handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd,uMsg,wParam,lParam);
} 
```



Die Eigenschaften Seite in diesem Beispiel verfügt über zwei Steuerelemente: einen Schieberegler und eine Schaltfläche " **auf Standard zurück** setzen". Wenn der Benutzer einen Bildlauf für den Schieberegler durchführt, legt die Eigenschaften Seite den Sättigungswert für den Filter fest. Wenn der Benutzer auf die Schaltfläche klickt, stellt die Eigenschaften Seite den Standard Sättigungswert des Filters wieder her. In jedem Fall enthält m \_ lnewval den aktuellen Wert, und m \_ LVAL enthält den ursprünglichen Wert. Der Wert von m \_ LVAL wird erst aktualisiert, wenn der Benutzer einen Commit für die Änderung ausführt. Dies geschieht, wenn der  Benutzer auf die Schaltfläche **OK** oder übernehmen im Eigenschaften Rahmen klickt.

Weiter: [Schritt 8. Anwenden von Eigenschafts Änderungen](step-8--apply-property-changes.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Filter Eigenschaften Seite](creating-a-filter-property-page.md)
</dt> </dl>

 

 



