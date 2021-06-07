---
title: Eigenschaften (Allgemeine Elemente)
description: Textdienstframework (TSF) stellt Eigenschaften bereit, die Metadaten einem Textbereich zuordnen.
ms.assetid: d1d0dd99-f303-4355-9835-917de9491a0b
keywords:
- Textdienstframework (TSF), Eigenschaften
- TSF (Textdienstframework),Properties
- Textdienste,Eigenschaften
- TSF-fähige Anwendungen,Eigenschaften
- properties
- Textdienstframework (TSF), Eigenschaftentypen
- TSF (Textdienstframework),Eigenschaftentypen
- Textdienste,Eigenschaftentypen
- TSF-fähige Anwendungen,Eigenschaftentypen
- Eigenschaftentypen
- Textdienstframework (TSF), beständige Speicherung von Eigenschaften
- TSF (Textdienstframework), persistente Speicherung von Eigenschaften
- Textdienste,persistente Speicherung von Eigenschaften
- TSF-fähige Anwendungen, beständige Speicherung von Eigenschaften
- Persistente Speicherung von Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b94a1f6c504fcd3e6491af9e66b399d59a3eeb
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524214"
---
# <a name="properties-common-elements"></a><span data-ttu-id="7c2b3-118">Eigenschaften (Allgemeine Elemente)</span><span class="sxs-lookup"><span data-stu-id="7c2b3-118">Properties (Common Elements)</span></span>

<span data-ttu-id="7c2b3-119">Textdienstframework (TSF) stellt Eigenschaften bereit, die Metadaten einem Textbereich zuordnen.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-119">Text Services Framework (TSF) provides properties that associate metadata with a range of text.</span></span> <span data-ttu-id="7c2b3-120">Zu diesen Eigenschaften zählen u. a. Anzeigeattribute wie fett formatierten Text, der Sprachbezeichner des Texts und rohe Daten, die von einem Textdienst bereitgestellt werden, z. B. die Audiodaten, die dem Text aus dem Sprachtextdienst zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-120">These properties include, but are not limited to, display attributes such as bold text, the language identifier of the text, and raw data provided by a text service such as the audio data associated with text from the speech text service.</span></span>

<span data-ttu-id="7c2b3-121">Im folgenden Beispiel wird veranschaulicht, wie eine hypothetische Textfarbeigenschaft mit möglichen Werten von Rot (R), Grün (G) oder Blau (B) angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-121">The following example demonstrates how a hypothetical text color property with possible values of red (R), green (G), or blue (B) can be viewed.</span></span>


```C++
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="7c2b3-122">Eigenschaften verschiedener Typen können sich überlappen.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-122">Properties of different types can overlap.</span></span> <span data-ttu-id="7c2b3-123">Nehmen Sie beispielsweise das vorherige Beispiel, und fügen Sie ein Textattribut hinzu, das entweder fett (B) oder italisch (I) sein kann.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-123">For example, take the previous example and add a text attribute that can be either bold (B) or italic (I).</span></span>


```C++
ATTRIB:BBBBBBB      IIIIIIIIIIII
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="7c2b3-124">Der Text "this" wäre fett, "is" wäre sowohl fett als auch rot, "some" würde normal angezeigt, "colored" wäre grün und italicized und "text" wäre italicized.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-124">The text "this" would be bold, "is" would be both bold and red, "some" would be displayed normally, "colored" would be green and italicized and "text" would be italicized.</span></span>

<span data-ttu-id="7c2b3-125">Eigenschaften desselben Typs dürfen sich nicht überlappen.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-125">Properties of the same type cannot overlap.</span></span> <span data-ttu-id="7c2b3-126">Die folgende Situation ist beispielsweise nicht zulässig, da "is" und "colored" überlappende Werte der gleichen Typen haben.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-126">For example, the following situation is not allowed because "is" and "colored" have overlapping values of the same types.</span></span>


