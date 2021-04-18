---
description: 'Schritt 1:'
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: 'Schritt 1: Definieren eines Mechanismus zum Festlegen der Eigenschaft'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a1845cfb3cdf5642378a2321e827e52720a83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368034"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a><span data-ttu-id="e7e85-104">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="e7e85-104">Step 1.</span></span> <span data-ttu-id="e7e85-105">Definieren eines Mechanismus zum Festlegen der Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e7e85-105">Define a Mechanism for Setting the Property</span></span>

<span data-ttu-id="e7e85-106">Der Filter muss eine Methode unterstützen, mit der die Eigenschaften Seite damit kommunizieren kann, damit die Eigenschaften Seite Eigenschaften des Filters festlegen und abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="e7e85-106">The filter must support a way for the property page to communicate with it, so that the property page can set and retrieve properties on the filter.</span></span> <span data-ttu-id="e7e85-107">Folgende Mechanismen sind möglich:</span><span class="sxs-lookup"><span data-stu-id="e7e85-107">Possible mechanisms include the following:</span></span>

-   <span data-ttu-id="e7e85-108">Macht eine benutzerdefinierte COM-Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e7e85-108">Expose a custom COM interface.</span></span>
-   <span data-ttu-id="e7e85-109">Unterstützung von Automatisierungs Eigenschaften über **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="e7e85-109">Support Automation properties, through **IDispatch**.</span></span>
-   <span data-ttu-id="e7e85-110">Macht die **IPropertyBag** -Schnittstelle verfügbar und definiert einen Satz benannter Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e7e85-110">Expose the **IPropertyBag** interface and define a set of named properties.</span></span>

<span data-ttu-id="e7e85-111">In diesem Beispiel wird eine benutzerdefinierte COM-Schnittstelle mit dem Namen isaturierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7e85-111">This example uses a custom COM interface, named ISaturation.</span></span> <span data-ttu-id="e7e85-112">Dabei handelt es sich nicht um eine tatsächliche DirectShow-Schnittstelle. Er ist nur für dieses Beispiel definiert.</span><span class="sxs-lookup"><span data-stu-id="e7e85-112">This is not an actual DirectShow interface; it is defined only for this example.</span></span> <span data-ttu-id="e7e85-113">Beginnen Sie, indem Sie die-Schnittstelle in einer Header Datei zusammen mit dem Schnittstellen Bezeichner (IID) deklarieren:</span><span class="sxs-lookup"><span data-stu-id="e7e85-113">Start by declaring the interface in a header file, along with the interface identifier (IID):</span></span>


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(IID_ISaturation, 0x19412d6e, 0x6401, 
0x475c, 0xb0, 0x48, 0x7a, 0xd2, 0x96, 0xe1, 0x6a, 0x19);

interface ISaturation : public IUnknown
{
    STDMETHOD(GetSaturation)(long *plSat) = 0;
    STDMETHOD(SetSaturation)(long lSat) = 0;
};
```



<span data-ttu-id="e7e85-114">Sie können auch die Schnittstelle mit IDL definieren und den Mittelpunkt Compiler zum Erstellen der Header Datei verwenden.</span><span class="sxs-lookup"><span data-stu-id="e7e85-114">You can also define the interface with IDL and use the MIDL compiler to create the header file.</span></span> <span data-ttu-id="e7e85-115">Implementieren Sie anschließend die benutzerdefinierte Schnittstelle im Filter.</span><span class="sxs-lookup"><span data-stu-id="e7e85-115">Next, implement the custom interface in the filter.</span></span> <span data-ttu-id="e7e85-116">In diesem Beispiel werden die Methoden "Get" und "Set" für den Sättigungswert des Filters verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7e85-116">This example uses "Get" and "Set" methods for the filter's saturation value.</span></span> <span data-ttu-id="e7e85-117">Beachten Sie, dass beide Methoden den m \_ lsättigung-Member mit einem kritischen Abschnitt schützen.</span><span class="sxs-lookup"><span data-stu-id="e7e85-117">Notice that both methods protect the m\_lSaturation member with a critical section.</span></span>


```C++
class CGrayFilter : public ISaturation, /* Other inherited classes. */
{
private:
    CCritSec  m_csShared;    // Protects shared data.
    long      m_lSaturation; // Saturation level.
public:
    STDMETHODIMP GetSaturation(long *plSat)
    {
        if (!plSat) return E_POINTER;
        CAutoLock lock(&m_csShared);
        *plSat = m_lSaturation;
        return S_OK;
    }
    STDMETHODIMP SetSaturation(long lSat)
    {
        CAutoLock lock(&m_csShared);
        if (lSat < SATURATION_MIN || lSat > SATURATION_MAX)
        {
            return E_INVALIDARG;
        }
        m_lSaturation = lSat;
        return S_OK;
    }
};
```



<span data-ttu-id="e7e85-118">Die Details Ihrer eigenen Implementierung unterscheiden sich natürlich von dem hier gezeigten Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e7e85-118">Of course, the details of your own implementation will differ from the example shown here.</span></span>

<span data-ttu-id="e7e85-119">Weiter: [Schritt 2. Implementieren Sie ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).</span><span class="sxs-lookup"><span data-stu-id="e7e85-119">Next: [Step 2. Implement ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7e85-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e7e85-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7e85-121">**Ccritsec-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e7e85-121">**CCritSec Class**</span></span>](ccritsec.md)
</dt> <dt>

[<span data-ttu-id="e7e85-122">Erstellen einer Filter Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="e7e85-122">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



