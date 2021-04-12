---
title: Direct2D-Fehler Behandlungsrichtlinien
description: In diesem Thema werden die Direct2D-Fehler Behandlungsrichtlinien beschrieben. Der Abschnitt ist wie folgt gegliedert.
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D, Fehlerbehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc930e7ee9e5b73b5f676103f45ffe25e4d4e61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949025"
---
# <a name="direct2d-error-handling-policies"></a><span data-ttu-id="bbb8d-105">Direct2D-Fehler Behandlungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="bbb8d-105">Direct2D Error Handling Policies</span></span>

<span data-ttu-id="bbb8d-106">In diesem Thema werden die Direct2D-Fehler Behandlungsrichtlinien beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-106">This topic describes the Direct2D error handling policies.</span></span> <span data-ttu-id="bbb8d-107">Der Abschnitt ist wie folgt gegliedert.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-107">It contains the following sections.</span></span>

-   [<span data-ttu-id="bbb8d-108">Verwendung von HRESULT</span><span class="sxs-lookup"><span data-stu-id="bbb8d-108">Use of HRESULT</span></span>](#use-of-hresult)
-   [<span data-ttu-id="bbb8d-109">Rückgabewert von Batch Funktionen</span><span class="sxs-lookup"><span data-stu-id="bbb8d-109">Return Value of Batched Functions</span></span>](#return-value-of-batched-functions)
-   [<span data-ttu-id="bbb8d-110">Ungültige Eingabe</span><span class="sxs-lookup"><span data-stu-id="bbb8d-110">Invalid Input</span></span>](#invalid-input)
    -   [<span data-ttu-id="bbb8d-111">Ausgabe Zeiger</span><span class="sxs-lookup"><span data-stu-id="bbb8d-111">Output Pointer</span></span>](#output-pointer)
    -   [<span data-ttu-id="bbb8d-112">Erforderlicher Parameter</span><span class="sxs-lookup"><span data-stu-id="bbb8d-112">Required Parameter</span></span>](#required-parameter)
-   [<span data-ttu-id="bbb8d-113">"NaN" und "schlecht geordnete Eingabe"</span><span class="sxs-lookup"><span data-stu-id="bbb8d-113">NaN and Poorly Ordered Input RECTs</span></span>](#nan-and-poorly-ordered-input-rects)
    -   [<span data-ttu-id="bbb8d-114">Nan als Eingabe</span><span class="sxs-lookup"><span data-stu-id="bbb8d-114">NaN as Input</span></span>](#nan-as-input)
    -   [<span data-ttu-id="bbb8d-115">Nicht ordnungs eine schlechte geordnete Eingabe</span><span class="sxs-lookup"><span data-stu-id="bbb8d-115">Poorly Ordered Input RECTs</span></span>](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a><span data-ttu-id="bbb8d-116">Verwendung von HRESULT</span><span class="sxs-lookup"><span data-stu-id="bbb8d-116">Use of HRESULT</span></span>

<span data-ttu-id="bbb8d-117">Wenn eine Funktion nicht in einem Batch verarbeitet wird und einen Laufzeitfehler verursachen kann, sollte **HRESULT** zurückgegeben werden, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-117">If a function is not batched and can have a run-time failure, it should return **HRESULT** to indicate a failure.</span></span> <span data-ttu-id="bbb8d-118">Bei einem Laufzeitfehler handelt es sich um einen Fehler, der zur Entwurfszeit nicht vermieden werden kann, z. b. nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-118">A run-time failure is any failure that cannot be avoided at design time, such as out of memory.</span></span>

## <a name="return-value-of-batched-functions"></a><span data-ttu-id="bbb8d-119">Rückgabewert von Batch Funktionen</span><span class="sxs-lookup"><span data-stu-id="bbb8d-119">Return Value of Batched Functions</span></span>

<span data-ttu-id="bbb8d-120">Batch Funktionen in Direct2D sind die Funktionen, die als einzelne Einheit verarbeitet werden, wenn [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-120">Batched functions in Direct2D are the functions that are processed as a single unit when [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) is called.</span></span> <span data-ttu-id="bbb8d-121">Dabei handelt es sich um die Zeichnungs Befehle zwischen [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) und **EndDraw** oder Befehlen in [**geometrysink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span><span class="sxs-lookup"><span data-stu-id="bbb8d-121">They are the drawing commands between [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and **EndDraw** or commands on [**GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span></span> <span data-ttu-id="bbb8d-122">Für diese Funktionen werden Fehler zu dem Zeitpunkt gemeldet, zu dem der Batch abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-122">For these functions, errors are reported at the time the batch is completed.</span></span> <span data-ttu-id="bbb8d-123">Der Fehler wird nach " **EndDraw** " für Zeichnungs Befehle und nach " **Close** " für " **geometrysink**" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-123">The error is returned after **EndDraw** for drawing commands, and after **Close** for **GeometrySink**.</span></span>

<span data-ttu-id="bbb8d-124">Rendertargets stoppt das Zeichnen, wenn ein Fehlerzustand festgelegt ist. eine Anwendung kann jedoch eine leeren [**aufzurufen,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) um den Fehlerzustand zurückzusetzen und das Zeichnen fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-124">RenderTargets stop drawing if an error state is set, but an application can call [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) to reset the error state and resume drawing.</span></span>

<span data-ttu-id="bbb8d-125">**Get** -und **set** -Funktionen haben keinen Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-125">**Get** and **Set** functions have no return value.</span></span> <span data-ttu-id="bbb8d-126">Wenn eine **Set** -Funktion jedoch über eine ungültige Eingabe verfügt, generiert die debugschicht eine Meldung.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-126">However, if a **Set** function has an invalid input, the debug layer generates a message.</span></span> <span data-ttu-id="bbb8d-127">In diesem Fall wird kein Fehlerzustand festgelegt, und die **Set** -Funktion führt keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-127">In this case, no error state is set and the **Set** function does nothing.</span></span>

## <a name="invalid-input"></a><span data-ttu-id="bbb8d-128">Ungültige Eingabe</span><span class="sxs-lookup"><span data-stu-id="bbb8d-128">Invalid Input</span></span>

<span data-ttu-id="bbb8d-129">Direct2D dereferenziert Ausgabe Zeiger und erforderliche Parameter, die zu Zugriffs Verstößen führen, wenn die Zeiger ungültig sind oder **null** sind.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-129">Direct2D dereferences output pointers and required parameters which result in access violations when the pointers are invalid or **NULL**.</span></span>

### <a name="output-pointer"></a><span data-ttu-id="bbb8d-130">Ausgabe Zeiger</span><span class="sxs-lookup"><span data-stu-id="bbb8d-130">Output Pointer</span></span>

<span data-ttu-id="bbb8d-131">Direct2D dereferenziert einen Ausgabe Zeiger und weist ihn sofort nach der Eingabe der Funktion **null** zu.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-131">Direct2D dereferences an output pointer and assigns it to **NULL** immediately upon entering the function.</span></span> <span data-ttu-id="bbb8d-132">Dies führt zu einer Zugriffsverletzung, wenn ein Aufrufer **null** als Zeiger auf den Rückgabewert übergibt.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-132">This causes an access violation if a caller passes in **NULL** as the pointer to the return value.</span></span> <span data-ttu-id="bbb8d-133">Diese Richtlinie gilt auch für Arrays von Zeigern.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-133">This policy also applies to arrays of pointers.</span></span> <span data-ttu-id="bbb8d-134">Bei anderen Ausgabeparametern, z. b. einer Struktur, erfolgt die Dereferenzierung später und führt ebenfalls zu einer Zugriffsverletzung.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-134">For other output parameters, such as a struct, the dereference happens later and also results in an access violation.</span></span> <span data-ttu-id="bbb8d-135">Es gibt jedoch einige Methoden mit optionalen Ausgabe Zeigern (d. h. [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)), die keine Zugriffsverletzung verursachen.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-135">However, there are some methods that have optional output pointers (that is, [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) that will not cause an access violation.</span></span>

### <a name="required-parameter"></a><span data-ttu-id="bbb8d-136">Erforderlicher Parameter</span><span class="sxs-lookup"><span data-stu-id="bbb8d-136">Required Parameter</span></span>

<span data-ttu-id="bbb8d-137">Wenn **null** an eine Funktion übermittelt wird, die einen gültigen Wert erfordert, dereferenziert die Funktion den ungültigen Zeiger frühzeitig und führt zu einer Zugriffsverletzung.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-137">If **NULL** is passed to any function requiring a valid value, the function dereferences the bad pointer early resulting in an access violation.</span></span> <span data-ttu-id="bbb8d-138">Bei optionalen Eingabe Parametern ist **null** ein gültiger Wert, der einen angemessenen Standardwert ergibt.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-138">For optional input parameters, **NULL** is a valid value that results in some reasonable default.</span></span>

## <a name="nan-and-poorly-ordered-input-rects"></a><span data-ttu-id="bbb8d-139">"NaN" und "schlecht geordnete Eingabe"</span><span class="sxs-lookup"><span data-stu-id="bbb8d-139">NaN and Poorly Ordered Input RECTs</span></span>

<span data-ttu-id="bbb8d-140">In Direct2D wird NaN als gültige Eingabe betrachtet, und eine nicht ordnungsgemäß geordnete Eingabe wird sortiert.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-140">In Direct2D, NaN is considered a valid input and poorly ordered input RECTs are sorted.</span></span>

### <a name="nan-as-input"></a><span data-ttu-id="bbb8d-141">Nan als Eingabe</span><span class="sxs-lookup"><span data-stu-id="bbb8d-141">NaN as Input</span></span>

<span data-ttu-id="bbb8d-142">NaN wird als gültige Eingabe betrachtet, obwohl es in der Regel zu der primitiven führt, die das Nan-Zeichen nicht zeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-142">NaN is considered a valid input, though it typically results in the primitive that contains the NaN not drawing.</span></span> <span data-ttu-id="bbb8d-143">Die Direct2D-API bietet keine explizite Filterung von Nan zum Validieren von Eingaben.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-143">The Direct2D API does not provide explicit filtering of NaN to validate input.</span></span>

### <a name="poorly-ordered-input-rects"></a><span data-ttu-id="bbb8d-144">Nicht ordnungs eine schlechte geordnete Eingabe</span><span class="sxs-lookup"><span data-stu-id="bbb8d-144">Poorly Ordered Input RECTs</span></span>

<span data-ttu-id="bbb8d-145">Nicht ordnungsgemäß sortierte Eingabe-rects werden so sortiert, dass die oberen, linken und unteren, rechten Ecken richtig angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-145">Poorly ordered input RECTs are sorted so that the top, left and bottom, right corners are correctly specified.</span></span> <span data-ttu-id="bbb8d-146">Bei der Ausgabe sehen leere Rechtecke wie folgt aus: {unendlich, unendlich, Floatmax, Floatmax}.</span><span class="sxs-lookup"><span data-stu-id="bbb8d-146">For output, empty rectangles look like this: {Infinity, Infinity, FloatMax, FloatMax}.</span></span>

 

 