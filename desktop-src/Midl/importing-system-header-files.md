---
title: Importieren von System-Headerdateien
description: Obwohl es häufig möglich ist, die \ include-Direktive zum Einschließen von Header Dateien in Ihre IDL-Datei zu verwenden, wird dies nicht empfohlen.
ms.assetid: ff524965-424d-416d-97cd-c2780ebf69ef
keywords:
- Importieren von mittlerer l-, System Header Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26df7ca983fa21ae8e604446f0221c302c73099
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761589"
---
# <a name="importing-system-header-files"></a><span data-ttu-id="2a5e4-104">Importieren von System-Headerdateien</span><span class="sxs-lookup"><span data-stu-id="2a5e4-104">Importing System Header Files</span></span>

<span data-ttu-id="2a5e4-105">Obwohl es häufig möglich ist, die **\# include** -Direktive zum Einschließen von Header Dateien in Ihre IDL-Datei zu verwenden, wird dies nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="2a5e4-105">While it is often possible to use the **\#include** directive to include header files in your IDL file, it is not recommended.</span></span> <span data-ttu-id="2a5e4-106">Der mittlerer l-Compiler generiert stubvorgänge für alle Funktionen, die in der zu kompilierende IDL-Datei definiert sind.</span><span class="sxs-lookup"><span data-stu-id="2a5e4-106">The MIDL compiler will generate stubs for all functions defined in the IDL file being compiled.</span></span> <span data-ttu-id="2a5e4-107">In der Regel enthält eine Header Datei eine Reihe von Prototypen, die Sie weder benötigen noch in die Stubdateien einschließen möchten, und ein **\# include** -Element fügt diese Definitionen effektiv in Ihre Haupt-IDL-Datei ein.</span><span class="sxs-lookup"><span data-stu-id="2a5e4-107">Usually a header file contains a number of prototypes that you neither need nor want to include in your stub files, and a **\#include** effectively puts all those definitions into your main IDL file.</span></span> <span data-ttu-id="2a5e4-108">Wenn außerdem nicht Remote fähige Typen in der Header Datei definiert sind, wird die IDL-Datei möglicherweise nicht kompiliert.</span><span class="sxs-lookup"><span data-stu-id="2a5e4-108">Furthermore, if there are nonremotable types defined in the header file, the IDL file may not compile.</span></span>

<span data-ttu-id="2a5e4-109">Es gibt zwei Möglichkeiten, Typdefinitionen aus Header Dateien in eine IDL-Datei einzubeziehen:</span><span class="sxs-lookup"><span data-stu-id="2a5e4-109">There are two ways to include type definitions from header files in an IDL file:</span></span>

-   <span data-ttu-id="2a5e4-110">Verwenden Sie die [**Import**](import.md) -Direktive, um in eine Header Datei definierte Datentypen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="2a5e4-110">Use the [**import**](import.md) directive to include data types defined in a header file.</span></span> <span data-ttu-id="2a5e4-111">Anders als bei der **\# include** -Direktive der C-Sprache übernimmt die **Import** -Direktive nur den Typ und die Konstanten Definitionen und ignoriert Prozedur Prototypen.</span><span class="sxs-lookup"><span data-stu-id="2a5e4-111">Unlike the C-language **\#include** directive, the **import** directive only picks up type and constant definitions and ignores procedure prototypes.</span></span> <span data-ttu-id="2a5e4-112">Diese Vorgehensweise funktioniert, solange die IDL-Hauptdatei nicht auf nicht Remote fähige Typen verweist, die in der Header Datei definiert sind.</span><span class="sxs-lookup"><span data-stu-id="2a5e4-112">This approach will work as long as your main IDL file does not reference any nonremotable types defined in the header file.</span></span>
-   <span data-ttu-id="2a5e4-113">Erstellen Sie eine IDL-Hilfsdatei mit einer Dummy-Schnittstelle, die die Header Dateien einschließt.</span><span class="sxs-lookup"><span data-stu-id="2a5e4-113">Create a helper IDL file with a dummy interface that includes the header files.</span></span> <span data-ttu-id="2a5e4-114">Verwenden Sie dann die [**Import**](import.md) -Direktive, um die Hilfsdatei einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="2a5e4-114">Then, use the [**import**](import.md) directive to include the helper file.</span></span> <span data-ttu-id="2a5e4-115">Auf diese Weise werden nur die [**typedef**](typedef.md)s in den kompilierten Stub angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a5e4-115">In this way, only the [**typedef**](typedef.md)s will appear in the compiled stubs.</span></span> <span data-ttu-id="2a5e4-116">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2a5e4-116">For example:</span></span>

```syntax
//in helper.idl:
interface dummy
{ 
   #include "kitchensink.h"
   #include "system.h"
}

//in main.idl:
import "helper.idl";
```
