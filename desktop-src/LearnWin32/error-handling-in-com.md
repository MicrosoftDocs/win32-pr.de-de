---
title: Fehlerbehandlung in COM (Los geht's mit Win32 und C++)
description: Fehlerbehandlung in COM (Los geht's mit Win32 und C++)
ms.assetid: 022ca652-59d2-4513-9d73-1c6d8688c478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cf89170087469fa6ef8587fb5377e6374f6a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103918"
---
# <a name="error-handling-in-com-get-started-with-win32-and-c"></a><span data-ttu-id="21dce-103">Fehlerbehandlung in COM (Los geht's mit Win32 und C++)</span><span class="sxs-lookup"><span data-stu-id="21dce-103">Error Handling in COM (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="21dce-104">COM verwendet **HRESULT-Werte,** um den Erfolg oder Fehler eines Methoden- oder Funktionsaufrufs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="21dce-104">COM uses **HRESULT** values to indicate the success or failure of a method or function call.</span></span> <span data-ttu-id="21dce-105">Verschiedene SDK-Header definieren verschiedene **HRESULT-Konstanten.**</span><span class="sxs-lookup"><span data-stu-id="21dce-105">Various SDK headers define various **HRESULT** constants.</span></span> <span data-ttu-id="21dce-106">Ein häufiger Satz von systemweiten Codes wird in WinError.h definiert.</span><span class="sxs-lookup"><span data-stu-id="21dce-106">A common set of system-wide codes is defined in WinError.h.</span></span> <span data-ttu-id="21dce-107">In der folgenden Tabelle sind einige dieser systemweiten Rückgabecodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="21dce-107">The following table shows some of those system-wide return codes.</span></span>



| <span data-ttu-id="21dce-108">Konstante</span><span class="sxs-lookup"><span data-stu-id="21dce-108">Constant</span></span>            | <span data-ttu-id="21dce-109">Numerischer Wert</span><span class="sxs-lookup"><span data-stu-id="21dce-109">Numeric value</span></span> | <span data-ttu-id="21dce-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21dce-110">Description</span></span>                                          |
|---------------------|---------------|------------------------------------------------------|
| <span data-ttu-id="21dce-111">**E \_ ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="21dce-111">**E\_ACCESSDENIED**</span></span> | <span data-ttu-id="21dce-112">0x80070005</span><span class="sxs-lookup"><span data-stu-id="21dce-112">0x80070005</span></span>    | <span data-ttu-id="21dce-113">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="21dce-113">Access denied.</span></span>                                       |
| <span data-ttu-id="21dce-114">**E \_ FAIL**</span><span class="sxs-lookup"><span data-stu-id="21dce-114">**E\_FAIL**</span></span>         | <span data-ttu-id="21dce-115">0x80004005</span><span class="sxs-lookup"><span data-stu-id="21dce-115">0x80004005</span></span>    | <span data-ttu-id="21dce-116">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="21dce-116">Unspecified error.</span></span>                                   |
| <span data-ttu-id="21dce-117">**E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="21dce-117">**E\_INVALIDARG**</span></span>   | <span data-ttu-id="21dce-118">0x80070057</span><span class="sxs-lookup"><span data-stu-id="21dce-118">0x80070057</span></span>    | <span data-ttu-id="21dce-119">Ungültiger Parameterwert.</span><span class="sxs-lookup"><span data-stu-id="21dce-119">Invalid parameter value.</span></span>                             |
| <span data-ttu-id="21dce-120">**E \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="21dce-120">**E\_OUTOFMEMORY**</span></span>  | <span data-ttu-id="21dce-121">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="21dce-121">0x8007000E</span></span>    | <span data-ttu-id="21dce-122">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="21dce-122">Out of memory.</span></span>                                       |
| <span data-ttu-id="21dce-123">**\_E-ZEIGER**</span><span class="sxs-lookup"><span data-stu-id="21dce-123">**E\_POINTER**</span></span>      | <span data-ttu-id="21dce-124">0x80004003</span><span class="sxs-lookup"><span data-stu-id="21dce-124">0x80004003</span></span>    | <span data-ttu-id="21dce-125">**NULL** wurde für einen Zeigerwert falsch übergeben.</span><span class="sxs-lookup"><span data-stu-id="21dce-125">**NULL** was passed incorrectly for a pointer value.</span></span> |
| <span data-ttu-id="21dce-126">**E \_ UNEXPECTED**</span><span class="sxs-lookup"><span data-stu-id="21dce-126">**E\_UNEXPECTED**</span></span>   | <span data-ttu-id="21dce-127">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="21dce-127">0x8000FFFF</span></span>    | <span data-ttu-id="21dce-128">Unerwartete Bedingung.</span><span class="sxs-lookup"><span data-stu-id="21dce-128">Unexpected condition.</span></span>                                |
| <span data-ttu-id="21dce-129">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="21dce-129">**S\_OK**</span></span>           | <span data-ttu-id="21dce-130">0x0</span><span class="sxs-lookup"><span data-stu-id="21dce-130">0x0</span></span>           | <span data-ttu-id="21dce-131">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="21dce-131">Success.</span></span>                                             |
| <span data-ttu-id="21dce-132">**S \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="21dce-132">**S\_FALSE**</span></span>        | <span data-ttu-id="21dce-133">0x1</span><span class="sxs-lookup"><span data-stu-id="21dce-133">0x1</span></span>           | <span data-ttu-id="21dce-134">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="21dce-134">Success.</span></span>                                             |



 

<span data-ttu-id="21dce-135">Alle Konstanten mit dem Präfix \_ "E" sind Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="21dce-135">All of the constants with the prefix "E\_" are error codes.</span></span> <span data-ttu-id="21dce-136">Die Konstanten **S \_ OK** und **S \_ FALSE** sind beide Erfolgscodes.</span><span class="sxs-lookup"><span data-stu-id="21dce-136">The constants **S\_OK** and **S\_FALSE** are both success codes.</span></span> <span data-ttu-id="21dce-137">Wahrscheinlich geben 99 % der COM-Methoden **S \_ OK** zurück, wenn sie erfolgreich sind, aber lassen Sie sich von dieser Tatsache nicht irreführen.</span><span class="sxs-lookup"><span data-stu-id="21dce-137">Probably 99% of COM methods return **S\_OK** when they succeed; but do not let this fact mislead you.</span></span> <span data-ttu-id="21dce-138">Eine Methode gibt möglicherweise andere Erfolgscodes zurück. Testen Sie daher immer mithilfe des Makros [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) oder [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) auf Fehler.</span><span class="sxs-lookup"><span data-stu-id="21dce-138">A method might return other success codes, so always test for errors by using the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) or [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="21dce-139">Der folgende Beispielcode zeigt die falsche Methode und die richtige Methode, um den Erfolg eines Funktionsaufrufs zu testen.</span><span class="sxs-lookup"><span data-stu-id="21dce-139">The following example code shows the wrong way and the right way to test for the success of a function call.</span></span>


```C++
// Wrong.
HRESULT hr = SomeFunction();
if (hr != S_OK)
{
    printf("Error!\n"); // Bad. hr might be another success code.
}

// Right.
HRESULT hr = SomeFunction();
if (FAILED(hr))
{
    printf("Error!\n"); 
}
```



<span data-ttu-id="21dce-140">Der Erfolgscode **S \_ FALSE** ist zu erwähnen.</span><span class="sxs-lookup"><span data-stu-id="21dce-140">The success code **S\_FALSE** deserves mention.</span></span> <span data-ttu-id="21dce-141">Einige Methoden verwenden **S \_ FALSE,** um ungefähr eine negative Bedingung zu bedeuten, die kein Fehler ist.</span><span class="sxs-lookup"><span data-stu-id="21dce-141">Some methods use **S\_FALSE** to mean, roughly, a negative condition that is not a failure.</span></span> <span data-ttu-id="21dce-142">Sie kann auch auf "no-op" hinweisen– die Methode war erfolgreich, hatte aber keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="21dce-142">It can also indicate a "no-op"—the method succeeded, but had no effect.</span></span> <span data-ttu-id="21dce-143">Beispielsweise gibt die [**CoInitializeEx-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) **S \_ FALSE** zurück, wenn Sie sie ein zweites Mal aus dem gleichen Thread aufrufen.</span><span class="sxs-lookup"><span data-stu-id="21dce-143">For example, the [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function returns **S\_FALSE** if you call it a second time from the same thread.</span></span> <span data-ttu-id="21dce-144">Wenn Sie in Ihrem Code zwischen **S \_ OK** und **S \_ FALSE** unterscheiden müssen, sollten Sie den Wert direkt testen, aber trotzdem [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) oder [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) verwenden, um die verbleibenden Fälle zu behandeln, wie im folgenden Beispielcode gezeigt.</span><span class="sxs-lookup"><span data-stu-id="21dce-144">If you need to differentiate between **S\_OK** and **S\_FALSE** in your code, you should test the value directly, but still use [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) or [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) to handle the remaining cases, as shown in the following example code.</span></span>


```C++
if (hr == S_FALSE)
{
    // Handle special case.
}
else if (SUCCEEDED(hr))
{
    // Handle general success case.
}
else
{
    // Handle errors.
    printf("Error!\n"); 
}
```



<span data-ttu-id="21dce-145">Einige **HRESULT-Werte** sind spezifisch für ein bestimmtes Feature oder Subsystem von Windows.</span><span class="sxs-lookup"><span data-stu-id="21dce-145">Some **HRESULT** values are specific to a particular feature or subsystem of Windows.</span></span> <span data-ttu-id="21dce-146">Beispielsweise definiert die Direct2D-Grafik-API den Fehlercode **D2DERR \_ UNSUPPORTED \_ PIXEL \_ FORMAT**, was bedeutet, dass das Programm ein nicht unterstütztes Pixelformat verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="21dce-146">For example, the Direct2D graphics API defines the error code **D2DERR\_UNSUPPORTED\_PIXEL\_FORMAT**, which means that the program used an unsupported pixel format.</span></span> <span data-ttu-id="21dce-147">Die MSDN-Dokumentation enthält häufig eine Liste spezifischer Fehlercodes, die von einer Methode zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="21dce-147">MSDN documentation often gives a list of specific error codes that a method might return.</span></span> <span data-ttu-id="21dce-148">Sie sollten diese Listen jedoch nicht als endgültig betrachten.</span><span class="sxs-lookup"><span data-stu-id="21dce-148">However, you should not consider these lists to be definitive.</span></span> <span data-ttu-id="21dce-149">Eine Methode kann immer einen **HRESULT-Wert** zurückgeben, der nicht in der Dokumentation aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="21dce-149">A method can always return an **HRESULT** value that is not listed in the documentation.</span></span> <span data-ttu-id="21dce-150">Verwenden Sie erneut die Makros [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) und [**FAILED.**](/windows/desktop/api/winerror/nf-winerror-failed)</span><span class="sxs-lookup"><span data-stu-id="21dce-150">Again, use the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) and [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macros.</span></span> <span data-ttu-id="21dce-151">Wenn Sie auf einen bestimmten Fehlercode testen, schließen Sie auch einen Standardfall ein.</span><span class="sxs-lookup"><span data-stu-id="21dce-151">If you test for a specific error code, include a default case as well.</span></span>


```C++
if (hr == D2DERR_UNSUPPORTED_PIXEL_FORMAT)
{
    // Handle the specific case of an unsupported pixel format.
}
else if (FAILED(hr))
{
    // Handle other errors.
}
```



## <a name="patterns-for-error-handling"></a><span data-ttu-id="21dce-152">Muster für die Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="21dce-152">Patterns for Error Handling</span></span>

<span data-ttu-id="21dce-153">In diesem Abschnitt werden einige Muster für die strukturierte Behandlung von COM-Fehlern behandelt.</span><span class="sxs-lookup"><span data-stu-id="21dce-153">This section looks at some patterns for handling COM errors in a structured way.</span></span> <span data-ttu-id="21dce-154">Jedes Muster hat Vor- und Nachteile.</span><span class="sxs-lookup"><span data-stu-id="21dce-154">Each pattern has advantages and disadvantages.</span></span> <span data-ttu-id="21dce-155">Bis zu einem gewissen Grad ist die Auswahl eine Frage des Vorliebes.</span><span class="sxs-lookup"><span data-stu-id="21dce-155">To some extent, the choice is a matter of taste.</span></span> <span data-ttu-id="21dce-156">Wenn Sie an einem vorhandenen Projekt arbeiten, verfügen sie möglicherweise bereits über Codierungsrichtlinien, die einen bestimmten Stil prokribieren.</span><span class="sxs-lookup"><span data-stu-id="21dce-156">If you work on an existing project, it might already have coding guidelines that proscribe a particular style.</span></span> <span data-ttu-id="21dce-157">Unabhängig davon, welches Muster Sie übernehmen, befolgt robuster Code die folgenden Regeln.</span><span class="sxs-lookup"><span data-stu-id="21dce-157">Regardless of which pattern you adopt, robust code will obey the following rules.</span></span>

-   <span data-ttu-id="21dce-158">Überprüfen Sie für jede Methode oder Funktion, die **ein HRESULT zurückgibt,** den Rückgabewert, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="21dce-158">For every method or function that returns an **HRESULT**, check the return value before proceeding.</span></span>
-   <span data-ttu-id="21dce-159">Geben Sie Ressourcen frei, nachdem sie verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="21dce-159">Release resources after they are used.</span></span>
-   <span data-ttu-id="21dce-160">Versuchen Sie nicht, auf ungültige oder nicht initialisierte Ressourcen wie **NULL-Zeiger** zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="21dce-160">Do not attempt to access invalid or uninitialized resources, such as **NULL** pointers.</span></span>
-   <span data-ttu-id="21dce-161">Versuchen Sie nicht, eine Ressource zu verwenden, nachdem Sie sie veröffentlicht haben.</span><span class="sxs-lookup"><span data-stu-id="21dce-161">Do not try to use a resource after you release it.</span></span>

<span data-ttu-id="21dce-162">Im Folgenden finden Sie vier Muster für die Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="21dce-162">With these rules in mind, here are four patterns for handling errors.</span></span>

-   [<span data-ttu-id="21dce-163">Geschachtelte ifs</span><span class="sxs-lookup"><span data-stu-id="21dce-163">Nested ifs</span></span>](#nested-ifs)
-   [<span data-ttu-id="21dce-164">Kaskadierenden Ifs</span><span class="sxs-lookup"><span data-stu-id="21dce-164">Cascading ifs</span></span>](#cascading-ifs)
-   [<span data-ttu-id="21dce-165">Jump on Fail</span><span class="sxs-lookup"><span data-stu-id="21dce-165">Jump on Fail</span></span>](#jump-on-fail)
-   [<span data-ttu-id="21dce-166">Bei Fehler auslösen</span><span class="sxs-lookup"><span data-stu-id="21dce-166">Throw on Fail</span></span>](#throw-on-fail)

### <a name="nested-ifs"></a><span data-ttu-id="21dce-167">Geschachtelte ifs</span><span class="sxs-lookup"><span data-stu-id="21dce-167">Nested ifs</span></span>

<span data-ttu-id="21dce-168">Verwenden Sie nach jedem Aufruf, der **ein HRESULT zurückgibt,** eine **if-Anweisung,** um den Erfolg zu testen.</span><span class="sxs-lookup"><span data-stu-id="21dce-168">After every call that returns an **HRESULT**, use an **if** statement to test for success.</span></span> <span data-ttu-id="21dce-169">Legen Sie dann den nächsten Methodenaufruf innerhalb des Bereichs der **if-Anweisung** ab.</span><span class="sxs-lookup"><span data-stu-id="21dce-169">Then, put the next method call within the scope of the **if** statement.</span></span> <span data-ttu-id="21dce-170">Mehr  if-Anweisungen können so tief wie nötig geschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="21dce-170">More **if** statements can be nested as deeply as needed.</span></span> <span data-ttu-id="21dce-171">In den vorherigen Codebeispielen in diesem Modul wurde dieses Muster verwendet, aber hier ist es wieder so:</span><span class="sxs-lookup"><span data-stu-id="21dce-171">The previous code examples in this module have all used this pattern, but here it is again:</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                // Use pItem (not shown). 
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    return hr;
}
```



<span data-ttu-id="21dce-172">Vorteile</span><span class="sxs-lookup"><span data-stu-id="21dce-172">Advantages</span></span>

-   <span data-ttu-id="21dce-173">Variablen können mit minimalem Gültigkeitsbereich deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="21dce-173">Variables can be declared with minimal scope.</span></span> <span data-ttu-id="21dce-174">Beispielsweise wird *pItem erst* deklariert, wenn es verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21dce-174">For example, *pItem* is not declared until it is used.</span></span>
-   <span data-ttu-id="21dce-175">Innerhalb jeder **if-Anweisung** sind bestimmte Invarianten true: Alle vorherigen Aufrufe sind erfolgreich, und alle erworbenen Ressourcen sind weiterhin gültig.</span><span class="sxs-lookup"><span data-stu-id="21dce-175">Within each **if** statement, certain invariants are true: All previous calls have succeeded, and all acquired resources are still valid.</span></span> <span data-ttu-id="21dce-176">Wenn das Programm im vorherigen Beispiel die innerste **if-Anweisung** erreicht, sind *sowohl pItem* als auch *pFileOpen* als gültig bekannt.</span><span class="sxs-lookup"><span data-stu-id="21dce-176">In the previous example, when the program reaches the innermost **if** statement, both *pItem* and *pFileOpen* are known to be valid.</span></span>
-   <span data-ttu-id="21dce-177">Es ist klar, wann Schnittstellenzeiger und andere Ressourcen veröffentlicht werden müssen.</span><span class="sxs-lookup"><span data-stu-id="21dce-177">It is clear when to release interface pointers and other resources.</span></span> <span data-ttu-id="21dce-178">Sie geben eine Ressource am Ende der **if-Anweisung** frei, die unmittelbar auf den Aufruf folgt, der die Ressource erworben hat.</span><span class="sxs-lookup"><span data-stu-id="21dce-178">You release a resource at the end of the **if** statement that immediately follows the call that acquired the resource.</span></span>

<span data-ttu-id="21dce-179">Nachteile</span><span class="sxs-lookup"><span data-stu-id="21dce-179">Disadvantages</span></span>

-   <span data-ttu-id="21dce-180">Bei einigen Personen ist die tiefe Schachtelung schwer zu lesen.</span><span class="sxs-lookup"><span data-stu-id="21dce-180">Some people find deep nesting hard to read.</span></span>
-   <span data-ttu-id="21dce-181">Die Fehlerbehandlung wird mit anderen Verzweigungs- und Schleifenanweisungen kombiniert.</span><span class="sxs-lookup"><span data-stu-id="21dce-181">Error handling is mixed in with other branching and looping statements.</span></span> <span data-ttu-id="21dce-182">Dies kann die Verfolgung der gesamten Programmlogik erschweren.</span><span class="sxs-lookup"><span data-stu-id="21dce-182">This can make the overall program logic harder to follow.</span></span>

### <a name="cascading-ifs"></a><span data-ttu-id="21dce-183">Kaskadierende Ifs</span><span class="sxs-lookup"><span data-stu-id="21dce-183">Cascading ifs</span></span>

<span data-ttu-id="21dce-184">Verwenden Sie nach jedem  Methodenaufruf eine if-Anweisung, um den Erfolg zu testen.</span><span class="sxs-lookup"><span data-stu-id="21dce-184">After each method call, use an **if** statement to test for success.</span></span> <span data-ttu-id="21dce-185">Wenn die Methode erfolgreich ist, platzieren  Sie den nächsten Methodenaufruf im if-Block.</span><span class="sxs-lookup"><span data-stu-id="21dce-185">If the method succeeds, place the next method call inside the **if** block.</span></span> <span data-ttu-id="21dce-186">Anstatt jedoch weitere **if-Anweisungen** zu schachteln, platzieren Sie jeden nachfolgenden [**SUCCEEDED-Test**](/windows/desktop/api/winerror/nf-winerror-succeeded) nach dem vorherigen **if-Block.**</span><span class="sxs-lookup"><span data-stu-id="21dce-186">But instead of nesting further **if** statements, place each subsequent [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) test after the previous **if** block.</span></span> <span data-ttu-id="21dce-187">Wenn eine Methode fehlschlägt, schlagen alle verbleibenden **SUCCEEDED-Tests** einfach fehl, bis der untere Rand der Funktion erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="21dce-187">If any method fails, all the remaining **SUCCEEDED** tests simply fail until the bottom of the function is reached.</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }
    if (SUCCEEDED(hr))
    {
        // Use pItem (not shown).
    }

    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



<span data-ttu-id="21dce-188">In diesem Muster geben Sie Ressourcen ganz am Ende der Funktion frei.</span><span class="sxs-lookup"><span data-stu-id="21dce-188">In this pattern, you release resources at the very end of the function.</span></span> <span data-ttu-id="21dce-189">Wenn ein Fehler auftritt, sind einige Zeiger möglicherweise ungültig, wenn die Funktion beendet wird.</span><span class="sxs-lookup"><span data-stu-id="21dce-189">If an error occurs, some pointers might be invalid when the function exits.</span></span> <span data-ttu-id="21dce-190">Wenn [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für einen ungültigen Zeiger aufgerufen wird, stürzt das Programm ab (oder noch schlechter). Daher müssen Sie alle Zeiger auf **NULL** initialisieren und überprüfen, ob sie **NULL** sind, bevor Sie sie freigeben.</span><span class="sxs-lookup"><span data-stu-id="21dce-190">Calling [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on an invalid pointer will crash the program (or worse), so you must initialize all pointers to **NULL** and check whether they are **NULL** before releasing them.</span></span> <span data-ttu-id="21dce-191">In diesem Beispiel wird die `SafeRelease` -Funktion verwendet. Intelligente Zeiger sind ebenfalls eine gute Wahl.</span><span class="sxs-lookup"><span data-stu-id="21dce-191">This example uses the `SafeRelease` function; smart pointers are also a good choice.</span></span>

<span data-ttu-id="21dce-192">Wenn Sie dieses Muster verwenden, müssen Sie mit Schleifenkonstrukten vorsichtig sein.</span><span class="sxs-lookup"><span data-stu-id="21dce-192">If you use this pattern, you must be careful with loop constructs.</span></span> <span data-ttu-id="21dce-193">Unterbrechen Sie innerhalb einer Schleife die Schleife, wenn ein Aufruf fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="21dce-193">Inside a loop, break from the loop if any call fails.</span></span>

<span data-ttu-id="21dce-194">Vorteile</span><span class="sxs-lookup"><span data-stu-id="21dce-194">Advantages</span></span>

-   <span data-ttu-id="21dce-195">Dieses Muster erstellt weniger Schachtelung als das "geschachtelte Ifs"-Muster.</span><span class="sxs-lookup"><span data-stu-id="21dce-195">This pattern creates less nesting than the "nested ifs" pattern.</span></span>
-   <span data-ttu-id="21dce-196">Die allgemeine Ablaufsteuerung ist einfacher zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="21dce-196">Overall control flow is easier to see.</span></span>
-   <span data-ttu-id="21dce-197">Ressourcen werden an einem Punkt im Code freigegeben.</span><span class="sxs-lookup"><span data-stu-id="21dce-197">Resources are released at one point in the code.</span></span>

<span data-ttu-id="21dce-198">Nachteile</span><span class="sxs-lookup"><span data-stu-id="21dce-198">Disadvantages</span></span>

-   <span data-ttu-id="21dce-199">Alle Variablen müssen am Anfang der Funktion deklariert und initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="21dce-199">All variables must be declared and initialized at the top of the function.</span></span>
-   <span data-ttu-id="21dce-200">Wenn ein Aufruf fehlschlägt, nimmt die Funktion mehrere nicht benötigte Fehlerüberprüfungen vor, anstatt die Funktion sofort zu beenden.</span><span class="sxs-lookup"><span data-stu-id="21dce-200">If a call fails, the function makes multiple unneeded error checks, instead of exiting the function immediately.</span></span>
-   <span data-ttu-id="21dce-201">Da der Ablauf der Steuerung nach einem Fehler durch die Funktion fortgesetzt wird, müssen Sie im gesamten Funktionstext darauf achten, nicht auf ungültige Ressourcen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="21dce-201">Because the flow of control continues through the function after a failure, you must be careful throughout the body of the function not to access invalid resources.</span></span>
-   <span data-ttu-id="21dce-202">Fehler innerhalb einer Schleife erfordern einen Sonderfall.</span><span class="sxs-lookup"><span data-stu-id="21dce-202">Errors inside a loop require a special case.</span></span>

### <a name="jump-on-fail"></a><span data-ttu-id="21dce-203">Fehler beim Springen</span><span class="sxs-lookup"><span data-stu-id="21dce-203">Jump on Fail</span></span>

<span data-ttu-id="21dce-204">Testen Sie nach jedem Methodenaufruf auf Fehler (nicht erfolgreich).</span><span class="sxs-lookup"><span data-stu-id="21dce-204">After each method call, test for failure (not success).</span></span> <span data-ttu-id="21dce-205">Wechseln Sie bei einem Fehler zu einer Bezeichnung am unteren Rand der Funktion.</span><span class="sxs-lookup"><span data-stu-id="21dce-205">On failure, jump to a label near the bottom of the function.</span></span> <span data-ttu-id="21dce-206">Geben Sie nach der Bezeichnung, aber vor dem Beenden der Funktion Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="21dce-206">After the label, but before exiting the function, release resources.</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->Show(NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->GetResult(&pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use pItem (not shown).

done:
    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



<span data-ttu-id="21dce-207">Vorteile</span><span class="sxs-lookup"><span data-stu-id="21dce-207">Advantages</span></span>

-   <span data-ttu-id="21dce-208">Die allgemeine Ablaufsteuerung ist leicht zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="21dce-208">The overall control flow is easy to see.</span></span>
-   <span data-ttu-id="21dce-209">Wenn Sie nicht zur Bezeichnung gesprungen sind, ist an jedem Punkt im Code nach einer [**FAILED-Überprüfung**](/windows/desktop/api/winerror/nf-winerror-failed) garantiert, dass alle vorherigen Aufrufe erfolgreich waren.</span><span class="sxs-lookup"><span data-stu-id="21dce-209">At every point in the code after a [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) check, if you have not jumped to the label, it is guaranteed that all the previous calls have succeeded.</span></span>
-   <span data-ttu-id="21dce-210">Ressourcen werden an einer Stelle im Code freigegeben.</span><span class="sxs-lookup"><span data-stu-id="21dce-210">Resources are released at one place in the code.</span></span>

<span data-ttu-id="21dce-211">Nachteile</span><span class="sxs-lookup"><span data-stu-id="21dce-211">Disadvantages</span></span>

-   <span data-ttu-id="21dce-212">Alle Variablen müssen am Anfang der Funktion deklariert und initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="21dce-212">All variables must be declared and initialized at the top of the function.</span></span>
-   <span data-ttu-id="21dce-213">Einige Programmierer möchten **goto** nicht in ihrem Code verwenden.</span><span class="sxs-lookup"><span data-stu-id="21dce-213">Some programmers do not like to use **goto** in their code.</span></span> <span data-ttu-id="21dce-214">(Beachten Sie jedoch, dass diese Verwendung von **goto** stark strukturiert ist. Der Code springt nie außerhalb des aktuellen Funktionsaufrufs.)</span><span class="sxs-lookup"><span data-stu-id="21dce-214">(However, it should be noted that this use of **goto** is highly structured; the code never jumps outside the current function call.)</span></span>
-   <span data-ttu-id="21dce-215">**goto-Anweisungen** überspringen Initialisierer.</span><span class="sxs-lookup"><span data-stu-id="21dce-215">**goto** statements skip initializers.</span></span>

### <a name="throw-on-fail"></a><span data-ttu-id="21dce-216">Bei Fehler auslösen</span><span class="sxs-lookup"><span data-stu-id="21dce-216">Throw on Fail</span></span>

<span data-ttu-id="21dce-217">Anstatt zu einer Bezeichnung zu springen, können Sie eine Ausnahme auslösen, wenn eine Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="21dce-217">Rather than jump to a label, you can throw an exception when a method fails.</span></span> <span data-ttu-id="21dce-218">Dies kann zu einem idiomatischen C++-Stil führen, wenn Sie es gewohnt sind, ausnahmesicheren Code zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="21dce-218">This can produce a more idiomatic style of C++ if you are used to writing exception-safe code.</span></span>


```C++
#include <comdef.h>  // Declares _com_error

inline void throw_if_fail(HRESULT hr)
{
    if (FAILED(hr))
    {
        throw _com_error(hr);
    }
}

void ShowDialog()
{
    try
    {
        CComPtr<IFileOpenDialog> pFileOpen;
        throw_if_fail(CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen)));

        throw_if_fail(pFileOpen->Show(NULL));

        CComPtr<IShellItem> pItem;
        throw_if_fail(pFileOpen->GetResult(&pItem));

        // Use pItem (not shown).
    }
    catch (_com_error err)
    {
        // Handle error.
    }
}
```



<span data-ttu-id="21dce-219">Beachten Sie, dass in diesem Beispiel die **CComPtr-Klasse** zum Verwalten von Schnittstellenzeigern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21dce-219">Notice that this example uses the **CComPtr** class to manage interface pointers.</span></span> <span data-ttu-id="21dce-220">Wenn Ihr Code Ausnahmen auslöst, sollten Sie im Allgemeinen das RAII-Muster (Resource Acquisition is Initialization) befolgen.</span><span class="sxs-lookup"><span data-stu-id="21dce-220">Generally, if your code throws exceptions, you should follow the RAII (Resource Acquisition is Initialization) pattern.</span></span> <span data-ttu-id="21dce-221">Das heißt, jede Ressource sollte von einem Objekt verwaltet werden, dessen Destruktor garantiert, dass die Ressource ordnungsgemäß freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="21dce-221">That is, every resource should be managed by an object whose destructor guarantees that the resource is correctly released.</span></span> <span data-ttu-id="21dce-222">Wenn eine Ausnahme ausgelöst wird, wird der Destruktor garantiert aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="21dce-222">If an exception is thrown, the destructor is guaranteed to be invoked.</span></span> <span data-ttu-id="21dce-223">Andernfalls kann das Programm Ressourcenverlusten.</span><span class="sxs-lookup"><span data-stu-id="21dce-223">Otherwise, your program might leak resources.</span></span>

<span data-ttu-id="21dce-224">Vorteile</span><span class="sxs-lookup"><span data-stu-id="21dce-224">Advantages</span></span>

-   <span data-ttu-id="21dce-225">Kompatibel mit vorhandenem Code, der die Ausnahmebehandlung verwendet.</span><span class="sxs-lookup"><span data-stu-id="21dce-225">Compatible with existing code that uses exception handling.</span></span>
-   <span data-ttu-id="21dce-226">Kompatibel mit C++-Bibliotheken, die Ausnahmen auslösen, z. B. die Standardvorlagenbibliothek (STL).</span><span class="sxs-lookup"><span data-stu-id="21dce-226">Compatible with C++ libraries that throw exceptions, such as the Standard Template Library (STL).</span></span>

<span data-ttu-id="21dce-227">Nachteile</span><span class="sxs-lookup"><span data-stu-id="21dce-227">Disadvantages</span></span>

-   <span data-ttu-id="21dce-228">Erfordert, dass C++-Objekte Ressourcen wie Arbeitsspeicher oder Dateihandles verwalten.</span><span class="sxs-lookup"><span data-stu-id="21dce-228">Requires C++ objects to manage resources such as memory or file handles.</span></span>
-   <span data-ttu-id="21dce-229">Erfordert ein gutes Verständnis des Schreibens von ausnahmesicherem Code.</span><span class="sxs-lookup"><span data-stu-id="21dce-229">Requires a good understanding of how to write exception-safe code.</span></span>

## <a name="next"></a><span data-ttu-id="21dce-230">Nächste</span><span class="sxs-lookup"><span data-stu-id="21dce-230">Next</span></span>

[<span data-ttu-id="21dce-231">Modul 3. Windows-Grafiken</span><span class="sxs-lookup"><span data-stu-id="21dce-231">Module 3. Windows Graphics</span></span>](module-3---windows-graphics.md)

 

 
