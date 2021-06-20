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
# <a name="using-display-attributes"></a><span data-ttu-id="2499b-108">Verwenden von Anzeigeattributen</span><span class="sxs-lookup"><span data-stu-id="2499b-108">Using Display Attributes</span></span>

<span data-ttu-id="2499b-109">Textdienstframework (TSF) ermöglicht es einem Textdienst, Anzeigeattribute für Text bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2499b-109">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="2499b-110">Dadurch kann eine Anwendung zusätzliches visuelles Feedback anzeigen.</span><span class="sxs-lookup"><span data-stu-id="2499b-110">This enables an application to display additional visual feedback.</span></span> <span data-ttu-id="2499b-111">Beispielsweise kann ein Textdienst für die Rechtschreibprüfung ein falsch geschriebenes Wort mit einer roten Unterstreichung hervorheben.</span><span class="sxs-lookup"><span data-stu-id="2499b-111">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="2499b-112">Die Anzeigeattribute, die bereitgestellt werden können, werden von der [TF \_ DISPLAYATTRIBUTE-Struktur](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) definiert und enthalten Textfarbe, Hintergrundfarbe für Text, Unterstreichungsstil, Unterstreichungsfarbe und Unterstreichungsgewichtung.</span><span class="sxs-lookup"><span data-stu-id="2499b-112">The display attributes that can be provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="2499b-113">Beim Rendern von Text sollte eine Anwendung die Anzeigeattribute für den gezeichneten Text abrufen und die Attribute verwenden, um zu ändern, wie der Text gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="2499b-113">When rendering text, an application should obtain the display attributes for the text drawn and use the attributes to modify how the text is drawn.</span></span> <span data-ttu-id="2499b-114">Führen Sie die folgenden Schritte aus, um Anzeigeattribute abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2499b-114">Complete the following steps to obtain display attributes.</span></span>

1.  <span data-ttu-id="2499b-115">Rufen Sie ein Eigenschaftenobjekt für GUID \_ PROP \_ ATTRIBUTE ab, indem Sie [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2499b-115">Obtain a property object for GUID\_PROP\_ATTRIBUTE by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).</span></span>
2.  <span data-ttu-id="2499b-116">Rufen Sie den Wert des GUID \_ PROP ATTRIBUTE für den \_ angegebenen Bereich ab, indem [Sie ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2499b-116">Obtain the value of the GUID\_PROP\_ATTRIBUTE for the specified range by calling [ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue).</span></span> <span data-ttu-id="2499b-117">Dadurch wird ein [TfGuidAtom-Wert](tfguidatom.md) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2499b-117">This supplies a [TfGuidAtom](tfguidatom.md) value.</span></span>
3.  <span data-ttu-id="2499b-118">Konvertieren Sie den [TfGuidAtom-Wert](tfguidatom.md) in eine GUID, indem [Sie ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2499b-118">Convert the [TfGuidAtom](tfguidatom.md) value into a GUID by calling [ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).</span></span>
4.  <span data-ttu-id="2499b-119">Erstellen Sie ein [ITfDisplayAttributeInfo-Objekt](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) für das Anzeigeattribut, indem [Sie ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2499b-119">Create an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for the display attribute by calling [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>
5.  <span data-ttu-id="2499b-120">Rufen Sie die Anzeigeattributinformationen ab, indem [Sie ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2499b-120">Obtain the display attribute information by calling [ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>

<span data-ttu-id="2499b-121">Im folgenden Codebeispiel wird eine Funktion veranschaulicht, die die Anzeigeattribute aus einem angegebenen Kontext, Bereich und Bearbeitungscookie erhält.</span><span class="sxs-lookup"><span data-stu-id="2499b-121">The following code example demonstrates a function that obtains the display attributes from a supplied context, range, and edit cookie.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2499b-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2499b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2499b-123">TF \_ DISPLAYATTRIBUTE</span><span class="sxs-lookup"><span data-stu-id="2499b-123">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="2499b-124">ITfContext::GetProperty</span><span class="sxs-lookup"><span data-stu-id="2499b-124">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="2499b-125">ITfReadOnlyProperty::GetValue</span><span class="sxs-lookup"><span data-stu-id="2499b-125">ITfReadOnlyProperty::GetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[<span data-ttu-id="2499b-126">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="2499b-126">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="2499b-127">ITfCategoryMgr::GetGUID</span><span class="sxs-lookup"><span data-stu-id="2499b-127">ITfCategoryMgr::GetGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="2499b-128">ITfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="2499b-128">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="2499b-129">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="2499b-129">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="2499b-130">ITfDisplayAttributeInfo::GetAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="2499b-130">ITfDisplayAttributeInfo::GetAttributeInfo</span></span> 
</dt> </dl>

 

 




