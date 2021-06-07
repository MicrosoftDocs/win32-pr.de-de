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
# <a name="properties-common-elements"></a>Eigenschaften (Allgemeine Elemente)

Textdienstframework (TSF) stellt Eigenschaften bereit, die Metadaten einem Textbereich zuordnen. Zu diesen Eigenschaften zählen u. a. Anzeigeattribute wie fett formatierten Text, der Sprachbezeichner des Texts und rohe Daten, die von einem Textdienst bereitgestellt werden, z. B. die Audiodaten, die dem Text aus dem Sprachtextdienst zugeordnet sind.

Im folgenden Beispiel wird veranschaulicht, wie eine hypothetische Textfarbeigenschaft mit möglichen Werten von Rot (R), Grün (G) oder Blau (B) angezeigt werden kann.


```C++
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



Eigenschaften verschiedener Typen können sich überlappen. Nehmen Sie beispielsweise das vorherige Beispiel, und fügen Sie ein Textattribut hinzu, das entweder fett (B) oder italisch (I) sein kann.


```C++
ATTRIB:BBBBBBB      IIIIIIIIIIII
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



Der Text "this" wäre fett, "is" wäre sowohl fett als auch rot, "some" würde normal angezeigt, "colored" wäre grün und italicized und "text" wäre italicized.

Eigenschaften desselben Typs dürfen sich nicht überlappen. Die folgende Situation ist beispielsweise nicht zulässig, da "is" und "colored" überlappende Werte der gleichen Typen haben.


