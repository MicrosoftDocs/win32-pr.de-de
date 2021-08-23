---
title: Informationen über Zeichenfolgen
description: In diesem Thema werden Zeichenfolgenfunktionen erläutert.
ms.assetid: f1799fbf-4619-4b19-998e-b1d2f4c19a35
keywords:
- Ressourcen,Zeichenfolgen
- Zeichenfolgen
- Zeichenfolgenfunktionen (string-Funktionen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50f47205ec021bffaa4cb6e24aa4825177a3fc0d8546f3a14b1d4b0e0ca4271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034388"
---
# <a name="about-strings"></a>Informationen über Zeichenfolgen

Die Zeichenfolgenfunktionen bieten Anwendungen die Möglichkeit, Zeichenfolgen zu kopieren, zu vergleichen, zu sortieren, zu formatieren und zu konvertieren sowie den Zeichentyp jedes Zeichens in einer Zeichenfolge zu bestimmen. Alle Zeichenfolgenfunktionen unterstützen die Einzel byte-, Doppel-Byte- und Unicode-Zeichensätze, wenn diese Zeichensätze vom Betriebssystem unterstützt werden, unter dem die Anwendung ausgeführt wird.

**Sicherheitswarnung:** Die falsche Verwendung von Zeichenfolgenfunktionen kann zu Sicherheitsproblemen für Ihre Anwendung führen. In der Regel umfasst dies einen Pufferüberlauf, der einen Denial-of-Service-Angriff auf Ihre Anwendung oder die Einjektion von ausführbarem Code durch einen Angreifer ermöglichen kann. Die Strsafe-Funktionen ermöglichen die sicherere Behandlung von Zeichenfolgen und werden für eine bessere Sicherheit ihrer Anwendung empfohlen. Weitere Informationen zu diesen Funktionen finden Sie unter [Verwenden der Strsafe.h-Funktionen](strsafe-ovw.md).

In diesem Abschnitt werden die folgenden Themen erläutert.

-   [Vergleich mit C-Run-Time-Zeichenfolgenfunktionen](#comparison-with-c-run-time-string-functions)
-   [Zeichenfolgenressourcen](#string-resources)

## <a name="comparison-with-c-run-time-string-functions"></a>Vergleich mit C-Run-Time-Zeichenfolgenfunktionen

Viele Zeichenfolgenfunktionen duplizieren oder verbessern vertraute Zeichenfolgenfunktionen aus der C-Standard-Laufzeitbibliothek (CRT). Viele der Verbesserungen ermöglichen es den Zeichenfolgenfunktionen, mit Unicode oder erweiterten Zeichensätzen zu arbeiten. Die folgende Tabelle zeigt die CRT-Funktionen, die Windows -Funktionen (die Unicode im Gegensatz zu den CRT-Funktionen unterstützen) und die StrSafe-Funktionen.



| CRT-Zeichenfolgenfunktion                                       | Windows Zeichenfolgenfunktion    | StrSafe-Funktion                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [strcat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019) | [**lstrcat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata) | <dl> <dt>[**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)</dt> <dt>[**StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)</dt> <dt>[**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)</dt> <dt>[**StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)</dt> </dl>         |
| [Strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp?view=vs-2019) | [**lstrcmp**](/windows/desktop/api/Winbase/nf-winbase-lstrcmpa) | (keine entsprechende Funktion)                                                                                                                                                                                                                                                                                                                                                                                  |
| [strcpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019) | [**lstrcpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya) | <dl> <dt>[**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)</dt> <dt>[**StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)</dt> <dt>[**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)</dt> <dt>[**StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)</dt> </dl> |
| [strlen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019) | [**lstrlen**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) | <dl> <dt>[**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)</dt> <dt> [ **StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)</dt> </dl>                                                                                                                                                                                       |



 

Die **strlen-Funktion** gibt z. B. immer die Anzahl der Bytes in einer Zeichenfolge zurück, aber die [**lstrlen-Funktion**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) gibt die Anzahl der **TCHAR-Werte** zurück, die auf Bytes für ANSI-Versionen der Funktion oder **WCHAR-Werte** für Unicode-Versionen verweist.

Die folgenden Zeichenfolgenfunktionen unterscheiden sich von C-Standardfunktionen wie **tolower** und **toupper,** da sie für jedes Zeichen in einem Zeichensatz verwendet werden. Mithilfe der [**CharLower-Funktion**](/windows/desktop/api/Winuser/nf-winuser-charlowera) kann beispielsweise eine Anwendung ein groß geschriebenes U mit einem Umlaut (Ü) in Kleinbuchstaben (ü) konvertieren. Weitere Informationen zu Zeichensätzen finden Sie unter [Einzel-Byte-Zeichensätze.](/windows/desktop/Intl/single-byte-character-sets)



| Funktion                               | Beschreibung                                   |
|----------------------------------------|-----------------------------------------------|
| [**CharLower**](/windows/desktop/api/Winuser/nf-winuser-charlowera)         | Konvertiert ein Zeichen oder eine Zeichenfolge in Kleinbuchstaben.  |
| [**CharLowerBuff**](/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa) | Konvertiert eine Zeichenfolge in Kleinbuchstaben.     |
| [**CharNext**](/windows/desktop/api/Winuser/nf-winuser-charnexta)           | Wechselt zum nächsten Zeichen in einer Zeichenfolge.      |
| [**CharPrev**](/windows/desktop/api/Winuser/nf-winuser-charpreva)           | Wechselt zum vorangehenden Zeichen in einer Zeichenfolge. |
| [**CharUpper**](/windows/desktop/api/Winuser/nf-winuser-charuppera)         | Konvertiert ein Zeichen oder eine Zeichenfolge in Großbuchstaben.  |
| [**CharUpperBuff**](/windows/desktop/api/Winuser/nf-winuser-charupperbuffa) | Konvertiert eine Zeichenfolge in Großbuchstaben.               |



 

Die folgenden Zeichenfolgenfunktionen treffen Entscheidungen über ein Zeichen basierend auf der Semantik der vom Benutzer ausgewählten Sprache. Diese Funktionen sind unicode-fähig.



| Funktion                                         | Beschreibung                                     |
|--------------------------------------------------|-------------------------------------------------|
| [**IsCharAlpha**](/windows/desktop/api/Winuser/nf-winuser-ischaralphaa)               | Bestimmt, ob ein Zeichen alphabetisch ist.   |
| [**IsCharAlphaNumeric**](/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica) | Bestimmt, ob ein Zeichen alphanumerisch ist. |
| [**IsCharLower**](/windows/desktop/api/Winuser/nf-winuser-ischarlowera)               | Bestimmt, ob ein Zeichen aus Kleinbuchstaben besteht.    |
| [**IsCharUpper**](/windows/desktop/api/Winuser/nf-winuser-ischaruppera)               | Bestimmt, ob ein Zeichen Großbuchstaben ist.    |



 

In der folgenden Tabelle sind die Unicode-Erweiterungen für die C-Standard-Laufzeitfunktionen (CRT) aufgeführt. Wie bereits erwähnt, ermöglichen die StrSafe-Funktionen eine sicherere Behandlung von Zeichenfolgen und werden für eine bessere Sicherheit ihrer Anwendung empfohlen.



| CRT-Standardfunktion                                       | Zeichenfolgenfunktion                | StrSafe-Funktion                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [sprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)  | [**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)   | <dl> <dt>[**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)</dt> <dt>[**StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)</dt> <dt>[**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)</dt> <dt>[**StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)</dt> </dl>         |
| [vsprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019) | [**wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa) | <dl> <dt>[**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)</dt> <dt>[**StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)</dt> <dt>[**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)</dt> <dt>[**StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)</dt> </dl> |



 

## <a name="string-resources"></a>Zeichenfolgenressourcen

Eine Anwendung, die Zeichenfolgen in Ressourcen verwaltet, kann mit minimalem Aufwand in neue Sprachen übersetzt werden. Anstatt in den Quellmodulen nach Zeichenfolgen zu suchen, können Sie einfach die Zeichenfolgen in der Ressourcendatei übersetzen und die Anwendung neu verlinken. Darüber hinaus vereinfacht die Verwendung von Zeichenfolgenressourcen die Erstellung von Unicode- und Nicht-Unicode-Versionen der Anwendung aus denselben Quelldateien.

Die [**LoadString-Funktion**](/windows/desktop/api/Winuser/nf-winuser-loadstringa) lädt eine Zeichenfolgenressource aus der ausführbaren Datei einer Anwendung. Die [**FormatMessage-Funktion**](/windows/desktop/api/winbase/nf-winbase-formatmessage) lädt eine Zeichenfolgenressource und interpretiert Formatierungsoptionen, die möglicherweise in die Zeichenfolge eingebettet werden.

Ressourcen in binärer Form werden im Unicode-Format gespeichert. Beim Laden von Ressourcen können Anwendungen die Unicode-Version der Ressourcenfunktionen (z. B.[**LoadStringW)**](/windows/desktop/api/Winuser/nf-winuser-loadstringa)verwenden, um Ressourcen als Unicode-Daten zu erhalten.

Bei 16-Bit-Zeichenfolgenressourcen sind 255 Zeichen die maximale Länge. Bei 32-Bit-Zeichenfolgenressourcen sind 65535 Zeichen die maximale Länge.

 

 