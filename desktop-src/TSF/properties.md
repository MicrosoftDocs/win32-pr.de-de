---
title: Eigenschaften (allgemeine Elemente)
description: Das Text Services-Framework (TSF) stellt Eigenschaften bereit, die Metadaten einem Textbereich zuordnen.
ms.assetid: d1d0dd99-f303-4355-9835-917de9491a0b
keywords:
- Text Dienst Framework (TSF), Eigenschaften
- TSF (Text Dienst Framework), Eigenschaften
- Text Dienste, Eigenschaften
- TSF-aktivierte Anwendungen, Eigenschaften
- properties
- Text Dienst Framework (TSF), Eigenschafts Typen
- TSF (Text Services Framework), Eigenschafts Typen
- Text Dienste, Eigenschafts Typen
- TSF-aktivierte Anwendungen, Eigenschafts Typen
- Eigenschaftentypen
- Text Dienst Framework (TSF), persistente Speicherung von Eigenschaften
- TSF (Text Dienst Framework), persistente Speicherung von Eigenschaften
- Text Dienste, persistente Speicherung von Eigenschaften
- TSF-aktivierte Anwendungen, persistente Speicherung von Eigenschaften
- persistente Speicherung von Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff852bccfb7d9b6c94e57a2fa0cf8eef6fbdf18
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106339923"
---
# <a name="properties-common-elements"></a><span data-ttu-id="b12ba-118">Eigenschaften (allgemeine Elemente)</span><span class="sxs-lookup"><span data-stu-id="b12ba-118">Properties (Common Elements)</span></span>

<span data-ttu-id="b12ba-119">Das Text Services-Framework (TSF) stellt Eigenschaften bereit, die Metadaten einem Textbereich zuordnen.</span><span class="sxs-lookup"><span data-stu-id="b12ba-119">Text Services Framework (TSF) provides properties that associate metadata with a range of text.</span></span> <span data-ttu-id="b12ba-120">Zu diesen Eigenschaften gehören unter anderem die Anzeige von Attributen wie fettem Text, der sprach Bezeichner des Texts und von einem Text Dienst bereitgestellte Rohdaten, wie z. b. die Audiodaten, die Text aus dem sprach Text Dienst zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b12ba-120">These properties include, but are not limited to, display attributes such as bold text, the language identifier of the text, and raw data provided by a text service such as the audio data associated with text from the speech text service.</span></span>

<span data-ttu-id="b12ba-121">Im folgenden Beispiel wird veranschaulicht, wie eine hypothetische Text Farb Eigenschaft mit möglichen Werten von rot (R), grün (G) oder blau (B) angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b12ba-121">The following example demonstrates how a hypothetical text color property with possible values of red (R), green (G), or blue (B) can be viewed.</span></span>


```C++
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="b12ba-122">Eigenschaften verschiedener Typen können sich überlappen.</span><span class="sxs-lookup"><span data-stu-id="b12ba-122">Properties of different types can overlap.</span></span> <span data-ttu-id="b12ba-123">Nehmen Sie z. B. das vorherige Beispiel, und fügen Sie ein Text Attribut hinzu, das entweder Fett (B) oder kursiv (I) sein kann.</span><span class="sxs-lookup"><span data-stu-id="b12ba-123">For example, take the previous example and add a text attribute that can be either bold (B) or italic (I).</span></span>


```C++
ATTRIB:BBBBBBB      IIIIIIIIIIII
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="b12ba-124">Der Text "This" wäre "Bold", "is", wäre "Bold" und "Red", "Some" wird normal angezeigt, "farbig" wäre grün und kursiv und "Text" wird kursiv formatiert.</span><span class="sxs-lookup"><span data-stu-id="b12ba-124">The text "this" would be bold, "is" would be both bold and red, "some" would be displayed normally, "colored" would be green and italicized and "text" would be italicized.</span></span>

