---
title: Arbeiten mit Zeichenfolgen
description: Arbeiten mit Zeichenfolgen
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4661c6b07a267d90e0fca05d04354c018be04527
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110968"
---
# <a name="working-with-strings"></a><span data-ttu-id="a5f7c-103">Arbeiten mit Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="a5f7c-103">Working with Strings</span></span>

<span data-ttu-id="a5f7c-104">Windows unterstützt nativ Unicode-Zeichenfolgen für Benutzeroberflächenelemente, Dateinamen usw.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-104">Windows natively supports Unicode strings for UI elements, file names, and so forth.</span></span> <span data-ttu-id="a5f7c-105">Unicode ist die bevorzugte Zeichencodierung, da alle Zeichensätze und Sprachen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-105">Unicode is the preferred character encoding, because it supports all character sets and languages.</span></span> <span data-ttu-id="a5f7c-106">Windows stellt Unicode-Zeichen mit UTF-16-Codierung dar, in der jedes Zeichen als 16-Bit-Wert codiert wird.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-106">Windows represents Unicode characters using UTF-16 encoding, in which each character is encoded as a 16-bit value.</span></span> <span data-ttu-id="a5f7c-107">UTF-16-Zeichen werden als *Breitzeichen* bezeichnet, um sie von 8-Bit-ANSI-Zeichen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-107">UTF-16 characters are called *wide* characters, to distinguish them from 8-bit ANSI characters.</span></span> <span data-ttu-id="a5f7c-108">Der Visual C++ Compiler unterstützt den integrierten Datentyp **wchar \_ t** für Breitzeichen.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-108">The Visual C++ compiler supports the built-in data type **wchar\_t** for wide characters.</span></span> <span data-ttu-id="a5f7c-109">Die Headerdatei WinNT.h definiert auch die folgende **Typedef.**</span><span class="sxs-lookup"><span data-stu-id="a5f7c-109">The header file WinNT.h also defines the following **typedef**.</span></span>


```C++
typedef wchar_t WCHAR;
```



<span data-ttu-id="a5f7c-110">Beide Versionen werden im MSDN-Beispielcode angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-110">You will see both versions in MSDN example code.</span></span> <span data-ttu-id="a5f7c-111">Um ein Breitzeichenliteral oder ein Zeichenfolgenliteral mit Breitzeichen zu deklarieren, setzen Sie **L** vor das Literal.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-111">To declare a wide-character literal or a wide-character string literal, put **L** before the literal.</span></span>


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



<span data-ttu-id="a5f7c-112">Im Folgenden finden Sie einige weitere zeichenfolgenbezogene Typedefs:</span><span class="sxs-lookup"><span data-stu-id="a5f7c-112">Here are some other string-related typedefs that you will see:</span></span>



| <span data-ttu-id="a5f7c-113">TypeDef</span><span class="sxs-lookup"><span data-stu-id="a5f7c-113">Typedef</span></span>                   | <span data-ttu-id="a5f7c-114">Definition</span><span class="sxs-lookup"><span data-stu-id="a5f7c-114">Definition</span></span>       |
|---------------------------|------------------|
| <span data-ttu-id="a5f7c-115">**CHAR**</span><span class="sxs-lookup"><span data-stu-id="a5f7c-115">**CHAR**</span></span>                  | `char`           |
| <span data-ttu-id="a5f7c-116">**PSTR** oder **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="a5f7c-116">**PSTR** or **LPSTR**</span></span>     | `char*`          |
| <span data-ttu-id="a5f7c-117">**PCSTR** oder **LPCSTR**</span><span class="sxs-lookup"><span data-stu-id="a5f7c-117">**PCSTR** or **LPCSTR**</span></span>   | `const char*`    |
| <span data-ttu-id="a5f7c-118">**PWSTR** oder **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a5f7c-118">**PWSTR** or **LPWSTR**</span></span>   | `wchar_t*`       |
| <span data-ttu-id="a5f7c-119">**PCWSTR** oder **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="a5f7c-119">**PCWSTR** or **LPCWSTR**</span></span> | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a><span data-ttu-id="a5f7c-120">Unicode- und ANSI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a5f7c-120">Unicode and ANSI Functions</span></span>

