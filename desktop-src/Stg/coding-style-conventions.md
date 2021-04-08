---
title: Codierungsstil Konventionen
description: Codierungsstil Konventionen werden in dieser Beispiel Reihe verwendet, um Klarheit und Konsistenz zu gewährleisten.
ms.assetid: d5e81a52-79f6-4561-891c-05fee125a1b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28e65e19d69f060a5f85d86976c4bd3694f7611
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734961"
---
# <a name="coding-style-conventions"></a><span data-ttu-id="df7b9-103">Codierungsstil Konventionen</span><span class="sxs-lookup"><span data-stu-id="df7b9-103">Coding Style Conventions</span></span>

<span data-ttu-id="df7b9-104">Codierungsstil Konventionen werden in dieser Beispiel Reihe verwendet, um Klarheit und Konsistenz zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="df7b9-104">Coding style conventions are used in this sample series to aid clarity and consistency.</span></span> <span data-ttu-id="df7b9-105">Die Konventionen für die "ungarisch"-Notation werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="df7b9-105">The "Hungarian" notation conventions are used.</span></span> <span data-ttu-id="df7b9-106">Diese wurden in der Win32-Programmierung häufig zum Codierungs Verhalten.</span><span class="sxs-lookup"><span data-stu-id="df7b9-106">These have become a common coding practice in Win32 programming.</span></span> <span data-ttu-id="df7b9-107">Sie enthalten Variablen Präfix-Notationen, die Variablennamen einen Vorschlag des Typs der Variablen geben.</span><span class="sxs-lookup"><span data-stu-id="df7b9-107">They include variable prefix notations that give to variable names a suggestion of the type of the variable.</span></span>

<span data-ttu-id="df7b9-108">In der folgenden Tabelle sind allgemeine Präfixe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="df7b9-108">The following table lists common prefixes.</span></span>



