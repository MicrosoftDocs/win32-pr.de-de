---
description: In diesem Thema werden die Unterschiede zwischen Zeichenfolgenfunktionen beschrieben, die bei der Behandlung von Unicode- und Zeichensatzinformationen verwendet werden. Diese Funktionen verfügen sowohl über Unicode- als auch Windows Codepageimplementierung, um Unicode- und Windows Codepageparameter zu unterstützen.
ms.assetid: 52a15957-b44b-49ba-b915-e5c8e003a7e6
title: Unterschiede bei Zeichenfolgenfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60a6208e858eceac65ac8826ffbff6303b970969cae6f635d0bcc027dd6d9f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146993"
---
# <a name="string-function-differences"></a>Unterschiede bei Zeichenfolgenfunktionen

In diesem Thema werden die Unterschiede zwischen Zeichenfolgenfunktionen beschrieben, die bei der Behandlung von Unicode- und Zeichensatzinformationen verwendet werden. Diese Funktionen verfügen sowohl [über Unicode-](unicode.md) [als auch Windows Codepageimplementierung,](code-pages.md) um Unicode- und Windows Codepageparameter zu unterstützen.

Die folgenden Zeichenfolgenfunktionen erfordern keinen speziellen Kommentar. Ihre Unicode- Windows Codepageimplementierung funktionieren identisch.

-   [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta)
-   [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva)
-   [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [ **StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)
-   [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [ **StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa)
-   [**StrCbLength,**](/windows/win32/api/strsafe/nf-strsafe-stringcblengtha) [ **StrCchLength**](/windows/win32/api/strsafe/nf-strsafe-stringcchlengtha)

Der längenwert, der von einer der Zeichenfolgenlängenfunktionen abgerufen wird, basiert immer auf der normalen Zeichenbreite: 8 Bits für Windows Codepages, 16 Bits für Unicode. Dieser Wert wird häufig als "Anzahl von Zeichen" bezeichnet. Dieser Begriff ist genau richtig, da Windows Codepages, die [Doppelbyte-Zeichensätze](double-byte-character-sets.md) (DBCSs) verwenden, einige Zeichen mit voller Breite enthalten, die tatsächlich durch zwei aufeinander folgende Bytes dargestellt werden. Eine ähnliche Situation tritt bei [Ersatzzeichen](surrogates-and-supplementary-characters.md) in Unicode auf.

Die folgenden Zeichenfolgenfunktionen sind für das -Locale des aktuellen Threads sensibel, abgeleitet von der Sprache, die der Benutzer im Systemsteuerung. Die [**Funktionen lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) und [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) führen keine Bytevergleiche durch, z. B. [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp). Stattdessen vergleichen sie Zeichenfolgen gemäß den Regeln des -Locale.

-   [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)
-   [**CharLowerBuff**](/windows/win32/api/winuser/nf-winuser-charlowerbuffa)
-   [**CharUpper**](/windows/win32/api/winuser/nf-winuser-charuppera)
-   [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
-   [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)
-   [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)

Die folgenden Funktionen konvertieren zwischen dem OEM-Zeichensatz und der aktuellen Windows Codepage oder Unicode, je nachdem, welche Version verwendet wird:

-   [**CharToOem**](/windows/win32/api/winuser/nf-winuser-chartooema)
-   [**CharToOemBuff**](/windows/win32/api/winuser/nf-winuser-chartooembuffa)
-   [**OemToCharBuff**](/windows/win32/api/winuser/nf-winuser-oemtocharbuffa)

Die Druckfunktionen, z. B. [**StringCbPrintf,**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa)unterstützen Unicode, indem sie die folgenden neuen und geänderten Datentypen in ihren Formatspezifikationen bereitstellen. Diese Formatspezifikationen beeinflussen die Interpretation des entsprechenden Eingabeparameters durch die Funktionen.



| Formatspezifikation | Datentyp für Windows-Codepageversion | Datentyp für Unicode-Version |
|----------------------|-----------------------------------------|-------------------------------|
| c                    | CHAR                                    | WCHAR                         |
| C                    | WCHAR                                   | CHAR                          |
| hc, hC               | CHAR                                    | CHAR                          |
| hs, hS               | LPSTR                                   | LPSTR                         |
| lc, lC               | WCHAR                                   | WCHAR                         |
| ls, lS               | LPWSTR                                  | LPWSTR                        |
| s                    | LPSTR                                   | LPWSTR                        |
| E                    | LPWSTR                                  | LPSTR                         |



 

Der Datentyp für den Ausgabetext hängt immer von der Version der Funktion ab. Wenn der Datentyp des Eingabeparameters und der Datentyp des Ausgabetexts nicht stimmen, führt die print-Funktion bei Bedarf eine Konvertierung von Unicode in die aktuelle Windows-Codepage oder umgekehrt durch.

Für die Unicode-Version der Druckfunktionen ist die Formatzeichenfolge Unicode, ebenso wie der Ausgabetext.

> [!Caution]  
> Eine schlechte Pufferbehandlung ist in vielen Sicherheitsproblemen mit Pufferüberläufen zu sehen. Weitere Informationen [finden Sie unter Strsafe.h Reference (Strsafe.h-Referenz).](../menurc/strsafe-ovw.md) Die in Strsafe.h definierten Funktionen bieten zusätzliche Verarbeitung für die richtige Pufferbehandlung in Ihrem Code. Aus diesem Grund sollen sie ihre integrierten C/C++-Entsprechungen sowie bestimmte Microsoft Windows ersetzen. Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unicode in der Windows-API](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
