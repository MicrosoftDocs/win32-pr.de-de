---
description: Factory-Vorlagen Array
ms.assetid: 310afccd-42a6-426e-b455-7bf98062bf36
title: Factory-Vorlagen Array
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645f2c8d05f37ab64142747755d6a0e7727f4b11
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125599"
---
# <a name="factory-template-array"></a><span data-ttu-id="991ef-103">Factory-Vorlagen Array</span><span class="sxs-lookup"><span data-stu-id="991ef-103">Factory Template Array</span></span>

<span data-ttu-id="991ef-104">Die Factory-Vorlage enthält die folgenden öffentlichen Member-Variablen:</span><span class="sxs-lookup"><span data-stu-id="991ef-104">The factory template contains the following public member variables:</span></span>

``` syntax
const WCHAR *              m_Name;                // Name
const CLSID *              m_ClsID;               // CLSID
LPFNNewCOMObject           m_lpfnNew;             // Function to create an instance
                                                  //   of the component
LPFNInitRoutine            m_lpfnInit;            // Initialization function (optional)
const AMOVIESETUP_FILTER * m_pAMovieSetup_Filter; // Set-up information (for filters)
```

<span data-ttu-id="991ef-105">Die zwei Funktionszeiger " [**m \_ lpfnnew**](cfactorytemplate-m-lpfnnew.md) " und " [**m \_ lpfninit**](cfactorytemplate-m-lpfninit.md)" verwenden die folgenden Typdefinitionen:</span><span class="sxs-lookup"><span data-stu-id="991ef-105">The two function pointers, [**m\_lpfnNew**](cfactorytemplate-m-lpfnnew.md) and [**m\_lpfnInit**](cfactorytemplate-m-lpfninit.md), use the following type definitions:</span></span>

``` syntax
typedef CUnknown *(CALLBACK *LPFNNewCOMObject)(LPUNKNOWN pUnkOuter, HRESULT *phr);
typedef void (CALLBACK *LPFNInitRoutine)(BOOL bLoading, const CLSID *rclsid);
```

<span data-ttu-id="991ef-106">Der erste ist die Instanziierung-Funktion für die Komponente.</span><span class="sxs-lookup"><span data-stu-id="991ef-106">The first is the instantiation function for the component.</span></span> <span data-ttu-id="991ef-107">Die zweite ist eine optionale Initialisierungsfunktion.</span><span class="sxs-lookup"><span data-stu-id="991ef-107">The second is an optional initialization function.</span></span> <span data-ttu-id="991ef-108">Wenn Sie eine Initialisierungsfunktion bereitstellen, wird diese innerhalb der DLL-Einstiegspunkt Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="991ef-108">If you provide an initialization function, it is called from inside the DLL entry-point function.</span></span> <span data-ttu-id="991ef-109">(Die DLL-Einstiegspunkt Funktion wird weiter unten in diesem Artikel erläutert.)</span><span class="sxs-lookup"><span data-stu-id="991ef-109">(The DLL entry-point function is discussed later in this article.)</span></span>

<span data-ttu-id="991ef-110">Angenommen, Sie erstellen eine DLL, die eine Komponente mit dem Namen cmycomponent enthält, die von [**cunknown**](cunknown.md)erbt.</span><span class="sxs-lookup"><span data-stu-id="991ef-110">Suppose you are creating a DLL that contains a component named CMyComponent, which inherits from [**CUnknown**](cunknown.md).</span></span> <span data-ttu-id="991ef-111">Sie müssen die folgenden Elemente in der DLL angeben:</span><span class="sxs-lookup"><span data-stu-id="991ef-111">You must provide the following items in your DLL:</span></span>

-   <span data-ttu-id="991ef-112">Die Initialisierungsfunktion, eine öffentliche Methode, die eine neue Instanz von cmycomponent zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="991ef-112">The initialization function, a public method that returns a new instance of CMyComponent.</span></span>
-   <span data-ttu-id="991ef-113">Ein globales Array von Factory-Vorlagen mit dem Namen *g- \_ Vorlagen.*</span><span class="sxs-lookup"><span data-stu-id="991ef-113">A global array of factory templates, named *g\_Templates.*</span></span> <span data-ttu-id="991ef-114">Dieses Array enthält die Factory-Vorlage für cmycomponent.</span><span class="sxs-lookup"><span data-stu-id="991ef-114">This array contains the factory template for CMyComponent.</span></span>
-   <span data-ttu-id="991ef-115">Eine globale Variable mit dem Namen " *g \_ ctemplates* ", die die Größe des Arrays angibt.</span><span class="sxs-lookup"><span data-stu-id="991ef-115">A global variable named *g\_cTemplates* that specifies the size of the array.</span></span>

