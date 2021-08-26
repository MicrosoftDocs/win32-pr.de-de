---
description: Surrogate und ergänzende Zeichen
ms.assetid: 0dea39e2-a2b4-47fc-b44a-56af8ba1e346
title: Surrogate und ergänzende Zeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b1dc4743627297962c7279449c06cc1ff967ac35f931a6e945b4577c937b59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130050"
---
# <a name="surrogates-and-supplementary-characters"></a>Surrogate und ergänzende Zeichen

Windows Anwendungen verwenden normalerweise UTF-16, um [Unicode-Zeichendaten](unicode.md) zu darstellen. Die Verwendung von 16 Bits ermöglicht die direkte Darstellung von 65.536 eindeutigen Zeichen, aber diese grundlegende mehrsprachige Ebene (Basic Multilingual Plane, BMP) reicht nicht fast aus, um alle symbole zu abdecken, die in menschlichen Sprachen verwendet werden. Unicode-Version 4.1 umfasst mehr als 97.000 Zeichen, mit mehr als 70.000 Zeichen allein für Chinesisch.

Der Unicode-Standard hat 16 zusätzliche "Ebenen" von Zeichen eingerichtet, die jeweils die gleiche Größe wie der BMP haben. Natürlich sind den meisten Codepunkten außerhalb des BMP noch keine Zeichen zugewiesen, aber die Definition der Ebenen gibt Unicode das Potenzial, 1.114.112 Zeichen (d. h. 2. ⁶ 17 Zeichen) innerhalb des Codepunktbereichs \* U+0000 bis U+10FFFF zu definieren. Damit UTF-16 diesen größeren Zeichensatz darstellen kann, definiert der Unicode-Standard "ergänzende Zeichen".

## <a name="about-supplementary-characters"></a>Informationen zu ergänzenden Zeichen

