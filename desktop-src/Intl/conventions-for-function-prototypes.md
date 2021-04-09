---
description: Der Windows SDK stellt Funktionsprototypen in generischen, Windows-Codepage-und Unicode-Versionen bereit.
ms.assetid: 601d24b0-11bb-48fa-a257-207c3acee226
title: Konventionen für Funktionsprototypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951860f72870dcbbcb88572f379e39dc843ecb11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865504"
---
# <a name="conventions-for-function-prototypes"></a><span data-ttu-id="b7bb7-103">Konventionen für Funktionsprototypen</span><span class="sxs-lookup"><span data-stu-id="b7bb7-103">Conventions for Function Prototypes</span></span>

<span data-ttu-id="b7bb7-104">Der Windows SDK stellt Funktionsprototypen in generischen, [Windows-Codepage](code-pages.md)-und [Unicode](unicode.md) -Versionen bereit.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-104">The Windows SDK provides function prototypes in generic, [Windows code page](code-pages.md), and [Unicode](unicode.md) versions.</span></span> <span data-ttu-id="b7bb7-105">Die Prototypen können kompiliert werden, um entweder Windows-Code Page Prototypen oder Unicode-Prototypen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-105">The prototypes can be compiled to produce either Windows code page prototypes or Unicode prototypes.</span></span> <span data-ttu-id="b7bb7-106">Alle drei Prototypen werden in diesem Thema erläutert und in den Codebeispielen für die Funktion " [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) " veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-106">All three prototypes are discussed in this topic and are illustrated by code samples for the [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) function.</span></span>

<span data-ttu-id="b7bb7-107">Im Folgenden finden Sie ein Beispiel eines generischen Prototyps:</span><span class="sxs-lookup"><span data-stu-id="b7bb7-107">The following is an example of a generic prototype.</span></span>


```C++
BOOL SetWindowText(
  HWND hwnd,
  LPCTSTR lpText
);
```



<span data-ttu-id="b7bb7-108">Die Headerdatei enthält den generischen Funktionsnamen als Makro implementiert.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-108">The header file provides the generic function name implemented as a macro.</span></span>


```C++
#ifdef UNICODE
#define SetWindowText SetWindowTextW
#else
#define SetWindowText SetWindowTextA
#endif // !UNICODE
```



<span data-ttu-id="b7bb7-109">Der Präprozessor erweitert das Makro entweder in den Windows-Codepage-oder Unicode-Funktionsnamen.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-109">The preprocessor expands the macro into either the Windows code page or Unicode function name.</span></span> <span data-ttu-id="b7bb7-110">Der Buchstabe "A" (ANSI) oder "W" (Unicode) wird nach Bedarf am Ende des generischen Funktionsnamens hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-110">The letter "A" (ANSI) or "W" (Unicode) is added at the end of the generic function name, as appropriate.</span></span> <span data-ttu-id="b7bb7-111">Die Header Datei enthält dann zwei spezifische Prototypen, eine für Windows-Codepages und eine für Unicode, wie in den folgenden Beispielen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-111">The header file then provides two specific prototypes, one for Windows code pages and one for Unicode, as shown in the following examples.</span></span>


```C++
BOOL SetWindowTextA(
  HWND hwnd,
  LPCSTR lpText
);
```




```C++
BOOL SetWindowTextW(
  HWND hwnd,
  LPCWSTR lpText
);
```



<span data-ttu-id="b7bb7-112">Wie in den [Windows-Datentypen für](windows-data-types-for-strings.md)Zeichen folgen erläutert, verwendet der generische Funktionsprototyp den Datentyp LPCTSTR für den Text Parameter.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-112">As explained in [Windows Data Types for Strings](windows-data-types-for-strings.md), the generic function prototype uses the data type LPCTSTR for the text parameter.</span></span> <span data-ttu-id="b7bb7-113">Allerdings wird für den Windows-Codeseitenprototyp der Typ LPCSTR und für den Unicode-Prototyp der Typ LPCWSTR verwendet.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-113">However, the Windows code page prototype uses the type LPCSTR, and the Unicode prototype uses LPCWSTR.</span></span>

<span data-ttu-id="b7bb7-114">Für alle Funktionen mit Textargumenten sollten Anwendungen normalerweise die generischen Funktionsprototypen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-114">For all functions with text arguments, applications should normally use the generic function prototypes.</span></span> <span data-ttu-id="b7bb7-115">Wenn eine Anwendung "Unicode" vor den **\# include** -Anweisungen für die Header Dateien oder während der Kompilierung definiert, werden die Anweisungen in Unicode-Funktionen kompiliert.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-115">If an application defines "UNICODE" either before the **\#include** statements for the header files or during compilation, the statements will be compiled into Unicode functions.</span></span>

