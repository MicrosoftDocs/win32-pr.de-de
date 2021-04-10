---
title: Unterschiede zwischen "Mittel l" und "MkTypLib"
description: Unterschiede zwischen "Mittel l" und "MkTypLib"
ms.assetid: 86abd70b-7238-49a6-a996-2c8906a14449
keywords:
- Mittel l-und ODL-Mittell, Unterschiede zwischen der mittleren und der MkTypLib
- MkTypLib-Mittell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a54b6103cc230e1c5e6700b0ddc93312c767f9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037603"
---
# <a name="differences-between-midl-and-mktyplib"></a><span data-ttu-id="1b36b-105">Unterschiede zwischen "Mittel l" und "MkTypLib"</span><span class="sxs-lookup"><span data-stu-id="1b36b-105">Differences Between MIDL and MkTypLib</span></span>

> [!Note]  
> <span data-ttu-id="1b36b-106">Das Mktyplib.exe Tool ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="1b36b-106">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="1b36b-107">Verwenden Sie stattdessen den Mittel l-Compiler.</span><span class="sxs-lookup"><span data-stu-id="1b36b-107">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="1b36b-108">Es gibt einige wichtige Bereiche, in denen der mittlerer l-Compiler von MkTypLib abweicht.</span><span class="sxs-lookup"><span data-stu-id="1b36b-108">There are a few key areas in which the MIDL compiler differs from MkTypLib.</span></span> <span data-ttu-id="1b36b-109">Die meisten dieser Unterschiede treten auf, weil die mittlere Anzahl eher an die C-Syntax gerichtet ist als auf MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="1b36b-109">Most of these differences arise because MIDL is oriented more toward C-syntax than MkTypLib.</span></span>

<span data-ttu-id="1b36b-110">Im Allgemeinen empfiehlt es sich, die Syntax Syntax in ihren IDL-Dateien zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b36b-110">In general, you will want to use the MIDL syntax in your IDL files.</span></span> <span data-ttu-id="1b36b-111">Wenn Sie jedoch eine vorhandene ODL-Datei kompilieren oder auf andere Weise die Kompatibilität mit MkTypLib beibehalten müssen, verwenden Sie die compiler2,03 Mkktyplib.exe Option [**/mktyplib203**](-mktyplib203.md) .</span><span class="sxs-lookup"><span data-stu-id="1b36b-111">However, if you need to compile an existing ODL file, or otherwise maintain compatibility with MkTypLib, use the [**/mktyplib203**](-mktyplib203.md) MIDL compiler option to force MIDL to behave like Mkktyplib.exe, version 2.03.</span></span> <span data-ttu-id="1b36b-112">(Dies ist die letzte Version des MkTypLib-Tools.) Die Option **/mktyplib203** löst die folgenden Unterschiede aus:</span><span class="sxs-lookup"><span data-stu-id="1b36b-112">(This is the last release of the MkTypLib tool.) Specifically, the **/mktyplib203** option resolves these differences:</span></span>