Ein ergänzendes Zeichen ist ein Zeichen, das sich außerhalb des BMP befindet, und ein "Ersatzzeichen" ist ein UTF-16-Codewert. Für UTF-16 ist ein Ersatzzeichenpaar erforderlich, um ein einzelnes ergänzendes Zeichen darstellen zu können. Das erste (hohe) Ersatzzeichen ist ein 16-Bit-Codewert im Bereich U+D800 bis U+DBFF. Das zweite (niedrige) Ersatzzeichen ist ein 16-Bit-Codewert im Bereich U+DC00 bis U+DFFF. Mit dem Ersatzzeichenmechanismus kann UTF-16 alle 1.114.112 potenziellen Unicode-Zeichen unterstützen. Weitere Informationen zu ergänzenden Zeichen, Ersatzzeichen und Ersatzzeichenpaaren finden Sie unter [The Unicode Standard](https://www.unicode.org/standard/standard.html).

> [!Note]  
> Windows 2000 bietet Unterstützung für grundlegende Eingaben, Ausgaben und die einfache Sortierung ergänzender Zeichen. Allerdings sind nicht alle Systemkomponenten mit ergänzenden Zeichen kompatibel.

 

Das Betriebssystem unterstützt ergänzende Zeichen auf folgende Weise:

-   Format 12 der CMAP-Schriftarttabelle OpenType unterstützt direkt den 4-Byte-Zeichencode. Weitere Informationen finden Sie in der [OpenType-Schriftartspezifikation](/typography/opentype/spec/).
-   Windows unterstützt ersatzfähige [Eingabemethode-Editoren (IMEs).](../dxtecharts/installing-and-using-input-method-editors.md)
-   Die [Windows GDI-API](../gdi/windows-gdi.md) unterstützt das Format 12 cmap-Tabellen in Schriftarten, sodass Ersatzzeichen ordnungsgemäß angezeigt werden können.
-   Die [Uniscribe-API](uniscribe.md) unterstützt ergänzende Zeichen.
-   [Windows-Steuerelemente](../controls/window-controls.md), einschließlich [Bearbeiten](../controls/edit-controls.md) und [Rich Edit,](../controls/rich-edit-controls.md)unterstützen ergänzende Zeichen.
-   Die HTML-Engine unterstützt HTML-Seiten, die ergänzende Zeichen für die Anzeige, Bearbeitung (über Outlook Express) und Formularübermittlung enthalten.
-   Die Sortiertabelle des Betriebssystems unterstützt ergänzende Zeichen.

## <a name="general-guidelines-for-software-development-using-supplementary-characters"></a>Allgemeine Richtlinien für die Softwareentwicklung mit ergänzenden Zeichen

UTF-16 verarbeitet ergänzende Zeichen als Ersatzzeichenpaare. Das Betriebssystem verarbeitet ein Ersatzzeichenpaar ähnlich der Art und Weise, wie es [Nicht-Paczeichen verarbeitet.](using-nonspacing-characters-and-diacritics.md) Zur Anzeigezeit wird das Ersatzzeichenpaar als ein Symbol mit uniscribe angezeigt, wie im Unicode-Standard vorgegeben.

Windows Vista führt drei neue Makros ein, um Ersatzzeichen und Ersatzzeichenpaare in UTF-16-Zeichenfolgen zu identifizieren. Dies [**sind IS HIGH \_ \_ SURROGATE,**](/windows/win32/api/Winnls/nf-winnls-is_high_surrogate) [**IS LOW \_ \_ SURROGATE**](/windows/win32/api/Winnls/nf-winnls-is_low_surrogate)und [**IS \_ SURROGATE \_ PAIR**](/windows/win32/api/Winnls/nf-winnls-is_surrogate_pair).

Anwendungen unterstützen automatisch ergänzende Zeichen, wenn sie Unicode unterstützen und Systemsteuerelemente und STANDARD-API-Funktionen wie [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) und [**DrawText verwenden.**](/windows/win32/api/winuser/nf-winuser-drawtext) Wenn Ihre Anwendung standardmäßige Systemsteuerelemente verwendet oder allgemeine [**ExtTextOut-Typaufrufe**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)zum Anzeigen verwendet, sollten ergänzende Zeichen ohne spezielle Codierung funktionieren.

Anwendungen, die ihre eigene Bearbeitungsunterstützung implementieren, indem sie Glyphenpositionen auf benutzerdefinierte Weise ausarbeiten, können Uniscribe für die text-Verarbeitung verwenden. Uniscribe verfügt über separate Funktionen für die Verarbeitung komplexer Skripts, z. B. Textanzeige, Treffertests und Cursorbewegung. Eine Anwendung muss die Uniscribe-Funktionen speziell aufrufen, um diese erweiterten Features zu erhalten. Beachten Sie, dass Anwendungen, die die Uniscribe-Funktionen verwenden, vollständig mehrsprachige Funktionen sind, dies jedoch zu Leistungssentspricht. Daher sollten einige Anwendungen ihre eigene Verarbeitung ergänzender Zeichen tun.

Da der Ersatzmechanismus zur Darstellung ergänzender Zeichen klar definiert ist, kann Ihre Anwendung Code für die Verarbeitung von UTF-16-Ersatztext enthalten. Wenn die Anwendung auf einen getrennten UTF-16-Wert vom unteren reservierten Ersatzzeichenbereich (ein niedriges Ersatzzeichen) oder dem oberen reservierten Ersatzzeichenbereich (ein hohes Ersatzzeichen) trifft, muss der Wert die Hälfte eines Ersatzzeichenpaars sein. Daher kann die Anwendung ein Ersatzzeichenpaar durch einfache Bereichsüberprüfung erkennen. Wenn ein UTF-16-Wert im unteren oder oberen Bereich gefunden wird, muss er eine 16-Bit-Breite rückwärts oder vorwärts nachverfolgen, um den Rest des Zeichens zu erhalten. Beachten Sie beim Schreiben Ihrer Anwendung, dass [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta) und [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva) um 16-Bit-Codepunkte und nicht durch Ersatzzeichenpaare bewegt werden.

> [!Note]  
> Eigenständige Ersatzcodepunkte verfügen entweder über ein hohes Ersatzzeichen ohne angrenzendes niedriges Ersatzzeichen oder umgekehrt. Diese Codepunkte sind ungültig und werden nicht unterstützt. Ihr Verhalten ist nicht definiert.

 

Wenn Sie eine Schriftart oder einen IME-Anbieter entwickeln, beachten Sie, dass vor Windows XP-Betriebssystemen die Unterstützung ergänzender Zeichen standardmäßig deaktiviert ist. Windows XP und höher aktivieren standardmäßig ergänzende Zeichen. Wenn Sie eine Schriftart und ein IME-Paket bereitstellen, die ergänzende Zeichen erfordern, muss Ihre Anwendung die folgenden Registrierungswerte festlegen:


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

 

 
