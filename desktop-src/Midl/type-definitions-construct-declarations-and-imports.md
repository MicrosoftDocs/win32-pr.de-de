---
title: Typdefinitionen, Konstruktordeklarationen und Importe
description: Typdefinitionen, Konstruktordeklarationen und Importe können außerhalb des Schnittstellen Texts auftreten.
ms.assetid: 5d9011ab-bfc4-41f6-bd69-953660191652
keywords:
- Schnittstellen-Mittell, Typdefinitionen
- Schnittstellen-Mittell, Konstruieren von Deklarationen
- Schnittstellen-Mittel l, Importe
- Typdefinitionen (Mittell)
- Konstruieren von Deklarationen in der Mitte
- importiert Mittel l
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645781f033566ba43dc6e355935ed112d0e8f5f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342247"
---
# <a name="type-definitions-construct-declarations-and-imports"></a><span data-ttu-id="0d16d-109">Typdefinitionen, Konstruktordeklarationen und Importe</span><span class="sxs-lookup"><span data-stu-id="0d16d-109">Type Definitions, Construct Declarations, and Imports</span></span>

<span data-ttu-id="0d16d-110">Typdefinitionen, Konstruktordeklarationen und Importe können außerhalb des Schnittstellen Texts auftreten.</span><span class="sxs-lookup"><span data-stu-id="0d16d-110">Type definitions, construct declarations, and imports can occur outside of the interface body.</span></span> <span data-ttu-id="0d16d-111">Alle Definitionen aus der Haupt-IDL-Datei werden in der generierten Header Datei angezeigt, und alle Prozeduren aus allen Schnittstellen in der Haupt-IDL-Datei generieren stubroutinen.</span><span class="sxs-lookup"><span data-stu-id="0d16d-111">All definitions from the main IDL file will appear in the generated header file, and all the procedures from all the interfaces in the main IDL file will generate stub routines.</span></span> <span data-ttu-id="0d16d-112">Dies ermöglicht es Anwendungen, die mehrere Schnittstellen unterstützen, IDL-Dateien in einer einzelnen, kombinierten IDL-Datei zusammenzuführen.</span><span class="sxs-lookup"><span data-stu-id="0d16d-112">This enables applications that support multiple interfaces to merge IDL files into a single, combined IDL file.</span></span>

