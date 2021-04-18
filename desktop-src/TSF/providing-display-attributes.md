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
# <a name="providing-display-attributes"></a>Bereitstellen von Anzeige Attributen

Mit dem Text Services-Framework (TSF) kann ein Text Dienst Anzeige Attribute für Text bereitstellen. Dadurch kann dem Benutzer zusätzliches visuelles Feedback bereitgestellt werden. Ein Rechtschreibprüfung-Text Dienst kann z. b. ein falsch geschriebenes Wort mit einer roten Unterstreichung markieren. Die angegebenen Anzeige Attribute werden durch die [tf \_ DisplayAttribute](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) -Struktur definiert und enthalten Textfarbe, Text Hintergrundfarbe, unterstrich Farbe, unterstrich Farbe und unterstrich Gewichtung.

Clients, die diese Anzeige Attributinformationen verwenden, sind meist Anwendungen, können aber auch Text Dienste enthalten. Der TSF-Manager mediiert zwischen dem Anzeige Attribut Anbieter und dem Client und verfolgt den Anzeige Attribut Anbieter der spezifischen Anzeige Attribute nach.

Zum Bereitstellen von Anzeige Attributen muss ein Text Dienst folgende Aktionen ausführen.

1.  Registrieren Sie den Text Dienst als Anzeige Attribut Anbieter durch Aufrufen von [itfcategorymgr:: registercategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) mit dem Klassen Bezeichner des Text Dienstanbieters für den ersten Parameter, GUID \_ tfcat \_ displayattributeprovider für den zweiten Parameter und der Klassen Bezeichner des Text Dienstanbieters für den dritten Parameter.
2.  Implementieren Sie [ITF displayattributeprovider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) , und stellen Sie Sie aus der Klassenfactory zur Verfügung.
3.  Implementieren Sie [ienumtfdisplayattributeinfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) , und stellen Sie Sie über [ITF displayattributeprovider:: enumdisplayattributeinfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)zur Verfügung.
4.  Implementieren Sie ein [ITF displayattributeinfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) -Objekt für jeden Typ von Anzeige Attribut, den der Text Dienst bereitstellt.

## <a name="applying-the-display-attributes"></a>Anwenden der Anzeige Attribute

Der Text Dienst muss das Anzeige Attribut auf einen Textbereich anwenden. Ein Text Dienst kann den Eigenschafts Wert nur während einer Sitzung mit Lese-/schreibbearbeitung ändern.

Wenn dies in einer Sitzung mit Lese-/schreibbearbeitung erfolgt, wird ein Anzeige Attribut wie folgt angewendet.

1.  Rufen Sie ein [itfrange](/windows/desktop/api/Msctf/nn-msctf-itfrange) -Objekt ab, das den Text abdeckt, auf den das Anzeige Attribut angewendet wird.
2.  Rufen Sie ein [itfproperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) -Objekt für die Text Attribute ab, indem Sie [ITfContext:: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) mit dem GUID- \_ Prop-Attribut aufrufen \_ .
3.  Erstellen Sie ein [tfguidatom](tfguidatom.md) aus der durch den Text Dienst definierten **GUID** des Anzeige Attribut Bezeichners durch Aufrufen von [itfcategorymgr:: registerguid](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).
4.  Initialisieren Sie eine Variant-Variable zu VT \_ I4, und legen Sie den **LVAL** -Member auf das im vorherigen Schritt erstellte **tfguidatom** fest.
5.  Wenden Sie das Anzeige Attribut auf den Bereich an, indem Sie [itfproperty:: SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) mit dem Cookie für die Lese-/schreibbearbeitung aufrufen, den Bereich und die Variante, die im vorherigen Schritt initialisiert wurden.


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



## <a name="supplying-the-display-attribute-information-object"></a>Bereitstellen des Anzeige Attribut Informationsobjekts

Ein Client erhält ein **ITF displayattributeinfo** -Objekt auf zwei Arten.

1.  Der Client ruft [ITF displayattributemgr:: getdisplayattributeinfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) mit dem **GUID** -Bezeichner des Anzeige Attributs auf. Wenn der Client zum ersten Mal **itfdisplayattributemgr:: getdisplayattributeinfo** aufruft, erstellt der TSF-Manager eine Instanz des Anzeige Attribut Anbieters durch Aufrufen von CoCreateInstance mit dem Klassen Bezeichner, der als erster Parameter an **itfcategorymgr:: registercategory** übergeben wird. Bei nachfolgenden Aufrufen von **itfdisplayattributemgr:: getdisplayattributeinfo** wird das Display Attribute Provider-Objekt wieder verwendet.

    Der TSF-Manager ruft dann [itfdisplayattributeprovider:: getdisplayattributeinfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) mit dem Display-Attribut **GUID** auf, um das **itfdisplayattributeinfo** -Objekt abzurufen.

    Der TSF-Manager übergibt dann das **itfdisplayattributeinfo** -Objekt an den Client zurück.

2.  Der Client ruft [itfdisplayattributemgr:: enumdisplayattributeinfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) auf, um ein **ienumtfdisplayattributeinfo** -Objekt zu erhalten, das alle Anzeige Attribute enthält, die von allen Anzeige Attribut Anbietern bereitgestellt werden. Der TSF-Manager listet jeden Anzeige Attribut Anbieter auf und erstellt eine Instanz jedes Anbieters durch Aufrufen von CoCreateInstance mit dem Klassen Bezeichner, der als dritter Parameter an **itfcategorymgr:: registercategory** übergeben wird.

    Der TSF-Manager ruft dann den **itfdisplayattributeprovider:: enumdisplayattributeinfo** jedes Anbieters auf, um ein **ienumtfdisplayattributeinfo** -Objekt zu erhalten, das alle vom Anbieter bereitgestellten Anzeige Attribute enthält.

    Der TSF-Manager ruft dann die [ienumtfdisplayattributeinfo:: Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) -Methode des Anbieters auf und fügt jedes **itfdisplayattributeinfo** -Objekt hinzu, das dem eigenen Enumerator des Managers abgerufen wurde, bis das Ende der Enumeration des Anbieters erreicht ist.

    Wenn alle **itfdisplayattributeinfo** -Objekte für alle Anzeige Attribut Anbieter dem Enumerator von TSF-Manager hinzugefügt werden, gibt der Manager seinen Enumerator an den Client zurück. Der Client ruft dann **ienumtfdisplayattributeinfo:: Next** einmal oder mehrmals auf, um die **itfdisplayattributeinfo** -Objekte abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[TF \_ DisplayAttribute](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[ITF categorymgr:: registercategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[ITF displayattributeprovider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[Ienumtfdisplayattributeinfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[ITF displayattributeprovider:: enumdisplayattributeinfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[ITF displayattributeinfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[Itfrange](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[ITF Property](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[ITF context:: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[Tfguidatom](tfguidatom.md)
</dt> <dt>

[ITF categorymgr:: registerguid](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[ITF Property:: SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[ITF displayattributemgr:: getdisplayattributeinfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[ITF displayattributeprovider:: getdisplayattributeinfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[ITF displayattributemgr:: enumdisplayattributeinfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 Ienumtfdisplayattributeinfo 
</dt> <dt>

 ITF displayattributeprovider:: enumdisplayattributeinfo 
</dt> <dt>

[Ienumtfdisplayattributeinfo:: Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 




