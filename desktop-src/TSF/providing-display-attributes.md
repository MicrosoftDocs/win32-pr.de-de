---
title: Bereitstellen von Anzeige Attributen
description: Mit dem Text Services-Framework (TSF) kann ein Text Dienst Anzeige Attribute für Text bereitstellen.
ms.assetid: 5809f5b8-0396-4abd-b5fe-61ecc8cd0914
keywords:
- Text Dienst Framework (TSF), Attribute anzeigen
- TSF (Text Dienste-Framework), Anzeige Attribute
- Text Dienste, Anzeigen von Attributen
- Anzeigeattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08f59bb64ef4f06df020a40189d273c703768d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340829"
---
# <a name="providing-display-attributes"></a><span data-ttu-id="6fd9e-107">Bereitstellen von Anzeige Attributen</span><span class="sxs-lookup"><span data-stu-id="6fd9e-107">Providing Display Attributes</span></span>

<span data-ttu-id="6fd9e-108">Mit dem Text Services-Framework (TSF) kann ein Text Dienst Anzeige Attribute für Text bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-108">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="6fd9e-109">Dadurch kann dem Benutzer zusätzliches visuelles Feedback bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-109">This enables additional visual feedback to be supplied to the user.</span></span> <span data-ttu-id="6fd9e-110">Ein Rechtschreibprüfung-Text Dienst kann z. b. ein falsch geschriebenes Wort mit einer roten Unterstreichung markieren.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-110">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="6fd9e-111">Die angegebenen Anzeige Attribute werden durch die [tf \_ DisplayAttribute](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) -Struktur definiert und enthalten Textfarbe, Text Hintergrundfarbe, unterstrich Farbe, unterstrich Farbe und unterstrich Gewichtung.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-111">The display attributes provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="6fd9e-112">Clients, die diese Anzeige Attributinformationen verwenden, sind meist Anwendungen, können aber auch Text Dienste enthalten.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-112">Clients that use this display attribute information will most often be applications, but can also include text services.</span></span> <span data-ttu-id="6fd9e-113">Der TSF-Manager mediiert zwischen dem Anzeige Attribut Anbieter und dem Client und verfolgt den Anzeige Attribut Anbieter der spezifischen Anzeige Attribute nach.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-113">The TSF manager mediates between the display attribute provider and the client and tracks the display attribute provider of the specific display attributes.</span></span>

<span data-ttu-id="6fd9e-114">Zum Bereitstellen von Anzeige Attributen muss ein Text Dienst folgende Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-114">To provide display attributes, a text service must do the following.</span></span>

