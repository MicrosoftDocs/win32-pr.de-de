---
title: Regeln für die Verwendung von Zeigern
description: Das Portieren von Code für die Kompilierung von Microsoft Windows 32-und 64-Bit ist unkompliziert. Sie müssen nur einige einfache Regeln zum Umwandeln von Zeigern befolgen und die neuen Datentypen in Ihrem Code verwenden. Die Regeln für die Zeiger Bearbeitung lauten wie folgt.
ms.assetid: 4c38bee2-fa1c-493f-a12d-e673df4d4895
keywords:
- Regeln für die Verwendung von Zeigern 64-Bit-Windows-Programmierung
- Zeiger Manipulation 64-Bit-Windows-Programmierung
- Umwandeln von Zeigern 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318ff5beed6dc90bd49b6b293131e17db6f92f6b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103949185"
---
# <a name="rules-for-using-pointers"></a><span data-ttu-id="3bad2-108">Regeln für die Verwendung von Zeigern</span><span class="sxs-lookup"><span data-stu-id="3bad2-108">Rules for Using Pointers</span></span>

<span data-ttu-id="3bad2-109">Das Portieren von Code für die Kompilierung von Microsoft Windows 32-und 64-Bit ist unkompliziert.</span><span class="sxs-lookup"><span data-stu-id="3bad2-109">Porting your code to compile for both 32- and 64-bit Microsoft Windows is straightforward.</span></span> <span data-ttu-id="3bad2-110">Sie müssen nur einige einfache Regeln zum Umwandeln von Zeigern befolgen und die neuen Datentypen in Ihrem Code verwenden.</span><span class="sxs-lookup"><span data-stu-id="3bad2-110">You need only follow a few simple rules about casting pointers, and use the new data types in your code.</span></span> <span data-ttu-id="3bad2-111">Die Regeln für die Zeiger Bearbeitung lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="3bad2-111">The rules for pointer manipulation are as follows.</span></span>

1.  <span data-ttu-id="3bad2-112">Verwenden Sie keine Zeiger in **int**, **Long**, **ulong** oder **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="3bad2-112">Do not cast pointers to **int**, **long**, **ULONG**, or **DWORD**.</span></span>

    <span data-ttu-id="3bad2-113">Wenn Sie einen Zeiger umwandeln müssen, um einige Bits zu testen, Bits festzulegen oder zu löschen oder den Inhalt anderweitig zu bearbeiten, verwenden Sie den **uint- \_ ptr** -oder den **int- \_ ptr** -Typ.</span><span class="sxs-lookup"><span data-stu-id="3bad2-113">If you must cast a pointer to test some bits, set or clear bits, or otherwise manipulate its contents, use the **UINT\_PTR** or **INT\_PTR** type.</span></span> <span data-ttu-id="3bad2-114">Bei diesen Typen handelt es sich um ganzzahlige Typen, die auf die Größe eines Zeigers für 32-und 64-Bit-Fenster skaliert werden (z. b. **ulong** für 32-Bit-Windows und \_ Int64 für 64-Bit-Windows).</span><span class="sxs-lookup"><span data-stu-id="3bad2-114">These types are integral types that scale to the size of a pointer for both 32- and 64-bit Windows (for example, **ULONG** for 32-bit Windows and \_int64 for 64-bit Windows).</span></span> <span data-ttu-id="3bad2-115">Nehmen Sie beispielsweise an, dass Sie den folgenden Code portieren:</span><span class="sxs-lookup"><span data-stu-id="3bad2-115">For example, assume you are porting the following code:</span></span>

    `ImageBase = (PVOID)((ULONG)ImageBase | 1);`

    <span data-ttu-id="3bad2-116">Im Rahmen des Portierungs Prozesses ändern Sie den Code wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3bad2-116">As a part of the porting process, you would change the code as follows:</span></span>

    `ImageBase = (PVOID)((ULONG_PTR)ImageBase | 1);`

    <span data-ttu-id="3bad2-117">Verwenden Sie ggf. **uint \_ ptr** und **int \_ ptr** (und wenn Sie unsicher sind, ob Sie erforderlich sind, gibt es keinen Schaden bei der Verwendung in der Groß-/Kleinschreibung).</span><span class="sxs-lookup"><span data-stu-id="3bad2-117">Use **UINT\_PTR** and **INT\_PTR** where appropriate (and if you are uncertain whether they are required, there is no harm in using them just in case).</span></span> <span data-ttu-id="3bad2-118">Wandeln Sie Ihre Zeiger nicht in die Typen **ulong**, **Long**, **int**, **uint** oder **DWORD** um.</span><span class="sxs-lookup"><span data-stu-id="3bad2-118">Do not cast your pointers to the types **ULONG**, **LONG**, **INT**, **UINT**, or **DWORD**.</span></span>

    <span data-ttu-id="3bad2-119">Beachten Sie, dass **handle** als **void \*** definiert ist, sodass ein **handle** -Wert für einen **ulong** -Wert zum Testen, festlegen oder Löschen der niedrig wertigen 2 Bits in 64-Bit-Fenstern ein Fehler ist.</span><span class="sxs-lookup"><span data-stu-id="3bad2-119">Note that **HANDLE** is defined as a **void\***, so typecasting a **HANDLE** value to a **ULONG** value to test, set, or clear the low-order 2 bits is an error on 64-bit Windows.</span></span>