-   <span data-ttu-id="1b36b-113">typedef-Syntax für komplexe Datentypen</span><span class="sxs-lookup"><span data-stu-id="1b36b-113">typedef syntax for complex data types</span></span>

    <span data-ttu-id="1b36b-114">In MkTypLib generieren beide der folgenden Definitionen einen tkind- \_ Datensatz für "This \_ struct" in der Typbibliothek.</span><span class="sxs-lookup"><span data-stu-id="1b36b-114">In MkTypLib, both of the following definitions generate a TKIND\_RECORD for "this\_struct" in the type library.</span></span> <span data-ttu-id="1b36b-115">Das Tag "struct \_ Tag" ist optional und wird, falls verwendet, nicht in der Typbibliothek angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1b36b-115">The tag "struct\_tag" is optional and, if used, will not show up in the type library.</span></span>

    ``` syntax
    typedef struct struct_tag { ... } this_struct;
    typedef struct { ... } that_struct;
    ```

    <span data-ttu-id="1b36b-116">Wenn ein optionales Tag fehlt, wird es von der Mittell generiert, wodurch der vom Benutzer bereitgestellten Definition ein Tag hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="1b36b-116">If an optional tag is missing, MIDL will generate it, effectively adding a tag to the definition supplied by the user.</span></span> <span data-ttu-id="1b36b-117">Da die erste Definition über ein Tag verfügt, generiert die mittlere l einen tkind \_ -Datensatz für "This \_ struct" und einen tkind- \_ Alias für "This \_ struct" ("This \_ struct" als Alias für "struct \_ Tag").</span><span class="sxs-lookup"><span data-stu-id="1b36b-117">Since the first definition has a tag, MIDL will generate a TKIND\_RECORD for "this\_struct" and a TKIND\_ALIAS for "this\_struct" (defining "this\_struct" as an alias for "struct\_tag").</span></span> <span data-ttu-id="1b36b-118">Da das-Tag in der zweiten Definition fehlt, generiert die Mittel-l einen tkind \_ -Datensatz für einen geschilderten Namen, der für den Benutzer und einen tkind- \_ Alias für "This struct" nicht aussagekräftig ist \_ .</span><span class="sxs-lookup"><span data-stu-id="1b36b-118">Because the tag is missing in the second definition, MIDL will generate a TKIND\_RECORD for a mangled name, internal to MIDL, that is not meaningful to the user and a TKIND\_ALIAS for "that\_struct".</span></span>

    <span data-ttu-id="1b36b-119">Dies hat potenzielle Auswirkungen auf Typbibliotheks Browser, die einfach den Namen eines Datensatzes in der Benutzeroberfläche anzeigen.</span><span class="sxs-lookup"><span data-stu-id="1b36b-119">This has potential implications for type library browsers that simply show the name of a record in their user interface.</span></span> <span data-ttu-id="1b36b-120">Wenn Sie davon ausgehen, dass ein tkind- \_ Datensatz einen echten Namen hat, können nicht erkennbare Namen in der Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1b36b-120">If you expect a TKIND\_RECORD to have a real name, unrecognizable names could appear in the user interface.</span></span> <span data-ttu-id="1b36b-121">Dieses Verhalten gilt auch für [**Union**](union.md) -und [**Enumeration**](enum.md) -Definitionen, mit dem Mittelwert Compiler, der tkind \_ Unions \_ bzw. tkind-enums erzeugt.</span><span class="sxs-lookup"><span data-stu-id="1b36b-121">This behavior also applies to [**union**](union.md) and [**enum**](enum.md) definitions, with the MIDL compiler generating TKIND\_UNIONs and TKIND\_ENUMs, respectively.</span></span>

    <span data-ttu-id="1b36b-122">In der mittleren l sind auch [**Struktur**](struct.md)-, [**Union**](union.md) [**-und**](enum.md) Enumerationsdefinitionen im C-Stil zulässig.</span><span class="sxs-lookup"><span data-stu-id="1b36b-122">MIDL also allows C-style [**struct**](struct.md), [**union**](union.md), and [**enum**](enum.md) definitions.</span></span> <span data-ttu-id="1b36b-123">Beispielsweise ist die folgende Definition in der Mitte gültig:</span><span class="sxs-lookup"><span data-stu-id="1b36b-123">For example, the following definition is legal in MIDL:</span></span>

    ``` syntax
    struct my_struct { ... };
    typedef struct my_struct your_struct;
    ```