<span data-ttu-id="a5f7c-121">Als Microsoft Die Unicode-Unterstützung für Windows eingeführt hat, wurde der Übergang vereinfacht, indem zwei parallele APIs zur Verfügung gestellt wurden: eine für ANSI-Zeichenfolgen und die andere für Unicode-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-121">When Microsoft introduced Unicode support to Windows, it eased the transition by providing two parallel sets of APIs, one for ANSI strings and the other for Unicode strings.</span></span> <span data-ttu-id="a5f7c-122">Es gibt beispielsweise zwei Funktionen, um den Text der Titelleiste eines Fensters festzulegen:</span><span class="sxs-lookup"><span data-stu-id="a5f7c-122">For example, there are two functions to set the text of a window's title bar:</span></span>

-   <span data-ttu-id="a5f7c-123">**SetWindowTextA** verwendet eine ANSI-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-123">**SetWindowTextA** takes an ANSI string.</span></span>
-   <span data-ttu-id="a5f7c-124">**SetWindowTextW** verwendet eine Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-124">**SetWindowTextW** takes a Unicode string.</span></span>

<span data-ttu-id="a5f7c-125">Intern übersetzt die ANSI-Version die Zeichenfolge in Unicode.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-125">Internally, the ANSI version translates the string to Unicode.</span></span> <span data-ttu-id="a5f7c-126">Die Windows-Header definieren auch ein Makro, das in die Unicode-Version aufgelöst wird, wenn das Präprozessorsymbol `UNICODE` definiert ist, oder andernfalls die ANSI-Version.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-126">The Windows headers also define a macro that resolves to the Unicode version when the preprocessor symbol `UNICODE` is defined or the ANSI version otherwise.</span></span>


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



<span data-ttu-id="a5f7c-127">In MSDN ist die Funktion unter dem Namen [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta)dokumentiert, obwohl dies tatsächlich der Makroname und nicht der tatsächliche Funktionsname ist.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-127">In MSDN, the function is documented under the name [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), even though that is really the macro name, not the actual function name.</span></span>

<span data-ttu-id="a5f7c-128">Neue Anwendungen sollten immer die Unicode-Versionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-128">New applications should always call the Unicode versions.</span></span> <span data-ttu-id="a5f7c-129">Viele Weltsprachen erfordern Unicode.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-129">Many world languages require Unicode.</span></span> <span data-ttu-id="a5f7c-130">Wenn Sie ANSI-Zeichenfolgen verwenden, ist es unmöglich, Ihre Anwendung zu lokalisieren.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-130">If you use ANSI strings, it will be impossible to localize your application.</span></span> <span data-ttu-id="a5f7c-131">Die ANSI-Versionen sind ebenfalls weniger effizient, da das Betriebssystem die ANSI-Zeichenfolgen zur Laufzeit in Unicode konvertieren muss.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-131">The ANSI versions are also less efficient, because the operating system must convert the ANSI strings to Unicode at run time.</span></span> <span data-ttu-id="a5f7c-132">Je nach Ihren Einstellungen können Sie die Unicode-Funktionen explizit aufrufen, z. B. **SetWindowTextW,** oder die Makros verwenden.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-132">Depending on your preference, you can call the Unicode functions explicitly, such as **SetWindowTextW**, or use the macros.</span></span> <span data-ttu-id="a5f7c-133">Der Beispielcode auf MSDN ruft in der Regel die Makros auf, aber die beiden Formen sind genau äquivalent.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-133">The example code on MSDN typically calls the macros, but the two forms are exactly equivalent.</span></span> <span data-ttu-id="a5f7c-134">Die meisten neueren APIs in Windows verfügen nur über eine Unicode-Version ohne entsprechende ANSI-Version.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-134">Most newer APIs in Windows have just a Unicode version, with no corresponding ANSI version.</span></span>

## <a name="tchars"></a><span data-ttu-id="a5f7c-135">TCHARs</span><span class="sxs-lookup"><span data-stu-id="a5f7c-135">TCHARs</span></span>

