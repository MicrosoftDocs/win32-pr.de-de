---
description: Der MOF-Compiler (Managed Object Format) unterstützt zwei Arten von Kommentaren unter Verwendung zweier verschiedener Arten von Kommentar Trennzeichen.
ms.assetid: 5ab71b45-7ed1-44c4-8710-6b833b0afb80
ms.tgt_platform: multiple
title: Erstellen eines Kommentars
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d0e7cf2484fef018c62c8c47d9c55d245191681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368241"
---
# <a name="creating-a-comment"></a><span data-ttu-id="2bba9-103">Erstellen eines Kommentars</span><span class="sxs-lookup"><span data-stu-id="2bba9-103">Creating a Comment</span></span>

<span data-ttu-id="2bba9-104">Der MOF-Compiler (Managed Object Format) unterstützt zwei Arten von Kommentaren unter Verwendung zweier verschiedener Arten von Kommentar Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="2bba9-104">The Managed Object Format (MOF) compiler supports two styles of comment using two different styles of comment delimiters.</span></span>

<span data-ttu-id="2bba9-105">In der folgenden Tabelle werden die Trennzeichen aufgelistet, die für Kommentare verwendet werden, und die Auswirkungen, die die Trennzeichen im Code aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2bba9-105">The following table lists the delimiters that are used for comments and the effect that the delimiters have in the code.</span></span>



| <span data-ttu-id="2bba9-106">Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="2bba9-106">Delimiter</span></span>   | <span data-ttu-id="2bba9-107">Markierungen</span><span class="sxs-lookup"><span data-stu-id="2bba9-107">Marks</span></span>                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------|
| //          | <span data-ttu-id="2bba9-108">Beginn eines Kommentars, der am Ende der Zeile endet.</span><span class="sxs-lookup"><span data-stu-id="2bba9-108">Start of a comment that terminates at the end of the line.</span></span>                                    |
| <span data-ttu-id="2bba9-109">/\* immer \*/</span><span class="sxs-lookup"><span data-stu-id="2bba9-109">/\* and \*/</span></span> | <span data-ttu-id="2bba9-110">Anfang und Ende eines Kommentars, der sich möglicherweise über mehrere Zeilen erstreckt oder nur einen Teil einer Zeile umfasst.</span><span class="sxs-lookup"><span data-stu-id="2bba9-110">Beginning and end of a comment that may span multiple lines or only span a portion of a line.</span></span> |



 

<span data-ttu-id="2bba9-111">Wie in den Programmiersprachen C und C++ muss das//-Trennzeichen nur mit einzeiligen Kommentaren verwendet werden. dabei werden die/ \* und \* /-Trennzeichen entweder mit einzeiligen oder mehrzeiligen Kommentaren verwendet.</span><span class="sxs-lookup"><span data-stu-id="2bba9-111">As in the C and C++ programming languages, you must use the // delimiter with single-line comments only, but use the /\* and \*/ delimiters with either single-line or multiple-line comments.</span></span>

<span data-ttu-id="2bba9-112">Im folgenden Codebeispiel werden die beiden Trennzeichen Stile beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2bba9-112">The following code example describes the two delimiter styles.</span></span>

``` syntax
int32 MyProp = 2; // This is a comment until the line ends.
int32 /* This is a comment. */ MyProp = 2;
```

## <a name="related-topics"></a><span data-ttu-id="2bba9-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2bba9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bba9-114">Entwerfen von Managed Object Format-Klassen (MOF)</span><span class="sxs-lookup"><span data-stu-id="2bba9-114">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



