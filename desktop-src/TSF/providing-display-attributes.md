---
title: Bereitstellen von Anzeigeattributen
description: Erfahren Sie, wie Sie Anzeigeattribute bereitstellen. Textdienstframework (TSF) ermöglicht einem Textdienst das Bereitstellen von Anzeigeattributen für Text.
ms.assetid: 5809f5b8-0396-4abd-b5fe-61ecc8cd0914
keywords:
- Textdienstframework (TSF), Anzeigen von Attributen
- TSF (Textdienstframework), Anzeigeattribute
- Textdienste,Anzeigeattribute
- Anzeigeattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780cc191e39d5b1d0c3329bab87af5267e4a6c73
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406113"
---
# <a name="providing-display-attributes"></a><span data-ttu-id="8a48e-108">Bereitstellen von Anzeigeattributen</span><span class="sxs-lookup"><span data-stu-id="8a48e-108">Providing Display Attributes</span></span>

<span data-ttu-id="8a48e-109">Textdienstframework (TSF) ermöglicht einem Textdienst das Bereitstellen von Anzeigeattributen für Text.</span><span class="sxs-lookup"><span data-stu-id="8a48e-109">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="8a48e-110">Dadurch kann dem Benutzer zusätzliches visuelles Feedback bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8a48e-110">This enables additional visual feedback to be supplied to the user.</span></span> <span data-ttu-id="8a48e-111">Beispielsweise kann ein Textdienst für die Rechtschreibprüfung ein falsch geschriebenes Wort mit einer roten Unterstreichung hervorheben.</span><span class="sxs-lookup"><span data-stu-id="8a48e-111">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="8a48e-112">Die bereitgestellten Anzeigeattribute werden durch die [TF \_ DISPLAYATTRIBUTE-Struktur](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) definiert und umfassen Textfarbe, Hintergrundfarbe des Texts, Unterstreichungsstil, Unterstreichungsfarbe und Unterstreichungsgewichtung.</span><span class="sxs-lookup"><span data-stu-id="8a48e-112">The display attributes provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="8a48e-113">Clients, die diese Anzeigeattributinformationen verwenden, sind am häufigsten Anwendungen, können aber auch Textdienste enthalten.</span><span class="sxs-lookup"><span data-stu-id="8a48e-113">Clients that use this display attribute information will most often be applications, but can also include text services.</span></span> <span data-ttu-id="8a48e-114">Der TSF-Manager vermittelt zwischen dem Anzeigeattributanbieter und dem Client und verfolgt den Anzeigeattributanbieter der spezifischen Anzeigeattribute nach.</span><span class="sxs-lookup"><span data-stu-id="8a48e-114">The TSF manager mediates between the display attribute provider and the client and tracks the display attribute provider of the specific display attributes.</span></span>

<span data-ttu-id="8a48e-115">Um Anzeigeattribute bereitstellen zu können, muss ein Textdienst Folgendes tun.</span><span class="sxs-lookup"><span data-stu-id="8a48e-115">To provide display attributes, a text service must do the following.</span></span>

1.  <span data-ttu-id="8a48e-116">Registrieren Sie den Textdienst als Anzeigeattributanbieter, indem Sie [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) mit dem Klassenbezeichner des Textdiensts für den ersten Parameter, GUID \_ TFCAT DISPLAYATTRIBUTEPROVIDER für den zweiten Parameter und dem Klassenbezeichner des Textdiensts erneut für den dritten Parameter \_ aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8a48e-116">Register the text service as a display attribute provider by calling [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) with the class identifier of the text service for the first parameter, GUID\_TFCAT\_DISPLAYATTRIBUTEPROVIDER for the second parameter and the class identifier of the text service again for the third parameter.</span></span>
2.  <span data-ttu-id="8a48e-117">Implementieren [Sie ITfDisplayAttributeProvider,](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) und stellen Sie es über die Klassen factory zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="8a48e-117">Implement [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) and make it available from the class factory.</span></span>
3.  <span data-ttu-id="8a48e-118">Implementieren [Sie IEnumTfDisplayAttributeInfo,](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) und stellen Sie es über [ITfDisplayAttributeProvider::EnumDisplayAttributeInfo zur Verfügung.](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)</span><span class="sxs-lookup"><span data-stu-id="8a48e-118">Implement [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) and make it available from [ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).</span></span>
4.  <span data-ttu-id="8a48e-119">Implementieren Sie [ein ITfDisplayAttributeInfo-Objekt](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) für jeden Vom Textdienst bereitgestellten Anzeigeattributtyp.</span><span class="sxs-lookup"><span data-stu-id="8a48e-119">Implement an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for each type of display attribute that the text service provides.</span></span>

