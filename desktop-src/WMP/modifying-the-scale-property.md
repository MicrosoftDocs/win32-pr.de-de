---
title: Ändern der Scale-Eigenschaft
description: Ändern der Scale-Eigenschaft
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- Windows Media Player-Plug-ins, Echo-Beispiel Eigenschaften
- Plug-ins, Echo-Beispiel Eigenschaften
- Plug-Ins für die digitale Signalverarbeitung, Echo-Beispiel Eigenschaften
- DSP-Plug-ins, Echo-Beispiel Eigenschaften
- Echo DSP-Plug-in-Beispiel, Scale-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd91e2315db9d0d1e14d2aec55f79a8b05c442ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338580"
---
# <a name="modifying-the-scale-property"></a><span data-ttu-id="af17a-108">Ändern der Scale-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af17a-108">Modifying the Scale Property</span></span>

<span data-ttu-id="af17a-109">Die Standard Implementierung des Assistenten macht die Scale-Eigenschaft verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af17a-109">The default wizard implementation exposes the scale property.</span></span> <span data-ttu-id="af17a-110">Sie können die vorhandene Implementierung ändern, um stattdessen die Eigenschaft Verzögerungszeit verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="af17a-110">You can change the existing implementation to expose the delay time property instead.</span></span>

<span data-ttu-id="af17a-111">Verwenden Sie zunächst das folgende Beispiel, um die Funktionsprototypen für get \_ Scale und Put \_ Scale in Echo. h zu ändern.</span><span class="sxs-lookup"><span data-stu-id="af17a-111">First, use the following example to change the function prototypes for get\_scale and put\_scale in Echo.h.</span></span> <span data-ttu-id="af17a-112">Ändern Sie den Namen der Methoden und Datentypen für die Parameter:</span><span class="sxs-lookup"><span data-stu-id="af17a-112">Change the name of the methods and the data types for the parameters:</span></span>


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



<span data-ttu-id="af17a-113">Ändern Sie als nächstes die Implementierungen der \_ Methoden get Scale und Put \_ Scale in Echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="af17a-113">Next, change the implementations of the get\_scale and put\_scale methods in Echo.cpp.</span></span> <span data-ttu-id="af17a-114">Stellen Sie den Code den folgenden Beispielen entsprechend dar:</span><span class="sxs-lookup"><span data-stu-id="af17a-114">Make the code match the following examples:</span></span>


```C++
// Formerly get_scale
STDMETHODIMP CEcho::get_delay(DWORD *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_dwDelayTime;

    return S_OK;
}

// Formerly put_scale
STDMETHODIMP CEcho::put_delay(DWORD newVal)
{
    m_dwDelayTime = newVal;

    return S_OK;
}

```



<span data-ttu-id="af17a-115">Im vorherigen Beispielcode werden die Methodennamen und die Parameter Datentypen geändert.</span><span class="sxs-lookup"><span data-stu-id="af17a-115">The preceding example code changes the method names and the parameter data types.</span></span> <span data-ttu-id="af17a-116">Der Name der Element Variablen sollte zuvor geändert worden sein.</span><span class="sxs-lookup"><span data-stu-id="af17a-116">The member variable name should have been changed previously.</span></span> <span data-ttu-id="af17a-117">Denken Sie daran, die Kommentare zu ändern, in denen auch die einzelnen Methoden eingeführt werden.</span><span class="sxs-lookup"><span data-stu-id="af17a-117">Remember to change the comments that introduce each method as well.</span></span>

<span data-ttu-id="af17a-118">Ändern Sie nun die Schnittstellen Definition.</span><span class="sxs-lookup"><span data-stu-id="af17a-118">Now, change the interface definition.</span></span> <span data-ttu-id="af17a-119">Der folgende Code ersetzt den Code in der IEcho-Schnittstellen Deklaration in Echo. idl:</span><span class="sxs-lookup"><span data-stu-id="af17a-119">The following code replaces the code in the IEcho interface declaration in Echo.idl:</span></span>


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a><span data-ttu-id="af17a-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af17a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af17a-121">**Echo-Beispiel Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="af17a-121">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




