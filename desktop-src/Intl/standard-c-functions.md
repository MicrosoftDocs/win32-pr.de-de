---
description: Die standardmäßigen C-Laufzeitbibliotheken enthalten beide Unicode-UTF-16-Versionen (breit Zeichen) von Zeichen folgen Funktionen, die mit Unicode-und Byte orientierten Versionen von Zeichen folgen Funktionen verwendet werden können, die mit Zeichen aus Einzel Byte-Zeichensätzen (SBCSs) verwendet werden können. Der Unicode-Datentyp WCHAR ist mit dem-Datentyp WCHAR \_ t in ANSI C kompatibel und ermöglicht den Zugriff auf die Unicode-Zeichen folgen Funktionen. Die Unicode-Versionen der Funktionen beginnen mit den Buchstaben &\# 0034; WCS&\# 0034; (oder manchmal &\# 0034; \_ WCS-&\# 0034;). Der für Codepages verwendete Datentyp char ist mit dem Zeichen Datentyp char in ANSI C kompatibel, um den Zugriff auf die Zeichen folgen Funktionen zu ermöglichen. Die Zeichen Versionen der Funktionen beginnen mit den Buchstaben &\# 0034; Str&\# 0034;. Es gibt auch spezielle Versionen für Doppelbyte-Zeichensätze (dbcss), die mit den Buchstaben &\# 0034; beginnen. \_ MSB&\# 0034;.
ms.assetid: a86626c1-7f90-4924-bfdd-384729bd0cc5
title: Standard-C-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6247b3707f96908ef16d887462ba06573fd8dd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868904"
---
# <a name="standard-c-functions"></a><span data-ttu-id="3d79d-108">Standard-C-Funktionen</span><span class="sxs-lookup"><span data-stu-id="3d79d-108">Standard C Functions</span></span>

<span data-ttu-id="3d79d-109">Die standardmäßigen C-Laufzeitbibliotheken enthalten beide Unicode-UTF-16-Versionen (breit Zeichen) von Zeichen folgen Funktionen, die mit [Unicode](unicode.md) -und Byte orientierten Versionen von Zeichen folgen Funktionen verwendet werden können, die mit Zeichen aus [Einzel Byte-Zeichensätzen](single-byte-character-sets.md) (SBCSs) verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3d79d-109">The standard C runtime libraries contain both Unicode UTF-16 (wide character) versions of string functions that can be used with [Unicode](unicode.md) and byte-oriented versions of string functions that can be used with characters from [single-byte character sets](single-byte-character-sets.md) (SBCSs).</span></span> <span data-ttu-id="3d79d-110">Der Unicode-Datentyp WCHAR ist mit dem-Datentyp WCHAR \_ t in ANSI C kompatibel und ermöglicht den Zugriff auf die Unicode-Zeichen folgen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="3d79d-110">The Unicode data type WCHAR is compatible with the data type wchar\_t in ANSI C, and allows access to the Unicode string functions.</span></span> <span data-ttu-id="3d79d-111">Die Unicode-Versionen der Funktionen beginnen mit den Buchstaben "WCS" (oder manchmal " \_ WCS").</span><span class="sxs-lookup"><span data-stu-id="3d79d-111">The Unicode versions of the functions start with the letters "wcs" (or sometimes "\_wcs").</span></span> <span data-ttu-id="3d79d-112">Der für Codepages verwendete Datentyp char ist mit dem Zeichen Datentyp char in ANSI C kompatibel, um den Zugriff auf die Zeichen folgen Funktionen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3d79d-112">The data type CHAR used for code pages is compatible with the character data type char in ANSI C, to allow access to the character string functions.</span></span> <span data-ttu-id="3d79d-113">Die Zeichen Versionen der Funktionen beginnen mit den Buchstaben "str".</span><span class="sxs-lookup"><span data-stu-id="3d79d-113">The character versions of the functions start with the letters "str".</span></span> <span data-ttu-id="3d79d-114">Es gibt auch spezielle Versionen für [Doppelbyte-Zeichensätze](double-byte-character-sets.md) (dbcss), die mit den Buchstaben " \_ MSB" beginnen.</span><span class="sxs-lookup"><span data-stu-id="3d79d-114">There are also special versions for [double-byte character sets](double-byte-character-sets.md) (DBCSs) that start with the letters "\_mbs".</span></span>

