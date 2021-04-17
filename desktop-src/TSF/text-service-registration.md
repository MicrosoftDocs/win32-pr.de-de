---
title: Text Dienst Registrierung
description: Zusätzlich zu den standardmäßigen com-in-proc Server-Registrierungs Einträgen muss sich ein Text Dienst selbst beim Text Services-Framework (TSF) registrieren, damit er für die Verwendung mit einer Anwendung verfügbar ist.
ms.assetid: 95676067-ab5c-470b-a4be-117ab6810d48
keywords:
- Text Dienst Framework (TSF), Registrierung
- TSF (Text Dienst Framework), Registrierung
- Text Dienste, Registrierung
- Text Dienst Framework (TSF), sprach profile
- TSF (Text Services Framework), sprach profile
- Text Dienste, sprach profile
- Text Dienst Framework (TSF), Kategorien
- TSF (Text Dienst Framework), Kategorien
- Text Dienste, Kategorien
- Registrieren von Text Diensten
- Registrieren von sprach Profilen
- Kategorien werden registriert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc1b91ad1a3b1fde9a2e49b92950ce2db4876f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473628"
---
# <a name="text-service-registration"></a><span data-ttu-id="a0b47-115">Text Dienst Registrierung</span><span class="sxs-lookup"><span data-stu-id="a0b47-115">Text Service Registration</span></span>

<span data-ttu-id="a0b47-116">Zusätzlich zu den standardmäßigen com-in-proc Server-Registrierungs Einträgen muss sich ein Text Dienst selbst beim Text Services-Framework (TSF) registrieren, damit er für die Verwendung mit einer Anwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a0b47-116">In addition to the standard COM in-proc server registry entries, a text service must register itself with the Text Services Framework (TSF) so that it can be available for use with an application.</span></span> <span data-ttu-id="a0b47-117">TSF stellt die Schnittstelle [itfinputprocessorprofiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) und [itfcategorymgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) bereit, um den Registrierungsprozess zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="a0b47-117">TSF supplies the [ITfInputProcessorProfiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) and [ITfCategoryMgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) interface to simplify the registration process.</span></span>

