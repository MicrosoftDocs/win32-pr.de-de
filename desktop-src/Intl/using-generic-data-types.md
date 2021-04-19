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
# <a name="using-generic-data-types"></a>Verwenden von generischen Datentypen

Wenn Sie generische Datentypen in Ihrem Code verwenden, können Sie [Sie einfach mit](unicode.md) einer Präprozessordirektive kompilieren, um "Unicode" vor den **\# include** -Anweisungen für die Header Dateien zu definieren. Um den Code für [Windows (ANSI)-Codepages](code-pages.md)zu kompilieren, lassen Sie die Unicode-Definition aus. Neue Windows-Anwendungen sollten Unicode verwenden, um Inkonsistenzen von unterschiedlichen Codepages zu vermeiden und die Lokalisierung

So erstellen Sie Quellcode, der entweder zur Verwendung von Unicode-Zeichen und Zeichen folgen oder zum Verwenden von Zeichen und Zeichen folgen aus Windows-Codepages kompiliert werden kann:

1.  Verwenden Sie generische Datentypen, z. b. TCHAR, LPTStr und lptch, für alle Zeichen-und Zeichen folgen Typen, die für Text verwendet werden. Weitere Informationen zu generischen Typen finden Sie unter [Windows-Datentypen für](windows-data-types-for-strings.md)Zeichen folgen.
2.  Stellen Sie sicher, dass Zeiger auf nicht Text-Datenpuffer oder binäre Byte Arrays mit Datentypen wie LPBYTE oder lpword anstelle des LPTStr-oder lptch-Typs codiert werden.
3.  Deklarieren Sie Zeiger des unbestimmten Typs explizit als void-Zeiger mithilfe von LPVOID, wenn dies erforderlich ist.
4.  Legen Sie einen arithmetischen Zeiger vom Typ unabhängig. Die Verwendung von Einheiten der TCHAR-Größe ergibt Variablen mit 2 Bytes, wenn Unicode definiert ist, und 1 Byte, wenn Unicode nicht definiert ist. Die Verwendung von Zeigerarithmetik gibt immer die Anzahl der Elemente zurück, die durch den Zeiger angegeben werden, unabhängig davon, ob die Elemente 1 oder 2 Bytes groß sind. Der folgende Ausdruck ruft immer die Anzahl der Elemente ab, unabhängig davon, ob Unicode definiert ist.

    ```C++
    cCount = lpEnd - lpStart;
    ```

    

    Der folgende Ausdruck bestimmt die Anzahl der verwendeten Bytes.

    ```C++
    cByteCount = (lpEnd - lpStart) * sizeof(TCHAR);
    ```

    

    Es ist nicht erforderlich, eine Anweisung wie die folgende zu ändern, da die zeigerinkrement auf das nächste Zeichen Element zeigt.

    ```C++
    chNext = *++lpText;
    ```

    

5.  Ersetzen Sie Literalzeichenfolgen und Manifest-Zeichen Konstanten durch Makros. Ändern Sie Ausdrücke wie die folgende.

    ```C++
    while(*lpFileName++ != '\\')
    {
        // ...
    }
    ```

    

    Verwenden Sie das [**Text**](/windows/desktop/api/Winnt/nf-winnt-text) Makro wie folgt in diesem Ausdruck.

    ```C++
    while(*lpFileName++ != TEXT('\\'))
    {
        // ...
    }
    ```

    

    Das [**Text**](/windows/desktop/api/Winnt/nf-winnt-text) Makro bewirkt, dass Zeichen folgen als L "String" ausgewertet werden, wenn Unicode definiert ist, andernfalls als "String". Um die Verwaltung zu vereinfachen, verschieben Sie Literalzeichenfolgen in Ressourcen, insbesondere dann, wenn Sie Zeichen außerhalb des ASCII-Bereichs (0x00 bis 0x7F) enthalten oder auf der Benutzeroberfläche verfügbar gemacht werden. Um die Lokalisierung Ihrer Anwendung für verschiedene nationale Sprachen zu unterstützen, ist es sehr wichtig, dass sich alle Benutzeroberflächen-Zeichen folgen in lokalisierbaren Ressourcen befinden.

6.  Verwenden Sie die generischen Versionen der Windows-Funktionen. Weitere Informationen finden Sie unter [Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md).
7.  Verwenden Sie die generischen Versionen der Standardfunktionen der c-Bibliotheks Zeichenfolge, und denken Sie daran, " \_ Unicode" und "Unicode" zu definieren, wie in [Standard-C-Funktionen](standard-c-functions.md)erläutert.
8.  Wenn Sie eine Anwendung anpassen, die ursprünglich für Windows-Codepages geschrieben wurde, denken Sie daran, Code zu ändern, der auf 255 als größten Wert für ein Zeichen basiert.

Wenn Sie Code kompilieren, den Sie wie oben beschrieben geschrieben haben, kann der Compiler sowohl Unicode-als auch Windows-Code Page Versionen der Anwendung aus derselben Quelle erstellen. Abhängig von den Definitionen für Unicode werden die generischen Funktionen aufgelöst, um dieselben Binärdateien zu erhalten, als wenn Sie Code exklusiv für Unicode oder exklusiv für Windows-Codepages geschrieben haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Unicode und Zeichensätzen](using-unicode-and-character-sets.md)
</dt> </dl>

 

 



