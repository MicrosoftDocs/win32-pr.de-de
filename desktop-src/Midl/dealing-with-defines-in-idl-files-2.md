---
title: Umgang mit Definitionen in IDL-Dateien
description: Auf dieser Seite wird beschrieben, warum Symbole, die mit "\ define" definiert sind, aus den von dem Mittelwert generierten H-Dateien verschwinden und welche Aktionen damit durchgeführt werden können. Diese Erläuterung gilt für alle Dateien, die von der mittleren l verarbeitet werden, z. b. \. idl, \. ACF, \. h-Dateien.
ms.assetid: 148dabda-96cc-4f7c-abc7-4bf78ac166ea
keywords:
- Mittlerer l-compilermittell, Umgang mit Definitionen
- definiert die mittlere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4af77979824c2e76352d6f28bef72161249845d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036918"
---
# <a name="dealing-with-defines-in-idl-files"></a><span data-ttu-id="06f46-106">Umgang mit \# Definitionen in IDL-Dateien</span><span class="sxs-lookup"><span data-stu-id="06f46-106">Dealing with \#defines in IDL Files</span></span>

<span data-ttu-id="06f46-107">Auf dieser Seite wird beschrieben, warum Symbole, die mit einer **\# Definition** definiert sind, aus den von dem Mittelwert generierten H-Dateien verschwinden und welche Aktionen damit durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="06f46-107">This page describes why symbols defined with a **\#define** disappear from the MIDL compiler generated H files, and what can be done about it.</span></span> <span data-ttu-id="06f46-108">Diese Erläuterung gilt für alle Dateien, die von der mittleren l verarbeitet werden, z. b. \* IDL-, \* ACF-und \* h-Dateien.</span><span class="sxs-lookup"><span data-stu-id="06f46-108">This explanation applies to any files processed by MIDL, such as \*.idl, \*.acf, \*.h files.</span></span>

<span data-ttu-id="06f46-109">Das Verschwinden von **\# definierenden** Symbolen ist das Ergebnis der Mittell, die die Vorverarbeitung von Eingabedateien an einen Präprozessor delegiert.</span><span class="sxs-lookup"><span data-stu-id="06f46-109">The disappearance of **\#define** symbols is a result of MIDL delegating the preprocessing of input files to a preprocessor.</span></span> <span data-ttu-id="06f46-110">Standardmäßig ist der Präprozessor ein C/C++-Präprozessor aus der Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="06f46-110">By default, the preprocessor is a C/C++ preprocessor from the build environment.</span></span> <span data-ttu-id="06f46-111">Nach der Vorverarbeitung weist der Eingabestream-Mittell-Empfang nur \# Zeilen Präprozessordirektiven auf.</span><span class="sxs-lookup"><span data-stu-id="06f46-111">After preprocessing, the input stream MIDL receives has only \#line preprocessor directives.</span></span> <span data-ttu-id="06f46-112">Insbesondere wird der Präprozessor alle Makro Definitionen in Eingabedateien aufhebt, sodass die Anwesenheit von der mittleren l nicht erkannt werden kann.</span><span class="sxs-lookup"><span data-stu-id="06f46-112">In particular, the preprocessor unrolls all macro definitions in input files, and therefore, MIDL cannot detect their presence.</span></span> <span data-ttu-id="06f46-113">Folglich werden die Definitionen nicht repliziert, wenn die-Klasse Typdefinitionen aus einer Eingabedatei in die generierte H-Datei repliziert \# .</span><span class="sxs-lookup"><span data-stu-id="06f46-113">Consequently, when MIDL replicates type definitions from an input file to the generated H file, the \#defines are not replicated.</span></span> <span data-ttu-id="06f46-114">Verwenden Sie daher keine \# direkt in IDL-Dateien definierten Definitionen, wenn diese später aus der generierten H-Datei verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="06f46-114">Therefore, do not use \#defines directly in IDL files if they are to be used later from the generated H file.</span></span>

<span data-ttu-id="06f46-115">Die folgenden vier Problem Umgehungen werden empfohlen:</span><span class="sxs-lookup"><span data-stu-id="06f46-115">The following four workarounds are recommended:</span></span>

