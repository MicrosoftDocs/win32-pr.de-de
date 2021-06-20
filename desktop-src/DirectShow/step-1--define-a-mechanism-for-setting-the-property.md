---
description: Definieren Sie einen Mechanismus zum Festlegen der Eigenschaft als Teil der Erstellung einer Filtereigenschaftsseite für einen benutzerdefinierten DirectShow-Filter.
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: 'Schritt 1: Definieren eines Mechanismus zum Festlegen der Eigenschaft'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 191014c35e27974c52961c2c6218e3a83effcc99
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410073"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a><span data-ttu-id="3a6a4-104">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="3a6a4-104">Step 1.</span></span> <span data-ttu-id="3a6a4-105">Definieren eines Mechanismus zum Festlegen der Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3a6a4-105">Define a Mechanism for Setting the Property</span></span>

<span data-ttu-id="3a6a4-106">Der Filter muss eine Möglichkeit unterstützen, damit die Eigenschaftenseite damit kommunizieren kann, damit die Eigenschaftenseite Eigenschaften für den Filter festlegen und abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="3a6a4-106">The filter must support a way for the property page to communicate with it, so that the property page can set and retrieve properties on the filter.</span></span> <span data-ttu-id="3a6a4-107">Folgende Mechanismen sind möglich:</span><span class="sxs-lookup"><span data-stu-id="3a6a4-107">Possible mechanisms include the following:</span></span>

-   <span data-ttu-id="3a6a4-108">Machen Sie eine benutzerdefinierte COM-Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3a6a4-108">Expose a custom COM interface.</span></span>
-   <span data-ttu-id="3a6a4-109">Automation-Eigenschaften werden über **IDispatch unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="3a6a4-109">Support Automation properties, through **IDispatch**.</span></span>
-   <span data-ttu-id="3a6a4-110">Machen Sie die **IPropertyBag-Schnittstelle** verfügbar, und definieren Sie einen Satz benannter Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3a6a4-110">Expose the **IPropertyBag** interface and define a set of named properties.</span></span>

<span data-ttu-id="3a6a4-111">In diesem Beispiel wird eine benutzerdefinierte COM-Schnittstelle namens ISaturation verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a6a4-111">This example uses a custom COM interface, named ISaturation.</span></span> <span data-ttu-id="3a6a4-112">Dies ist keine tatsächliche DirectShow-Schnittstelle. sie wird nur für dieses Beispiel definiert.</span><span class="sxs-lookup"><span data-stu-id="3a6a4-112">This is not an actual DirectShow interface; it is defined only for this example.</span></span> <span data-ttu-id="3a6a4-113">Deklarieren Sie zunächst die Schnittstelle in einer Headerdatei zusammen mit dem Schnittstellenbezeichner (IID):</span><span class="sxs-lookup"><span data-stu-id="3a6a4-113">Start by declaring the interface in a header file, along with the interface identifier (IID):</span></span>


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



<span data-ttu-id="3a6a4-114">Sie können die Schnittstelle auch mit IDL definieren und den MIDL-Compiler verwenden, um die Headerdatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3a6a4-114">You can also define the interface with IDL and use the MIDL compiler to create the header file.</span></span> <span data-ttu-id="3a6a4-115">Implementieren Sie als Nächstes die benutzerdefinierte Schnittstelle im Filter.</span><span class="sxs-lookup"><span data-stu-id="3a6a4-115">Next, implement the custom interface in the filter.</span></span> <span data-ttu-id="3a6a4-116">In diesem Beispiel werden die Methoden "Get" und "Set" für den Sättigungswert des Filters verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a6a4-116">This example uses "Get" and "Set" methods for the filter's saturation value.</span></span> <span data-ttu-id="3a6a4-117">Beachten Sie, dass beide Methoden den m \_ lSaturation-Member mit einem kritischen Abschnitt schützen.</span><span class="sxs-lookup"><span data-stu-id="3a6a4-117">Notice that both methods protect the m\_lSaturation member with a critical section.</span></span>


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



<span data-ttu-id="3a6a4-118">Natürlich unterscheiden sich die Details Ihrer eigenen Implementierung von dem hier gezeigten Beispiel.</span><span class="sxs-lookup"><span data-stu-id="3a6a4-118">Of course, the details of your own implementation will differ from the example shown here.</span></span>

<span data-ttu-id="3a6a4-119">Weiter: [Schritt 2. Implementieren Sie ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).</span><span class="sxs-lookup"><span data-stu-id="3a6a4-119">Next: [Step 2. Implement ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a6a4-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a6a4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a6a4-121">**CCritSec-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3a6a4-121">**CCritSec Class**</span></span>](ccritsec.md)
</dt> <dt>

[<span data-ttu-id="3a6a4-122">Erstellen einer Filtereigenschaftsseite</span><span class="sxs-lookup"><span data-stu-id="3a6a4-122">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