<span data-ttu-id="a0b47-118">Text Dienstanbieter sollten auch digitale Signaturen mit Ihren binären ausführbaren Dateien bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a0b47-118">Text service providers should also provide digital signatures with their binary executables.</span></span> <span data-ttu-id="a0b47-119">Siehe [Einführung in die Code Signatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a0b47-119">See [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span></span>

## <a name="registering-the-text-service"></a><span data-ttu-id="a0b47-120">Registrieren des Text Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a0b47-120">Registering the Text Service</span></span>

<span data-ttu-id="a0b47-121">Ein Text Dienst registriert sich bei TSF durch Aufrufen von [itfinputprocessorprofiles:: Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) mit dem Klassen Bezeichner des Text dienstanzdienstaners.</span><span class="sxs-lookup"><span data-stu-id="a0b47-121">A text service registers itself with TSF by calling [ITfInputProcessorProfiles::Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) with the class identifier of the text service.</span></span> <span data-ttu-id="a0b47-122">Eine Instanz der **itfinputprocessorprofiles** -Schnittstelle wird durch Aufrufen von **CoCreateInstance** mit CLSID \_ tf \_ inputprocessorprofiles abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a0b47-122">An instance of the **ITfInputProcessorProfiles** interface is obtained by calling **CoCreateInstance** with CLSID\_TF\_InputProcessorProfiles.</span></span>

<span data-ttu-id="a0b47-123">Im folgenden Beispiel wird veranschaulicht, wie ein **itfinputprocessorprofiles** -Objekt erstellt und der Text Dienst registriert wird.</span><span class="sxs-lookup"><span data-stu-id="a0b47-123">The following example demonstrates how to create an **ITfInputProcessorProfiles** object and register the text service.</span></span>


```C++
BOOL RegisterTextService(CLSID clsidTextService)
{
    HRESULT hr;
    ITfInputProcessorProfiles *pInputProcessProfiles;

    hr = CoCreateInstance(  CLSID_TF_InputProcessorProfiles, 
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_ITfInputProcessorProfiles, 
                            (LPVOID*)&pInputProcessProfiles);

    if (hr != S_OK)
    {
        return FALSE;
    }

    hr = pInputProcessProfiles->Register(clsidTextService);

    pInputProcessProfiles->Release();
    
    return (S_OK == hr);
}
```



[<span data-ttu-id="a0b47-124">Itfinputprocessorprofiles:: Unregister</span><span class="sxs-lookup"><span data-stu-id="a0b47-124">ITfInputProcessorProfiles::Unregister</span></span>](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-unregister)

## <a name="registering-language-profiles"></a><span data-ttu-id="a0b47-125">Registrieren von sprach Profilen</span><span class="sxs-lookup"><span data-stu-id="a0b47-125">Registering Language Profiles</span></span>

<span data-ttu-id="a0b47-126">Ein Text Dienst ist nur verfügbar, wenn eine Anwendung den Fokus besitzt und in der sprach Leiste die richtige Sprache ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a0b47-126">A text service is only available when an application has the focus and the proper language is selected in the language bar.</span></span> <span data-ttu-id="a0b47-127">Um dies zu vereinfachen, erfordert TSF, dass sich ein Text Dienst selbst für alle unterstützten Sprachen registriert.</span><span class="sxs-lookup"><span data-stu-id="a0b47-127">To facilitate this, TSF requires that a text service register itself for all of the languages that it supports.</span></span> <span data-ttu-id="a0b47-128">Der Text Dienst registriert seine sprach Profile durch Aufrufen von [itfinputprocessorprofiles:: addlanguageprofile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) mit dem Text Dienst-Klassen Bezeichner, dem sprach Bezeichner des Profils und einer durch den Text Dienst definierten **GUID** , die das Sprachprofil identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a0b47-128">The text service registers its language profiles by calling [ITfInputProcessorProfiles::AddLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) with the text service class identifier, that language identifier of the profile, and a text service defined **GUID** that identifies the language profile.</span></span>

<span data-ttu-id="a0b47-129">Ein Sprachprofil kann durch Aufrufen von [itfinputprocessorprofiles:: removelanguageprofile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile)entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a0b47-129">A language profile can be removed by calling [ITfInputProcessorProfiles::RemoveLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile).</span></span> <span data-ttu-id="a0b47-130">**Itfinputprocessorprofiles:: unregister** entfernt alle sprach Profile für den Text Dienst. Wenn ein Text Dienst deinstalliert wird, müssen die einzelnen sprach Profile entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a0b47-130">**ITfInputProcessorProfiles::Unregister** removes all language profiles for the text service; when a text service is uninstalled, it does require removal of the individual language profiles.</span></span>

## <a name="registering-categories"></a><span data-ttu-id="a0b47-131">Kategorien werden registriert</span><span class="sxs-lookup"><span data-stu-id="a0b47-131">Registering Categories</span></span>

<span data-ttu-id="a0b47-132">Ein Text Dienst muss auch die Kategorie registrieren, für die der Text Dienst gilt.</span><span class="sxs-lookup"><span data-stu-id="a0b47-132">A text service must also register the category that the text service applies to.</span></span> <span data-ttu-id="a0b47-133">Wenn der Text Dienst beispielsweise Anzeige Attributinformationen liefert, muss er sich selbst als Anzeige Attribut Anbieter registrieren, indem [itfcategorymgr:: registercategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) mit dem Klassen Bezeichner des Text Dienstanbieters für den ersten Parameter, GUID \_ tfcat \_ displayattributeprovider für den zweiten Parameter und der Klassen Bezeichner des Text Dienstanbieters für den dritten Parameter.</span><span class="sxs-lookup"><span data-stu-id="a0b47-133">For example, if the text service supplies display attribute information, it must register itself as a display attribute provider by calling [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) with the class identifier of the text service for the first parameter, GUID\_TFCAT\_DISPLAYATTRIBUTEPROVIDER for the second parameter and the class identifier of the text service again for the third parameter.</span></span> <span data-ttu-id="a0b47-134">Die möglichen Kategorien sind unter [vordefinierte Kategoriewerte](predefined-category-values.md)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0b47-134">The possible categories are listed under [Predefined Category Values](predefined-category-values.md).</span></span>

<span data-ttu-id="a0b47-135">Entfernen Sie zuvor registrierte Kategorien durch Aufrufen von [itfcategorymgr:: unregistercategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory).</span><span class="sxs-lookup"><span data-stu-id="a0b47-135">Remove previously registered categories by calling [ITfCategoryMgr::UnregisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory).</span></span> <span data-ttu-id="a0b47-136">Itfinputprocessorprofiles:: unregister entfernt alle Kategorien für den Text Dienst. Wenn ein Text Dienst deinstalliert wird, müssen die einzelnen Kategorien entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a0b47-136">ITfInputProcessorProfiles::Unregister removes all categories for the text service; when a text service is uninstalled, it must remove the individual categories.</span></span>

 

 