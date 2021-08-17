---
description: Die meisten Zeichenfolgenvorgänge können dieselbe Logik für Unicode und Windows Codepages verwenden.
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: Windows-Datentypen für Zeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a2bef3dc98b7b8649b6cb0fc5bd9450c6f22c8b2bb6e3345790dab0dd24587f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146813"
---
# <a name="windows-data-types-for-strings"></a>Windows-Datentypen für Zeichenfolgen

Die meisten Zeichenfolgenvorgänge können dieselbe Logik für [Unicode](unicode.md) und Windows [Codepages verwenden.](code-pages.md) Der einzige Unterschied ist, dass die grundlegende Vorgangseinheit ein 16-Bit-Zeichen (auch als Breitzeichen bezeichnet) für Unicode und ein 8-Bit-Zeichen für Windows Codepages ist. Die Windows-Headerdateien stellen mehrere Typdefinitionen zur Verfügung, die das Erstellen von Quellen, die für Unicode oder für codepages Windows können, einfach machen.

Windows unterstützt drei Sätze von Zeichen- und Zeichenfolgendatentypen: einen Satz generischer Typdefinitionen, die entweder für Unicode- oder Windows-Codepages kompiliert werden können, und zwei Sätze spezifischer Typdefinitionen. Ein Satz spezifischer Typdefinitionen ist für die Verwendung mit Unicode und der andere für die Verwendung mit Windows Codepages.

Eine Anwendung, die generische Datentypen verwendet, kann für Unicode kompiliert werden, indem einfach "UNICODE" vor den **\# Include-Anweisungen** für die Headerdateien oder während der Kompilierung definiert wird. Neue Windows sollten Unicode verwenden, um inkonsistente Codepages zu vermeiden und die Lokalisierung zu vereinfachen. Sie sollten mit generischen Datentypen geschrieben werden und "UNICODE" definieren, um diese Typen in Unicode-Typen zu kompilieren. An den wenigen Stellen, an denen eine Anwendung mit 8-Bit-Zeichendaten arbeiten muss, kann sie explizit die Typen für Windows verwenden.

Die Möglichkeit zum Kompilieren der generischen Typen in Typen für Windows Codepages besteht hauptsächlich zur Unterstützung von Legacyanwendungen. Um für Windows Codepages zu kompilieren, lässt die Anwendung nur die UNICODE-Definition aus.

Das folgende Beispiel zeigt die -Methode, die in Windows Headerdateien verwendet wird, um die drei Sätze von Datentypen zu definieren. Informationen zur Implementierung finden Sie in der Headerdatei Winnt.h.


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



Der Buchstabe "T" in einer Typdefinition, z. B. TCHAR oder LPTSTR, bezeichnet einen generischen Typ, der für Windows Codepages oder Unicode kompiliert werden kann. Der Buchstabe "W" in einer Typdefinition, z. B. WCHAR oder LPWSTR, bezeichnet einen Unicode-Typ. Da Windows Codepages die ältere Form haben, verfügen sie über einfache Typdefinitionen wie CHAR und LPSTR. Eine vollständige Beschreibung der Datentypen in Windows finden Sie unter [Windows Datentypen](../winprog/windows-data-types.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unicode in der Windows-API](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