-   <span data-ttu-id="1b36b-124">Boolean-Datentypen</span><span class="sxs-lookup"><span data-stu-id="1b36b-124">Boolean data types</span></span>

    <span data-ttu-id="1b36b-125">In MkTypLib entsprechen der [**boolesche**](boolean.md) Basistyp und der MkTypLib-Datentyp bool dem Wert VT \_ bool, der Variant \_ bool zugeordnet und als [**kurz**](short.md)definiert ist.</span><span class="sxs-lookup"><span data-stu-id="1b36b-125">In MkTypLib, the [**Boolean**](boolean.md) base type and the MkTypLib data type BOOL equate to VT\_BOOL, which maps to VARIANT\_BOOL, and which is defined as a [**short**](short.md).</span></span> <span data-ttu-id="1b36b-126">In der mittleren l entspricht der **boolesche** Basistyp VT \_ UI1, der als [**Ganzzahl ohne Vorzeichen char**](unsigned.md)definiert ist, und der boolesche Datentyp ist als [**Long**](long.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="1b36b-126">In MIDL, the **Boolean** base type is equivalent to VT\_UI1, which is defined as an [**unsigned char**](unsigned.md), and the BOOL data type is defined as a [**long**](long.md).</span></span> <span data-ttu-id="1b36b-127">Dies führt zu Problemen, wenn Sie die IDL-Syntax und die ODL-Syntax in derselben Datei mischen, während Sie trotzdem versuchen, die Kompatibilität mit MkTypLib aufrechtzuerhalten.</span><span class="sxs-lookup"><span data-stu-id="1b36b-127">This leads to difficulties if you mix IDL syntax and ODL syntax in the same file while still trying to maintain compatibility with MkTypLib.</span></span> <span data-ttu-id="1b36b-128">Da die Datentypen unterschiedlich groß sind, entspricht der Marshallingcode nicht den Informationen, die in den Typinformationen beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1b36b-128">Because the data types are different sizes, the marshaling code will not match what is described in the type information.</span></span> <span data-ttu-id="1b36b-129">Wenn Sie \_ in ihrer Typbibliothek einen VT-booleschen Wert verwenden möchten, sollten Sie den \_ Datentyp Variant bool verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b36b-129">If you want a VT\_BOOL in your type library, you should use the VARIANT\_BOOL data type.</span></span>

-   <span data-ttu-id="1b36b-130">GUID-Definitionen in Header Dateien</span><span class="sxs-lookup"><span data-stu-id="1b36b-130">GUID definitions in header files</span></span>

    <span data-ttu-id="1b36b-131">In MkTypLib werden GUIDs in der Header Datei mit einem Makro definiert, das bedingt kompiliert werden kann, um entweder eine GUID-prädefinition oder eine instanziierte GUID zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1b36b-131">In MkTypLib, GUIDs are defined in the header file with a macro that can be conditionally compiled to generate either a GUID predefinition or an instantiated GUID.</span></span> <span data-ttu-id="1b36b-132">In der Regel werden GUID-prädefinitionen in den generierten Header Dateien und GUID-Instanziierungen nur in der vom [**/IID**](-iid.md) -Schalter generierten Datei abgelegt.</span><span class="sxs-lookup"><span data-stu-id="1b36b-132">MIDL normally puts GUID predefinitions in its generated header files and GUID instantiations only in the file generated by the [**/iid**](-iid.md) switch.</span></span>

<span data-ttu-id="1b36b-133">Die folgenden Unterschiede im Verhalten können nicht mithilfe des [**/mktyplib203**](-mktyplib203.md) -Schalters aufgelöst werden:</span><span class="sxs-lookup"><span data-stu-id="1b36b-133">The following differences in behavior cannot be resolved by using the [**/mktyplib203**](-mktyplib203.md) switch:</span></span>

-   <span data-ttu-id="1b36b-134">Groß- und Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="1b36b-134">Case sensitivity</span></span>

    <span data-ttu-id="1b36b-135">Bei der Groß-/Kleinschreibung wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="1b36b-135">MIDL is case sensitive, OLE Automation is not.</span></span>

-   <span data-ttu-id="1b36b-136">Bereich von Symbolen in einer Aufzählungs Deklaration</span><span class="sxs-lookup"><span data-stu-id="1b36b-136">Scope of symbols in an enum declaration</span></span>

    <span data-ttu-id="1b36b-137">In MkTypLib ist der Gültigkeitsbereich von Symbolen in einer Aufzählung lokal.</span><span class="sxs-lookup"><span data-stu-id="1b36b-137">In MkTypLib the scope of symbols in an enum is local.</span></span> <span data-ttu-id="1b36b-138">In der mittleren l ist der Gültigkeitsbereich von Symbolen in einer-Aufzählung Global, wie er in C ist. Der folgende Code wird z. b. in MkTypLib kompiliert, generiert jedoch einen doppelten Namensfehler in der mittleren l:</span><span class="sxs-lookup"><span data-stu-id="1b36b-138">In MIDL, the scope of symbols in an enum is global, as it is in C. For example, the following code will compile in MkTypLib, but will generate a duplicate name error in MIDL:</span></span>

    ``` syntax
    typedef struct { ... } a;
    enum {a=1, b=2, c=3};
    ```

-   <span data-ttu-id="1b36b-139">Bereich des öffentlichen Attributs</span><span class="sxs-lookup"><span data-stu-id="1b36b-139">Scope of public attribute</span></span>

    <span data-ttu-id="1b36b-140">Wenn Sie das [**Public**](public.md) -Attribut auf einen Schnittstellen Block anwenden, behandelt MkTypLib jede typedef in diesem Schnittstellen Block als Public.</span><span class="sxs-lookup"><span data-stu-id="1b36b-140">If you apply the [**public**](public.md) attribute to an interface block, MkTypLib treats every typedef inside that interface block as public.</span></span> <span data-ttu-id="1b36b-141">Bei der mittleren l ist es erforderlich, dass Sie das **öffentliche** Attribut explizit auf die Typedefs anwenden, die öffentlich sein sollen.</span><span class="sxs-lookup"><span data-stu-id="1b36b-141">MIDL requires that you explicitly apply the **public** attribute to those typedefs that you want public.</span></span>

-   <span data-ttu-id="1b36b-142">Importlib-Such Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="1b36b-142">Importlib search order</span></span>

    <span data-ttu-id="1b36b-143">Wenn Sie mehr als eine Typbibliothek importieren und diese Bibliotheken doppelte Verweise enthalten, löst MkTypLib dies mithilfe des ersten gefundenen Verweises auf.</span><span class="sxs-lookup"><span data-stu-id="1b36b-143">If you import more than one type library, and if these libraries contain duplicate references, MkTypLib resolves this by using the first reference that it finds.</span></span> <span data-ttu-id="1b36b-144">In der Mitte wird der letzte Verweis verwendet, den er findet.</span><span class="sxs-lookup"><span data-stu-id="1b36b-144">MIDL will use the last reference that it finds.</span></span> <span data-ttu-id="1b36b-145">Mit der folgenden ODL-Syntax verwendet Library C z. b. die MOO-typedef von Bibliothek A, wenn Sie mit MkTypLib kompilieren, und die MOO-Typdefinition aus Bibliothek B, wenn Sie mit der mittleren l kompilieren:</span><span class="sxs-lookup"><span data-stu-id="1b36b-145">For example, given the following ODL syntax, library C will use the MOO typedef from library A if you compile with MkTypLib, and the MOO typedef from library B if you compile with MIDL:</span></span>

    ``` syntax
    [...]library A
    {
        typedef struct tagMOO
        {...}MOO
    }

    [...]library B
    {
        typedef struct tagMOO
        {...} MOO
    }

    [...]library C
    {
        importlib (A.TLB)
        importlib (B.TLB)
        typedef struct tagBAA
        {MOO y;}BAA
    }
    ```

    <span data-ttu-id="1b36b-146">Die entsprechende Problem Umgehung hierfür besteht darin, jeden Verweis auf diesen Verweis mit dem richtigen Import Bibliotheksnamen zu qualifizieren, wie im folgenden Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1b36b-146">The appropriate workaround for this is to qualify each such reference with the correct import library name, like this:</span></span>

    ``` syntax
    typedef struct tagBAA
        {A.MOO y;}BAA
    ```

-   <span data-ttu-id="1b36b-147">VOID-Datentyp wurde nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="1b36b-147">VOID data type not recognized</span></span>

    <span data-ttu-id="1b36b-148">Der Datentyp " [**void**](void.md) " der C-Sprache wird von der mittleren l erkannt, und der Datentyp "OLE Automation void" wird nicht erkannt</span><span class="sxs-lookup"><span data-stu-id="1b36b-148">MIDL recognizes the C-language [**void**](void.md) data type and does not recognize the OLE Automation VOID data type.</span></span> <span data-ttu-id="1b36b-149">Wenn Sie über eine ODL-Datei verfügen, die void verwendet, platzieren Sie diese Definition am Anfang der Datei:</span><span class="sxs-lookup"><span data-stu-id="1b36b-149">If you have an ODL file that uses VOID, place this definition at the top of the file:</span></span>

    ``` syntax
#define VOID void
    ```

-   <span data-ttu-id="1b36b-150">Exponentialschreibweise</span><span class="sxs-lookup"><span data-stu-id="1b36b-150">Exponential notation</span></span>

    <span data-ttu-id="1b36b-151">Die in der Exponentialnotation ausgedrückte Werte müssen in Anführungszeichen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="1b36b-151">MIDL requires that values expressed in exponential notation be contained within quotation marks.</span></span> <span data-ttu-id="1b36b-152">Beispiel: "-2.5 e + 3"</span><span class="sxs-lookup"><span data-stu-id="1b36b-152">For example, "-2.5E+3"</span></span>

-   <span data-ttu-id="1b36b-153">LCID-Werte und-Konstanten</span><span class="sxs-lookup"><span data-stu-id="1b36b-153">LCID values and constants</span></span>

    <span data-ttu-id="1b36b-154">Normalerweise wird die LCID beim Auswerten von Dateien in der Mitte nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="1b36b-154">Normally MIDL does not consider the LCID when parsing files.</span></span> <span data-ttu-id="1b36b-155">Um dieses Verhalten für einen Wert zu erzwingen, oder wenn Sie beim Definieren einer Konstante eine Gebiets Schema spezifische Notation verwenden müssen, müssen Sie den Wert oder die Konstante in Anführungszeichen einschließen.</span><span class="sxs-lookup"><span data-stu-id="1b36b-155">To force this behavior for a value, or if you need to use locale-specific notation when defining a constant, enclose the value or constant in quotation marks.</span></span>

<span data-ttu-id="1b36b-156">Weitere Informationen finden Sie unter [**/mktyplib203**](-mktyplib203.md), [**/IID**](-iid.md)und Marshalling von [OLE-Datentypen](marshaling-ole-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="1b36b-156">For more information, see [**/mktyplib203**](-mktyplib203.md), [**/iid**](-iid.md), and [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 