```C++
COLOR: GGG GGGG RRR BBBBGGG     
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



## <a name="property-types"></a><span data-ttu-id="7c2b3-127">Eigenschaftentypen</span><span class="sxs-lookup"><span data-stu-id="7c2b3-127">Property Types</span></span>

<span data-ttu-id="7c2b3-128">TSF definiert drei verschiedene Typen von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-128">TSF defines three different types of properties.</span></span>



|   <span data-ttu-id="7c2b3-129">Eigenschaftstyp</span><span class="sxs-lookup"><span data-stu-id="7c2b3-129">Property type</span></span>             |   <span data-ttu-id="7c2b3-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c2b3-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c2b3-131">statischen</span><span class="sxs-lookup"><span data-stu-id="7c2b3-131">Static</span></span>         | <span data-ttu-id="7c2b3-132">Ein statisches Eigenschaftenobjekt speichert die Eigenschaftsdaten mit Text.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-132">A static property object stores the property data with text.</span></span> <span data-ttu-id="7c2b3-133">Außerdem wird der Bereich der Textinformationen für jeden Bereich gespeichert, für den die Eigenschaft gilt.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-133">It also stores the range of text information for each range that the property applies to.</span></span> <span data-ttu-id="7c2b3-134">ITfReadOnlyProperty::GetType gibt die KATEGORIE GUID \_ TFCAT \_ PROPSTYLE \_ STATIC zurück.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-134">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATIC category.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="7c2b3-135">Static-Compact</span><span class="sxs-lookup"><span data-stu-id="7c2b3-135">Static-Compact</span></span> | <span data-ttu-id="7c2b3-136">Ein static-compact-Eigenschaftsobjekt ist mit einem statischen Eigenschaftsobjekt identisch, mit der Ausnahme, dass eine statisch-kompakte Eigenschaft keine Bereichsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-136">A static-compact property object is identical to a static property object except a static-compact property does not store range data.</span></span> <span data-ttu-id="7c2b3-137">Wenn der Bereich angefordert wird, der von einer statisch-kompakten Eigenschaft abgedeckt wird, wird ein Bereich für jede Gruppe benachbarter Eigenschaften erstellt.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-137">When the range covered by a static-compact property is requested, a range is created for each group of adjacent properties.</span></span> <span data-ttu-id="7c2b3-138">Statisch-kompakte Eigenschaften sind die effizienteste Möglichkeit, Eigenschaften pro Zeichen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-138">Static-compact properties are the most efficient way to store properties on a per-character basis.</span></span> <span data-ttu-id="7c2b3-139">ITfReadOnlyProperty::GetType gibt die KATEGORIE GUID \_ TFCAT \_ PROPSTYLE \_ STATICCOMPACT zurück.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-139">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATICCOMPACT category.</span></span> |
| <span data-ttu-id="7c2b3-140">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="7c2b3-140">Custom</span></span>         | <span data-ttu-id="7c2b3-141">Ein benutzerdefiniertes Eigenschaftenobjekt speichert die Bereichsinformationen für jeden Bereich, für den die Eigenschaft gilt.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-141">A custom property object stores the range information for each range that the property applies to.</span></span> <span data-ttu-id="7c2b3-142">Die tatsächlichen Daten für die Eigenschaft werden jedoch nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-142">It does not, however, store the actual data for the property.</span></span> <span data-ttu-id="7c2b3-143">Stattdessen speichert eine benutzerdefinierte Eigenschaft ein ITfPropertyStore-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-143">Instead, a custom property stores an ITfPropertyStore object.</span></span> <span data-ttu-id="7c2b3-144">Der TSF-Manager verwendet dieses Objekt, um auf die Eigenschaftendaten zu zugreifen und diese zu verwalten. ITfReadOnlyProperty::GetType gibt die KATEGORIE GUID \_ TFCAT \_ PROPSTYLE \_ CUSTOM zurück.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-144">The TSF manager uses this object to access and maintain the property data.ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_CUSTOM category.</span></span>                                                                    |



 

## <a name="working-with-properties"></a><span data-ttu-id="7c2b3-145">Arbeiten mit Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c2b3-145">Working with Properties</span></span>

<span data-ttu-id="7c2b3-146">Der Eigenschaftswert und die Attribute werden mithilfe der [ITfReadOnlyProperty-Schnittstelle](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) ermittelt und mithilfe der [ITfProperty-Schnittstelle](/windows/desktop/api/Msctf/nn-msctf-itfproperty) geändert.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-146">The property value and attributes are obtained using the [ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) interface and modified using the [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) interface.</span></span>

<span data-ttu-id="7c2b3-147">Wenn ein bestimmter Eigenschaftentyp erforderlich ist, wird [ITfContext::GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-147">If a specific property type is required, then [ITfContext::GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) is used.</span></span> <span data-ttu-id="7c2b3-148">**ITfContext::GetProperty** erfordert eine **GUID,** die die zu erhaltende Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-148">**ITfContext::GetProperty** requires a **GUID** that identifies the property to obtain.</span></span> <span data-ttu-id="7c2b3-149">TSF definiert einen Satz von [vordefinierten Eigenschaftenbezeichnern,](predefined-properties.md) die verwendet werden, oder ein Textdienst kann seine eigenen Eigenschaftenbezeichner definieren.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-149">TSF defines a set of [predefined property identifiers](predefined-properties.md) used or a text service can define its own property identifiers.</span></span> <span data-ttu-id="7c2b3-150">Wenn eine benutzerdefinierte Eigenschaft verwendet wird, muss der Eigenschaftenanbieter die **Eigenschaften-GUID** und das Format der erhaltenen Daten veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-150">If a custom property is used, the property provider must publish the property **GUID** and the format of the data obtained.</span></span>

<span data-ttu-id="7c2b3-151">Um beispielsweise die **CLSID** für den Besitzer eines Textbereichs zu erhalten, rufen Sie **ITfContext::GetProperty** auf, um das Eigenschaftenobjekt zu erhalten, rufen [Sie ITfProperty::FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) auf, um den Bereich zu erhalten, der die Eigenschaft vollständig abdeckt, und rufen Sie dann [ITfReadOnlyProperty::GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) auf, um ein [TfGuidAtom-Objekt](/windows/desktop/TSF/tfguidatom) zu erhalten, das die **CLSID** des Textdiensts darstellt, der den Text besitzt.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-151">For example, to obtain the **CLSID** for the owner of a range of text, call **ITfContext::GetProperty** to obtain the property object, call [ITfProperty::FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) to obtain the range that entirely covers the property, then call [ITfReadOnlyProperty::GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) to get a [TfGuidAtom](/windows/desktop/TSF/tfguidatom) that represents the **CLSID** of the text service that owns the text.</span></span> <span data-ttu-id="7c2b3-152">Das folgende Beispiel zeigt eine Funktion, die bei einem Kontext, einem Bereich und einem Bearbeitungscookie die **CLSID** des Textdiensts erhält, der den Text besitzt.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-152">The following example shows a function that, given a context, range and an edit cookie, will obtain the **CLSID** of the text service that owns the text.</span></span>


```C++
HRESULT GetTextOwner(   ITfContext *pContext, 
                        ITfRange *pRange, 
                        TfEditCookie ec, 
                        CLSID *pclsidOwner)
{
    HRESULT     hr;
    ITfProperty *pProp;

    *pclsidOwner = GUID_NULL;

    hr = pContext->GetProperty(GUID_PROP_TEXTOWNER, &pProp);
    if(S_OK == hr)
    {
        ITfRange    *pPropRange;

        hr = pProp->FindRange(ec, pRange, &pPropRange, TF_ANCHOR_START);
        if(S_OK == hr)
        {
            VARIANT var;

            VariantInit(&var);
            hr = pProp->GetValue(ec, pPropRange, &var);
            if(S_OK == hr)
            {
                if(VT_I4 == var.vt)
                {
                    /*
                    var.lVal is a TfGuidAtom that represents the CLSID of the 
                    text owner. Use ITfCategoryMgr to obtain the CLSID from 
                    the TfGuidAtom.
                    */
                    ITfCategoryMgr  *pCatMgr;

                    hr = CoCreateInstance(  CLSID_TF_CategoryMgr,
                                            NULL, 
                                            CLSCTX_INPROC_SERVER, 
                                            IID_ITfCategoryMgr, 
                                            (LPVOID*)&pCatMgr);
                    if(SUCCEEDED(hr))
                    {
                        hr = pCatMgr->GetGUID((TfGuidAtom)var.lVal, pclsidOwner);
                        if(SUCCEEDED(hr))
                        {
                            /*
                            *pclsidOwner now contains the CLSID of the text 
                            service that owns the text at the selection.
                            */
                        }

                        pCatMgr->Release();
                    }
                }
                else
                {
                    //Unrecognized VARIANT type 
                    hr = E_FAIL;
                }
                
                VariantClear(&var);
            }
            
            pPropRange->Release();
        }
        
        pProp->Release();
    }

    return hr;
}

