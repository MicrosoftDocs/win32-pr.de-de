---
title: Verwenden von Anzeigeattributen
description: Erfahren Sie mehr über die Verwendung von Anzeigeattributen. Textdienstframework (TSF) ermöglicht es einem Textdienst, Anzeigeattribute für Text bereitzustellen.
ms.assetid: b0f6e8e8-586a-4b51-a498-fb22bd36161f
keywords:
- Textdienstframework (TSF),Anzeigeattribute
- TSF (Textdienstframework),Anzeigeattribute
- TSF-fähige Anwendungen, Anzeigeattribute
- Anzeigeattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3c576064ab22571b5a7822f5e6ff143add55d03
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406133"
---
# <a name="using-display-attributes"></a>Verwenden von Anzeigeattributen

Textdienstframework (TSF) ermöglicht es einem Textdienst, Anzeigeattribute für Text bereitzustellen. Dadurch kann eine Anwendung zusätzliches visuelles Feedback anzeigen. Beispielsweise kann ein Textdienst für die Rechtschreibprüfung ein falsch geschriebenes Wort mit einer roten Unterstreichung hervorheben. Die Anzeigeattribute, die bereitgestellt werden können, werden von der [TF \_ DISPLAYATTRIBUTE-Struktur](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) definiert und enthalten Textfarbe, Hintergrundfarbe für Text, Unterstreichungsstil, Unterstreichungsfarbe und Unterstreichungsgewichtung.

Beim Rendern von Text sollte eine Anwendung die Anzeigeattribute für den gezeichneten Text abrufen und die Attribute verwenden, um zu ändern, wie der Text gezeichnet wird. Führen Sie die folgenden Schritte aus, um Anzeigeattribute abzurufen.

1.  Rufen Sie ein Eigenschaftenobjekt für GUID \_ PROP \_ ATTRIBUTE ab, indem Sie [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)aufrufen.
2.  Rufen Sie den Wert des GUID \_ PROP ATTRIBUTE für den \_ angegebenen Bereich ab, indem [Sie ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)aufrufen. Dadurch wird ein [TfGuidAtom-Wert](tfguidatom.md) bereitgestellt.
3.  Konvertieren Sie den [TfGuidAtom-Wert](tfguidatom.md) in eine GUID, indem [Sie ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)aufrufen.
4.  Erstellen Sie ein [ITfDisplayAttributeInfo-Objekt](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) für das Anzeigeattribut, indem [Sie ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)aufrufen.
5.  Rufen Sie die Anzeigeattributinformationen ab, indem [Sie ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)aufrufen.

Im folgenden Codebeispiel wird eine Funktion veranschaulicht, die die Anzeigeattribute aus einem angegebenen Kontext, Bereich und Bearbeitungscookie erhält.


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

[TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 ITfDisplayAttributeInfo::GetAttributeInfo 
</dt> </dl>

 

 




