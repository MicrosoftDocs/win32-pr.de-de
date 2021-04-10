---
description: Implementieren von DllRegisterServer
ms.assetid: aaa4069e-0b6a-4a76-b950-1a85a9ed969d
title: Implementieren von DllRegisterServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b994e80a181b69efffbe6123382957e7a38f8278
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125036"
---
# <a name="implementing-dllregisterserver"></a><span data-ttu-id="513be-103">Implementieren von DllRegisterServer</span><span class="sxs-lookup"><span data-stu-id="513be-103">Implementing DllRegisterServer</span></span>

<span data-ttu-id="513be-104">Der letzte Schritt besteht darin, die **DllRegisterServer** -Funktion zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="513be-104">The final step is to implement the **DllRegisterServer** function.</span></span> <span data-ttu-id="513be-105">Die dll, die die Komponente enthält, muss diese Funktion exportieren.</span><span class="sxs-lookup"><span data-stu-id="513be-105">The DLL that contains the component must export this function.</span></span> <span data-ttu-id="513be-106">Die Funktion wird von einer Setup Anwendung aufgerufen, oder wenn der Benutzer das Regsvr32.exe Tool ausführt.</span><span class="sxs-lookup"><span data-stu-id="513be-106">The function will be called by a set-up application, or when the user runs the Regsvr32.exe tool.</span></span>

<span data-ttu-id="513be-107">Das folgende Beispiel zeigt eine minimale Implementierung von **DllRegisterServer**:</span><span class="sxs-lookup"><span data-stu-id="513be-107">The following example shows a minimal implementation of **DlLRegisterServer**:</span></span>


```C++
STDAPI DllRegisterServer(void)
{
    return AMovieDllRegisterServer2(TRUE);
}
```



