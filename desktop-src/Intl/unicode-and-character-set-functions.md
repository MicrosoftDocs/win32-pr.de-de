---
description: Die folgenden Funktionen werden mit Zeichensätzen verwendet.
ms.assetid: 1799f5da-1391-4b6e-ac13-718017a77557
title: Unicode- und Zeichensatzfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd26edd8931b1a63887816ca07698d779bd0d4d3decceb3b53faf5d499605612
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811711"
---
# <a name="unicode-and-character-set-functions"></a>Unicode- und Zeichensatzfunktionen

Die folgenden Funktionen werden mit Zeichensätzen verwendet.



| Funktion                                                       | Beschreibung                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**GetTextCharset**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharset)                       | Ruft einen Zeichensatzbezeichner für die Schriftart ab, die derzeit in einem angegebenen Gerätekontext ausgewählt ist.         |
| [**GetTextCharsetInfo**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharsetinfo)               | Ruft Informationen zum Zeichensatz der Schriftart ab, die derzeit in einem angegebenen Gerätekontext ausgewählt ist. |
| [**IsDBCSLeadByte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte)                       | Bestimmt, ob ein angegebenes Zeichen ein Lead-Byte für den Systemstandard Windows ANSI-Codepage (CP \_ ACP) ist.           |
| [**IsDBCSLeadByteEx**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyteex)                   | Bestimmt, ob ein angegebenes Zeichen potenziell ein lead-Byte ist.                                                       |
| [**IsTextUnicode**](/windows/desktop/api/Winbase/nf-winbase-istextunicode)                         | Bestimmt, ob ein Puffer wahrscheinlich eine Form von Unicode-Text enthält.                                                   |
| [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)             | Karten eine Zeichenfolge in eine UTF-16-Zeichenfolge (Breitzeichen).                                                          |
| [**TranslateCharsetInfo**](/windows/desktop/api/Wingdi/nf-wingdi-translatecharsetinfo)           | Übersetzt Zeichensatzinformationen und legt alle Member einer Zielstruktur auf entsprechende Werte fest.           |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)             | Karten eine UTF-16-Zeichenfolge (Breitzeichen) in eine neue Zeichenfolge.                                                      |
| [**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))                       | Darf nicht verwendet werden.                                                                                                           |
| [**NlsDllCodePageTranslation**](/windows/desktop/api/Gb18030/nf-gb18030-nlsdllcodepagetranslation) | Darf nicht verwendet werden.                                                                                                           |
| [**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))                       | Nicht verwenden.                                                                                                           |



 

 

 
