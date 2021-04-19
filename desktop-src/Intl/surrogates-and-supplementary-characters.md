---
description: Surrogate und ergänzende Zeichen
ms.assetid: 0dea39e2-a2b4-47fc-b44a-56af8ba1e346
title: Surrogate und ergänzende Zeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8d6b738955c8b8de4f6cb0ae43c78f86752a928
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346299"
---
# <a name="surrogates-and-supplementary-characters"></a>Surrogate und ergänzende Zeichen

Windows-Anwendungen verwenden in der Regel UTF-16, um [Unicode](unicode.md) -Zeichendaten darzustellen. Die Verwendung von 16 Bits ermöglicht die direkte Darstellung von 65.536 eindeutigen Zeichen, aber diese grundlegende mehrsprachige Ebene (BMP) ist nicht fast genug, um alle Symbole abzudecken, die in der menschlichen Sprache verwendet werden. Unicode-Version 4,1 umfasst mehr als 97.000 Zeichen, mit mehr als 70.000 Zeichen für Chinesisch.

Der Unicode-Standard hat 16 zusätzliche "Ebenen" von Zeichen eingerichtet, die jeweils dieselbe Größe wie der BMP aufweisen. Natürlich sind den meisten Code Punkten, die über den BMP hinausgehen, noch keine Zeichen zugewiesen, aber die Definition der Ebenen gibt Unicode das Potenzial, 1.114.112 Zeichen (d. h. 2 ¹ ⁶ \* 17 Zeichen) im Code punktbereich von u + 0000 bis u + 10FFFF zu definieren. Damit UTF-16 diesen größeren Satz von Zeichen darstellt, definiert der Unicode-Standard "ergänzende Zeichen".

## <a name="about-supplementary-characters"></a>Informationen zu ergänzenden Zeichen

