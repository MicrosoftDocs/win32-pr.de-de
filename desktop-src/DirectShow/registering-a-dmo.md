---
description: Registrieren eines DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: Registrieren eines DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c5364304fd5f6a9557c84a4b27c86d29fa4e84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346593"
---
# <a name="registering-a-dmo"></a><span data-ttu-id="76d2e-103">Registrieren eines DMO</span><span class="sxs-lookup"><span data-stu-id="76d2e-103">Registering a DMO</span></span>

<span data-ttu-id="76d2e-104">Damit Clients ihren DMO verwenden können, muss die CLSID auf dem System des Benutzers registriert werden.</span><span class="sxs-lookup"><span data-stu-id="76d2e-104">In order for clients to use your DMO, the CLSID must be registered on the user's system.</span></span> <span data-ttu-id="76d2e-105">Dies erfolgt über die **DllRegisterServer** -Funktion der dll.</span><span class="sxs-lookup"><span data-stu-id="76d2e-105">This is done through the DLL's **DllRegisterServer** function.</span></span> <span data-ttu-id="76d2e-106">Wenn Sie die Active Template Library (ATL) verwenden, wird diese Funktion vom ATL-Assistenten automatisch generiert.</span><span class="sxs-lookup"><span data-stu-id="76d2e-106">If you are using the Active Template Library (ATL), the ATL wizard automatically generates this function.</span></span>

<span data-ttu-id="76d2e-107">Sie können Ihre DMO auch unter mindestens einer DMO-Standard Kategorie registrieren.</span><span class="sxs-lookup"><span data-stu-id="76d2e-107">You can also register your DMO under one or more standard DMO categories.</span></span> <span data-ttu-id="76d2e-108">Dadurch können Clients ihre DMO mithilfe der [**dmoenum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) -Funktion ermitteln.</span><span class="sxs-lookup"><span data-stu-id="76d2e-108">This enables clients to discover your DMO using the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function.</span></span> <span data-ttu-id="76d2e-109">Die Kategorien werden durch die GUID definiert und sind im Abschnitt [DMO GUIDs](dmo-guids.md)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="76d2e-109">The categories are defined by GUID, and are listed in the section [DMO GUIDs](dmo-guids.md).</span></span>

