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
# <a name="providing-display-attributes"></a>Bereitstellen von Anzeigeattributen

Textdienstframework (TSF) ermöglicht einem Textdienst das Bereitstellen von Anzeigeattributen für Text. Dadurch kann dem Benutzer zusätzliches visuelles Feedback bereitgestellt werden. Beispielsweise kann ein Textdienst für die Rechtschreibprüfung ein falsch geschriebenes Wort mit einer roten Unterstreichung hervorheben. Die bereitgestellten Anzeigeattribute werden durch die [TF \_ DISPLAYATTRIBUTE-Struktur](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) definiert und umfassen Textfarbe, Hintergrundfarbe des Texts, Unterstreichungsstil, Unterstreichungsfarbe und Unterstreichungsgewichtung.

Clients, die diese Anzeigeattributinformationen verwenden, sind am häufigsten Anwendungen, können aber auch Textdienste enthalten. Der TSF-Manager vermittelt zwischen dem Anzeigeattributanbieter und dem Client und verfolgt den Anzeigeattributanbieter der spezifischen Anzeigeattribute nach.

Um Anzeigeattribute bereitstellen zu können, muss ein Textdienst Folgendes tun.

1.  Registrieren Sie den Textdienst als Anzeigeattributanbieter, indem Sie [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) mit dem Klassenbezeichner des Textdiensts für den ersten Parameter, GUID \_ TFCAT DISPLAYATTRIBUTEPROVIDER für den zweiten Parameter und dem Klassenbezeichner des Textdiensts erneut für den dritten Parameter \_ aufrufen.
2.  Implementieren [Sie ITfDisplayAttributeProvider,](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) und stellen Sie es über die Klassen factory zur Verfügung.
3.  Implementieren [Sie IEnumTfDisplayAttributeInfo,](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) und stellen Sie es über [ITfDisplayAttributeProvider::EnumDisplayAttributeInfo zur Verfügung.](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
4.  Implementieren Sie [ein ITfDisplayAttributeInfo-Objekt](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) für jeden Vom Textdienst bereitgestellten Anzeigeattributtyp.

## <a name="applying-the-display-attributes"></a>Anwenden der Anzeigeattribute

Der Textdienst muss das Anzeigeattribut auf einen Textbereich anwenden. Ein Textdienst kann den Eigenschaftswert nur während einer Lese-/Schreibbearbeitungssitzung ändern.

Wenn dies innerhalb einer Lese-/Schreibbearbeitungssitzung erfolgt, wird ein Anzeigeattribut wie folgt angewendet.

1.  Abrufen eines [ITfRange-Objekts,](/windows/desktop/api/Msctf/nn-msctf-itfrange) das den Text abdeckt, auf den das Anzeigeattribut angewendet wird.
2.  Rufen Sie [ein ITfProperty-Objekt](/windows/desktop/api/Msctf/nn-msctf-itfproperty) für die Textattribute ab, indem [Sie ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) mit GUID \_ PROP ATTRIBUTE \_ aufrufen.
3.  Erstellen Sie ein [TfGuidAtom-Attribut](tfguidatom.md) aus der vom Textdienst definierten Anzeigeattributbezeichner-GUID, indem [Sie ITfCategoryMgr::RegisterGUID aufrufen.](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid) 
4.  Initialisieren Sie eine VARIANT-Variable mit VT I4, und legen Sie den lVal-Member auf das \_ **tfGuidAtom** fest, das im vorherigen Schritt erstellt wurde. 
5.  Wenden Sie das Anzeigeattribut auf den Bereich an, indem [Sie ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) mit dem Lese-/Schreibbearbeitungscookie, dem Bereich und dem VARIANT aufrufen, die im vorherigen Schritt initialisiert wurden.


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



## <a name="supplying-the-display-attribute-information-object"></a>Angeben des Anzeigeattributinformationsobjekts

Ein Client erhält ein **ITfDisplayAttributeInfo-Objekt** auf zwei Arten.

1.  Der Client ruft [ITfDisplayAttributeMgr::GetDisplayAttributeInfo mit](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) dem **GUID-Bezeichner** des Anzeigeattributs auf. Wenn der Client **ITfDisplayAttributeMgr::GetDisplayAttributeInfo** zum ersten Mal aufruft, erstellt der TSF-Manager eine Instanz des Anzeigeattributanbieters, indem er CoCreateInstance mit dem Klassenbezeichner aufruft, der als erster Parameter **an ITfCategoryMgr::RegisterCategory übergeben wird.** Nachfolgende Aufrufe von **ITfDisplayAttributeMgr::GetDisplayAttributeInfo** verwenden das Anzeigeattributanbieterobjekt erneut.

    Der TSF-Manager ruft dann [ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) mit dem Anzeigeattribut **GUID** auf, um das **ITfDisplayAttributeInfo-Objekt zu** erhalten.

    Der TSF-Manager übergibt dann das **ITfDisplayAttributeInfo-Objekt** zurück an den Client.

2.  Der Client ruft [ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) auf, um ein **IEnumTfDisplayAttributeInfo-Objekt** zu erhalten, das alle Anzeigeattribute enthält, die von allen Anzeigeattributanbietern bereitgestellt werden. Der TSF-Manager führt jeden Anzeigeattributanbieter auf und erstellt eine Instanz jedes Anbieters, indem er CoCreateInstance mit dem Klassenbezeichner aufruft, der als dritter Parameter an **ITfCategoryMgr::RegisterCategory** übergeben wird.

    Der TSF-Manager ruft dann den **ITfDisplayAttributeProvider::EnumDisplayAttributeInfo** jedes Anbieters auf, um ein **IEnumTfDisplayAttributeInfo-Objekt** zu erhalten, das alle vom Anbieter bereitgestellten Anzeigeattribute enthält.

    Der TSF-Manager ruft dann die [IEnumTfDisplayAttributeInfo::Next-Methode](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) des Anbieters auf und fügt jedes **ITfDisplayAttributeInfo-Objekt** hinzu, das dem eigenen Enumerator des Managers abgerufen wurde, bis das Ende der Anbieterenumeration erreicht ist.

    Wenn alle **ITfDisplayAttributeInfo-Objekte** für alle Anzeigeattributanbieter dem Enumerator des TSF-Managers hinzugefügt werden, gibt der Manager seinen Enumerator an den Client zurück. Der Client ruft dann **mindestens einmal IEnumTfDisplayAttributeInfo::Next** auf, um die **ITfDisplayAttributeInfo-Objekte zu** erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 IEnumTfDisplayAttributeInfo 
</dt> <dt>

 ITfDisplayAttributeProvider::EnumDisplayAttributeInfo 
</dt> <dt>

[IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 




