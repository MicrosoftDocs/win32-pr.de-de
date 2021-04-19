---
description: 'Im folgenden finden Sie Optionen für die Anzeige und verwandte Verarbeitung von Text, um feine typografieeffekte oder komplexe Skripts zu unterstützen: Text functionsedit controlsrich Edit controlsunischreiber'
ms.assetid: 337bc798-e75d-4389-8fea-577eb82a0ed5
title: Komplexe Skript Verarbeitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e4be6295bff949c8e29036ef3af496c673575e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373075"
---
# <a name="complex-script-processing"></a>Komplexe Skript Verarbeitung

Im folgenden finden Sie Optionen für die Anzeige und verwandte Verarbeitung von Text, um feine typografieeffekte oder komplexe Skripts zu unterstützen:

-   Textfunktionen
-   Steuerelemente bearbeiten
-   Rich Edit-Steuerelemente
-   Unischreiber

Welche Optionen Sie auswählen, hängt von den folgenden Faktoren ab:

-   Der Typ von Text oder Skripts.
-   Das Implementierungs Modell, z. b. das Text Layout und die Handhabung von Zeilenumbruch durch die Anwendung.
-   Aktualisieren einer vorhandenen Anwendung im Vergleich zur Erstellung einer neuen Anwendung.

Im Allgemeinen kann eine Anwendung, die eine relativ einfache Skript Verarbeitung durchführt, eine beliebige Option zum Verarbeiten komplexer Skripts auswählen. Allerdings wird uniscriempfohlen, um die umfassende Kontrolle über die komplexe Skript Verarbeitung zu erhalten.

## <a name="complex-script-processing-using-text-functions"></a>Komplexe Skript Verarbeitung mit Text Funktionen

Anwendungen, die größtenteils nur-Text verwenden, d. h. Text, der die gleiche Schriftart, Gewichtung, Farbe usw. verwendet, haben in der Regel Text und gemessene Zeilenlängen mithilfe von Standardtext Funktionen geschrieben, wie z. b. [**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta), [**exttextout**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**tabbedtextout**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)und [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa). Diese Funktionen unterstützen die Verarbeitung komplexer Skripts und der fein typografieeffekte. Weitere Informationen finden Sie unter [Schriftarten und Text](../gdi/fonts-and-text.md).

Im Allgemeinen ist die standardmäßige Textunterstützung für Anwendungen transparent, die komplexe Skripts verarbeiten. Sie sollten jedoch bestimmte Regeln beachten, die beim Schreiben von Anwendungen beachtet werden müssen, die feine typografieskripts unterstützen und komplexe Skripts verarbeiten:

-   Die Anwendung sollte Zeichen in einem Puffer speichern und eine ganze Textzeile gleichzeitig anzeigen, anstatt beispielsweise [**exttextout**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) für jedes Zeichen aufzurufen, das vom Benutzer eingegeben wird. Dieser Mechanismus ermöglicht es den erweiterten Text Strukturierungs Modulen, den Kontext zum ordnungsgemäßen anordnen [und Generieren von](uniscribe-glossary.md) Symbolen zu verwenden.
-   Die Anwendung sollte [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) verwenden, um die Zeilenlänge zu bestimmen, anstatt die Zeilenlängen von zwischengespeicherten Zeichen breiten zu berechnen, da die Breite eines Symbols je nach Kontext variieren kann.
-   Die Anwendung sollte optional Unterstützung für die Lesefolge von rechts nach links und die Rechte Ausrichtung hinzufügen.
-   Die Neuanordnung und die kontextabhängige Verarbeitung, die für komplexe Skripts oder eine fein Typografie erforderlich ist, erfordern eine deutliche Steigerung der Verarbeitung über die einfache Textanzeige für einfache Skripts Um Leistungsprobleme zu vermeiden, sollte Ihre Anwendung daher keine großen Textmengen verarbeiten, bevor Ergebnisse angezeigt und die Steuerung an den Benutzer zurückgegeben wird.

## <a name="complex-script-processing-using-edit-controls"></a>Komplexe Skript Verarbeitung mit Bearbeitungs Steuerelementen

Die standardmäßigen Windows-Bearbeitungs Steuerelemente wurden erweitert, um mehrsprachigen Text und komplexe Skripts zu unterstützen. Die erweiterte Unterstützung umfasst die Eingabe und die Anzeige sowie die korrekte Cursor Bewegung über Zeichen Cluster, z. b. in den Skripts "Thai" und "Devanagari". Weitere Informationen finden Sie unter [Edit Controls](../controls/edit-controls.md).

## <a name="complex-script-processing-using-rich-edit-controls"></a>Komplexe Skript Verarbeitung mithilfe von Rich-Edit-Steuerelementen

Rich Edit 3,0 ist eine Auflistung von Schnittstellen auf höherer Ebene, die uniwriter nutzt, um textlayoutanwendungen von den Komplexitäten bestimmter Skripts zu isolieren. Die umfangreiche Bearbeitung ist die einfachste Möglichkeit für Anwendungen, komplexe Skripts anzuzeigen, auch wenn Ihr primärer Zweck nicht unbedingt das Text Layout ist. Die umfangreiche Bearbeitung bietet eine schnelle, vielseitige Bearbeitung von umfangreichem Unicode-Text und einfachem Text. Es umfasst umfangreiche Nachrichten-und COM-Schnittstellen, Textbearbeitung, Formatierung, Zeilenumbruch, einfaches Tabellenlayout, vertikales Text Layout, bidirektionales Text Layout, indic-und thailändische Unterstützung, eine Bearbeitungs Benutzeroberfläche ähnlich wie Microsoft Word und Textobjekt Modell Schnittstellen.

Zusammen mit den Rich-Edit-Schnittstellen können Anwendungen mithilfe der [**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta) -Funktion für Rich-Edit automatisch Zeilen analysieren, strukturieren, positionieren und umbrechen. Weitere Informationen finden Sie unter [Rich Edit](../controls/rich-edit-controls.md)-Steuerelemente.

## <a name="complex-script-processing-using-uniscribe"></a>Komplexe Skript Verarbeitung mit unischreiber

[Uniwriter](uniscribe.md) bietet die umfassendste Unterstützung für die Verarbeitung von Text mit fein typografieeffekten und komplexen Skripts. Es unterstützt die komplexen Regeln in Skripts, wie z. b. Arabisch, de vanagari und Thai. Es behandelt Skripts, die von rechts nach links geschrieben werden, z. b. Arabisch und Hebräisch, und unterstützt das Mischen von Skripts. Uniscrimacht auch [OpenType](opentype-font-format.md) -Schriftart Features verfügbar, die von Anwendungen verwendet werden können, um feine typografieeffekte zu steuern. Weitere Informationen finden Sie unter [verarbeiten komplexer Skripts](processing-complex-scripts.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu uniscri](about-uniscribe.md)
</dt> <dt>

[Verarbeiten komplexer Skripts](processing-complex-scripts.md)
</dt> </dl>

 

 
