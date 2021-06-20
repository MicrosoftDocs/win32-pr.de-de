---
description: Implementieren Sie die ISpecifyPropertyPages-Schnittstelle im Filter als Teil der Erstellung einer Filtereigenschaftenseite für einen benutzerdefinierten DirectShow-Filter.
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: 'Schritt 2: Implementieren von ISpecifyPropertyPages'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe37a22c6ba9c14f8656ac41294360569316be1a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410053"
---
# <a name="step-2-implement-ispecifypropertypages"></a><span data-ttu-id="aaf20-104">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="aaf20-104">Step 2.</span></span> <span data-ttu-id="aaf20-105">Implementieren von ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="aaf20-105">Implement ISpecifyPropertyPages</span></span>

<span data-ttu-id="aaf20-106">Implementieren Sie als Nächstes die **ISpecifyPropertyPages-Schnittstelle** in Ihrem Filter.</span><span class="sxs-lookup"><span data-stu-id="aaf20-106">Next, implement the **ISpecifyPropertyPages** interface in your filter.</span></span> <span data-ttu-id="aaf20-107">Diese Schnittstelle verfügt über eine einzelne **Methode, GetPages,** die ein Array von CLSIDs für die Eigenschaftenseiten zurückgibt, die der Filter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aaf20-107">This interface has a single method, **GetPages**, which returns an array of CLSIDs for the property pages that the filter supports.</span></span> <span data-ttu-id="aaf20-108">In diesem Beispiel verfügt der Filter über eine einzelne Eigenschaftenseite.</span><span class="sxs-lookup"><span data-stu-id="aaf20-108">In this example, the filter has a single property page.</span></span> <span data-ttu-id="aaf20-109">Generieren Sie zunächst die CLSID, und deklarieren Sie sie in Ihrer Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="aaf20-109">Start by generating the CLSID and declaring it in your header file:</span></span>


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



<span data-ttu-id="aaf20-110">Implementieren Sie nun die **GetPages-Methode:**</span><span class="sxs-lookup"><span data-stu-id="aaf20-110">Now implement the **GetPages** method:</span></span>


```C++
class CGrayFilter : public ISaturation,
                    public ISpecifyPropertyPages, 
                    /* Other inherited classes. */
{
public:
    STDMETHODIMP GetPages(CAUUID *pPages)
    {
        if (pPages == NULL) return E_POINTER;
        pPages->cElems = 1;
        pPages->pElems = (GUID*)CoTaskMemAlloc(sizeof(GUID));
        if (pPages->pElems == NULL) 
        {
            return E_OUTOFMEMORY;
        }
        pPages->pElems[0] = CLSID_SaturationProp;
        return S_OK;
    }
};

/* ... */

}
```



<span data-ttu-id="aaf20-111">Ordnen Sie Arbeitsspeicher für das Array **mithilfe von CoTaskMemAlloc zu.**</span><span class="sxs-lookup"><span data-stu-id="aaf20-111">Allocate memory for the array using **CoTaskMemAlloc**.</span></span> <span data-ttu-id="aaf20-112">Der Aufrufer gibt den Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="aaf20-112">The caller will release the memory.</span></span>

<span data-ttu-id="aaf20-113">Weiter: [Schritt 3. Unterstützung von QueryInterface.](step-3--support-queryinterface.md)</span><span class="sxs-lookup"><span data-stu-id="aaf20-113">Next: [Step 3. Support QueryInterface](step-3--support-queryinterface.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aaf20-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aaf20-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaf20-115">Erstellen einer Filtereigenschaftsseite</span><span class="sxs-lookup"><span data-stu-id="aaf20-115">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