> [!Note]  
> <span data-ttu-id="b7bb7-116">Neue Windows-Anwendungen sollten Unicode verwenden, um die Inkonsistenzen von unterschiedlichen Codepages und eine einfache Lokalisierung zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-116">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and for ease of localization.</span></span> <span data-ttu-id="b7bb7-117">Sie sollten mit generischen Funktionen geschrieben werden und müssen Unicode definieren, um die Funktionen in Unicode-Funktionen zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-117">They should be written with generic functions, and should define UNICODE to compile the functions into Unicode functions.</span></span> <span data-ttu-id="b7bb7-118">An den wenigen Stellen, an denen eine Anwendung mit 8-Bit-Zeichendaten arbeiten muss, kann Sie die Funktionen für Windows-Codepages explizit verwenden.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-118">In the few places where an application must work with 8-bit character data, it can make explicit use of the functions for Windows code pages.</span></span>

 

<span data-ttu-id="b7bb7-119">Die Anwendung sollte stets einen generischen Funktionsprototyp mit den generischen Typen für Zeichenfolgen und Zeichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-119">Your application should always use a generic function prototype with the generic string and character types.</span></span> <span data-ttu-id="b7bb7-120">Alle Funktionen, die mit dem Großbuchstaben "W" enden, nehmen Unicode-Parameter entgegen, d. h. Breitzeichen.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-120">All function names that end with an uppercase "W" take Unicode, that is, wide character, parameters.</span></span> <span data-ttu-id="b7bb7-121">Einige Funktionen sind nur in Unicode-Versionen vorhanden und können nur mit den entsprechenden Datentypen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-121">Some functions exist only in Unicode versions and can be used only with the appropriate data types.</span></span> <span data-ttu-id="b7bb7-122">Beispielsweise haben [**lcidtolocalename**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) und [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) nur Unicode-Versionen.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-122">For example, [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) and [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) have only Unicode versions.</span></span>

<span data-ttu-id="b7bb7-123">Der Abschnitt "Anforderungen" in der Referenz Dokumentation für jede Unicode-und Zeichensatz Funktion enthält Informationen zu den Funktions Versionen, die von unterstützten Betriebssystemen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-123">The Requirements section in the reference documentation for each Unicode and character set function provides information on the function versions implemented by supported operating systems.</span></span> <span data-ttu-id="b7bb7-124">Wenn eine Zeile, die mit "Unicode" beginnt, enthalten ist, verfügt die Funktion über separate Unicode-und Windows-Code Page Versionen.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-124">If a line beginning with "Unicode" is included, the function has separate Unicode and Windows code page versions.</span></span>

> [!Note]  
> <span data-ttu-id="b7bb7-125">Wenn eine Funktion einen length-Parameter für eine Zeichenfolge aufweist, muss die Länge als Anzahl von TCHAR-Werten in der Zeichenfolge dokumentiert werden.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-125">When a function has a length parameter for a character string, the length should be documented as a count of TCHAR values in the string.</span></span> <span data-ttu-id="b7bb7-126">Dieser Datentyp bezieht sich auf Bytes für Windows-Code Page Versionen der-Funktion oder 16-Bit-Wörter für Unicode-Versionen.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-126">This data type refers to bytes for Windows code page versions of the function or 16-bit words for Unicode versions.</span></span> <span data-ttu-id="b7bb7-127">Funktionen, die Zeiger auf nicht typisierte Speicherblöcke benötigen oder zurückgeben, z. b. die [**globalbelegc**](/windows/win32/api/winbase/nf-winbase-globalalloc) -Funktion, nehmen jedoch im Allgemeinen eine Größe in Byte, unabhängig vom verwendeten Prototyp.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-127">However, functions that require or return pointers to untyped memory blocks, such as the [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) function, generally take a size in bytes, regardless of the prototype that is used.</span></span> <span data-ttu-id="b7bb7-128">Wenn die Zuordnung von nicht typisiertem Speicher für eine Zeichenfolge gilt, muss die Anwendung die Anzahl der Zeichen mit sizeof (TCHAR) multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="b7bb7-128">If the allocation of untyped memory is for a string, the application must multiply the number of characters by sizeof(TCHAR).</span></span> <span data-ttu-id="b7bb7-129">Weitere Informationen finden Sie unter [Verwenden von generischen Datentypen](using-generic-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="b7bb7-129">For additional information, see [Using Generic Data Types](using-generic-data-types.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b7bb7-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b7bb7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7bb7-131">Unicode in der Windows-API</span><span class="sxs-lookup"><span data-stu-id="b7bb7-131">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
