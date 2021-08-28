---
description: Das Windows SDK stellt Funktionsprototypen in generischen, Windows Codepage und Unicode-Versionen bereit.
ms.assetid: 601d24b0-11bb-48fa-a257-207c3acee226
title: Konventionen für Funktionsprototypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd37171ed4cd1f0f00267b935ec57f17ef2957514b63d770efdc851b9c08bb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746140"
---
# <a name="conventions-for-function-prototypes"></a>Konventionen für Funktionsprototypen

Das Windows SDK stellt Funktionsprototypen in generischen, Windows [Codepage und](code-pages.md) [Unicode-Versionen](unicode.md) bereit. Die Prototypen können kompiliert werden, um entweder Windows Codepageprototypen oder Unicode-Prototypen zu erzeugen. Alle drei Prototypen werden in diesem Thema erläutert und in Codebeispielen für die [**SetWindowText-Funktion**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) veranschaulicht.

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



Der Präprozessor erweitert das Makro entweder in die Windows Codepage oder in den Unicode-Funktionsnamen. Der Buchstabe "A" (ANSI) oder "W" (Unicode) wird am Ende des generischen Funktionsnamens entsprechend hinzugefügt. Die Headerdatei stellt dann zwei spezifische Prototypen zur Verfügung: einen für Windows Codepages und einen für Unicode, wie in den folgenden Beispielen gezeigt.


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



Wie in Windows Data Types for Strings (Datentypen für [Zeichenfolgen)](windows-data-types-for-strings.md)erläutert, verwendet der Prototyp der generischen Funktion den Datentyp LPCTSTR für den Textparameter. Allerdings wird für den Windows-Codeseitenprototyp der Typ LPCSTR und für den Unicode-Prototyp der Typ LPCWSTR verwendet.

Für alle Funktionen mit Textargumenten sollten Anwendungen normalerweise die generischen Funktionsprototypen verwenden. Wenn eine Anwendung "UNICODE" entweder vor den **\# Include-Anweisungen** für die Headerdateien oder während der Kompilierung definiert, werden die Anweisungen in Unicode-Funktionen kompiliert.

> [!Note]  
> Neue Windows sollten Unicode verwenden, um inkonsistente Codepages zu vermeiden und die Lokalisierung zu erleichtern. Sie sollten mit generischen Funktionen geschrieben werden und UNICODE definieren, um die Funktionen in Unicode-Funktionen zu kompilieren. An den wenigen Stellen, an denen eine Anwendung mit 8-Bit-Zeichendaten arbeiten muss, kann sie explizit die Funktionen für Windows verwenden.

 

Die Anwendung sollte stets einen generischen Funktionsprototyp mit den generischen Typen für Zeichenfolgen und Zeichen verwenden. Alle Funktionen, die mit dem Großbuchstaben "W" enden, nehmen Unicode-Parameter entgegen, d. h. Breitzeichen. Einige Funktionen sind nur in Unicode-Versionen vorhanden und können nur mit den entsprechenden Datentypen verwendet werden. Beispielsweise verfügen [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) und [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) nur über Unicode-Versionen.

Der Abschnitt Anforderungen in der Referenzdokumentation für jede Unicode- und Zeichensatzfunktion enthält Informationen zu den Funktionsversionen, die von unterstützten Betriebssystemen implementiert werden. Wenn eine Zeile enthalten ist, die mit "Unicode" beginnt, verfügt die Funktion über separate Unicode- und Windows Codepageversionen.

> [!Note]  
> Wenn eine Funktion über einen Length-Parameter für eine Zeichenfolge verfügt, sollte die Länge als Anzahl von TCHAR-Werten in der Zeichenfolge dokumentiert werden. Dieser Datentyp bezieht sich auf Bytes für Windows Codepageversionen der Funktion oder 16-Bit-Wörter für Unicode-Versionen. Funktionen, die Zeiger auf nicht typisierte Speicherblöcke erfordern oder zurückgeben, z. B. die [**GlobalAlloc-Funktion,**](/windows/win32/api/winbase/nf-winbase-globalalloc) haben jedoch in der Regel eine Größe in Bytes, unabhängig vom verwendeten Prototyp. Wenn die Zuordnung von nicht typisiertem Speicher für eine Zeichenfolge gilt, muss die Anwendung die Anzahl der Zeichen mit sizeof(TCHAR) multiplizieren. Weitere Informationen finden Sie unter [Verwenden generischer Datentypen.](using-generic-data-types.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unicode in der Windows-API](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
