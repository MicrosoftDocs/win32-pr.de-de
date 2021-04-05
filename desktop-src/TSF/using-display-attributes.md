---
title: Verwenden von Anzeige Attributen
description: Mit dem Text Services-Framework (TSF) kann ein Text Dienst Anzeige Attribute für Text bereitstellen.
ms.assetid: b0f6e8e8-586a-4b51-a498-fb22bd36161f
keywords:
- Text Dienst Framework (TSF), Attribute anzeigen
- TSF (Text Dienste-Framework), Anzeige Attribute
- TSF-aktivierte Anwendungen, Anzeigen von Attributen
- Anzeigeattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc725f67fab904db23f6232ac5efb5d63c62c26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708345"
---
# <a name="using-display-attributes"></a>Verwenden von Anzeige Attributen

Mit dem Text Services-Framework (TSF) kann ein Text Dienst Anzeige Attribute für Text bereitstellen. Dies ermöglicht es einer Anwendung, zusätzliches visuelles Feedback anzuzeigen. Ein Rechtschreibprüfung-Text Dienst kann z. b. ein falsch geschriebenes Wort mit einer roten Unterstreichung markieren. Die Anzeige Attribute, die bereitgestellt werden können, werden durch die [tf \_ DisplayAttribute](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) -Struktur definiert und enthalten Textfarbe, Text Hintergrundfarbe, unterstrich-Stil, unterstrich Farbe und unterstrich Gewichtung.

Beim Rendern von Text sollte eine Anwendung die Anzeige Attribute für den gezeichneten Text abrufen und die Attribute verwenden, um die Art und Weise zu ändern, wie der Text gezeichnet wird. Führen Sie die folgenden Schritte aus, um Anzeige Attribute abzurufen.

1.  Rufen Sie ein Eigenschafts Objekt für das GUID- \_ Prop- \_ Attribut durch Aufrufen von [ITfContext:: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)ab.
2.  Rufen Sie den Wert des GUID- \_ Prop- \_ Attributs für den angegebenen Bereich durch Aufrufen von [itfreadonlyproperty:: GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)ab. Dadurch wird ein [tfguidatom](tfguidatom.md) -Wert bereitstellt.
3.  Konvertieren Sie den [tfguidatom](tfguidatom.md) -Wert durch Aufrufen von [itfcategorymgr:: GetGuid](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)in eine GUID.
4.  Erstellen Sie ein [itfdisplayattributeinfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) -Objekt für das Anzeige Attribut, indem Sie [itfdisplayattributemgr:: getdisplayattributeinfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)aufrufen.
5.  Rufen Sie die Anzeige Attributinformationen durch Aufrufen von [itfdisplayattributeinfo:: getattributeinfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)ab.

Im folgenden Codebeispiel wird eine Funktion veranschaulicht, die die Anzeige Attribute aus einem angegebenen Kontext, Bereich und Bearbeitungs Cookie abruft.


```C++
HRESULT GetDispAttrFromRange(   ITfContext *pContext, 
                                ITfRange *pRange, 
                                TfEditCookie ec, 
                                TF_DISPLAYATTRIBUTE *pDispAttr)
{
    HRESULT     hr;
    
    //Create the category manager. 
    ITfCategoryMgr  *pCategoryMgr;
    hr = CoCreateInstance(  CLSID_TF_CategoryMgr,
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_ITfCategoryMgr, 
                            (LPVOID*)&pCategoryMgr);
    if(FAILED(hr))
    {
        return hr;
    }

    //Create the display attribute manager. 
    ITfDisplayAttributeMgr  *pDispMgr;
    hr = CoCreateInstance(  CLSID_TF_DisplayAttributeMgr,
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_ITfDisplayAttributeMgr, 
                            (LPVOID*)&pDispMgr);
    if(FAILED(hr))
    {
        pCategoryMgr->Release();
        return hr;
    }
    
    //Get the display attribute property. 
    ITfProperty *pProp;
    hr = pContext->GetProperty(GUID_PROP_ATTRIBUTE, &pProp);
    if(SUCCEEDED(hr))
    {
        VARIANT var;

        VariantInit(&var);
        hr = pProp->GetValue(ec, pRange, &var);
        if(S_OK == hr)  //Returns S_FALSE if the range is not completely covered by the property.  
        {
            if(VT_I4 == var.vt)
            {
                //The property is a guidatom. 
                GUID    guid;

                //Convert the guidatom into a GUID. 
                hr = pCategoryMgr->GetGUID((TfGuidAtom)var.lVal, &guid);
                if(SUCCEEDED(hr))
                {
                    ITfDisplayAttributeInfo *pDispInfo;

                    //Get the display attribute info object for this attribute. 
                    hr = pDispMgr->GetDisplayAttributeInfo(guid, &pDispInfo, NULL);
                    if(SUCCEEDED(hr))
                    {
                        //Get the display attribute info. 
                        hr = pDispInfo->GetAttributeInfo(pDispAttr);

                        pDispInfo->Release();
                    }
                }
            }
            else
            {
                //An error occurred; GUID_PROP_ATTRIBUTE must always be VT_I4. 
                hr = E_FAIL;
            }
            VariantClear(&var);
        }
    pProp->Release();
    }

    pCategoryMgr->Release();
    pDispMgr->Release();

    return hr;
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[TF \_ DisplayAttribute](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[ITF context:: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[Itfreadonlyproperty:: GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[Tfguidatom](tfguidatom.md)
</dt> <dt>

[ITF categorymgr:: GetGuid](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[ITF displayattributeinfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[ITF displayattributemgr:: getdisplayattributeinfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 ITF displayattributeinfo:: getattributeinfo 
</dt> </dl>

 

 




