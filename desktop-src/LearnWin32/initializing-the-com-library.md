---
title: Initialisieren der com-Bibliothek
description: Initialisieren der com-Bibliothek
ms.assetid: b044e146-8409-4f8d-87d3-52f21ebc2255
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663cfb73455e118579f45710788ab72385ada335
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340267"
---
# <a name="initializing-the-com-library"></a><span data-ttu-id="64ba9-103">Initialisieren der com-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="64ba9-103">Initializing the COM Library</span></span>

<span data-ttu-id="64ba9-104">Jedes Windows-Programm, das com verwendet, muss die com-Bibliothek initialisieren, indem die [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="64ba9-104">Any Windows program that uses COM must initialize the COM library by calling the [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function.</span></span> <span data-ttu-id="64ba9-105">Jeder Thread, der eine COM-Schnittstelle verwendet, muss einen separaten Rückruf für diese Funktion durchführen.</span><span class="sxs-lookup"><span data-stu-id="64ba9-105">Each thread that uses a COM interface must make a separate call to this function.</span></span> <span data-ttu-id="64ba9-106">**CoInitializeEx** hat die folgende Signatur:</span><span class="sxs-lookup"><span data-stu-id="64ba9-106">**CoInitializeEx** has the following signature:</span></span>


```C++
HRESULT CoInitializeEx(LPVOID pvReserved, DWORD dwCoInit);
```



<span data-ttu-id="64ba9-107">Der erste Parameter ist reserviert und muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="64ba9-107">The first parameter is reserved and must be **NULL**.</span></span> <span data-ttu-id="64ba9-108">Der zweite Parameter gibt das Threading Modell an, das von Ihrem Programm verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="64ba9-108">The second parameter specifies the threading model that your program will use.</span></span> <span data-ttu-id="64ba9-109">COM unterstützt zwei verschiedene Threading Modelle, *Apartment Thread* und *Multithread*.</span><span class="sxs-lookup"><span data-stu-id="64ba9-109">COM supports two different threading models, *apartment threaded* and *multithreaded*.</span></span> <span data-ttu-id="64ba9-110">Wenn Sie Apartment Threading angeben, haben Sie folgende Garantien:</span><span class="sxs-lookup"><span data-stu-id="64ba9-110">If you specify apartment threading, you are making the following guarantees:</span></span>

-   <span data-ttu-id="64ba9-111">Sie greifen auf jedes COM-Objekt von einem einzelnen Thread aus zu. COM-Schnittstellen Zeiger werden nicht zwischen mehreren Threads gemeinsam verwendet.</span><span class="sxs-lookup"><span data-stu-id="64ba9-111">You will access each COM object from a single thread; you will not share COM interface pointers between multiple threads.</span></span>
-   <span data-ttu-id="64ba9-112">Der Thread verfügt über eine Nachrichten Schleife.</span><span class="sxs-lookup"><span data-stu-id="64ba9-112">The thread will have a message loop.</span></span> <span data-ttu-id="64ba9-113">(Siehe [Fenster Meldungen](window-messages.md) in Modul 1.)</span><span class="sxs-lookup"><span data-stu-id="64ba9-113">(See [Window Messages](window-messages.md) in Module 1.)</span></span>

<span data-ttu-id="64ba9-114">Wenn eine dieser Einschränkungen nicht zutrifft, verwenden Sie das Multithread-Modell.</span><span class="sxs-lookup"><span data-stu-id="64ba9-114">If either of these constraints is not true, use the multithreaded model.</span></span> <span data-ttu-id="64ba9-115">Legen Sie zum Angeben des Threading Modells eines der folgenden Flags im *dwcoinit* -Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="64ba9-115">To specify the threading model, set one of the following flags in the *dwCoInit* parameter.</span></span>



| <span data-ttu-id="64ba9-116">Flag</span><span class="sxs-lookup"><span data-stu-id="64ba9-116">Flag</span></span>                          | <span data-ttu-id="64ba9-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64ba9-117">Description</span></span>         |
|-------------------------------|---------------------|
| <span data-ttu-id="64ba9-118">**coinit \_ Apartmentthreaded**</span><span class="sxs-lookup"><span data-stu-id="64ba9-118">**COINIT\_APARTMENTTHREADED**</span></span> | <span data-ttu-id="64ba9-119">Apartment Thread.</span><span class="sxs-lookup"><span data-stu-id="64ba9-119">Apartment threaded.</span></span> |
| <span data-ttu-id="64ba9-120">**coinit- \_ Multithread**</span><span class="sxs-lookup"><span data-stu-id="64ba9-120">**COINIT\_MULTITHREADED**</span></span>     | <span data-ttu-id="64ba9-121">Multithread.</span><span class="sxs-lookup"><span data-stu-id="64ba9-121">Multithreaded.</span></span>      |



 

<span data-ttu-id="64ba9-122">Sie müssen genau eines dieser Flags festlegen.</span><span class="sxs-lookup"><span data-stu-id="64ba9-122">You must set exactly one of these flags.</span></span> <span data-ttu-id="64ba9-123">Im Allgemeinen sollte ein Thread, der ein Fenster erstellt, das **coinit \_ Apartmentthreaded** -Flag verwenden, und andere Threads sollten **coinit \_ Multithreaded** verwenden.</span><span class="sxs-lookup"><span data-stu-id="64ba9-123">Generally, a thread that creates a window should use the **COINIT\_APARTMENTTHREADED** flag, and other threads should use **COINIT\_MULTITHREADED**.</span></span> <span data-ttu-id="64ba9-124">Einige COM-Komponenten erfordern jedoch ein bestimmtes Threading Modell.</span><span class="sxs-lookup"><span data-stu-id="64ba9-124">However, some COM components require a particular threading model.</span></span> <span data-ttu-id="64ba9-125">In der MSDN-Dokumentation sollten Sie wissen, wann dies der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="64ba9-125">The MSDN documentation should tell you when that is the case.</span></span>

> [!Note]  
> <span data-ttu-id="64ba9-126">Selbst wenn Sie das Apartment Threading angeben, ist es weiterhin möglich, Schnittstellen zwischen Threads mithilfe einer *Methode namens* Marshalling gemeinsam zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="64ba9-126">Actually, even if you specify apartment threading, it is still possible to share interfaces between threads, by using a technique called *marshaling*.</span></span> <span data-ttu-id="64ba9-127">Das Marshalling geht über den Rahmen dieses Moduls hinaus.</span><span class="sxs-lookup"><span data-stu-id="64ba9-127">Marshaling is beyond the scope of this module.</span></span> <span data-ttu-id="64ba9-128">Wichtig ist, dass Sie beim Apartment Threading nie einfach einen Schnittstellen Zeiger auf einen anderen Thread kopieren müssen.</span><span class="sxs-lookup"><span data-stu-id="64ba9-128">The important point is that with apartment threading, you must never simply copy an interface pointer to another thread.</span></span> <span data-ttu-id="64ba9-129">Weitere Informationen zu den COM-Threading Modellen finden Sie unter [Prozesse, Threads und Apartments](/windows/desktop/com/processes--threads--and-apartments).</span><span class="sxs-lookup"><span data-stu-id="64ba9-129">For more information about the COM threading models, see [Processes, Threads, and Apartments](/windows/desktop/com/processes--threads--and-apartments).</span></span>

 

<span data-ttu-id="64ba9-130">Zusätzlich zu den bereits erwähnten Flags empfiehlt es sich, das kennflag " **coinit \_ deaktivierte \_ OLE1DDE** " im Parameter " *dwcoinit* " festzulegen.</span><span class="sxs-lookup"><span data-stu-id="64ba9-130">In addition to the flags already mentioned, it is a good idea to set the **COINIT\_DISABLE\_OLE1DDE** flag in the *dwCoInit* parameter.</span></span> <span data-ttu-id="64ba9-131">Wenn dieses Flag festgelegt wird, wird ein zusätzlicher Aufwand vermieden, der mit dem Objekt Verknüpfungs-und Einbettungs-und Einbettungs-1,0 (</span><span class="sxs-lookup"><span data-stu-id="64ba9-131">Setting this flag avoids some overhead associated with Object Linking and Embedding (OLE) 1.0, an obsolete technology.</span></span>

<span data-ttu-id="64ba9-132">Im folgenden wird erläutert, wie Sie com für Apartment Threading initialisieren:</span><span class="sxs-lookup"><span data-stu-id="64ba9-132">Here is how you would initialize COM for apartment threading:</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
```



<span data-ttu-id="64ba9-133">Der **HRESULT** -Rückgabetyp enthält einen Fehler-oder Erfolgs Code.</span><span class="sxs-lookup"><span data-stu-id="64ba9-133">The **HRESULT** return type contains an error or success code.</span></span> <span data-ttu-id="64ba9-134">Im nächsten Abschnitt sehen wir uns die com-Fehlerbehandlung an.</span><span class="sxs-lookup"><span data-stu-id="64ba9-134">We'll look at COM error handling in the next section.</span></span>

## <a name="uninitializing-the-com-library"></a><span data-ttu-id="64ba9-135">Aufheben der Initialisierung der com-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="64ba9-135">Uninitializing the COM Library</span></span>

<span data-ttu-id="64ba9-136">Bei jedem erfolgreichen Aufrufen von [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)müssen Sie " [**zählinitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) " aufrufen, bevor der Thread beendet wird.</span><span class="sxs-lookup"><span data-stu-id="64ba9-136">For every successful call to [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), you must call [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) before the thread exits.</span></span> <span data-ttu-id="64ba9-137">Diese Funktion nimmt keine Parameter an und weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="64ba9-137">This function takes no parameters and has no return value.</span></span>


```C++
CoUninitialize();
```



## <a name="next"></a><span data-ttu-id="64ba9-138">Nächste</span><span class="sxs-lookup"><span data-stu-id="64ba9-138">Next</span></span>

[<span data-ttu-id="64ba9-139">Fehler Codes in com</span><span class="sxs-lookup"><span data-stu-id="64ba9-139">Error Codes in COM</span></span>](error-codes-in-com.md)

 

 