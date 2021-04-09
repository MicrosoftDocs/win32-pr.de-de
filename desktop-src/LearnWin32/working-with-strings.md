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
# <a name="working-with-strings"></a>Arbeiten mit Zeichenfolgen

Windows unterstützt nativ Unicode-Zeichen folgen für Benutzeroberflächen Elemente, Dateinamen usw. Unicode ist die bevorzugte Zeichencodierung, da Sie alle Zeichensätze und Sprachen unterstützt. Windows stellt Unicode-Zeichen mithilfe der UTF-16-Codierung dar, in der jedes Zeichen als 16-Bit-Wert codiert wird. UTF-16-Zeichen werden als *breit* Zeichen bezeichnet, um Sie von 8-Bit-ANSI-Zeichen zu unterscheiden. Der Visual C++-Compiler unterstützt den integrierten Datentyp **WCHAR \_ t** für breit Zeichen. Die Header Datei "Winnt. h" definiert auch die folgende **typedef**.


```C++
typedef wchar_t WCHAR;
```



Beide Versionen werden im MSDN-Beispielcode angezeigt. Zum Deklarieren eines breit Zeichenliterals oder eines breit Zeichenfolgenliterals geben Sie **L** vor dem Literalzeichen ein.


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



Im folgenden finden Sie einige weitere Typdefinitionen für Zeichen folgen, die Sie sehen werden:



| TypeDef                   | Definition       |
|---------------------------|------------------|
| **CHAR**                  | `char`           |
| **Pstr** oder **LPSTR**     | `char*`          |
| **Pcstr** oder **LPCSTR**   | `const char*`    |
| **Pwstr** oder **LPWSTR**   | `wchar_t*`       |
| **Pcwstr** oder **LPCWSTR** | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a>Unicode-und ANSI-Funktionen

Wenn Microsoft Unicode-Unterstützung für Windows eingeführt hat, wurde der Übergang durch Bereitstellung von zwei parallelen Sätzen von APIs gelockert, eine für ANSI-Zeichen folgen und die andere für Unicode-Zeichen folgen. Beispielsweise gibt es zwei Funktionen, um den Text der Titelleiste eines Fensters festzulegen:

-   **Setwindowtexta** nimmt eine ANSI-Zeichenfolge an.
-   **Setwindowtextw** nimmt eine Unicode-Zeichenfolge an.

Intern übersetzt die ANSI-Version die Zeichenfolge in Unicode. Die Windows-Header definieren auch ein Makro, das in die Unicode-Version aufgelöst wird, wenn das Präprozessorsymbol `UNICODE` definiert ist, oder andernfalls die ANSI-Version.


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



In MSDN ist die-Funktion unter dem Namen [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta)dokumentiert, obwohl dies tatsächlich der Makro Name und nicht der tatsächliche Funktionsname ist.

Neue Anwendungen sollten immer die Unicode-Versionen abrufen. Viele Weltsprachen erfordern Unicode. Wenn Sie ANSI-Zeichen folgen verwenden, kann die Anwendung nicht lokalisiert werden. Die ANSI-Versionen sind ebenfalls weniger effizient, da das Betriebssystem die ANSI-Zeichen folgen zur Laufzeit in Unicode konvertieren muss. Abhängig von ihrer Einstellung können Sie die Unicode-Funktionen explizit aufrufen, z. b. **setwindowtextw**, oder Sie verwenden die Makros. Der Beispielcode auf MSDN ruft in der Regel die Makros auf, aber beide Formen sind genau gleichwertig. Die meisten neueren APIs in Windows verfügen nur über eine Unicode-Version ohne entsprechende ANSI-Version.

## <a name="tchars"></a>Tchars

Wenn Anwendungen sowohl Windows NT als auch Windows 95, Windows 98 und Windows Me unterstützen müssen, war es hilfreich, den gleichen Code für ANSI-oder Unicode-Zeichen folgen abhängig von der Zielplattform zu kompilieren. Zu diesem Zweck stellt die Windows SDK Makros bereit, die Zeichen folgen in Abhängigkeit von der Plattform Unicode oder ANSI zuordnen.



| Makro     | Unicode   | ANSI   |
|-----------|-----------|--------|
| TCHAR     | `wchar_t` | `char` |
| Text ("x") | `L"x"`    | `"x"`  |



 

Beispielsweise folgender Code:


```C++
SetWindowText(TEXT("My Application"));
```



löst einen der folgenden Schritte aus:


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



Die **Text** -und **TCHAR** -Makros sind heute weniger nützlich, da alle Anwendungen Unicode verwenden sollten. Möglicherweise werden Sie jedoch in einem älteren Code und in einigen der MSDN-Codebeispiele angezeigt.

Die Header für die Microsoft C-Laufzeitbibliotheken definieren einen ähnlichen Satz von Makros. Beispielsweise wird **\_ tcslen** in " **straulen** " aufgelöst, wenn nicht `_UNICODE` definiert ist. andernfalls wird es in " **wcslen**" aufgelöst, d. h. die breit Zeichen Version von " **strinlen**".


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



Seien Sie vorsichtig: einige Header verwenden das Präprozessorsymbol `UNICODE` , `_UNICODE` von anderen Benutzern mit einem Unterstrich-Präfix. Definieren Sie immer beide Symbole. Visual C++ legt diese standardmäßig fest, wenn Sie ein neues Projekt erstellen.

## <a name="next"></a>Nächste

[Was ist ein Fenster?](what-is-a-window-.md)

 

 