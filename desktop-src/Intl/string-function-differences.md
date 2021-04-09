---
description: In diesem Thema werden die Unterschiede zwischen Zeichen folgen Funktionen beschrieben, die beim Verarbeiten von Unicode-und Zeichensatz Informationen Diese Funktionen verfügen sowohl über Unicode-als auch über Windows-Code Page Implementierungen zur Unterstützung von Unicode-und Windows-Code Page Parametern
ms.assetid: 52a15957-b44b-49ba-b915-e5c8e003a7e6
title: Unterschiede in Zeichen folgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c940aa8be1603f7958fb1993cc521ca7b1ed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959352"
---
# <a name="string-function-differences"></a>Unterschiede in Zeichen folgen

In diesem Thema werden die Unterschiede zwischen Zeichen folgen Funktionen beschrieben, die beim Verarbeiten von Unicode-und Zeichensatz Informationen Diese Funktionen verfügen sowohl über [Unicode](unicode.md) -als auch über [Windows-Code Page](code-pages.md) Implementierungen zur Unterstützung von Unicode-und Windows-Code Page Parametern

Die folgenden Zeichen folgen Funktionen erfordern keinen speziellen Kommentar. Ihre Unicode-und Windows-Codepage-Implementierungen funktionieren identisch.

-   [**Charnext**](/windows/win32/api/winuser/nf-winuser-charnexta)
-   [**Charprev**](/windows/win32/api/winuser/nf-winuser-charpreva)
-   [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [ **stringcchkatin**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)
-   [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [ **stringcchcopyex**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa)
-   " [**Straucblength**](/windows/win32/api/strsafe/nf-strsafe-stringcblengtha)", " [ **Strauch Länge** "](/windows/win32/api/strsafe/nf-strsafe-stringcchlengtha)

Der von einer der Funktionen der Zeichen folgen Länge abgerufene Längen Wert basiert immer auf der normalen Zeichenbreite: 8 Bits für Windows-Codepages, 16 Bits für Unicode. Dieser Wert wird häufig als "Anzahl von Zeichen" bezeichnet. Dieser Begriff ist streng richtig, da Windows-Codepages, die [Doppelbyte-Zeichensätze](double-byte-character-sets.md) (dbcss) verwenden, über einige Zeichen in voller Breite verfügen, die tatsächlich durch zwei aufeinander folgende Bytes dargestellt werden. Eine ähnliche Situation tritt bei [Surrogates](surrogates-and-supplementary-characters.md) in Unicode auf.

Die folgenden Zeichen folgen Funktionen sind sensibel für das Gebiets Schema des aktuellen Threads, abgeleitet von der Sprache, die der Benutzer in der Systemsteuerung auswählt. Die [**lstraucmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) -und [**lstrecmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) -Funktionen führen keine Byte Vergleiche wie deren ANSI-nameseln aus, z. b. " [straucmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp)". Stattdessen vergleichen Sie Zeichen folgen gemäß den Regeln des Gebiets Schemas.

-   [**Charlower**](/windows/win32/api/winuser/nf-winuser-charlowera)
-   [**Charlowerbuff**](/windows/win32/api/winuser/nf-winuser-charlowerbuffa)
-   [**Charupper**](/windows/win32/api/winuser/nf-winuser-charuppera)
-   [**Charupperbuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
-   [**lstraucmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)
-   [**lstraucmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)

Die folgenden Funktionen konvertieren in Abhängigkeit davon, welche Version verwendet wird, zwischen dem OEM-Zeichensatz und der aktuellen Windows-Codepage oder dem Unicode-Unicode-Zeichensatz:

-   [**Charper OEM**](/windows/win32/api/winuser/nf-winuser-chartooema)
-   [**Chartoken**](/windows/win32/api/winuser/nf-winuser-chartooembuffa)
-   [**Oemzu charbuff**](/windows/win32/api/winuser/nf-winuser-oemtocharbuffa)

Die Druckfunktionen, z. b. [**stringcbprintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), unterstützen Unicode, indem die folgenden neuen und geänderten Datentypen in ihren Formatspezifikationen bereitgestellt werden. Diese Formatspezifikationen beeinflussen die Art und Weise, in der die Funktionen den entsprechenden Eingabeparameter interpretieren.



| Formatspezifikation | Datentyp für Windows-Codepage-Version | Datentyp für Unicode-Version |
|----------------------|-----------------------------------------|-------------------------------|
| c                    | CHAR                                    | WCHAR                         |
| C                    | WCHAR                                   | CHAR                          |
| HC, HC               | CHAR                                    | CHAR                          |
| HS, HS               | LPSTR                                   | LPSTR                         |
| LC, LC               | WCHAR                                   | WCHAR                         |
| ls, ls               | LPWSTR                                  | LPWSTR                        |
| s                    | LPSTR                                   | LPWSTR                        |
| E                    | LPWSTR                                  | LPSTR                         |



 

Der Datentyp für den Ausgabetext hängt immer von der Version der Funktion ab. Wenn der Datentyp des Eingabe Parameters und des Datentyps des Ausgabe Texts nicht übereinstimmen, führt die Druckfunktion eine Konvertierung von Unicode zur aktuellen Windows-Codepage durch oder umgekehrt.

Bei der Unicode-Version der Druckfunktionen ist die Format Zeichenfolge Unicode, ebenso wie der Ausgabetext.

> [!Caution]  
> Eine schlechte Puffer Behandlung ist in vielen Sicherheitsproblemen enthalten, die Pufferüberläufe einschließen. Weitere Informationen finden Sie unter [Referenz](../menurc/strsafe-ovw.md)zu "" Die in "strausafe. h" definierten Funktionen bieten zusätzliche Verarbeitungsschritte für die ordnungsgemäße Puffer Behandlung in Ihrem Code. Aus diesem Grund sind Sie zum Ersetzen Ihrer integrierten C/C++-Gegenstücke sowie bestimmter Microsoft Windows-Implementierungen vorgesehen. Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unicode in der Windows-API](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
