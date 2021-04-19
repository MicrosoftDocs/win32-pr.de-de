---
description: Wenn Sie generische Datentypen in Ihrem Code verwenden, können Sie ihn einfach mithilfe einer Präprozessordirektive zum Definieren von &\# 0034; Unicode&\# 0034; vor den \# include-Anweisungen für die Header Dateien.
ms.assetid: 1c9cbb18-9295-4847-86c1-d596668cbe57
title: Verwenden von generischen Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2604f87b12e86076bed47f509c6398fa8482b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359605"
---
# <a name="using-generic-data-types"></a><span data-ttu-id="644ce-103">Verwenden von generischen Datentypen</span><span class="sxs-lookup"><span data-stu-id="644ce-103">Using Generic Data Types</span></span>

<span data-ttu-id="644ce-104">Wenn Sie generische Datentypen in Ihrem Code verwenden, können Sie [Sie einfach mit](unicode.md) einer Präprozessordirektive kompilieren, um "Unicode" vor den **\# include** -Anweisungen für die Header Dateien zu definieren.</span><span class="sxs-lookup"><span data-stu-id="644ce-104">If you use generic data types in your code, it can be compiled for [Unicode](unicode.md) simply by using a preprocessor directive to define "UNICODE" before the **\#include** statements for the header files.</span></span> <span data-ttu-id="644ce-105">Um den Code für [Windows (ANSI)-Codepages](code-pages.md)zu kompilieren, lassen Sie die Unicode-Definition aus.</span><span class="sxs-lookup"><span data-stu-id="644ce-105">To compile the code for [Windows (ANSI) code pages](code-pages.md), omit the "UNICODE" definition.</span></span> <span data-ttu-id="644ce-106">Neue Windows-Anwendungen sollten Unicode verwenden, um Inkonsistenzen von unterschiedlichen Codepages zu vermeiden und die Lokalisierung</span><span class="sxs-lookup"><span data-stu-id="644ce-106">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and simplify localization.</span></span>

<span data-ttu-id="644ce-107">So erstellen Sie Quellcode, der entweder zur Verwendung von Unicode-Zeichen und Zeichen folgen oder zum Verwenden von Zeichen und Zeichen folgen aus Windows-Codepages kompiliert werden kann:</span><span class="sxs-lookup"><span data-stu-id="644ce-107">To create source code that can be compiled either to use Unicode characters and strings or to use characters and strings from Windows code pages:</span></span>

1.  <span data-ttu-id="644ce-108">Verwenden Sie generische Datentypen, z. b. TCHAR, LPTStr und lptch, für alle Zeichen-und Zeichen folgen Typen, die für Text verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="644ce-108">Use generic data types, such as TCHAR, LPTSTR, and LPTCH, for all character and string types used for text.</span></span> <span data-ttu-id="644ce-109">Weitere Informationen zu generischen Typen finden Sie unter [Windows-Datentypen für](windows-data-types-for-strings.md)Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="644ce-109">For more about generic types, see [Windows Data Types for Strings](windows-data-types-for-strings.md).</span></span>
2.  <span data-ttu-id="644ce-110">Stellen Sie sicher, dass Zeiger auf nicht Text-Datenpuffer oder binäre Byte Arrays mit Datentypen wie LPBYTE oder lpword anstelle des LPTStr-oder lptch-Typs codiert werden.</span><span class="sxs-lookup"><span data-stu-id="644ce-110">Be sure that pointers to non-text data buffers or binary byte arrays are coded with data types such as LPBYTE or LPWORD, instead of the LPTSTR or LPTCH type.</span></span>
3.  <span data-ttu-id="644ce-111">Deklarieren Sie Zeiger des unbestimmten Typs explizit als void-Zeiger mithilfe von LPVOID, wenn dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="644ce-111">Declare pointers of indeterminate type explicitly as void pointers by using LPVOID as appropriate.</span></span>
4.  <span data-ttu-id="644ce-112">Legen Sie einen arithmetischen Zeiger vom Typ unabhängig.</span><span class="sxs-lookup"><span data-stu-id="644ce-112">Make pointer arithmetic type-independent.</span></span> <span data-ttu-id="644ce-113">Die Verwendung von Einheiten der TCHAR-Größe ergibt Variablen mit 2 Bytes, wenn Unicode definiert ist, und 1 Byte, wenn Unicode nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="644ce-113">Using units of TCHAR size yields variables that are 2 bytes if UNICODE is defined, and 1 byte if UNICODE is not defined.</span></span> <span data-ttu-id="644ce-114">Die Verwendung von Zeigerarithmetik gibt immer die Anzahl der Elemente zurück, die durch den Zeiger angegeben werden, unabhängig davon, ob die Elemente 1 oder 2 Bytes groß sind.</span><span class="sxs-lookup"><span data-stu-id="644ce-114">Using pointer arithmetic always returns the number of elements indicated by the pointer, whether the elements are 1 or 2 bytes in size.</span></span> <span data-ttu-id="644ce-115">Der folgende Ausdruck ruft immer die Anzahl der Elemente ab, unabhängig davon, ob Unicode definiert ist.</span><span class="sxs-lookup"><span data-stu-id="644ce-115">The following expression always retrieves the number of elements, regardless of whether UNICODE is defined.</span></span>

    ```C++
    cCount = lpEnd - lpStart;
    ```

    

    <span data-ttu-id="644ce-116">Der folgende Ausdruck bestimmt die Anzahl der verwendeten Bytes.</span><span class="sxs-lookup"><span data-stu-id="644ce-116">The following expression determines the number of bytes used.</span></span>

    ```C++
    cByteCount = (lpEnd - lpStart) * sizeof(TCHAR);
    ```

    

    <span data-ttu-id="644ce-117">Es ist nicht erforderlich, eine Anweisung wie die folgende zu ändern, da die zeigerinkrement auf das nächste Zeichen Element zeigt.</span><span class="sxs-lookup"><span data-stu-id="644ce-117">There is no need to change a statement like the following one, because the pointer increment points to the next character element.</span></span>

    ```C++
    chNext = *++lpText;
    ```

    