2.  <span data-ttu-id="3bad2-120">Verwenden Sie die **ptrtolong** -oder **ptrtoulong** -Funktion, um Zeiger zu kürzen.</span><span class="sxs-lookup"><span data-stu-id="3bad2-120">Use the **PtrToLong** or **PtrToUlong** function to truncate pointers.</span></span>

    <span data-ttu-id="3bad2-121">Wenn Sie einen Zeiger auf einen 32-Bit-Wert kürzen müssen, verwenden Sie die **ptrtolong** -oder **ptrtoulong** -Funktion (in basetsd. h definiert).</span><span class="sxs-lookup"><span data-stu-id="3bad2-121">If you must truncate a pointer to a 32-bit value, use the **PtrToLong** or **PtrToUlong** function (defined in Basetsd.h).</span></span> <span data-ttu-id="3bad2-122">Diese Funktionen deaktivieren die zeigertrunzierungswarnung für die Dauer des Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="3bad2-122">These functions disable the pointer truncation warning for the duration of the call.</span></span>

    <span data-ttu-id="3bad2-123">Verwenden Sie diese Funktionen sorgfältig.</span><span class="sxs-lookup"><span data-stu-id="3bad2-123">Use these functions carefully.</span></span> <span data-ttu-id="3bad2-124">Nachdem Sie eine Zeiger Variable mithilfe einer dieser Funktionen konvertiert haben, verwenden Sie Sie nie erneut als Zeiger.</span><span class="sxs-lookup"><span data-stu-id="3bad2-124">After you convert a pointer variable using one of these functions, never use it as a pointer again.</span></span> <span data-ttu-id="3bad2-125">Diese Funktionen kürzen die oberen 32 Bits einer Adresse, die normalerweise benötigt werden, um auf den Speicher zuzugreifen, auf den ursprünglich durch Zeiger verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3bad2-125">These functions truncate the upper 32 bits of an address, which are usually needed to access the memory originally referenced by pointer.</span></span> <span data-ttu-id="3bad2-126">Wenn Sie diese Funktionen ohne sorgfältige Überlegung verwenden, führt dies zu zerbrechlichem Code.</span><span class="sxs-lookup"><span data-stu-id="3bad2-126">Using these functions without careful consideration will result in fragile code.</span></span>