<span data-ttu-id="513be-108">Die [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) -Funktion erstellt Registrierungseinträge für jede Komponente im</span><span class="sxs-lookup"><span data-stu-id="513be-108">The [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function creates registry entries for every component in the</span></span>


```
g_Templates
```



<span data-ttu-id="513be-109">Array.</span><span class="sxs-lookup"><span data-stu-id="513be-109">array.</span></span> <span data-ttu-id="513be-110">Diese Funktion weist jedoch einige Einschränkungen auf.</span><span class="sxs-lookup"><span data-stu-id="513be-110">However, this function has some limitations.</span></span> <span data-ttu-id="513be-111">Zuerst wird jeder Filter der Kategorie "DirectShow Filters" (CLSID \_ legacyamfiltercategory) zugewiesen, aber nicht jeder Filter gehört zu dieser Kategorie.</span><span class="sxs-lookup"><span data-stu-id="513be-111">First, it assigns every filter to the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory), but not every filter belongs in this category.</span></span> <span data-ttu-id="513be-112">Erfassungs Filter und Komprimierungs Filter verfügen z. b. über eigene Kategorien.</span><span class="sxs-lookup"><span data-stu-id="513be-112">Capture filters and compression filters, for example, have their own categories.</span></span> <span data-ttu-id="513be-113">Zweitens: Wenn Ihr Filter ein Hardware Gerät unterstützt, müssen Sie möglicherweise zwei weitere Informationen registrieren, die **AMovieDLLRegisterServer2** nicht behandelt: die Kategorie *Mittel* und *Pin*.</span><span class="sxs-lookup"><span data-stu-id="513be-113">Second, if your filter supports a hardware device, you might need to register two additional pieces of information that **AMovieDLLRegisterServer2** does not handle: the *medium* and the *pin category*.</span></span> <span data-ttu-id="513be-114">Ein Medium definiert eine Kommunikationsmethode in einem Hardware Gerät, z. b. einem Bus.</span><span class="sxs-lookup"><span data-stu-id="513be-114">A medium defines a method of communication in a hardware device, such as a bus.</span></span> <span data-ttu-id="513be-115">Die PIN-Kategorie definiert die Funktion einer PIN.</span><span class="sxs-lookup"><span data-stu-id="513be-115">The pin category defines the function of a pin.</span></span> <span data-ttu-id="513be-116">Informationen zu Medien finden Sie unter "kspin- \_ Medium" im Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="513be-116">For information on mediums, see "KSPIN\_MEDIUM" in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="513be-117">Eine Liste der PIN-Kategorien finden Sie unter [PIN-Eigenschaften Satz](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="513be-117">For a list of pin categories, see [Pin Property Set](pin-property-set.md).</span></span>

<span data-ttu-id="513be-118">Wenn Sie eine Filterkategorie, eine mittlere oder eine PIN-Kategorie angeben möchten, müssen Sie die [**IFilterMapper2:: registerfilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) -Methode innerhalb von **DllRegisterServer** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="513be-118">If you want to specify a filter category, a medium, or a pin category, call the [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method from within **DllRegisterServer**.</span></span> <span data-ttu-id="513be-119">Diese Methode nimmt einen Zeiger auf eine [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) -Struktur, die Informationen über den Filter angibt.</span><span class="sxs-lookup"><span data-stu-id="513be-119">This method takes a pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure, which specifies information about the filter.</span></span>

<span data-ttu-id="513be-120">Um die Dinge etwas komplizierter zu machen, unterstützt die **REGFILTER2** -Struktur zwei verschiedene Formate zum Registrieren von Pins.</span><span class="sxs-lookup"><span data-stu-id="513be-120">To complicate matters somewhat, the **REGFILTER2** structure supports two different formats for registering pins.</span></span> <span data-ttu-id="513be-121">Der **dwVersion** -Member gibt das Format an:</span><span class="sxs-lookup"><span data-stu-id="513be-121">The **dwVersion** member specifies the format:</span></span>

-   <span data-ttu-id="513be-122">Wenn **dwVersion** den Wert 1 hat, ist das PIN-Format die **amoviesetup- \_ Pin** (zuvor beschrieben).</span><span class="sxs-lookup"><span data-stu-id="513be-122">If **dwVersion** is 1, the pin format is **AMOVIESETUP\_PIN** (described previously).</span></span>
-   <span data-ttu-id="513be-123">Wenn **dwVersion** 2 ist, ist das PIN-Format [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).</span><span class="sxs-lookup"><span data-stu-id="513be-123">If **dwVersion** is 2, the pin format is [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).</span></span>

<span data-ttu-id="513be-124">Die **REGFILTERPINS2** -Struktur enthält Einträge für PIN-Medien und PIN-Kategorien.</span><span class="sxs-lookup"><span data-stu-id="513be-124">The **REGFILTERPINS2** structure includes entries for pin mediums and pin categories.</span></span> <span data-ttu-id="513be-125">Außerdem werden Bitflags für einige Elemente verwendet, die von der **amoviesetup- \_ Pin** als boolesche Werte deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="513be-125">Also, it uses bit flags for some items that **AMOVIESETUP\_PIN** declares as Boolean values.</span></span>

<span data-ttu-id="513be-126">Im folgenden Beispiel wird gezeigt, wie **IFilterMapper2:: registerfilter** von innerhalb von **DllRegisterServer** aufgerufen wird:</span><span class="sxs-lookup"><span data-stu-id="513be-126">The following example shows how to call **IFilterMapper2::RegisterFilter** from inside **DllRegisterServer**:</span></span>


```C++
REGFILTER2 rf2FilterReg = {
    1,              // Version 1 (no pin mediums or pin category).
    MERIT_NORMAL,   // Merit.
    1,              // Number of pins.
    &sudPins        // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
        return hr;

    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->RegisterFilter(
        CLSID_SomeFilter,                // Filter CLSID. 
        g_wszName,                       // Filter name.
        NULL,                            // Device moniker. 
        &CLSID_VideoCompressorCategory,  // Video compressor category.
        g_wszName,                       // Instance data.
        &rf2FilterReg                    // Pointer to filter information.
    );
    pFM2->Release();
    return hr;
}
```



 

 