| <span data-ttu-id="df7b9-109">Präfix</span><span class="sxs-lookup"><span data-stu-id="df7b9-109">Prefix</span></span> | <span data-ttu-id="df7b9-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df7b9-110">Description</span></span>                         |
|--------|-------------------------------------|
| <span data-ttu-id="df7b9-111">a</span><span class="sxs-lookup"><span data-stu-id="df7b9-111">a</span></span>      | <span data-ttu-id="df7b9-112">Array</span><span class="sxs-lookup"><span data-stu-id="df7b9-112">Array</span></span>                               |
| <span data-ttu-id="df7b9-113">b</span><span class="sxs-lookup"><span data-stu-id="df7b9-113">b</span></span>      | <span data-ttu-id="df7b9-114">Bool (int)</span><span class="sxs-lookup"><span data-stu-id="df7b9-114">BOOL (int)</span></span>                          |
| <span data-ttu-id="df7b9-115">c</span><span class="sxs-lookup"><span data-stu-id="df7b9-115">c</span></span>      | <span data-ttu-id="df7b9-116">Char</span><span class="sxs-lookup"><span data-stu-id="df7b9-116">Char</span></span>                                |
| <span data-ttu-id="df7b9-117">betrieben</span><span class="sxs-lookup"><span data-stu-id="df7b9-117">cb</span></span>     | <span data-ttu-id="df7b9-118">Anzahl von Bytes</span><span class="sxs-lookup"><span data-stu-id="df7b9-118">Count of bytes</span></span>                      |
| <span data-ttu-id="df7b9-119">cr</span><span class="sxs-lookup"><span data-stu-id="df7b9-119">cr</span></span>     | <span data-ttu-id="df7b9-120">Farb Verweis Wert</span><span class="sxs-lookup"><span data-stu-id="df7b9-120">Color reference value</span></span>               |
| <span data-ttu-id="df7b9-121">verschoben</span><span class="sxs-lookup"><span data-stu-id="df7b9-121">cx</span></span>     | <span data-ttu-id="df7b9-122">Anzahl von x (Short)</span><span class="sxs-lookup"><span data-stu-id="df7b9-122">Count of x (short)</span></span>                  |
| <span data-ttu-id="df7b9-123">dw</span><span class="sxs-lookup"><span data-stu-id="df7b9-123">dw</span></span>     | <span data-ttu-id="df7b9-124">DWORD (unsigned long)</span><span class="sxs-lookup"><span data-stu-id="df7b9-124">DWORD (unsigned long)</span></span>               |
| <span data-ttu-id="df7b9-125">f</span><span class="sxs-lookup"><span data-stu-id="df7b9-125">f</span></span>      | <span data-ttu-id="df7b9-126">Flags (in der Regel mehrere Bitwerte)</span><span class="sxs-lookup"><span data-stu-id="df7b9-126">Flags (usually multiple bit values)</span></span> |
| <span data-ttu-id="df7b9-127">fn</span><span class="sxs-lookup"><span data-stu-id="df7b9-127">fn</span></span>     | <span data-ttu-id="df7b9-128">Funktion</span><span class="sxs-lookup"><span data-stu-id="df7b9-128">Function</span></span>                            |
| <span data-ttu-id="df7b9-129">selbst\_</span><span class="sxs-lookup"><span data-stu-id="df7b9-129">g\_</span></span>    | <span data-ttu-id="df7b9-130">Global</span><span class="sxs-lookup"><span data-stu-id="df7b9-130">Global</span></span>                              |
| <span data-ttu-id="df7b9-131">h.</span><span class="sxs-lookup"><span data-stu-id="df7b9-131">h</span></span>      | <span data-ttu-id="df7b9-132">Handle</span><span class="sxs-lookup"><span data-stu-id="df7b9-132">Handle</span></span>                              |
| <span data-ttu-id="df7b9-133">i</span><span class="sxs-lookup"><span data-stu-id="df7b9-133">i</span></span>      | <span data-ttu-id="df7b9-134">Integer</span><span class="sxs-lookup"><span data-stu-id="df7b9-134">Integer</span></span>                             |
| <span data-ttu-id="df7b9-135">l</span><span class="sxs-lookup"><span data-stu-id="df7b9-135">l</span></span>      | <span data-ttu-id="df7b9-136">Long</span><span class="sxs-lookup"><span data-stu-id="df7b9-136">Long</span></span>                                |
| <span data-ttu-id="df7b9-137">lp</span><span class="sxs-lookup"><span data-stu-id="df7b9-137">lp</span></span>     | <span data-ttu-id="df7b9-138">Long-Zeiger</span><span class="sxs-lookup"><span data-stu-id="df7b9-138">Long pointer</span></span>                        |
| <span data-ttu-id="df7b9-139">800\_</span><span class="sxs-lookup"><span data-stu-id="df7b9-139">m\_</span></span>    | <span data-ttu-id="df7b9-140">Datenmember einer Klasse</span><span class="sxs-lookup"><span data-stu-id="df7b9-140">Data member of a class</span></span>              |
| <span data-ttu-id="df7b9-141">n</span><span class="sxs-lookup"><span data-stu-id="df7b9-141">n</span></span>      | <span data-ttu-id="df7b9-142">Short int</span><span class="sxs-lookup"><span data-stu-id="df7b9-142">Short int</span></span>                           |
| <span data-ttu-id="df7b9-143">p</span><span class="sxs-lookup"><span data-stu-id="df7b9-143">p</span></span>      | <span data-ttu-id="df7b9-144">Zeiger</span><span class="sxs-lookup"><span data-stu-id="df7b9-144">Pointer</span></span>                             |
| <span data-ttu-id="df7b9-145">s</span><span class="sxs-lookup"><span data-stu-id="df7b9-145">s</span></span>      | <span data-ttu-id="df7b9-146">String</span><span class="sxs-lookup"><span data-stu-id="df7b9-146">String</span></span>                              |
| <span data-ttu-id="df7b9-147">sz</span><span class="sxs-lookup"><span data-stu-id="df7b9-147">sz</span></span>     | <span data-ttu-id="df7b9-148">NULL beendete Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="df7b9-148">Zero terminated String</span></span>              |
| <span data-ttu-id="df7b9-149">tm</span><span class="sxs-lookup"><span data-stu-id="df7b9-149">tm</span></span>     | <span data-ttu-id="df7b9-150">Textmetrik</span><span class="sxs-lookup"><span data-stu-id="df7b9-150">Text metric</span></span>                         |
| <span data-ttu-id="df7b9-151">u</span><span class="sxs-lookup"><span data-stu-id="df7b9-151">u</span></span>      | <span data-ttu-id="df7b9-152">Unsigned int</span><span class="sxs-lookup"><span data-stu-id="df7b9-152">Unsigned int</span></span>                        |
| <span data-ttu-id="df7b9-153">nützlichen</span><span class="sxs-lookup"><span data-stu-id="df7b9-153">ul</span></span>     | <span data-ttu-id="df7b9-154">Unsigned long (ULONG)</span><span class="sxs-lookup"><span data-stu-id="df7b9-154">Unsigned long (ULONG)</span></span>               |
| <span data-ttu-id="df7b9-155">w</span><span class="sxs-lookup"><span data-stu-id="df7b9-155">w</span></span>      | <span data-ttu-id="df7b9-156">Word (kurz ohne Vorzeichen)</span><span class="sxs-lookup"><span data-stu-id="df7b9-156">WORD (unsigned short)</span></span>               |
| <span data-ttu-id="df7b9-157">x, y</span><span class="sxs-lookup"><span data-stu-id="df7b9-157">x,y</span></span>    | <span data-ttu-id="df7b9-158">x, y-Koordinaten (kurz)</span><span class="sxs-lookup"><span data-stu-id="df7b9-158">x, y coordinates (short)</span></span>            |



 

