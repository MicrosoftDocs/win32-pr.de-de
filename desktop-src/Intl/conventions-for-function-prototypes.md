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
# <a name="conventions-for-function-prototypes"></a>Konventionen für Funktionsprototypen

Der Windows SDK stellt Funktionsprototypen in generischen, [Windows-Codepage](code-pages.md)-und [Unicode](unicode.md) -Versionen bereit. Die Prototypen können kompiliert werden, um entweder Windows-Code Page Prototypen oder Unicode-Prototypen zu erstellen. Alle drei Prototypen werden in diesem Thema erläutert und in den Codebeispielen für die Funktion " [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) " veranschaulicht.

Im Folgenden finden Sie ein Beispiel eines generischen Prototyps:


```C++
BOOL SetWindowText(
  HWND hwnd,
  LPCTSTR lpText
);
```



Die Headerdatei enthält den generischen Funktionsnamen als Makro implementiert.


```C++
#ifdef UNICODE
#define SetWindowText SetWindowTextW
#else
#define SetWindowText SetWindowTextA
#endif // !UNICODE
```



Der Präprozessor erweitert das Makro entweder in den Windows-Codepage-oder Unicode-Funktionsnamen. Der Buchstabe "A" (ANSI) oder "W" (Unicode) wird nach Bedarf am Ende des generischen Funktionsnamens hinzugefügt. Die Header Datei enthält dann zwei spezifische Prototypen, eine für Windows-Codepages und eine für Unicode, wie in den folgenden Beispielen gezeigt.


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



Wie in den [Windows-Datentypen für](windows-data-types-for-strings.md)Zeichen folgen erläutert, verwendet der generische Funktionsprototyp den Datentyp LPCTSTR für den Text Parameter. Allerdings wird für den Windows-Codeseitenprototyp der Typ LPCSTR und für den Unicode-Prototyp der Typ LPCWSTR verwendet.

Für alle Funktionen mit Textargumenten sollten Anwendungen normalerweise die generischen Funktionsprototypen verwenden. Wenn eine Anwendung "Unicode" vor den **\# include** -Anweisungen für die Header Dateien oder während der Kompilierung definiert, werden die Anweisungen in Unicode-Funktionen kompiliert.

> [!Note]  
> Neue Windows-Anwendungen sollten Unicode verwenden, um die Inkonsistenzen von unterschiedlichen Codepages und eine einfache Lokalisierung zu vermeiden. Sie sollten mit generischen Funktionen geschrieben werden und müssen Unicode definieren, um die Funktionen in Unicode-Funktionen zu kompilieren. An den wenigen Stellen, an denen eine Anwendung mit 8-Bit-Zeichendaten arbeiten muss, kann Sie die Funktionen für Windows-Codepages explizit verwenden.

 

Die Anwendung sollte stets einen generischen Funktionsprototyp mit den generischen Typen für Zeichenfolgen und Zeichen verwenden. Alle Funktionen, die mit dem Großbuchstaben "W" enden, nehmen Unicode-Parameter entgegen, d. h. Breitzeichen. Einige Funktionen sind nur in Unicode-Versionen vorhanden und können nur mit den entsprechenden Datentypen verwendet werden. Beispielsweise haben [**lcidtolocalename**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) und [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) nur Unicode-Versionen.

Der Abschnitt "Anforderungen" in der Referenz Dokumentation für jede Unicode-und Zeichensatz Funktion enthält Informationen zu den Funktions Versionen, die von unterstützten Betriebssystemen implementiert werden. Wenn eine Zeile, die mit "Unicode" beginnt, enthalten ist, verfügt die Funktion über separate Unicode-und Windows-Code Page Versionen.

> [!Note]  
> Wenn eine Funktion einen length-Parameter für eine Zeichenfolge aufweist, muss die Länge als Anzahl von TCHAR-Werten in der Zeichenfolge dokumentiert werden. Dieser Datentyp bezieht sich auf Bytes für Windows-Code Page Versionen der-Funktion oder 16-Bit-Wörter für Unicode-Versionen. Funktionen, die Zeiger auf nicht typisierte Speicherblöcke benötigen oder zurückgeben, z. b. die [**globalbelegc**](/windows/win32/api/winbase/nf-winbase-globalalloc) -Funktion, nehmen jedoch im Allgemeinen eine Größe in Byte, unabhängig vom verwendeten Prototyp. Wenn die Zuordnung von nicht typisiertem Speicher für eine Zeichenfolge gilt, muss die Anwendung die Anzahl der Zeichen mit sizeof (TCHAR) multiplizieren. Weitere Informationen finden Sie unter [Verwenden von generischen Datentypen](using-generic-data-types.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unicode in der Windows-API](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
