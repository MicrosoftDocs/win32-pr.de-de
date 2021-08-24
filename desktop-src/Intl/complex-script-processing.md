---
description: 'Im Folgenden finden Sie Optionen für die Anzeige und die zugehörige Verarbeitung von Text zur Unterstützung von feinen Typografieeffekten oder komplexen Skripts: TextfunktionenSteuerelemente Bearbeiten Von Steuerelementen bearbeitenUniscribe'
ms.assetid: 337bc798-e75d-4389-8fea-577eb82a0ed5
title: Komplexe Skriptverarbeitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15671aed99e0c596d83bd65a2f4a0925ff61293cf90ed37e2aed371f23f114fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754910"
---
# <a name="complex-script-processing"></a>Komplexe Skriptverarbeitung

Im Folgenden finden Sie Optionen für die Anzeige und die zugehörige Verarbeitung von Text zur Unterstützung von Feintypografieeffekten oder komplexen Skripts:

-   Textfunktionen
-   Bearbeiten von Steuerelementen
-   Rich Edit-Steuerelemente
-   Uniscribe

Welche Optionen Sie auswählen, hängt von den folgenden Faktoren ab:

-   Der Typ von Text oder Skripts.
-   Das Implementierungsmodell, z. B. das Textlayout und die Behandlung von Zeilenumbrüchen durch die Anwendung.
-   Aktualisierung einer vorhandenen Anwendung im Vergleich zur Erstellung einer neuen Anwendung.

Im Allgemeinen kann eine Anwendung, die eine relativ einfache Skriptverarbeitung vorzieht, eine beliebige Option für die Verarbeitung komplexer Skripts auswählen. Für die umfassendste Kontrolle der komplexen Skriptverarbeitung wird jedoch Uniscribe empfohlen.

## <a name="complex-script-processing-using-text-functions"></a>Komplexe Skriptverarbeitung mitHilfe von Textfunktionen

Anwendungen, die größtenteils Nur-Text verwenden, d. h. Text, der die gleiche Schriftart, Gewichtung, Farbe usw. verwendet, haben traditionell Text und gemessene Zeilenlängen mit Standardtextfunktionen wie [**TextOut,**](/windows/win32/api/wingdi/nf-wingdi-textouta) [**ExtTextOut,**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) [**TabbedTextOut,**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta) [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)und [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa)geschrieben. Diese Funktionen unterstützen die Verarbeitung komplexer Skripts und feiner Typografieeffekte. Weitere Informationen finden Sie unter [Schriftarten und Text.](../gdi/fonts-and-text.md)

Im Allgemeinen ist die Standardtextunterstützung für Anwendungen transparent, die komplexe Skripts verarbeiten. Sie sollten jedoch einige spezifische Regeln kennen, die beim Schreiben von Anwendungen befolgt werden müssen, die eine präzise Typografie unterstützen und komplexe Skripts verarbeiten:

-   Ihre Anwendung sollte Zeichen in einem Puffer speichern und eine ganze Textzeile gleichzeitig anzeigen, anstatt z. B. [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) für jedes Zeichen aufzurufen, während es vom Benutzer eingegeben wird. Dieser Mechanismus ermöglicht es den erweiterten Textstrukturierungsmodulen, Kontext zu verwenden, um [Glyphen](uniscribe-glossary.md) ordnungsgemäß neu anzuordnen und zu generieren.
-   Die Anwendung sollte [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) verwenden, um die Zeilenlänge zu bestimmen, anstatt Zeilenlängen aus zwischengespeicherten Zeichenbreiten zu berechnen, da die Breite eines Glyphens je nach Kontext variieren kann.
-   Die Anwendung sollte optional Unterstützung für die Leserichtung von rechts nach links und die Ausrichtung nach rechts hinzufügen.
-   Die neu angeordnete und kontextbezogene Verarbeitung, die für komplexe Skripts oder die Feintypografie erforderlich ist, erfordert einen erheblichen Anstieg der Verarbeitung gegenüber der einfachen Textanzeige für einfache Skripts. Um Leistungsprobleme zu vermeiden, sollte Ihre Anwendung daher keine großen Mengen an Text verarbeiten, bevor Ergebnisse angezeigt und dem Benutzer die Steuerung zurückgegeben wird.

## <a name="complex-script-processing-using-edit-controls"></a>Komplexe Skriptverarbeitung mit Bearbeitungssteuerelementen

Die Standard-Windows-Bearbeitungssteuerelemente wurden erweitert, um mehrsprachigen Text und komplexe Skripts zu unterstützen. Die erweiterte Unterstützung umfasst Eingabe und Anzeige sowie eine korrekte Cursorbewegung über Zeichencluster, z. B. in Thai- und Devanagari-Skripts. Weitere Informationen finden Sie unter [Bearbeiten von Steuerelementen.](../controls/edit-controls.md)

## <a name="complex-script-processing-using-rich-edit-controls"></a>Komplexe Skriptverarbeitung mit Rich Edit-Steuerelementen

Rich Edit 3.0 ist eine allgemeine Sammlung von Schnittstellen, die Uniscribe nutzt, um Textlayoutanwendungen vor der Komplexität bestimmter Skripts zu schützen. Rich Edit ist die einfachste Möglichkeit für Anwendungen, komplexe Skripts anzuzeigen, obwohl ihr Hauptzweck nicht unbedingt das Textlayout ist. Rich Edit ermöglicht die schnelle, vielseitigen Bearbeitung von umfangreichem mehrsprachigem Unicode-Text und einfachem Nur-Text. Es umfasst umfangreiche Nachrichten- und COM-Schnittstellen, Textbearbeitung, Formatierung, Zeilen breaking, einfaches Tabellenlayout, vertikales Textlayout, bidirektionales Textlayout, Unterstützung für indic und Thai, eine Bearbeitungs-Benutzeroberfläche, die Microsoft Word ähnelt, und Textobjektmodell-Schnittstellen.

Zusammen mit den Rich Edit-Schnittstellen können Anwendungen die Rich Edit [**TextOut-Funktion**](/windows/win32/api/wingdi/nf-wingdi-textouta) verwenden, um Zeilen automatisch zu analysieren, zu formen, zu positionieren und zu unterbrechen. Weitere Informationen finden Sie unter [Rich Edit Controls](../controls/rich-edit-controls.md).

## <a name="complex-script-processing-using-uniscribe"></a>Komplexe Skriptverarbeitung mit Uniscribe

[Uniscribe](uniscribe.md) bietet die umfassendste Unterstützung für die Verarbeitung von Text mit feinen Typografieeffekten und komplexen Skripts. Sie unterstützt die komplexen Regeln in Skripts wie Arabisch, Devanagari und Thailändisch. Er verarbeitet Skripts, die von rechts nach links geschrieben werden, z. B. Arabisch und Hebräisch, und unterstützt die Kombination von Skripts. Uniscribe macht auch [OpenType-Schriftartfeatures](opentype-font-format.md) verfügbar, die von Anwendungen zur Steuerung von Feintypografieeffekten verwendet werden können. Weitere Informationen finden Sie unter [Verarbeiten komplexer Skripts.](processing-complex-scripts.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Uniscribe](about-uniscribe.md)
</dt> <dt>

[Verarbeiten komplexer Skripts](processing-complex-scripts.md)
</dt> </dl>

 

 
