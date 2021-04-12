---
title: Importieren von Dateien und Typbibliotheken
description: Mit den mittleren Schlüsselwörtern "include", "Import" und "importlib" können Sie Code wieder verwenden, indem Sie auf vorhandene Header-, IDL-und ODL-Dateien (Object Definition Language) und kompilierte Typbibliotheken verweisen.
ms.assetid: b4571c1d-4bd7-4ab1-9ef6-14356a6c4bb4
keywords:
- Microsoft Interface Definition Language mittlerer l, Aufgaben, Importieren von Dateien und Typbibliotheken
- Importieren der Mittell
- Typbibliotheken, Mittel l, importieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b740f29726c1ce4d401fc69b2ea07e811eac0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104353989"
---
# <a name="importing-files-and-type-libraries"></a><span data-ttu-id="a2ba0-106">Importieren von Dateien und Typbibliotheken</span><span class="sxs-lookup"><span data-stu-id="a2ba0-106">Importing Files and Type Libraries</span></span>

<span data-ttu-id="a2ba0-107">Mit den mittleren Schlüsselwörtern " [**include**](include.md)", " [**Import**](import.md)" und " [**importlib**](importlib.md) " können Sie Code wieder verwenden, indem Sie auf vorhandene Header-, IDL-und ODL-Dateien (Object Definition Language) und kompilierte Typbibliotheken verweisen.</span><span class="sxs-lookup"><span data-stu-id="a2ba0-107">The MIDL keywords [**include**](include.md), [**import**](import.md), and [**importlib**](importlib.md) let you reuse code by referencing existing header, IDL, and object definition language (ODL) files, and compiled type libraries.</span></span>

<span data-ttu-id="a2ba0-108">Mit der ACF [**include**](include.md) -Direktive können Sie in einer ACF-Datei eine oder mehrere C-sprach Header Dateien angeben, die in den in der Mitte generierten Stub-Code eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a2ba0-108">The ACF [**include**](include.md) directive lets you specify in an ACF file one or more C-language header files to be included in the MIDL-generated stub code.</span></span> <span data-ttu-id="a2ba0-109">Die generierte Datei enthält eine Zeile mit einer **\# include** -C-Präprozessordirektive mit der angezeigten Header Datei.</span><span class="sxs-lookup"><span data-stu-id="a2ba0-109">The generated file will have a line with a **\#include** C-preprocessor directive with the indicated header file.</span></span> <span data-ttu-id="a2ba0-110">Verwenden Sie diese **include** -Direktive zum Einbinden von Header Dateien, die für eine bestimmte Betriebsumgebung spezifisch sind und keine Informationen enthalten, die für die Schnittstelle zwischen Client und Server erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a2ba0-110">Use this **include** directive to bring in header files that are specific to a particular operating environment and that do not contain information necessary for the interface between client and server.</span></span> <span data-ttu-id="a2ba0-111">Verwenden Sie **include** nicht für Header Dateien, die Datentypen enthalten, die für die IDL-Datei verfügbar sein sollen. Verwenden Sie stattdessen die [**Import**](import.md) -Direktive.</span><span class="sxs-lookup"><span data-stu-id="a2ba0-111">Do not use **include** for header files containing data types that you want available to the IDL file; instead, use the [**import**](import.md) directive.</span></span>

## <a name="example-1"></a><span data-ttu-id="a2ba0-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a2ba0-112">Example 1</span></span>

``` syntax
[
  auto_handle
] 
interface X86PC
{ 
  include "gendefs.h", "protos.h", "myfile.h"; 
  //interface typdefs and function declarations here
}
```

<span data-ttu-id="a2ba0-113">Die IDL- [**Import**](import.md) Direktive ist die Standardmethode zum Übertragen von Typ-und Schnittstellendefinitionen aus anderen IDL-Dateien (oder ODL-Dateien) und Header Dateien in Ihre IDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="a2ba0-113">The IDL [**import**](import.md) directive is the standard method for bringing type and interface definitions from other IDL (or ODL) files and header files into your IDL file.</span></span> <span data-ttu-id="a2ba0-114">Alle IDL-Anweisungen in der importierten Datei (z. b. Typedefs, [**Konstante Deklarationen**](const.md) und Schnittstellendefinitionen) werden für die importierende IDL-Datei verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a2ba0-114">All IDL statements in the imported file, such as typedefs, [**const**](const.md) declarations, and interface definitions become available to the importing IDL file.</span></span>

