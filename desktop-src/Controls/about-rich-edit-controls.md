---
title: Informationen zu Rich Edit-Steuerelementen
description: In diesem Abschnitt werden Rich Edit-Steuerelemente vorgestellt.
ms.assetid: ab9dcdf4-a311-4159-8f37-e67e144f31f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d95f6dc1cc1f37bf604e6c0a891f92cd20bb7af6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "106337267"
---
# <a name="about-rich-edit-controls"></a>Informationen zu Rich Edit-Steuerelementen

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Versionen von Rich Edit](#versions-of-rich-edit)
    -   [Rich Edit-Version 1,0](#rich-edit-version-10)
    -   [Rich Edit-Version 2,0](#rich-edit-version-20)
    -   [Rich Edit-Version 3,0](#rich-edit-version-30)
    -   [Rich Edit-Version 4,1](#rich-edit-version-41)
-   [Nicht unterstützte Bearbeitungs Steuerelement-Funktionalität](#unsupported-edit-control-functionality)
-   [Tastenkombinationen für die reichhaltige Bearbeitung](#rich-edit-shortcut-keys)
-   [Zugehörige Themen](#related-topics)

## <a name="versions-of-rich-edit"></a>Versionen von Rich Edit

Die ursprüngliche Spezifikation für Rich Edit-Steuerelemente ist Microsoft Rich Edit 1,0; die aktuelle Spezifikation ist Microsoft Rich Edit 4,1. Jede Version der umfassenden Bearbeitung ist eine supermenge der oben genannten, mit der Ausnahme, dass nur asiatische Builds von Microsoft Rich Edit 1,0 über eine vertikale Text Option verfügen. Vor dem Erstellen eines Rich-Edit-Steuer Elements sollte die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion aufgerufen werden, um zu überprüfen, welche Version von Microsoft Rich Edit installiert ist.

In der folgenden Tabelle ist aufgeführt, welche DLL mit welcher Version von Rich Edit übereinstimmt. Beachten Sie, dass der Name der Datei nicht von Version 2,0 in Version 3,0 geändert wurde. Dies ermöglicht die Aktualisierung von Version 2,0 auf Version 3,0, ohne vorhandenen Code zu unterbrechen.



| Rich-Edit-Version | DLL          | Window-Klasse    |
|-------------------|--------------|-----------------|
| 1.0               | Riched32.dll | RichEdit- \_ Klasse |
| 2.0               | Riched20.dll | RichEdit- \_ Klasse |
| 3.0               | Riched20.dll | RichEdit- \_ Klasse |
| 4,1               | Msftedit.dll | MSF-dit- \_ Klasse |



 

### <a name="rich-edit-version-10"></a>Rich Edit-Version 1,0

Microsoft Rich Edit 1,0 umfasst die folgenden Features.



|                                                                                    |                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Text Eingabe und-Auswahl                                                           | Überwiegend Standard-(System Bearbeitungssteuerung) Auswahl und Text Eintrag. Auswahl leisten Unterstützung (die Auswahl Leiste ist ein nicht markierter Bereich auf der linken Seite der einzelnen Absätze, der die Zeile auswählt). Optionen für Wort Umbruch und automatische Wort Auswahl. Einzel-, Doppel-und Triple-Click-Auswahl. |
| Bearbeitung von ANSI (Einzel Byte-Zeichensatz (SBCS) und Multibytezeichen-Zeichensatz (MBCS) | Es ist jedoch keine Unicode-Bearbeitung vorhanden.                                                                                                                                                                                                                                                     |
| Grundlegender Satz von Eigenschaften für Zeichen/Absatz Formatierung                             | Weitere Informationen finden Sie unter [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) und [**paraformat**](/windows/desktop/api/Richedit/ns-richedit-paraformat).                                                                                                                                                                                                                |
| Zeichen Formatierungs Eigenschaften                                                    | Schriftart Name und-Größe, Fett, kursiv, einfarbig Unterstreichung, ausgehender Text, geschützt, Links, Offset und Textfarbe.                                                                                                                                                                                   |
| Absatz Formatierungs Eigenschaften                                                    | Eingangs Einzug, rechter Einzug, nachfolgende Zeilen Offset, Aufzählungs Zeichen, Ausrichtung (Links, zentriert, rechts) und Registerkarten.                                                                                                                                                                                    |
| Vorwärts suchen                                                                       | Beinhaltet Optionen ohne Berücksichtigung der Groß-/Kleinschreibung und Match-ganz wortoptionen.                                                                                                                                                                                                                                   |
| Nachrichten basierte Schnittstelle                                                            | Fast eine supermenge des System Bearbeitungs Steuerungs-Nachrichten Satzes plus zwei Schnittstellen, [**iricheditole**](/windows/desktop/api/Richole/nn-richole-iricheditole) und [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback).                                                                                                              |
| Eingebettete Objekte                                                                   | Erfordert die Client Zusammenarbeit basierend auf der [**iricheditole**](/windows/desktop/api/Richole/nn-richole-iricheditole) -und der [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) -Schnittstelle.                                                                                                                                          |
| Unterstützung für die Rechte Schaltfläche                                                          | Verwendet die [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) -Schnittstelle.                                                                                                                                                                                                                      |
| Bearbeitung per Drag & Drop                                                              | Die Drag & Drop-Bearbeitung wird unterstützt.                                                                                                                                                                                                                                                       |
| Benachrichtigungen                                                                      | [**WM \_**](/windows/desktop/menurc/wm-command) An den Client gesendete Befehls Meldungen sowie eine Reihe von anderen. Dies ist eine übergeordnete Gruppe von Benachrichtigungen über allgemeine Steuerelemente.                                                                                                                                                 |
| Rückgängig/Wiederholen auf einer Ebene                                                             | Verhält sich ähnlich wie das Bearbeitungs Steuerelement von System. Durch Auswahl von rückgängig wird die letzte Aktion **Rückgängig** gemacht, und diese **Aktion wird dann zur neuen Wiederholungs** Aktion.                                                                                                                                          |
| Einfacher vertikaler Text                                                               | (Nur asiatische Builds).                                                                                                                                                                                                                                                                      |
| Unterstützung für Eingabemethoden-Editor (IME)                                                  | (Nur asiatische Builds).                                                                                                                                                                                                                                                                      |
| WYSIWYG-Bearbeitung mithilfe von druckermetriken                                              | Diese Funktion ist insbesondere für Microsoft WordPad erforderlich.                                                                                                                                                                                                                              |
| Ausschneiden/Kopieren/Einfügen/Streaming/StreamOut                                                  | Mit nur-Text (**CF \_ Text**) oder RTF (Rich Text Format) mit und ohne Objekte.                                                                                                                                                                                                        |
| C-Codebasis                                                                        | Der Code ist in C geschrieben, der eine solide und vielseitige Grundlage bereitstellt.                                                                                                                                                                                                                |
| Unterschiedliche Builds für verschiedene Skripts                                             | Microsoft Rich Edit 1,0 behandelt Lokalisierungs Probleme mit unterschiedlichen Builds.                                                                                                                                                                                                              |



 

### <a name="rich-edit-version-20"></a>Rich Edit-Version 2,0

Microsoft Rich Edit 2,0 hat mehrere zusätzliche Features integriert, z. b. Unterstützung für Unicode-und asiatische Sprachen, mehrstufige rückgängig-, Component Object Model (com)-Schnittstellen und zahlreiche Erweiterungen der Benutzeroberfläche.

Microsoft Rich Edit 2,0 umfasst neben den Features von [Microsoft Rich Edit 1,0](#rich-edit-version-10)die folgenden Features.



|                                               |                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unicode                                       | Mit Unicode wird der Aufwand für die Verarbeitung von internationalem Text erleichtert. Der Aufwand ist jedoch erforderlich, um die Kompatibilität mit vorhandenen nicht-Unicode-Dokumenten aufrechtzuerhalten, d. h. die Möglichkeit, in/aus nicht-Unicode-Plain und Rich-Text zu konvertieren.                                                                                                                                                             |
| Allgemeiner Internationaler Support                 | Allgemeiner Zeilenumbruch Algorithmus (Erweiterung der Kinsoku-Regeln), einfaches Verknüpfen von Schriftart, Tastatur Schriftart wechseln.                                                                                                                                                                                                                                                                          |
| Asiatischer Support                                 | Ebene 2 (Dialogfeld) und 3 (Inline) werden in IMEs unterstützt.                                                                                                                                                                                                                                                                                                                            |
| Unterstützung für die Suche nach oben und nach unten                     | Die vorwärts-und Rückwärtssuche wird unterstützt.                                                                                                                                                                                                                                                                                                                                         |
| Bidirektionaler Support                         | Diese ist in Microsoft Rich Edit 2,1 enthalten.                                                                                                                                                                                                                                                                                                                                          |
| Mehrstufige rückgängig machen                               | Eine erweiterbare rückgängig-Architektur ermöglicht es dem Client, am Anwendungs weiten rückgängig-Modell teilzunehmen.                                                                                                                                                                                                                                                                                         |
| Unterstützung von Magellan Maus                        | Dabei handelt es sich um die Maus mit einer Walze für den Bildlauf.                                                                                                                                                                                                                                                                                                                                       |
| Unterstützung für duale Schriftart                             | Mit der Tastatur können Schriftarten automatisch gewechselt werden, wenn die aktive Schriftart für die aktuelle Tastatur ungeeignet ist, z. b. Kanji-Zeichen in den Uhrzeiten New Roman.                                                                                                                                                                                                                            |
| Intelligente Schriftart anwenden                              | Der Schriftart Change Request wendet keine westlichen Schriftarten auf asiatische Zeichen an.                                                                                                                                                                                                                                                                                                                |
| Verbesserte Anzeige                              | Eine Offscreen-Bitmap wird verwendet, wenn mehrere Schriftarten in derselben Zeile vorkommen. Dadurch kann z. b. der letzte Buchstabe des Worts "cool" nicht abgeschnitten werden.                                                                                                                                                                                                                           |
| Transparenz Unterstützung                          | Auch im fensterlosen Modus.                                                                                                                                                                                                                                                                                                                                                             |
| System Auswahl Farben                       | Wird zum Auswählen von Text verwendet.                                                                                                                                                                                                                                                                                                                                                             |
| Automatische URL-Erkennung                     | Kann auf eine Reihe von URL-Formaten (z. b. http:) überprüfen                                                                                                                                                                                                                                                                                                                           |
| Kompatibilität mit Microsoft Word-Benutzeroberfläche bearbeiten          | Auswahl, Cursor-Keypad-Semantik.                                                                                                                                                                                                                                                                                                                                                  |
| Word Standard EoP                             | Die Ende-der-Absatz Marke (CR) kann auch Wagen Rücklauf/Zeilenvorschub (CR/LF) verarbeiten (Wagen Rücklauf, Zeilenvorschub).                                                                                                                                                                                                                                                                       |
| Nur-Text-und Rich-Text-Funktionalität | Einzelzeichen Format und Einzel Absatzformat.                                                                                                                                                                                                                                                                                                                                 |
| Einzeilige und mehrzeilige Steuerelemente            | Kürzen Sie das erste Ende des Absatzes und keinen WordWrap.                                                                                                                                                                                                                                                                                                                                  |
| Zugriffstasten                              | Zugriffstasten werden unterstützt.                                                                                                                                                                                                                                                                                                                                                      |
| Stil des Kenn Wort Fensters                         | Steuerelemente zur Kenn Wort Bearbeitung werden über [**EM \_ getpasswordchar**](em-getpasswordchar.md) und [**EM \_ setpasswordchar**](em-setpasswordchar.md)bereitgestellt.                                                                                                                                                                                                                                 |
| Skalierbare Architektur                         | Zum Reduzieren der instanzgröße.                                                                                                                                                                                                                                                                                                                                                             |
| Fensterlose Operation und Schnittstellen           | Dies wird über die Schnittstellen [**itexthost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) und [**itextservices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) bereitgestellt.                                                                                                                                                                                                                                                                   |
| Duale com-Schnittstellen                           | Tom (Text Object Model)-Schnittstellen.                                                                                                                                                                                                                                                                                                                                                  |
| CHARFORMAT2                                   | Hinzugefügte Schrift Breite, Hintergrundfarbe, Gebiets Schema Bezeichner, unterstrichungstyp, hoch gestellt und Index (zusätzlich zu Offset), deaktivierter Effekt. Bei RTF-Roundtrips wurde die Menge zwischen Buchstaben, der Twip-Größe, oberhalb der das Kern Zeichenpaar, der animierte Texttyp, verschiedene Effekte hinzugefügt: Schriftart Schatten/-Gliederung, alle Obergrenzen, kleine, verborgene, geprägte, Schattierungs-und überarbeitetes Zeichen. |
| PARAFORMAT2                                   | Leerraum vor und nach und Zeilenabstand. Nur für RTF-Roundtrips, hinzugefügte Schattierungs Gewichtung/-Format, Nummerierung von Start/Stil/Tab, Rahmen Bereich/Breite/Seiten, Registerkarten Ausrichtung/Führungskräfte, verschiedene Wort Absatz Effekte: RTL-Absatz, keep, Keep-Next, page-break-before, No-line-number, No-Witwe-Control, do-not-hyphenate, nebeneinander.                                         |
| Weitere RTF-Roundtrips                        | Alle Word formatfont-und formatparagraph-Eigenschaften.                                                                                                                                                                                                                                                                                                                           |
| Code Stabilität und-Stabilisierung              | Beispiele: Überprüfung von Parametern und Objekten, Funktions invarianten, Wiederaufnahme Wächter, Objekt Stabilisierung.                                                                                                                                                                                                                                                                             |
| Starke Testinfrastruktur                 | Einschließlich umfassender Regressionen Tests.                                                                                                                                                                                                                                                                                                                                               |
| Verbesserte Leistung                          | Kleinere Workingsets, schnellere Lade-und Neuanzeige Zeiten usw.                                                                                                                                                                                                                                                                                                                     |
| C++-Codebasis                                 | Der Code ist in C++ geschrieben und bietet eine solide Grundlage für die Erstellung von Microsoft Rich Edit 3,0.                                                                                                                                                                                                                                                                             |



 

Mit einigen Ausnahmen verwendet Microsoft Rich Edit 2,0 dieselben Funktionen, Strukturen und Nachrichten wie Microsoft Rich Edit 1,0. Beachten Sie jedoch die folgenden Unterschiede:

-   Der Name der Microsoft Rich Edit 1,0 Window-Klasse lautet **RichEdit**. Microsoft Rich Edit 2,0 verfügt über die ANSI-und Unicode-Fenster Klassen **RichEdit20A** bzw. **RichEdit20W** . Um die entsprechende Rich-Edit-Fenster Klasse anzugeben, verwenden Sie die RichEdit- \_ Klassen Konstante, die die RichEdit. h-Datei abhängig von der Definition des Unicode-Kompilierungs Flags definiert.
-   Wenn Sie in Microsoft Rich Edit 2,0 ein Unicode-Rich-Edit-Steuerelement erstellen (eines, das Unicode-Textnachrichten erwartet), müssen Sie nur Unicode-Daten in allen Fenster Nachrichten angeben, die an das Steuerelement gesendet werden. Ebenso sollten Sie beim Erstellen eines ANSI-Rich-Edit-Steuer Elements nur ANSI-oder Double-Byte-Zeichensatz Daten (DBCS) senden. Sie können die [**iswindowunicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) -Funktion verwenden, um zu bestimmen, ob ein Rich-Edit-Steuerelement Unicode-Textnachrichten verwendet. Beachten Sie, dass die Rich-Edit-com-Schnittstellen Unicode-Text verwenden, es sei denn, Sie stoßen auf
-   Microsoft Rich Edit 1,0 verwendete CR/LF-Zeichenkombinationen für Absatz Marker. Microsoft Rich Edit 2,0 hat nur ein Wagen Rücklauf Zeichen (" \\ r") verwendet. Microsoft Rich Edit 3,0 verwendet nur ein Wagen Rücklauf Zeichen, kann jedoch Microsoft Rich Edit 1,0 in dieser Hinsicht emulieren.
-   Microsoft Rich Edit 2,0 hat die folgenden neuen Nachrichten eingeführt. 

    | `Message`                                           | BESCHREIBUNG                                                             |
    |---------------------------------------------------|-------------------------------------------------------------------------|
    | [**EM \_ autourldetect**](em-autourldetect.md)     | Aktiviert oder deaktiviert die automatische URL-Erkennung.                            |
    | [**EM \_ CanRedo**](em-canredo.md)                 | Bestimmt, ob in der Wiederholungs Warteschlange Aktionen vorhanden sind.             |
    | [**EM \_ getimecompmode**](em-getimecompmode.md)   | Ruft den aktuellen IME-Modus (Eingabemethoden-Editor) ab.                   |
    | [**EM \_ getlangoptions**](em-getlangoptions.md)   | Ruft Optionen für die Unterstützung von IME und asiatischer Sprache ab.                   |
    | [**EM \_ getredoname**](em-getredoname.md)         | Ruft den Typnamen der nächsten Aktion in der Wiederholungs Warteschlange ab.           |
    | [**EM \_ gettextmode**](em-gettextmode.md)         | Ruft den Textmodus oder die rückgängig-Ebene ab.                                  |
    | [**EM \_ getundoname**](em-getundoname.md)         | Ruft den Typnamen der nächsten Aktion in der Rückgängig-Warteschlange ab.           |
    | [**EM- \_ Wiederholung**](em-redo.md)                       | Führt die nächste Aktion in der Wiederholungs Warteschlange erneut aus.                               |
    | [**EM \_ setlangoptions**](em-setlangoptions.md)   | Legt Optionen für die Unterstützung von IME und asiatischer Sprache fest.                        |
    | [**EM \_ settextmode**](em-settextmode.md)         | Legt den Textmodus oder die rückgängig-Ebene fest.                                       |
    | [**EM- \_ tundolimit**](em-setundolimit.md)       | Legt die maximale Anzahl von Aktionen in der Rückgängig-Warteschlange fest.                   |
    | [**EM \_ stopgrouptypisierung**](em-stopgrouptyping.md) | Beendet das Gruppieren aufeinander folgender Typisierungsaktionen in der aktuellen Rückgängig-Aktion. |

    

     

-   Microsoft Rich Edit 2,0 führte die folgenden neuen Strukturen ein. 

    | Struktur                          | BESCHREIBUNG                                      |
    |------------------------------------|--------------------------------------------------|
    | [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) | Enthält Informationen über die Zeichen Formatierung. |
    | [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) | Enthält Informationen über die Absatz Formatierung. |

    

     

-   Die folgenden Meldungen werden nur in asiatischen Sprachversionen von Microsoft Rich Edit 1,0 unterstützt. Sie werden in höheren Versionen der Rich Edit-Version nicht unterstützt.

    [**EM- \_ vposition**](em-convposition.md)

    [**EM \_ getimecolor**](em-getimecolor.md)

    [**EM \_ getIMEOptions**](em-getimeoptions.md)

    [**EM- \_ Zeichensatz**](em-getpunctuation.md)

    [**EM \_ getwordwrapmode**](em-getwordwrapmode.md)

    [**EM- \_ Zeit Farbe**](em-setimecolor.md)

    [**EM- \_ Zeit Optionen**](em-setimeoptions.md)

    [**EM- \_ setinterpunktions Zeichen**](em-setpunctuation.md)

    [**EM \_ setwordwrapmode**](em-setwordwrapmode.md)

### <a name="rich-edit-version-30"></a>Rich Edit-Version 3,0

Microsoft Rich Edit 3,0 ist eine einzelne, skalierbare, Welt weite dll, die hohe Leistung und Kompatibilität mit Word in einem kleinen Paket bietet. Zu den neuen Features für Microsoft Rich Edit 3,0 zählen mehr Text, Zoom, Schriftart Bindung, leistungsfähigere IME-Unterstützung und umfangreiche komplexe Skriptunterstützung (bidirektional, indic und Thai).

Microsoft Rich Edit 3,0 umfasst zusätzlich zu den Features, die von der [Rich Edit-Version 2,0](#rich-edit-version-20)bereitgestellt werden, die folgenden Features.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Zoom</td>
<td>Der Zoomfaktor wird durch ein Verhältnis angegeben.</td>
</tr>
<tr class="even">
<td>Absatz Nummerierung (Einzel Ebene)</td>
<td>Numeric, Upper und Lower alphabetisch oder Roman numeral.</td>
</tr>
<tr class="odd">
<td>Einfache Tabellen</td>
<td>Das Löschen und Einfügen von Zeilen ist möglich, aber weder die Größe noch das umwickeln in Zellen. Wenn die erweiterte Typografie aktiviert ist (siehe <a href="em-gettypographyoptions.md"><strong>EM_GETTYPOGRAPHYOPTIONS</strong></a>), kann Microsoft Rich Edit 3,0 Spalten zentriert oder leert ausrichten und Dezimalstellen einschließen. Zellen werden von Registerkarten simuliert, sodass Text Registerkarten und Wagen Rückläufe durch Leerzeichen ersetzt werden.</td>
</tr>
<tr class="even">
<td>Normale und Überschriften Stile</td>
<td>Integrierte normale Stil-und Überschrift Stile 1 bis 9 werden von den Schnittstellen <a href="em-setparaformat.md"><strong>EM_SETPARAFORMAT</strong></a> und <a href="text-object-model.md">Text Objektmodell</a> (Tom) unterstützt.</td>
</tr>
<tr class="odd">
<td>Weitere Unterstreichung von Typen</td>
<td>Gestrichelte, Bindestriche, Bindestriche und Punkte werden hinzugefügt.</td>
</tr>
<tr class="even">
<td>Unterstreichung der Farbgebung</td>
<td>Unterstrichener Text kann mit einer von 15 Dokument Optionen für unterstrich Farben gekennzeichnet werden.</td>
</tr>
<tr class="odd">
<td>Verborgener Text</td>
<td>Gekennzeichnet durch das CHARFORMAT2-Attribut. Nützlich für das Roundtrips (Schreiben in eine Datei, was gelesen wurde) von Informationen, die normalerweise nicht angezeigt werden sollten.</td>
</tr>
<tr class="even">
<td>Weitere standardmäßige Kürzungs Tasten</td>
<td>Diese Abkürzungs Tasten funktionieren identisch mit denen in Word. Z. b. die europäischen Akzent-Schlüssel (nur US-Tastaturen). Number Hot Key (STRG + L) durchläuft die verfügbaren nummerierungoptionen, beginnend mit dem Aufzählungs Zeichen.</td>
</tr>
<tr class="odd">
<td>Hexin Unicode-IME</td>
<td>Ermöglicht Benutzern das Konvertieren zwischen hexadezimal und Unicode mithilfe von Abkürzungs Schlüsseln.</td>
</tr>
<tr class="even">
<td>Smarttags</td>
<td>Diese Funktion wird von Strg + Alt + ' für die Tastatur in den USA ein-und ausgeschaltet.</td>
</tr>
<tr class="odd">
<td>Weiche Bindestriche</td>
<td>Verwenden Sie für Klartext den Text 0xAD. Verwenden Sie für RTF \- .</td>
</tr>
<tr class="even">
<td>Kursiv Cursor</td>
<td>Außerdem wird der Maus Cursor bei über-URLs in eine Hand geändert.</td>
</tr>
<tr class="odd">
<td>Erweiterte typografieoption</td>
<td>Microsoft Rich Edit 3,0 kann eine erweiterte typografieoption für Zeilenumbruch und-Anzeige verwenden (siehe <a href="em-gettypographyoptions.md"><strong>EM_GETTYPOGRAPHYOPTIONS</strong></a>). Diese elegante Option wurde hauptsächlich hinzugefügt, um die Verarbeitung komplexer Skripts (bidirektional, indic und Thai) zu vereinfachen. Außerdem treten für einfache Skripts eine Reihe von Verbesserungen auf. Beispiele:
<ul>
<li>Zentrieren, rechts, Dezimaltrennzeichen</li>
<li>Vollständig berechtigter Text</li>
<li>Unterstreichung der Durchschnittswerte, was eine einheitliche Unterstreichung bietet, auch wenn angrenzende Text Ausführungen unterschiedliche Schriftgrößen aufweisen.</li>
</ul></td>
</tr>
<tr class="even">
<td> Unterstützung komplexer Skripts</td>
<td>Microsoft Rich Edit 3,0 unterstützt bidirektionale (Text mit Arabisch und/oder Hebräisch gemischt mit anderen Skripts), indic (indische Skripts wie "de vangari") und thailändischer Text. Zur Unterstützung dieser komplexen Skripts werden die erweiterten typografiekomponenten und uniscriekomponenten verwendet.</td>
</tr>
<tr class="odd">
<td>Schriftart Bindung</td>
<td>Microsoft Rich Edit 3,0 wählt automatisch eine passende Schriftart für Zeichen aus, die eindeutig nicht zum aktuellen Zeichensatz Stempel gehören. Dies erfolgt durch Zuweisen von Zeichensätzen zu Textläufen und Zuordnen von Schriftarten zu diesen Zeichensätzen. Weitere Informationen finden Sie unter <a href="using-rich-edit-controls.md">Schriftart Bindung</a>.</td>
</tr>
<tr class="even">
<td>Nur-Text-Lese-/Schreiboptionen für Zeichensätze</td>
<td>Dies ermöglicht das Lesen einer Datei mit einem Zeichensatz und das Schreiben mit einem anderen Zeichensatz.</td>
</tr>
<tr class="odd">
<td>UTF-8 RTF</td>
<td>Dies wird für das Ausschnitten, kopieren und Einfügen von Vorgängen empfohlen. Dieses Dateiformat ist kompakter als normale RTF, schneller und kompatibel mit Unicode.</td>
</tr>
<tr class="even">
<td>Microsoft Office 9 IME-Unterstützung (IME98)</td>
<td>Diese leistungsfähigere IME-Funktion wurde in ein unabhängiges Modul aufgeteilt. Folgende Features sind enthalten:
<ul>
<li>Neukonvertierung in früheren Versionen musste der Benutzer zuerst die endgültige Zeichenfolge löschen und dann eine neue Zeichenfolge eingeben, um zum richtigen Kandidaten zu gelangen. Mit dieser neuen Funktion kann der Benutzer die endgültige Zeichenfolge wieder in den Kompositions Modus konvertieren und so eine einfache Auswahl einer anderen Kandidaten Zeichenfolge ermöglichen.<br/></li>
<li>Dokument Feed diese Funktion bietet IME98 den Text für den aktuellen Absatz, mit dem IME98 bei der Eingabe eine genauere Konvertierung durchführen kann.<br/></li>
<li>Maus Betrieb diese Funktion ermöglicht eine bessere Steuerung der Kandidaten-und Benutzeroberflächen Fenster während der Eingabe.<br/></li>
<li>Position der Einfügemarke diese Funktion stellt die aktuellen Einfügemarke und die Zeilen Informationen bereit, die IME98 zum Positionieren von UI-Fenstern verwendet (z. b. eine Kandidatenliste).<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Unterstützung für Active Input Method Manager (IMM)</td>
<td>Benutzer können das aktive imm-Objekt aufrufen, das es Benutzern ermöglicht, asiatische Zeichen in US-Systemen einzugeben.</td>
</tr>
<tr class="even">
<td>Hexin-Unicode-Unterstützung</td>
<td>Benutzer können mithilfe von Tastenkombinationen zwischen hexadezimal Schreibweise und Unicode konvertieren.</td>
</tr>
<tr class="odd">
<td>Weitere RTF-Roundtrips</td>
<td>RTF-Text, der aus einer Datei gelesen wird, wird intakt zurückgeschrieben.</td>
</tr>
<tr class="even">
<td>Verbesserter 1,0-Kompatibilitätsmodus</td>
<td>Microsoft Rich Edit 3,0 kann das Microsoft Rich Edit 1,0-Verhalten emulieren. Beispielsweise ist es möglich, zwischen den MBCS-und Unicode-Zuordnungen (Zeichenposition) zu wechseln.</td>
</tr>
<tr class="odd">
<td>Höheres Freeze-Steuerelement</td>
<td>Die Anzeige kann über mehrere API-Aufrufe fixiert und dann nicht eingefroren werden, um die Updates anzuzeigen.</td>
</tr>
<tr class="even">
<td>Erhöhter rückgängig-Kontrolle</td>
<td>Rückgängigmachen können angehalten und fortgesetzt werden (eine IME-Anforderung).</td>
</tr>
<tr class="odd">
<td>Schriftgröße vergrößern/verkleinern</td>
<td>Erhöht oder verringert die Schriftgröße auf einen von sechs Standardwerten (12, 28, 36, 48, 72 und 80 Punkte).</td>
</tr>
</tbody>
</table>



 

### <a name="rich-edit-version-41"></a>Rich Edit-Version 4,1

Die Fenster Klasse für Microsoft Rich Edit 4,1 ist die MSF- \_ Klasse. Zu den neuen Features für Microsoft Rich Edit 4,1 zählen die Unterstützung von hyphenation, Seiten Drehung und Unterstützung von Text Services Framework (TSF).

Microsoft Rich Edit 4,1 umfasst zusätzlich zu den Features, die von der [Rich Edit-Version 3,0](#rich-edit-version-30)bereitgestellt werden, die folgenden Features.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Silben Trennung</td>
<td>Die Bindestriche werden über die folgenden APIs unterstützt: " <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>hyphenateproc</em></a>", " <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a>" und " <a href="em-gethyphenateinfo.md"><strong>EM_GETHYPHENATEINFO</strong></a>".</td>
</tr>
<tr class="even">
<td>Seiten Drehung</td>
<td>Das Layout von oben nach unten und von unten nach oben wird durch <a href="em-setpagerotate.md"><strong>EM_SETPAGEROTATE</strong></a> und <a href="em-getpagerotate.md"><strong>EM_GETPAGEROTATE</strong></a>unterstützt.</td>
</tr>
<tr class="odd">
<td>Unterstützung für Text Dienst Framework</td>
<td><ul>
<li>Verwenden Sie zum Aktivieren von TSF und bestimmten TSF-Features die folgenden Stile in <a href="em-seteditstyle.md"><strong>EM_SETEDITSTYLE</strong></a>: SES_USECTF, SES_CTFALLOWEMBED, SES_CTFALLOWPROOFING und SES_CTFALLOWSMARTTAG.</li>
<li>Um den TSF-modusbias festzulegen und zu erhalten, verwenden Sie <a href="em-setctfmodebias.md"><strong>EM_SETCTFMODEBIAS</strong></a> und <a href="em-getctfmodebias.md"><strong>EM_GETCTFMODEBIAS</strong></a>.</li>
<li>Um den TSF-Tastatur Status festzulegen und zu erhalten, verwenden Sie <a href="em-setctfopenstatus.md"><strong>EM_SETCTFOPENSTATUS</strong></a> und <a href="em-getctfopenstatus.md"><strong>EM_GETCTFOPENSTATUS</strong></a>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Zusätzliche IME-Unterstützung</td>
<td><ul>
<li>Um den IME-modusbias festzulegen und zu erhalten, verwenden Sie <a href="em-setimemodebias.md"><strong>EM_SETIMEMODEBIAS</strong></a> und <a href="em-getimemodebias.md"><strong>EM_GETIMEMODEBIAS</strong></a>.</li>
<li>Verwenden Sie <a href="em-getimeproperty.md"><strong>EM_GETIMEPROPERTY</strong></a>, um die Eigenschaften und Funktionen des IME zu erhalten.</li>
<li>Verwenden Sie <a href="em-getimecomptext.md"><strong>EM_GETIMECOMPTEXT</strong></a>, um den IME-Kompositions Text zu erhalten.</li>
<li>Verwenden Sie <a href="em-isime.md"><strong>EM_ISIME</strong></a>, um zu bestimmen, ob das Gebiets Schema ein ostasiatische Gebiets Schema ist.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Zusätzliche <a href="em-seteditstyle.md"><strong>EM_SETEDITSTYLE</strong></a> Einstellungen</td>
<td>Neben den TSF-Einstellungen gibt es neue Einstellungen, die IMEs ausschließen, den bidirektionalen Text Fluss festlegen, draftmode-Schriftarten verwenden und vieles mehr.</td>
</tr>
<tr class="even">
<td>Zusätzliche <a href="em-setcharformat.md"><strong>EM_SETCHARFORMAT</strong></a> Einstellungen</td>
<td>Neue Flags ermöglichen es dem Client, die Standard Schriftart und Schriftgröße für eine bestimmte LCID oder einen bestimmten Zeichensatz festzulegen, um die Standard Schriftart für das Steuerelement festzulegen, um zu verhindern, dass der Tastatur Wechsel der Schriftart entspricht.</td>
</tr>
<tr class="odd">
<td>Einschränken der Eingabe auf ANSI-Text</td>
<td>Durch die Verwendung von <a href="/windows/win32/api/richedit/ne-richedit-textmode"><strong>TM_SINGLECODEPAGE</strong></a> in <a href="em-settextmode.md"><strong>EM_SETTEXTMODE</strong></a> wird verhindert, dass Unicode-Eingaben in ein Rich Edit</td>
</tr>
<tr class="even">
<td>Nicht unterstützte RTF-Schlüsselwort Benachrichtigung.</td>
<td><a href="en-lowfirtf.md">EN_LOWFIRTF</a> eine Anwendung gewarnt, wenn ein nicht unterstütztes RTF-Schlüsselwort vorhanden ist.</td>
</tr>
<tr class="odd">
<td>Zusätzliche Sprachunterstützung</td>
<td>Weitere Sprachen sind "Armenisch", "Divehi", "Telugu" und andere.</td>
</tr>
<tr class="even">
<td>Verbesserte Tabellen Unterstützung</td>
<td>Zu den Features gehören: umschließen innerhalb von Zellen, verbesserte Handhabung über RTF und verbesserte Navigation.</td>
</tr>
<tr class="odd">
<td>ES_VERTICAL</td>
<td>Der <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> Fenster Stil wird unterstützt.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-unichar"><strong>WM_UNICHAR</strong></a> Unterstützung</td>
<td>Verwenden Sie <a href="/windows/desktop/inputdev/wm-unichar"><strong>WM_UNICHAR</strong></a>, um Unicode-Zeichen an ANSI-Fenster zu senden oder zu veröffentlichen. Dies entspricht <a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a>, aber es wird (UTF)-32 verwendet.</td>
</tr>
</tbody>
</table>



 

## <a name="unsupported-edit-control-functionality"></a>Nicht unterstützte Bearbeitungs Steuerelement-Funktionalität

Rich Edit-Steuerelemente unterstützen die meisten, aber nicht alle Funktionen für mehrzeilige Bearbeitungs Steuerelemente. In diesem Abschnitt werden die Bearbeitungs Steuerelement Meldungen und Fenster Stile aufgelistet, die von Rich-Edit-Steuerelementen *nicht* unterstützt werden.

Die folgenden Meldungen werden von Bearbeitungs Steuerelementen verarbeitet, aber *nicht* von Rich Edit-Steuerelementen.



| Nicht unterstützte Nachricht                         | Kommentare                                                                                                                    |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**EM- \_ Zeilen Trennlinien**](em-fmtlines.md)         | Wird nicht unterstützt.                                                                                                              |
| [**EM \_ GetHandle**](em-gethandle.md)       | Rich Edit-Steuerelemente speichern Text nicht als einfaches Zeichen Array.                                                       |
| [**EM \_ getimestatus**](em-getimestatus.md) | Wird nicht unterstützt.                                                                                                              |
| [**EM- \_ getMargin**](em-getmargins.md)     | Wird nicht unterstützt.                                                                                                              |
| [**EM- \_ andle**](em-sethandle.md)       | Rich Edit-Steuerelemente speichern Text nicht als einfaches Zeichen Array.                                                       |
| [**EM- \_ Zeit Status**](em-setimestatus.md) | Wird nicht unterstützt.                                                                                                              |
| [**EM- \_ setMargin**](em-setmargins.md)     | Unterstützt in Microsoft Rich Edit 3,0.                                                                                       |
| [**EM \_ setrectnp**](em-setrectnp.md)       | Wird nicht unterstützt.                                                                                                              |
| [**EM- \_ settabstopps**](em-settabstops.md)   | Stattdessen wird die [**EM \_ SetParaFormat**](em-setparaformat.md) -Meldung verwendet. Unterstützt in Microsoft Rich Edit 3,0.<br/> |
| [**WM \_ CtlColor**](/windows/desktop/DevNotes/wm-ctlcolor-)    | Stattdessen wird die " [**EM \_ setbkgndcolor**](em-setbkgndcolor.md) "-Meldung verwendet.                                                  |
| [**WM- \_ getFont**](/windows/desktop/winmsg/wm-getfont)        | Stattdessen wird die [**EM \_ getcharformat**](em-getcharformat.md) -Meldung verwendet.                                                  |



 

Die folgenden Fenster Stile werden mit mehrzeiligen Bearbeitungs Steuerelementen verwendet, aber nicht mit Rich Edit-Steuerelementen: [**es sind \_ klein**](edit-control-styles.md)Buchstaben, [**es \_ Großbuchstaben**](edit-control-styles.md)und [**es \_ oemconvert**](edit-control-styles.md).

## <a name="rich-edit-shortcut-keys"></a>Tastenkombinationen für die reichhaltige Bearbeitung

Rich Edit-Steuerelemente unterstützen die folgenden Tastenkombinationen.



| Schlüssel                      | Operations                                                                                                                               | Kommentare                                                                                                                                                                                                                       |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Umschalt + Rücktaste           | Generieren eines LRM/LRM auf einer Bidi-Tastatur                                                                                                    | Bidi-spezifisch                                                                                                                                                                                                                  |
| STRG+TAB                  | Registerkarte                                                                                                                                      |                                                                                                                                                                                                                                |
| STRG + Clear                | Alles auswählen                                                                                                                               |                                                                                                                                                                                                                                |
| STRG + Zahlen-Pad 5         | Alles auswählen                                                                                                                               |                                                                                                                                                                                                                                |
| STRG+A                    | Alles auswählen                                                                                                                               |                                                                                                                                                                                                                                |
| STRG+E                    | Ausrichtung zentrieren                                                                                                                         |                                                                                                                                                                                                                                |
| STRG+J                    | Ausrichtung rechtfertigen                                                                                                                        |                                                                                                                                                                                                                                |
| STRG+R                    | Rechte Ausrichtung                                                                                                                          |                                                                                                                                                                                                                                |
| STRG+L                    | Linke Ausrichtung                                                                                                                           |                                                                                                                                                                                                                                |
| STRG+C                    | Kopieren                                                                                                                                     |                                                                                                                                                                                                                                |
| STRG+V                    | Einfügen                                                                                                                                    |                                                                                                                                                                                                                                |
| STRG+X                    | Ausschneiden                                                                                                                                      |                                                                                                                                                                                                                                |
| STRG+Z                    | Rückgängig                                                                                                                                     |                                                                                                                                                                                                                                |
| STRG+Y                    | Wiederholen                                                                                                                                     |                                                                                                                                                                                                                                |
| Strg + "+" (STRG + UMSCHALT + "=") | Hochgestellt                                                                                                                              |                                                                                                                                                                                                                                |
| STRG + ' = '                  | Tiefgestellt                                                                                                                                |                                                                                                                                                                                                                                |
| STRG+1                    | Zeilenabstand = 1 Zeile.                                                                                                                   |                                                                                                                                                                                                                                |
| STRG+2                    | Zeilenabstand = 2 Zeilen.                                                                                                                  |                                                                                                                                                                                                                                |
| STRG+5                    | Zeilenabstand = 1,5 Zeilen.                                                                                                                |                                                                                                                                                                                                                                |
| STRG + ' (Apostroph)       | Akzente akut                                                                                                                             | Nach dem Drücken der Kurztaste drücken Sie den entsprechenden Buchstaben (z. b. a, e oder u). Dies gilt nur für Englisch, Französisch, Deutsch, Italienisch und Spanisch.                                                         |
| STRG + \` (Grab)           | Akzent                                                                                                                             | Siehe STRG + ' Kommentare.                                                                                                                                                                                                           |
| STRG + ~ (Tilde)            | Akzent Tilde                                                                                                                             | Siehe STRG + ' Kommentare.                                                                                                                                                                                                           |
| STRG +; Semikolon        | Akzent                                                                                                                            | Siehe STRG + ' Kommentare.                                                                                                                                                                                                           |
| STRG + UMSCHALT + 6              | Akzent-Caretzeichen (umgangen)                                                                                                                | Siehe STRG + ' Kommentare.                                                                                                                                                                                                           |
| STRG +, (Komma)            | Akzent cedilla                                                                                                                           | Siehe STRG + ' Kommentare.                                                                                                                                                                                                           |
| STRG + UMSCHALT + ' (Apostroph) | Smarttags aktivieren                                                                                                                    |                                                                                                                                                                                                                                |
| Rücktaste                 | Wenn der Text geschützt ist, sollten Sie ihn nicht löschen. Andernfalls sollten Sie das vorherige Zeichen löschen.                                                   |                                                                                                                                                                                                                                |
| STRG+RÜCKTASTE            | Vorheriges Wort löschen. Dadurch wird ein VK- \_ F16-Code generiert.                                                                                     |                                                                                                                                                                                                                                |
| F16                       | Identisch mit Rückraum.                                                                                                                       |                                                                                                                                                                                                                                |
| STRG+EINFG               | Kopieren                                                                                                                                     |                                                                                                                                                                                                                                |
| UMSCHALT + EINFG              | Einfügen                                                                                                                                    |                                                                                                                                                                                                                                |
| Einfügen                    | Overwrite                                                                                                                                | DBCS überschreibt nicht.                                                                                                                                                                                                       |
| STRG+NACH-LINKS           | Bewegen Sie den Cursor um ein Wort nach links.                                                                                                        | Auf Bidi-Tastatur hängt dies von der Textrichtung ab.                                                                                                                                                                   |
| STRG+NACH-RECHTS          | Bewegen Sie den Cursor um ein Wort nach rechts.                                                                                                       | Weitere Informationen finden Sie unter Strg + Pfeil nach links.                                                                                                                                                                                                  |
| STRG + Left Shift           | Linke Ausrichtung                                                                                                                           | In Bidi-Dokumenten ist dies die Lesereihenfolge von links nach rechts.                                                                                                                                                                    |
| STRG + Rechte UMSCHALTTASTE          | Rechte Ausrichtung                                                                                                                          | In Bidi-Dokumenten ist dies die Lesefolge von rechts nach links.                                                                                                                                                                    |
| STRG+NACH-OBEN             | Wechseln Sie zur obigen Zeile.                                                                                                                  |                                                                                                                                                                                                                                |
| STRG+NACH-UNTEN           | Wechseln Sie zur nachfolgenden Zeile.                                                                                                                  |                                                                                                                                                                                                                                |
| STRG+POS1                 | Zum Anfang des Dokuments wechseln.                                                                                                   |                                                                                                                                                                                                                                |
| STRG+ENDE                  | Springt zum Ende des Dokuments                                                                                                         |                                                                                                                                                                                                                                |
| STRG + Bild-auf              | Verschieben Sie eine Seite nach oben.                                                                                                                        | Wenn Sie im Systemadministrator Modus und einzeiligen Steuerelement keine Aktion ausführen.                                                                                                                                                                      |
| STRG + Bild-ab            | Verschieben Sie eine Seite nach unten.                                                                                                                      | Weitere Informationen finden Sie auf der Seite STRG + Bild-auf                                                                                                                                                                                                     |
| STRG+ENTF               | Löschen Sie das nächste Wort oder die ausgewählten Zeichen.                                                                                             |                                                                                                                                                                                                                                |
| UMSCHALT+ENTF              | Schneidet die ausgewählten Zeichen aus.                                                                                                             |                                                                                                                                                                                                                                |
| ESC                       | Ziehen Sie Drag & amp; Drop.                                                                                                                          | Beim Drag & Drop von Text.                                                                                                                                                                                               |
| ALT + ESC                   | Ändern Sie die aktive Anwendung.                                                                                                           |                                                                                                                                                                                                                                |
| ALT+X                     | Konvertiert den hexadezimalen Unicode-Wert vor der Einfügemarke in das entsprechende Unicode-Zeichen.                             |                                                                                                                                                                                                                                |
| ALT + UMSCHALT + X               | Konvertiert das Unicode-Zeichen vor der Einfügemarke in den entsprechenden Unicode-Hexadezimalwert.                             |                                                                                                                                                                                                                                |
| Alt + 0xxx (Zahlen-Pad)     | Fügt Unicode-Werte ein, wenn xxx größer als 255 ist. Wenn xxx kleiner als 256 ist, wird der ASCI-Bereichs Text basierend auf der aktuellen Tastatur eingefügt. | Muss Dezimalwerte eingeben.                                                                                                                                                                                                     |
| ALT + UMSCHALT + STRG + F12        | Hex in Unicode.                                                                                                                          | Für den Fall, dass alt + X bereits für eine andere Verwendung verwendet wird.                                                                                                                                                                                |
| ALT + UMSCHALT + STRG + F11        | Der ausgewählte Text wird im Debuggerfenster ausgegeben und in% Temp% \\DumpFontInfo.txt gespeichert.                                               | Nur für Debug (muss Flag = 8 in Win.ini festlegen)                                                                                                                                                                                 |
| STRG + UMSCHALT + A              | Legen Sie alle Caps fest.                                                                                                                            |                                                                                                                                                                                                                                |
| STRG+UMSCHALT+L              | Der Aufzählungs Zeichenstil.                                                                                                                     |                                                                                                                                                                                                                                |
| STRG+UMSCHALT+NACH-RECHTS    | Vergrößern Sie den Schrift Grad.                                                                                                                      | Schriftart Größe ändert sich um einen Punkt im Bereich 4pt-11pt; von 2 Punkten für 12pt-28pt; Es ändert sich von 28pt-> 36pt-> 48pt-> 72pt-> 80pt; Es ändert sich um 10 Punkte im Bereich 80pt-1630pt; der Höchstwert ist 1638. |
| STRG+UMSCHALT+NACH-LINKS     | Verringern Sie den Schrift Grad.                                                                                                                      | Siehe STRG + UMSCHALT + nach-rechts-Taste.                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Fensterlose Rich Edit-Steuerelemente](windowless-rich-edit-controls.md)
</dt> </dl>

