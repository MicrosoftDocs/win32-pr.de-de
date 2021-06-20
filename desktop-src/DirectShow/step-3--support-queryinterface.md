---
description: Machen Sie die neuen Schnittstellen eines Filters für Clients verfügbar, wenn Sie eine Filtereigenschaftsseite für einen benutzerdefinierten DirectShow-Filter erstellen.
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: 'Schritt 3: Unterstützung von QueryInterface'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b62132a6f24c68453ad4e51f72cdd9a2a78c65
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410023"
---
# <a name="step-3-support-queryinterface"></a><span data-ttu-id="9c28a-104">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="9c28a-104">Step 3.</span></span> <span data-ttu-id="9c28a-105">Unterstützung von QueryInterface</span><span class="sxs-lookup"><span data-stu-id="9c28a-105">Support QueryInterface</span></span>

<span data-ttu-id="9c28a-106">Gehen Sie wie folgt vor, um die neuen Schnittstellen des Filters für Clients verfügbar zu machen:</span><span class="sxs-lookup"><span data-stu-id="9c28a-106">To expose the filter's new interfaces to clients, do the following:</span></span>

-   <span data-ttu-id="9c28a-107">Schließen Sie [**das DECLARE \_ IUNKNOWN-Makro**](declare-iunknown.md) in den öffentlichen Deklarationsabschnitt Ihres Filters ein:</span><span class="sxs-lookup"><span data-stu-id="9c28a-107">Include the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section of your filter:</span></span>
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   <span data-ttu-id="9c28a-108">Überschreiben [**Sie CUnknown::NonDelegatingQueryInterface,**](cunknown-nondelegatingqueryinterface.md) um nach den IIDs der beiden Schnittstellen zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="9c28a-108">Override [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IIDs of the two interfaces:</span></span>
    ```C++
    STDMETHODIMP CGrayFilter::NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if (riid == IID_ISpecifyPropertyPages)
        {
            return GetInterface(
               static_cast<ISpecifyPropertyPages*>(this),
               ppv);
        }
        else if (riid == IID_ISaturation)
        {
            return GetInterface(static_cast<ISaturation*>(this), ppv);
        }
        else
        {
            // Call the parent class.
            return CBaseFilter::NonDelegatingQueryInterface(riid, ppv);

            // NOTE: This example assumes that the filter inherits directly
            // from CBaseFilter. If your filter inherits from another class,
            // call the NonDelegatingQueryInterface method of that class.
        }
    }
    ```

    

<span data-ttu-id="9c28a-109">Weiter: [Schritt 4. Erstellen Sie die Eigenschaftenseite](step-4--create-the-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="9c28a-109">Next: [Step 4. Create the Property Page](step-4--create-the-property-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c28a-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c28a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c28a-111">Erstellen einer Filtereigenschaftsseite</span><span class="sxs-lookup"><span data-stu-id="9c28a-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> <dt>

[<span data-ttu-id="9c28a-112">Implementieren von IUnknown</span><span class="sxs-lookup"><span data-stu-id="9c28a-112">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 



