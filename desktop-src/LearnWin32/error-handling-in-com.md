---
title: Fehlerbehandlung in com (Get Started with Win32 and C++)
description: .
ms.assetid: 022ca652-59d2-4513-9d73-1c6d8688c478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505f8cfe6867db07da77616e6a94fdc257e32f3e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341978"
---
# <a name="error-handling-in-com-get-started-with-win32-and-c"></a><span data-ttu-id="10399-103">Fehlerbehandlung in com (Get Started with Win32 and C++)</span><span class="sxs-lookup"><span data-stu-id="10399-103">Error Handling in COM (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="10399-104">COM verwendet **HRESULT** -Werte, um den Erfolg oder Misserfolg einer Methode oder eines Funktions Aufrufes anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="10399-104">COM uses **HRESULT** values to indicate the success or failure of a method or function call.</span></span> <span data-ttu-id="10399-105">Verschiedene SDK-Header definieren verschiedene **HRESULT** -Konstanten.</span><span class="sxs-lookup"><span data-stu-id="10399-105">Various SDK headers define various **HRESULT** constants.</span></span> <span data-ttu-id="10399-106">Ein allgemeiner Satz von systemweiten Codes wird in WinError. h definiert.</span><span class="sxs-lookup"><span data-stu-id="10399-106">A common set of system-wide codes is defined in WinError.h.</span></span> <span data-ttu-id="10399-107">In der folgenden Tabelle sind einige dieser systemweiten Rückgabecodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="10399-107">The following table shows some of those system-wide return codes.</span></span>



| <span data-ttu-id="10399-108">Konstante</span><span class="sxs-lookup"><span data-stu-id="10399-108">Constant</span></span>            | <span data-ttu-id="10399-109">Numerischer Wert</span><span class="sxs-lookup"><span data-stu-id="10399-109">Numeric value</span></span> | <span data-ttu-id="10399-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10399-110">Description</span></span>                                          |
|---------------------|---------------|------------------------------------------------------|
| <span data-ttu-id="10399-111">**E \_ AccessDenied**</span><span class="sxs-lookup"><span data-stu-id="10399-111">**E\_ACCESSDENIED**</span></span> | <span data-ttu-id="10399-112">0x80070005</span><span class="sxs-lookup"><span data-stu-id="10399-112">0x80070005</span></span>    | <span data-ttu-id="10399-113">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="10399-113">Access denied.</span></span>                                       |
| <span data-ttu-id="10399-114">**E \_ fehlschlagen**</span><span class="sxs-lookup"><span data-stu-id="10399-114">**E\_FAIL**</span></span>         | <span data-ttu-id="10399-115">0x80004005</span><span class="sxs-lookup"><span data-stu-id="10399-115">0x80004005</span></span>    | <span data-ttu-id="10399-116">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="10399-116">Unspecified error.</span></span>                                   |
| <span data-ttu-id="10399-117">**E \_ invalidArg**</span><span class="sxs-lookup"><span data-stu-id="10399-117">**E\_INVALIDARG**</span></span>   | <span data-ttu-id="10399-118">0x80070057</span><span class="sxs-lookup"><span data-stu-id="10399-118">0x80070057</span></span>    | <span data-ttu-id="10399-119">Ungültiger Parameterwert.</span><span class="sxs-lookup"><span data-stu-id="10399-119">Invalid parameter value.</span></span>                             |
| <span data-ttu-id="10399-120">**E \_ outo-Memory**</span><span class="sxs-lookup"><span data-stu-id="10399-120">**E\_OUTOFMEMORY**</span></span>  | <span data-ttu-id="10399-121">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="10399-121">0x8007000E</span></span>    | <span data-ttu-id="10399-122">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="10399-122">Out of memory.</span></span>                                       |
| <span data-ttu-id="10399-123">**E- \_ Zeiger**</span><span class="sxs-lookup"><span data-stu-id="10399-123">**E\_POINTER**</span></span>      | <span data-ttu-id="10399-124">0x80004003</span><span class="sxs-lookup"><span data-stu-id="10399-124">0x80004003</span></span>    | <span data-ttu-id="10399-125">**Null** wurde für einen Zeiger Wert falsch übermittelt.</span><span class="sxs-lookup"><span data-stu-id="10399-125">**NULL** was passed incorrectly for a pointer value.</span></span> |
| <span data-ttu-id="10399-126">**E \_ unerwartet**</span><span class="sxs-lookup"><span data-stu-id="10399-126">**E\_UNEXPECTED**</span></span>   | <span data-ttu-id="10399-127">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="10399-127">0x8000FFFF</span></span>    | <span data-ttu-id="10399-128">Unerwartete Bedingung.</span><span class="sxs-lookup"><span data-stu-id="10399-128">Unexpected condition.</span></span>                                |
| <span data-ttu-id="10399-129">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="10399-129">**S\_OK**</span></span>           | <span data-ttu-id="10399-130">0x0</span><span class="sxs-lookup"><span data-stu-id="10399-130">0x0</span></span>           | <span data-ttu-id="10399-131">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="10399-131">Success.</span></span>                                             |
| <span data-ttu-id="10399-132">**S \_ false**</span><span class="sxs-lookup"><span data-stu-id="10399-132">**S\_FALSE**</span></span>        | <span data-ttu-id="10399-133">0x1</span><span class="sxs-lookup"><span data-stu-id="10399-133">0x1</span></span>           | <span data-ttu-id="10399-134">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="10399-134">Success.</span></span>                                             |



 

