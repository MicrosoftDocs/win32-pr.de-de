---
title: Arbeiten mit Zeichenfolgen
description: .
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c74530a1acd0eb94f0d88662924203a8c58116
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101550"
---
# <a name="working-with-strings"></a><span data-ttu-id="7251b-103">Arbeiten mit Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="7251b-103">Working with Strings</span></span>

<span data-ttu-id="7251b-104">Windows unterstützt nativ Unicode-Zeichen folgen für Benutzeroberflächen Elemente, Dateinamen usw.</span><span class="sxs-lookup"><span data-stu-id="7251b-104">Windows natively supports Unicode strings for UI elements, file names, and so forth.</span></span> <span data-ttu-id="7251b-105">Unicode ist die bevorzugte Zeichencodierung, da Sie alle Zeichensätze und Sprachen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7251b-105">Unicode is the preferred character encoding, because it supports all character sets and languages.</span></span> <span data-ttu-id="7251b-106">Windows stellt Unicode-Zeichen mithilfe der UTF-16-Codierung dar, in der jedes Zeichen als 16-Bit-Wert codiert wird.</span><span class="sxs-lookup"><span data-stu-id="7251b-106">Windows represents Unicode characters using UTF-16 encoding, in which each character is encoded as a 16-bit value.</span></span> <span data-ttu-id="7251b-107">UTF-16-Zeichen werden als *breit* Zeichen bezeichnet, um Sie von 8-Bit-ANSI-Zeichen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="7251b-107">UTF-16 characters are called *wide* characters, to distinguish them from 8-bit ANSI characters.</span></span> <span data-ttu-id="7251b-108">Der Visual C++-Compiler unterstützt den integrierten Datentyp **WCHAR \_ t** für breit Zeichen.</span><span class="sxs-lookup"><span data-stu-id="7251b-108">The Visual C++ compiler supports the built-in data type **wchar\_t** for wide characters.</span></span> <span data-ttu-id="7251b-109">Die Header Datei "Winnt. h" definiert auch die folgende **typedef**.</span><span class="sxs-lookup"><span data-stu-id="7251b-109">The header file WinNT.h also defines the following **typedef**.</span></span>


```C++
typedef wchar_t WCHAR;
```



<span data-ttu-id="7251b-110">Beide Versionen werden im MSDN-Beispielcode angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7251b-110">You will see both versions in MSDN example code.</span></span> <span data-ttu-id="7251b-111">Zum Deklarieren eines breit Zeichenliterals oder eines breit Zeichenfolgenliterals geben Sie **L** vor dem Literalzeichen ein.</span><span class="sxs-lookup"><span data-stu-id="7251b-111">To declare a wide-character literal or a wide-character string literal, put **L** before the literal.</span></span>


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



<span data-ttu-id="7251b-112">Im folgenden finden Sie einige weitere Typdefinitionen für Zeichen folgen, die Sie sehen werden:</span><span class="sxs-lookup"><span data-stu-id="7251b-112">Here are some other string-related typedefs that you will see:</span></span>



| <span data-ttu-id="7251b-113">TypeDef</span><span class="sxs-lookup"><span data-stu-id="7251b-113">Typedef</span></span>                   | <span data-ttu-id="7251b-114">Definition</span><span class="sxs-lookup"><span data-stu-id="7251b-114">Definition</span></span>       |
|---------------------------|------------------|
| <span data-ttu-id="7251b-115">**CHAR**</span><span class="sxs-lookup"><span data-stu-id="7251b-115">**CHAR**</span></span>                  | `char`           |
| <span data-ttu-id="7251b-116">**Pstr** oder **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="7251b-116">**PSTR** or **LPSTR**</span></span>     | `char*`          |
| <span data-ttu-id="7251b-117">**Pcstr** oder **LPCSTR**</span><span class="sxs-lookup"><span data-stu-id="7251b-117">**PCSTR** or **LPCSTR**</span></span>   | `const char*`    |
| <span data-ttu-id="7251b-118">**Pwstr** oder **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7251b-118">**PWSTR** or **LPWSTR**</span></span>   | `wchar_t*`       |
| <span data-ttu-id="7251b-119">**Pcwstr** oder **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="7251b-119">**PCWSTR** or **LPCWSTR**</span></span> | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a><span data-ttu-id="7251b-120">Unicode-und ANSI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7251b-120">Unicode and ANSI Functions</span></span>