<span data-ttu-id="a2ba0-115">Wie bei der Präprozessordirektive der C-Sprache weist die [**Import**](import.md) -Direktive den Compiler **\# an, Daten** Typen einzuschließen, die in den importierten IDL-Dateien definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="a2ba0-115">Like the C-language preprocessor directive **\#include**, the [**import**](import.md) directive tells the compiler to include data types that were defined in the imported IDL files.</span></span> <span data-ttu-id="a2ba0-116">Anders als bei der **\# include** -Direktive ignoriert die **Import** -Direktive Prozedur Prototypen, da für Elemente in der importierten Datei keine Stubdaten generiert werden.</span><span class="sxs-lookup"><span data-stu-id="a2ba0-116">Unlike the **\#include** directive, the **import** directive ignores procedure prototypes, since no stubs are generated for anything in the imported file.</span></span> <span data-ttu-id="a2ba0-117">Da der Präprozessor für die importierte Datei separat aufgerufen wird, werden Präprozessordirektiven (z. b. \* \*) nicht auf die importierende IDL-Datei übertragen.</span><span class="sxs-lookup"><span data-stu-id="a2ba0-117">Because the preprocessor is invoked separately for the imported file, preprocessor directives (such as \*\*) do not carry over to the importing IDL file.</span></span>

<span data-ttu-id="a2ba0-118">Weitere Informationen zur Verwendung von [**Import**](import.md) zum Einschließen von System Header Dateien in eine IDL-Datei finden Sie unter [Importieren von System Header Dateien](importing-system-header-files.md).</span><span class="sxs-lookup"><span data-stu-id="a2ba0-118">For additional information on using [**import**](import.md) to include system header files in an IDL file, see [Importing System Header Files](importing-system-header-files.md).</span></span>

## <a name="example-2"></a><span data-ttu-id="a2ba0-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a2ba0-119">Example 2</span></span>

``` syntax
[
  uuid(. . .), object
] 
interface IKnown : IUnknown
{
  import "base.idl", "unknwn.idl", "helper.idl";
  //remainder of interface definition
}
```

<span data-ttu-id="a2ba0-120">Mit der ODL [**importlib**](importlib.md) -Direktive können Sie in ihrer IDL-oder ODL-Datei auf eine kompilierte Typbibliothek verweisen.</span><span class="sxs-lookup"><span data-stu-id="a2ba0-120">The ODL [**importlib**](importlib.md) directive lets you reference a compiled type library in your IDL or ODL file.</span></span> <span data-ttu-id="a2ba0-121">Die **importlib** -Direktive muss sich in einer [**Library**](library.md) -Anweisung befinden und muss vor anderen Typbeschreibungen in der Bibliothek stehen.</span><span class="sxs-lookup"><span data-stu-id="a2ba0-121">The **importlib** directive must be inside a [**library**](library.md) statement, and must precede other type descriptions in the library.</span></span> <span data-ttu-id="a2ba0-122">Die importierte Bibliothek und die generierte Bibliothek müssen zur Laufzeit für die Anwendung verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="a2ba0-122">The imported library, as well as the generated library, must be available to the application at runtime.</span></span>

## <a name="example-3"></a><span data-ttu-id="a2ba0-123">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a2ba0-123">Example 3</span></span>

``` syntax
library NewBrowser
{
  importlib("stdole32.tlb");
  importlib("legacy.tlb");
  //remainder of library definition
};
```

<span data-ttu-id="a2ba0-124">Sie können auch die C-präprocessor **\# include** -Direktive verwenden, um Header und andere Dateien in Ihre IDL-oder ODL-Datei einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="a2ba0-124">You can also use the C-preprocessor **\#include** directive to include headers and other files in your IDL or ODL file.</span></span> <span data-ttu-id="a2ba0-125">Beachten Sie jedoch, dass diese Direktive den gesamten Inhalt der angegebenen Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="a2ba0-125">Be aware, however, that this directive will literally include the entire contents of the specified file.</span></span> <span data-ttu-id="a2ba0-126">Wenn eine Header Datei Prototypen enthält, die Sie in den von der Mitte generierten Stubdateien nicht benötigen oder verwenden möchten, oder wenn Sie nicht Remote fähige Typdefinitionen enthält, sollten Sie anstelle der **\# include** -Direktive die [**Import**](import.md) Direktive "Mittel l" verwenden.</span><span class="sxs-lookup"><span data-stu-id="a2ba0-126">If a header file contains prototypes that you do not need or want in the MIDL-generated stub files, or if it contains nonremotable type definitions, you should use the MIDL [**import**](import.md) directive instead of the **\#include** directive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2ba0-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a2ba0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2ba0-128">**Importieren**</span><span class="sxs-lookup"><span data-stu-id="a2ba0-128">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="a2ba0-129">**importlib**</span><span class="sxs-lookup"><span data-stu-id="a2ba0-129">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="a2ba0-130">**darunter**</span><span class="sxs-lookup"><span data-stu-id="a2ba0-130">**include**</span></span>](include.md)
</dt> <dt>

[<span data-ttu-id="a2ba0-131">Importieren von System-Headerdateien</span><span class="sxs-lookup"><span data-stu-id="a2ba0-131">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> </dl>

 

 




