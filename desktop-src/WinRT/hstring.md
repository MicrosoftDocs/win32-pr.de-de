---
description: Ein Handle für eine Windows-Runtime Zeichenfolge.
ms.assetid: 763ACE57-EFDD-482E-851E-668D7756C5DF
title: Hstring (hstring. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9e73d7627a4bab8f02a95056e5b208569d922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348398"
---
# <a name="hstring"></a><span data-ttu-id="9a2b9-103">HSTRING</span><span class="sxs-lookup"><span data-stu-id="9a2b9-103">HSTRING</span></span>

<span data-ttu-id="9a2b9-104">Ein Handle für eine Windows-Runtime Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-104">A handle to a Windows Runtime string.</span></span>


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a><span data-ttu-id="9a2b9-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a2b9-105">Remarks</span></span>

<span data-ttu-id="9a2b9-106">Verwenden Sie **hstring** , um unveränderliche Zeichen folgen in der Windows-Runtime darzustellen.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-106">Use **HSTRING** to represent immutable strings in the Windows Runtime.</span></span>

<span data-ttu-id="9a2b9-107">In JavaScript und anderen Sprachen, wie z. b. C \# und Microsoft Visual Basic, können Zeichen folgen verwendet werden, die mithilfe von **hstring** dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-107">JavaScript and other languages, such as C\#, and Microsoft Visual Basic, can use strings that are represented by using **HSTRING**.</span></span> <span data-ttu-id="9a2b9-108">In der folgenden Tabelle wird gezeigt, wie ein **hstring** in anderen Sprachen dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-108">The following table shows how an **HSTRING** is represented in other languages.</span></span>



| <span data-ttu-id="9a2b9-109">Programmiersprache</span><span class="sxs-lookup"><span data-stu-id="9a2b9-109">Programming Language</span></span>                                                                    | <span data-ttu-id="9a2b9-110">Zeichen folgen Darstellung</span><span class="sxs-lookup"><span data-stu-id="9a2b9-110">String Representation</span></span>                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="9a2b9-111">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="9a2b9-111">C++/WinRT</span></span>](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | <span data-ttu-id="9a2b9-112">[WinRT:: hstring](/uwp/cpp-ref-for-winrt/hstring) -Klasse</span><span class="sxs-lookup"><span data-stu-id="9a2b9-112">[winrt::hstring](/uwp/cpp-ref-for-winrt/hstring) class</span></span>     |
| <span data-ttu-id="9a2b9-113">Komponenten Erweiterungen für Visual C++ ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx))</span><span class="sxs-lookup"><span data-stu-id="9a2b9-113">Visual C++ component extensions ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx))</span></span> | <span data-ttu-id="9a2b9-114">[Platform:: String](/cpp/cppcx/platform-string-class) -Klasse</span><span class="sxs-lookup"><span data-stu-id="9a2b9-114">[Platform::String](/cpp/cppcx/platform-string-class) class</span></span> |
| <span data-ttu-id="9a2b9-115">JavaScript</span><span class="sxs-lookup"><span data-stu-id="9a2b9-115">JavaScript</span></span>                                                                              | <span data-ttu-id="9a2b9-116">String-Objekt</span><span class="sxs-lookup"><span data-stu-id="9a2b9-116">String object</span></span>                                              |
| <span data-ttu-id="9a2b9-117">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="9a2b9-117">.NET Framework</span></span>                                                                          | <span data-ttu-id="9a2b9-118">System.String-Klasse</span><span class="sxs-lookup"><span data-stu-id="9a2b9-118">System.String class</span></span>                                        |



 

