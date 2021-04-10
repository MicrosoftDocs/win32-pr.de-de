---
description: Die meisten Zeichen folgen Operationen können die gleiche Logik für Unicode und für Windows-Codepages verwenden.
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: Windows-Datentypen für Zeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e24be1024736ce324e040e58f6ac45636a11d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050606"
---
# <a name="windows-data-types-for-strings"></a>Windows-Datentypen für Zeichenfolgen

Die meisten Zeichen folgen Operationen können die gleiche Logik für [Unicode](unicode.md) und für [Windows-Codepages](code-pages.md)verwenden. Der einzige Unterschied besteht darin, dass die grundlegende Betriebseinheit ein 16-Bit-Zeichen (auch als breit Zeichen bezeichnet) für Unicode und ein 8-Bit-Zeichen für Windows-Codepages ist. Die Windows-Header Dateien bieten mehrere Typdefinitionen, die das Erstellen von Quellen erleichtern, die für Unicode oder für Windows-Codepages kompiliert werden können.

Windows unterstützt drei Sätze von Zeichen-und Zeichen folgen Datentypen: eine Reihe von generischen Typdefinitionen, die für Unicode-oder Windows-Codepages und zwei Sätze spezifischer Typdefinitionen kompiliert werden können. Ein Satz spezifischer Typdefinitionen dient zur Verwendung mit Unicode, der andere für die Verwendung mit Windows-Codepages.

Eine Anwendung, die generische Datentypen verwendet, kann einfach durch Definieren von "Unicode" vor den **\# include** -Anweisungen für die Header Dateien oder während der Kompilierung kompiliert werden. Neue Windows-Anwendungen sollten Unicode verwenden, um Inkonsistenzen von verschiedenen Codepages zu vermeiden und die Lokalisierung zu vereinfachen. Sie sollten mit generischen Datentypen geschrieben werden und sollten "Unicode" definieren, damit diese Typen in Unicode-Typen kompiliert werden können. An den wenigen Stellen, an denen eine Anwendung mit 8-Bit-Zeichendaten arbeiten muss, kann Sie die Typen für Windows-Codepages explizit verwenden.

Die Möglichkeit zum Kompilieren der generischen Typen in Typen für Windows-Codepages besteht hauptsächlich darin, ältere Anwendungen zu unterstützen. Zur Kompilierung für Windows-Codepages lässt die Anwendung lediglich die Unicode-Definition aus.

Das folgende Beispiel zeigt die-Methode, die in den Windows-Header Dateien zum Definieren der drei Sätze von Datentypen verwendet wird. Informationen zur Implementierung finden Sie in der Header Datei "Winnt. h".


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



Der Buchstabe "T" in einer Typdefinition, z. b. TCHAR oder LPTSTR, legt einen generischen Typ fest, der für Windows-Codepages oder Unicode kompiliert werden kann. Der Buchstabe "W" in einer Typdefinition, z. b. "WCHAR" oder "LPWSTR", bezeichnet einen Unicode-Typ. Da Windows-Codepages die ältere Form aufweisen, verfügen Sie über einfache Typdefinitionen, wie z. b. Char und LPStr. Eine umfassende Beschreibung der Datentypen in Windows finden Sie unter [Windows-Datentypen](../winprog/windows-data-types.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unicode in der Windows-API](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