<span data-ttu-id="3d79d-115">Die standardmäßigen c-Laufzeitbibliotheken enthalten generische Funktionen für alle Standard-c-Zeichen folgen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="3d79d-115">The standard C runtime libraries include generic functions for all standard C string functions.</span></span> <span data-ttu-id="3d79d-116">Sie beginnen mit " \_ TCS" und sind in der Header Datei "Tchar. h" aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d79d-116">They start with "\_tcs" and are listed in the Tchar.h header file.</span></span> <span data-ttu-id="3d79d-117">Diese Funktionen verwenden den generischen TCHAR-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="3d79d-117">These functions use the generic TCHAR data type.</span></span>

<span data-ttu-id="3d79d-118">Eine Anwendung muss die folgenden Zeilen hinzufügen, um die generischen Funktionen zu verwenden und für Unicode zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="3d79d-118">An application must add the following lines to use the generic functions and compile for Unicode.</span></span>


```C++
#define _UNICODE

#include <tchar.h>
#include <wchar.h>
```



<span data-ttu-id="3d79d-119">Beachten Sie, dass die Dateien "Tchar. h" und "WCHAR. h" erforderlich sind und dass der führende Unterstrich für die \_ Unicode-Variable ebenfalls erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3d79d-119">Note that both the Tchar.h and Wchar.h files are required, and that the leading underscore on the \_UNICODE variable is also required.</span></span> <span data-ttu-id="3d79d-120">Diese Nomenklatur ist spezifisch für die Standard-C-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="3d79d-120">This nomenclature is specific to the standard C library.</span></span> <span data-ttu-id="3d79d-121">"Unicode", die ohne Unterstrich gerendert wird, ist für die Microsoft Windows-Laufzeiten.</span><span class="sxs-lookup"><span data-stu-id="3d79d-121">"UNICODE" rendered without the underscore is for the Microsoft Windows runtimes.</span></span>

<span data-ttu-id="3d79d-122">Die Funktionen [wcstomsb](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) und [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) können mit einigen Einschränkungen aus dem von der Standard-C-Bibliothek unterstützten Zeichensatz in Unicode und Back konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="3d79d-122">The [wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) and [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) functions can convert from the character set supported by the standard C library to Unicode and back, with some limitations.</span></span> <span data-ttu-id="3d79d-123">Weitere Informationen zum Übersetzen von Zeichen folgen in und aus Unicode finden Sie unter [Übersetzung zwischen Zeichen folgen Typen](translation-between-string-types.md).</span><span class="sxs-lookup"><span data-stu-id="3d79d-123">For more information about translating strings to and from Unicode, see [Translation Between String Types](translation-between-string-types.md).</span></span>

<span data-ttu-id="3d79d-124">Die in Tchar. h definierte [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) -Funktion unterstützt die gleichen Formatspezifikationen wie die "strausafe. h"-Druckfunktionen, z. b. " [**stringcbprintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa)".</span><span class="sxs-lookup"><span data-stu-id="3d79d-124">The [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) function defined in Tchar.h supports the same format specifications as the Strsafe.h print functions, for example [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa).</span></span> <span data-ttu-id="3d79d-125">Ebenso definiert Tchar. h eine [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) -Funktion, in der die Format Zeichenfolge selbst eine Unicode-Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="3d79d-125">Similarly, Tchar.h defines a [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) function, in which the format string itself is a Unicode string.</span></span>

> [!Caution]  
> <span data-ttu-id="3d79d-126">Eine schlechte Puffer Behandlung ist in vielen Sicherheitsproblemen enthalten, die Pufferüberläufe einschließen.</span><span class="sxs-lookup"><span data-stu-id="3d79d-126">Poor buffer handling is implicated in many security issues that involve buffer overruns.</span></span> <span data-ttu-id="3d79d-127">Weitere Informationen finden Sie unter [Referenz](../menurc/strsafe-ovw.md)zu ""</span><span class="sxs-lookup"><span data-stu-id="3d79d-127">See [Strsafe.h Reference](../menurc/strsafe-ovw.md).</span></span> <span data-ttu-id="3d79d-128">Die in "strausafe. h" definierten Funktionen bieten zusätzliche Verarbeitungsschritte für die ordnungsgemäße Puffer Behandlung in Ihrem Code.</span><span class="sxs-lookup"><span data-stu-id="3d79d-128">The functions defined in Strsafe.h provide additional processing for proper buffer handling in your code.</span></span> <span data-ttu-id="3d79d-129">Sie sind dazu gedacht, Ihre integrierten C/C++-Gegenstücke und bestimmte Microsoft Windows-Implementierungen zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="3d79d-129">They are intended to replace their built-in C/C++ counterparts as well as specific Microsoft Windows implementations.</span></span> <span data-ttu-id="3d79d-130">Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="3d79d-130">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3d79d-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3d79d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d79d-132">Unicode in der Windows-API</span><span class="sxs-lookup"><span data-stu-id="3d79d-132">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
