---
title: " include"
description: Die \ include-Direktive bewirkt, dass der Ressourcen Compiler die im filename-Parameter angegebene Datei verarbeitet.
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8d36f1d0ae24f3dc21d67eec57056872aabdbd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391466"
---
# <a name="-include"></a><span data-ttu-id="4b15a-103">darunter</span><span class="sxs-lookup"><span data-stu-id="4b15a-103">' include'</span></span>

<span data-ttu-id="4b15a-104">Die **\# include** -Direktive bewirkt, dass der Ressourcen Compiler die im *filename* -Parameter angegebene Datei verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="4b15a-104">The **\#include** directive causes the resource compiler to process the file specified in the *filename* parameter.</span></span> <span data-ttu-id="4b15a-105">Bei dieser Datei sollte es sich um eine Header Datei handeln, die die in der Ressourcen Definitionsdatei verwendeten Konstanten definiert.</span><span class="sxs-lookup"><span data-stu-id="4b15a-105">This file should be a header file that defines the constants used in the resource-definition file.</span></span> <span data-ttu-id="4b15a-106">Die Datei kann Einzel Byte-, Doppelbyte-oder Unicode-Zeichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b15a-106">The file can use single-byte, double-byte, or Unicode characters.</span></span>

``` syntax
#include filename
```

<dl> <dt>

<span data-ttu-id="4b15a-107"><span id="filename"></span><span id="FILENAME"></span>*Einfügen*</span><span class="sxs-lookup"><span data-stu-id="4b15a-107"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="4b15a-108">Der Name der einzuschließenden Datei.</span><span class="sxs-lookup"><span data-stu-id="4b15a-108">Name of the file to be included.</span></span> <span data-ttu-id="4b15a-109">Wenn sich die Datei im aktuellen Verzeichnis befindet, muss die Zeichenfolge in doppelte Anführungszeichen eingeschlossen werden. Wenn sich die Datei in dem Verzeichnis befindet, das durch die include-Umgebungsvariable angegeben ist, muss die Zeichenfolge in eine kleiner-als-oder größer-als-Zeichen (<>) eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="4b15a-109">If the file is in the current directory, the string must be enclosed in double quotation marks; if the file is in the directory specified by the INCLUDE environment variable, the string must be enclosed in less-than and greater-than characters (<>).</span></span> <span data-ttu-id="4b15a-110">Sie müssen einen vollständigen Pfad in doppelte Anführungszeichen (") einschließen, wenn sich die Datei nicht im aktuellen Verzeichnis oder in dem Verzeichnis befindet, das in der INCLUDE-Umgebungsvariablen angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4b15a-110">You must give a full path enclosed in double quotation marks (") if the file is not in the current directory or in the directory specified by the INCLUDE environment variable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b15a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b15a-111">Remarks</span></span>

<span data-ttu-id="4b15a-112">Verwenden Sie die folgende Anweisung in der Header Datei, um-Anweisungen zu umschließen, die von einem C-Compiler, aber nicht von RC kompiliert werden können:</span><span class="sxs-lookup"><span data-stu-id="4b15a-112">Use the following statement in your header file to surround statements that can be compiled by a C compiler but not RC:</span></span>

``` syntax
#ifndef RC_INVOKED
```

<span data-ttu-id="4b15a-113">Auf diese Weise können Sie die gleichen Include-Dateien in den c-und RC-Dateien verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b15a-113">This way, you can use the same include files in your .c and .rc files.</span></span>

## <a name="example"></a><span data-ttu-id="4b15a-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4b15a-114">Example</span></span>

<span data-ttu-id="4b15a-115">In diesem Beispiel werden die Header Dateien "Windows. h" und "mydefs. h" beim Kompilieren der Ressourcen Definitionsdatei verarbeitet:</span><span class="sxs-lookup"><span data-stu-id="4b15a-115">This example processes the header files Windows.h and MyDefs.h while compiling the resource-definition file:</span></span>

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a><span data-ttu-id="4b15a-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b15a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b15a-117">Präprozessordirektiven</span><span class="sxs-lookup"><span data-stu-id="4b15a-117">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