5.  <span data-ttu-id="644ce-118">Ersetzen Sie Literalzeichenfolgen und Manifest-Zeichen Konstanten durch Makros.</span><span class="sxs-lookup"><span data-stu-id="644ce-118">Replace literal strings and manifest character constants with macros.</span></span> <span data-ttu-id="644ce-119">Ändern Sie Ausdrücke wie die folgende.</span><span class="sxs-lookup"><span data-stu-id="644ce-119">Change expressions like the following one.</span></span>

    ```C++
    while(*lpFileName++ != '\\')
    {
        // ...
    }
    ```

    

    <span data-ttu-id="644ce-120">Verwenden Sie das [**Text**](/windows/desktop/api/Winnt/nf-winnt-text) Makro wie folgt in diesem Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="644ce-120">Use the [**TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) macro as follows in this expression.</span></span>

    ```C++
    while(*lpFileName++ != TEXT('\\'))
    {
        // ...
    }
    ```

    

    <span data-ttu-id="644ce-121">Das [**Text**](/windows/desktop/api/Winnt/nf-winnt-text) Makro bewirkt, dass Zeichen folgen als L "String" ausgewertet werden, wenn Unicode definiert ist, andernfalls als "String".</span><span class="sxs-lookup"><span data-stu-id="644ce-121">The [**TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) macro causes strings to be evaluated as L"string" when UNICODE is defined, and as "string" otherwise.</span></span> <span data-ttu-id="644ce-122">Um die Verwaltung zu vereinfachen, verschieben Sie Literalzeichenfolgen in Ressourcen, insbesondere dann, wenn Sie Zeichen außerhalb des ASCII-Bereichs (0x00 bis 0x7F) enthalten oder auf der Benutzeroberfläche verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="644ce-122">For easier management, move literal strings into resources, especially if they contain characters outside the ASCII range (0x00 through 0x7F) or are exposed at the user interface.</span></span> <span data-ttu-id="644ce-123">Um die Lokalisierung Ihrer Anwendung für verschiedene nationale Sprachen zu unterstützen, ist es sehr wichtig, dass sich alle Benutzeroberflächen-Zeichen folgen in lokalisierbaren Ressourcen befinden.</span><span class="sxs-lookup"><span data-stu-id="644ce-123">To support localization of your application for different national languages, it is very important for all user interface strings to be in localizable resources.</span></span>

6.  <span data-ttu-id="644ce-124">Verwenden Sie die generischen Versionen der Windows-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="644ce-124">Use the generic versions of the Windows functions.</span></span> <span data-ttu-id="644ce-125">Weitere Informationen finden Sie unter [Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="644ce-125">For more information, see [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span>
7.  <span data-ttu-id="644ce-126">Verwenden Sie die generischen Versionen der Standardfunktionen der c-Bibliotheks Zeichenfolge, und denken Sie daran, " \_ Unicode" und "Unicode" zu definieren, wie in [Standard-C-Funktionen](standard-c-functions.md)erläutert.</span><span class="sxs-lookup"><span data-stu-id="644ce-126">Use the generic versions of the standard C library string functions, and remember to define "\_UNICODE" as well as "UNICODE", as discussed in [Standard C Functions](standard-c-functions.md).</span></span>
8.  <span data-ttu-id="644ce-127">Wenn Sie eine Anwendung anpassen, die ursprünglich für Windows-Codepages geschrieben wurde, denken Sie daran, Code zu ändern, der auf 255 als größten Wert für ein Zeichen basiert.</span><span class="sxs-lookup"><span data-stu-id="644ce-127">If you are adapting an application originally written for Windows code pages, remember to change any code that relies on 255 as the largest value for a character.</span></span>

<span data-ttu-id="644ce-128">Wenn Sie Code kompilieren, den Sie wie oben beschrieben geschrieben haben, kann der Compiler sowohl Unicode-als auch Windows-Code Page Versionen der Anwendung aus derselben Quelle erstellen.</span><span class="sxs-lookup"><span data-stu-id="644ce-128">When you compile code that you have written as outlined above, the compiler can create both Unicode and Windows code page versions of your application from the same source.</span></span> <span data-ttu-id="644ce-129">Abhängig von den Definitionen für Unicode werden die generischen Funktionen aufgelöst, um dieselben Binärdateien zu erhalten, als wenn Sie Code exklusiv für Unicode oder exklusiv für Windows-Codepages geschrieben haben.</span><span class="sxs-lookup"><span data-stu-id="644ce-129">Depending on the definitions for UNICODE, the generic functions are resolved to produce the same binary files as if you wrote code exclusively for Unicode or exclusively for Windows code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="644ce-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="644ce-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="644ce-131">Verwenden von Unicode und Zeichensätzen</span><span class="sxs-lookup"><span data-stu-id="644ce-131">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 



