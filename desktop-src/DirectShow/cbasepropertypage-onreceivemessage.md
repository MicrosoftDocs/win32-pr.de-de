---
description: Die onreceivemess-Methode wird aufgerufen, wenn das Dialogfeld eine Meldung empfängt.
ms.assetid: ea93500d-fd0f-4820-a54a-a186c40899ad
title: Cbasepropertypage. onreceivemess Age-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69d9da708d45524d15f735273d47f242104ee22f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373629"
---
# <a name="cbasepropertypageonreceivemessage-method"></a><span data-ttu-id="919c2-103">Cbasepropertypage. onreceivemess Age-Methode</span><span class="sxs-lookup"><span data-stu-id="919c2-103">CBasePropertyPage.OnReceiveMessage method</span></span>

<span data-ttu-id="919c2-104">Die- `OnReceiveMessage` Methode wird aufgerufen, wenn das Dialogfeld eine Meldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="919c2-104">The `OnReceiveMessage` method is called when the dialog box receives a message.</span></span>

## <a name="syntax"></a><span data-ttu-id="919c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="919c2-105">Syntax</span></span>


```C++
virtual INT_PTR OnReceiveMessage(
   HWND   hwnd,
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="919c2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="919c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="919c2-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="919c2-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="919c2-108">Handle für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="919c2-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="919c2-109">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="919c2-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="919c2-110">Message (Nachricht):</span><span class="sxs-lookup"><span data-stu-id="919c2-110">Message.</span></span>

</dd> <dt>

<span data-ttu-id="919c2-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="919c2-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="919c2-112">Der erste Message-Parameter.</span><span class="sxs-lookup"><span data-stu-id="919c2-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="919c2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="919c2-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="919c2-114">Der zweite Meldungs Parameter.</span><span class="sxs-lookup"><span data-stu-id="919c2-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="919c2-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="919c2-115">Return value</span></span>

<span data-ttu-id="919c2-116">Gibt einen booleschen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="919c2-116">Returns a Boolean value.</span></span> <span data-ttu-id="919c2-117">Die Dialogfeld Prozedur gibt diesen Wert zurück. Weitere Informationen finden Sie in der Platform SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="919c2-117">The dialog procedure returns this value; for more information, see the Platform SDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="919c2-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="919c2-118">Remarks</span></span>

<span data-ttu-id="919c2-119">Die Basisklassen Implementierung ruft **defwindowproc** auf.</span><span class="sxs-lookup"><span data-stu-id="919c2-119">The base-class implementation calls **DefWindowProc**.</span></span> <span data-ttu-id="919c2-120">Überschreiben Sie diese Methode, um Meldungen zu verarbeiten, die sich auf die Dialogfeld Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="919c2-120">Override this method to handle messages that relate to the dialog controls.</span></span> <span data-ttu-id="919c2-121">Wenn die über schreibende Methode eine bestimmte Nachricht nicht verarbeitet, sollte Sie die Basisklassen Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="919c2-121">If the overriding method does not handle a particular message, it should call the base-class method.</span></span>

<span data-ttu-id="919c2-122">Wenn der Benutzereigenschaften über die Dialogfeld Steuerelemente ändert, legen Sie das [**\_ bdirty-Flag "cbasepropertypage:: m**](cbasepropertypage-m-bdirty.md) " auf " **true**" fest.</span><span class="sxs-lookup"><span data-stu-id="919c2-122">If the user changes any properties via the dialog controls, set the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag to **TRUE**.</span></span> <span data-ttu-id="919c2-123">Anschließend können Sie die **ipropertypagesite:: OnStatusChange** -Methode auf dem [**cbasepropertypage:: m \_ ppagesite**](cbasepropertypage-m-ppagesite.md) -Zeiger aufrufen, um den Frame zu informieren.</span><span class="sxs-lookup"><span data-stu-id="919c2-123">Then call the **IPropertyPageSite::OnStatusChange** method on the [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) pointer to inform the frame.</span></span>

## <a name="examples"></a><span data-ttu-id="919c2-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="919c2-124">Examples</span></span>

<span data-ttu-id="919c2-125">Im folgenden Beispiel wird auf einen Klick auf eine Schaltfläche reagiert, indem eine Element Variable aktualisiert wird, die in der abgeleiteten Klasse definiert wird.</span><span class="sxs-lookup"><span data-stu-id="919c2-125">The following example responds to a button click by updating a member variable, which is assumed to be defined in the derived class.</span></span> <span data-ttu-id="919c2-126">Dieses Beispiel zeigt auch eine Hilfsfunktion zum Festlegen des Status "Dirty" der Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="919c2-126">This example also shows a helper function for setting the property page's dirty status.</span></span>


```C++
INT_PTR CMyProp::OnReceiveMessage(HWND hwnd,
  UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_BUTTON1)
        {
            m_lNewVal = GetDlgItemInt(m_Dlg, IDC_EDIT1, 0, TRUE);
            SetDirty();
            return (INT_PTR)TRUE;
        }
        break;
    } // switch

    // Did not handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd, uMsg, wParam, lParam);
}

// Helper function to update the dirty status.
void CMyProp::SetDirty()
{
    m_bDirty = TRUE;
    if (m_pPageSite)
    {
        m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
    }
}
```



## <a name="requirements"></a><span data-ttu-id="919c2-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="919c2-127">Requirements</span></span>



| <span data-ttu-id="919c2-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="919c2-128">Requirement</span></span> | <span data-ttu-id="919c2-129">Wert</span><span class="sxs-lookup"><span data-stu-id="919c2-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="919c2-130">Header</span><span class="sxs-lookup"><span data-stu-id="919c2-130">Header</span></span><br/>  | <dl> <span data-ttu-id="919c2-131"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="919c2-131"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="919c2-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="919c2-132">Library</span></span><br/> | <dl> <span data-ttu-id="919c2-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="919c2-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="919c2-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="919c2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="919c2-135">**Cbasepropertypage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="919c2-135">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




