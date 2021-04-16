---
title: Verwalten der Lebensdauer eines Objekts
description: Erfahren Sie, wie Sie die adressf-und releasemethoden verwalten, um die Lebensdauer eines Objekts zu steuern.
ms.assetid: 0e522ded-8976-4cdd-9a61-eae7834c896b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495e657863150612e5b8efa21fff0b00c7a936b9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104551680"
---
# <a name="managing-the-lifetime-of-an-object"></a><span data-ttu-id="cc4f8-103">Verwalten der Lebensdauer eines Objekts</span><span class="sxs-lookup"><span data-stu-id="cc4f8-103">Managing the Lifetime of an Object</span></span>

<span data-ttu-id="cc4f8-104">Es gibt eine Regel für COM-Schnittstellen, die noch nicht erwähnt wurden.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-104">There is a rule for COM interfaces that we have not yet mentioned.</span></span> <span data-ttu-id="cc4f8-105">Jede COM-Schnittstelle muss direkt oder indirekt von einer Schnittstelle mit dem Namen " [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)" erben.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-105">Every COM interface must inherit, directly or indirectly, from an interface named [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="cc4f8-106">Diese Schnittstelle bietet einige grundlegende Funktionen, die alle COM-Objekte unterstützen müssen.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-106">This interface provides some baseline capabilities that all COM objects must support.</span></span>

<span data-ttu-id="cc4f8-107">Die [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle definiert drei Methoden:</span><span class="sxs-lookup"><span data-stu-id="cc4f8-107">The [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface defines three methods:</span></span>

-   <span data-ttu-id="cc4f8-108">[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="cc4f8-108">[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
-   [<span data-ttu-id="cc4f8-109">**AddRef**</span><span class="sxs-lookup"><span data-stu-id="cc4f8-109">**AddRef**</span></span>](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)
-   [<span data-ttu-id="cc4f8-110">**Release**</span><span class="sxs-lookup"><span data-stu-id="cc4f8-110">**Release**</span></span>](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)

<span data-ttu-id="cc4f8-111">Die [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode ermöglicht einem Programm, die Funktionen des Objekts zur Laufzeit abzufragen.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-111">The [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method enables a program to query the capabilities of the object at run time.</span></span> <span data-ttu-id="cc4f8-112">Weitere Informationen dazu finden Sie im nächsten Thema, in dem [ein Objekt für eine Schnittstelle abgefragt](asking-an-object-for-an-interface.md)wird.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-112">We'll say more about that in the next topic, [Asking an Object for an Interface](asking-an-object-for-an-interface.md).</span></span> <span data-ttu-id="cc4f8-113">Die [**adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) -und [**releasemethoden**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) werden verwendet, um die Lebensdauer eines Objekts zu steuern.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-113">The [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods are used to control the lifetime of an object.</span></span> <span data-ttu-id="cc4f8-114">Dies ist der Betreff dieses Themas.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-114">This is the subject of this topic.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="cc4f8-115">Verweis Zählung</span><span class="sxs-lookup"><span data-stu-id="cc4f8-115">Reference Counting</span></span>

<span data-ttu-id="cc4f8-116">Was ein Programm möglicherweise tut, wird zu einem bestimmten Zeitpunkt Ressourcen zuweisen und freigeben.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-116">Whatever else a program might do, at some point it will allocate and free resources.</span></span> <span data-ttu-id="cc4f8-117">Das Zuordnen einer Ressource ist einfach.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-117">Allocating a resource is easy.</span></span> <span data-ttu-id="cc4f8-118">Das wissen, wann die Ressource freigegeben werden soll, ist schwierig, insbesondere, wenn die Lebensdauer der Ressource den aktuellen Bereich überschreitet.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-118">Knowing when to free the resource is hard, especially if the lifetime of the resource extends beyond the current scope.</span></span> <span data-ttu-id="cc4f8-119">Dieses Problem ist nicht eindeutig für com.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-119">This problem is not unique to COM.</span></span> <span data-ttu-id="cc4f8-120">Alle Programme, die Heap Speicher zuweisen, müssen das gleiche Problem lösen.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-120">Any program that allocates heap memory must solve the same problem.</span></span> <span data-ttu-id="cc4f8-121">Beispielsweise verwendet C++ automatische de-dektoren, während c# und Java Garbage Collection verwenden.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-121">For example, C++ uses automatic destructors, while C# and Java use garbage collection.</span></span> <span data-ttu-id="cc4f8-122">COM verwendet einen Ansatz namens *Verweis Zählung*.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-122">COM uses an approach called *reference counting*.</span></span>

<span data-ttu-id="cc4f8-123">Jedes COM-Objekt behält eine interne Anzahl bei.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-123">Every COM object maintains an internal count.</span></span> <span data-ttu-id="cc4f8-124">Dies wird als Verweis Zähler bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-124">This is known as the reference count.</span></span> <span data-ttu-id="cc4f8-125">Der Verweis Zähler verfolgt, wie viele Verweise auf das Objekt zurzeit aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-125">The reference count tracks how many references to the object are currently active.</span></span> <span data-ttu-id="cc4f8-126">Wenn die Anzahl der Verweise auf Null sinkt, löscht das Objekt sich selbst.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-126">When the number of references drops to zero, the object deletes itself.</span></span> <span data-ttu-id="cc4f8-127">Der letzte Teil sollte sich wiederholen: das Objekt löscht sich selbst.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-127">The last part is worth repeating: The object deletes itself.</span></span> <span data-ttu-id="cc4f8-128">Das Programm löscht das Objekt nie explizit.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-128">The program never explicitly deletes the object.</span></span>

<span data-ttu-id="cc4f8-129">Im folgenden sind die Regeln für die Verweis Zählung aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="cc4f8-129">Here are the rules for reference counting:</span></span>

-   <span data-ttu-id="cc4f8-130">Wenn das Objekt erstmalig erstellt wird, ist der Verweis Zähler 1.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-130">When the object is first created, its reference count is 1.</span></span> <span data-ttu-id="cc4f8-131">An diesem Punkt verfügt das Programm über einen einzelnen Zeiger auf das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-131">At this point, the program has a single pointer to the object.</span></span>
-   <span data-ttu-id="cc4f8-132">Das Programm kann einen neuen Verweis erstellen, indem der Zeiger dupliziert (kopiert) wird.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-132">The program can create a new reference by duplicating (copying) the pointer.</span></span> <span data-ttu-id="cc4f8-133">Wenn Sie den Zeiger kopieren, müssen Sie die [**adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) -Methode des Objekts aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-133">When you copy the pointer, you must call the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method of the object.</span></span> <span data-ttu-id="cc4f8-134">Diese Methode erhöht den Verweis Zähler um 1.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-134">This method increments the reference count by one.</span></span>
-   <span data-ttu-id="cc4f8-135">Wenn Sie mit der Verwendung eines Zeigers auf das-Objekt fertig sind, müssen Sie [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)abrufen.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-135">When you are finished using a pointer to the object, you must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="cc4f8-136">Die **releasemethode** verringert den Verweis Zähler um 1.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-136">The **Release** method decrements the reference count by one.</span></span> <span data-ttu-id="cc4f8-137">Außerdem wird der Zeiger für ungültig erklärt.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-137">It also invalidates the pointer.</span></span> <span data-ttu-id="cc4f8-138">Verwenden Sie den Zeiger nicht erneut, nachdem Sie **Release** aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-138">Do not use the pointer again after you call **Release**.</span></span> <span data-ttu-id="cc4f8-139">(Wenn Sie über andere Zeiger auf dasselbe Objekt verfügen, können Sie diese Zeiger weiterhin verwenden.)</span><span class="sxs-lookup"><span data-stu-id="cc4f8-139">(If you have other pointers to the same object, you can continue to use those pointers.)</span></span>
-   <span data-ttu-id="cc4f8-140">Wenn Sie [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) mit jedem Zeiger aufgerufen haben, erreicht der Objekt Verweis Zähler des Objekts 0 (null), und das Objekt löscht sich selbst.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-140">When you have called [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) with every pointer, the object reference count of the object reaches zero, and the object deletes itself.</span></span>

<span data-ttu-id="cc4f8-141">Im folgenden Diagramm wird ein einfacher, aber typischer Fall angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-141">The following diagram shows a simple but typical case.</span></span>

![Diagramm, das einen einfachen Fall der Verweis Zählung anzeigt.](images/com04.png)

<span data-ttu-id="cc4f8-143">Das Programm erstellt ein-Objekt und speichert einen Zeiger (*p*) für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-143">The program creates an object and stores a pointer (*p*) to the object.</span></span> <span data-ttu-id="cc4f8-144">An diesem Punkt ist der Verweis Zähler 1.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-144">At this point, the reference count is 1.</span></span> <span data-ttu-id="cc4f8-145">Wenn das Programm mit dem-Zeiger fertig ist, wird [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-145">When the program is finished using the pointer, it calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="cc4f8-146">Der Verweis Zähler wird auf 0 (null) dekrementiert, und das Objekt löscht sich selbst.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-146">The reference count is decremented to zero, and the object deletes itself.</span></span> <span data-ttu-id="cc4f8-147">*P* ist nun ungültig.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-147">Now *p* is invalid.</span></span> <span data-ttu-id="cc4f8-148">Es ist ein Fehler, *p* für weitere Methodenaufrufe zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-148">It is an error to use *p* for any further method calls.</span></span>

<span data-ttu-id="cc4f8-149">Das nächste Diagramm zeigt ein komplexeres Beispiel.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-149">The next diagram shows a more complex example.</span></span>

![Darstellung der Verweis Zählung](images/com05.png)

<span data-ttu-id="cc4f8-151">Hier erstellt das Programm ein Objekt und speichert den Zeiger *p* wie zuvor.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-151">Here, the program creates an object and stores the pointer *p*, as before.</span></span> <span data-ttu-id="cc4f8-152">Als nächstes kopiert das Programm *p* in eine neue Variable, *f*.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-152">Next, the program copies *p* to a new variable, *q*.</span></span> <span data-ttu-id="cc4f8-153">An diesem Punkt muss das Programm die [**adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) anrufen, um den Verweis Zähler zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-153">At this point, the program must call [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) to increment the reference count.</span></span> <span data-ttu-id="cc4f8-154">Der Verweis Zähler ist jetzt 2, und es gibt zwei gültige Zeiger auf das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-154">The reference count is now 2, and there are two valid pointers to the object.</span></span> <span data-ttu-id="cc4f8-155">Nehmen Sie nun an, dass das Programm die Verwendung von *p* beendet hat.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-155">Now suppose that the program is finished using *p*.</span></span> <span data-ttu-id="cc4f8-156">Das Programm ruft [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)auf, der Verweis Zähler wird auf 1 und *p* nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-156">The program calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), the reference count goes to 1, and *p* is no longer valid.</span></span> <span data-ttu-id="cc4f8-157">*Q* ist jedoch weiterhin gültig.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-157">However, *q* is still valid.</span></span> <span data-ttu-id="cc4f8-158">Später wird das Programm mit *q* beendet.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-158">Later, the program finishes using *q*.</span></span> <span data-ttu-id="cc4f8-159">Daher wird **Release** erneut aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-159">Therefore, it calls **Release** again.</span></span> <span data-ttu-id="cc4f8-160">Der Verweis Zähler wird auf 0 (null) gesetzt, und das Objekt löscht sich selbst.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-160">The reference count goes to zero, and the object deletes itself.</span></span>

<span data-ttu-id="cc4f8-161">Vielleicht Fragen Sie sich, warum das Programm *p* kopieren würde.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-161">You might wonder why the program would copy *p*.</span></span> <span data-ttu-id="cc4f8-162">Es gibt zwei Hauptgründe: Erstens können Sie den Zeiger in einer Datenstruktur speichern, z. b. in einer Liste.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-162">There are two main reasons: First, you might want to store the pointer in a data structure, such as a list.</span></span> <span data-ttu-id="cc4f8-163">Zweitens können Sie den Zeiger über den aktuellen Gültigkeitsbereich der ursprünglichen Variablen hinaus behalten.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-163">Second, you might want to keep the pointer beyond the current scope of the original variable.</span></span> <span data-ttu-id="cc4f8-164">Daher müssen Sie Sie in eine neue Variable mit größerem Gültigkeitsbereich kopieren.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-164">Therefore, you would copy it to a new variable with wider scope.</span></span>

<span data-ttu-id="cc4f8-165">Ein Vorteil der Verweis Zählung besteht darin, dass Sie Zeiger in verschiedenen Code Abschnitten freigeben können, ohne dass die verschiedenen Codepfade zum Löschen des Objekts koordiniert werden.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-165">One advantage of reference counting is that you can share pointers across different sections of code, without the various code paths coordinating to delete the object.</span></span> <span data-ttu-id="cc4f8-166">Stattdessen ruft jeder Codepfad nur [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf, wenn dieser Codepfad mithilfe des-Objekts durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-166">Instead, each code path merely calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) when that code path is done using the object.</span></span> <span data-ttu-id="cc4f8-167">Das Objekt behandelt das Löschen selbst zur richtigen Zeit.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-167">The object handles deleting itself at the correct time.</span></span>

## <a name="example"></a><span data-ttu-id="cc4f8-168">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cc4f8-168">Example</span></span>

<span data-ttu-id="cc4f8-169">Im folgenden Beispiel wird der Code aus dem [Dialogfeld "Öffnen" angezeigt](example--the-open-dialog-box.md) .</span><span class="sxs-lookup"><span data-stu-id="cc4f8-169">Here is the code from the [Open dialog box example](example--the-open-dialog-box.md) again.</span></span>

```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    IFileOpenDialog *pFileOpen;

    hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL,
            IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                PWSTR pszFilePath;
                hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
                if (SUCCEEDED(hr))
                {
                    MessageBox(NULL, pszFilePath, L&quot;File Path&quot;, MB_OK);
                    CoTaskMemFree(pszFilePath);
                }
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    CoUninitialize();
}
````

<span data-ttu-id="cc4f8-170">Die Verweis Zählung tritt an zwei Stellen in diesem Code auf.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-170">Reference counting occurs in two places in this code.</span></span> <span data-ttu-id="cc4f8-171">Wenn das Programm das allgemeine Element Dialogfeld Objekt erstellt, muss es zuerst [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf dem *pfileopen* -Zeiger aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-171">First, if program successfully creates the Common Item Dialog object, it must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on the *pFileOpen* pointer.</span></span>

```C++
hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
        IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

if (SUCCEEDED(hr))
{
    // ...
    pFileOpen->Release();
}
```

<span data-ttu-id="cc4f8-172">Zweitens: Wenn die [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) -Methode einen Zeiger auf die [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) -Schnittstelle zurückgibt, muss das Programm [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf dem *pitem* -Zeiger aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-172">Second, when the [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) method returns a pointer to the [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) interface, the program must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on the *pItem* pointer.</span></span>

```C++
hr = pFileOpen->GetResult(&pItem);

if (SUCCEEDED(hr))
{
    // ...
    pItem->Release();
}
```

<span data-ttu-id="cc4f8-173">Beachten Sie, dass in beiden Fällen der [**releasebefehl**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) der letzte Vorgang ist, der auftritt, bevor der Zeiger den Gültigkeitsbereich verlässt.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-173">Notice that in both cases, the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) call is the last thing that happens before the pointer goes out of scope.</span></span> <span data-ttu-id="cc4f8-174">Beachten Sie auch, dass **Release** erst aufgerufen wird, nachdem Sie das **HRESULT** auf Erfolg getestet haben.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-174">Also notice that **Release** is called only after you test the **HRESULT** for success.</span></span> <span data-ttu-id="cc4f8-175">Wenn z. b. beim Aufrufen von [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ein Fehler auftritt, ist der *pfileopen* -Zeiger ungültig.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-175">For example, if the call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fails, the *pFileOpen* pointer is not valid.</span></span> <span data-ttu-id="cc4f8-176">Daher ist es ein Fehler, **Release** auf dem Zeiger aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="cc4f8-176">Therefore, it would be an error to call **Release** on the pointer.</span></span>

## <a name="next"></a><span data-ttu-id="cc4f8-177">Nächste</span><span class="sxs-lookup"><span data-stu-id="cc4f8-177">Next</span></span>

[<span data-ttu-id="cc4f8-178">Anfordern eines Objekts für eine Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cc4f8-178">Asking an Object for an Interface</span></span>](asking-an-object-for-an-interface.md)