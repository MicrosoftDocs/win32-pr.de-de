---
description: Die folgenden Funktionen werden mit Zeichensätzen verwendet.
ms.assetid: 1799f5da-1391-4b6e-ac13-718017a77557
title: Unicode-und Zeichensatz Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6996139d8a9bb426c21a460ac2bcb1358e6c8e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050323"
---
# <a name="unicode-and-character-set-functions"></a>Unicode-und Zeichensatz Funktionen

Die folgenden Funktionen werden mit Zeichensätzen verwendet.



| Funktion                                                       | BESCHREIBUNG                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**Gettextcharset**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharset)                       | Ruft einen Zeichensatz Bezeichner für die Schriftart ab, die derzeit in einem angegebenen Gerätekontext ausgewählt ist.         |
| [**Gettextcharctinfo**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharsetinfo)               | Ruft Informationen über den Zeichensatz der Schriftart ab, die derzeit in einem angegebenen Gerätekontext ausgewählt ist. |
| [**Isdbcsleadbyte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte)                       | Bestimmt, ob ein angegebenes Zeichen ein führendes Byte für die standardmäßige Windows-ANSI-Codepage (CP \_ ACP) ist.           |
| [**Isdbcsleadbyteex**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyteex)                   | Bestimmt, ob ein angegebenes Zeichen potenziell ein führendes Byte ist.                                                       |
| [**IsTextUnicode**](/windows/desktop/api/Winbase/nf-winbase-istextunicode)                         | Bestimmt, ob ein Puffer wahrscheinlich eine Form von Unicode-Text enthält.                                                   |
| [**MultiByteToWideChar muss**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)             | Ordnet eine Zeichenfolge einer UTF-16-Zeichenfolge (breit Zeichen) zu.                                                          |
| [**Translatecharltinfo**](/windows/desktop/api/Wingdi/nf-wingdi-translatecharsetinfo)           | Übersetzt Zeichensatz Informationen und legt alle Elemente einer Zielstruktur auf entsprechende Werte fest.           |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)             | Ordnet eine UTF-16-Zeichenfolge (breit Zeichen) einer neuen Zeichenfolge zu.                                                      |
| [**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))                       | Darf nicht verwendet werden.                                                                                                           |
| [**Nlsdllcodepagetranslation**](/windows/desktop/api/Gb18030/nf-gb18030-nlsdllcodepagetranslation) | Darf nicht verwendet werden.                                                                                                           |
| [**Unicodebybytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))                       | Nicht verwenden.                                                                                                           |



 

 

 
