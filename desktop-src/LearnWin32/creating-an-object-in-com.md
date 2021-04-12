---
title: Erstellen eines Objekts in com
description: Um eine COM-Schnittstelle zu verwenden, erstellt das Programm zuerst eine Instanz eines Objekts, das diese Schnittstelle implementiert.
ms.assetid: 75f2115d-d49d-4e4e-8f99-67a231559ba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f96e4d9c2afbac028bfcefffcec6a070c78c8b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390227"
---
# <a name="creating-an-object-in-com"></a><span data-ttu-id="2c378-103">Erstellen eines Objekts in com</span><span class="sxs-lookup"><span data-stu-id="2c378-103">Creating an Object in COM</span></span>

<span data-ttu-id="2c378-104">Nachdem ein Thread die com-Bibliothek initialisiert hat, ist es sicher, dass der Thread com-Schnittstellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c378-104">After a thread has initialized the COM library, it is safe for the thread to use COM interfaces.</span></span> <span data-ttu-id="2c378-105">Um eine COM-Schnittstelle zu verwenden, erstellt das Programm zuerst eine Instanz eines Objekts, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="2c378-105">To use a COM interface, your program first creates an instance of an object that implements that interface.</span></span>

<span data-ttu-id="2c378-106">Im Allgemeinen gibt es zwei Möglichkeiten, ein COM-Objekt zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="2c378-106">In general, there are two ways to create a COM object:</span></span>