<span data-ttu-id="a5f7c-136">Wenn Anwendungen sowohl Windows NT als auch Windows 95, Windows 98 und Windows Me unterstützen mussten, war es hilfreich, je nach Zielplattform den gleichen Code für ANSI- oder Unicode-Zeichenfolgen zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-136">Back when applications needed to support both Windows NT as well as Windows 95, Windows 98, and Windows Me, it was useful to compile the same code for either ANSI or Unicode strings, depending on the target platform.</span></span> <span data-ttu-id="a5f7c-137">Zu diesem Zweck stellt Windows SDK Makros zur Verfügung, die Zeichenfolgen je nach Plattform Unicode oder ANSI zuordnen.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-137">To this end, the Windows SDK provides macros that map strings to Unicode or ANSI, depending on the platform.</span></span>



| <span data-ttu-id="a5f7c-138">Makro</span><span class="sxs-lookup"><span data-stu-id="a5f7c-138">Macro</span></span>     | <span data-ttu-id="a5f7c-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="a5f7c-139">Unicode</span></span>   | <span data-ttu-id="a5f7c-140">ANSI</span><span class="sxs-lookup"><span data-stu-id="a5f7c-140">ANSI</span></span>   |
|-----------|-----------|--------|
| <span data-ttu-id="a5f7c-141">TCHAR</span><span class="sxs-lookup"><span data-stu-id="a5f7c-141">TCHAR</span></span>     | `wchar_t` | `char` |
| <span data-ttu-id="a5f7c-142">TEXT("x")</span><span class="sxs-lookup"><span data-stu-id="a5f7c-142">TEXT("x")</span></span> | `L"x"`    | `"x"`  |



 

<span data-ttu-id="a5f7c-143">Beispielsweise folgender Code:</span><span class="sxs-lookup"><span data-stu-id="a5f7c-143">For example, the following code:</span></span>


```C++
SetWindowText(TEXT("My Application"));
```



<span data-ttu-id="a5f7c-144">wird in eine der folgenden Auflösungen behoben:</span><span class="sxs-lookup"><span data-stu-id="a5f7c-144">resolves to one of the following:</span></span>


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



<span data-ttu-id="a5f7c-145">Die **Makros TEXT** und **TCHAR** sind derzeit weniger nützlich, da alle Anwendungen Unicode verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-145">The **TEXT** and **TCHAR** macros are less useful today, because all applications should use Unicode.</span></span> <span data-ttu-id="a5f7c-146">Sie werden jedoch möglicherweise in älterem Code und in einigen MSDN-Codebeispielen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-146">However, you might see them in older code and in some of the MSDN code examples.</span></span>

<span data-ttu-id="a5f7c-147">Die Header für die Microsoft C-Laufzeitbibliotheken definieren einen ähnlichen Satz von Makros.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-147">The headers for the Microsoft C run-time libraries define a similar set of macros.</span></span> <span data-ttu-id="a5f7c-148">Beispielsweise wird **\_ tcslen** in **strlen** auflösen, wenn nicht definiert ist. Andernfalls wird es in `_UNICODE` **wcslenaufgelöset.** Dies ist die Breitzeichenversion von **strlen**.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-148">For example, **\_tcslen** resolves to **strlen** if `_UNICODE` is undefined; otherwise it resolves to **wcslen**, which is the wide-character version of **strlen**.</span></span>


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



<span data-ttu-id="a5f7c-149">Seien Sie vorsichtig: Einige Header verwenden das Präprozessorsymbol, `UNICODE` andere verwenden mit einem `_UNICODE` Unterstrichpräfix.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-149">Be careful: Some headers use the preprocessor symbol `UNICODE`, others use `_UNICODE` with an underscore prefix.</span></span> <span data-ttu-id="a5f7c-150">Definieren Sie immer beide Symbole.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-150">Always define both symbols.</span></span> <span data-ttu-id="a5f7c-151">Visual C++ werden beide standardmäßig festgelegt, wenn Sie ein neues Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="a5f7c-151">Visual C++ sets them both by default when you create a new project.</span></span>

## <a name="next"></a><span data-ttu-id="a5f7c-152">Nächste</span><span class="sxs-lookup"><span data-stu-id="a5f7c-152">Next</span></span>

[<span data-ttu-id="a5f7c-153">Was ist ein Fenster?</span><span class="sxs-lookup"><span data-stu-id="a5f7c-153">What Is a Window?</span></span>](what-is-a-window-.md)

 

 