```



<span data-ttu-id="7c2b3-153">Eigenschaften können auch durch Abrufen einer [IEnumTfProperties-Schnittstelle](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) aus [ITfContext::EnumProperties aufzählt werden.](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties)</span><span class="sxs-lookup"><span data-stu-id="7c2b3-153">Properties can also be enumerated by obtaining an [IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) interface from [ITfContext::EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).</span></span>

## <a name="persistent-storage-of-properties"></a><span data-ttu-id="7c2b3-154">Persistente Speicherung von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c2b3-154">Persistent Storage of Properties</span></span>

<span data-ttu-id="7c2b3-155">Häufig sind Eigenschaften für eine Anwendung transparent und werden von mindestens einem Textdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-155">Often, properties are transparent to an application and are used by one or more text services.</span></span> <span data-ttu-id="7c2b3-156">Um die Eigenschaftsdaten zu erhalten, z. B. beim Speichern in einer Datei, muss eine Anwendung die Eigenschaftsdaten serialisieren, wenn sie gespeichert werden, und die Eigenschaftsdaten bei der Wiederherstellung der Daten neu serialisieren.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-156">In order to preserve the property data, such as when saving to a file, an application must serialize the property data when it is stored and unserialize the property data when the data is restored.</span></span> <span data-ttu-id="7c2b3-157">In diesem Fall sollte die Anwendung nicht an einzelnen Eigenschaften interessiert sein, sondern alle Eigenschaften im Kontext aufzählen und speichern.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-157">In this case, the application should not be interested in individual properties, but should enumerate all properties in the context and store them.</span></span>

<span data-ttu-id="7c2b3-158">Beim Speichern von Eigenschaftsdaten sollte eine Anwendung die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-158">When storing property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="7c2b3-159">Rufen Sie einen Eigenschaftenenumerator ab, indem **Sie ITfContext::EnumProperties aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="7c2b3-159">Obtain a property enumerator by calling **ITfContext::EnumProperties**.</span></span>
2.  <span data-ttu-id="7c2b3-160">Enumerieren Sie jede Eigenschaft, indem Sie [IEnumTfProperties::Next aufrufen.](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next)</span><span class="sxs-lookup"><span data-stu-id="7c2b3-160">Enumerate each property by calling [IEnumTfProperties::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).</span></span>
3.  <span data-ttu-id="7c2b3-161">Rufen Sie für jede Eigenschaft einen Bereichsenumerator ab, indem [Sie ITfReadOnlyProperty::EnumRanges aufrufen.](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges)</span><span class="sxs-lookup"><span data-stu-id="7c2b3-161">For each property, obtain a range enumerator by calling [ITfReadOnlyProperty::EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).</span></span>
4.  <span data-ttu-id="7c2b3-162">Aufzählen Sie jeden Bereich in der -Eigenschaft, indem [Sie IEnumTfRanges::Next aufrufen.](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next)</span><span class="sxs-lookup"><span data-stu-id="7c2b3-162">Enumerate each range in the property by calling [IEnumTfRanges::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).</span></span>
5.  <span data-ttu-id="7c2b3-163">Rufen Sie für jeden Bereich in der -Eigenschaft [ITextStoreACPServices::Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) mit der -Eigenschaft, dem Bereich, einer [TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP-Struktur](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) und einem von der Anwendung implementierten Streamobjekt auf.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-163">For each range in the property, call [ITextStoreACPServices::Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) with the property, range, a [TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) structure, and a stream object implemented by the application.</span></span>
6.  <span data-ttu-id="7c2b3-164">Schreiben Sie den Inhalt der **TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP-Struktur** in den persistenten Speicher.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-164">Write the contents of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure into persistent memory.</span></span>
7.  <span data-ttu-id="7c2b3-165">Schreiben Sie den Inhalt des Streamobjekts in den persistenten Speicher.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-165">Write the contents of the stream object into persistent memory.</span></span>
8.  <span data-ttu-id="7c2b3-166">Fahren Sie mit den vorherigen Schritten für alle Bereiche in allen Eigenschaften fort.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-166">Continue the previous steps for all of the ranges in all of the properties.</span></span>
9.  <span data-ttu-id="7c2b3-167">Die Anwendung sollte einen Typ von Abschlusszeichen in den Stream schreiben, damit bei der Wiederherstellung der Daten ein Beendigungspunkt identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-167">The application should write some type of terminiator into the stream so that, when the data is restored, a stopping point can be identified.</span></span>


```C++
HRESULT SaveProperties( ITfContext *pContext, 
                        ITextStoreACPServices *pServices, 
                        TfEditCookie ec, 
                        IStream *pStream)
{
    HRESULT             hr;
    IEnumTfProperties   *pEnumProps;
    TF_PERSISTENT_PROPERTY_HEADER_ACP PropHeader;
    ULONG uWritten;
    
    //Enumerate the properties in the context. 
    hr = pContext->EnumProperties(&pEnumProps);
    if(SUCCEEDED(hr))
    {
        ITfProperty *pProp;
        ULONG       uFetched;

        while(SUCCEEDED(pEnumProps->Next(1, &pProp, &uFetched)) && uFetched)
        {
            //Enumerate all the ranges that contain the property. 
            IEnumTfRanges   *pEnumRanges;
            hr = pProp->EnumRanges(ec, &pEnumRanges, NULL);
            if(SUCCEEDED(hr))
            {
                IStream *pTempStream;

                //Create a temporary stream to write the property data to. 
                hr = CreateStreamOnHGlobal(NULL, TRUE, &pTempStream);
                if(SUCCEEDED(hr))
                {
                    ITfRange    *pRange;

                    while(SUCCEEDED(pEnumRanges->Next(1, &pRange, &uFetched)) && uFetched)
                    {
                        LARGE_INTEGER li;

                        //Reset the temporary stream pointer. 
                        li.QuadPart = 0;
                        pTempStream->Seek(li, STREAM_SEEK_SET, NULL);
                        
                        //Get the property header and data for the range. 
                        hr = pServices->Serialize(pProp, pRange, &PropHeader, pTempStream);

                        /*
                        Write the property header into the primary stream. 
                        The header also contains the size of the property 
                        data.
                        */
                        hr = pStream->Write(&PropHeader, sizeof(PropHeader), &uWritten);

                        //Reset the temporary stream pointer. 
                        li.QuadPart = 0;
                        pTempStream->Seek(li, STREAM_SEEK_SET, NULL);

                        //Copy the property data from the temporary stream into the primary stream. 
                        ULARGE_INTEGER  uli;
                        uli.QuadPart = PropHeader.cb;

                        hr = pTempStream->CopyTo(pStream, uli, NULL, NULL);

                        pRange->Release();
                    }
                    
                    pTempStream->Release();
                }
                
                pEnumRanges->Release();
            }
            
            pProp->Release();
        }
        
        pEnumProps->Release();
    }

    //Write a property header with zero size and guid into the stream as a terminator 
    ZeroMemory(&PropHeader, sizeof(PropHeader));
    hr = pStream->Write(&PropHeader, sizeof(PropHeader), &uWritten);

    return hr;
}