<span data-ttu-id="7251b-121">Wenn Microsoft Unicode-Unterstützung für Windows eingeführt hat, wurde der Übergang durch Bereitstellung von zwei parallelen Sätzen von APIs gelockert, eine für ANSI-Zeichen folgen und die andere für Unicode-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="7251b-121">When Microsoft introduced Unicode support to Windows, it eased the transition by providing two parallel sets of APIs, one for ANSI strings and the other for Unicode strings.</span></span> <span data-ttu-id="7251b-122">Beispielsweise gibt es zwei Funktionen, um den Text der Titelleiste eines Fensters festzulegen:</span><span class="sxs-lookup"><span data-stu-id="7251b-122">For example, there are two functions to set the text of a window's title bar:</span></span>

-   <span data-ttu-id="7251b-123">**Setwindowtexta** nimmt eine ANSI-Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="7251b-123">**SetWindowTextA** takes an ANSI string.</span></span>
-   <span data-ttu-id="7251b-124">**Setwindowtextw** nimmt eine Unicode-Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="7251b-124">**SetWindowTextW** takes a Unicode string.</span></span>

<span data-ttu-id="7251b-125">Intern übersetzt die ANSI-Version die Zeichenfolge in Unicode.</span><span class="sxs-lookup"><span data-stu-id="7251b-125">Internally, the ANSI version translates the string to Unicode.</span></span> <span data-ttu-id="7251b-126">Die Windows-Header definieren auch ein Makro, das in die Unicode-Version aufgelöst wird, wenn das Präprozessorsymbol `UNICODE` definiert ist, oder andernfalls die ANSI-Version.</span><span class="sxs-lookup"><span data-stu-id="7251b-126">The Windows headers also define a macro that resolves to the Unicode version when the preprocessor symbol `UNICODE` is defined or the ANSI version otherwise.</span></span>


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



<span data-ttu-id="7251b-127">In MSDN ist die-Funktion unter dem Namen [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta)dokumentiert, obwohl dies tatsächlich der Makro Name und nicht der tatsächliche Funktionsname ist.</span><span class="sxs-lookup"><span data-stu-id="7251b-127">In MSDN, the function is documented under the name [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), even though that is really the macro name, not the actual function name.</span></span>

<span data-ttu-id="7251b-128">Neue Anwendungen sollten immer die Unicode-Versionen abrufen.</span><span class="sxs-lookup"><span data-stu-id="7251b-128">New applications should always call the Unicode versions.</span></span> <span data-ttu-id="7251b-129">Viele Weltsprachen erfordern Unicode.</span><span class="sxs-lookup"><span data-stu-id="7251b-129">Many world languages require Unicode.</span></span> <span data-ttu-id="7251b-130">Wenn Sie ANSI-Zeichen folgen verwenden, kann die Anwendung nicht lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7251b-130">If you use ANSI strings, it will be impossible to localize your application.</span></span> <span data-ttu-id="7251b-131">Die ANSI-Versionen sind ebenfalls weniger effizient, da das Betriebssystem die ANSI-Zeichen folgen zur Laufzeit in Unicode konvertieren muss.</span><span class="sxs-lookup"><span data-stu-id="7251b-131">The ANSI versions are also less efficient, because the operating system must convert the ANSI strings to Unicode at run time.</span></span> <span data-ttu-id="7251b-132">Abhängig von ihrer Einstellung können Sie die Unicode-Funktionen explizit aufrufen, z. b. **setwindowtextw**, oder Sie verwenden die Makros.</span><span class="sxs-lookup"><span data-stu-id="7251b-132">Depending on your preference, you can call the Unicode functions explicitly, such as **SetWindowTextW**, or use the macros.</span></span> <span data-ttu-id="7251b-133">Der Beispielcode auf MSDN ruft in der Regel die Makros auf, aber beide Formen sind genau gleichwertig.</span><span class="sxs-lookup"><span data-stu-id="7251b-133">The example code on MSDN typically calls the macros, but the two forms are exactly equivalent.</span></span> <span data-ttu-id="7251b-134">Die meisten neueren APIs in Windows verfügen nur über eine Unicode-Version ohne entsprechende ANSI-Version.</span><span class="sxs-lookup"><span data-stu-id="7251b-134">Most newer APIs in Windows have just a Unicode version, with no corresponding ANSI version.</span></span>

## <a name="tchars"></a><span data-ttu-id="7251b-135">Tchars</span><span class="sxs-lookup"><span data-stu-id="7251b-135">TCHARs</span></span>