-   <span data-ttu-id="06f46-116">Verwenden Sie [**die Konstante**](const.md) Deklaration.</span><span class="sxs-lookup"><span data-stu-id="06f46-116">Use the [**const**](const.md) declaration specification.</span></span>
-   <span data-ttu-id="06f46-117">Verwenden Sie separate Header Dateien, die importiert oder in die IDL-Datei eingeschlossen werden und später in den C-Quellcode eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="06f46-117">Use separate header files that are imported or included in the IDL file, and later included in the C-source code.</span></span>
-   <span data-ttu-id="06f46-118">Verwenden Sie Enumerationskonstanten in der IDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="06f46-118">Use enumeration constants in the IDL file.</span></span>
-   <span data-ttu-id="06f46-119">Verwenden Sie das [**cpp- \_ Zitat**](cpp-quote.md) , um die **\# Definition** in der generierten Header Datei zu reproduzieren.</span><span class="sxs-lookup"><span data-stu-id="06f46-119">Use [**cpp\_quote**](cpp-quote.md) to reproduce **\#define** in the generated header file.</span></span>

<span data-ttu-id="06f46-120">Sie können manifestresskonstanten mithilfe der **IDL-Konstante Deklaration** reproduzieren.</span><span class="sxs-lookup"><span data-stu-id="06f46-120">You can reproduce manifest constants using the **IDL constant-declaration syntax**.</span></span> <span data-ttu-id="06f46-121">Beachten Sie, dass die [**Konstante in der**](const.md) IDL-Konstantendeklaration von der C **/C++-Konstanten** Semantik abweicht und einfach eine benannte Konstante für eine IDL-Kompilierung einführt.</span><span class="sxs-lookup"><span data-stu-id="06f46-121">Note that the [**const**](const.md) in the IDL constant-declaration is different from C/C++ **const** semantics, and simply introduces a named constant for an IDL compilation.</span></span> <span data-ttu-id="06f46-122">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="06f46-122">For example:</span></span>

``` syntax
const short ARRSIZE = 10
```

<span data-ttu-id="06f46-123">In diesem Beispiel wird angegeben, dass " **arrsize** " eine Konstante mit dem Wert "10" ist.</span><span class="sxs-lookup"><span data-stu-id="06f46-123">This example specifies that **ARRSIZE** is a constant with a value of 10.</span></span> <span data-ttu-id="06f46-124">Benannte Konstanten können in IDL-Array Deklaratoren und an anderen Stellen verwendet werden, an denen ein C-Programmierer ein Manifest definiert.</span><span class="sxs-lookup"><span data-stu-id="06f46-124">Named constants can be used in IDL array declarators and other places where a C programmer would use a manifest defines.</span></span> <span data-ttu-id="06f46-125">Außerdem führt diese Syntax dazu, dass die folgende Zeile in der Header Datei generiert wird:</span><span class="sxs-lookup"><span data-stu-id="06f46-125">In addition, this syntax results in the following line being generated in the header file:</span></span>

``` syntax
#define ARRSIZE 10
```

<span data-ttu-id="06f46-126">Eine andere Möglichkeit zur Behandlung von **\#** define-Anweisungen besteht darin, Sie in einer separaten Header Datei zu packen, entweder in einer Datei, **\#** die zum Definieren von Anweisungen oder in einer Datei mit nur Typdefinitionen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="06f46-126">Another way to handle **\#** define statements is to package them in a separate header file, either into a file devoted to **\#** define statements or into a file that contains only type definitions.</span></span> <span data-ttu-id="06f46-127">Eine Datei, die nur Präprozessordirektiven enthält, kann sowohl von der IDL-Datei als auch von den C-Quelldateien sicher eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="06f46-127">A file that contains only preprocessor directives may be safely included both by the IDL file and the C-source files.</span></span> <span data-ttu-id="06f46-128">Obwohl die-Direktiven nicht in der vom Mittel l-Compiler generierten Header Datei verfügbar sind, kann das C-Source-Programm die separate Header Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="06f46-128">Although the directives will not be available in the header file generated by the MIDL compiler, the C-source program can include the separate header file.</span></span> <span data-ttu-id="06f46-129">Auf ähnliche Weise kann eine Header Datei mit **\#** define-Anweisungen und regulären Typdefinitionen aus der IDL-Datei importiert werden.</span><span class="sxs-lookup"><span data-stu-id="06f46-129">In a similar fashion, a header file with **\#** define statements and regular type definitions can be imported from your IDL file.</span></span> <span data-ttu-id="06f46-130">Bei diesem Ansatz werden die **\#** define-und typedef-Anweisungen in einer H-Datei eingeschlossen, sodass die **\#** definierenden Symbole nicht direkt in der importierten IDL-Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06f46-130">This approach encapsulates the **\#** define and typedef statements by using them in an H file such that the **\#** define symbols are not used in the importing IDL file directly.</span></span> <span data-ttu-id="06f46-131">Durch das Importieren einer Header-oder IDL-Datei in eine andere IDL-Datei wird verhindert, dass die typedef-Anweisungen in die von "Mittel l" generierte H-Datei repliziert werden (im Gegensatz zu **\#** include-Anweisungen).</span><span class="sxs-lookup"><span data-stu-id="06f46-131">Importing a header or IDL file to another IDL file prevents the typedef statements from being replicated to the H file generated by MIDL (which is in contrast to **\#** include statements).</span></span> <span data-ttu-id="06f46-132">Dieser Ansatz ermöglicht, dass die ursprüngliche Header Datei auf sichere Weise aus dem C-Code entlang der generierten H-Datei referenziert werden kann, ohne dass ein Problem mit duplizierten Definitionen vorliegt.</span><span class="sxs-lookup"><span data-stu-id="06f46-132">This approach allows the original header file to be safely referenced from the C code along the generated H file without having a problem with duplicated definitions.</span></span>