-   <span data-ttu-id="2c378-107">Das Modul, das das Objekt implementiert, kann möglicherweise eine Funktion bereitstellen, die speziell zum Erstellen von Instanzen dieses Objekts entworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="2c378-107">The module that implements the object might provide a function specifically designed to create instances of that object.</span></span>
-   <span data-ttu-id="2c378-108">Alternativ bietet com eine generische Erstellungs Funktion mit dem Namen [**cokreatabstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="2c378-108">Alternatively, COM provides a generic creation function named [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="2c378-109">Nehmen Sie z. b. das hypothetische `Shape` Objekt aus dem Thema [Was ist eine COM-Schnittstelle?](what-is-a-com-interface-.md).</span><span class="sxs-lookup"><span data-stu-id="2c378-109">For example, take the hypothetical `Shape` object from the topic [What Is a COM Interface?](what-is-a-com-interface-.md).</span></span> <span data-ttu-id="2c378-110">In diesem Beispiel implementiert das- `Shape` Objekt eine-Schnittstelle mit dem Namen `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="2c378-110">In that example, the `Shape` object implements an interface named `IDrawable`.</span></span> <span data-ttu-id="2c378-111">Die Grafikbibliothek, die das `Shape` Objekt implementiert, könnte eine Funktion mit der folgenden Signatur exportieren.</span><span class="sxs-lookup"><span data-stu-id="2c378-111">The graphics library that implements the `Shape` object might export a function with the following signature.</span></span>


```C++
// Not an actual Windows function. 

HRESULT CreateShape(IDrawable** ppShape);
```



<span data-ttu-id="2c378-112">Mit dieser Funktion können Sie wie folgt ein neues- `Shape` Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="2c378-112">Given this function, you could create a new `Shape` object as follows.</span></span>


```C++
IDrawable *pShape;

HRESULT hr = CreateShape(&pShape);
if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



<span data-ttu-id="2c378-113">Der *ppshape* -Parameter ist vom Typ "Pointer-to-Pointer-to-" `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="2c378-113">The *ppShape* parameter is of type pointer-to-pointer-to-`IDrawable`.</span></span> <span data-ttu-id="2c378-114">Wenn Sie dieses Muster noch nicht gesehen haben, kann die doppelte Dereferenzierung verwirrend sein.</span><span class="sxs-lookup"><span data-stu-id="2c378-114">If you have not seen this pattern before, the double indirection might be puzzling.</span></span>

<span data-ttu-id="2c378-115">Beachten Sie die Anforderungen der- `CreateShape` Funktion.</span><span class="sxs-lookup"><span data-stu-id="2c378-115">Consider the requirements of the `CreateShape` function.</span></span> <span data-ttu-id="2c378-116">Die Funktion muss einen `IDrawable` Zeiger an den Aufrufer zurücksenden.</span><span class="sxs-lookup"><span data-stu-id="2c378-116">The function must give an `IDrawable` pointer back to the caller.</span></span> <span data-ttu-id="2c378-117">Der Rückgabewert der Funktion wird jedoch bereits für den Fehler-/Erfolgscode verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c378-117">But the function's return value is already used for the error/success code.</span></span> <span data-ttu-id="2c378-118">Daher muss der-Zeiger durch ein Argument für die-Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2c378-118">Therefore, the pointer must be returned through an argument to the function.</span></span> <span data-ttu-id="2c378-119">Der Aufrufer übergibt eine Variable vom Typ `IDrawable*` an die Funktion, und die Funktion überschreibt diese Variable mit einem neuen `IDrawable` Zeiger.</span><span class="sxs-lookup"><span data-stu-id="2c378-119">The caller will pass a variable of type `IDrawable*` to the function, and the function will overwrite this variable with a new `IDrawable` pointer.</span></span> <span data-ttu-id="2c378-120">In C++ gibt es nur zwei Möglichkeiten, wie eine Funktion einen Parameterwert überschreiben kann: "Pass-by-Reference" oder "Pass by address".</span><span class="sxs-lookup"><span data-stu-id="2c378-120">In C++, there are only two ways for a function to overwrite a parameter value: pass by reference, or pass by address.</span></span> <span data-ttu-id="2c378-121">COM verwendet die letztgenannte Pass-by-address.</span><span class="sxs-lookup"><span data-stu-id="2c378-121">COM uses the latter, pass-by-address.</span></span> <span data-ttu-id="2c378-122">Und die Adresse eines Zeigers ist ein Zeiger auf einen Zeiger, daher muss der Parametertyp sein `IDrawable**` .</span><span class="sxs-lookup"><span data-stu-id="2c378-122">And the address of a pointer is a pointer-to-a-pointer, so the parameter type must be `IDrawable**`.</span></span>

<span data-ttu-id="2c378-123">Im folgenden finden Sie ein Diagramm, mit dem Sie visualisieren können, was passiert.</span><span class="sxs-lookup"><span data-stu-id="2c378-123">Here is a diagram to help visualize what's going on.</span></span>

![Diagramm, das die doppelte Zeiger Dereferenzierung anzeigt](images/com03.png)

<span data-ttu-id="2c378-125">Die- `CreateShape` Funktion verwendet die Adresse von *pshape* ( `&pShape` ), um einen neuen Zeiger Wert in *pshape* zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="2c378-125">The `CreateShape` function uses the address of *pShape* (`&pShape`) to write a new pointer value to *pShape*.</span></span>

## <a name="cocreateinstance-a-generic-way-to-create-objects"></a><span data-ttu-id="2c378-126">Cokreatanstance: eine generische Methode zum Erstellen von Objekten</span><span class="sxs-lookup"><span data-stu-id="2c378-126">CoCreateInstance: A Generic Way to Create Objects</span></span>

<span data-ttu-id="2c378-127">Die [**cokreateinzustance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion stellt einen generischen Mechanismus zum Erstellen von-Objekten bereit.</span><span class="sxs-lookup"><span data-stu-id="2c378-127">The [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function provides a generic mechanism for creating objects.</span></span> <span data-ttu-id="2c378-128">Beachten Sie, dass zwei COM-Objekte die gleiche Schnittstelle implementieren können und ein Objekt zwei oder mehr Schnittstellen implementieren kann, um **cokreateinstance** nachzuvollziehen.</span><span class="sxs-lookup"><span data-stu-id="2c378-128">To understand **CoCreateInstance**, keep in mind that two COM objects can implement the same interface, and one object can implement two or more interfaces.</span></span> <span data-ttu-id="2c378-129">Daher benötigt eine generische Funktion, die-Objekte erstellt, zwei Informationen.</span><span class="sxs-lookup"><span data-stu-id="2c378-129">Thus, a generic function that creates objects needs two pieces of information.</span></span>

-   <span data-ttu-id="2c378-130">Welches Objekt erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c378-130">Which object to create.</span></span>
-   <span data-ttu-id="2c378-131">Die Schnittstelle, die vom-Objekt abgeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c378-131">Which interface to get from the object.</span></span>

<span data-ttu-id="2c378-132">Aber wie geben wir diese Informationen an, wenn wir die Funktion bezeichnen?</span><span class="sxs-lookup"><span data-stu-id="2c378-132">But how do we indicate this information when we call the function?</span></span> <span data-ttu-id="2c378-133">In com wird ein Objekt oder eine Schnittstelle durch Zuweisen einer 128-Bit-Nummer identifiziert, die als *Globally Unique Identifier* (GUID) bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="2c378-133">In COM, an object or an interface is identified by assigning it a 128-bit number, called a *globally unique identifier* (GUID).</span></span> <span data-ttu-id="2c378-134">GUIDs werden auf eine Weise generiert, die Sie effektiv eindeutig macht.</span><span class="sxs-lookup"><span data-stu-id="2c378-134">GUIDs are generated in a way that makes them effectively unique.</span></span> <span data-ttu-id="2c378-135">GUIDs stellen eine Lösung für das Problem dar, wie eindeutige Bezeichner ohne zentrale Registrierungsstelle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2c378-135">GUIDs are a solution to the problem of how to create unique identifiers without a central registration authority.</span></span> <span data-ttu-id="2c378-136">GUIDs werden manchmal als *universell eindeutige* Bezeichner (UUIDs) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2c378-136">GUIDs are sometimes called *universally unique identifiers* (UUIDs).</span></span> <span data-ttu-id="2c378-137">Vor com wurden Sie in DCE/RPC verwendet (verteilte Computerumgebung/Remote Prozedur Aufruf).</span><span class="sxs-lookup"><span data-stu-id="2c378-137">Prior to COM, they were used in DCE/RPC (Distributed Computing Environment/Remote Procedure Call).</span></span> <span data-ttu-id="2c378-138">Zum Erstellen neuer GUIDs sind mehrere Algorithmen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2c378-138">Several algorithms exist for creating new GUIDs.</span></span> <span data-ttu-id="2c378-139">Nicht alle diese Algorithmen garantieren die Eindeutigkeit streng, aber die Wahrscheinlichkeit, dass der gleiche GUID-Wert zweimal erstellt wird, ist extrem klein – effektiv 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2c378-139">Not all of these algorithms strictly guarantee uniqueness, but the probability of accidentally creating the same GUID value twice is extremely small—effectively zero.</span></span> <span data-ttu-id="2c378-140">GUIDs können verwendet werden, um jede Art von Entität zu identifizieren, nicht nur Objekte und Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="2c378-140">GUIDs can be used to identify any sort of entity, not just objects and interfaces.</span></span> <span data-ttu-id="2c378-141">Dies ist jedoch die einzige Verwendung, die uns in diesem Modul betrifft.</span><span class="sxs-lookup"><span data-stu-id="2c378-141">However, that is the only use that concerns us in this module.</span></span>

<span data-ttu-id="2c378-142">Beispielsweise kann die `Shapes` Bibliothek zwei GUID-Konstanten deklarieren:</span><span class="sxs-lookup"><span data-stu-id="2c378-142">For example, the `Shapes` library might declare two GUID constants:</span></span>


```C++
extern const GUID CLSID_Shape;
extern const GUID IID_IDrawable; 
```



<span data-ttu-id="2c378-143">(Sie können davon ausgehen, dass die tatsächlichen numerischen 128-Bit-Werte für diese Konstanten an anderer Stelle definiert sind.) Die Konstante **CLSID- \_ Form** identifiziert das `Shape` Objekt, während die Konstante **IID \_ idrawable** die `IDrawable` Schnittstelle identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2c378-143">(You can assume that the actual 128-bit numeric values for these constants are defined elsewhere.) The constant **CLSID\_Shape** identifies the `Shape` object, while the constant **IID\_IDrawable** identifies the `IDrawable` interface.</span></span> <span data-ttu-id="2c378-144">Das Präfix "CLSID" steht für den *Klassen Bezeichner*, und die Präfix- *IID* steht für den *Schnittstellen Bezeichner*.</span><span class="sxs-lookup"><span data-stu-id="2c378-144">The prefix "CLSID" stands for *class identifier*, and the prefix *IID* stands for *interface identifier*.</span></span> <span data-ttu-id="2c378-145">Dabei handelt es sich um Standard Benennungs Konventionen in com.</span><span class="sxs-lookup"><span data-stu-id="2c378-145">These are standard naming conventions in COM.</span></span>

<span data-ttu-id="2c378-146">Wenn Sie diese Werte haben, würden Sie `Shape` wie folgt eine neue Instanz erstellen:</span><span class="sxs-lookup"><span data-stu-id="2c378-146">Given these values, you would create a new `Shape` instance as follows:</span></span>


```C++
IDrawable *pShape;
hr = CoCreateInstance(CLSID_Shape, NULL, CLSCTX_INPROC_SERVER, IID_Drawable,
     reinterpret_cast<void**>(&pShape));

if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



<span data-ttu-id="2c378-147">Die [**cokreateinzustance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion hat fünf Parameter.</span><span class="sxs-lookup"><span data-stu-id="2c378-147">The [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function has five parameters.</span></span> <span data-ttu-id="2c378-148">Der erste und vierte Parameter sind der Klassen Bezeichner und der Schnittstellen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="2c378-148">The first and fourth parameters are the class identifier and interface identifier.</span></span> <span data-ttu-id="2c378-149">Tatsächlich teilen diese Parameter die Funktion "Create the Shape Object" und geben mir einen Zeiger auf die idrawable-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2c378-149">In effect, these parameters tell the function, "Create the Shape object, and give me a pointer to the IDrawable interface."</span></span>

<span data-ttu-id="2c378-150">Legen Sie den zweiten Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="2c378-150">Set the second parameter to **NULL**.</span></span> <span data-ttu-id="2c378-151">(Weitere Informationen zur Bedeutung dieses Parameters finden Sie im Thema [Aggregation](/windows/desktop/com/aggregation) in der com-Dokumentation.) Der dritte Parameter nimmt einen Satz von Flags an, dessen Hauptzweck darin besteht, den *Ausführungs Kontext* für das Objekt anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2c378-151">(For more information about the meaning of this parameter, see the topic [Aggregation](/windows/desktop/com/aggregation) in the COM documentation.) The third parameter takes a set of flags whose main purpose is to specify the *execution context* for the object.</span></span> <span data-ttu-id="2c378-152">Der Ausführungs Kontext gibt an, ob das Objekt in demselben Prozess wie die Anwendung ausgeführt wird. in einem anderen Prozess auf demselben Computer oder auf einem Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="2c378-152">The execution context specifies whether the object runs in the same process as the application; in a different process on the same computer; or on a remote computer.</span></span> <span data-ttu-id="2c378-153">In der folgenden Tabelle werden die gängigsten Werte für diesen Parameter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c378-153">The following table shows the most common values for this parameter.</span></span>



| <span data-ttu-id="2c378-154">Flag</span><span class="sxs-lookup"><span data-stu-id="2c378-154">Flag</span></span>                       | <span data-ttu-id="2c378-155">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c378-155">Description</span></span>                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c378-156">**CLSCTX- \_ INPROC- \_ Server**</span><span class="sxs-lookup"><span data-stu-id="2c378-156">**CLSCTX\_INPROC\_SERVER**</span></span> | <span data-ttu-id="2c378-157">Der gleiche Prozess.</span><span class="sxs-lookup"><span data-stu-id="2c378-157">Same process.</span></span>                                                                                                                                                      |
| <span data-ttu-id="2c378-158">**lokaler CLSCTX- \_ \_ Server**</span><span class="sxs-lookup"><span data-stu-id="2c378-158">**CLSCTX\_LOCAL\_SERVER**</span></span>  | <span data-ttu-id="2c378-159">Anderer Prozess, gleicher Computer.</span><span class="sxs-lookup"><span data-stu-id="2c378-159">Different process, same computer.</span></span>                                                                                                                                  |
| <span data-ttu-id="2c378-160">**CLSCTX- \_ Remote \_ Server**</span><span class="sxs-lookup"><span data-stu-id="2c378-160">**CLSCTX\_REMOTE\_SERVER**</span></span> | <span data-ttu-id="2c378-161">Anderer Computer.</span><span class="sxs-lookup"><span data-stu-id="2c378-161">Different computer.</span></span>                                                                                                                                                |
| <span data-ttu-id="2c378-162">**Alle CLSCTX \_**</span><span class="sxs-lookup"><span data-stu-id="2c378-162">**CLSCTX\_ALL**</span></span>            | <span data-ttu-id="2c378-163">Verwenden Sie die effizienteste Option, die vom-Objekt unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2c378-163">Use the most efficient option that the object supports.</span></span> <span data-ttu-id="2c378-164">(Die Rangfolge, von der effizientesten bis zum geringsten Effizienz, ist: Prozess interne, Prozess-und Computer übergreifend.)</span><span class="sxs-lookup"><span data-stu-id="2c378-164">(The ranking, from most efficient to least efficient, is: in-process, out-of-process, and cross-computer.)</span></span> |



 

<span data-ttu-id="2c378-165">Die Dokumentation für eine bestimmte Komponente kann Ihnen mitteilen, welchen Ausführungs Kontext das Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2c378-165">The documentation for a particular component might tell you which execution context the object supports.</span></span> <span data-ttu-id="2c378-166">Wenn nicht, verwenden Sie " **CLSCTX \_ all**".</span><span class="sxs-lookup"><span data-stu-id="2c378-166">If not, use **CLSCTX\_ALL**.</span></span> <span data-ttu-id="2c378-167">Wenn Sie einen Ausführungs Kontext anfordern, der vom Objekt nicht unterstützt wird, gibt die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion den Fehlercode **RegDB \_ E \_ classnotreg** zurück.</span><span class="sxs-lookup"><span data-stu-id="2c378-167">If you request an execution context that the object does not support, the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function returns the error code **REGDB\_E\_CLASSNOTREG**.</span></span> <span data-ttu-id="2c378-168">Dieser Fehlercode kann auch darauf hindeuten, dass die CLSID keiner Komponente entspricht, die auf dem Computer des Benutzers registriert ist.</span><span class="sxs-lookup"><span data-stu-id="2c378-168">This error code can also indicate that the CLSID does not correspond to any component registered on the user's computer.</span></span>

<span data-ttu-id="2c378-169">Der fünfte Parameter für [**cokreateingestance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) erhält einen Zeiger auf die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2c378-169">The fifth parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) receives a pointer to the interface.</span></span> <span data-ttu-id="2c378-170">Da **cokreateingestance** ein generischer Mechanismus ist, kann dieser Parameter nicht stark typisiert sein.</span><span class="sxs-lookup"><span data-stu-id="2c378-170">Because **CoCreateInstance** is a generic mechanism, this parameter cannot be strongly typed.</span></span> <span data-ttu-id="2c378-171">Stattdessen ist der Datentyp " **void \* \***", und der Aufrufer muss die Adresse des Zeigers in **einen \* \* void** -Typ umwandeln.</span><span class="sxs-lookup"><span data-stu-id="2c378-171">Instead, the data type is **void\*\***, and the caller must coerce the address of the pointer to a **void\*\*** type.</span></span> <span data-ttu-id="2c378-172">Dies ist der Zweck der **erneuten interpretierungsumwandlung \_** im vorherigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="2c378-172">That is the purpose of the **reinterpret\_cast** in the previous example.</span></span>

<span data-ttu-id="2c378-173">Es ist wichtig, dass Sie den Rückgabewert von [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2c378-173">It is crucial to check the return value of [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="2c378-174">Wenn die Funktion einen Fehlercode zurückgibt, ist der COM-Schnittstellen Zeiger ungültig. der Versuch, ihn zu dereferenzieren, kann dazu führen, dass das Programm abstürzt.</span><span class="sxs-lookup"><span data-stu-id="2c378-174">If the function returns an error code, the COM interface pointer is invalid, and attempting to dereference it can cause your program to crash.</span></span>

<span data-ttu-id="2c378-175">Intern verwendet die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion verschiedene Techniken, um ein Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2c378-175">Internally, the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function uses various techniques to create an object.</span></span> <span data-ttu-id="2c378-176">Im einfachsten Fall wird der Klassen Bezeichner in der Registrierung nachgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="2c378-176">In the simplest case, it looks up the class identifier in the registry.</span></span> <span data-ttu-id="2c378-177">Der Registrierungs Eintrag verweist auf eine DLL oder exe, die das Objekt implementiert.</span><span class="sxs-lookup"><span data-stu-id="2c378-177">The registry entry points to a DLL or EXE that implements the object.</span></span> <span data-ttu-id="2c378-178">Von **cokreateinstance** können auch Informationen aus einem com+-Katalog oder einem parallelen (SxS) Manifest verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c378-178">**CoCreateInstance** can also use information from a COM+ catalog or a side-by-side (SxS) manifest.</span></span> <span data-ttu-id="2c378-179">Unabhängig davon sind die Details für den Aufrufer transparent.</span><span class="sxs-lookup"><span data-stu-id="2c378-179">Regardless, the details are transparent to the caller.</span></span> <span data-ttu-id="2c378-180">Weitere Informationen zu den internen Details von **cokreateinstance** finden Sie unter [com-Clients und-Server](/windows/desktop/com/com-clients-and-servers).</span><span class="sxs-lookup"><span data-stu-id="2c378-180">For more information about the internal details of **CoCreateInstance**, see [COM Clients and Servers](/windows/desktop/com/com-clients-and-servers).</span></span>

<span data-ttu-id="2c378-181">Das `Shapes` Beispiel, das wir bereits verwendet haben, ist etwas verwirrend. Nun können wir nun ein Beispiel für com in Aktion aktivieren: Anzeigen des Dialog Felds **Öffnen** , in dem der Benutzer eine Datei auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="2c378-181">The `Shapes` example that we have been using is somewhat contrived, so now let's turn to a real-world example of COM in action: displaying the **Open** dialog box for the user to select a file.</span></span>

## <a name="next"></a><span data-ttu-id="2c378-182">Nächste</span><span class="sxs-lookup"><span data-stu-id="2c378-182">Next</span></span>

[<span data-ttu-id="2c378-183">Beispiel: das Dialog Feld "Öffnen"</span><span class="sxs-lookup"><span data-stu-id="2c378-183">Example: The Open Dialog Box</span></span>](example--the-open-dialog-box.md)

 

 