Ein zusätzliches Zeichen ist ein Zeichen, das sich hinter dem BMP befindet, und ein "Ersatz Zeichen" ist ein UTF-16-Codewert. Für UTF-16 ist ein "Ersatzpaar" erforderlich, um ein einzelnes zusätzliches Zeichen darzustellen. Das erste (hohe) Ersatz Zeichen ist ein 16-Bit-Codewert im Bereich von u + D800 und bis U + DBFF. Das zweite (niedrige) Ersatz Zeichen ist ein 16-Bit-Codewert im Bereich von u + DC00 und bis U + DFFF. Mit dem Ersatz Zeichen Mechanismus kann UTF-16 alle 1.114.112 potenziellen Unicode-Zeichen unterstützen. Weitere Informationen zu ergänzenden Zeichen, Surrogates und Ersatz Zeichen Paaren finden Sie [im Unicode-Standard](https://www.unicode.org/standard/standard.html).

> [!Note]  
> Windows 2000 bietet Unterstützung für die grundlegende Eingabe, Ausgabe und einfache Sortierung von ergänzenden Zeichen. Allerdings sind nicht alle Systemkomponenten mit ergänzenden Zeichen kompatibel.

 

Das Betriebssystem unterstützt ergänzende Zeichen auf folgende Weise:

-   Das Format 12 der CMAP-Tabelle der OpenType-Schriftart unterstützt direkt den 4-Byte-Zeichencode. Weitere Informationen finden Sie in der [OpenType-Schriftart Spezifikation](/typography/opentype/spec/).
-   Windows unterstützt Ersatz aktivierte [Eingabemethoden-Editoren (Input Method Editors, IMEs)](../dxtecharts/installing-and-using-input-method-editors.md)
-   Die [Windows-GDI](../gdi/windows-gdi.md) -API unterstützt cmap-Tabellen im Format 12 in Schriftarten, damit Ersatz Zeichen ordnungsgemäß angezeigt werden können.
-   Die [uniscrieapi](uniscribe.md) unterstützt ergänzende Zeichen.
-   [Windows](../controls/window-controls.md)-Steuerelemente, einschließlich [Edit](../controls/edit-controls.md) und [Rich Edit](../controls/rich-edit-controls.md), unterstützen zusätzliche Zeichen.
-   Die HTML-Engine unterstützt HTML-Seiten, die ergänzende Zeichen zum Anzeigen, bearbeiten (über Outlook Express) und zum Einreichen von Formularen enthalten.
-   Die Sortier Tabelle des Betriebssystems unterstützt ergänzende Zeichen.

## <a name="general-guidelines-for-software-development-using-supplementary-characters"></a>Allgemeine Richtlinien für die Software Entwicklung mit ergänzenden Zeichen

In UTF-16 werden ergänzende Zeichen als Ersatz Zeichenpaare behandelt. Das Betriebssystem verarbeitet ein Ersatz Zeichenpaar entsprechend der Art und Weise, in der es keine [abstandsmarkierungen](using-nonspacing-characters-and-diacritics.md)verarbeitet. Zum Zeitpunkt der Anzeige wird das Ersatz Zeichenpaar als ein Symbol mithilfe von unischreiber angezeigt, wie vom Unicode-Standard vorgeschrieben.

Windows Vista führt drei neue Makros ein, mit denen Ersatz Zeichen und Ersatz Zeichenpaare in UTF-16-Zeichen folgen identifiziert werden können. Dabei handelt es sich [**um ein \_ hohes \_ Ersatz**](/windows/win32/api/Winnls/nf-winnls-is_high_surrogate)Zeichen, ein [**\_ niedriges \_ Ersatz**](/windows/win32/api/Winnls/nf-winnls-is_low_surrogate)Zeichen und ein [**Ersatz Zeichen \_ \_ paar**](/windows/win32/api/Winnls/nf-winnls-is_surrogate_pair).

Anwendungen unterstützen automatisch ergänzende Zeichen, wenn Sie Unicode unterstützen und System Steuerelemente und API-Standardfunktionen verwenden, z. [**b. exttextout**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) und [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). Wenn Ihre Anwendung also Standardsystem Steuerelemente verwendet oder allgemeine [**exttextout**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)-Aufrufe zur Anzeige verwendet, sollten ergänzende Zeichen ohne spezielle Codierung funktionieren.

Anwendungen, die ihre eigene Bearbeitungs Unterstützung implementieren, indem Sie Symbol Positionen in einer angepassten Weise auslagern, können uniwriter für die gesamte Textverarbeitung verwenden. Uniwriter verfügt über separate Funktionen für die Verarbeitung komplexer Skript Verarbeitung, wie z. b. Textanzeige, Treffer Tests und Cursor Bewegung. Eine Anwendung muss die unischreiber-Funktionen speziell zum Abrufen dieser erweiterten Features aufruft. Beachten Sie, dass Anwendungen, die die uniscriefunktionen verwenden, vollständig mehrsprachig sind, was jedoch zu Leistungseinbußen führt. Daher sollten einige Anwendungen eine eigene Verarbeitung ergänzender Zeichen ausführen.

Da der ersatzmechanismus zur Darstellung ergänzender Zeichen klar definiert ist, kann die Anwendung Code zum Verarbeiten der UTF-16-Ersatztext Verarbeitung enthalten. Wenn die Anwendung einen getrennten UTF-16-Wert aus dem unteren reservierten Ersatz Zeichenbereich (ein niedriges Ersatz Zeichen) oder dem oberen reservierten Ersatz Zeichenbereich (ein hohes Ersatz Zeichen) trifft, muss der Wert eine Hälfte eines Ersatz Zeichen Paars sein. Daher kann die Anwendung ein Ersatz Zeichenpaar durch eine einfache Bereichs Überprüfung erkennen. Wenn ein UTF-16-Wert im unteren oder oberen Bereich angezeigt wird, muss er eine abwärts-oder vorwärts-1 16-Bit-Breite nachverfolgen, um das restliche Zeichen zu erhalten. Beachten Sie beim Schreiben der Anwendung, dass [**charnext**](/windows/win32/api/winuser/nf-winuser-charnexta) und [**charprev**](/windows/win32/api/winuser/nf-winuser-charpreva) von 16-Bit-Code Punkten, nicht von Ersatz Zeichen Paaren bewegt werden.

> [!Note]  
> Eigenständige Ersatz Zeichencode Punkte verfügen entweder über ein hohes Ersatz Zeichen ohne ein benachbartes niedriges Ersatz Zeichen oder umgekehrt. Diese Code Punkte sind ungültig und werden nicht unterstützt. Das Verhalten ist nicht definiert.

 

Wenn Sie einen Schriftart-oder IME-Anbieter entwickeln, beachten Sie, dass die Betriebssysteme vor Windows XP die Unterstützung zusätzlicher Zeichen standardmäßig deaktivieren. In Windows XP und höher werden zusätzliche Zeichen standardmäßig aktiviert. Wenn Sie ein Schriftart-und ein IME-Paket bereitstellen, das zusätzliche Zeichen erfordert, muss Ihre Anwendung die folgenden Registrierungs Werte festlegen:


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\LanguagePack]
SURROGATE=(REG_DWORD)0x00000002

[HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\International\Scripts\42]
IEFixedFontName=[Surrogate Font Face Name]
IEPropFontName=[Surrogate Font Face Name]
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zeichensätze](character-sets.md)
</dt> </dl>

 

 