<span data-ttu-id="06f46-133">Die Verwendung von Enumerationskonstanten in der IDL-Datei ist ebenfalls effektiv.</span><span class="sxs-lookup"><span data-stu-id="06f46-133">Use of enumeration constants in the IDL file is also effective.</span></span> <span data-ttu-id="06f46-134">Diese Konstanten können in konstanten Ausdrücken in IDL verwendet werden, z. b. in arraydeklaratoren.</span><span class="sxs-lookup"><span data-stu-id="06f46-134">These constants can be used in constant expressions in IDL, for example, in array declarators.</span></span> <span data-ttu-id="06f46-135">Enumerationskonstanten werden in den frühen Phasen der mittleren Kompilierung durch den C-Compiler-Präprozessor nicht entfernt, sodass Enumerationskonstanten in der vom Mittelwert Compiler generierten Header Datei verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="06f46-135">Enumeration constants are not removed during the early phases of MIDL compilation by the C-compiler preprocessor, so enumeration constants are available in the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="06f46-136">Betrachten Sie folgende Anweisung:</span><span class="sxs-lookup"><span data-stu-id="06f46-136">Consider the following statement:</span></span>

``` syntax
typedef enum midlworkaround { MAXSTRINGCOUNT = 300 };
```

<span data-ttu-id="06f46-137">Diese Anweisung wird nicht während der Kompilierungs Kompilierung durch den C-Präprozessor entfernt, und die typedef wird in die generierte H-Datei repliziert.</span><span class="sxs-lookup"><span data-stu-id="06f46-137">This statement will not be removed during MIDL compilation by the C preprocessor and the typedef will be replicated to the generated H file.</span></span> <span data-ttu-id="06f46-138">Die Konstante maxstringcount ist für C-Quell Programme verfügbar, die die vom Mittelwert Compiler generierte Header Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="06f46-138">The constant MAXSTRINGCOUNT is available to C-source programs that include the header file generated by the MIDL compiler.</span></span>

<span data-ttu-id="06f46-139">Schließlich kann die [**cpp- \_ Zitat**](cpp-quote.md) Anweisung von "Mittel l" verwendet werden, um eine beliebige Zeichenfolge direkt in die generierte H-Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="06f46-139">Finally, the [**cpp\_quote**](cpp-quote.md) directive of MIDL can be used to write out an arbitrary string directly into the generated H file.</span></span> <span data-ttu-id="06f46-140">Um beispielsweise die Manifestressource zu erhalten, die zuvor auf dieser Seite mit **cpp- \_ Anführungs** Zeichen verwendet wurde, kann die folgende Anweisung verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="06f46-140">For example, to get the manifest constant used previously on this page with **cpp\_quote**, the following statement can be used:</span></span>

``` syntax
cpp_quote ("#define ARRSIZE 10")
```

<span data-ttu-id="06f46-141">Diese Anweisung führt dazu, dass die folgende Zeile in der Header Datei generiert wird:</span><span class="sxs-lookup"><span data-stu-id="06f46-141">This statement results in the following line being generated in the header file:</span></span>

``` syntax
#define ARRSIZE 10
```

 

 




