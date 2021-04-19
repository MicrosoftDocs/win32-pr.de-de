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
# <a name="properties-common-elements"></a>Eigenschaften (allgemeine Elemente)

Das Text Services-Framework (TSF) stellt Eigenschaften bereit, die Metadaten einem Textbereich zuordnen. Zu diesen Eigenschaften gehören unter anderem die Anzeige von Attributen wie fettem Text, der sprach Bezeichner des Texts und von einem Text Dienst bereitgestellte Rohdaten, wie z. b. die Audiodaten, die Text aus dem sprach Text Dienst zugeordnet sind.

Im folgenden Beispiel wird veranschaulicht, wie eine hypothetische Text Farb Eigenschaft mit möglichen Werten von rot (R), grün (G) oder blau (B) angezeigt werden kann.


```C++
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



Eigenschaften verschiedener Typen können sich überlappen. Nehmen Sie z. B. das vorherige Beispiel, und fügen Sie ein Text Attribut hinzu, das entweder Fett (B) oder kursiv (I) sein kann.


```C++
ATTRIB:BBBBBBB      IIIIIIIIIIII
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



Der Text "This" wäre "Bold", "is", wäre "Bold" und "Red", "Some" wird normal angezeigt, "farbig" wäre grün und kursiv und "Text" wird kursiv formatiert.

Eigenschaften desselben Typs dürfen sich nicht überlappen. Beispielsweise ist die folgende Situation nicht zulässig, da "ist" und "farbig" überlappende Werte desselben Typs aufweisen.


