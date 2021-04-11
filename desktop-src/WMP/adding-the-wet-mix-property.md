---
title: Hinzufügen der Eigenschaft "nass Mischung"
description: Hinzufügen der Eigenschaft "nass Mischung"
ms.assetid: 4605d893-8ac0-42fd-a1ac-51430561f174
keywords:
- Windows Media Player-Plug-ins, Echo-Beispiel Eigenschaften
- Plug-ins, Echo-Beispiel Eigenschaften
- Plug-Ins für die digitale Signalverarbeitung, Echo-Beispiel Eigenschaften
- DSP-Plug-ins, Echo-Beispiel Eigenschaften
- Echo DSP-Plug-in-Beispiel, Eigenschaften
- Echo DSP-Plug-in-Beispiel, Eigenschaft "nass Mischung"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6af8e7b4857ccbf6b725044575d1b8524aaf50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310088"
---
# <a name="adding-the-wet-mix-property"></a><span data-ttu-id="772d8-109">Hinzufügen der Eigenschaft "nass Mischung"</span><span class="sxs-lookup"><span data-stu-id="772d8-109">Adding the Wet Mix Property</span></span>

<span data-ttu-id="772d8-110">Sie müssen den Code hinzufügen, um die zusätzliche Eigenschaft für die Wirkungs Ebene bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="772d8-110">You must add the code to provide the additional property for the effect level.</span></span>

<span data-ttu-id="772d8-111">Im Abschnitt [Hinzufügen von Eigenschaften zum Sample audiodsp-Plug-in](adding-properties-to-the-sample-audio-dsp-plug-in.md) finden Sie ausführliche Informationen zum Hinzufügen einer neuen Eigenschaft mit Visual C++.</span><span class="sxs-lookup"><span data-stu-id="772d8-111">The section [Adding Properties to the Sample Audio DSP Plug-in](adding-properties-to-the-sample-audio-dsp-plug-in.md) provides details about how to add a new property using Visual C++.</span></span> <span data-ttu-id="772d8-112">In diesem Abschnitt wird gezeigt, wie Sie den Code manuell hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="772d8-112">This section shows you how to add the code manually.</span></span> <span data-ttu-id="772d8-113">Dies umfasst das Hinzufügen von Code an denselben drei Stellen, an denen Sie den Code für die Eigenschaft Verzögerungszeit geändert haben.</span><span class="sxs-lookup"><span data-stu-id="772d8-113">This entails adding code in the same three places where you modified the code for the delay time property.</span></span>

<span data-ttu-id="772d8-114">Fügen Sie die Prototypen für die get \_ -Methode Get wetmix und Put \_ wetmix direkt nach den anderen Eigenschaften Methoden Prototypen in Echo. h ein.</span><span class="sxs-lookup"><span data-stu-id="772d8-114">Add the prototypes for the get\_wetmix and put\_wetmix methods immediately following the other property method prototypes in Echo.h.</span></span> <span data-ttu-id="772d8-115">Verwenden Sie die folgende Syntax:</span><span class="sxs-lookup"><span data-stu-id="772d8-115">Use the following syntax:</span></span>


```C++
STDMETHOD(get_wetmix)(double *pVal);
STDMETHOD(put_wetmix)(double newVal);

```



<span data-ttu-id="772d8-116">Fügen Sie jetzt die Implementierung für jede Methode direkt nach den anderen Eigenschafts Implementierungen in Echo. cpp hinzu.</span><span class="sxs-lookup"><span data-stu-id="772d8-116">Now, add the implementation for each method immediately following the other property implementations in Echo.cpp.</span></span> <span data-ttu-id="772d8-117">Das folgende Beispiel zeigt den Code für beide Methoden:</span><span class="sxs-lookup"><span data-stu-id="772d8-117">The following example shows the code for both methods:</span></span>


```C++
// Property get to retrieve the wet mix value by using the public interface.
STDMETHODIMP CEcho::get_wetmix(double *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_fWetMix;

    return S_OK;
}

// Property put to store the wet mix value by using the public interface.
STDMETHODIMP CEcho::put_wetmix(double newVal)
{
    m_fWetMix = newVal;

    // Calculate m_fDryMix
    m_fDryMix = 1.0 - m_fWetMix;
    
    return S_OK;
}

```



<span data-ttu-id="772d8-118">Beachten Sie, dass die Implementierung von put \_ wetmix den Code enthält, um den korrekten Wert für m \_ fdrymix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="772d8-118">Notice that the implementation of put\_wetmix includes the code to calculate the correct value for m\_fDryMix.</span></span> <span data-ttu-id="772d8-119">Jedes Mal, wenn ein neuer Wert für m-" \_ fiwetmix" angegeben wird, ist diese Berechnung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="772d8-119">Each time a new value is specified for m\_fWetMix, this calculation is required.</span></span>

<span data-ttu-id="772d8-120">Fügen Sie den folgenden Code in der Schnittstellen Definition direkt nach dem Code für die Delay-Methoden in Echo. idl hinzu:</span><span class="sxs-lookup"><span data-stu-id="772d8-120">Add the following code in the interface definition just after the code for the delay methods in Echo.idl:</span></span>


```C++
HRESULT get_wetmix([out] double *pVal);
HRESULT put_wetmix([in] double newVal);

```



## <a name="related-topics"></a><span data-ttu-id="772d8-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="772d8-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="772d8-122">**Echo-Beispiel Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="772d8-122">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