<span data-ttu-id="9a2b9-119">Das **hstring** -Handle ist ein Standard behandlertyp.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-119">The **HSTRING** handle is a standard handle type.</span></span> <span data-ttu-id="9a2b9-120">Semantisch stellt ein **hstring** , der den Wert **null** enthält, die leere Zeichenfolge dar, die aus keinem Inhalts Zeichen und einem abschließenden **null** -Zeichen besteht.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-120">Semantically, an **HSTRING** containing the value **NULL** represents the empty string, which consists of zero content characters and a terminating **NULL** character.</span></span> <span data-ttu-id="9a2b9-121">Das Erstellen einer Zeichenfolge über [**windowscreatestring**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) mit NULL Zeichen erzeugt den Handle-Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-121">Creating a string via [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) with zero characters will produce the handle value **NULL**.</span></span> <span data-ttu-id="9a2b9-122">Beim Aufrufen von [**windowsgetstringrawbuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) mit dem Wert **null** wird ein Zeiger auf eine leere Zeichenfolge zurückgegeben, auf die nur das Zeichen für das abschließende **NUL** -Zeichen folgt.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-122">When calling [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) with the value **NULL**, a pointer to an empty string followed only by the **NUL** terminating character will be returned.</span></span> <span data-ttu-id="9a2b9-123">Es gibt keinen eindeutigen Wert, der einen nicht initialisierten **hstring** darstellt.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-123">No distinct value exists to represent an **HSTRING** that is uninitialized.</span></span>

<span data-ttu-id="9a2b9-124">Rufen Sie die [**windowscreatestring**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) -Funktion auf, um einen neuen **hstring**-Code zu erstellen, und rufen Sie die [**windowsdeletestring**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) -Funktion auf, um den Verweis auf den Zeichen folgen Speicher für die</span><span class="sxs-lookup"><span data-stu-id="9a2b9-124">Call the [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) function to create a new **HSTRING**, and call the [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) function to release the reference to the backing string memory.</span></span> <span data-ttu-id="9a2b9-125">Rufen Sie die [**windowscreatestrauch ingreferenzierungsfunktion**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) auf, um einen Zeichen folgen Verweis zu erstellen. dieser wird auch als *fast-Pass-Zeichenfolge* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-125">Call the [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) function to create a string reference, which is also called a *fast-pass string*.</span></span>