<span data-ttu-id="7251b-136">Wenn Anwendungen sowohl Windows NT als auch Windows 95, Windows 98 und Windows Me unterstützen müssen, war es hilfreich, den gleichen Code für ANSI-oder Unicode-Zeichen folgen abhängig von der Zielplattform zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="7251b-136">Back when applications needed to support both Windows NT as well as Windows 95, Windows 98, and Windows Me, it was useful to compile the same code for either ANSI or Unicode strings, depending on the target platform.</span></span> <span data-ttu-id="7251b-137">Zu diesem Zweck stellt die Windows SDK Makros bereit, die Zeichen folgen in Abhängigkeit von der Plattform Unicode oder ANSI zuordnen.</span><span class="sxs-lookup"><span data-stu-id="7251b-137">To this end, the Windows SDK provides macros that map strings to Unicode or ANSI, depending on the platform.</span></span>



| <span data-ttu-id="7251b-138">Makro</span><span class="sxs-lookup"><span data-stu-id="7251b-138">Macro</span></span>     | <span data-ttu-id="7251b-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="7251b-139">Unicode</span></span>   | <span data-ttu-id="7251b-140">ANSI</span><span class="sxs-lookup"><span data-stu-id="7251b-140">ANSI</span></span>   |
|-----------|-----------|--------|
| <span data-ttu-id="7251b-141">TCHAR</span><span class="sxs-lookup"><span data-stu-id="7251b-141">TCHAR</span></span>     | `wchar_t` | `char` |
| <span data-ttu-id="7251b-142">Text ("x")</span><span class="sxs-lookup"><span data-stu-id="7251b-142">TEXT("x")</span></span> | `L"x"`    | `"x"`  |



 

<span data-ttu-id="7251b-143">Beispielsweise folgender Code:</span><span class="sxs-lookup"><span data-stu-id="7251b-143">For example, the following code:</span></span>


```C++
SetWindowText(TEXT("My Application"));
```



<span data-ttu-id="7251b-144">löst einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="7251b-144">resolves to one of the following:</span></span>


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



<span data-ttu-id="7251b-145">Die **Text** -und **TCHAR** -Makros sind heute weniger nützlich, da alle Anwendungen Unicode verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="7251b-145">The **TEXT** and **TCHAR** macros are less useful today, because all applications should use Unicode.</span></span> <span data-ttu-id="7251b-146">Möglicherweise werden Sie jedoch in einem älteren Code und in einigen der MSDN-Codebeispiele angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7251b-146">However, you might see them in older code and in some of the MSDN code examples.</span></span>

<span data-ttu-id="7251b-147">Die Header für die Microsoft C-Laufzeitbibliotheken definieren einen ähnlichen Satz von Makros.</span><span class="sxs-lookup"><span data-stu-id="7251b-147">The headers for the Microsoft C run-time libraries define a similar set of macros.</span></span> <span data-ttu-id="7251b-148">Beispielsweise wird **\_ tcslen** in " **straulen** " aufgelöst, wenn nicht `_UNICODE` definiert ist. andernfalls wird es in " **wcslen**" aufgelöst, d. h. die breit Zeichen Version von " **strinlen**".</span><span class="sxs-lookup"><span data-stu-id="7251b-148">For example, **\_tcslen** resolves to **strlen** if `_UNICODE` is undefined; otherwise it resolves to **wcslen**, which is the wide-character version of **strlen**.</span></span>


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



<span data-ttu-id="7251b-149">Seien Sie vorsichtig: einige Header verwenden das Präprozessorsymbol `UNICODE` , `_UNICODE` von anderen Benutzern mit einem Unterstrich-Präfix.</span><span class="sxs-lookup"><span data-stu-id="7251b-149">Be careful: Some headers use the preprocessor symbol `UNICODE`, others use `_UNICODE` with an underscore prefix.</span></span> <span data-ttu-id="7251b-150">Definieren Sie immer beide Symbole.</span><span class="sxs-lookup"><span data-stu-id="7251b-150">Always define both symbols.</span></span> <span data-ttu-id="7251b-151">Visual C++ legt diese standardmäßig fest, wenn Sie ein neues Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="7251b-151">Visual C++ sets them both by default when you create a new project.</span></span>

## <a name="next"></a><span data-ttu-id="7251b-152">Nächste</span><span class="sxs-lookup"><span data-stu-id="7251b-152">Next</span></span>

[<span data-ttu-id="7251b-153">Was ist ein Fenster?</span><span class="sxs-lookup"><span data-stu-id="7251b-153">What Is a Window?</span></span>](what-is-a-window-.md)

 

 