## <a name="applying-the-display-attributes"></a><span data-ttu-id="8a48e-120">Anwenden der Anzeigeattribute</span><span class="sxs-lookup"><span data-stu-id="8a48e-120">Applying the Display Attributes</span></span>

<span data-ttu-id="8a48e-121">Der Textdienst muss das Anzeigeattribut auf einen Textbereich anwenden.</span><span class="sxs-lookup"><span data-stu-id="8a48e-121">The text service must apply the display attribute to a range of text.</span></span> <span data-ttu-id="8a48e-122">Ein Textdienst kann den Eigenschaftswert nur während einer Lese-/Schreibbearbeitungssitzung ändern.</span><span class="sxs-lookup"><span data-stu-id="8a48e-122">A text service can only modify the property value during a read/write edit session.</span></span>

<span data-ttu-id="8a48e-123">Wenn dies innerhalb einer Lese-/Schreibbearbeitungssitzung erfolgt, wird ein Anzeigeattribut wie folgt angewendet.</span><span class="sxs-lookup"><span data-stu-id="8a48e-123">Assuming this is within a read/write edit session, a display attribute is applied in the following manner.</span></span>

1.  <span data-ttu-id="8a48e-124">Abrufen eines [ITfRange-Objekts,](/windows/desktop/api/Msctf/nn-msctf-itfrange) das den Text abdeckt, auf den das Anzeigeattribut angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8a48e-124">Obtain an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) object that covers the text that the display attribute will be applied to.</span></span>
2.  <span data-ttu-id="8a48e-125">Rufen Sie [ein ITfProperty-Objekt](/windows/desktop/api/Msctf/nn-msctf-itfproperty) für die Textattribute ab, indem [Sie ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) mit GUID \_ PROP ATTRIBUTE \_ aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8a48e-125">Obtain an [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) object for the text attributes by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) with GUID\_PROP\_ATTRIBUTE.</span></span>
3.  <span data-ttu-id="8a48e-126">Erstellen Sie ein [TfGuidAtom-Attribut](tfguidatom.md) aus der vom Textdienst definierten Anzeigeattributbezeichner-GUID, indem [Sie ITfCategoryMgr::RegisterGUID aufrufen.](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid) </span><span class="sxs-lookup"><span data-stu-id="8a48e-126">Create a [TfGuidAtom](tfguidatom.md) from the text service-defined display attribute identifier **GUID** by calling [ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span></span>
4.  <span data-ttu-id="8a48e-127">Initialisieren Sie eine VARIANT-Variable mit VT I4, und legen Sie den lVal-Member auf das \_ **tfGuidAtom** fest, das im vorherigen Schritt erstellt wurde. </span><span class="sxs-lookup"><span data-stu-id="8a48e-127">Initialize a VARIANT variable to VT\_I4 and set the **lVal** member to the **TfGuidAtom** created in the previous step.</span></span>
5.  <span data-ttu-id="8a48e-128">Wenden Sie das Anzeigeattribut auf den Bereich an, indem [Sie ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) mit dem Lese-/Schreibbearbeitungscookie, dem Bereich und dem VARIANT aufrufen, die im vorherigen Schritt initialisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="8a48e-128">Apply the display attribute to the range by calling [ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) with the read/write edit cookie, the range and the VARIANT initialized in the previous step.</span></span>


```C++
STDAPI CEditSession::DoEditSession(TfEditCookie ec)
{
    HRESULT hr;
    ITfCategoryMgr *pCategoryMgr;
    TfGuidAtom  gaDisplayAttribute = TF_INVALID_GUIDATOM;

    //Create a TfGuidAtom for the display attribute identifier. 
    hr = CoCreateInstance(CLSID_TF_CategoryMgr,
                         NULL, 
                         CLSCTX_INPROC_SERVER, 
                         IID_ITfCategoryMgr, 
                         (void**)&pCategoryMgr);
    
    if(SUCCEEDED(hr))
    {
        hr = pCategoryMgr->RegisterGUID(guidDisplayAttribute, &gaDisplayAttribute);

        pCategoryMgr->Release();
    }
    
    //Apply the display attribute to the selected text. 
    if(TF_INVALID_GUIDATOM != gaDisplayAttribute)
    {
        TF_SELECTION tfSel;
        ULONG cFetched;

        //Get the selection. 
        hr = m_pContext->GetSelection(ec, TF_DEFAULT_SELECTION, 1, &tfSel, &cFetched);
        if(SUCCEEDED(hr) && cFetched)
        {
            ITfProperty *pDisplayAttributeProperty;

            //Get the display attribute property. 
            hr = m_pContext->GetProperty(GUID_PROP_ATTRIBUTE, &pDisplayAttributeProperty);
            if(SUCCEEDED(hr))
            {
                VARIANT var;

                VariantInit(&var);

                //All display attributes are TfGuidAtoms and TfGuidAtoms are VT_I4. 
                var.vt = VT_I4; 
                var.lVal = gaDisplayAttribute;

                //Set the display attribute value over the range. 
                hr = pDisplayAttributeProperty->SetValue(ec, tfSel.range, &var);

                pDisplayAttributeProperty->Release();
            }

            tfSel.range->Release();
        }
    }

    return S_OK;
}
```



## <a name="supplying-the-display-attribute-information-object"></a><span data-ttu-id="8a48e-129">Angeben des Anzeigeattributinformationsobjekts</span><span class="sxs-lookup"><span data-stu-id="8a48e-129">Supplying the Display Attribute Information Object</span></span>

<span data-ttu-id="8a48e-130">Ein Client erhält ein **ITfDisplayAttributeInfo-Objekt** auf zwei Arten.</span><span class="sxs-lookup"><span data-stu-id="8a48e-130">A client obtains an **ITfDisplayAttributeInfo** object in one of two ways.</span></span>

1.  <span data-ttu-id="8a48e-131">Der Client ruft [ITfDisplayAttributeMgr::GetDisplayAttributeInfo mit](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) dem **GUID-Bezeichner** des Anzeigeattributs auf.</span><span class="sxs-lookup"><span data-stu-id="8a48e-131">The client calls [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) with the **GUID** identifier of the display attribute.</span></span> <span data-ttu-id="8a48e-132">Wenn der Client **ITfDisplayAttributeMgr::GetDisplayAttributeInfo** zum ersten Mal aufruft, erstellt der TSF-Manager eine Instanz des Anzeigeattributanbieters, indem er CoCreateInstance mit dem Klassenbezeichner aufruft, der als erster Parameter **an ITfCategoryMgr::RegisterCategory übergeben wird.**</span><span class="sxs-lookup"><span data-stu-id="8a48e-132">The first time the client calls **ITfDisplayAttributeMgr::GetDisplayAttributeInfo**, the TSF manager will create an instance of the display attribute provider by calling CoCreateInstance with the class identifier passed as the first parameter to **ITfCategoryMgr::RegisterCategory**.</span></span> <span data-ttu-id="8a48e-133">Nachfolgende Aufrufe von **ITfDisplayAttributeMgr::GetDisplayAttributeInfo** verwenden das Anzeigeattributanbieterobjekt erneut.</span><span class="sxs-lookup"><span data-stu-id="8a48e-133">Subsequent calls to **ITfDisplayAttributeMgr::GetDisplayAttributeInfo** will reuse the display attribute provider object.</span></span>

    <span data-ttu-id="8a48e-134">Der TSF-Manager ruft dann [ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) mit dem Anzeigeattribut **GUID** auf, um das **ITfDisplayAttributeInfo-Objekt zu** erhalten.</span><span class="sxs-lookup"><span data-stu-id="8a48e-134">The TSF manager then calls [ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) with the display attribute **GUID** to obtain the **ITfDisplayAttributeInfo** object.</span></span>

    <span data-ttu-id="8a48e-135">Der TSF-Manager übergibt dann das **ITfDisplayAttributeInfo-Objekt** zurück an den Client.</span><span class="sxs-lookup"><span data-stu-id="8a48e-135">The TSF manager then passes the **ITfDisplayAttributeInfo** object back to the client.</span></span>

2.  <span data-ttu-id="8a48e-136">Der Client ruft [ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) auf, um ein **IEnumTfDisplayAttributeInfo-Objekt** zu erhalten, das alle Anzeigeattribute enthält, die von allen Anzeigeattributanbietern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8a48e-136">The client calls [ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by all of the display attribute providers.</span></span> <span data-ttu-id="8a48e-137">Der TSF-Manager führt jeden Anzeigeattributanbieter auf und erstellt eine Instanz jedes Anbieters, indem er CoCreateInstance mit dem Klassenbezeichner aufruft, der als dritter Parameter an **ITfCategoryMgr::RegisterCategory** übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="8a48e-137">The TSF manager enumerates each display attribute provider and creates an instance of each provider by calling CoCreateInstance with the class identifier passed as the third parameter to **ITfCategoryMgr::RegisterCategory**.</span></span>

    <span data-ttu-id="8a48e-138">Der TSF-Manager ruft dann den **ITfDisplayAttributeProvider::EnumDisplayAttributeInfo** jedes Anbieters auf, um ein **IEnumTfDisplayAttributeInfo-Objekt** zu erhalten, das alle vom Anbieter bereitgestellten Anzeigeattribute enthält.</span><span class="sxs-lookup"><span data-stu-id="8a48e-138">The TSF manager then calls each provider's **ITfDisplayAttributeProvider::EnumDisplayAttributeInfo** to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by the provider.</span></span>

    <span data-ttu-id="8a48e-139">Der TSF-Manager ruft dann die [IEnumTfDisplayAttributeInfo::Next-Methode](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) des Anbieters auf und fügt jedes **ITfDisplayAttributeInfo-Objekt** hinzu, das dem eigenen Enumerator des Managers abgerufen wurde, bis das Ende der Anbieterenumeration erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="8a48e-139">The TSF manager then calls the provider's [IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) method, adding each **ITfDisplayAttributeInfo** object obtained to the manager's own enumerator, until the end of the provider's enumeration is reached.</span></span>

    <span data-ttu-id="8a48e-140">Wenn alle **ITfDisplayAttributeInfo-Objekte** für alle Anzeigeattributanbieter dem Enumerator des TSF-Managers hinzugefügt werden, gibt der Manager seinen Enumerator an den Client zurück.</span><span class="sxs-lookup"><span data-stu-id="8a48e-140">When all of the **ITfDisplayAttributeInfo** objects for all of the display attribute providers are added to the TSF manager's enumerator, the manager returns its enumerator to the client.</span></span> <span data-ttu-id="8a48e-141">Der Client ruft dann **mindestens einmal IEnumTfDisplayAttributeInfo::Next** auf, um die **ITfDisplayAttributeInfo-Objekte zu** erhalten.</span><span class="sxs-lookup"><span data-stu-id="8a48e-141">The client then calls **IEnumTfDisplayAttributeInfo::Next** one or more times to obtain the **ITfDisplayAttributeInfo** objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a48e-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8a48e-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a48e-143">TF \_ DISPLAYATTRIBUTE</span><span class="sxs-lookup"><span data-stu-id="8a48e-143">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="8a48e-144">ITfCategoryMgr::RegisterCategory</span><span class="sxs-lookup"><span data-stu-id="8a48e-144">ITfCategoryMgr::RegisterCategory</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[<span data-ttu-id="8a48e-145">ITfDisplayAttributeProvider</span><span class="sxs-lookup"><span data-stu-id="8a48e-145">ITfDisplayAttributeProvider</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[<span data-ttu-id="8a48e-146">IEnumTfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="8a48e-146">IEnumTfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="8a48e-147">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="8a48e-147">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="8a48e-148">ITfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="8a48e-148">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="8a48e-149">ITfRange</span><span class="sxs-lookup"><span data-stu-id="8a48e-149">ITfRange</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[<span data-ttu-id="8a48e-150">ITfProperty</span><span class="sxs-lookup"><span data-stu-id="8a48e-150">ITfProperty</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[<span data-ttu-id="8a48e-151">ITfContext::GetProperty</span><span class="sxs-lookup"><span data-stu-id="8a48e-151">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="8a48e-152">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="8a48e-152">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="8a48e-153">ITfCategoryMgr::RegisterGUID</span><span class="sxs-lookup"><span data-stu-id="8a48e-153">ITfCategoryMgr::RegisterGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[<span data-ttu-id="8a48e-154">ITfProperty::SetValue</span><span class="sxs-lookup"><span data-stu-id="8a48e-154">ITfProperty::SetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[<span data-ttu-id="8a48e-155">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="8a48e-155">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="8a48e-156">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="8a48e-156">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="8a48e-157">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="8a48e-157">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="8a48e-158">IEnumTfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="8a48e-158">IEnumTfDisplayAttributeInfo</span></span> 
</dt> <dt>

 <span data-ttu-id="8a48e-159">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="8a48e-159">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span> 
</dt> <dt>

[<span data-ttu-id="8a48e-160">IEnumTfDisplayAttributeInfo::Next</span><span class="sxs-lookup"><span data-stu-id="8a48e-160">IEnumTfDisplayAttributeInfo::Next</span></span>](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 




