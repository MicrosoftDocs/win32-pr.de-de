---
title: COM-Codierungs Methoden
description: In diesem Thema wird beschrieben, wie Sie Ihren com-Code effektiver und robuster gestalten können.
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a26143e5049c3db7efcbcc9353e74890fe0009c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104102478"
---
# <a name="com-coding-practices"></a><span data-ttu-id="26fb8-103">COM-Codierungs Methoden</span><span class="sxs-lookup"><span data-stu-id="26fb8-103">COM Coding Practices</span></span>

<span data-ttu-id="26fb8-104">In diesem Thema wird beschrieben, wie Sie Ihren com-Code effektiver und robuster gestalten können.</span><span class="sxs-lookup"><span data-stu-id="26fb8-104">This topic describes ways to make your COM code more effective and robust.</span></span>

-   [<span data-ttu-id="26fb8-105">Der \_ \_ uuidof-Operator</span><span class="sxs-lookup"><span data-stu-id="26fb8-105">The \_\_uuidof Operator</span></span>](/windows)
-   [<span data-ttu-id="26fb8-106">Das IID \_ PPV \_ args-Makro</span><span class="sxs-lookup"><span data-stu-id="26fb8-106">The IID\_PPV\_ARGS Macro</span></span>](/windows)
-   [<span data-ttu-id="26fb8-107">Das saferelease-Muster</span><span class="sxs-lookup"><span data-stu-id="26fb8-107">The SafeRelease Pattern</span></span>](#the-saferelease-pattern)
-   [<span data-ttu-id="26fb8-108">Intelligente com-Zeiger</span><span class="sxs-lookup"><span data-stu-id="26fb8-108">COM Smart Pointers</span></span>](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a><span data-ttu-id="26fb8-109">Der \_ \_ uuidof-Operator</span><span class="sxs-lookup"><span data-stu-id="26fb8-109">The \_\_uuidof Operator</span></span>

<span data-ttu-id="26fb8-110">Wenn Sie das Programm erstellen, erhalten Sie möglicherweise Linker-Fehler ähnlich den folgenden:</span><span class="sxs-lookup"><span data-stu-id="26fb8-110">When you build your program, you might get linker errors similar to the following:</span></span>

`unresolved external symbol "struct _GUID const IID_IDrawable"`

<span data-ttu-id="26fb8-111">Dieser Fehler bedeutet, dass eine GUID-Konstante mit externer Verknüpfung (**extern**) deklariert wurde und der Linker die Definition der Konstante nicht finden konnte.</span><span class="sxs-lookup"><span data-stu-id="26fb8-111">This error means that a GUID constant was declared with external linkage (**extern**), and the linker could not find the definition of the constant.</span></span> <span data-ttu-id="26fb8-112">Der Wert einer GUID-Konstante wird in der Regel aus einer statischen Bibliotheksdatei exportiert.</span><span class="sxs-lookup"><span data-stu-id="26fb8-112">The value of a GUID constant is usually exported from a static library file.</span></span> <span data-ttu-id="26fb8-113">Wenn Sie Microsoft Visual C++ verwenden, können Sie vermeiden, dass eine statische Bibliothek mit dem **\_ \_ uuidof** -Operator verknüpft werden muss.</span><span class="sxs-lookup"><span data-stu-id="26fb8-113">If you are using Microsoft Visual C++, you can avoid the need to link a static library by using the **\_\_uuidof** operator.</span></span> <span data-ttu-id="26fb8-114">Dieser Operator ist eine Microsoft-Spracherweiterung.</span><span class="sxs-lookup"><span data-stu-id="26fb8-114">This operator is a Microsoft language extension.</span></span> <span data-ttu-id="26fb8-115">Er gibt einen GUID-Wert aus einem Ausdruck zurück.</span><span class="sxs-lookup"><span data-stu-id="26fb8-115">It returns a GUID value from an expression.</span></span> <span data-ttu-id="26fb8-116">Der Ausdruck kann ein Schnittstellentyp Name, ein Klassenname oder ein Schnittstellen Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="26fb8-116">The expression can be an interface type name, a class name, or an interface pointer.</span></span> <span data-ttu-id="26fb8-117">Mithilfe von **\_ \_ uuidof** können Sie das gemeinsame Element Dialog Objekt wie folgt erstellen:</span><span class="sxs-lookup"><span data-stu-id="26fb8-117">Using **\_\_uuidof**, you can create the Common Item Dialog object as follows:</span></span>


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



<span data-ttu-id="26fb8-118">Der Compiler extrahiert den GUID-Wert aus dem Header, sodass kein Bibliotheks Export notwendig ist.</span><span class="sxs-lookup"><span data-stu-id="26fb8-118">The compiler extracts the GUID value from the header, so no library export is necessary.</span></span>

> [!Note]  
> <span data-ttu-id="26fb8-119">Der GUID-Wert wird durch Deklarieren im-Header dem Typnamen zugeordnet `__declspec(uuid( ... ))` .</span><span class="sxs-lookup"><span data-stu-id="26fb8-119">The GUID value is associated with the type name by declaring `__declspec(uuid( ... ))` in the header.</span></span> <span data-ttu-id="26fb8-120">Weitere Informationen finden Sie in der Dokumentation zu **\_ \_ declspec** in der Visual C++-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="26fb8-120">For more information, see the documentation for **\_\_declspec** in the Visual C++ documentation.</span></span>

 

## <a name="the-iid_ppv_args-macro"></a><span data-ttu-id="26fb8-121">Das IID \_ PPV \_ args-Makro</span><span class="sxs-lookup"><span data-stu-id="26fb8-121">The IID\_PPV\_ARGS Macro</span></span>

<span data-ttu-id="26fb8-122">Wir haben gesehen, dass sowohl [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) als auch [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) das Umwandeln des letzten Parameters in einen **void \* \*** -Typ erfordern.</span><span class="sxs-lookup"><span data-stu-id="26fb8-122">We saw that both [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) require coercing the final parameter to a **void\*\*** type.</span></span> <span data-ttu-id="26fb8-123">Dadurch wird das Potenzial eines Typen Konflikts erstellt.</span><span class="sxs-lookup"><span data-stu-id="26fb8-123">This creates the potential for a type mismatch.</span></span> <span data-ttu-id="26fb8-124">Betrachten Sie das folgende Codefragment:</span><span class="sxs-lookup"><span data-stu-id="26fb8-124">Consider the following code fragment:</span></span>


```C++
// Wrong!

IFileOpenDialog *pFileOpen;

hr = CoCreateInstance(
    __uuidof(FileOpenDialog), 
    NULL, 
    CLSCTX_ALL, 
    __uuidof(IFileDialogCustomize),       // The IID does not match the pointer type!
    reinterpret_cast<void**>(&pFileOpen)  // Coerce to void**.
    );
```



<span data-ttu-id="26fb8-125">Dieser Code fordert die [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) -Schnittstelle an, übergibt aber einen [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="26fb8-125">This code asks for the [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) interface, but passes in an [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) pointer.</span></span> <span data-ttu-id="26fb8-126">Der **reinterpretierungscast \_** -Ausdruck umgeht das C++-Typsystem, sodass der Compiler diesen Fehler nicht abfängt.</span><span class="sxs-lookup"><span data-stu-id="26fb8-126">The **reinterpret\_cast** expression circumvents the C++ type system, so the compiler will not catch this error.</span></span> <span data-ttu-id="26fb8-127">Im besten Fall, wenn das Objekt die angeforderte Schnittstelle nicht implementiert, schlägt der-Befehl einfach fehl.</span><span class="sxs-lookup"><span data-stu-id="26fb8-127">In the best case, if the object does not implement the requested interface, the call simply fails.</span></span> <span data-ttu-id="26fb8-128">Im schlimmsten Fall ist die Funktion erfolgreich, und Sie verfügen über einen nicht übereinstimmenden Zeiger.</span><span class="sxs-lookup"><span data-stu-id="26fb8-128">In the worst case, the function succeeds and you have a mismatched pointer.</span></span> <span data-ttu-id="26fb8-129">Anders ausgedrückt: der Zeigertyp stimmt nicht mit der tatsächlichen Vtable im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="26fb8-129">In other words, the pointer type does not match the actual vtable in memory.</span></span> <span data-ttu-id="26fb8-130">Wie Sie sich vorstellen können, kann an dieser Stelle nichts gutes vorkommen.</span><span class="sxs-lookup"><span data-stu-id="26fb8-130">As you can imagine, nothing good can happen at that point.</span></span>

> [!Note]  
> <span data-ttu-id="26fb8-131">Eine *vtable* (Virtual Method Table) ist eine Tabelle mit Funktions Zeigern.</span><span class="sxs-lookup"><span data-stu-id="26fb8-131">A *vtable* (virtual method table) is a table of function pointers.</span></span> <span data-ttu-id="26fb8-132">Die Vtable-Methode gibt an, wie com einen Methodenaufruf an seine Implementierung zur Laufzeit bindet.</span><span class="sxs-lookup"><span data-stu-id="26fb8-132">The vtable is how COM binds a method call to its implementation at run time.</span></span> <span data-ttu-id="26fb8-133">Nicht zufällig stellen vtables dar, wie die meisten C++-Compiler virtuelle Methoden implementieren.</span><span class="sxs-lookup"><span data-stu-id="26fb8-133">Not coincidentally, vtables are how most C++ compilers implement virtual methods.</span></span>

 

<span data-ttu-id="26fb8-134">Das [**IID \_ PPV \_ args**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) -Makro hilft, diese Fehler Klasse zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="26fb8-134">The [**IID\_PPV\_ARGS**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) macro helps to avoid this class of error.</span></span> <span data-ttu-id="26fb8-135">Um dieses Makro zu verwenden, ersetzen Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="26fb8-135">To use this macro, replace the following code:</span></span>


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



<span data-ttu-id="26fb8-136">durch diesen:</span><span class="sxs-lookup"><span data-stu-id="26fb8-136">with this:</span></span>


```C++
IID_PPV_ARGS(&pFileOpen)
```



<span data-ttu-id="26fb8-137">Das Makro fügt automatisch `__uuidof(IFileOpenDialog)` für den Schnittstellen Bezeichner ein, sodass es sicher ist, dass es mit dem Zeigertyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="26fb8-137">The macro automatically inserts `__uuidof(IFileOpenDialog)` for the interface identifier, so it is guaranteed to match the pointer type.</span></span> <span data-ttu-id="26fb8-138">Dies ist der geänderte (und korrekte) Code:</span><span class="sxs-lookup"><span data-stu-id="26fb8-138">Here is the modified (and correct) code:</span></span>


```C++
// Right.
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    IID_PPV_ARGS(&pFileOpen));
```



<span data-ttu-id="26fb8-139">Sie können dasselbe Makro mit [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))verwenden:</span><span class="sxs-lookup"><span data-stu-id="26fb8-139">You can use the same macro with [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span></span>


```C++
IFileDialogCustomize *pCustom;
hr = pFileOpen->QueryInterface(IID_PPV_ARGS(&pCustom));
```



## <a name="the-saferelease-pattern"></a><span data-ttu-id="26fb8-140">Das saferelease-Muster</span><span class="sxs-lookup"><span data-stu-id="26fb8-140">The SafeRelease Pattern</span></span>

<span data-ttu-id="26fb8-141">Die Verweis Zählung ist eine der Dinge in der Programmierung, die im Grunde einfach ist, aber auch mühsam ist, sodass es leicht schief geht.</span><span class="sxs-lookup"><span data-stu-id="26fb8-141">Reference counting is one of those things in programming that is basically easy, but is also tedious, which makes it easy to get wrong.</span></span> <span data-ttu-id="26fb8-142">Typische Fehler sind:</span><span class="sxs-lookup"><span data-stu-id="26fb8-142">Typical errors include:</span></span>

-   <span data-ttu-id="26fb8-143">Ein Schnittstellen Zeiger kann nicht freigegeben werden, wenn Sie ihn nicht mehr verwenden.</span><span class="sxs-lookup"><span data-stu-id="26fb8-143">Failing to release an interface pointer when you are done using it.</span></span> <span data-ttu-id="26fb8-144">Diese Fehler Klasse bewirkt, dass Ihr Programmspeicher und andere Ressourcen nicht mehr unternimmt, da Objekte nicht zerstört werden.</span><span class="sxs-lookup"><span data-stu-id="26fb8-144">This class of bug will cause your program to leak memory and other resources, because objects are not destroyed.</span></span>
-   <span data-ttu-id="26fb8-145">[**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) mit einem ungültigen Zeiger wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="26fb8-145">Calling [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) with an invalid pointer.</span></span> <span data-ttu-id="26fb8-146">Dieser Fehler kann z. b. auftreten, wenn das Objekt nie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="26fb8-146">For example, this error can happen if the object was never created.</span></span> <span data-ttu-id="26fb8-147">Diese Fehler Kategorie führt wahrscheinlich zu einem Absturz Ihres Programms.</span><span class="sxs-lookup"><span data-stu-id="26fb8-147">This category of bug will probably cause your program to crash.</span></span>
-   <span data-ttu-id="26fb8-148">Dereferenzierung eines Schnittstellen Zeigers nach dem Aufrufen des [**Releases**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="26fb8-148">Dereferencing an interface pointer after [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) is called.</span></span> <span data-ttu-id="26fb8-149">Dieser Fehler kann zum Absturz des Programms führen.</span><span class="sxs-lookup"><span data-stu-id="26fb8-149">This bug may cause your program to crash.</span></span> <span data-ttu-id="26fb8-150">Schlimmer noch: das Programm kann zu einem zufälligen späteren Zeitpunkt abstürzen, sodass es schwierig ist, den ursprünglichen Fehler zu finden.</span><span class="sxs-lookup"><span data-stu-id="26fb8-150">Worse, it may cause your program to crash at a random later time, making it hard to track down the original error.</span></span>

<span data-ttu-id="26fb8-151">Eine Möglichkeit, diese Fehler zu vermeiden, besteht darin, die [**Freigabe**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) über eine Funktion aufzurufen, die den Zeiger sicher freigibt.</span><span class="sxs-lookup"><span data-stu-id="26fb8-151">One way to avoid these bugs is to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) through a function that safely releases the pointer.</span></span> <span data-ttu-id="26fb8-152">Der folgende Code zeigt eine Funktion, die Folgendes bewirkt:</span><span class="sxs-lookup"><span data-stu-id="26fb8-152">The following code shows a function that does this:</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



<span data-ttu-id="26fb8-153">Diese Funktion verwendet einen COM-Schnittstellen Zeiger als Parameter und führt folgende Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="26fb8-153">This function takes a COM interface pointer as a parameter and does the following:</span></span>

1.  <span data-ttu-id="26fb8-154">Überprüft, ob der Zeiger **null** ist.</span><span class="sxs-lookup"><span data-stu-id="26fb8-154">Checks whether the pointer is **NULL**.</span></span>
2.  <span data-ttu-id="26fb8-155">Ruft [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf, wenn der Zeiger nicht **null** ist.</span><span class="sxs-lookup"><span data-stu-id="26fb8-155">Calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) if the pointer is not **NULL**.</span></span>
3.  <span data-ttu-id="26fb8-156">Legt den Zeiger auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="26fb8-156">Sets the pointer to **NULL**.</span></span>

<span data-ttu-id="26fb8-157">Im folgenden finden Sie ein Beispiel für die Verwendung von `SafeRelease` :</span><span class="sxs-lookup"><span data-stu-id="26fb8-157">Here is an example of how to use `SafeRelease`:</span></span>


```C++
void UseSafeRelease()
{
    IFileOpenDialog *pFileOpen = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        // Use the object.
    }
    SafeRelease(&pFileOpen);
}
```



<span data-ttu-id="26fb8-158">Wenn [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) erfolgreich ist, gibt der-Befehl `SafeRelease` den-Zeiger frei.</span><span class="sxs-lookup"><span data-stu-id="26fb8-158">If [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) succeeds, the call to `SafeRelease` releases the pointer.</span></span> <span data-ttu-id="26fb8-159">Wenn **cokreateingestance** fehlschlägt, bleibt *pfileopen* gleich **null**.</span><span class="sxs-lookup"><span data-stu-id="26fb8-159">If **CoCreateInstance** fails, *pFileOpen* remains **NULL**.</span></span> <span data-ttu-id="26fb8-160">Die `SafeRelease` Funktion prüft dies und überspringt den [**Freigabe Freigabe**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)Vorgang.</span><span class="sxs-lookup"><span data-stu-id="26fb8-160">The `SafeRelease` function checks for this and skips the call to [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span>

<span data-ttu-id="26fb8-161">Es ist auch sicher, mehrmals `SafeRelease` auf demselben Zeiger aufzurufen, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="26fb8-161">It is also safe to call `SafeRelease` more than once on the same pointer, as shown here:</span></span>


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a><span data-ttu-id="26fb8-162">Intelligente com-Zeiger</span><span class="sxs-lookup"><span data-stu-id="26fb8-162">COM Smart Pointers</span></span>

<span data-ttu-id="26fb8-163">Die- `SafeRelease` Funktion ist nützlich, erfordert jedoch zwei Dinge:</span><span class="sxs-lookup"><span data-stu-id="26fb8-163">The `SafeRelease` function is useful, but it requires you to remember two things:</span></span>

-   <span data-ttu-id="26fb8-164">Initialisieren Sie jeden Schnittstellen Zeiger auf **null**.</span><span class="sxs-lookup"><span data-stu-id="26fb8-164">Initialize every interface pointer to **NULL**.</span></span>
-   <span data-ttu-id="26fb8-165">Wird aufgerufen `SafeRelease` , bevor jeder Zeiger den Gültigkeitsbereich verlässt.</span><span class="sxs-lookup"><span data-stu-id="26fb8-165">Call `SafeRelease` before each pointer goes out of scope.</span></span>

<span data-ttu-id="26fb8-166">Als C++-Programmierer denken Sie wahrscheinlich daran, dass Sie sich keine dieser Dinge merken müssen.</span><span class="sxs-lookup"><span data-stu-id="26fb8-166">As a C++ programmer, you are probably thinking that you shouldn't have to remember either of these things.</span></span> <span data-ttu-id="26fb8-167">Das ist der Grund, warum C++ über Konstruktoren und Dekonstruktoren verfügt.</span><span class="sxs-lookup"><span data-stu-id="26fb8-167">After all, that's why C++ has constructors and destructors.</span></span> <span data-ttu-id="26fb8-168">Es wäre schön, eine Klasse zu haben, die den zugrunde liegenden Schnittstellen Zeiger umschließt und den Zeiger automatisch initialisiert und freigibt.</span><span class="sxs-lookup"><span data-stu-id="26fb8-168">It would be nice to have a class that wraps the underlying interface pointer and automatically initializes and releases the pointer.</span></span> <span data-ttu-id="26fb8-169">Anders ausgedrückt, wir möchten etwa Folgendes:</span><span class="sxs-lookup"><span data-stu-id="26fb8-169">In other words, we want something like this:</span></span>


```C++
// Warning: This example is not complete.

template <class T>
class SmartPointer
{
    T* ptr;

 public:
    SmartPointer(T *p) : ptr(p) { }
    ~SmartPointer()
    {
        if (ptr) { ptr->Release(); }
    }
};
```



<span data-ttu-id="26fb8-170">Die hier gezeigte Klassendefinition ist unvollständig und kann nicht wie dargestellt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26fb8-170">The class definition shown here is incomplete, and is not usable as shown.</span></span> <span data-ttu-id="26fb8-171">Sie müssen mindestens einen Kopierkonstruktor, einen Zuweisungs Operator und eine Möglichkeit für den Zugriff auf den zugrunde liegenden COM-Zeiger definieren.</span><span class="sxs-lookup"><span data-stu-id="26fb8-171">At a minimum, you would need to define a copy constructor, an assignment operator, and a way to access the underlying COM pointer.</span></span> <span data-ttu-id="26fb8-172">Glücklicherweise müssen Sie keine dieser Aufgaben erledigen, da Microsoft Visual Studio bereits eine intelligente Zeiger Klasse als Teil der Active Template Library (ATL) bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="26fb8-172">Fortunately, you don't need to do any of this work, because Microsoft Visual Studio already provides a smart pointer class as part of the Active Template Library (ATL).</span></span>

<span data-ttu-id="26fb8-173">Die intelligente ATL-Zeiger Klasse hat den Namen " **CComPtr**".</span><span class="sxs-lookup"><span data-stu-id="26fb8-173">The ATL smart pointer class is named **CComPtr**.</span></span> <span data-ttu-id="26fb8-174">(Es gibt auch eine **CComQIPtr** -Klasse, die hier nicht erläutert wird.) Hier sehen Sie das [Dialog Feld Öffnen](example--the-open-dialog-box.md) , das für die Verwendung von **CComPtr** umgeschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="26fb8-174">(There is also a **CComQIPtr** class, which is not discussed here.) Here is the [Open Dialog Box](example--the-open-dialog-box.md) example rewritten to use **CComPtr**.</span></span>


```C++
#include <windows.h>
#include <shobjidl.h> 
#include <atlbase.h> // Contains the declaration of CComPtr.

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CComPtr<IFileOpenDialog> pFileOpen;

        // Create the FileOpenDialog object.
        hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                CComPtr<IShellItem> pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBox(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                }

                // pItem goes out of scope.
            }

            // pFileOpen goes out of scope.
        }
        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="26fb8-175">Der Hauptunterschied zwischen diesem Code und dem ursprünglichen Beispiel besteht darin, dass diese Version [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)nicht explizit aufruft.</span><span class="sxs-lookup"><span data-stu-id="26fb8-175">The main difference between this code and the original example is that this version does not explicitly call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="26fb8-176">Wenn die **CComPtr** -Instanz den Gültigkeitsbereich verlässt, ruft der Dekonstruktor **Release** auf dem zugrunde liegenden Zeiger auf.</span><span class="sxs-lookup"><span data-stu-id="26fb8-176">When the **CComPtr** instance goes out of scope, the destructor calls **Release** on the underlying pointer.</span></span>

<span data-ttu-id="26fb8-177">**CComPtr** ist eine Klassen Vorlage.</span><span class="sxs-lookup"><span data-stu-id="26fb8-177">**CComPtr** is a class template.</span></span> <span data-ttu-id="26fb8-178">Das Vorlagen Argument ist der com-Schnittstellentyp.</span><span class="sxs-lookup"><span data-stu-id="26fb8-178">The template argument is the COM interface type.</span></span> <span data-ttu-id="26fb8-179">Intern enthält **CComPtr** einen Zeiger dieses Typs.</span><span class="sxs-lookup"><span data-stu-id="26fb8-179">Internally, **CComPtr** holds a pointer of that type.</span></span> <span data-ttu-id="26fb8-180">**CComPtr** überschreibt **Operator-> ()** und **Operator& ()** , sodass die Klasse wie der zugrunde liegende Zeiger fungiert.</span><span class="sxs-lookup"><span data-stu-id="26fb8-180">**CComPtr** overrides **operator->()** and **operator&()** so that the class acts like the underlying pointer.</span></span> <span data-ttu-id="26fb8-181">Beispielsweise entspricht der folgende Code dem direkten Aufrufen der **IFileOpenDialog:: Show** -Methode:</span><span class="sxs-lookup"><span data-stu-id="26fb8-181">For example, the following code is equivalent to calling the **IFileOpenDialog::Show** method directly:</span></span>


```C++
hr = pFileOpen->Show(NULL);
```



<span data-ttu-id="26fb8-182">**CComPtr** definiert auch eine **CComPtr:: cokreatan Stance** -Methode, die die com- [**cokreateinzustance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion mit einigen Standardparameterwerten aufruft.</span><span class="sxs-lookup"><span data-stu-id="26fb8-182">**CComPtr** also defines a **CComPtr::CoCreateInstance** method, which calls the COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function with some default parameter values.</span></span> <span data-ttu-id="26fb8-183">Der einzige erforderliche Parameter ist der Klassen Bezeichner, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="26fb8-183">The only required parameter is the class identifier, as the next example shows:</span></span>


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



<span data-ttu-id="26fb8-184">Die **CComPtr:: cokreateinzustance** -Methode wird ausschließlich als praktische bereitgestellt. Wenn Sie möchten, können Sie weiterhin die com- [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="26fb8-184">The **CComPtr::CoCreateInstance** method is provided purely as a convenience; you can still call the COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, if you prefer.</span></span>

## <a name="next"></a><span data-ttu-id="26fb8-185">Nächste</span><span class="sxs-lookup"><span data-stu-id="26fb8-185">Next</span></span>

[<span data-ttu-id="26fb8-186">Fehlerbehandlung in com</span><span class="sxs-lookup"><span data-stu-id="26fb8-186">Error Handling in COM</span></span>](error-handling-in-com.md)

 

 