<span data-ttu-id="df7b9-159">Diese werden häufig kombiniert, wie im folgenden.</span><span class="sxs-lookup"><span data-stu-id="df7b9-159">These are often combined, as in the following.</span></span>



| <span data-ttu-id="df7b9-160">Präfix Kombination</span><span class="sxs-lookup"><span data-stu-id="df7b9-160">Prefix combination</span></span> | <span data-ttu-id="df7b9-161">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df7b9-161">Description</span></span>                                             |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="df7b9-162">pszmystring</span><span class="sxs-lookup"><span data-stu-id="df7b9-162">pszMyString</span></span>        | <span data-ttu-id="df7b9-163">Ein Zeiger auf eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="df7b9-163">A pointer to a string.</span></span>                                  |
| <span data-ttu-id="df7b9-164">m \_ pszmystring</span><span class="sxs-lookup"><span data-stu-id="df7b9-164">m\_pszMyString</span></span>     | <span data-ttu-id="df7b9-165">Ein Zeiger auf eine Zeichenfolge, die ein Datenmember einer Klasse ist.</span><span class="sxs-lookup"><span data-stu-id="df7b9-165">A pointer to a string that is a data member of a class.</span></span> |



 

<span data-ttu-id="df7b9-166">In der folgenden Tabelle sind andere Konventionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="df7b9-166">Other conventions are listed in the following table.</span></span>



| <span data-ttu-id="df7b9-167">Konvention</span><span class="sxs-lookup"><span data-stu-id="df7b9-167">Convention</span></span>       | <span data-ttu-id="df7b9-168">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df7b9-168">Description</span></span>                                              |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="df7b9-169">CMyClass</span><span class="sxs-lookup"><span data-stu-id="df7b9-169">CMyClass</span></span>         | <span data-ttu-id="df7b9-170">Präfix "C" für C++-Klassennamen.</span><span class="sxs-lookup"><span data-stu-id="df7b9-170">Prefix 'C' for C++ class names.</span></span>                          |
| <span data-ttu-id="df7b9-171">Comyobjectclass</span><span class="sxs-lookup"><span data-stu-id="df7b9-171">COMyObjectClass</span></span>  | <span data-ttu-id="df7b9-172">Präfix ' Co ' für COM-Objektklassen Namen.</span><span class="sxs-lookup"><span data-stu-id="df7b9-172">Prefix 'CO' for COM object class names.</span></span>                  |
| <span data-ttu-id="df7b9-173">Cfmyclassfactory</span><span class="sxs-lookup"><span data-stu-id="df7b9-173">CFMyClassFactory</span></span> | <span data-ttu-id="df7b9-174">Präfix ' CF ' für com-klassenfactorynamen.</span><span class="sxs-lookup"><span data-stu-id="df7b9-174">Prefix 'CF' for COM class factory names.</span></span>                 |
| <span data-ttu-id="df7b9-175">Imeineschnittstelle</span><span class="sxs-lookup"><span data-stu-id="df7b9-175">IMyInterface</span></span>     | <span data-ttu-id="df7b9-176">Präfix "I" für Namen der COM-Schnittstellen Klasse.</span><span class="sxs-lookup"><span data-stu-id="df7b9-176">Prefix 'I' for COM interface class names.</span></span>                |
| <span data-ttu-id="df7b9-177">Cimpimyinterface</span><span class="sxs-lookup"><span data-stu-id="df7b9-177">CImpIMyInterface</span></span> | <span data-ttu-id="df7b9-178">Präfix ' cimpi ' für Implementierungsklassen der COM-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="df7b9-178">Prefix 'CImpI' for COM interface implementation classes.</span></span> |



 