<span data-ttu-id="76d2e-110">Das Registrieren eines DMO unter einer Kategorie ist optional.</span><span class="sxs-lookup"><span data-stu-id="76d2e-110">Registering a DMO under a category is optional.</span></span> <span data-ttu-id="76d2e-111">Dazu müssen Sie die [**dmoregiester**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) -Funktion und den anzeigen amen des DMO, der CLSID und der Kategorie angeben.</span><span class="sxs-lookup"><span data-stu-id="76d2e-111">To do so, call the [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) function and specify the friendly name of the DMO, the CLSID, and the category.</span></span> <span data-ttu-id="76d2e-112">Optional können Sie auch einen Satz von Medientypen registrieren, die von ihren DMOS unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="76d2e-112">Optionally, you can also register a set of media types that your DMOs supports.</span></span> <span data-ttu-id="76d2e-113">Weitere Informationen finden Sie unter [DMO Media Types](dmo-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="76d2e-113">For more information, see [DMO Media Types](dmo-media-types.md).</span></span>

<span data-ttu-id="76d2e-114">Im folgenden Beispiel wird gezeigt, wie Sie einen Audioeffekt-DMO registrieren, der PCM-Audioeingabe und-Ausgabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="76d2e-114">The following example shows how to register an audio effect DMO that supports PCM audio input and output.</span></span> <span data-ttu-id="76d2e-115">In diesem Fall sind die Eingabe-und Ausgabetypen identisch.</span><span class="sxs-lookup"><span data-stu-id="76d2e-115">In this case the input types and output types are the same.</span></span>


```C++
STDAPI DllRegisterServer(void)
{
    // Register the DMO as a PCM audio effect DMO
    DMO_PARTIAL_MEDIATYPE mt;
    mt.type    = MEDIATYPE_Audio;
    mt.subtype = MEDIASUBTYPE_PCM;
    HRESULT hr = DMORegister(
        L"MyDMO",                  // Friendly name
        CLSID_MyDMO,               // CLSID
        DMOCATEGORY_AUDIO_EFFECT,  // Category
        0,                         // Flags 
        1,                         // Number of input types
        &mt,                       // Array of input types
        1,                         // Number of output types
        &mt);                      // Array of output types

    if (FAILED(hr)) return hr;

    // Registers the object, with no typelib.
    return _Module.RegisterServer(FALSE);
}
```



<span data-ttu-id="76d2e-116">In diesem Beispiel wird davon ausgegangen, dass ATL zum Erstellen des Projekts verwendet wurde. die letzte Zeile der-Funktion Ruft die Standard-ATL-Methode auf, um den com-Server zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="76d2e-116">This example assumes that ATL was used to create the project; the last line of the function calls the standard ATL method to register the COM server.</span></span> <span data-ttu-id="76d2e-117">Wenn Sie ATL nicht verwenden, sieht die Funktion anders aus.</span><span class="sxs-lookup"><span data-stu-id="76d2e-117">If you are not using ATL, your function will look different.</span></span>

<span data-ttu-id="76d2e-118">**Aufheben der Registrierung eines DMO**</span><span class="sxs-lookup"><span data-stu-id="76d2e-118">**Unregistering a DMO**</span></span>

<span data-ttu-id="76d2e-119">Die **DllUnregisterServer** -Funktion muss alle Registrierungseinträge entfernen, die von der **DllRegisterServer** -Funktion erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="76d2e-119">Your **DllUnregisterServer** function must remove any registry entries that the **DllRegisterServer** function creates.</span></span> <span data-ttu-id="76d2e-120">Wenn Sie **dmoregister** beim Registrieren des DMO aufzurufen, müssen Sie [**dmounregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) bei der Registrierung des DMO bei der Aufhebung der Registrierung in derselben Kategorie durch dmounregistrieren.</span><span class="sxs-lookup"><span data-stu-id="76d2e-120">If you call **DMORegister** when you register the DMO, you must [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) with the same category when you unregister the DMO.</span></span>

<span data-ttu-id="76d2e-121">Im folgenden Beispiel werden die im vorherigen Beispiel erstellten Registrierungseinträge entfernt:</span><span class="sxs-lookup"><span data-stu-id="76d2e-121">The following example removes the registry entries created in the previous example:</span></span>


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



<span data-ttu-id="76d2e-122">**DirectShow-Verdienst Werte**</span><span class="sxs-lookup"><span data-stu-id="76d2e-122">**DirectShow Merit Values**</span></span>

<span data-ttu-id="76d2e-123">Zum Zweck der Erstellung von Filter Diagrammen weist DirectShow DMOS einen Standardwert für den Verdienst zu.</span><span class="sxs-lookup"><span data-stu-id="76d2e-123">For purposes of building filter graphs, DirectShow assigns a default merit value to DMOs.</span></span> <span data-ttu-id="76d2e-124">Sie können diesen Wert überschreiben, indem Sie einen Registrierungs Eintrag zum Registrierungsschlüssel von DMO in HKEY \_ Classes \_ root \\ CLSID hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="76d2e-124">You can override this value by adding a registry entry to the DMO's registry key in HKEY\_CLASSES\_ROOT\\CLSID.</span></span> <span data-ttu-id="76d2e-125">Fügen Sie einen **DWORD** -Wert mit dem Namen ein, `Merit` dessen Wert den Verdienst angibt.</span><span class="sxs-lookup"><span data-stu-id="76d2e-125">Include a **DWORD** value named `Merit` whose value specifies the merit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76d2e-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="76d2e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76d2e-127">Schreiben eines DMO</span><span class="sxs-lookup"><span data-stu-id="76d2e-127">Writing a DMO</span></span>](writing-a-dmo.md)
</dt> </dl>

 

 



