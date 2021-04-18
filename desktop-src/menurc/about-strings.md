---
title: Informationen über Zeichenfolgen
description: In diesem Thema werden Zeichen folgen Funktionen erläutert.
ms.assetid: f1799fbf-4619-4b19-998e-b1d2f4c19a35
keywords:
- Ressourcen, Zeichen folgen
- Zeichenfolgen
- Zeichenfolgenfunktionen (string-Funktionen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff9fa6c9d93ba2f5c089b52b56816cad74bb61c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339876"
---
# <a name="about-strings"></a>Informationen über Zeichenfolgen

Mit den Zeichen folgen Funktionen können Anwendungen Zeichen folgen kopieren, vergleichen, sortieren, formatieren und konvertieren sowie die Möglichkeit, den Zeichentyp der einzelnen Zeichen in einer Zeichenfolge zu bestimmen. Alle Zeichen folgen Funktionen unterstützen die Einzel Byte-, Doppelbyte-und Unicode-Zeichensätze, wenn diese Zeichensätze von dem Betriebssystem unterstützt werden, auf dem die Anwendung ausgeführt wird.

**Sicherheitswarnung:** Die falsche Verwendung von Zeichen folgen Funktionen kann zu Sicherheitsproblemen für Ihre Anwendung führen. Dies umfasst in der Regel einen Pufferüberlauf, der einen Denial-of-Service-Angriff gegen Ihre Anwendung oder die Injektion von ausführbarem Code von einem Angreifer zulässt. Die strsafe-Funktionen ermöglichen die sicherere Behandlung von Zeichen folgen und werden empfohlen, um die Sicherheit Ihrer Anwendung zu verbessern. Weitere Informationen zu diesen Funktionen finden Sie unter [Verwenden der "stresafe. h](strsafe-ovw.md)"-Funktionen.

In diesem Abschnitt werden die folgenden Themen behandelt.

-   [Vergleich mit C-Run-Time Zeichen folgen Funktionen](#comparison-with-c-run-time-string-functions)
-   [Zeichen folgen Ressourcen](#string-resources)

## <a name="comparison-with-c-run-time-string-functions"></a>Vergleich mit C-Run-Time Zeichen folgen Funktionen

Viele Zeichen folgen Funktionen duplizieren oder verbessern vertraute Zeichen folgen Funktionen aus der Standard-C-Lauf Zeit Bibliothek (CRT). Viele der Verbesserungen ermöglichen es den Zeichen folgen Funktionen, mit Unicode oder erweiterten Zeichensätzen zu arbeiten. In der folgenden Tabelle werden die CRT-Funktionen, die Windows-Funktionen (die Unicode unterstützen, im Gegensatz zu den CRT-Funktionen) und die-Funktionen von-Funktionen aufgeführt.



| CRT-Zeichen folgen Funktion                                       | Windows-Zeichen folgen Funktion    | Strausafe-Funktion                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [strcat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019) | [**lstrincat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata) | <dl> <dt>[**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)</dt> <dt>[**stringcchcatcher**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)</dt> <dt>[**stringcbcat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)</dt> <dt>[**stringcbcr Ex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)</dt> </dl>         |
| [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp?view=vs-2019) | [**lstraucmp**](/windows/desktop/api/Winbase/nf-winbase-lstrcmpa) | (keine äquivalente Funktion)                                                                                                                                                                                                                                                                                                                                                                                  |
| [strcpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019) | [**lstrincpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya) | <dl> <dt>[**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)</dt> <dt>[**stringcchcopyex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)</dt> <dt>[**stringcbcopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)</dt> <dt>[**stringcbcopyex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)</dt> </dl> |
| [strlen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019) | [**lstrlen**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) | <dl> <dt>[**Stringcchlength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)</dt> <dt> [ **stringcblength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)</dt> </dl>                                                                                                                                                                                       |



 

Die **Funktion "** -Funktion" gibt z. b. immer die Anzahl von Bytes in einer Zeichenfolge zurück, aber die [**lstraulen**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) -Funktion gibt die Anzahl von **TCHAR** -Werten zurück, die auf Bytes für ANSI-Versionen der Funktion oder **WCHAR** -Werte für Unicode-Versionen verweisen.

Die folgenden Zeichen folgen Funktionen unterscheiden sich von Standard-C-Funktionen wie z. b. **ToLower** und **toupperin** , dass Sie mit jedem beliebigen Zeichen in einem Zeichensatz arbeiten. Mithilfe der [**charlower**](/windows/desktop/api/Winuser/nf-winuser-charlowera) -Funktion kann eine Anwendung z. b. eine Großbuchstaben-U mit einem Umlaut (ü) in einen Kleinbuchstaben (i) konvertieren. Weitere Informationen zu Zeichensätzen finden Sie unter [Einzel Byte-Zeichensätze](/windows/desktop/Intl/single-byte-character-sets).



| Funktion                               | BESCHREIBUNG                                   |
|----------------------------------------|-----------------------------------------------|
| [**Charlower**](/windows/desktop/api/Winuser/nf-winuser-charlowera)         | Konvertiert ein Zeichen oder eine Zeichenfolge in Kleinbuchstaben.  |
| [**Charlowerbuff**](/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa) | Konvertiert eine Zeichenfolge in Kleinbuchstaben.     |
| [**Charnext**](/windows/desktop/api/Winuser/nf-winuser-charnexta)           | Wechselt zum nächsten Zeichen in einer Zeichenfolge.      |
| [**Charprev**](/windows/desktop/api/Winuser/nf-winuser-charpreva)           | Wechselt zum vorangehenden Zeichen in einer Zeichenfolge. |
| [**Charupper**](/windows/desktop/api/Winuser/nf-winuser-charuppera)         | Konvertiert ein Zeichen oder eine Zeichenfolge in Großbuchstaben.  |
| [**Charupperbuff**](/windows/desktop/api/Winuser/nf-winuser-charupperbuffa) | Konvertiert eine Zeichenfolge in Großbuchstaben.               |



 

Die folgenden Zeichen folgen Funktionen treffen basierend auf der Semantik der vom Benutzer ausgewählten Sprache Determinationen bezüglich eines Zeichens. Diese Funktionen sind Unicode-fähig.



| Funktion                                         | BESCHREIBUNG                                     |
|--------------------------------------------------|-------------------------------------------------|
| [**Ischaralpha**](/windows/desktop/api/Winuser/nf-winuser-ischaralphaa)               | Bestimmt, ob ein Zeichen alphabetisch ist.   |
| [**Ischaralpha numerisch**](/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica) | Bestimmt, ob ein Zeichen alphanumerisch ist. |
| [**Ischarlower**](/windows/desktop/api/Winuser/nf-winuser-ischarlowera)               | Bestimmt, ob ein Zeichen klein geschrieben ist.    |
| [**Ischarupper**](/windows/desktop/api/Winuser/nf-winuser-ischaruppera)               | Bestimmt, ob ein Zeichen in Großbuchstaben vorliegt.    |



 

In der folgenden Tabelle sind die Unicode-Erweiterungen der standardmäßigen C-Lauf Zeitfunktionen (CRT) aufgeführt. Wie bereits erwähnt, ermöglichen die strsafe-Funktionen eine sicherere Behandlung von Zeichen folgen und werden empfohlen, um die Sicherheit Ihrer Anwendung zu verbessern.



| CRT-Standard Funktion                                       | String-Funktion                | Strausafe-Funktion                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [sprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)  | [**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)   | <dl> <dt>[**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)</dt> <dt>[**stringcchprintfex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)</dt> <dt>[**stringcbprintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)</dt> <dt>[**stringcbprintfex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)</dt> </dl>         |
| [vsprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019) | [**Wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa) | <dl> <dt>[**Stringcchvprintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)</dt> <dt>[**stringcchvprintfex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)</dt> <dt>[**stringcbvprintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)</dt> <dt>[**stringcbvprintfex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)</dt> </dl> |



 

## <a name="string-resources"></a>Zeichen folgen Ressourcen

Eine Anwendung, die Zeichen folgen in Ressourcen verwaltet, kann mit minimalem Aufwand in neue Sprachen übersetzt werden. Anstatt in den Quell Modulen nach Zeichen folgen zu suchen, können Sie einfach die Zeichen folgen in der Ressourcen Datei übersetzen und die Anwendung erneut verknüpfen. Außerdem vereinfacht die Verwendung von Zeichen folgen Ressourcen die Erstellung von Unicode-und nicht-Unicode-Versionen der Anwendung aus denselben Quelldateien.

Die [**LoadString**](/windows/desktop/api/Winuser/nf-winuser-loadstringa) -Funktion lädt eine Zeichen folgen Ressource aus der ausführbaren Datei einer Anwendung. Die [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) -Funktion lädt eine Zeichen folgen Ressource und interpretiert Formatierungsoptionen, die möglicherweise in die Zeichenfolge eingebettet sind.

Ressourcen in binärer Form werden im Unicode-Format gespeichert. Beim Laden von Ressourcen können Anwendungen mit der Unicode-Version der Ressourcen Funktionen (z. b.[**loadstringw**](/windows/desktop/api/Winuser/nf-winuser-loadstringa)) Ressourcen als Unicode-Daten abrufen.

Bei 16-Bit-Zeichen folgen Ressourcen ist 255 Zeichen die maximale Länge. Bei 32-Bit-Zeichen folgen Ressourcen ist 65535 Zeichen die maximale Länge.

 

 