<span data-ttu-id="df7b9-179">Einige konsistente Konventionen für Kommentar Header Blöcke werden wie folgt in dieser Beispiel Reihe verwendet.</span><span class="sxs-lookup"><span data-stu-id="df7b9-179">Some consistent conventions for comment header blocks are used in this sample series as follows.</span></span>

## <a name="file-header"></a><span data-ttu-id="df7b9-180">Datei Header</span><span class="sxs-lookup"><span data-stu-id="df7b9-180">File Header</span></span>

``` syntax
/*+===================================================================
  File:      MYFILE.EXT

  Summary:   Brief summary of the file contents and purpose.

  Classes:   Classes declared or used (in source files).

  Functions: Functions exported (in source files).

  Origin:    Indications of where content may have come from. This
             is not a change history but rather a reference to the
             editor-inheritance behind the content or other
             indications about the origin of the source.

  Copyright and Legal notices.
  Copyright and Legal notices.
===================================================================+*/
```

## <a name="plain-comment-block"></a><span data-ttu-id="df7b9-181">Block "Plain comment"</span><span class="sxs-lookup"><span data-stu-id="df7b9-181">Plain Comment Block</span></span>

``` syntax
/*--------------------------------------------------------------------
  Plain block of comment text that usually takes several lines.
  Plain block of comment text that usually takes several lines.
--------------------------------------------------------------------*/
```

## <a name="class-declaration-header"></a><span data-ttu-id="df7b9-182">Klassen Deklarations Header</span><span class="sxs-lookup"><span data-stu-id="df7b9-182">Class Declaration Header</span></span>

``` syntax
/*C+C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C
  Class:    CMyClass

  Summary:  Short summary of purpose and content of CMyClass.
            Short summary of purpose and content of CMyClass.

  Methods:  MyMethodOne
              Short description of MyMethodOne.
            MyMethodTwo
              Short description of MyMethodTwo.
            CMyClass
              Constructor.
            ~CMyClass
              Destructor.
C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C-C*/
```

## <a name="class-method-definition-header"></a><span data-ttu-id="df7b9-183">Klassen Methoden-Definitions Header</span><span class="sxs-lookup"><span data-stu-id="df7b9-183">Class Method Definition Header</span></span>

``` syntax
/*M+M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M
  Method:   CMyClass::MyMethodOne

  Summary:  Short summary of purpose and content of MyMethodOne.
            Short summary of purpose and content of MyMethodOne.

  Args:     MYTYPE MyArgOne
              Short description of argument MyArgOne.
            MYTYPE MyArgTwo
              Short description of argument MyArgTwo.

  Modifies: [list of member data variables modified by this method].

  Returns:  MYRETURNTYPE
              Short description of meaning of the return type values.
M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M-M*/
```

## <a name="unexported-or-local-function"></a><span data-ttu-id="df7b9-184">Nicht exportierte oder lokale Funktion</span><span class="sxs-lookup"><span data-stu-id="df7b9-184">Unexported or Local Function</span></span>

``` syntax
/*F+F+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
  Function: MyLocalFunction

  Summary:  What MyLocalFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
-----------------------------------------------------------------F-F*/
```

## <a name="exported-function-definition-header"></a><span data-ttu-id="df7b9-185">Definitions Header der exportierten Funktion</span><span class="sxs-lookup"><span data-stu-id="df7b9-185">Exported Function Definition Header</span></span>

``` syntax
/*F+F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F
  Function: MyFunction

  Summary:  What MyFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F-F*/
```