```



<span data-ttu-id="7c2b3-168">**ITextStoreACPServices::Serialize**[ITfPropertyStore::Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span><span class="sxs-lookup"><span data-stu-id="7c2b3-168">**ITextStoreACPServices::Serialize**[ITfPropertyStore::Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span></span>

<span data-ttu-id="7c2b3-169">Beim Wiederherstellen von Eigenschaftsdaten sollte eine Anwendung die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-169">When restoring property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="7c2b3-170">Legen Sie den Streamzeiger auf den Anfang der ersten **TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP-Struktur** fest.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-170">Set the stream pointer to the start of the first **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
2.  <span data-ttu-id="7c2b3-171">Lesen Sie die **TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP-Struktur.**</span><span class="sxs-lookup"><span data-stu-id="7c2b3-171">Read the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
3.  <span data-ttu-id="7c2b3-172">Rufen **Sie ITfContext::GetProperty** mit dem **guidType-Member** der **TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP-Struktur** auf.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-172">Call **ITfContext::GetProperty** with the **guidType** member of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
4.  <span data-ttu-id="7c2b3-173">Die Anwendung kann an diesem Punkt eines von zwei Dingen tun.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-173">The application can do one of two things at this point.</span></span>
    1.  <span data-ttu-id="7c2b3-174">Erstellen Sie eine Instanz eines [ITfPersistentPropertyLoaderACP-Objekts,](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) das die Anwendung implementieren muss.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-174">Create an instance of an [ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) object that the application must implement.</span></span> <span data-ttu-id="7c2b3-175">Rufen Sie dann [ITextStoreACPServices::Unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) mit **NULL** für *pStream* und den **ITfPersistentPropertyLoaderACP-Zeiger** auf.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-175">Then call [ITextStoreACPServices::Unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) with **NULL** for *pStream* and the **ITfPersistentPropertyLoaderACP** pointer.</span></span>
    2.  <span data-ttu-id="7c2b3-176">Übergeben Sie den Eingabestream **an ITextStoreACPServices::Unserialize** und **NULL** für *pLoader*.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-176">Pass the input stream to **ITextStoreACPServices::Unserialize** and **NULL** for *pLoader*.</span></span>

    <span data-ttu-id="7c2b3-177">Die erste Methode wird bevorzugt, da sie am effizientesten ist.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-177">The first method is preferred as it is the most efficient.</span></span> <span data-ttu-id="7c2b3-178">Die Implementierung der zweiten Methode bewirkt, dass alle Eigenschaftsdaten während des **ITextStoreACPServices::Unserialize-Aufrufs** aus dem Stream gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-178">Implementing the second method causes all of the property data to be read from the stream during the **ITextStoreACPServices::Unserialize** call.</span></span> <span data-ttu-id="7c2b3-179">Die erste Methode bewirkt, dass die Eigenschaftsdaten bei Bedarf zu einem späteren Zeitpunkt gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-179">The first method causes the property data to be read on demand at a later time.</span></span>
5.  <span data-ttu-id="7c2b3-180">Wiederholen Sie die vorherigen Schritte, bis alle Eigenschaftenblöcke erneutialisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-180">Repeat the previous steps until all property blocks are unserialized.</span></span>


```C++
HRESULT LoadProperties( ITfContext *pContext, 
                        ITextStoreACPServices *pServices, 
                        IStream *pStream)
{
    HRESULT hr;
    ULONG   uRead;
    TF_PERSISTENT_PROPERTY_HEADER_ACP PropHeader;

    /*
    Read each property header and property data from the stream. The 
    list of properties is terminated by a TF_PERSISTENT_PROPERTY_HEADER_ACP 
    structure with a cb member of zero.
    */
    hr = pStream->Read(&PropHeader, sizeof(PropHeader), &uRead);
    while(  SUCCEEDED(hr) && 
            (sizeof(PropHeader) == uRead) && 
            (0 != PropHeader.cb))
    {
        ITfProperty *pProp;

        hr = pContext->GetProperty(PropHeader.guidType, &pProp);
        if(SUCCEEDED(hr))
        {
            /*
            Have TSF read the property data from the stream. This call 
            requests a read-only lock, so be sure it can be granted 
            or else this method will fail.
            */
            CTSFPersistentPropertyLoader *pLoader = new CTSFPersistentPropertyLoader(&PropHeader, pStream);
            hr = pServices->Unserialize(pProp, &PropHeader, NULL, pLoader);

            pProp->Release();
        }

        //Read the next header. 
        hr = pStream->Read(&PropHeader, sizeof(PropHeader), &uRead);
    }

    return hr;
}

```



 

 
