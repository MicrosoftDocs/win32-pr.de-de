---
description: Deklarieren der Factory-Vorlage
ms.assetid: 3060c167-ea23-4061-b32a-16e750f55e6f
title: Deklarieren der Factory-Vorlage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3168f16b6281417846f13b7a17141282053c4705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123692"
---
# <a name="declaring-the-factory-template"></a><span data-ttu-id="b82bd-103">Deklarieren der Factory-Vorlage</span><span class="sxs-lookup"><span data-stu-id="b82bd-103">Declaring the Factory Template</span></span>

<span data-ttu-id="b82bd-104">Der nächste Schritt besteht darin, die Factory-Vorlage für den Filter zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="b82bd-104">The next step is to declare the factory template for your filter.</span></span> <span data-ttu-id="b82bd-105">Eine Factoryvorlage ist eine C++-Klasse, die Informationen für die Klassenfactory enthält.</span><span class="sxs-lookup"><span data-stu-id="b82bd-105">A factory template is a C++ class that contains information for the class factory.</span></span> <span data-ttu-id="b82bd-106">Deklarieren Sie in der dll ein globales Array von [**cfactoriytemplate**](cfactorytemplate.md) -Objekten, eines für jeden Filter oder jede COM-Komponente in der dll.</span><span class="sxs-lookup"><span data-stu-id="b82bd-106">In your DLL, declare a global array of [**CFactoryTemplate**](cfactorytemplate.md) objects, one for each filter or COM component in your DLL.</span></span> <span data-ttu-id="b82bd-107">Das Array muss als *g- \_ Vorlagen* benannt werden.</span><span class="sxs-lookup"><span data-stu-id="b82bd-107">The array must be named *g\_Templates*.</span></span> <span data-ttu-id="b82bd-108">Weitere Informationen zu Factory-Vorlagen finden [Sie unter Erstellen einer DirectShow-Filter-DLL](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="b82bd-108">For more information about factory templates, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

<span data-ttu-id="b82bd-109">Der **m \_ pamoviesetup- \_ Filter** Member der Factory-Vorlage ist ein Zeiger auf die zuvor beschriebene [**amoviesetup- \_ Filter**](amoviesetup-filter.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="b82bd-109">The **m\_pAMovieSetup\_Filter** member of the factory template is a pointer to the [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure described previously.</span></span> <span data-ttu-id="b82bd-110">Das folgende Beispiel zeigt eine Factory-Vorlage unter Verwendung der im vorherigen Beispiel angegebenen Struktur:</span><span class="sxs-lookup"><span data-stu-id="b82bd-110">The following example shows a factory template, using the structure given in the previous example:</span></span>


```C++
CFactoryTemplate g_Templates[] = {
    {
        g_wszName,                      // Name.
        &CLSID_SomeFilter,              // CLSID.
        CSomeFilter::CreateInstance,    // Creation function.
        NULL,
        &sudFilterReg                   // Pointer to filter information.
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);
```



<span data-ttu-id="b82bd-111">Wenn Sie keine Filter Informationen deklariert haben, kann der " **m \_ pamovesetup \_** "-Filter **null** sein.</span><span class="sxs-lookup"><span data-stu-id="b82bd-111">If you did not declare any filter information, **m\_pAMoveSetup\_Filter** can be **NULL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b82bd-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b82bd-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b82bd-113">Registrieren von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="b82bd-113">How to Register DirectShow Filters</span></span>](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