## <a name="com-interface-declaration-header"></a><span data-ttu-id="df7b9-186">Deklaration der COM-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="df7b9-186">COM Interface Declaration Header</span></span>

``` syntax
/*I+I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I
  Interface: IMyInterface

  Summary:   Short summary of what features the interface can bring to
             a COM Component.

  Methods:   MYTYPE MyMethodOne
               Description.
             MYTYPE MyMethodTwo
               Description.
I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I-I*/
```

## <a name="com-object-class-declaration-header"></a><span data-ttu-id="df7b9-187">COM-Objektklassen Deklarations Header</span><span class="sxs-lookup"><span data-stu-id="df7b9-187">COM Object Class Declaration Header</span></span>

``` syntax
/*O+O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O
  ObjectClass: COMyCOMObject

  Summary:     Short summary of purpose and content of this object.

  Interfaces:  IUnknown
                 Standard interface providing COM object features.
               IMyInterfaceOne
                 Description.
               IMyInterfaceTwo
                 Description.

  Aggregation: [whether this COM Object is aggregatable or not]
O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O-O*/
```

<span data-ttu-id="df7b9-188">Alle diese Kommentar Block Konventionen haben konsistente Anfangs-und Endtoken-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="df7b9-188">All of these comment block conventions have consistent beginning and ending token strings.</span></span> <span data-ttu-id="df7b9-189">Diese Konsistenz unterstützt die automatische Verarbeitung der Header auf irgendeine Weise.</span><span class="sxs-lookup"><span data-stu-id="df7b9-189">This consistency supports automatic processing of the headers in some fashion.</span></span> <span data-ttu-id="df7b9-190">Beispielsweise können awk-Skripts geschrieben werden, um die Funktions Header in eine separate Textdatei zu filtern, die als Grundlage für ein Spezifikationsdokument dienen kann.</span><span class="sxs-lookup"><span data-stu-id="df7b9-190">For example, AWK scripts can be written to filter the function headers into a separate text file that can then serve as the basis for a specification document.</span></span> <span data-ttu-id="df7b9-191">Ebenso können Tools wie das nicht unterstützte autoduck-Hilfsprogramm (zurzeit auf der Microsoft Developer Network Development Library-CD-ROM verfügbar) zum Verarbeiten der Kommentar Blöcke in diesen Headern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df7b9-191">Similarly, tools like the unsupported AUTODUCK utility (currently available on the Microsoft Developer Network Development Library CD-ROM) can be used to process the comment blocks in these headers.</span></span>

<span data-ttu-id="df7b9-192">In der folgenden Tabelle werden die in Beispiel Lernprogrammen verwendeten Zeichen folgen für den Anfang und das Beenden aufgeführt</span><span class="sxs-lookup"><span data-stu-id="df7b9-192">The following table lists beginning and ending token strings used in sample tutorials.</span></span>



