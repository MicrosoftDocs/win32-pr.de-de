---
description: Wenn Sie generische Datentypen in Ihrem Code verwenden, kann er für Unicode kompiliert werden, indem einfach eine Präprozessordirektive verwendet wird, um &\# 0034 zu definieren. UNICODE&\# 0034; vor den \# include-Anweisungen für die Headerdateien.
ms.assetid: 1c9cbb18-9295-4847-86c1-d596668cbe57
title: Verwenden generischer Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a61bed094506f0d31718b0b88fe519028ba1db785ebda3e00404a7aa3257e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535461"
---
# <a name="using-generic-data-types"></a>Verwenden generischer Datentypen

Wenn Sie generische Datentypen in Ihrem Code verwenden, kann er für [Unicode](unicode.md) kompiliert werden, indem einfach eine Präprozessordirektive verwendet wird, um "UNICODE" vor den **\# include-Anweisungen** für die Headerdateien zu definieren. Um den Code für [Windows (ANSI)-Codepages](code-pages.md)zu kompilieren, lassen Sie die UNICODE-Definition aus. Neue Windows Anwendungen sollten Unicode verwenden, um die Inkonsistenzen verschiedener Codepages zu vermeiden und die Lokalisierung zu vereinfachen.

So erstellen Sie Quellcode, der entweder kompiliert werden kann, um Unicode-Zeichen und -Zeichenfolgen zu verwenden, oder um Zeichen und Zeichenfolgen aus Windows Codepages zu verwenden:

1.  Verwenden Sie generische Datentypen wie TCHAR, LPTSTR und LPTCH für alle Zeichen- und Zeichenfolgentypen, die für Text verwendet werden. Weitere Informationen zu generischen Typen finden Sie unter [Windows Datentypen für Zeichenfolgen.](windows-data-types-for-strings.md)
2.  Stellen Sie sicher, dass Zeiger auf Nicht-Text-Datenpuffer oder binäre Bytearrays mit Datentypen wie LPBYTE oder LPWORD anstelle des LPTSTR- oder LPTCH-Typs codiert werden.
3.  Deklarieren Sie Zeiger des unbestimmten Typs explizit als void-Zeiger, indem Sie LPVOID entsprechend verwenden.
4.  Sorgen Sie dafür, dass zeigerarithmetische Typen unabhängig sind. Die Verwendung von Einheiten der TCHAR-Größe ergibt Variablen, die 2 Bytes sind, wenn UNICODE definiert ist, und 1 Byte, wenn UNICODE nicht definiert ist. Die Zeigerarithmetik gibt immer die Anzahl der vom Zeiger angegebenen Elemente zurück, unabhängig davon, ob die Elemente 1 oder 2 Bytes groß sind. Der folgende Ausdruck ruft immer die Anzahl der Elemente ab, unabhängig davon, ob UNICODE definiert ist.

    ```C++
    cCount = lpEnd - lpStart;
    ```

    

    Der folgende Ausdruck bestimmt die Anzahl der verwendeten Bytes.

    ```C++
    cByteCount = (lpEnd - lpStart) * sizeof(TCHAR);
    ```

    

    Es ist nicht erforderlich, eine Anweisung wie die folgende zu ändern, da das Zeigerinkrement auf das nächste Zeichenelement zeigt.

    ```C++
    chNext = *++lpText;
    ```

    

5.  Ersetzen Sie Literalzeichenfolgen und Manifestzeichenkonstanten durch Makros. Ändern Sie Ausdrücke wie die folgende.

    ```C++
    while(*lpFileName++ != '\\')
    {
        // ...
    }
    ```

    

    Verwenden Sie das [**TEXT-Makro**](/windows/desktop/api/Winnt/nf-winnt-text) wie folgt in diesem Ausdruck.

    ```C++
    while(*lpFileName++ != TEXT('\\'))
    {
        // ...
    }
    ```

    

    Das [**TEXT-Makro**](/windows/desktop/api/Winnt/nf-winnt-text) bewirkt, dass Zeichenfolgen als L"string" ausgewertet werden, wenn UNICODE definiert ist, und andernfalls als "string". Verschieben Sie Literalzeichenfolgen zur einfacheren Verwaltung in Ressourcen, insbesondere, wenn sie Zeichen außerhalb des ASCII-Bereichs (0x00 bis 0x7F) enthalten oder auf der Benutzeroberfläche verfügbar gemacht werden. Um die Lokalisierung Ihrer Anwendung für verschiedene nationale Sprachen zu unterstützen, ist es sehr wichtig, dass sich alle Zeichenfolgen der Benutzeroberfläche in lokalisierbaren Ressourcen befindet.

6.  Verwenden Sie die generischen Versionen der Windows-Funktionen. Weitere Informationen finden Sie unter [Konventionen für Funktionsprototypen.](conventions-for-function-prototypes.md)
7.  Verwenden Sie die generischen Versionen der Zeichenfolgenfunktionen der C-Standardbibliothek, und denken Sie daran, \_ "UNICODE" und "UNICODE" zu definieren, wie in [C-Standardfunktionen](standard-c-functions.md)erläutert.
8.  Wenn Sie eine Anwendung anpassen, die ursprünglich für Windows Codepages geschrieben wurde, denken Sie daran, code, der auf 255 basiert, als größten Wert für ein Zeichen zu ändern.

Wenn Sie Code kompilieren, den Sie wie oben beschrieben geschrieben haben, kann der Compiler sowohl Unicode- als auch Windows Codepageversionen Ihrer Anwendung aus derselben Quelle erstellen. Abhängig von den Definitionen für UNICODE werden die generischen Funktionen aufgelöst, um die gleichen Binärdateien zu erzeugen, als würden Sie Code ausschließlich für Unicode oder ausschließlich für Windows Codepages schreiben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Unicode und Zeichensätzen](using-unicode-and-character-sets.md)
</dt> </dl>

 

 