<span data-ttu-id="0d16d-113">Daher ist es weniger Zeit, die Dateien zu kompilieren, und kann die Redundanz in den generierten Stubdaten auch durch die mittlere Größe verringern.</span><span class="sxs-lookup"><span data-stu-id="0d16d-113">As a result, it requires less time to compile the files and also allows MIDL to reduce redundancies in the generated stubs.</span></span> <span data-ttu-id="0d16d-114">Dadurch können [**Objekt**](object.md) Schnittstellen erheblich verbessert werden, indem allgemeiner Code für Basis Schnittstellen und abgeleitete Schnittstellen gemeinsam genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="0d16d-114">This can significantly improve [**object**](object.md) interfaces through the ability to share common code for base interfaces and derived interfaces.</span></span> <span data-ttu-id="0d16d-115">Bei nicht- **Objekt** Schnittstellen müssen die Namen der Prozedur über alle Schnittstellen hinweg eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="0d16d-115">For non- **object** interfaces, the procedure names must be unique across all the interfaces.</span></span> <span data-ttu-id="0d16d-116">Bei **Objekt** Schnittstellen müssen die Namen der Prozedur nur innerhalb einer Schnittstelle eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="0d16d-116">For **object** interfaces, the procedure names need to be unique only within an interface.</span></span> <span data-ttu-id="0d16d-117">Beachten Sie, dass mehrere Schnittstellen nicht zulässig sind, wenn Sie den Schalter [**/OSF**](-osf.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="0d16d-117">Note that multiple interfaces are not permitted when you use the [**/osf**](-osf.md) switch.</span></span>

## <a name="declarative-constructs"></a><span data-ttu-id="0d16d-118">Deklarative Konstrukte</span><span class="sxs-lookup"><span data-stu-id="0d16d-118">Declarative Constructs</span></span>

<span data-ttu-id="0d16d-119">Die Syntax für deklarative Konstrukte in der IDL-Datei ähnelt der Syntax für c. in der Mitte werden alle deklarativen Microsoft C/C++-Konstrukte unterstützt, mit Ausnahme der folgenden:</span><span class="sxs-lookup"><span data-stu-id="0d16d-119">The syntax for declarative constructs in the IDL file is similar to that for C. MIDL supports all Microsoft C/C++ declarative constructs except the following:</span></span>

-   <span data-ttu-id="0d16d-120">Ältere typdeklaratoren, die es ermöglichen, dass ein Deklarator ohne Typspezifizierer angegeben wird, z. b.:</span><span class="sxs-lookup"><span data-stu-id="0d16d-120">Older style declarators that allow a declarator to be specified without a type specifier, such as:</span></span>

    ``` syntax
    x (y) 
    short x (y)
    ```

-   <span data-ttu-id="0d16d-121">Deklarationen mit Initialisierern (in der Mitte dürfen nur Deklarationen akzeptiert werden, die der Syntax der [**Konstanten Konstanten**](const.md) entsprechen).</span><span class="sxs-lookup"><span data-stu-id="0d16d-121">Declarations with initializers (MIDL only accepts declarations that conform to the MIDL [**const**](const.md) syntax).</span></span>

<span data-ttu-id="0d16d-122">Das [**Import**](import.md) -Schlüsselwort gibt die Namen von mindestens einer IDL-Datei an, die importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d16d-122">The [**import**](import.md) keyword specifies the names of one or more IDL files to import.</span></span> <span data-ttu-id="0d16d-123">Die Import-Direktive ähnelt der C [**include**](include.md) -Direktive, mit dem Unterschied, dass nur Datentypen in die importierte IDL-Datei aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="0d16d-123">The import directive is similar to the C [**include**](include.md) directive, except that only data types are assimilated into the importing IDL file.</span></span>

## <a name="constant-declaration"></a><span data-ttu-id="0d16d-124">Konstante Deklaration</span><span class="sxs-lookup"><span data-stu-id="0d16d-124">Constant Declaration</span></span>

<span data-ttu-id="0d16d-125">Die Konstante Deklaration gibt [**boolesche**](boolean.md), ganzzahlige, Zeichen-, breit Zeichen-, Zeichen folgen-und **\* void** -Konstanten an.</span><span class="sxs-lookup"><span data-stu-id="0d16d-125">The constant declaration specifies [**Boolean**](boolean.md), integer, character, wide-character, string, and **void \*** constants.</span></span> <span data-ttu-id="0d16d-126">Weitere Informationen finden Sie unter [**konstant**](const.md).</span><span class="sxs-lookup"><span data-stu-id="0d16d-126">For more information, see [**const**](const.md).</span></span>

## <a name="general-declaration"></a><span data-ttu-id="0d16d-127">Allgemeine Deklaration</span><span class="sxs-lookup"><span data-stu-id="0d16d-127">General Declaration</span></span>

<span data-ttu-id="0d16d-128">Eine allgemeine Deklaration ähnelt der C- [**typedef**](typedef.md) -Anweisung mit dem Hinzufügen von IDL-Typattributen.</span><span class="sxs-lookup"><span data-stu-id="0d16d-128">A general declaration is similar to the C [**typedef**](typedef.md) statement with the addition of IDL type attributes.</span></span> <span data-ttu-id="0d16d-129">Mit Ausnahme des [**/OSF**](-osf.md) -Modus ermöglicht der-Mittell-Compiler auch eine implizite Deklaration in Form einer Variablen Definition.</span><span class="sxs-lookup"><span data-stu-id="0d16d-129">Except in [**/osf**](-osf.md) mode, the MIDL compiler also allows an implicit declaration in the form of a variable definition.</span></span>

## <a name="function-declaration"></a><span data-ttu-id="0d16d-130">Funktionsdeklaration</span><span class="sxs-lookup"><span data-stu-id="0d16d-130">Function Declaration</span></span>

<span data-ttu-id="0d16d-131">Der funktionsdeklarator ist ein Sonderfall der allgemeinen Deklaration.</span><span class="sxs-lookup"><span data-stu-id="0d16d-131">The function declarator is a special case of the general declaration.</span></span> <span data-ttu-id="0d16d-132">Sie können IDL-Attribute verwenden, um das Verhalten des Funktions Rückgabe Typs und jedes Parameters anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0d16d-132">You can use IDL attributes to specify the behavior of the function return type and each of the parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="0d16d-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d16d-133">Examples</span></span>

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(3.1), 
    pointer_default(unique) 
] 
interface IdlGrammarExample 
{ 
    import "windows.idl", "other.idl"; 
    const wchar_t * NAME = L"Example Program"; 
    typedef char * PCHAR; 
 
    HRESULT DictCheckSpelling( 
        [in, string] PCHAR   word,     // word to look up 
        [out]        short * isPresent // 0 if not present 
    ); 
}
```

 

 




