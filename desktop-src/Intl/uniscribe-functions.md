---
description: In diesem Abschnitt werden Funktionen für Typografie und komplexe Skriptverarbeitung beschrieben.
ms.assetid: 876e36f5-a91c-490b-87bd-b7cb4993f8c4
title: Uniscribe-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 547bdd2179e734120fe07c2ae774c8a066d9fd5d9db2be1262e67b505cbb04ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582190"
---
# <a name="uniscribe-functions"></a>Uniscribe-Funktionen

In diesem Abschnitt werden Funktionen für Typografie und komplexe Skriptverarbeitung beschrieben.



| Funktion                                                               | Beschreibung                                                                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ScriptApplyDigitSubs untertitel**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution)   | Wendet die angegebenen Ziffernersetzungseinstellungen auf die angegebenen Skriptsteuersteuer- und Skriptzustandsstrukturen an.                                                                    |
| [**ScriptApplyLogicalWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth)             | Verwendet ein Array von Vorbreiten für eine Ausführung und generiert ein Array angepasster, vordr.glyphenbreiten.                                                                               |
| [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)                                     | Ruft Informationen zum Bestimmen von Zeilenumbrüchen ab.                                                                                                                                |
| [**ScriptCacheGetHeight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight)                   | Ruft die Höhe der aktuell zwischengespeicherten Schriftart ab.                                                                                                                                |
| [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox)                                     | Generiert den x-Offset vom linken Ende oder führenden Rand einer Ausführung bis zum führenden oder nachdenkenden Rand eines logischen Zeichenclusters.                                          |
| [**ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache)                             | Gibt einen Skriptcache frei.                                                                                                                                                             |
| [**ScriptGetCMap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap)                                 | Ruft die Symbolindizes der Unicode-Zeichen in einer Zeichenfolge gemäß der TrueType-CMAP-Tabelle oder der standardmäßigen cmap-Tabelle ab, die für Schriftarten im alten Stil implementiert ist.         |
| [**ScriptGetFontAlternateGlyphs**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)   | Ruft eine Liste alternativer Glyphen für ein angegebenes Zeichen ab, auf das über ein angegebenes OpenType-Feature zugegriffen werden kann.                                                         |
| [**ScriptGetFontFeatureTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)           | Ruft eine Liste typografischer Features für das definierte Schreibsystem für die OpenType-Verarbeitung ab.                                                                                  |
| [**ScriptGetFontLanguageTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)         | Ruft eine Liste von Sprachtags ab, die für das angegebene Element verfügbar sind und von einem angegebenen Skripttag für die OpenType-Verarbeitung unterstützt werden.                                  |
| [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)             | Ruft Informationen aus dem Schriftartcache zu den speziellen Glyphen ab, die von einer Schriftart verwendet werden.                                                                                                   |
| [**ScriptGetFontScriptTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)             | Ruft eine Liste der Skripts ab, die in der Schriftart für die OpenType-Verarbeitung verfügbar sind.                                                                                                        |
| [**ScriptGetGlyphABCWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth)               | Ruft die ABC-Breite eines angegebenen Glyphens ab.                                                                                                                                         |
| [**ScriptGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths)               | Konvertiert die glyphenverbreiteten Vorbreiten für eine bestimmte Schriftart in logische Breiten.                                                                                                        |
| [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties)                     | Ruft Informationen zu den aktuellen Skripts ab.                                                                                                                                  |
| [**ScriptIsComplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex)                             | Bestimmt, ob eine Unicode-Zeichenfolge eine komplexe Skriptverarbeitung erfordert.                                                                                                           |
| [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)                                 | Unterbricht eine Unicode-Zeichenfolge in einzeln formbare Elemente.                                                                                                                        |
| [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)                 | Unterbricht eine Unicode-Zeichenfolge in einzeln formbare Elemente und stellt ein Array von Featuretags für jedes formbare Element für die OpenType-Verarbeitung zur Verfügung.                                  |
| [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify)                                 | Erstellt eine Tabelle mit der breiteten Breite, um eine Textbeendung zu ermöglichen, wenn sie an die [**ScriptTextOut-Funktion übergeben**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) wird.                                                   |
| [**ScriptLayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout)                                   | Konvertiert ein Array von Ausführungs-Einbettungsebenen in eine Zuordnung von visueller zu logischer Position und/oder logischer zu visueller Position.                                                               |
| [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)                                     | Generiert Informationen zur glyphenverbreiteten Breite und zum zweidimensionalen Offset aus der Ausgabe von [**ScriptShape.**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)                                                       |
| [**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)                     | Generiert Glyphen und visuelle Attribute für eine Unicode-Ausführung mit OpenType-Informationen aus der Ausgabe von [**ScriptShapeOpenType.**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)                         |
| [**ScriptPositionSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)         | Positioniert ein einzelnes Glyphen mit einer einzelnen Anpassung unter Verwendung eines angegebenen Features, das in der Schriftart für die OpenType-Verarbeitung bereitgestellt wird.                                                         |
| [**ScriptRecordDigitSubsregistrieren**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) | Liest die nativen Ziffern- und Ziffernersetzungseinstellungen der National Language Support (NLS) und zeichnet sie in einer [**SCRIPT \_ DIGITSUBSTITUTE-Struktur**](/windows/win32/api/usp10/ns-usp10-script_digitsubstitute) auf. |
| [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)                                     | Generiert Glyphen und visuelle Attribute für eine Unicode-Ausführung.                                                                                                                         |
| [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)                     | Generiert Glyphen und visuelle Attribute für eine Unicode-Ausführung mit OpenType-Informationen.                                                                                               |
| [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)                     | Analysiert eine Nur-Text-Zeichenfolge.                                                                                                                                                     |
| [**ScriptStringCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox)                         | Ruft die x-Koordinate für den führenden oder nachdenkenden Rand einer Zeichenposition ab.                                                                                              |
| [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree)                           | Gibt eine [**SCRIPT \_ STRING \_ ANALYSIS-Struktur**](script-string-analysis.md) frei.                                                                                                     |
| [**ScriptStringGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths)   | Konvertiert visuelle Breiten in logische Breiten.                                                                                                                                       |
| [**ScriptStringGetOrder**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder)                   | Erstellt ein Array, das eine ursprüngliche Zeichenposition einer Glyphenposition zu ordnet.                                                                                                    |
| [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)                             | Zeigt eine Zeichenfolge an, die durch einen vorherigen Aufruf von [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) generiert wurde, und fügt optional Hervorhebungen hinzu.                                               |
| [**ScriptString \_ pcOutChars**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars)            | Gibt nach dem Clipping einen Zeiger auf die Länge einer Zeichenfolge zurück.                                                                                                                       |
| [**ScriptString \_ pLogAttr**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr)                | Gibt einen Zeiger auf einen logischen Attributpuffer für eine analysierte Zeichenfolge zurück.                                                                                                          |
| [**ScriptString \_ pSize**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize)                      | Gibt einen Zeiger auf eine [**SIZE-Struktur**](/previous-versions//dd145106(v=vs.85)) für eine analysierte Zeichenfolge zurück.                                                                                                     |
| [**ScriptStringValidate**](/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate)                   | Überprüft eine [**SCRIPT \_ STRING \_ ANALYSIS-Struktur**](script-string-analysis.md) auf ungültige Sequenzen.                                                                              |
| [**ScriptStringXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp)                         | Konvertiert eine x-Koordinate in eine Zeichenposition.                                                                                                                                 |
| [**ScriptSubstituteSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)     | Ermöglicht die Ersetzung eines einzelnen Glyphen durch eine alternative Form desselben Glyphen für die OpenType-Verarbeitung.                                                                         |
| [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout)                                 | Zeigt Text für die angegebene Skriptform und die angegebenen Ortsinformationen an.                                                                                                               |
| [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)                                     | Generiert den führenden oder nachlaufenden Rand eines logischen Zeichenclusters aus dem x-Offset einer Ausführung.                                                                                 |



 

 

 
