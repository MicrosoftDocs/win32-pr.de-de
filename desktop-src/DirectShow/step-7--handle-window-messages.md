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
# <a name="step-7-handle-window-messages"></a><span data-ttu-id="00171-104">Schritt 7.</span><span class="sxs-lookup"><span data-stu-id="00171-104">Step 7.</span></span> <span data-ttu-id="00171-105">Fenster Meldungen behandeln</span><span class="sxs-lookup"><span data-stu-id="00171-105">Handle Window Messages</span></span>

<span data-ttu-id="00171-106">Überschreiben Sie die [**cbasepropertypage:: onreceivemess**](cbasepropertypage-onreceivemessage.md) -Methode, um die Dialogfeld Steuerelemente als Reaktion auf Benutzereingaben zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="00171-106">Override the [**CBasePropertyPage::OnReceiveMessage**](cbasepropertypage-onreceivemessage.md) method to update the dialog controls in response to user input.</span></span> <span data-ttu-id="00171-107">Wenn Sie eine bestimmte Nachricht nicht verarbeiten, müssen Sie die Methode **onreceivemess** für die übergeordnete Klasse aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="00171-107">If you don't handle a particular message, call the **OnReceiveMessage** method on the parent class.</span></span> <span data-ttu-id="00171-108">Wenn der Benutzer eine Eigenschaft ändert, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="00171-108">Whenever the user changes a property, do the following:</span></span>

-   <span data-ttu-id="00171-109">Legen Sie die Variable **m \_ bdirty** der Eigenschaften Seite auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="00171-109">Set the **m\_bDirty** variable of the property page to **TRUE**.</span></span>
-   <span data-ttu-id="00171-110">Aufrufen der **ipropertypagesite:: OnStatusChange** -Methode des Eigenschaften Frames mit dem proppagestatus- \_ Flag "Dirty".</span><span class="sxs-lookup"><span data-stu-id="00171-110">Call the **IPropertyPageSite::OnStatusChange** method of the property frame with the PROPPAGESTATUS\_DIRTY flag.</span></span> <span data-ttu-id="00171-111">Dieses Flag informiert den Eigenschaften Rahmen darüber, dass die Schaltfläche **anwenden** aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="00171-111">This flag informs the property frame that it should enable the **Apply** button.</span></span> <span data-ttu-id="00171-112">Der [**cbasepropertypage:: m \_ ppagesite**](cbasepropertypage-m-ppagesite.md) -Member enthält einen Zeiger auf die **ipropertypagesite** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="00171-112">The [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) member holds a pointer to the **IPropertyPageSite** interface.</span></span>

<span data-ttu-id="00171-113">Um diesen Schritt zu vereinfachen, können Sie der Eigenschaften Seite die folgende Hilfsfunktion hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="00171-113">To simplify this step, you can add the following helper function to your property page:</span></span>


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



<span data-ttu-id="00171-114">Diese private Methode wird in **onreceivemess** aufgerufen, wenn eine Benutzeraktion eine Eigenschaft ändert, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="00171-114">Call this private method inside **OnReceiveMessage** whenever a user action changes a property, as shown in the following example:</span></span>


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



<span data-ttu-id="00171-115">Die Eigenschaften Seite in diesem Beispiel verfügt über zwei Steuerelemente: einen Schieberegler und eine Schaltfläche " **auf Standard zurück** setzen".</span><span class="sxs-lookup"><span data-stu-id="00171-115">The property page in this example has two controls, a slider bar and a **Revert to Default** button.</span></span> <span data-ttu-id="00171-116">Wenn der Benutzer einen Bildlauf für den Schieberegler durchführt, legt die Eigenschaften Seite den Sättigungswert für den Filter fest.</span><span class="sxs-lookup"><span data-stu-id="00171-116">If the user scrolls the slider bar, the property page sets the saturation value on the filter.</span></span> <span data-ttu-id="00171-117">Wenn der Benutzer auf die Schaltfläche klickt, stellt die Eigenschaften Seite den Standard Sättigungswert des Filters wieder her.</span><span class="sxs-lookup"><span data-stu-id="00171-117">If the user clicks the button, the property page restores the filter's default saturation value.</span></span> <span data-ttu-id="00171-118">In jedem Fall enthält m \_ lnewval den aktuellen Wert, und m \_ LVAL enthält den ursprünglichen Wert.</span><span class="sxs-lookup"><span data-stu-id="00171-118">In each case, m\_lNewVal holds the current value and m\_lVal holds the original value.</span></span> <span data-ttu-id="00171-119">Der Wert von m \_ LVAL wird erst aktualisiert, wenn der Benutzer einen Commit für die Änderung ausführt. Dies geschieht, wenn der  Benutzer auf die Schaltfläche **OK** oder übernehmen im Eigenschaften Rahmen klickt.</span><span class="sxs-lookup"><span data-stu-id="00171-119">The value of m\_lVal is not updated until the user commits the change, which happens when the user clicks the **OK** or **Apply** button on the property frame.</span></span>

<span data-ttu-id="00171-120">Weiter: [Schritt 8. Anwenden von Eigenschafts Änderungen](step-8--apply-property-changes.md).</span><span class="sxs-lookup"><span data-stu-id="00171-120">Next: [Step 8. Apply Property Changes](step-8--apply-property-changes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00171-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00171-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00171-122">Erstellen einer Filter Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="00171-122">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