3.  <span data-ttu-id="3bad2-127">Seien Sie vorsichtig, wenn Sie Zeiger \_ 32-Werte in Code verwenden, die als 64-Bit-Code kompiliert werden können.</span><span class="sxs-lookup"><span data-stu-id="3bad2-127">Be careful when using POINTER\_32 values in code that may be compiled as 64-bit code.</span></span> <span data-ttu-id="3bad2-128">Der Compiler signiert den Zeiger, wenn er einem systemeigenen Zeiger im 64-Bit-Code zugewiesen wird, und nicht mit 0 (null).</span><span class="sxs-lookup"><span data-stu-id="3bad2-128">The compiler will sign-extend the pointer when it is assigned to a native pointer in 64-bit code, not zero-extend the pointer.</span></span>
4.  <span data-ttu-id="3bad2-129">Seien Sie vorsichtig, wenn Sie Zeiger \_ 64-Werte in Code verwenden, die als 32-Bit-Code kompiliert werden können.</span><span class="sxs-lookup"><span data-stu-id="3bad2-129">Be careful when using POINTER\_64 values in code that may be compiled as 32-bit code.</span></span> <span data-ttu-id="3bad2-130">Der Compiler signiert den Zeiger im 32-Bit-Code und erweitert den Zeiger nicht mit NULL.</span><span class="sxs-lookup"><span data-stu-id="3bad2-130">The compiler will sign-extend the pointer in 32-bit code, not zero-extend the pointer.</span></span>
5.  <span data-ttu-id="3bad2-131">Achten Sie darauf, out-Parameter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3bad2-131">Be careful using OUT parameters.</span></span>

    <span data-ttu-id="3bad2-132">Angenommen, Sie haben eine Funktion wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="3bad2-132">For example, suppose you have a function defined as follows:</span></span>

    `void func( OUT PULONG *PointerToUlong );`

    <span data-ttu-id="3bad2-133">Diese Funktion kann nicht wie folgt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3bad2-133">Do not call this function as follows.</span></span>

    ``` syntax
    ULONG ul;
    PULONG lp;
    func((PULONG *)&ul);
    lp = (PULONG)ul;
    ```

    <span data-ttu-id="3bad2-134">Verwenden Sie stattdessen den folgenden-Befehl.</span><span class="sxs-lookup"><span data-stu-id="3bad2-134">Instead, use the following call.</span></span>

    ``` syntax
    PULONG lp;
    func(&lp);
    ```

    <span data-ttu-id="3bad2-135">Typecasting &UL auf **Pulong \*** verhindert einen Compilerfehler, aber die Funktion schreibt einen 64-Bit-Zeiger Wert in den Arbeitsspeicher &UL.</span><span class="sxs-lookup"><span data-stu-id="3bad2-135">Typecasting &ul to **PULONG\*** prevents a compiler error, but the function will write a 64-bit pointer value into the memory at &ul.</span></span> <span data-ttu-id="3bad2-136">Dieser Code funktioniert auf 32-Bit-Fenstern, führt jedoch zu Daten Beschädigungen auf 64-Bit-Fenstern und ist eine feine, schwer zu suchende Beschädigung.</span><span class="sxs-lookup"><span data-stu-id="3bad2-136">This code works on 32-bit Windows, but will cause data corruption on 64-bit Windows and it will be subtle, hard-to-find corruption.</span></span> <span data-ttu-id="3bad2-137">In der untersten Zeile: spielen Sie keine Tricks mit dem C-Code. – unkompliziert und einfach ist besser.</span><span class="sxs-lookup"><span data-stu-id="3bad2-137">The bottom line: Do not play tricks with the C code—straightforward and simple is better.</span></span>

6.  <span data-ttu-id="3bad2-138">Seien Sie vorsichtig mit polymorphen Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="3bad2-138">Be careful with polymorphic interfaces.</span></span>

    <span data-ttu-id="3bad2-139">Erstellen Sie keine Funktionen, die **DWORD** -Parameter für polymorphe Daten akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="3bad2-139">Do not create functions that accept **DWORD** parameters for polymorphic data.</span></span> <span data-ttu-id="3bad2-140">Wenn die Daten ein Zeiger oder ein ganzzahliger Wert sein können, verwenden Sie den uint- \_ Typ PTR oder **pVoid** .</span><span class="sxs-lookup"><span data-stu-id="3bad2-140">If the data can be a pointer or an integral value, use the UINT\_PTR or **PVOID** type.</span></span>

    <span data-ttu-id="3bad2-141">Erstellen Sie z. b. keine Funktion, die ein Array von Ausnahme Parametern akzeptiert, die als **DWORD** -Werte typisiert sind.</span><span class="sxs-lookup"><span data-stu-id="3bad2-141">For example, do not create a function that accepts an array of exception parameters typed as **DWORD** values.</span></span> <span data-ttu-id="3bad2-142">Das Array muss ein Array von **DWORD- \_ ptr** -Werten sein.</span><span class="sxs-lookup"><span data-stu-id="3bad2-142">The array should be an array of **DWORD\_PTR** values.</span></span> <span data-ttu-id="3bad2-143">Daher können die Array Elemente Adressen oder ganzzahlige 32-Bit-Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="3bad2-143">Therefore, the array elements can hold addresses or 32-bit integral values.</span></span> <span data-ttu-id="3bad2-144">(Die allgemeine Regel ist, dass, wenn der ursprüngliche Typ **DWORD** ist und es sich um eine Zeiger Breite handeln muss, in einen **DWORD- \_ ptr** -Wert konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="3bad2-144">(The general rule is that if the original type is **DWORD** and it needs to be pointer width, convert it to a **DWORD\_PTR** value.</span></span> <span data-ttu-id="3bad2-145">Daher gibt es entsprechende Typen von Zeiger Genauigkeit.) Wenn Sie über Code verfügen, der **DWORD**-, **ulong**-oder andere 32-Bit-Typen in polymorph-Weise verwendet (d. h., Sie möchten, dass der Parameter oder der Strukturmember eine Adresse enthält), verwenden Sie **uint \_ ptr** anstelle des aktuellen Typs.</span><span class="sxs-lookup"><span data-stu-id="3bad2-145">That is why there are corresponding pointer-precision types.) If you have code that uses **DWORD**, **ULONG**, or other 32-bit types in a polymorphic way (that is, you really want the parameter or structure member to hold an address), use **UINT\_PTR** in place of the current type.</span></span>

