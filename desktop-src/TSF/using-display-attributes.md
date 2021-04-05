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
# <a name="using-display-attributes"></a><span data-ttu-id="32572-107">Verwenden von Anzeige Attributen</span><span class="sxs-lookup"><span data-stu-id="32572-107">Using Display Attributes</span></span>

<span data-ttu-id="32572-108">Mit dem Text Services-Framework (TSF) kann ein Text Dienst Anzeige Attribute für Text bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="32572-108">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="32572-109">Dies ermöglicht es einer Anwendung, zusätzliches visuelles Feedback anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="32572-109">This enables an application to display additional visual feedback.</span></span> <span data-ttu-id="32572-110">Ein Rechtschreibprüfung-Text Dienst kann z. b. ein falsch geschriebenes Wort mit einer roten Unterstreichung markieren.</span><span class="sxs-lookup"><span data-stu-id="32572-110">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="32572-111">Die Anzeige Attribute, die bereitgestellt werden können, werden durch die [tf \_ DisplayAttribute](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) -Struktur definiert und enthalten Textfarbe, Text Hintergrundfarbe, unterstrich-Stil, unterstrich Farbe und unterstrich Gewichtung.</span><span class="sxs-lookup"><span data-stu-id="32572-111">The display attributes that can be provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="32572-112">Beim Rendern von Text sollte eine Anwendung die Anzeige Attribute für den gezeichneten Text abrufen und die Attribute verwenden, um die Art und Weise zu ändern, wie der Text gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="32572-112">When rendering text, an application should obtain the display attributes for the text drawn and use the attributes to modify how the text is drawn.</span></span> <span data-ttu-id="32572-113">Führen Sie die folgenden Schritte aus, um Anzeige Attribute abzurufen.</span><span class="sxs-lookup"><span data-stu-id="32572-113">Complete the following steps to obtain display attributes.</span></span>

1.  <span data-ttu-id="32572-114">Rufen Sie ein Eigenschafts Objekt für das GUID- \_ Prop- \_ Attribut durch Aufrufen von [ITfContext:: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)ab.</span><span class="sxs-lookup"><span data-stu-id="32572-114">Obtain a property object for GUID\_PROP\_ATTRIBUTE by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).</span></span>
2.  <span data-ttu-id="32572-115">Rufen Sie den Wert des GUID- \_ Prop- \_ Attributs für den angegebenen Bereich durch Aufrufen von [itfreadonlyproperty:: GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)ab.</span><span class="sxs-lookup"><span data-stu-id="32572-115">Obtain the value of the GUID\_PROP\_ATTRIBUTE for the specified range by calling [ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue).</span></span> <span data-ttu-id="32572-116">Dadurch wird ein [tfguidatom](tfguidatom.md) -Wert bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="32572-116">This supplies a [TfGuidAtom](tfguidatom.md) value.</span></span>
3.  <span data-ttu-id="32572-117">Konvertieren Sie den [tfguidatom](tfguidatom.md) -Wert durch Aufrufen von [itfcategorymgr:: GetGuid](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)in eine GUID.</span><span class="sxs-lookup"><span data-stu-id="32572-117">Convert the [TfGuidAtom](tfguidatom.md) value into a GUID by calling [ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).</span></span>
4.  <span data-ttu-id="32572-118">Erstellen Sie ein [itfdisplayattributeinfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) -Objekt für das Anzeige Attribut, indem Sie [itfdisplayattributemgr:: getdisplayattributeinfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="32572-118">Create an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for the display attribute by calling [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>
5.  <span data-ttu-id="32572-119">Rufen Sie die Anzeige Attributinformationen durch Aufrufen von [itfdisplayattributeinfo:: getattributeinfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)ab.</span><span class="sxs-lookup"><span data-stu-id="32572-119">Obtain the display attribute information by calling [ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>

<span data-ttu-id="32572-120">Im folgenden Codebeispiel wird eine Funktion veranschaulicht, die die Anzeige Attribute aus einem angegebenen Kontext, Bereich und Bearbeitungs Cookie abruft.</span><span class="sxs-lookup"><span data-stu-id="32572-120">The following code example demonstrates a function that obtains the display attributes from a supplied context, range, and edit cookie.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="32572-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="32572-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32572-122">TF \_ DisplayAttribute</span><span class="sxs-lookup"><span data-stu-id="32572-122">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="32572-123">ITF context:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="32572-123">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="32572-124">Itfreadonlyproperty:: GetValue</span><span class="sxs-lookup"><span data-stu-id="32572-124">ITfReadOnlyProperty::GetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[<span data-ttu-id="32572-125">Tfguidatom</span><span class="sxs-lookup"><span data-stu-id="32572-125">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="32572-126">ITF categorymgr:: GetGuid</span><span class="sxs-lookup"><span data-stu-id="32572-126">ITfCategoryMgr::GetGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="32572-127">ITF displayattributeinfo</span><span class="sxs-lookup"><span data-stu-id="32572-127">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="32572-128">ITF displayattributemgr:: getdisplayattributeinfo</span><span class="sxs-lookup"><span data-stu-id="32572-128">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="32572-129">ITF displayattributeinfo:: getattributeinfo</span><span class="sxs-lookup"><span data-stu-id="32572-129">ITfDisplayAttributeInfo::GetAttributeInfo</span></span> 
</dt> </dl>

 

 




