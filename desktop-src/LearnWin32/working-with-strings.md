---
title: Arbeiten mit Zeichenfolgen
description: Arbeiten mit Zeichenfolgen
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1850d531a1cff713ec71a7e96399f029794545db9b695abe5b826ed63f0f080
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075200"
---
# <a name="working-with-strings"></a>Arbeiten mit Zeichenfolgen

Windows unterstützt nativ Unicode-Zeichenfolgen für Benutzeroberflächenelemente, Dateinamen usw. Unicode ist die bevorzugte Zeichencodierung, da sie alle Zeichensätze und Sprachen unterstützt. Windows stellt Unicode-Zeichen mit UTF-16-Codierung dar, bei der jedes Zeichen als 16-Bit-Wert codiert wird. UTF-16-Zeichen werden als *Breitzeichen* bezeichnet, um sie von 8-Bit-ANSI-Zeichen zu unterscheiden. Der Visual C++-Compiler unterstützt den integrierten Datentyp **wchar \_ t** für Breitzeichen. Die Headerdatei WinNT.h definiert auch die folgende **Typedef.**


```C++
typedef wchar_t WCHAR;
```



Sie sehen beide Versionen im MSDN-Beispielcode. Um ein Breitzeichenliteral oder ein Breitzeichen-Zeichenfolgenliteral zu deklarieren, setzen **Sie L** vor das Literal.


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



Hier sind einige andere zeichenfolgenbezogene Typdefinitionen, die Sie sehen werden:



| TypeDef                   | Definition       |
|---------------------------|------------------|
| **CHAR**                  | `char`           |
| **PSTR oder** **LPSTR**     | `char*`          |
| **PCSTR** oder **LPCSTR**   | `const char*`    |
| **PWSTR** oder **LPWSTR**   | `wchar_t*`       |
| **PCWSTR** oder **LPCWSTR** | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a>Unicode- und ANSI-Funktionen

Als Microsoft Unicode-Unterstützung für Windows eingeführt hat, wurde der Übergang vereinfacht, indem zwei parallele Sätze von APIs zur Verfügung stellten: eine für ANSI-Zeichenfolgen und die andere für Unicode-Zeichenfolgen. Beispielsweise gibt es zwei Funktionen, um den Text der Titelleiste eines Fensters zu festlegen:

-   **SetWindowTextA verwendet** eine ANSI-Zeichenfolge.
-   **SetWindowTextW verwendet** eine Unicode-Zeichenfolge.

Intern übersetzt die ANSI-Version die Zeichenfolge in Unicode. Die Windows-Header definieren auch ein Makro, das in die Unicode-Version auflöset, wenn das Präprozessorsymbol definiert ist, andernfalls die `UNICODE` ANSI-Version.


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



In MSDN ist die Funktion unter dem Namen [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta)dokumentiert, obwohl dies tatsächlich der Makroname und nicht der tatsächliche Funktionsname ist.

Neue Anwendungen sollten immer die Unicode-Versionen aufrufen. Viele Weltsprachen erfordern Unicode. Wenn Sie ANSI-Zeichenfolgen verwenden, ist es unmöglich, Ihre Anwendung zu lokalisieren. Die ANSI-Versionen sind ebenfalls weniger effizient, da das Betriebssystem die ANSI-Zeichenfolgen zur Laufzeit in Unicode konvertieren muss. Je nach Ihren Einstellungen können Sie die Unicode-Funktionen explizit aufrufen, z. B. **SetWindowTextW,** oder die Makros verwenden. Der Beispielcode auf MSDN ruft in der Regel die Makros auf, aber die beiden Formen sind genau äquivalent. Die meisten neueren APIs in Windows verfügen nur über eine Unicode-Version ohne entsprechende ANSI-Version.

## <a name="tchars"></a>TCHARs

Wenn Anwendungen sowohl Windows NT als auch Windows 95, Windows 98 und Windows Me unterstützen mussten, war es hilfreich, je nach Zielplattform den gleichen Code für ANSI- oder Unicode-Zeichenfolgen zu kompilieren. Zu diesem Zweck stellt das Windows SDK Makros bereit, die Zeichenfolgen je nach Plattform Unicode oder ANSI zuordnen.



| Makro     | Unicode   | ANSI   |
|-----------|-----------|--------|
| TCHAR     | `wchar_t` | `char` |
| TEXT("x") | `L"x"`    | `"x"`  |



 

Beispielsweise folgender Code:


```C++
SetWindowText(TEXT("My Application"));
```



wird in eine der folgenden Auflösungen behoben:


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



Die **Makros TEXT** und **TCHAR** sind derzeit weniger nützlich, da alle Anwendungen Unicode verwenden sollten. Sie werden jedoch möglicherweise in älterem Code und in einigen MSDN-Codebeispielen verwendet.

Die Header für die Microsoft C-Laufzeitbibliotheken definieren einen ähnlichen Satz von Makros. Beispielsweise wird **\_ tcslen** in **strlen** auflösen, wenn nicht definiert ist. Andernfalls wird es in `_UNICODE` **wcslenaufgelöset.** Dies ist die Breitzeichenversion von **strlen**.


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



Seien Sie vorsichtig: Einige Header verwenden das Präprozessorsymbol, `UNICODE` andere verwenden mit einem `_UNICODE` Unterstrichpräfix. Definieren Sie immer beide Symbole. Visual C++ werden beide standardmäßig festgelegt, wenn Sie ein neues Projekt erstellen.

## <a name="next"></a>Nächste

[Was ist ein Fenster?](what-is-a-window-.md)

 

 
