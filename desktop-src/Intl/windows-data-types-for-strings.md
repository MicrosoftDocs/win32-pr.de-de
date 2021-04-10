---
description: Die meisten Zeichen folgen Operationen können die gleiche Logik für Unicode und für Windows-Codepages verwenden.
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: Windows-Datentypen für Zeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e24be1024736ce324e040e58f6ac45636a11d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050606"
---
# <a name="windows-data-types-for-strings"></a><span data-ttu-id="7252b-103">Windows-Datentypen für Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="7252b-103">Windows Data Types for Strings</span></span>

<span data-ttu-id="7252b-104">Die meisten Zeichen folgen Operationen können die gleiche Logik für [Unicode](unicode.md) und für [Windows-Codepages](code-pages.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="7252b-104">Most string operations can use the same logic for [Unicode](unicode.md) and for [Windows code pages](code-pages.md).</span></span> <span data-ttu-id="7252b-105">Der einzige Unterschied besteht darin, dass die grundlegende Betriebseinheit ein 16-Bit-Zeichen (auch als breit Zeichen bezeichnet) für Unicode und ein 8-Bit-Zeichen für Windows-Codepages ist.</span><span class="sxs-lookup"><span data-stu-id="7252b-105">The only difference is that the basic unit of operation is a 16-bit character (also known as a wide character) for Unicode and an 8-bit character for Windows code pages.</span></span> <span data-ttu-id="7252b-106">Die Windows-Header Dateien bieten mehrere Typdefinitionen, die das Erstellen von Quellen erleichtern, die für Unicode oder für Windows-Codepages kompiliert werden können.</span><span class="sxs-lookup"><span data-stu-id="7252b-106">The Windows header files provide several type definitions that make it easy to create sources that can be compiled for Unicode or for Windows code pages.</span></span>

<span data-ttu-id="7252b-107">Windows unterstützt drei Sätze von Zeichen-und Zeichen folgen Datentypen: eine Reihe von generischen Typdefinitionen, die für Unicode-oder Windows-Codepages und zwei Sätze spezifischer Typdefinitionen kompiliert werden können.</span><span class="sxs-lookup"><span data-stu-id="7252b-107">Windows supports three sets of character and string data types: a set of generic type definitions that can compile for either Unicode or Windows code pages, and two sets of specific type definitions.</span></span> <span data-ttu-id="7252b-108">Ein Satz spezifischer Typdefinitionen dient zur Verwendung mit Unicode, der andere für die Verwendung mit Windows-Codepages.</span><span class="sxs-lookup"><span data-stu-id="7252b-108">One set of specific type definitions is for use with Unicode, and the other is for use with Windows code pages.</span></span>

<span data-ttu-id="7252b-109">Eine Anwendung, die generische Datentypen verwendet, kann einfach durch Definieren von "Unicode" vor den **\# include** -Anweisungen für die Header Dateien oder während der Kompilierung kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="7252b-109">An application using generic data types can be compiled for Unicode simply by defining "UNICODE" before the **\#include** statements for the header files, or during compilation.</span></span> <span data-ttu-id="7252b-110">Neue Windows-Anwendungen sollten Unicode verwenden, um Inkonsistenzen von verschiedenen Codepages zu vermeiden und die Lokalisierung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="7252b-110">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and to simplify localization.</span></span> <span data-ttu-id="7252b-111">Sie sollten mit generischen Datentypen geschrieben werden und sollten "Unicode" definieren, damit diese Typen in Unicode-Typen kompiliert werden können.</span><span class="sxs-lookup"><span data-stu-id="7252b-111">They should be written with generic data types, and should define "UNICODE" in order to compile these types into Unicode types.</span></span> <span data-ttu-id="7252b-112">An den wenigen Stellen, an denen eine Anwendung mit 8-Bit-Zeichendaten arbeiten muss, kann Sie die Typen für Windows-Codepages explizit verwenden.</span><span class="sxs-lookup"><span data-stu-id="7252b-112">In the few places where an application must work with 8-bit character data, it can make explicit use of the types for Windows code pages.</span></span>

<span data-ttu-id="7252b-113">Die Möglichkeit zum Kompilieren der generischen Typen in Typen für Windows-Codepages besteht hauptsächlich darin, ältere Anwendungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7252b-113">The ability to compile the generic types into types for Windows code pages exists mainly to support legacy applications.</span></span> <span data-ttu-id="7252b-114">Zur Kompilierung für Windows-Codepages lässt die Anwendung lediglich die Unicode-Definition aus.</span><span class="sxs-lookup"><span data-stu-id="7252b-114">To compile for Windows code pages, the application just omits the UNICODE definition.</span></span>

<span data-ttu-id="7252b-115">Das folgende Beispiel zeigt die-Methode, die in den Windows-Header Dateien zum Definieren der drei Sätze von Datentypen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7252b-115">The following example shows the method used in the Windows header files to define the three sets of data types.</span></span> <span data-ttu-id="7252b-116">Informationen zur Implementierung finden Sie in der Header Datei "Winnt. h".</span><span class="sxs-lookup"><span data-stu-id="7252b-116">For the implementation, see the Winnt.h header file.</span></span>


```C++
// Generic types

#ifdef UNICODE
    typedef wchar_t TCHAR;
#else
    typedef unsigned char TCHAR;
#endif

typedef TCHAR *LPTSTR, *LPTCH;

// 8-bit character specific

typedef unsigned char CHAR;
typedef CHAR *LPSTR, *LPCH;

// Unicode specific (wide characters)

typedef unsigned wchar_t WCHAR;
typedef WCHAR *LPWSTR, *LPWCH;
```



<span data-ttu-id="7252b-117">Der Buchstabe "T" in einer Typdefinition, z. b. TCHAR oder LPTSTR, legt einen generischen Typ fest, der für Windows-Codepages oder Unicode kompiliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7252b-117">The letter "T" in a type definition, for example, TCHAR or LPTSTR, designates a generic type that can be compiled for either Windows code pages or Unicode.</span></span> <span data-ttu-id="7252b-118">Der Buchstabe "W" in einer Typdefinition, z. b. "WCHAR" oder "LPWSTR", bezeichnet einen Unicode-Typ.</span><span class="sxs-lookup"><span data-stu-id="7252b-118">The letter "W" in a type definition, for example, WCHAR or LPWSTR, designates a Unicode type.</span></span> <span data-ttu-id="7252b-119">Da Windows-Codepages die ältere Form aufweisen, verfügen Sie über einfache Typdefinitionen, wie z. b. Char und LPStr.</span><span class="sxs-lookup"><span data-stu-id="7252b-119">Because Windows code pages are of the older form, they have simple type definitions, such as CHAR and LPSTR.</span></span> <span data-ttu-id="7252b-120">Eine umfassende Beschreibung der Datentypen in Windows finden Sie unter [Windows-Datentypen](../winprog/windows-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="7252b-120">For a complete description of data types in Windows, see [Windows Data Types](../winprog/windows-data-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7252b-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7252b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7252b-122">Unicode in der Windows-API</span><span class="sxs-lookup"><span data-stu-id="7252b-122">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