<span data-ttu-id="9a2b9-126">Kopieren Sie ein **hstring-Zeichen** , indem Sie die [**windowsduplicatestring**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-126">Copy an **HSTRING** by calling the [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) function.</span></span>

<span data-ttu-id="9a2b9-127">Verkettet zwei Zeichen folgen durch Aufrufen der [**windowsconcatstring**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-127">Concatenate two strings by calling the [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) function.</span></span>

<span data-ttu-id="9a2b9-128">Greifen Sie über die [**windowsgetstringrawbuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) -Funktion auf den Speicher für die Unterstützungs Zeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-128">Access the backing string memory by calling the [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) function.</span></span>

<span data-ttu-id="9a2b9-129">**Hstring** kann eingebettete **NUL** -Zeichen speichern und verwenden.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-129">**HSTRING** can store and use embedded **NUL** characters.</span></span> <span data-ttu-id="9a2b9-130">Verwenden Sie die [**windowsstringhasembeddednull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) -Funktion, um vor der Verwendung von Funktionen, die möglicherweise unerwartete Ergebnisse verursachen, nach eingebetteten **NUL** -Zeichen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-130">Use the [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) function to check for embedded **NUL** characters before using any functions which may produce unexpected results.</span></span> <span data-ttu-id="9a2b9-131">Beispielsweise verwenden die meisten Windows-Funktionen **LPCWSTR** als Eingabeparameter und berechnen die Länge der Zeichenfolge nur, bis die erste **NUL** erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-131">For example, most of the Windows functions use **LPCWSTR** as an input parameter, and they compute the length of the string only until the first **NUL** is encountered.</span></span>

<span data-ttu-id="9a2b9-132">Die Unterstützungs Zeichenfolge muss unveränderlich und NULL-terminiert bleiben.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-132">The backing string must remain immutable and null-terminated.</span></span> <span data-ttu-id="9a2b9-133">Wenn der aufrufende Code einen Zeichen folgen Verweis mithilfe der [**windowscreatestrauferenferenzierungsfunktion**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) erstellt, befindet sich der Arbeitsspeicher, der die zugrunde liegende Zeichen folgen Darstellung enthält, dem Aufrufer.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-133">When calling code creates a string reference by using the [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) function, the memory containing the backing string representation is owned by the caller.</span></span> <span data-ttu-id="9a2b9-134">Der Windows-Runtime der den Inhalt der ursprünglichen Zeichenfolge verlässt, bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-134">The Windows Runtime relies on the contents of the original string to remain unchanged.</span></span> <span data-ttu-id="9a2b9-135">Wenn Sie einen Zeichen folgen Verweis an den Windows-Runtime übergeben, liegt es in der Verantwortung des Aufrufers sicherzustellen, dass sich der Inhalt der Zeichenfolge ändert und die **NUL** für die Dauer des Aufrufes beendet wird.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-135">When passing a string reference into the Windows Runtime, it is the caller’s responsibility to ensure that the string’s contents are unchanging and **NUL** terminated for the duration of the call.</span></span> <span data-ttu-id="9a2b9-136">Der Windows-Runtime gibt alle Verweise auf den Zeichen folgen Verweis frei, wenn der-Rückruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-136">The Windows Runtime releases all references to the string reference when the call returns.</span></span>

<span data-ttu-id="9a2b9-137">Wenn Sie ein **hstring** als out-Parameter erhalten, empfiehlt es sich, das Handle auf **null** festzulegen, wenn Sie damit fertig sind.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-137">When you receive an **HSTRING** as an out parameter, it is good practice to set the handle to **NULL** when you are finished with it.</span></span>

<span data-ttu-id="9a2b9-138">Rufen Sie die [**windowshalallocatestringbuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) -Funktion auf, um einen änderbaren Zeichen folgen Puffer zuzuweisen, den Sie zum Erstellen eines unveränderlichen **hstring** verwenden können.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-138">Call the [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) function to allocate a mutable string buffer that you can use to create an immutable **HSTRING**.</span></span> <span data-ttu-id="9a2b9-139">Wenn Sie das Auffüllen des Puffers abgeschlossen haben, rufen Sie die [**windowspromotestringbuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) -Funktion auf, um den **hstring** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-139">When you have finished populating the buffer, you call the [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) function to create the **HSTRING**.</span></span> <span data-ttu-id="9a2b9-140">Dieses zweistufige Konstruktionsmuster ermöglicht eine ähnliche Funktionalität wie ein "String Builder".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-140">This two-phase construction pattern enables functionality that is similar to a "string builder."</span></span>

## <a name="requirements"></a><span data-ttu-id="9a2b9-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a2b9-141">Requirements</span></span>



| <span data-ttu-id="9a2b9-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a2b9-142">Requirement</span></span> | <span data-ttu-id="9a2b9-143">Wert</span><span class="sxs-lookup"><span data-stu-id="9a2b9-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9a2b9-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a2b9-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9a2b9-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9a2b9-145">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="9a2b9-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a2b9-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9a2b9-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9a2b9-147">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="9a2b9-148">Header</span><span class="sxs-lookup"><span data-stu-id="9a2b9-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a2b9-149"><dt>Hstring. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a2b9-149"><dt>Hstring.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a2b9-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a2b9-150">See also</span></span>

<dl> <span data-ttu-id="9a2b9-151"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="9a2b9-151"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="9a2b9-152">**Windowscreatestring**</span><span class="sxs-lookup"><span data-stu-id="9a2b9-152">**WindowsCreateString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowscreatestring)
</dt> <dt>

[<span data-ttu-id="9a2b9-153">**Windowsdeletestring**</span><span class="sxs-lookup"><span data-stu-id="9a2b9-153">**WindowsDeleteString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowsdeletestring)
</dt> <dt>

[<span data-ttu-id="9a2b9-154">**Windowsduplicatestring**</span><span class="sxs-lookup"><span data-stu-id="9a2b9-154">**WindowsDuplicateString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)
</dt> <dt>

[<span data-ttu-id="9a2b9-155">**Windowshalzugecatestringbuffer**</span><span class="sxs-lookup"><span data-stu-id="9a2b9-155">**WindowsPreallocateStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> </dl>

 

 
