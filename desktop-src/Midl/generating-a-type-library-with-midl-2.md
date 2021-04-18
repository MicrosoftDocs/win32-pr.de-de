---
title: Erstellen einer Typbibliothek mit "Mittel l"
description: Das Element der obersten Ebene der ODL-Syntax ist die Library-Anweisung (Library-Block).
ms.assetid: e21a9e6e-4e10-4280-af8f-24534cb2ab90
keywords:
- Microsoft Interface Definition Language mittlerer l, Aufgaben, Erstellen einer Typbibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85f6e8f7ea6f65bc503c08872c9199ff3d5fd828
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341519"
---
# <a name="generating-a-type-library-with-midl"></a><span data-ttu-id="e8d92-104">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="e8d92-104">Generating a Type Library with MIDL</span></span>

<span data-ttu-id="e8d92-105">Das Element der obersten Ebene der ODL-Syntax ist die Library-Anweisung (Library-Block).</span><span class="sxs-lookup"><span data-stu-id="e8d92-105">The top-level element of the ODL syntax is the library statement (library block).</span></span> <span data-ttu-id="e8d92-106">Jede andere ODL-Anweisung, mit Ausnahme der Attribute, die auf die Library-Anweisung angewendet werden, muss innerhalb des Bibliotheks Blocks definiert werden.</span><span class="sxs-lookup"><span data-stu-id="e8d92-106">Every other ODL statement, with the exception of the attributes that are applied to the library statement, must be defined within the library block.</span></span> <span data-ttu-id="e8d92-107">Wenn der mittlerer l-Compiler einen Bibliotheks Block sieht, generiert er eine Typbibliothek ähnlich wie MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="e8d92-107">When the MIDL compiler sees a library block, it generates a type library in much the same way that MkTypLib does.</span></span> <span data-ttu-id="e8d92-108">Mit einigen Ausnahmen, die [unter Unterschiede zwischen mittlerer l und MkTypLib](differences-between-midl-and-mktyplib.md)beschrieben werden, sollten die Anweisungen innerhalb des Bibliotheks Blocks dieselbe Syntax wie in der ODL-Sprache und MkTypLib befolgen.</span><span class="sxs-lookup"><span data-stu-id="e8d92-108">With a few exceptions, described in [Differences Between MIDL and MKTYPLIB](differences-between-midl-and-mktyplib.md), the statements within the library block should follow the same syntax as in the ODL language and MkTypLib.</span></span>

> [!Note]  
> <span data-ttu-id="e8d92-109">Das Mktyplib.exe Tool ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="e8d92-109">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="e8d92-110">Verwenden Sie stattdessen den Mittel l-Compiler.</span><span class="sxs-lookup"><span data-stu-id="e8d92-110">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="e8d92-111">Sie können odl-Attribute auf Elemente anwenden, die entweder innerhalb oder außerhalb des Bibliotheks Blocks definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e8d92-111">You can apply ODL attributes to elements that are defined either inside or outside the library block.</span></span> <span data-ttu-id="e8d92-112">Diese Attribute haben keine Auswirkung außerhalb des Bibliotheks Blocks, es sei denn, auf das Element, auf das Sie angewendet werden, wird im Bibliotheks Block verwiesen.</span><span class="sxs-lookup"><span data-stu-id="e8d92-112">These attributes have no effect outside the library block unless the element they are applied to is referenced from within the library block.</span></span> <span data-ttu-id="e8d92-113">Anweisungen innerhalb des Bibliotheks Blocks können auf ein außen Element verweisen, indem es entweder als Basistyp verwendet wird, von ihm geerbt wird, oder indem in einer Zeile wie gezeigt auf das Element verwiesen wird:</span><span class="sxs-lookup"><span data-stu-id="e8d92-113">Statements inside the library block can reference an outside element either by using it as a base type, inheriting from it, or by referencing it on a line as shown:</span></span>

``` syntax
<some IDL definitions including definitions for interface IFace and struct bar>
[<some attributes>]
library a
{
    interface IFace;
    struct this_struct;
...
};
```

<span data-ttu-id="e8d92-114">Wenn innerhalb des Bibliotheks Blocks auf ein Element verwiesen wird, das außerhalb des Bibliotheks Blocks definiert ist, wird seine Definition in die generierte Typbibliothek eingefügt.</span><span class="sxs-lookup"><span data-stu-id="e8d92-114">If an element defined outside the library block is referenced within the library block, then its definition will be put into the generated type library.</span></span> <span data-ttu-id="e8d92-115">Der mittlerer l-Compiler behandelt die Anweisungen außerhalb eines Bibliotheks Blocks als eine typische IDL-Datei und analysiert diese Anweisungen, wie Sie dies immer getan haben.</span><span class="sxs-lookup"><span data-stu-id="e8d92-115">The MIDL compiler treats the statements outside of a library block as a typical IDL file and parses those statements as it has always done.</span></span> <span data-ttu-id="e8d92-116">Normalerweise bedeutet dies, dass C-sprach-Stub für eine RPC-Anwendung erzeugt werden.</span><span class="sxs-lookup"><span data-stu-id="e8d92-116">Normally, this means generating C-language stubs for an RPC application.</span></span>

<span data-ttu-id="e8d92-117">Weitere Informationen zur allgemeinen Syntax für eine ODL-Datei finden Sie unter [Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax).</span><span class="sxs-lookup"><span data-stu-id="e8d92-117">For more information about the general syntax for an ODL file see [ODL File Syntax](/previous-versions/windows/desktop/automat/odl-file-syntax).</span></span>

 

 