7.  <span data-ttu-id="3bad2-146">Verwenden Sie die neuen Fenster Klassen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="3bad2-146">Use the new window class functions.</span></span>

    <span data-ttu-id="3bad2-147">Wenn Sie über private Fenster-oder Klassen Daten verfügen, die Zeiger enthalten, muss der Code die folgenden neuen Funktionen verwenden:</span><span class="sxs-lookup"><span data-stu-id="3bad2-147">If you have window or class private data that contains pointers, your code will need to use the following new functions:</span></span>

    -   [<span data-ttu-id="3bad2-148">**Getclasslongptr**</span><span class="sxs-lookup"><span data-stu-id="3bad2-148">**GetClassLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getclasslongptra)
    -   [<span data-ttu-id="3bad2-149">**Getwindowlongptr**</span><span class="sxs-lookup"><span data-stu-id="3bad2-149">**GetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
    -   [<span data-ttu-id="3bad2-150">**Setclasslongptr**</span><span class="sxs-lookup"><span data-stu-id="3bad2-150">**SetClassLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-setclasslongptra)
    -   [<span data-ttu-id="3bad2-151">**Setwindowlongptr**</span><span class="sxs-lookup"><span data-stu-id="3bad2-151">**SetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)

    <span data-ttu-id="3bad2-152">Diese Funktionen können in 32-und 64-Bit-Fenstern verwendet werden, sind jedoch auf 64-Bit-Windows erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3bad2-152">These functions can be used on both 32- and 64-bit Windows, but they are required on 64-bit Windows.</span></span> <span data-ttu-id="3bad2-153">Bereiten Sie sich auf den Übergang vor, indem Sie diese Funktionen jetzt verwenden.</span><span class="sxs-lookup"><span data-stu-id="3bad2-153">Prepare for the transition by using these functions now.</span></span>

    <span data-ttu-id="3bad2-154">Außerdem müssen Sie auf Zeiger oder Handles in der Klasse private Daten zugreifen, indem Sie die neuen Funktionen auf 64-Bit-Windows verwenden.</span><span class="sxs-lookup"><span data-stu-id="3bad2-154">Additionally, you must access pointers or handles in class private data using the new functions on 64-bit Windows.</span></span> <span data-ttu-id="3bad2-155">Die folgenden Indizes werden bei einer 64-Bit-Kompilierung nicht in winuser. h definiert, um Sie bei der Suche nach diesen Fällen zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="3bad2-155">To aid you in finding these cases, the following indexes are not defined in Winuser.h during a 64-bit compile:</span></span>

    -   <span data-ttu-id="3bad2-156">GWL \_ WndProc</span><span class="sxs-lookup"><span data-stu-id="3bad2-156">GWL\_WNDPROC</span></span>
    -   <span data-ttu-id="3bad2-157">GWL- \_ HINSTANCE</span><span class="sxs-lookup"><span data-stu-id="3bad2-157">GWL\_HINSTANCE</span></span>
    -   <span data-ttu-id="3bad2-158">GWL \_ hwdparent</span><span class="sxs-lookup"><span data-stu-id="3bad2-158">GWL\_HWDPARENT</span></span>
    -   <span data-ttu-id="3bad2-159">GWL \_ User Data</span><span class="sxs-lookup"><span data-stu-id="3bad2-159">GWL\_USERDATA</span></span>

    <span data-ttu-id="3bad2-160">Stattdessen definiert Winuser. h die folgenden neuen Indizes:</span><span class="sxs-lookup"><span data-stu-id="3bad2-160">Instead, Winuser.h defines the following new indexes:</span></span>

    -   <span data-ttu-id="3bad2-161">gwlp \_ WndProc</span><span class="sxs-lookup"><span data-stu-id="3bad2-161">GWLP\_WNDPROC</span></span>
    -   <span data-ttu-id="3bad2-162">gwlp \_ HINSTANCE</span><span class="sxs-lookup"><span data-stu-id="3bad2-162">GWLP\_HINSTANCE</span></span>
    -   <span data-ttu-id="3bad2-163">gwlp \_ hwndParent</span><span class="sxs-lookup"><span data-stu-id="3bad2-163">GWLP\_HWNDPARENT</span></span>
    -   <span data-ttu-id="3bad2-164">gwlp \_ UserData</span><span class="sxs-lookup"><span data-stu-id="3bad2-164">GWLP\_USERDATA</span></span>
    -   <span data-ttu-id="3bad2-165">gwlp- \_ ID</span><span class="sxs-lookup"><span data-stu-id="3bad2-165">GWLP\_ID</span></span>

    <span data-ttu-id="3bad2-166">Der folgende Code wird z. b. nicht kompiliert:</span><span class="sxs-lookup"><span data-stu-id="3bad2-166">For example, the following code does not compile:</span></span>

    `SetWindowLong(hWnd, GWL_WNDPROC, (LONG)MyWndProc);`

    <span data-ttu-id="3bad2-167">Er sollte wie folgt geändert werden:</span><span class="sxs-lookup"><span data-stu-id="3bad2-167">It should be changed as follows:</span></span>

    `SetWindowLongPtr(hWnd, GWLP_WNDPROC, (LONG_PTR)MyWndProc);`

    <span data-ttu-id="3bad2-168">Wenn Sie das **CbWndExtra** -Element der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur festlegen, stellen Sie sicher, dass genügend Speicherplatz für Zeiger reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="3bad2-168">When setting the **cbWndExtra** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure, be sure to reserve enough space for pointers.</span></span> <span data-ttu-id="3bad2-169">Wenn Sie z. b. gerade sizeof-bytes (DWORD) für einen Zeiger Wert reservieren, reservieren Sie sizeof-bytes (DWORD \_ PTR).</span><span class="sxs-lookup"><span data-stu-id="3bad2-169">For example, if you are currently reserving sizeof(DWORD) bytes for a pointer value, reserve sizeof(DWORD\_PTR) bytes.</span></span>

8.  <span data-ttu-id="3bad2-170">Greifen Sie mit dem **Feld \_ Offset** auf alle Fenster-und Klassen Daten zu.</span><span class="sxs-lookup"><span data-stu-id="3bad2-170">Access all window and class data using **FIELD\_OFFSET**.</span></span>

    <span data-ttu-id="3bad2-171">Es ist üblich, mithilfe von hart codierten Offsets auf Fenster Daten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="3bad2-171">It is common to access window data using hard-coded offsets.</span></span> <span data-ttu-id="3bad2-172">Dieses Verfahren ist nicht für 64-Bit-Windows-Anwendungen portabel.</span><span class="sxs-lookup"><span data-stu-id="3bad2-172">This technique is not portable to 64-bit Windows.</span></span> <span data-ttu-id="3bad2-173">Um Ihren Code portabel zu machen, greifen Sie mit dem **Field \_ Offset** -Makro auf die Fenster-und Klassen Daten zu.</span><span class="sxs-lookup"><span data-stu-id="3bad2-173">To make your code portable, access your window and class data using the **FIELD\_OFFSET** macro.</span></span> <span data-ttu-id="3bad2-174">Gehen Sie nicht davon aus, dass der zweite Zeiger einen Offset von 4 aufweist.</span><span class="sxs-lookup"><span data-stu-id="3bad2-174">Do not assume that the second pointer has an offset of 4.</span></span>

9.  <span data-ttu-id="3bad2-175">Der **LPARAM**-, der **wParam**-und der **LRESULT** -Typ ändern die Größe mit der-Plattform.</span><span class="sxs-lookup"><span data-stu-id="3bad2-175">The **LPARAM**, **WPARAM**, and **LRESULT** types change size with the platform.</span></span>

    <span data-ttu-id="3bad2-176">Beim Kompilieren von 64-Bit-Code werden diese Typen auf 64 Bits erweitert, da Sie in der Regel Zeiger oder ganzzahlige Typen enthalten.</span><span class="sxs-lookup"><span data-stu-id="3bad2-176">When compiling 64-bit code, these types expand to 64 bits, because they typically hold pointers or integral types.</span></span> <span data-ttu-id="3bad2-177">Mischen Sie diese Werte nicht mit den Werten **DWORD**, **ulong**, **uint**, **int**, **int** oder **Long** .</span><span class="sxs-lookup"><span data-stu-id="3bad2-177">Do not mix these values with **DWORD**, **ULONG**, **UINT**, **INT**, **int**, or **long** values.</span></span> <span data-ttu-id="3bad2-178">Überprüfen Sie, wie Sie diese Typen verwenden, und stellen Sie sicher, dass Sie die Werte nicht versehentlich abschneiden.</span><span class="sxs-lookup"><span data-stu-id="3bad2-178">Examine how you use these types and ensure that you do not inadvertently truncate values.</span></span>

 

 