<span data-ttu-id="10399-135">Alle Konstanten mit dem Präfix "E \_ " sind Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="10399-135">All of the constants with the prefix "E\_" are error codes.</span></span> <span data-ttu-id="10399-136">Die Konstanten **s \_ OK** und **S \_ false** sind beide Erfolgs Codes.</span><span class="sxs-lookup"><span data-stu-id="10399-136">The constants **S\_OK** and **S\_FALSE** are both success codes.</span></span> <span data-ttu-id="10399-137">99% der com-Methoden geben bei erfolgreicher Ausführung von "S" den Wert " **\_ OK** " aus.</span><span class="sxs-lookup"><span data-stu-id="10399-137">Probably 99% of COM methods return **S\_OK** when they succeed; but do not let this fact mislead you.</span></span> <span data-ttu-id="10399-138">Eine Methode gibt möglicherweise andere Erfolgs Codes zurück. Testen Sie daher immer mit [**dem Makro**](/windows/desktop/api/winerror/nf-winerror-failed) [**erfolgreich**](/windows/desktop/api/winerror/nf-winerror-succeeded) oder Fehler.</span><span class="sxs-lookup"><span data-stu-id="10399-138">A method might return other success codes, so always test for errors by using the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) or [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="10399-139">Der folgende Beispielcode zeigt die falsche Methode und die richtige Methode zum Testen auf den Erfolg eines Funktions Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="10399-139">The following example code shows the wrong way and the right way to test for the success of a function call.</span></span>


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



<span data-ttu-id="10399-140">Die Erfolgs Codes **' \_ false** ' sollten erwähnt werden.</span><span class="sxs-lookup"><span data-stu-id="10399-140">The success code **S\_FALSE** deserves mention.</span></span> <span data-ttu-id="10399-141">Einige Methoden verwenden " **S \_ false** ", um ungefähr eine negative Bedingung zu verwenden, die kein Fehler ist.</span><span class="sxs-lookup"><span data-stu-id="10399-141">Some methods use **S\_FALSE** to mean, roughly, a negative condition that is not a failure.</span></span> <span data-ttu-id="10399-142">Es kann auch ein "No-op"-– die Methode war erfolgreich, aber hat keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="10399-142">It can also indicate a "no-op"—the method succeeded, but had no effect.</span></span> <span data-ttu-id="10399-143">Beispielsweise gibt die [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) -Funktion **S \_ false** zurück, wenn Sie Sie ein zweites Mal aus demselben Thread aufrufen.</span><span class="sxs-lookup"><span data-stu-id="10399-143">For example, the [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function returns **S\_FALSE** if you call it a second time from the same thread.</span></span> <span data-ttu-id="10399-144">Wenn Sie in Ihrem Code zwischen **S \_ OK** und **s \_ false** unterscheiden müssen, sollten Sie den Wert direkt testen, aber dennoch " [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) " [**oder "**](/windows/desktop/api/winerror/nf-winerror-succeeded) failed" verwenden, um die restlichen Fälle zu behandeln, wie im folgenden Beispielcode gezeigt.</span><span class="sxs-lookup"><span data-stu-id="10399-144">If you need to differentiate between **S\_OK** and **S\_FALSE** in your code, you should test the value directly, but still use [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) or [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) to handle the remaining cases, as shown in the following example code.</span></span>


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



<span data-ttu-id="10399-145">Einige **HRESULT** -Werte sind spezifisch für eine bestimmte Funktion oder ein bestimmtes Subsystem von Windows.</span><span class="sxs-lookup"><span data-stu-id="10399-145">Some **HRESULT** values are specific to a particular feature or subsystem of Windows.</span></span> <span data-ttu-id="10399-146">Beispielsweise wird durch die Direct2D-Grafik-API der Fehlercode **D2DERR \_ nicht unterstütztes \_ Pixel \_ Format** definiert, was bedeutet, dass das Programm ein nicht unterstütztes Pixel Format verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="10399-146">For example, the Direct2D graphics API defines the error code **D2DERR\_UNSUPPORTED\_PIXEL\_FORMAT**, which means that the program used an unsupported pixel format.</span></span> <span data-ttu-id="10399-147">Die MSDN-Dokumentation enthält häufig eine Liste mit spezifischen Fehlercodes, die von einer Methode zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="10399-147">MSDN documentation often gives a list of specific error codes that a method might return.</span></span> <span data-ttu-id="10399-148">Sie sollten diese Listen jedoch nicht als definitiv in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="10399-148">However, you should not consider these lists to be definitive.</span></span> <span data-ttu-id="10399-149">Eine Methode kann immer einen **HRESULT** -Wert zurückgeben, der nicht in der Dokumentation aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="10399-149">A method can always return an **HRESULT** value that is not listed in the documentation.</span></span> <span data-ttu-id="10399-150">Verwenden Sie erneut die Makros [**erfolgreich**](/windows/desktop/api/winerror/nf-winerror-succeeded) und [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) .</span><span class="sxs-lookup"><span data-stu-id="10399-150">Again, use the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) and [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macros.</span></span> <span data-ttu-id="10399-151">Wenn Sie auf einen bestimmten Fehlercode testen, sollten Sie auch einen Standardfall einschließen.</span><span class="sxs-lookup"><span data-stu-id="10399-151">If you test for a specific error code, include a default case as well.</span></span>


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



## <a name="patterns-for-error-handling"></a><span data-ttu-id="10399-152">Muster für die Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="10399-152">Patterns for Error Handling</span></span>

<span data-ttu-id="10399-153">In diesem Abschnitt werden einige Muster zur Behandlung von com-Fehlern auf strukturierte Weise erläutert.</span><span class="sxs-lookup"><span data-stu-id="10399-153">This section looks at some patterns for handling COM errors in a structured way.</span></span> <span data-ttu-id="10399-154">Jedes Muster hat vor-und Nachteile.</span><span class="sxs-lookup"><span data-stu-id="10399-154">Each pattern has advantages and disadvantages.</span></span> <span data-ttu-id="10399-155">In gewissem Umfang ist die Wahl eine Frage des Geschmacks.</span><span class="sxs-lookup"><span data-stu-id="10399-155">To some extent, the choice is a matter of taste.</span></span> <span data-ttu-id="10399-156">Wenn Sie an einem vorhandenen Projekt arbeiten, verfügen Sie möglicherweise bereits über Codierungs Richtlinien, die einen bestimmten Stil proschreiben.</span><span class="sxs-lookup"><span data-stu-id="10399-156">If you work on an existing project, it might already have coding guidelines that proscribe a particular style.</span></span> <span data-ttu-id="10399-157">Unabhängig davon, welches Muster Sie annehmen, befolgt robuster Code die folgenden Regeln.</span><span class="sxs-lookup"><span data-stu-id="10399-157">Regardless of which pattern you adopt, robust code will obey the following rules.</span></span>

-   <span data-ttu-id="10399-158">Überprüfen Sie für jede Methode oder Funktion, die ein **HRESULT** zurückgibt, den Rückgabewert, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="10399-158">For every method or function that returns an **HRESULT**, check the return value before proceeding.</span></span>
-   <span data-ttu-id="10399-159">Freigeben von Ressourcen nach ihrer Verwendung.</span><span class="sxs-lookup"><span data-stu-id="10399-159">Release resources after they are used.</span></span>
-   <span data-ttu-id="10399-160">Versuchen Sie nicht, auf ungültige oder nicht initialisierte Ressourcen wie z. b. **null** -Zeiger zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="10399-160">Do not attempt to access invalid or uninitialized resources, such as **NULL** pointers.</span></span>
-   <span data-ttu-id="10399-161">Versuchen Sie nicht, eine Ressource zu verwenden, nachdem Sie Sie freigegeben haben.</span><span class="sxs-lookup"><span data-stu-id="10399-161">Do not try to use a resource after you release it.</span></span>

<span data-ttu-id="10399-162">Mit diesen Regeln sind die folgenden vier Muster zum Behandeln von Fehlern zu beachten.</span><span class="sxs-lookup"><span data-stu-id="10399-162">With these rules in mind, here are four patterns for handling errors.</span></span>

-   [<span data-ttu-id="10399-163">Netsted IFS</span><span class="sxs-lookup"><span data-stu-id="10399-163">Nested ifs</span></span>](#nested-ifs)
-   [<span data-ttu-id="10399-164">Kaskadierende IFS</span><span class="sxs-lookup"><span data-stu-id="10399-164">Cascading ifs</span></span>](#cascading-ifs)
-   [<span data-ttu-id="10399-165">Springen bei Fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="10399-165">Jump on Fail</span></span>](#jump-on-fail)
-   [<span data-ttu-id="10399-166">Auslösen bei Fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="10399-166">Throw on Fail</span></span>](#throw-on-fail)

### <a name="nested-ifs"></a><span data-ttu-id="10399-167">Netsted IFS</span><span class="sxs-lookup"><span data-stu-id="10399-167">Nested ifs</span></span>

<span data-ttu-id="10399-168">Verwenden Sie nach jedem Rückruf, der ein **HRESULT** zurückgibt, eine **if** -Anweisung, um den Erfolg zu testen.</span><span class="sxs-lookup"><span data-stu-id="10399-168">After every call that returns an **HRESULT**, use an **if** statement to test for success.</span></span> <span data-ttu-id="10399-169">Fügen Sie anschließend den nächsten Methoden aufrufim Gültigkeitsbereich der **if** -Anweisung ein.</span><span class="sxs-lookup"><span data-stu-id="10399-169">Then, put the next method call within the scope of the **if** statement.</span></span> <span data-ttu-id="10399-170">Weitere **if** -Anweisungen können bei Bedarf beliebig geschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="10399-170">More **if** statements can be nested as deeply as needed.</span></span> <span data-ttu-id="10399-171">Die vorherigen Codebeispiele in diesem Modul haben dieses Muster verwendet, aber hier ist es noch einmal:</span><span class="sxs-lookup"><span data-stu-id="10399-171">The previous code examples in this module have all used this pattern, but here it is again:</span></span>


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



<span data-ttu-id="10399-172">Vorteile</span><span class="sxs-lookup"><span data-stu-id="10399-172">Advantages</span></span>

-   <span data-ttu-id="10399-173">Variablen können mit minimalem Gültigkeitsbereich deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="10399-173">Variables can be declared with minimal scope.</span></span> <span data-ttu-id="10399-174">Beispielsweise wird *pitem* erst deklariert, wenn es verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="10399-174">For example, *pItem* is not declared until it is used.</span></span>
-   <span data-ttu-id="10399-175">In jeder **if** -Anweisung haben bestimmte invarianten den Wert "true": alle vorherigen Aufrufe waren erfolgreich, und alle erhaltenen Ressourcen sind weiterhin gültig.</span><span class="sxs-lookup"><span data-stu-id="10399-175">Within each **if** statement, certain invariants are true: All previous calls have succeeded, and all acquired resources are still valid.</span></span> <span data-ttu-id="10399-176">Wenn das Programm im vorherigen Beispiel die innerste **if** -Anweisung erreicht, sind sowohl *pitem* als auch *pfileopen* als gültig bekannt.</span><span class="sxs-lookup"><span data-stu-id="10399-176">In the previous example, when the program reaches the innermost **if** statement, both *pItem* and *pFileOpen* are known to be valid.</span></span>
-   <span data-ttu-id="10399-177">Es ist klar, wann Schnittstellen Zeiger und andere Ressourcen freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="10399-177">It is clear when to release interface pointers and other resources.</span></span> <span data-ttu-id="10399-178">Sie geben eine Ressource am Ende der **if** -Anweisung frei, die direkt auf den-Rückruf folgt, der die Ressource abgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="10399-178">You release a resource at the end of the **if** statement that immediately follows the call that acquired the resource.</span></span>

<span data-ttu-id="10399-179">Nachteile</span><span class="sxs-lookup"><span data-stu-id="10399-179">Disadvantages</span></span>

-   <span data-ttu-id="10399-180">Einige Leute finden die Tiefe Schachtelung schwer lesbar.</span><span class="sxs-lookup"><span data-stu-id="10399-180">Some people find deep nesting hard to read.</span></span>
-   <span data-ttu-id="10399-181">Die Fehlerbehandlung ist mit anderen Verzweigungs-und Schleifen Anweisungen gemischt.</span><span class="sxs-lookup"><span data-stu-id="10399-181">Error handling is mixed in with other branching and looping statements.</span></span> <span data-ttu-id="10399-182">Dadurch kann die gesamte Programmlogik schwerer befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="10399-182">This can make the overall program logic harder to follow.</span></span>

### <a name="cascading-ifs"></a><span data-ttu-id="10399-183">Kaskadierende IFS</span><span class="sxs-lookup"><span data-stu-id="10399-183">Cascading ifs</span></span>

<span data-ttu-id="10399-184">Verwenden Sie nach jedem Methoden Aufrufes eine **if** -Anweisung, um den Erfolg zu testen.</span><span class="sxs-lookup"><span data-stu-id="10399-184">After each method call, use an **if** statement to test for success.</span></span> <span data-ttu-id="10399-185">Wenn die Methode erfolgreich ist, platzieren Sie den nächsten Methoden Aufrufvorgang innerhalb des **if** -Blocks.</span><span class="sxs-lookup"><span data-stu-id="10399-185">If the method succeeds, place the next method call inside the **if** block.</span></span> <span data-ttu-id="10399-186">Anstatt weitere **if** -Anweisungen zu schachteln, platzieren Sie jeden [**nachfolgenden**](/windows/desktop/api/winerror/nf-winerror-succeeded) erfolgreichen Test nach dem vorherigen **if** -Block.</span><span class="sxs-lookup"><span data-stu-id="10399-186">But instead of nesting further **if** statements, place each subsequent [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) test after the previous **if** block.</span></span> <span data-ttu-id="10399-187">Wenn eine Methode fehlschlägt, schlagen alle **verbleibenden** erfolgreichen Tests einfach fehl, bis das Ende der Funktion erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="10399-187">If any method fails, all the remaining **SUCCEEDED** tests simply fail until the bottom of the function is reached.</span></span>


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



<span data-ttu-id="10399-188">In diesem Muster veröffentlichen Sie Ressourcen am Ende der Funktion.</span><span class="sxs-lookup"><span data-stu-id="10399-188">In this pattern, you release resources at the very end of the function.</span></span> <span data-ttu-id="10399-189">Wenn ein Fehler auftritt, sind einige Zeiger möglicherweise ungültig, wenn die Funktion beendet wird.</span><span class="sxs-lookup"><span data-stu-id="10399-189">If an error occurs, some pointers might be invalid when the function exits.</span></span> <span data-ttu-id="10399-190">Wenn Sie die [**Freigabe**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf einem ungültigen Zeiger aufrufen, stürzt das Programm ab (oder schlimmer), sodass Sie alle Zeiger auf **null** initialisieren und prüfen müssen, ob Sie **null** sind, bevor Sie Sie freigeben.</span><span class="sxs-lookup"><span data-stu-id="10399-190">Calling [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on an invalid pointer will crash the program (or worse), so you must initialize all pointers to **NULL** and check whether they are **NULL** before releasing them.</span></span> <span data-ttu-id="10399-191">In diesem Beispiel wird die- `SafeRelease` Funktion verwendet. intelligente Zeiger sind ebenfalls eine gute Wahl.</span><span class="sxs-lookup"><span data-stu-id="10399-191">This example uses the `SafeRelease` function; smart pointers are also a good choice.</span></span>

<span data-ttu-id="10399-192">Wenn Sie dieses Muster verwenden, müssen Sie mit Schleifen Konstrukten bedacht werden.</span><span class="sxs-lookup"><span data-stu-id="10399-192">If you use this pattern, you must be careful with loop constructs.</span></span> <span data-ttu-id="10399-193">Brechen Sie in einer Schleife die Schleife ab, wenn ein beliebiger Rückruf fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="10399-193">Inside a loop, break from the loop if any call fails.</span></span>

<span data-ttu-id="10399-194">Vorteile</span><span class="sxs-lookup"><span data-stu-id="10399-194">Advantages</span></span>

-   <span data-ttu-id="10399-195">Dieses Muster erstellt weniger Schachtelung als das "Nested IFS"-Muster.</span><span class="sxs-lookup"><span data-stu-id="10399-195">This pattern creates less nesting than the "nested ifs" pattern.</span></span>
-   <span data-ttu-id="10399-196">Die allgemeine Ablauf Steuerung ist leichter zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="10399-196">Overall control flow is easier to see.</span></span>
-   <span data-ttu-id="10399-197">Ressourcen werden an einem Punkt im Code freigegeben.</span><span class="sxs-lookup"><span data-stu-id="10399-197">Resources are released at one point in the code.</span></span>

<span data-ttu-id="10399-198">Nachteile</span><span class="sxs-lookup"><span data-stu-id="10399-198">Disadvantages</span></span>

-   <span data-ttu-id="10399-199">Alle Variablen müssen am Anfang der Funktion deklariert und initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="10399-199">All variables must be declared and initialized at the top of the function.</span></span>
-   <span data-ttu-id="10399-200">Wenn ein-Befehl fehlschlägt, führt die Funktion mehrere nicht benötigte Fehlerüberprüfungen aus, anstatt die Funktion sofort zu beenden.</span><span class="sxs-lookup"><span data-stu-id="10399-200">If a call fails, the function makes multiple unneeded error checks, instead of exiting the function immediately.</span></span>
-   <span data-ttu-id="10399-201">Da der Ablauf der Steuerung nach einem Fehler durch die Funktion weitergeleitet wird, müssen Sie im gesamten Text der Funktion darauf achten, dass Sie nicht auf ungültige Ressourcen zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="10399-201">Because the flow of control continues through the function after a failure, you must be careful throughout the body of the function not to access invalid resources.</span></span>
-   <span data-ttu-id="10399-202">Fehler in einer Schleife erfordern einen Sonderfall.</span><span class="sxs-lookup"><span data-stu-id="10399-202">Errors inside a loop require a special case.</span></span>

### <a name="jump-on-fail"></a><span data-ttu-id="10399-203">Springen bei Fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="10399-203">Jump on Fail</span></span>

<span data-ttu-id="10399-204">Prüfen Sie nach jedem Methoden Aufrufversuch, dass ein Fehler auftritt (nicht erfolgreich).</span><span class="sxs-lookup"><span data-stu-id="10399-204">After each method call, test for failure (not success).</span></span> <span data-ttu-id="10399-205">Springen Sie bei einem Fehler zu einer Bezeichnung am Ende der Funktion.</span><span class="sxs-lookup"><span data-stu-id="10399-205">On failure, jump to a label near the bottom of the function.</span></span> <span data-ttu-id="10399-206">Geben Sie nach der Bezeichnung, aber vor dem Beenden der Funktion Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="10399-206">After the label, but before exiting the function, release resources.</span></span>


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



<span data-ttu-id="10399-207">Vorteile</span><span class="sxs-lookup"><span data-stu-id="10399-207">Advantages</span></span>

-   <span data-ttu-id="10399-208">Die allgemeine Ablauf Steuerung ist leicht zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="10399-208">The overall control flow is easy to see.</span></span>
-   <span data-ttu-id="10399-209">An jedem Punkt im Code nach einer [**fehlgeschlagenen**](/windows/desktop/api/winerror/nf-winerror-failed) Überprüfung ist sichergestellt, dass alle vorherigen Aufrufe erfolgreich waren, wenn Sie nicht auf die Bezeichnung gesprungen sind.</span><span class="sxs-lookup"><span data-stu-id="10399-209">At every point in the code after a [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) check, if you have not jumped to the label, it is guaranteed that all the previous calls have succeeded.</span></span>
-   <span data-ttu-id="10399-210">Ressourcen werden an einem Ort im Code freigegeben.</span><span class="sxs-lookup"><span data-stu-id="10399-210">Resources are released at one place in the code.</span></span>

<span data-ttu-id="10399-211">Nachteile</span><span class="sxs-lookup"><span data-stu-id="10399-211">Disadvantages</span></span>

-   <span data-ttu-id="10399-212">Alle Variablen müssen am Anfang der Funktion deklariert und initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="10399-212">All variables must be declared and initialized at the top of the function.</span></span>
-   <span data-ttu-id="10399-213">Einige Programmierer möchten **goto** nicht in Ihrem Code verwenden.</span><span class="sxs-lookup"><span data-stu-id="10399-213">Some programmers do not like to use **goto** in their code.</span></span> <span data-ttu-id="10399-214">(Es sollte jedoch beachtet werden, dass diese Verwendung von **goto** sehr strukturiert ist. der Code springt nie außerhalb des aktuellen Funktions Aufrufes.)</span><span class="sxs-lookup"><span data-stu-id="10399-214">(However, it should be noted that this use of **goto** is highly structured; the code never jumps outside the current function call.)</span></span>
-   <span data-ttu-id="10399-215">**goto** -Anweisungen überspringen Initialisierer.</span><span class="sxs-lookup"><span data-stu-id="10399-215">**goto** statements skip initializers.</span></span>

### <a name="throw-on-fail"></a><span data-ttu-id="10399-216">Auslösen bei Fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="10399-216">Throw on Fail</span></span>

<span data-ttu-id="10399-217">Anstatt zu einer Bezeichnung zu springen, können Sie eine Ausnahme auslösen, wenn eine Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="10399-217">Rather than jump to a label, you can throw an exception when a method fails.</span></span> <span data-ttu-id="10399-218">Dies kann zu einem eher idiomatischen Stil von C++ führen, wenn Sie zum Schreiben von Ausnahme sicherem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10399-218">This can produce a more idiomatic style of C++ if you are used to writing exception-safe code.</span></span>


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



<span data-ttu-id="10399-219">Beachten Sie, dass in diesem Beispiel die **CComPtr** -Klasse zum Verwalten von Schnittstellen Zeigern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="10399-219">Notice that this example uses the **CComPtr** class to manage interface pointers.</span></span> <span data-ttu-id="10399-220">Wenn Ihr Code Ausnahmen auslöst, sollten Sie im Allgemeinen das Muster RAII (Resource Acquisition Is Initialization) befolgen.</span><span class="sxs-lookup"><span data-stu-id="10399-220">Generally, if your code throws exceptions, you should follow the RAII (Resource Acquisition is Initialization) pattern.</span></span> <span data-ttu-id="10399-221">Das heißt, jede Ressource sollte von einem Objekt verwaltet werden, dessen Dekonstruktor gewährleistet, dass die Ressource ordnungsgemäß freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="10399-221">That is, every resource should be managed by an object whose destructor guarantees that the resource is correctly released.</span></span> <span data-ttu-id="10399-222">Wenn eine Ausnahme ausgelöst wird, wird sichergestellt, dass der Dekonstruktor aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="10399-222">If an exception is thrown, the destructor is guaranteed to be invoked.</span></span> <span data-ttu-id="10399-223">Andernfalls könnte das Programmressourcen nicht mehr unterliegen.</span><span class="sxs-lookup"><span data-stu-id="10399-223">Otherwise, your program might leak resources.</span></span>

<span data-ttu-id="10399-224">Vorteile</span><span class="sxs-lookup"><span data-stu-id="10399-224">Advantages</span></span>

-   <span data-ttu-id="10399-225">Kompatibel mit vorhandenem Code, der die Ausnahmebehandlung verwendet.</span><span class="sxs-lookup"><span data-stu-id="10399-225">Compatible with existing code that uses exception handling.</span></span>
-   <span data-ttu-id="10399-226">Kompatibel mit C++-Bibliotheken, die Ausnahmen auslösen, wie z. b. die Standard Vorlagen Bibliothek (STL).</span><span class="sxs-lookup"><span data-stu-id="10399-226">Compatible with C++ libraries that throw exceptions, such as the Standard Template Library (STL).</span></span>

<span data-ttu-id="10399-227">Nachteile</span><span class="sxs-lookup"><span data-stu-id="10399-227">Disadvantages</span></span>

-   <span data-ttu-id="10399-228">Erfordert C++-Objekte, um Ressourcen wie Arbeitsspeicher oder Datei Handles zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="10399-228">Requires C++ objects to manage resources such as memory or file handles.</span></span>
-   <span data-ttu-id="10399-229">Erfordert ein gutes Verständnis für das Schreiben von Ausnahme sicherem Code.</span><span class="sxs-lookup"><span data-stu-id="10399-229">Requires a good understanding of how to write exception-safe code.</span></span>

## <a name="next"></a><span data-ttu-id="10399-230">Nächste</span><span class="sxs-lookup"><span data-stu-id="10399-230">Next</span></span>

[<span data-ttu-id="10399-231">Modul 3. Windows-Grafiken</span><span class="sxs-lookup"><span data-stu-id="10399-231">Module 3. Windows Graphics</span></span>](module-3---windows-graphics.md)

 

 