| <span data-ttu-id="df7b9-193">Token</span><span class="sxs-lookup"><span data-stu-id="df7b9-193">Token</span></span> | <span data-ttu-id="df7b9-194">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df7b9-194">Description</span></span>                      |
|-------|----------------------------------|
| /\*+  | <span data-ttu-id="df7b9-195">Datei Header Anfang</span><span class="sxs-lookup"><span data-stu-id="df7b9-195">File Header Begin</span></span>                |
| +\*/  | <span data-ttu-id="df7b9-196">Datei Header Ende</span><span class="sxs-lookup"><span data-stu-id="df7b9-196">File Header End</span></span>                  |
| /\*-  | <span data-ttu-id="df7b9-197">Anfang der Block Kopfzeile für Klartext</span><span class="sxs-lookup"><span data-stu-id="df7b9-197">Plain comment block Header Begin</span></span> |
| -\*/  | <span data-ttu-id="df7b9-198">Ende der Block Kopfzeile des Plain comment</span><span class="sxs-lookup"><span data-stu-id="df7b9-198">Plain comment block Header End</span></span>   |
| <span data-ttu-id="df7b9-199">/\*Scher</span><span class="sxs-lookup"><span data-stu-id="df7b9-199">/\*C</span></span>  | <span data-ttu-id="df7b9-200">Klassen Header Anfang</span><span class="sxs-lookup"><span data-stu-id="df7b9-200">Class Header Begin</span></span>               |
| <span data-ttu-id="df7b9-201">Scher\*/</span><span class="sxs-lookup"><span data-stu-id="df7b9-201">C\*/</span></span>  | <span data-ttu-id="df7b9-202">Header Ende der Klasse</span><span class="sxs-lookup"><span data-stu-id="df7b9-202">Class Header End</span></span>                 |
| <span data-ttu-id="df7b9-203">/\*800</span><span class="sxs-lookup"><span data-stu-id="df7b9-203">/\*M</span></span>  | <span data-ttu-id="df7b9-204">Methoden Header Anfang</span><span class="sxs-lookup"><span data-stu-id="df7b9-204">Method Header Begin</span></span>              |
| <span data-ttu-id="df7b9-205">800\*/</span><span class="sxs-lookup"><span data-stu-id="df7b9-205">M\*/</span></span>  | <span data-ttu-id="df7b9-206">Methoden Header Ende</span><span class="sxs-lookup"><span data-stu-id="df7b9-206">Method Header End</span></span>                |
| <span data-ttu-id="df7b9-207">/\*C</span><span class="sxs-lookup"><span data-stu-id="df7b9-207">/\*F</span></span>  | <span data-ttu-id="df7b9-208">Funktions Header Anfang</span><span class="sxs-lookup"><span data-stu-id="df7b9-208">Function Header Begin</span></span>            |
| <span data-ttu-id="df7b9-209">C\*/</span><span class="sxs-lookup"><span data-stu-id="df7b9-209">F\*/</span></span>  | <span data-ttu-id="df7b9-210">Funktions Header Ende</span><span class="sxs-lookup"><span data-stu-id="df7b9-210">Function Header End</span></span>              |
| <span data-ttu-id="df7b9-211">/\*Ich</span><span class="sxs-lookup"><span data-stu-id="df7b9-211">/\*I</span></span>  | <span data-ttu-id="df7b9-212">Schnittstellen-Header Anfang</span><span class="sxs-lookup"><span data-stu-id="df7b9-212">Interface Header Begin</span></span>           |
| <span data-ttu-id="df7b9-213">Ich\*/</span><span class="sxs-lookup"><span data-stu-id="df7b9-213">I\*/</span></span>  | <span data-ttu-id="df7b9-214">Schnittstellen-Header Ende</span><span class="sxs-lookup"><span data-stu-id="df7b9-214">Interface Header End</span></span>             |
| <span data-ttu-id="df7b9-215">/\*'</span><span class="sxs-lookup"><span data-stu-id="df7b9-215">/\*O</span></span>  | <span data-ttu-id="df7b9-216">Anfang der com-Objektklassen Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="df7b9-216">COM Object Class Header Begin</span></span>    |
| <span data-ttu-id="df7b9-217">'\*/</span><span class="sxs-lookup"><span data-stu-id="df7b9-217">O\*/</span></span>  | <span data-ttu-id="df7b9-218">Header Ende der com-Objektklasse</span><span class="sxs-lookup"><span data-stu-id="df7b9-218">COM Object Class Header End</span></span>      |



 

<span data-ttu-id="df7b9-219">Diese Header können auch als visuelle Hinweise für das schnelle Scannen von Quelldateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df7b9-219">These headers can also be used as visual cues for rapid scanning of source files.</span></span> <span data-ttu-id="df7b9-220">Außerdem bieten Sie Ihnen die Möglichkeit, schnell zu einem Quell Speicherort zu gelangen, wenn Sie Such Zeichenfolgen in Ihrem Editor einrichten und dann "Letzte Suche" wiederholen, um diese Header schnell zu finden.</span><span class="sxs-lookup"><span data-stu-id="df7b9-220">They also provide convenience for rapidly getting to some source location if you set up search strings in your editor and then 'repeat last search' to quickly locate these headers.</span></span>

<span data-ttu-id="df7b9-221">Die Such Zeichenfolge "m + M" findet z. b. den Anfang von Methoden Headern, und "m-m" findet den Anfang des tatsächlichen Methoden Definitions-/Implementierungs Codes.</span><span class="sxs-lookup"><span data-stu-id="df7b9-221">For example, the search string "M+M" will locate the start of method headers, and "M-M" will locate the beginning of the actual method definition/implementation code.</span></span>

 

 




