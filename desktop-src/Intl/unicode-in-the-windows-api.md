---
description: 'Windows-API-Funktionen, die Zeichen bearbeiten, werden im Allgemeinen in einem von drei Formaten implementiert:'
ms.assetid: e7698f0b-dbcb-4cd0-9cb5-23a26edb966a
title: Unicode in der Windows-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5686a7f65edefb11458374b7f72262448becd6d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373161"
---
# <a name="unicode-in-the-windows-api"></a><span data-ttu-id="6fe0f-103">Unicode in der Windows-API</span><span class="sxs-lookup"><span data-stu-id="6fe0f-103">Unicode in the Windows API</span></span>

<span data-ttu-id="6fe0f-104">Windows-API-Funktionen, die Zeichen bearbeiten, werden im Allgemeinen in einem von drei Formaten implementiert:</span><span class="sxs-lookup"><span data-stu-id="6fe0f-104">Windows API functions that manipulate characters are generally implemented in one of three formats:</span></span>

-   <span data-ttu-id="6fe0f-105">Eine generische Version, die für Windows-Codepages oder Unicode kompiliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-105">A generic version that can be compiled for either Windows code pages or Unicode</span></span>
-   <span data-ttu-id="6fe0f-106">Eine [Windows-Codepage](code-pages.md) -Version mit dem Buchstaben "A", mit der "ANSI" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-106">A [Windows code page](code-pages.md) version with the letter "A" used to indicate "ANSI"</span></span>
-   <span data-ttu-id="6fe0f-107">Eine [Unicode](unicode.md) -Version mit dem Buchstaben "W", die "Wide" angibt</span><span class="sxs-lookup"><span data-stu-id="6fe0f-107">A [Unicode](unicode.md) version with the letter "W" used to indicate "wide"</span></span>

<span data-ttu-id="6fe0f-108">Einige neuere Funktionen unterstützen nur Unicode-Versionen.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-108">Some newer functions support only Unicode versions.</span></span> <span data-ttu-id="6fe0f-109">Weitere Informationen finden Sie unter [Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="6fe0f-109">For more information, see [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span>

<span data-ttu-id="6fe0f-110">In den folgenden Themen finden Sie Informationen zu Unicode-Datentypen und deren Verwendung in Funktionen und Nachrichten. Verwendung von Ressourcen, Dateinamen und Befehlszeilen Argumenten und Methoden zum Übersetzen zwischen verschiedenen Zeichen folgen Typen.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-110">The following topics discuss Unicode data types and how they are used in functions and messages; the use of resources, file names, and command line arguments; and methods of translating between different types of strings.</span></span>

-   [<span data-ttu-id="6fe0f-111">Automatische Nachrichten Übersetzung</span><span class="sxs-lookup"><span data-stu-id="6fe0f-111">Automatic Message Translation</span></span>](automatic-message-translation.md)
-   [<span data-ttu-id="6fe0f-112">In Dateinamen verwendete Zeichensätze</span><span class="sxs-lookup"><span data-stu-id="6fe0f-112">Character Sets Used in File Names</span></span>](character-sets-used-in-file-names.md)
-   [<span data-ttu-id="6fe0f-113">Befehlszeilenargumente</span><span class="sxs-lookup"><span data-stu-id="6fe0f-113">Command Line Arguments</span></span>](command-line-arguments.md)
-   [<span data-ttu-id="6fe0f-114">Konventionen für Funktionsprototypen</span><span class="sxs-lookup"><span data-stu-id="6fe0f-114">Conventions for Function Prototypes</span></span>](conventions-for-function-prototypes.md)
-   [<span data-ttu-id="6fe0f-115">Standard-C-Funktionen</span><span class="sxs-lookup"><span data-stu-id="6fe0f-115">Standard C Functions</span></span>](standard-c-functions.md)
-   [<span data-ttu-id="6fe0f-116">Unterschiede in Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="6fe0f-116">String Function Differences</span></span>](string-function-differences.md)
-   [<span data-ttu-id="6fe0f-117">Übersetzung zwischen Zeichen folgen Typen</span><span class="sxs-lookup"><span data-stu-id="6fe0f-117">Translation Between String Types</span></span>](translation-between-string-types.md)
-   [<span data-ttu-id="6fe0f-118">Windows-Datentypen für Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="6fe0f-118">Windows Data Types for Strings</span></span>](windows-data-types-for-strings.md)

## <a name="related-topics"></a><span data-ttu-id="6fe0f-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6fe0f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fe0f-120">Informationen zu Unicode und Zeichensätzen</span><span class="sxs-lookup"><span data-stu-id="6fe0f-120">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



