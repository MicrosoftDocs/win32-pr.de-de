---
description: In diesem Abschnitt werden die Funktionen für die Typografie und die komplexe Skript Verarbeitung beschrieben.
ms.assetid: 876e36f5-a91c-490b-87bd-b7cb4993f8c4
title: Uniscriefunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f623c8da04f985f88d091f8e9e2b4cb724c0801
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354853"
---
# <a name="uniscribe-functions"></a>Uniscriefunktionen

In diesem Abschnitt werden die Funktionen für die Typografie und die komplexe Skript Verarbeitung beschrieben.



| Funktion                                                               | BESCHREIBUNG                                                                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Scriptapplydigitsubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution)   | Wendet die angegebenen Ziffern Ersetzungs Einstellungen auf das angegebene Skript Steuerelement und die Skript Zustands Strukturen an.                                                                    |
| [**Scriptapplylogicalwidth**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth)             | Nimmt ein Array von Vorlauf breiten für einen Testlauf an und generiert ein Array der angepassten vorwärts Symbol Breite.                                                                               |
| [**Scriptbreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)                                     | Ruft Informationen zum Bestimmen von Zeilenumbrüchen ab.                                                                                                                                |
| [**Scriptcachegetheight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight)                   | Ruft die Höhe der aktuell zwischengespeicherten Schriftart ab.                                                                                                                                |
| [**Scriptcptox**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox)                                     | Generiert den x-Offset vom linken oder führenden Rand einer Run-Instanz bis zum führenden oder nachfolgenden Rand eines logischen Zeichen Clusters.                                          |
| [**Scriptfreecache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache)                             | Gibt einen Skript Cache frei.                                                                                                                                                             |
| [**Scriptgetcmap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap)                                 | Ruft die Symbol Indizes der Unicode-Zeichen in einer Zeichenfolge entsprechend der TrueType-cmap-Tabelle oder der Standard-cmap-Tabelle ab, die für Schriftarten im alten Stil implementiert ist.         |
| [**Scriptgetfontalternateglyphs**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)   | Ruft eine Liste alternativer Symbole für ein angegebenes Zeichen ab, auf die über eine angegebene OpenType-Funktion zugegriffen werden kann.                                                         |
| [**Scriptgetfontfeaturetags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)           | Ruft eine Liste von typografischen Features für das definierte Schreibsystem für die OpenType-Verarbeitung ab.                                                                                  |
| [**Scriptgetfontlanguagetags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)         | Ruft eine Liste von sprach Tags ab, die für das angegebene Element verfügbar sind und von einem angegebenen Skripttag für die OpenType-Verarbeitung unterstützt werden.                                  |
| [**Scriptgetfontproperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)             | Ruft Informationen aus dem Schriftart Cache auf den speziellen Symbolen ab, die von einer Schriftart verwendet werden.                                                                                                   |
| [**Scriptgetfontscripttags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)             | Ruft eine Liste der in der Schriftart verfügbaren Skripts für die OpenType-Verarbeitung ab.                                                                                                        |
| [**Scriptgetglyphabcwidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth)               | Ruft die ABC-Breite eines angegebenen Symbols ab.                                                                                                                                         |
| [**Scriptgetlogicalbreiten**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths)               | Konvertiert die Symbol vorbreite für eine bestimmte Schriftart in logische breiten.                                                                                                        |
| [**Scriptgetproperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties)                     | Ruft Informationen zu den aktuellen Skripts ab.                                                                                                                                  |
| [**Scriptiscomplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex)                             | Bestimmt, ob eine Unicode-Zeichenfolge eine komplexe Skript Verarbeitung erfordert.                                                                                                           |
| [**Scriptitemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)                                 | Unterteilt eine Unicode-Zeichenfolge in einzeln Shape-Elemente.                                                                                                                        |
| [**Scriptitemizeopentype**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)                 | Unterteilt eine Unicode-Zeichenfolge in individuell Shape Bare Elemente und stellt ein Array von featuretags für jedes Element dar, das für die OpenType-Verarbeitung bereit ist.                                  |
| [**Scriptrecht**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify)                                 | Erstellt eine Tabelle mit Vorlauf breiten, um die Textausrichtung bei der Übergabe an die [**scripttextout**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) -Funktion zuzulassen.                                                   |
| [**Scriptlayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout)                                   | Konvertiert ein Array von Einbettungs Ebenen für das Ausführen in eine Zuordnung von der Visualisierung zu einer logischen Position und/oder der logischen zu visuellen Position.                                                               |
| [**Scriptplace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)                                     | Generiert die Symbole für die vorwärts Breite und die zweidimensionalen Offset Informationen aus der Ausgabe von [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape).                                                       |
| [**Scriptplaceopentype**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)                     | Generiert Symbole und visuelle Attribute für ein Unicode-Lauf mit OpenType-Informationen aus der Ausgabe von [**scriptshapeopentype**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype).                         |
| [**Scriptpositionsingleglyph**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)         | Positioniert ein einzelnes Symbol mit einer einzelnen Anpassung mithilfe einer angegebenen Funktion, die in der Schriftart für die OpenType-Verarbeitung bereitgestellt wird.                                                         |
| [**Scriptrecorddigitsubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) | Liest die NLS (National Language Support)-Einstellungen für Native Ziffern und Ziffern Ersetzung und zeichnet diese in einer [**Skript- \_ digitersatzstruktur**](/windows/win32/api/usp10/ns-usp10-script_digitsubstitute) auf. |
| [**Scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)                                     | Generiert Symbole und visuelle Attribute für eine Unicode-Laufzeit.                                                                                                                         |
| [**Scriptshapeopentype**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)                     | Generiert Symbole und visuelle Attribute für ein Unicode-Lauf mit OpenType-Informationen.                                                                                               |
| [**Scriptstringanalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)                     | Analysiert eine einfache Text Zeichenfolge.                                                                                                                                                     |
| [**Scriptstringcptox**](/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox)                         | Ruft die x-Koordinate für den führenden oder nachfolgenden Rand einer Zeichenposition ab.                                                                                              |
| [**Scriptstringfree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree)                           | Gibt eine [**Skript \_ Zeichenfolgen- \_ Analyse**](script-string-analysis.md) Struktur frei.                                                                                                     |
| [**Scriptstringgetlogicalbreiten**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths)   | Konvertiert visuelle breiten in logische breiten.                                                                                                                                       |
| [**Scriptstringgetor**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder)                   | Erstellt ein Array, das eine ursprüngliche Zeichenposition einer Symbol Position zuordnet.                                                                                                    |
| [**Scriptstringout**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)                             | Zeigt eine Zeichenfolge an, die von einem vorherigen [**calltstringanalyse-Skript**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) generiert wurde, und fügt optional Hervorhebung hinzu.                                               |
| [**Scriptstring \_ pcoutchars**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars)            | Gibt nach dem Clipping einen Zeiger auf die Länge einer Zeichenfolge zurück.                                                                                                                       |
| [**Scriptstring \_ plogattr**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr)                | Gibt einen Zeiger auf einen Puffer für logische Attribute für eine analysierte Zeichenfolge zurück.                                                                                                          |
| [**Scriptstring \_ Psize**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize)                      | Gibt einen Zeiger auf eine [**Größen**](/previous-versions//dd145106(v=vs.85)) Struktur für eine analysierte Zeichenfolge zurück.                                                                                                     |
| [**Scriptstringvalidate**](/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate)                   | Überprüft eine [**Skript \_ Zeichenfolgen- \_ Analyse**](script-string-analysis.md) Struktur auf ungültige Sequenzen.                                                                              |
| [**Scriptstringxtcp**](/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp)                         | Konvertiert eine x-Koordinate in eine Zeichenposition.                                                                                                                                 |
| [**Scriptsubstitutesingleglyph**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)     | Ermöglicht die Ersetzung eines einzelnen Symbols durch eine alternative Form desselben Symbols für die OpenType-Verarbeitung.                                                                         |
| [**Scripttextout**](/windows/desktop/api/Usp10/nf-usp10-scripttextout)                                 | Zeigt Text für die angegebene Skript Form und die angegebenen Ortsinformationen an.                                                                                                               |
| [**Scriptxtcp**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)                                     | Generiert den führenden oder nachfolgenden Rand eines logischen Zeichen Clusters aus dem x-Offset einer Testlauf.                                                                                 |



 

 

 