<span data-ttu-id="b12ba-125">Eigenschaften desselben Typs dürfen sich nicht überlappen.</span><span class="sxs-lookup"><span data-stu-id="b12ba-125">Properties of the same type cannot overlap.</span></span> <span data-ttu-id="b12ba-126">Beispielsweise ist die folgende Situation nicht zulässig, da "ist" und "farbig" überlappende Werte desselben Typs aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b12ba-126">For example, the following situation is not allowed because "is" and "colored" have overlapping values of the same types.</span></span>


```C++
COLOR: GGG GGGG RRR BBBBGGG     
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



## <a name="property-types"></a><span data-ttu-id="b12ba-127">Eigenschaftentypen</span><span class="sxs-lookup"><span data-stu-id="b12ba-127">Property Types</span></span>

<span data-ttu-id="b12ba-128">TSF definiert drei verschiedene Typen von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b12ba-128">TSF defines three different types of properties.</span></span>



|                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b12ba-129">statischen</span><span class="sxs-lookup"><span data-stu-id="b12ba-129">Static</span></span>         | <span data-ttu-id="b12ba-130">Ein statisches Eigenschaften Objekt speichert die Eigenschafts Daten mit Text.</span><span class="sxs-lookup"><span data-stu-id="b12ba-130">A static property object stores the property data with text.</span></span> <span data-ttu-id="b12ba-131">Außerdem wird der Bereich der Textinformationen für jeden Bereich gespeichert, für den die Eigenschaft gilt.</span><span class="sxs-lookup"><span data-stu-id="b12ba-131">It also stores the range of text information for each range that the property applies to.</span></span> <span data-ttu-id="b12ba-132">Itfreadonlyproperty:: GetType gibt die statische GUID \_ tfcat \_ propstyle- \_ Kategorie zurück.</span><span class="sxs-lookup"><span data-stu-id="b12ba-132">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATIC category.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="b12ba-133">Static-Compact</span><span class="sxs-lookup"><span data-stu-id="b12ba-133">Static-Compact</span></span> | <span data-ttu-id="b12ba-134">Ein statisches Compact-Eigenschafts Objekt ist mit einem statischen Eigenschafts Objekt identisch, außer eine static-Compact-Eigenschaft speichert keine Bereichs Daten.</span><span class="sxs-lookup"><span data-stu-id="b12ba-134">A static-compact property object is identical to a static property object except a static-compact property does not store range data.</span></span> <span data-ttu-id="b12ba-135">Wenn der von einer static-Compact-Eigenschaft abgedeckte Bereich angefordert wird, wird für jede Gruppe von angrenzenden Eigenschaften ein Bereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="b12ba-135">When the range covered by a static-compact property is requested, a range is created for each group of adjacent properties.</span></span> <span data-ttu-id="b12ba-136">Statische Compact-Eigenschaften sind die effizienteste Methode, um Eigenschaften pro Zeichen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b12ba-136">Static-compact properties are the most efficient way to store properties on a per-character basis.</span></span> <span data-ttu-id="b12ba-137">Itfreadonlyproperty:: GetType gibt die GUID \_ tfcat \_ propstyle \_ staticcompact-Kategorie zurück.</span><span class="sxs-lookup"><span data-stu-id="b12ba-137">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATICCOMPACT category.</span></span> |
| <span data-ttu-id="b12ba-138">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="b12ba-138">Custom</span></span>         | <span data-ttu-id="b12ba-139">Ein benutzerdefiniertes Eigenschaften Objekt speichert die Bereichs Informationen für jeden Bereich, auf den die Eigenschaft angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="b12ba-139">A custom property object stores the range information for each range that the property applies to.</span></span> <span data-ttu-id="b12ba-140">Die eigentlichen Daten für die Eigenschaft werden jedoch nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b12ba-140">It does not, however, store the actual data for the property.</span></span> <span data-ttu-id="b12ba-141">Stattdessen speichert eine benutzerdefinierte Eigenschaft ein ITF PropertyStore-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b12ba-141">Instead, a custom property stores an ITfPropertyStore object.</span></span> <span data-ttu-id="b12ba-142">Der TSF-Manager verwendet dieses Objekt, um auf die Eigenschaften Daten zuzugreifen und diese zu verwalten. Itfreadonlyproperty:: GetType gibt die \_ benutzerdefinierte Kategorie GUID tfcat \_ propstyle zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="b12ba-142">The TSF manager uses this object to access and maintain the property data.ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_CUSTOM category.</span></span>                                                                    |



 

## <a name="working-with-properties"></a><span data-ttu-id="b12ba-143">Arbeiten mit Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b12ba-143">Working with Properties</span></span>

<span data-ttu-id="b12ba-144">Der Eigenschafts Wert und die Attribute werden mithilfe der [itfreadonlyproperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) -Schnittstelle abgerufen und mithilfe der [ITF Property](/windows/desktop/api/Msctf/nn-msctf-itfproperty) -Schnittstelle geändert.</span><span class="sxs-lookup"><span data-stu-id="b12ba-144">The property value and attributes are obtained using the [ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) interface and modified using the [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) interface.</span></span>

<span data-ttu-id="b12ba-145">Wenn ein bestimmter Eigenschaftentyp erforderlich ist, wird [ITF context:: GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b12ba-145">If a specific property type is required, then [ITfContext::GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) is used.</span></span> <span data-ttu-id="b12ba-146">**ITfContext:: GetProperty** erfordert eine **GUID** , die die abzurufenden Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b12ba-146">**ITfContext::GetProperty** requires a **GUID** that identifies the property to obtain.</span></span> <span data-ttu-id="b12ba-147">TSF definiert eine Reihe von [vordefinierten Eigenschaften bezeichgern](predefined-properties.md) , die verwendet werden, oder ein Text Dienst kann seine eigenen Eigenschaften Bezeichner definieren.</span><span class="sxs-lookup"><span data-stu-id="b12ba-147">TSF defines a set of [predefined property identifiers](predefined-properties.md) used or a text service can define its own property identifiers.</span></span> <span data-ttu-id="b12ba-148">Wenn eine benutzerdefinierte Eigenschaft verwendet wird, muss der Eigenschafts Anbieter die Eigenschafts- **GUID** und das Format der erhaltenen Daten veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="b12ba-148">If a custom property is used, the property provider must publish the property **GUID** and the format of the data obtained.</span></span>

<span data-ttu-id="b12ba-149">Wenn Sie z. b. die **CLSID** für den Besitzer eines Text Bereichs abrufen möchten, rufen Sie **ITfContext:: GetProperty** auf, um das Property-Objekt abzurufen, rufen Sie [itfproperty:: findrange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) auf, um den Bereich zu erhalten, der die Eigenschaft vollständig abdeckt, und rufen Sie dann [itfreadonlyproperty:: GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) auf, um ein [tfguidatom](/windows/desktop/TSF/tfguidatom) abzurufen, das die **CLSID** des Text dienstantexts darstellt</span><span class="sxs-lookup"><span data-stu-id="b12ba-149">For example, to obtain the **CLSID** for the owner of a range of text, call **ITfContext::GetProperty** to obtain the property object, call [ITfProperty::FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) to obtain the range that entirely covers the property, then call [ITfReadOnlyProperty::GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) to get a [TfGuidAtom](/windows/desktop/TSF/tfguidatom) that represents the **CLSID** of the text service that owns the text.</span></span> <span data-ttu-id="b12ba-150">Im folgenden Beispiel wird eine Funktion veranschaulicht, die bei Angabe von Kontext, Bereich und Bearbeitungs Cookie die **CLSID** des Text Dienstanbieter erhält, der den Text besitzt.</span><span class="sxs-lookup"><span data-stu-id="b12ba-150">The following example shows a function that, given a context, range and an edit cookie, will obtain the **CLSID** of the text service that owns the text.</span></span>


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



<span data-ttu-id="b12ba-151">Eigenschaften können auch aufgelistet werden, indem eine [ienumtfproperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) -Schnittstelle von [ITF context:: EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties)erhalten wird.</span><span class="sxs-lookup"><span data-stu-id="b12ba-151">Properties can also be enumerated by obtaining an [IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) interface from [ITfContext::EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).</span></span>

## <a name="persistent-storage-of-properties"></a><span data-ttu-id="b12ba-152">Persistente Speicherung von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b12ba-152">Persistent Storage of Properties</span></span>

<span data-ttu-id="b12ba-153">Häufig sind Eigenschaften für eine Anwendung transparent und werden von einem oder mehreren Text Diensten verwendet.</span><span class="sxs-lookup"><span data-stu-id="b12ba-153">Often, properties are transparent to an application and are used by one or more text services.</span></span> <span data-ttu-id="b12ba-154">Um die Eigenschaften Daten beizubehalten, z. b. beim Speichern in einer Datei, muss eine Anwendung die Eigenschaften Daten bei der Speicherung serialisieren und die Eigenschafts Daten beim Wiederherstellen der Daten wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="b12ba-154">In order to preserve the property data, such as when saving to a file, an application must serialize the property data when it is stored and unserialize the property data when the data is restored.</span></span> <span data-ttu-id="b12ba-155">In diesem Fall sollte die Anwendung nicht an einzelnen Eigenschaften interessiert sein, sondern alle Eigenschaften im Kontext auflisten und speichern.</span><span class="sxs-lookup"><span data-stu-id="b12ba-155">In this case, the application should not be interested in individual properties, but should enumerate all properties in the context and store them.</span></span>

<span data-ttu-id="b12ba-156">Beim Speichern von Eigenschaften Daten sollte eine Anwendung die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="b12ba-156">When storing property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="b12ba-157">Rufen Sie einen eigenschaftenenumerator durch Aufrufen von **ITfContext:: EnumProperties** ab.</span><span class="sxs-lookup"><span data-stu-id="b12ba-157">Obtain a property enumerator by calling **ITfContext::EnumProperties**.</span></span>
2.  <span data-ttu-id="b12ba-158">Zählen Sie die einzelnen Eigenschaften durch Aufrufen von [ienumtfproperties:: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next)auf.</span><span class="sxs-lookup"><span data-stu-id="b12ba-158">Enumerate each property by calling [IEnumTfProperties::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).</span></span>
3.  <span data-ttu-id="b12ba-159">Rufen Sie für jede Eigenschaft einen Bereichs Enumerator durch Aufrufen von [itfreadonlyproperty:: enumranges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges)ab.</span><span class="sxs-lookup"><span data-stu-id="b12ba-159">For each property, obtain a range enumerator by calling [ITfReadOnlyProperty::EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).</span></span>
4.  <span data-ttu-id="b12ba-160">Listet jeden Bereich in der Eigenschaft durch Aufrufen von [ienumtfranges:: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next)auf.</span><span class="sxs-lookup"><span data-stu-id="b12ba-160">Enumerate each range in the property by calling [IEnumTfRanges::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).</span></span>
5.  <span data-ttu-id="b12ba-161">Für jeden Bereich in der-Eigenschaft wird [itextstoreacpservices:: Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) mit der-Eigenschaft, dem Range, einem [tf \_ persistent \_ \_ -Eigenschaften Header \_ ACP-](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) Struktur und einem von der Anwendung implementierten Stream-Objekt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b12ba-161">For each range in the property, call [ITextStoreACPServices::Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) with the property, range, a [TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) structure, and a stream object implemented by the application.</span></span>
6.  <span data-ttu-id="b12ba-162">Schreiben Sie den Inhalt der Überschrift für den **\_ persistenten TF \_ \_ -Eigenschaften Header \_ ACP** in den persistenten Speicher.</span><span class="sxs-lookup"><span data-stu-id="b12ba-162">Write the contents of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure into persistent memory.</span></span>
7.  <span data-ttu-id="b12ba-163">Schreiben Sie den Inhalt des Datenstrom Objekts in den persistenten Speicher.</span><span class="sxs-lookup"><span data-stu-id="b12ba-163">Write the contents of the stream object into persistent memory.</span></span>
8.  <span data-ttu-id="b12ba-164">Führen Sie die vorherigen Schritte für alle Bereiche in allen Eigenschaften aus.</span><span class="sxs-lookup"><span data-stu-id="b12ba-164">Continue the previous steps for all of the ranges in all of the properties.</span></span>
9.  <span data-ttu-id="b12ba-165">Die Anwendung muss eine Art von terminiator in den Stream schreiben, damit beim Wiederherstellen der Daten ein Haltepunkt identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b12ba-165">The application should write some type of terminiator into the stream so that, when the data is restored, a stopping point can be identified.</span></span>


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



<span data-ttu-id="b12ba-166">**Itextstoreacpservices:: Serialize**[ITF PropertyStore:: Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span><span class="sxs-lookup"><span data-stu-id="b12ba-166">**ITextStoreACPServices::Serialize**[ITfPropertyStore::Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span></span>

<span data-ttu-id="b12ba-167">Beim Wiederherstellen von Eigenschaften Daten sollte eine Anwendung die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="b12ba-167">When restoring property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="b12ba-168">Legen Sie den Streamzeiger auf den Anfang der ersten **tf \_ -Struktur der persistenten \_ \_ \_ -Eigenschaften Kopfzeile** fest.</span><span class="sxs-lookup"><span data-stu-id="b12ba-168">Set the stream pointer to the start of the first **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
2.  <span data-ttu-id="b12ba-169">Lesen Sie den beständigen **tf \_ \_ \_ -Eigenschaften Header \_ ACP-** Struktur.</span><span class="sxs-lookup"><span data-stu-id="b12ba-169">Read the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
3.  <span data-ttu-id="b12ba-170">Aufrufen von **ITfContext:: GetProperty** mit dem **guidtype** -Member des **tf-Elements für \_ persistente \_ Eigenschaften \_ Header \_ ACP** .</span><span class="sxs-lookup"><span data-stu-id="b12ba-170">Call **ITfContext::GetProperty** with the **guidType** member of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
4.  <span data-ttu-id="b12ba-171">An dieser Stelle kann die Anwendung eine von zwei Punkten ausführen.</span><span class="sxs-lookup"><span data-stu-id="b12ba-171">The application can do one of two things at this point.</span></span>
    1.  <span data-ttu-id="b12ba-172">Erstellen Sie eine Instanz eines [ITF persistentpropertyloaderacp-](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) Objekts, das von der Anwendung implementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="b12ba-172">Create an instance of an [ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) object that the application must implement.</span></span> <span data-ttu-id="b12ba-173">Nennen Sie dann [itextstoreacpservices:: unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) mit **null** für *pStream* und den **itfpersistentpropertyloaderacp-** Zeiger.</span><span class="sxs-lookup"><span data-stu-id="b12ba-173">Then call [ITextStoreACPServices::Unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) with **NULL** for *pStream* and the **ITfPersistentPropertyLoaderACP** pointer.</span></span>
    2.  <span data-ttu-id="b12ba-174">Übergeben Sie den Eingabedaten Strom an **itextstoreacpservices:: unserialize** und **null** für *ploader*.</span><span class="sxs-lookup"><span data-stu-id="b12ba-174">Pass the input stream to **ITextStoreACPServices::Unserialize** and **NULL** for *pLoader*.</span></span>

    <span data-ttu-id="b12ba-175">Die erste Methode wird bevorzugt, da Sie die effizienteste ist.</span><span class="sxs-lookup"><span data-stu-id="b12ba-175">The first method is preferred as it is the most efficient.</span></span> <span data-ttu-id="b12ba-176">Das Implementieren der zweiten Methode bewirkt, dass alle Eigenschaften Daten während des **itextstoreacpservices:: unserialize** -Aufrufes aus dem Stream gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="b12ba-176">Implementing the second method causes all of the property data to be read from the stream during the **ITextStoreACPServices::Unserialize** call.</span></span> <span data-ttu-id="b12ba-177">Die erste Methode bewirkt, dass die Eigenschaften Daten zu einem späteren Zeitpunkt bei Bedarf gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="b12ba-177">The first method causes the property data to be read on demand at a later time.</span></span>
5.  <span data-ttu-id="b12ba-178">Wiederholen Sie die vorherigen Schritte, bis alle Eigenschafts Blöcke unserialisiert sind.</span><span class="sxs-lookup"><span data-stu-id="b12ba-178">Repeat the previous steps until all property blocks are unserialized.</span></span>


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



 

 
