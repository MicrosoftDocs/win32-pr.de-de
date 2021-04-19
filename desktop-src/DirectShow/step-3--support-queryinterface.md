---
description: 'Schritt 3:'
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: 'Schritt 3: QueryInterface-Unterstützung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e3d44b67971e165b8586aa3a02cc65ab3ab05f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356998"
---
# <a name="step-3-support-queryinterface"></a><span data-ttu-id="068a1-104">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="068a1-104">Step 3.</span></span> <span data-ttu-id="068a1-105">QueryInterface-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="068a1-105">Support QueryInterface</span></span>

<span data-ttu-id="068a1-106">Gehen Sie folgendermaßen vor, um die neuen Schnittstellen des Filters für Clients verfügbar zu machen:</span><span class="sxs-lookup"><span data-stu-id="068a1-106">To expose the filter's new interfaces to clients, do the following:</span></span>

-   <span data-ttu-id="068a1-107">Fügen Sie das Makro [**Declare \_ IUnknown**](declare-iunknown.md) in den Abschnitt Public Declaration Ihres Filters ein:</span><span class="sxs-lookup"><span data-stu-id="068a1-107">Include the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section of your filter:</span></span>
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   <span data-ttu-id="068a1-108">Überschreiben Sie [**cunknown:: nondelegatingqueryinterface**](cunknown-nondelegatingqueryinterface.md) , um die IIDs der beiden Schnittstellen zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="068a1-108">Override [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IIDs of the two interfaces:</span></span>
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

    

<span data-ttu-id="068a1-109">Weiter: [Schritt 4. Erstellen Sie die Eigenschaften Seite](step-4--create-the-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="068a1-109">Next: [Step 4. Create the Property Page](step-4--create-the-property-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="068a1-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="068a1-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="068a1-111">Erstellen einer Filter Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="068a1-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> <dt>

[<span data-ttu-id="068a1-112">Implementieren von IUnknown</span><span class="sxs-lookup"><span data-stu-id="068a1-112">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 