```C++
COLOR: GGG GGGG RRR BBBBGGG     
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



## <a name="property-types"></a>Eigenschaftentypen

TSF definiert drei verschiedene Typen von Eigenschaften.



|   Eigenschaftstyp             |   BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| statischen         | Ein statisches Eigenschaftenobjekt speichert die Eigenschaftsdaten mit Text. Außerdem wird der Bereich der Textinformationen für jeden Bereich gespeichert, für den die Eigenschaft gilt. ITfReadOnlyProperty::GetType gibt die KATEGORIE GUID \_ TFCAT \_ PROPSTYLE \_ STATIC zurück.                                                                                                                                                                                                                      |
| Static-Compact | Ein static-compact-Eigenschaftsobjekt ist mit einem statischen Eigenschaftsobjekt identisch, mit der Ausnahme, dass eine statisch-kompakte Eigenschaft keine Bereichsdaten enthält. Wenn der Bereich angefordert wird, der von einer statisch-kompakten Eigenschaft abgedeckt wird, wird ein Bereich für jede Gruppe benachbarter Eigenschaften erstellt. Statisch-kompakte Eigenschaften sind die effizienteste Möglichkeit, Eigenschaften pro Zeichen zu speichern. ITfReadOnlyProperty::GetType gibt die KATEGORIE GUID \_ TFCAT \_ PROPSTYLE \_ STATICCOMPACT zurück. |
| Benutzerdefiniert         | Ein benutzerdefiniertes Eigenschaftenobjekt speichert die Bereichsinformationen für jeden Bereich, für den die Eigenschaft gilt. Die tatsächlichen Daten für die Eigenschaft werden jedoch nicht gespeichert. Stattdessen speichert eine benutzerdefinierte Eigenschaft ein ITfPropertyStore-Objekt. Der TSF-Manager verwendet dieses Objekt, um auf die Eigenschaftendaten zu zugreifen und diese zu verwalten. ITfReadOnlyProperty::GetType gibt die KATEGORIE GUID \_ TFCAT \_ PROPSTYLE \_ CUSTOM zurück.                                                                    |



 

## <a name="working-with-properties"></a>Arbeiten mit Eigenschaften

Der Eigenschaftswert und die Attribute werden mithilfe der [ITfReadOnlyProperty-Schnittstelle](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) ermittelt und mithilfe der [ITfProperty-Schnittstelle](/windows/desktop/api/Msctf/nn-msctf-itfproperty) geändert.

Wenn ein bestimmter Eigenschaftentyp erforderlich ist, wird [ITfContext::GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) verwendet. **ITfContext::GetProperty** erfordert eine **GUID,** die die zu erhaltende Eigenschaft identifiziert. TSF definiert einen Satz von [vordefinierten Eigenschaftenbezeichnern,](predefined-properties.md) die verwendet werden, oder ein Textdienst kann seine eigenen Eigenschaftenbezeichner definieren. Wenn eine benutzerdefinierte Eigenschaft verwendet wird, muss der Eigenschaftenanbieter die **Eigenschaften-GUID** und das Format der erhaltenen Daten veröffentlichen.

Um beispielsweise die **CLSID** für den Besitzer eines Textbereichs zu erhalten, rufen Sie **ITfContext::GetProperty** auf, um das Eigenschaftenobjekt zu erhalten, rufen [Sie ITfProperty::FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) auf, um den Bereich zu erhalten, der die Eigenschaft vollständig abdeckt, und rufen Sie dann [ITfReadOnlyProperty::GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) auf, um ein [TfGuidAtom-Objekt](/windows/desktop/TSF/tfguidatom) zu erhalten, das die **CLSID** des Textdiensts darstellt, der den Text besitzt. Das folgende Beispiel zeigt eine Funktion, die bei einem Kontext, einem Bereich und einem Bearbeitungscookie die **CLSID** des Textdiensts erhält, der den Text besitzt.


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



Eigenschaften können auch durch Abrufen einer [IEnumTfProperties-Schnittstelle](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) aus [ITfContext::EnumProperties aufzählt werden.](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties)

## <a name="persistent-storage-of-properties"></a>Persistente Speicherung von Eigenschaften

Häufig sind Eigenschaften für eine Anwendung transparent und werden von mindestens einem Textdienst verwendet. Um die Eigenschaftsdaten zu erhalten, z. B. beim Speichern in einer Datei, muss eine Anwendung die Eigenschaftsdaten serialisieren, wenn sie gespeichert werden, und die Eigenschaftsdaten bei der Wiederherstellung der Daten neu serialisieren. In diesem Fall sollte die Anwendung nicht an einzelnen Eigenschaften interessiert sein, sondern alle Eigenschaften im Kontext aufzählen und speichern.

Beim Speichern von Eigenschaftsdaten sollte eine Anwendung die folgenden Schritte ausführen.

1.  Rufen Sie einen Eigenschaftenenumerator ab, indem **Sie ITfContext::EnumProperties aufrufen.**
2.  Enumerieren Sie jede Eigenschaft, indem Sie [IEnumTfProperties::Next aufrufen.](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next)
3.  Rufen Sie für jede Eigenschaft einen Bereichsenumerator ab, indem [Sie ITfReadOnlyProperty::EnumRanges aufrufen.](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges)
4.  Aufzählen Sie jeden Bereich in der -Eigenschaft, indem [Sie IEnumTfRanges::Next aufrufen.](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next)
5.  Rufen Sie für jeden Bereich in der -Eigenschaft [ITextStoreACPServices::Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) mit der -Eigenschaft, dem Bereich, einer [TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP-Struktur](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) und einem von der Anwendung implementierten Streamobjekt auf.
6.  Schreiben Sie den Inhalt der **TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP-Struktur** in den persistenten Speicher.
7.  Schreiben Sie den Inhalt des Streamobjekts in den persistenten Speicher.
8.  Fahren Sie mit den vorherigen Schritten für alle Bereiche in allen Eigenschaften fort.
9.  Die Anwendung sollte einen Typ von Abschlusszeichen in den Stream schreiben, damit bei der Wiederherstellung der Daten ein Beendigungspunkt identifiziert werden kann.


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



**ITextStoreACPServices::Serialize**[ITfPropertyStore::Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)

Beim Wiederherstellen von Eigenschaftsdaten sollte eine Anwendung die folgenden Schritte ausführen.

1.  Legen Sie den Streamzeiger auf den Anfang der ersten **TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP-Struktur** fest.
2.  Lesen Sie die **TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP-Struktur.**
3.  Rufen **Sie ITfContext::GetProperty** mit dem **guidType-Member** der **TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP-Struktur** auf.
4.  Die Anwendung kann an diesem Punkt eines von zwei Dingen tun.
    1.  Erstellen Sie eine Instanz eines [ITfPersistentPropertyLoaderACP-Objekts,](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) das die Anwendung implementieren muss. Rufen Sie dann [ITextStoreACPServices::Unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) mit **NULL** für *pStream* und den **ITfPersistentPropertyLoaderACP-Zeiger** auf.
    2.  Übergeben Sie den Eingabestream **an ITextStoreACPServices::Unserialize** und **NULL** für *pLoader*.

    Die erste Methode wird bevorzugt, da sie am effizientesten ist. Die Implementierung der zweiten Methode bewirkt, dass alle Eigenschaftsdaten während des **ITextStoreACPServices::Unserialize-Aufrufs** aus dem Stream gelesen werden. Die erste Methode bewirkt, dass die Eigenschaftsdaten bei Bedarf zu einem späteren Zeitpunkt gelesen werden.
5.  Wiederholen Sie die vorherigen Schritte, bis alle Eigenschaftenblöcke erneutialisiert wurden.


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



 

 