<span data-ttu-id="991ef-116">Im folgenden Beispiel wird gezeigt, wie Sie diese Elemente deklarieren:</span><span class="sxs-lookup"><span data-stu-id="991ef-116">The following example shows how to declare these items:</span></span>


```C++
// Public method that returns a new instance. 
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = new CMyComponent(NAME("My Component"), pUnk, pHr );
    if (pNewObject == NULL) {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 

CFactoryTemplate g_Templates[1] = 
{
    { 
      L"My Component",                // Name
      &CLSID_MyComponent,             // CLSID
      CMyComponent::CreateInstance,   // Method to create an instance of MyComponent
      NULL,                           // Initialization function
      NULL                            // Set-up information (for filters)
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);    
```



<span data-ttu-id="991ef-117">Die `CreateInstance` -Methode ruft den-Klassenkonstruktor auf und gibt einen Zeiger auf die neue Klasseninstanz zurück.</span><span class="sxs-lookup"><span data-stu-id="991ef-117">The `CreateInstance` method calls the class constructor and returns a pointer to the new class instance.</span></span> <span data-ttu-id="991ef-118">Der Parameter- *Punk* ist ein Zeiger auf die aggregierte [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="991ef-118">The parameter *pUnk* is a pointer to the aggregating [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="991ef-119">Sie können diesen Parameter einfach an den-Klassenkonstruktor übergeben.</span><span class="sxs-lookup"><span data-stu-id="991ef-119">You can simply pass this parameter to the class constructor.</span></span> <span data-ttu-id="991ef-120">Der *PHR* -Parameter ist ein Zeiger auf einen HRESULT-Wert.</span><span class="sxs-lookup"><span data-stu-id="991ef-120">The parameter *pHr* is a pointer to an HRESULT value.</span></span> <span data-ttu-id="991ef-121">Der Klassenkonstruktor legt diesen auf einen geeigneten Wert fest. wenn der Konstruktor jedoch fehlschlägt, legen Sie den Wert auf "E \_ outo fmemory" fest.</span><span class="sxs-lookup"><span data-stu-id="991ef-121">The class constructor sets this to an appropriate value, but if the constructor fails, set the value to E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="991ef-122">Das [**Name**](name.md) -Makro generiert eine Zeichenfolge in Debugbuilds, wird jedoch in Einzelhandels Builds in **null** aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="991ef-122">The [**NAME**](name.md) macro generates a string in debug builds but resolves to **NULL** in retail builds.</span></span> <span data-ttu-id="991ef-123">Sie wird in diesem Beispiel verwendet, um der Komponente einen Namen zu geben, der in Debugprotokollen enthalten ist, aber keinen Arbeitsspeicher in der endgültigen Version einnimmt.</span><span class="sxs-lookup"><span data-stu-id="991ef-123">It is used in this example to give the component a name that appears in debug logs but does not occupy memory in the final version.</span></span>

<span data-ttu-id="991ef-124">Die- `CreateInstance` Methode kann einen beliebigen Namen haben, da die Klassenfactory auf den Funktionszeiger in der Factoryvorlage verweist.</span><span class="sxs-lookup"><span data-stu-id="991ef-124">The `CreateInstance` method can have any name, because the class factory refers to the function pointer in the factory template.</span></span> <span data-ttu-id="991ef-125">Allerdings sind *g- \_ Vorlagen* und *g \_ ctemplates* globale Variablen, die von der Klassenfactory erwartet werden, sodass Sie genau diese Namen aufweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="991ef-125">However, *g\_Templates* and *g\_cTemplates* are global variables that the class factory expects to find, so they must have exactly those names.</span></span>

## <a name="related-topics"></a><span data-ttu-id="991ef-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="991ef-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="991ef-127">Erstellen einer DirectShow-Filter-dll</span><span class="sxs-lookup"><span data-stu-id="991ef-127">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 