1.  <span data-ttu-id="6fd9e-115">Registrieren Sie den Text Dienst als Anzeige Attribut Anbieter durch Aufrufen von [itfcategorymgr:: registercategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) mit dem Klassen Bezeichner des Text Dienstanbieters für den ersten Parameter, GUID \_ tfcat \_ displayattributeprovider für den zweiten Parameter und der Klassen Bezeichner des Text Dienstanbieters für den dritten Parameter.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-115">Register the text service as a display attribute provider by calling [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) with the class identifier of the text service for the first parameter, GUID\_TFCAT\_DISPLAYATTRIBUTEPROVIDER for the second parameter and the class identifier of the text service again for the third parameter.</span></span>
2.  <span data-ttu-id="6fd9e-116">Implementieren Sie [ITF displayattributeprovider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) , und stellen Sie Sie aus der Klassenfactory zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-116">Implement [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) and make it available from the class factory.</span></span>
3.  <span data-ttu-id="6fd9e-117">Implementieren Sie [ienumtfdisplayattributeinfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) , und stellen Sie Sie über [ITF displayattributeprovider:: enumdisplayattributeinfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-117">Implement [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) and make it available from [ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).</span></span>
4.  <span data-ttu-id="6fd9e-118">Implementieren Sie ein [ITF displayattributeinfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) -Objekt für jeden Typ von Anzeige Attribut, den der Text Dienst bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-118">Implement an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for each type of display attribute that the text service provides.</span></span>

## <a name="applying-the-display-attributes"></a><span data-ttu-id="6fd9e-119">Anwenden der Anzeige Attribute</span><span class="sxs-lookup"><span data-stu-id="6fd9e-119">Applying the Display Attributes</span></span>

<span data-ttu-id="6fd9e-120">Der Text Dienst muss das Anzeige Attribut auf einen Textbereich anwenden.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-120">The text service must apply the display attribute to a range of text.</span></span> <span data-ttu-id="6fd9e-121">Ein Text Dienst kann den Eigenschafts Wert nur während einer Sitzung mit Lese-/schreibbearbeitung ändern.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-121">A text service can only modify the property value during a read/write edit session.</span></span>

<span data-ttu-id="6fd9e-122">Wenn dies in einer Sitzung mit Lese-/schreibbearbeitung erfolgt, wird ein Anzeige Attribut wie folgt angewendet.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-122">Assuming this is within a read/write edit session, a display attribute is applied in the following manner.</span></span>

1.  <span data-ttu-id="6fd9e-123">Rufen Sie ein [itfrange](/windows/desktop/api/Msctf/nn-msctf-itfrange) -Objekt ab, das den Text abdeckt, auf den das Anzeige Attribut angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-123">Obtain an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) object that covers the text that the display attribute will be applied to.</span></span>
2.  <span data-ttu-id="6fd9e-124">Rufen Sie ein [itfproperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) -Objekt für die Text Attribute ab, indem Sie [ITfContext:: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) mit dem GUID- \_ Prop-Attribut aufrufen \_ .</span><span class="sxs-lookup"><span data-stu-id="6fd9e-124">Obtain an [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) object for the text attributes by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) with GUID\_PROP\_ATTRIBUTE.</span></span>
3.  <span data-ttu-id="6fd9e-125">Erstellen Sie ein [tfguidatom](tfguidatom.md) aus der durch den Text Dienst definierten **GUID** des Anzeige Attribut Bezeichners durch Aufrufen von [itfcategorymgr:: registerguid](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span><span class="sxs-lookup"><span data-stu-id="6fd9e-125">Create a [TfGuidAtom](tfguidatom.md) from the text service-defined display attribute identifier **GUID** by calling [ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span></span>
4.  <span data-ttu-id="6fd9e-126">Initialisieren Sie eine Variant-Variable zu VT \_ I4, und legen Sie den **LVAL** -Member auf das im vorherigen Schritt erstellte **tfguidatom** fest.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-126">Initialize a VARIANT variable to VT\_I4 and set the **lVal** member to the **TfGuidAtom** created in the previous step.</span></span>
5.  <span data-ttu-id="6fd9e-127">Wenden Sie das Anzeige Attribut auf den Bereich an, indem Sie [itfproperty:: SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) mit dem Cookie für die Lese-/schreibbearbeitung aufrufen, den Bereich und die Variante, die im vorherigen Schritt initialisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-127">Apply the display attribute to the range by calling [ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) with the read/write edit cookie, the range and the VARIANT initialized in the previous step.</span></span>


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



## <a name="supplying-the-display-attribute-information-object"></a><span data-ttu-id="6fd9e-128">Bereitstellen des Anzeige Attribut Informationsobjekts</span><span class="sxs-lookup"><span data-stu-id="6fd9e-128">Supplying the Display Attribute Information Object</span></span>

<span data-ttu-id="6fd9e-129">Ein Client erhält ein **ITF displayattributeinfo** -Objekt auf zwei Arten.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-129">A client obtains an **ITfDisplayAttributeInfo** object in one of two ways.</span></span>

1.  <span data-ttu-id="6fd9e-130">Der Client ruft [ITF displayattributemgr:: getdisplayattributeinfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) mit dem **GUID** -Bezeichner des Anzeige Attributs auf.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-130">The client calls [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) with the **GUID** identifier of the display attribute.</span></span> <span data-ttu-id="6fd9e-131">Wenn der Client zum ersten Mal **itfdisplayattributemgr:: getdisplayattributeinfo** aufruft, erstellt der TSF-Manager eine Instanz des Anzeige Attribut Anbieters durch Aufrufen von CoCreateInstance mit dem Klassen Bezeichner, der als erster Parameter an **itfcategorymgr:: registercategory** übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-131">The first time the client calls **ITfDisplayAttributeMgr::GetDisplayAttributeInfo**, the TSF manager will create an instance of the display attribute provider by calling CoCreateInstance with the class identifier passed as the first parameter to **ITfCategoryMgr::RegisterCategory**.</span></span> <span data-ttu-id="6fd9e-132">Bei nachfolgenden Aufrufen von **itfdisplayattributemgr:: getdisplayattributeinfo** wird das Display Attribute Provider-Objekt wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-132">Subsequent calls to **ITfDisplayAttributeMgr::GetDisplayAttributeInfo** will reuse the display attribute provider object.</span></span>

    <span data-ttu-id="6fd9e-133">Der TSF-Manager ruft dann [itfdisplayattributeprovider:: getdisplayattributeinfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) mit dem Display-Attribut **GUID** auf, um das **itfdisplayattributeinfo** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-133">The TSF manager then calls [ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) with the display attribute **GUID** to obtain the **ITfDisplayAttributeInfo** object.</span></span>

    <span data-ttu-id="6fd9e-134">Der TSF-Manager übergibt dann das **itfdisplayattributeinfo** -Objekt an den Client zurück.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-134">The TSF manager then passes the **ITfDisplayAttributeInfo** object back to the client.</span></span>

2.  <span data-ttu-id="6fd9e-135">Der Client ruft [itfdisplayattributemgr:: enumdisplayattributeinfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) auf, um ein **ienumtfdisplayattributeinfo** -Objekt zu erhalten, das alle Anzeige Attribute enthält, die von allen Anzeige Attribut Anbietern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-135">The client calls [ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by all of the display attribute providers.</span></span> <span data-ttu-id="6fd9e-136">Der TSF-Manager listet jeden Anzeige Attribut Anbieter auf und erstellt eine Instanz jedes Anbieters durch Aufrufen von CoCreateInstance mit dem Klassen Bezeichner, der als dritter Parameter an **itfcategorymgr:: registercategory** übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-136">The TSF manager enumerates each display attribute provider and creates an instance of each provider by calling CoCreateInstance with the class identifier passed as the third parameter to **ITfCategoryMgr::RegisterCategory**.</span></span>

    <span data-ttu-id="6fd9e-137">Der TSF-Manager ruft dann den **itfdisplayattributeprovider:: enumdisplayattributeinfo** jedes Anbieters auf, um ein **ienumtfdisplayattributeinfo** -Objekt zu erhalten, das alle vom Anbieter bereitgestellten Anzeige Attribute enthält.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-137">The TSF manager then calls each provider's **ITfDisplayAttributeProvider::EnumDisplayAttributeInfo** to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by the provider.</span></span>

    <span data-ttu-id="6fd9e-138">Der TSF-Manager ruft dann die [ienumtfdisplayattributeinfo:: Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) -Methode des Anbieters auf und fügt jedes **itfdisplayattributeinfo** -Objekt hinzu, das dem eigenen Enumerator des Managers abgerufen wurde, bis das Ende der Enumeration des Anbieters erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-138">The TSF manager then calls the provider's [IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) method, adding each **ITfDisplayAttributeInfo** object obtained to the manager's own enumerator, until the end of the provider's enumeration is reached.</span></span>

    <span data-ttu-id="6fd9e-139">Wenn alle **itfdisplayattributeinfo** -Objekte für alle Anzeige Attribut Anbieter dem Enumerator von TSF-Manager hinzugefügt werden, gibt der Manager seinen Enumerator an den Client zurück.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-139">When all of the **ITfDisplayAttributeInfo** objects for all of the display attribute providers are added to the TSF manager's enumerator, the manager returns its enumerator to the client.</span></span> <span data-ttu-id="6fd9e-140">Der Client ruft dann **ienumtfdisplayattributeinfo:: Next** einmal oder mehrmals auf, um die **itfdisplayattributeinfo** -Objekte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6fd9e-140">The client then calls **IEnumTfDisplayAttributeInfo::Next** one or more times to obtain the **ITfDisplayAttributeInfo** objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fd9e-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6fd9e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fd9e-142">TF \_ DisplayAttribute</span><span class="sxs-lookup"><span data-stu-id="6fd9e-142">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="6fd9e-143">ITF categorymgr:: registercategory</span><span class="sxs-lookup"><span data-stu-id="6fd9e-143">ITfCategoryMgr::RegisterCategory</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[<span data-ttu-id="6fd9e-144">ITF displayattributeprovider</span><span class="sxs-lookup"><span data-stu-id="6fd9e-144">ITfDisplayAttributeProvider</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[<span data-ttu-id="6fd9e-145">Ienumtfdisplayattributeinfo</span><span class="sxs-lookup"><span data-stu-id="6fd9e-145">IEnumTfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="6fd9e-146">ITF displayattributeprovider:: enumdisplayattributeinfo</span><span class="sxs-lookup"><span data-stu-id="6fd9e-146">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="6fd9e-147">ITF displayattributeinfo</span><span class="sxs-lookup"><span data-stu-id="6fd9e-147">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="6fd9e-148">Itfrange</span><span class="sxs-lookup"><span data-stu-id="6fd9e-148">ITfRange</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[<span data-ttu-id="6fd9e-149">ITF Property</span><span class="sxs-lookup"><span data-stu-id="6fd9e-149">ITfProperty</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[<span data-ttu-id="6fd9e-150">ITF context:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="6fd9e-150">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="6fd9e-151">Tfguidatom</span><span class="sxs-lookup"><span data-stu-id="6fd9e-151">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="6fd9e-152">ITF categorymgr:: registerguid</span><span class="sxs-lookup"><span data-stu-id="6fd9e-152">ITfCategoryMgr::RegisterGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[<span data-ttu-id="6fd9e-153">ITF Property:: SetValue</span><span class="sxs-lookup"><span data-stu-id="6fd9e-153">ITfProperty::SetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[<span data-ttu-id="6fd9e-154">ITF displayattributemgr:: getdisplayattributeinfo</span><span class="sxs-lookup"><span data-stu-id="6fd9e-154">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="6fd9e-155">ITF displayattributeprovider:: getdisplayattributeinfo</span><span class="sxs-lookup"><span data-stu-id="6fd9e-155">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="6fd9e-156">ITF displayattributemgr:: enumdisplayattributeinfo</span><span class="sxs-lookup"><span data-stu-id="6fd9e-156">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="6fd9e-157">Ienumtfdisplayattributeinfo</span><span class="sxs-lookup"><span data-stu-id="6fd9e-157">IEnumTfDisplayAttributeInfo</span></span> 
</dt> <dt>

 <span data-ttu-id="6fd9e-158">ITF displayattributeprovider:: enumdisplayattributeinfo</span><span class="sxs-lookup"><span data-stu-id="6fd9e-158">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span> 
</dt> <dt>

[<span data-ttu-id="6fd9e-159">Ienumtfdisplayattributeinfo:: Next</span><span class="sxs-lookup"><span data-stu-id="6fd9e-159">IEnumTfDisplayAttributeInfo::Next</span></span>](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 