```C++
COLOR: GGG GGGG RRR BBBBGGG     
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



## <a name="property-types"></a>Eigenschaftentypen

TSF definiert drei verschiedene Typen von Eigenschaften.



|                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| statischen         | Ein statisches Eigenschaften Objekt speichert die Eigenschafts Daten mit Text. Außerdem wird der Bereich der Textinformationen für jeden Bereich gespeichert, für den die Eigenschaft gilt. Itfreadonlyproperty:: GetType gibt die statische GUID \_ tfcat \_ propstyle- \_ Kategorie zurück.                                                                                                                                                                                                                      |
| Static-Compact | Ein statisches Compact-Eigenschafts Objekt ist mit einem statischen Eigenschafts Objekt identisch, außer eine static-Compact-Eigenschaft speichert keine Bereichs Daten. Wenn der von einer static-Compact-Eigenschaft abgedeckte Bereich angefordert wird, wird für jede Gruppe von angrenzenden Eigenschaften ein Bereich erstellt. Statische Compact-Eigenschaften sind die effizienteste Methode, um Eigenschaften pro Zeichen zu speichern. Itfreadonlyproperty:: GetType gibt die GUID \_ tfcat \_ propstyle \_ staticcompact-Kategorie zurück. |
| Benutzerdefiniert         | Ein benutzerdefiniertes Eigenschaften Objekt speichert die Bereichs Informationen für jeden Bereich, auf den die Eigenschaft angewendet wird. Die eigentlichen Daten für die Eigenschaft werden jedoch nicht gespeichert. Stattdessen speichert eine benutzerdefinierte Eigenschaft ein ITF PropertyStore-Objekt. Der TSF-Manager verwendet dieses Objekt, um auf die Eigenschaften Daten zuzugreifen und diese zu verwalten. Itfreadonlyproperty:: GetType gibt die \_ benutzerdefinierte Kategorie GUID tfcat \_ propstyle zurück \_ .                                                                    |



 

## <a name="working-with-properties"></a>Arbeiten mit Eigenschaften

Der Eigenschafts Wert und die Attribute werden mithilfe der [itfreadonlyproperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) -Schnittstelle abgerufen und mithilfe der [ITF Property](/windows/desktop/api/Msctf/nn-msctf-itfproperty) -Schnittstelle geändert.

Wenn ein bestimmter Eigenschaftentyp erforderlich ist, wird [ITF context:: GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) verwendet. **ITfContext:: GetProperty** erfordert eine **GUID** , die die abzurufenden Eigenschaft identifiziert. TSF definiert eine Reihe von [vordefinierten Eigenschaften bezeichgern](predefined-properties.md) , die verwendet werden, oder ein Text Dienst kann seine eigenen Eigenschaften Bezeichner definieren. Wenn eine benutzerdefinierte Eigenschaft verwendet wird, muss der Eigenschafts Anbieter die Eigenschafts- **GUID** und das Format der erhaltenen Daten veröffentlichen.

Wenn Sie z. b. die **CLSID** für den Besitzer eines Text Bereichs abrufen möchten, rufen Sie **ITfContext:: GetProperty** auf, um das Property-Objekt abzurufen, rufen Sie [itfproperty:: findrange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) auf, um den Bereich zu erhalten, der die Eigenschaft vollständig abdeckt, und rufen Sie dann [itfreadonlyproperty:: GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) auf, um ein [tfguidatom](/windows/desktop/TSF/tfguidatom) abzurufen, das die **CLSID** des Text dienstantexts darstellt Im folgenden Beispiel wird eine Funktion veranschaulicht, die bei Angabe von Kontext, Bereich und Bearbeitungs Cookie die **CLSID** des Text Dienstanbieter erhält, der den Text besitzt.


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



Eigenschaften können auch aufgelistet werden, indem eine [ienumtfproperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) -Schnittstelle von [ITF context:: EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties)erhalten wird.

## <a name="persistent-storage-of-properties"></a>Persistente Speicherung von Eigenschaften

Häufig sind Eigenschaften für eine Anwendung transparent und werden von einem oder mehreren Text Diensten verwendet. Um die Eigenschaften Daten beizubehalten, z. b. beim Speichern in einer Datei, muss eine Anwendung die Eigenschaften Daten bei der Speicherung serialisieren und die Eigenschafts Daten beim Wiederherstellen der Daten wiederherstellen. In diesem Fall sollte die Anwendung nicht an einzelnen Eigenschaften interessiert sein, sondern alle Eigenschaften im Kontext auflisten und speichern.

Beim Speichern von Eigenschaften Daten sollte eine Anwendung die folgenden Schritte ausführen.

1.  Rufen Sie einen eigenschaftenenumerator durch Aufrufen von **ITfContext:: EnumProperties** ab.
2.  Zählen Sie die einzelnen Eigenschaften durch Aufrufen von [ienumtfproperties:: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next)auf.
3.  Rufen Sie für jede Eigenschaft einen Bereichs Enumerator durch Aufrufen von [itfreadonlyproperty:: enumranges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges)ab.
4.  Listet jeden Bereich in der Eigenschaft durch Aufrufen von [ienumtfranges:: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next)auf.
5.  Für jeden Bereich in der-Eigenschaft wird [itextstoreacpservices:: Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) mit der-Eigenschaft, dem Range, einem [tf \_ persistent \_ \_ -Eigenschaften Header \_ ACP-](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) Struktur und einem von der Anwendung implementierten Stream-Objekt aufgerufen.
6.  Schreiben Sie den Inhalt der Überschrift für den **\_ persistenten TF \_ \_ -Eigenschaften Header \_ ACP** in den persistenten Speicher.
7.  Schreiben Sie den Inhalt des Datenstrom Objekts in den persistenten Speicher.
8.  Führen Sie die vorherigen Schritte für alle Bereiche in allen Eigenschaften aus.
9.  Die Anwendung muss eine Art von terminiator in den Stream schreiben, damit beim Wiederherstellen der Daten ein Haltepunkt identifiziert werden kann.


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



**Itextstoreacpservices:: Serialize**[ITF PropertyStore:: Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)

Beim Wiederherstellen von Eigenschaften Daten sollte eine Anwendung die folgenden Schritte ausführen.

1.  Legen Sie den Streamzeiger auf den Anfang der ersten **tf \_ -Struktur der persistenten \_ \_ \_ -Eigenschaften Kopfzeile** fest.
2.  Lesen Sie den beständigen **tf \_ \_ \_ -Eigenschaften Header \_ ACP-** Struktur.
3.  Aufrufen von **ITfContext:: GetProperty** mit dem **guidtype** -Member des **tf-Elements für \_ persistente \_ Eigenschaften \_ Header \_ ACP** .
4.  An dieser Stelle kann die Anwendung eine von zwei Punkten ausführen.
    1.  Erstellen Sie eine Instanz eines [ITF persistentpropertyloaderacp-](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) Objekts, das von der Anwendung implementiert werden muss. Nennen Sie dann [itextstoreacpservices:: unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) mit **null** für *pStream* und den **itfpersistentpropertyloaderacp-** Zeiger.
    2.  Übergeben Sie den Eingabedaten Strom an **itextstoreacpservices:: unserialize** und **null** für *ploader*.

    Die erste Methode wird bevorzugt, da Sie die effizienteste ist. Das Implementieren der zweiten Methode bewirkt, dass alle Eigenschaften Daten während des **itextstoreacpservices:: unserialize** -Aufrufes aus dem Stream gelesen werden. Die erste Methode bewirkt, dass die Eigenschaften Daten zu einem späteren Zeitpunkt bei Bedarf gelesen werden.
5.  Wiederholen Sie die vorherigen Schritte, bis alle Eigenschafts Blöcke unserialisiert sind.


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



 

 
