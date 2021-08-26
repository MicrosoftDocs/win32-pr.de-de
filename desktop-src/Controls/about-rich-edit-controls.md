---
title: Informationen zu Rich Edit-Steuerelementen
description: In diesem Abschnitt werden umfassende Bearbeitungssteuerelemente vorgestellt.
ms.assetid: ab9dcdf4-a311-4159-8f37-e67e144f31f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d528ceff19bfc1e377bf8297b40a7495fc92385e49b57724b6a81902a5ec499
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922400"
---
# <a name="about-rich-edit-controls"></a>Informationen zu Rich Edit-Steuerelementen

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Versionen von Rich Edit](#versions-of-rich-edit)
    -   [Rich Edit Version 1.0](#rich-edit-version-10)
    -   [Rich Edit Version 2.0](#rich-edit-version-20)
    -   [Rich Edit Version 3.0](#rich-edit-version-30)
    -   [Rich Edit Version 4.1](#rich-edit-version-41)
-   [Nicht unterstützte Bearbeitungssteuerelementfunktionalität](#unsupported-edit-control-functionality)
-   [Rich Edit-Tastenkombinationen](#rich-edit-shortcut-keys)
-   [Zugehörige Themen](#related-topics)

## <a name="versions-of-rich-edit"></a>Versionen von Rich Edit

Die ursprüngliche Spezifikation für Rich Edit-Steuerelemente ist Microsoft Rich Edit 1.0. Die aktuelle Spezifikation ist Microsoft Rich Edit 4.1. Jede Version von Rich Edit ist eine Obermenge der vorherigen, mit der Ausnahme, dass nur asiatische Builds von Microsoft Rich Edit 1.0 über eine vertikale Textoption verfügen. Bevor Sie ein Rich Edit-Steuerelement erstellen, sollten Sie die [**LoadLibrary-Funktion**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) aufrufen, um zu überprüfen, welche Version von Microsoft Rich Edit installiert ist.

Die folgende Tabelle zeigt, welche DLL welcher Version von Rich Edit entspricht. Beachten Sie, dass sich der Name der Datei nicht von Version 2.0 in Version 3.0 geändert hat. Dadurch kann Version 2.0 auf Version 3.0 aktualisiert werden, ohne dass vorhandener Code unterbrochen wird.



| Rich Edit-Version | DLL          | Window-Klasse    |
|-------------------|--------------|-----------------|
| 1.0               | Riched32.dll | \_RICHEDIT-KLASSE |
| 2.0               | Riched20.dll | \_RICHEDIT-KLASSE |
| 3.0               | Riched20.dll | \_RICHEDIT-KLASSE |
| 4.1               | Msftedit.dll | \_MSFTEDIT-KLASSE |



 

### <a name="rich-edit-version-10"></a>Rich Edit Version 1.0

Microsoft Rich Edit 1.0 umfasst die folgenden Features.



|    Funktion   | BESCHREIBUNG   |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Texteingabe und -auswahl                                                           | Größtenteils Standardmäßige Auswahl und Eingabe von Text (Systembearbeitungssteuerelement). Unterstützung der Auswahlleiste (die Auswahlleiste ist ein nicht markierter Bereich links neben jedem Absatz, in dem beim Klicken die Zeile ausgewählt wird). Optionen für Zeilenumbruch und automatisches Auswählen von Wörtern. Einzel-, Doppel- und Dreiklickauswahl. |
| BEARBEITUNG VON ANSI (Single-Byte-Zeichensatz (SBCS) und Multibyte-Zeichensatz (MBCS)) | Es gibt jedoch keine Unicode-Bearbeitung.                                                                                                                                                                                                                                                     |
| Grundlegende Zeichen-/Absatzformatierungseigenschaften                             | Siehe [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) und [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat).                                                                                                                                                                                                                |
| Eigenschaften der Zeichenformatierung                                                    | Schriftname und Schriftgrad, fett, kursiv, Volltonunterstärkung, durchgestrichen, geschützt, Link, Offset und Textfarbe.                                                                                                                                                                                   |
| Absatzformatierungseigenschaften                                                    | Starteinzug, rechter Einzug, nachfolgender Zeilenoffset, Aufzählungszeichen, Ausrichtung (links, mitte, rechts) und Registerkarten.                                                                                                                                                                                    |
| Vorwärts suchen                                                                       | Schließt Optionen ohne Unterscheidung nach Groß-/Kleinschreibung und Übereinstimmung mit ganzen Wörtern ein.                                                                                                                                                                                                                                   |
| Nachrichtenbasierte Schnittstelle                                                            | Fast eine Obermenge des Meldungssatzes für die Bearbeitungssteuerung des Systems plus zwei Schnittstellen, [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) und [**IRichEditOleCallback.**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback)                                                                                                              |
| Eingebettete Objekte                                                                   | Erfordert die Zusammenarbeit von Clients basierend auf [**IRichEditOle-**](/windows/desktop/api/Richole/nn-richole-iricheditole) und [**IRichEditOleCallback-Schnittstellen.**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback)                                                                                                                                          |
| Unterstützung des Menüs mit der rechten Maustaste                                                          | Verwendet die [**IRichEditOleCallback-Schnittstelle.**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback)                                                                                                                                                                                                                      |
| Drag & Drop-Bearbeitung                                                              | Drag & Drop-Bearbeitung wird unterstützt.                                                                                                                                                                                                                                                       |
| Benachrichtigungen                                                                      | [**WM \_ COMMAND-Nachrichten,**](/windows/desktop/menurc/wm-command) die an den Client gesendet werden, sowie eine Reihe anderer Nachrichten. Dies ist eine Obermenge von Benachrichtigungen mit allgemeiner Steuerung.                                                                                                                                                 |
| Rückgängig/Wiederholen auf einer einzelnen Ebene                                                             | Verhält sich ähnlich wie das Bearbeitungssteuerelement des Systems. Wenn Sie **Rückgängig** auswählen, wird die letzte Aktion rückgängig gemacht, und diese Aktion wird dann zur neuen **Wiederholungsaktion.**                                                                                                                                          |
| Einfacher vertikaler Text                                                               | (Nur asiatisch erstellt).                                                                                                                                                                                                                                                                      |
| Unterstützung des Eingabemethoden-Editors (INPUT Method Editor, IME)                                                  | (Nur asiatisch erstellt).                                                                                                                                                                                                                                                                      |
| WYSIWYG-Bearbeitung mitHilfe von Druckermetriken                                              | Dieses Feature ist insbesondere für Microsoft WordPad erforderlich.                                                                                                                                                                                                                              |
| Ausschneiden/Kopieren/Einfügen/StreamIn/StreamOut                                                  | Mit Nur-Text (**CF \_ TEXT**) oder Rich Text Format (RTF) mit und ohne -Objekten.                                                                                                                                                                                                        |
| C-Codebasis                                                                        | Der Code ist in C geschrieben und bietet eine solide und vielseitig einsetzbare Grundlage.                                                                                                                                                                                                                |
| Verschiedene Builds für verschiedene Skripts                                             | Microsoft Rich Edit 1.0 behandelt Lokalisierungsprobleme mit verschiedenen Builds.                                                                                                                                                                                                              |



 

### <a name="rich-edit-version-20"></a>Rich Edit Version 2.0

Microsoft Rich Edit 2.0 umfasste mehrere zusätzliche Features, z. B. Unterstützung für Unicode- und asienische Sprachen, rückgängig machen auf mehreren Ebenen, Component Object Model(COM)-Schnittstellen und zahlreiche Verbesserungen der Benutzeroberfläche.

Microsoft Rich Edit 2.0 enthält zusätzlich zu den Features von [Microsoft Rich Edit 1.0](#rich-edit-version-10)die folgenden Features.



|    Funktion                                           |    BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unicode                                       | Unicode erleichtert den Aufwand bei der Verarbeitung von internationalem Text. Es ist jedoch ein Aufwand erforderlich, um die Kompatibilität mit vorhandenen Nicht-Unicode-Dokumenten aufrechtzuerhalten, d. h. die Möglichkeit, Nur-Unicode-Text und Rich-Text in/aus Nicht-Unicode zu konvertieren.                                                                                                                                                             |
| Allgemeine internationale Unterstützung                 | Allgemeiner Algorithmus für Zeilenumbrüche (Erweiterung der Kinsoku-Regeln), einfache Schriftartverknüpfung, Tastaturschriftartwechsel.                                                                                                                                                                                                                                                                          |
| Unterstützung für Asien                                 | Ebene 2 (Dialogfeld) und 3 (Inline) werden in IMEs unterstützt.                                                                                                                                                                                                                                                                                                                            |
| Unterstützung für Suche/Suche nach unten                     | Die Vorwärts- und Rückwärtssuche wird unterstützt.                                                                                                                                                                                                                                                                                                                                         |
| Bidirektionale Unterstützung                         | Dies ist in Microsoft Rich Edit 2.1 enthalten.                                                                                                                                                                                                                                                                                                                                          |
| Rückgängig auf mehreren Ebenen                               | Eine erweiterbare Undo-Architektur ermöglicht dem Client die Teilnahme am anwendungsweiten Rückgängig-Modell.                                                                                                                                                                                                                                                                                         |
| Magellan-Mausunterstützung                        | Dies ist die Maus mit einer Rolle zum Scrollen.                                                                                                                                                                                                                                                                                                                                       |
| Unterstützung für Doppelschriftarten                             | Die Tastatur kann Schriftarten automatisch wechseln, wenn die aktive Schriftart für die aktuelle Tastatur ungeeignet ist, z. B. Kanji-Zeichen in Times New Roman.                                                                                                                                                                                                                            |
| Smart Font Apply                              | Die Anforderung zur Schriftartänderung wendet keine westen Schriftarten auf asiatische Zeichen an.                                                                                                                                                                                                                                                                                                                |
| Verbesserte Anzeige                              | Eine Off-Screen-Bitmap wird verwendet, wenn mehrere Schriftarten in derselben Zeile auftreten. Dadurch kann z. B. der letzte Buchstabe des Worts cool nicht abgeschnitten werden.                                                                                                                                                                                                                           |
| Transparenzunterstützung                          | Auch im fensterlosen Modus.                                                                                                                                                                                                                                                                                                                                                             |
| Farben der Systemauswahl                       | Wird zum Auswählen von Text verwendet.                                                                                                                                                                                                                                                                                                                                                             |
| Automatische URL-Erkennung                     | Kann eine Reihe von URL-Formaten überprüfen (z.B. http:).                                                                                                                                                                                                                                                                                                                           |
| Microsoft Word Bearbeiten der Benutzeroberflächenkompatibilität          | Auswahl, Cursor-Tastatur-Semantik.                                                                                                                                                                                                                                                                                                                                                  |
| Word-Standard-EOP                             | Die Absatzendemarke (End-of-Paragraph Mark, CR) kann auch Wagenrücklauf/Zeilenvorschub (CR/LF) (Wagenrücklauf, Zeilenvorschub) verarbeiten.                                                                                                                                                                                                                                                                       |
| Nur-Text- und Rich-Text-Funktionalität | Einzelzeichenformat und Einzel absatzformat.                                                                                                                                                                                                                                                                                                                                 |
| Einzeilige und mehrzeilige Steuerelemente            | Abschneiden am ersten Ende des Absatzes und kein Wordwrap.                                                                                                                                                                                                                                                                                                                                  |
| Zugriffstasten                              | Zugriffstasten werden unterstützt.                                                                                                                                                                                                                                                                                                                                                      |
| Format des Kennwortfensters                         | Steuerelemente zur Kennwortbearbeitung werden über [**EM \_ GETPASSWORDCHAR**](em-getpasswordchar.md) und [**EM \_ SETPASSWORDCHAR**](em-setpasswordchar.md)bereitgestellt.                                                                                                                                                                                                                                 |
| Skalierbare Architektur                         | So verringern Sie die Instanzgröße.                                                                                                                                                                                                                                                                                                                                                             |
| Fensterloser Betrieb und Schnittstellen           | Dies wird über die Schnittstellen [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) und [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) bereitgestellt.                                                                                                                                                                                                                                                                   |
| Duale COM-Schnittstellen                           | TOM-Schnittstellen (Text Object Model).                                                                                                                                                                                                                                                                                                                                                  |
| CHARFORMAT2                                   | Schriftbreite, Hintergrundfarbe, Gebietsschemabezeichner, Unterstreichungstyp, Superscript und Tiefgestellt (zusätzlich zum Offset), deaktivierter Effekt hinzugefügt. Nur beim RTF-Roundtripping wurde der Abstand zwischen Buchstaben, die Twipgröße, über die an kern-Zeichenpaar, animierter Texttyp, verschiedene Effekte angepasst: Schriftschatten/-kontur, alle Kapselungen, kleine Kapselungen, ausgeblendete, eingeblendete, vergrößerungsbasierte und überarbeitete. |
| PARAFORMAT2                                   | Leerzeichen vor und nach und Zeilenabstand von Word hinzugefügt. Nur für RTF-Roundtripping, hinzugefügte Schattierungsgewichtung/-stil, Nummerierung start/style/tab, Rahmenraum/Breite/Seiten, Tabstoppausrichtung/-leader, verschiedene Word-Absatzeffekte: RTL-Absatz, Keep, Keep-Next, Seitenumbruch vor, Keine Zeilennummer, Keine-Steuerelement-Steuerelement, Nicht-Bindestrich, nebeneinander.                                         |
| Weitere RTF-Roundtrippings                        | Alle Word-Eigenschaften FormatFont und FormatParagraph.                                                                                                                                                                                                                                                                                                                           |
| Codestabilität und Stabilisierung              | Beispiele: Parameter- und Objektvalidierung, Funktionsinvarianten, Reentrancy-Wächter, Objektstabilität.                                                                                                                                                                                                                                                                             |
| Starke Testinfrastruktur                 | Einschließlich umfangreicher Regressionstests.                                                                                                                                                                                                                                                                                                                                               |
| Verbesserte Leistung                          | Kleinere Arbeitsmenge, schnellere Lade- und erneute Anzeigezeiten usw.                                                                                                                                                                                                                                                                                                                     |
| C++-Codebasis                                 | Der Code ist in C++ geschrieben und bietet eine solide Grundlage für die Erstellung von Microsoft Rich Edit 3.0.                                                                                                                                                                                                                                                                             |



 

Mit einigen Ausnahmen verwendet Microsoft Rich Edit 2.0 die gleichen Funktionen, Strukturen und Nachrichten wie Microsoft Rich Edit 1.0. Beachten Sie jedoch die folgenden Unterschiede:

-   Der Name der Microsoft Rich Edit 1.0-Fensterklasse lautet **RichEdit.** Microsoft Rich Edit 2.0 verfügt über die Ansi- und Unicode-Fensterklassen **RichEdit20A** bzw. **RichEdit20W.** Um die entsprechende Rich Edit Window-Klasse anzugeben, verwenden Sie die RICHEDIT \_ CLASS-Konstante, die die Datei Richedit.h abhängig von der Definition des UNICODE-Kompilierungsflags definiert.
-   Wenn Sie in Microsoft Rich Edit 2.0 ein Unicode-Rich Edit-Steuerelement erstellen (ein Steuerelement, das Unicode-Textnachrichten erwartet), müssen Sie nur Unicode-Daten in allen Fenstermeldungen angeben, die an das Steuerelement gesendet werden. Wenn Sie ein ANSI-Rich-Edit-Steuerelement erstellen, senden Sie auf ähnliche Weise nur ANSI- oder Doppel-Byte-Zeichensatzdaten (DBCS). Sie können die [**IsWindowUnicode-Funktion**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) verwenden, um zu bestimmen, ob ein Rich Edit-Steuerelement Unicode-Textnachrichten verwendet. Beachten Sie, dass die RICH EDIT-COM-Schnittstellen Unicode-Text verwenden, es sei denn, sie stoßen auf ein Codepageargument.
-   Microsoft Rich Edit 1.0 verwendete CR/LF-Zeichenkombinationen für Absatzmarkierungen. Microsoft Rich Edit 2.0 hat nur ein Wagenrücklaufzeichen (' \\ r') verwendet. Microsoft Rich Edit 3.0 verwendet nur ein Wagenrücklaufzeichen, kann in diesem Zusammenhang jedoch Microsoft Rich Edit 1.0 emulieren.
-   In Microsoft Rich Edit 2.0 wurden die folgenden neuen Meldungen eingeführt. 

    | `Message`                                           | BESCHREIBUNG                                                             |
    |---------------------------------------------------|-------------------------------------------------------------------------|
    | [**EM \_ AUTOURLDETECT**](em-autourldetect.md)     | Aktiviert oder deaktiviert die automatische URL-Erkennung.                            |
    | [**EM \_ CANREDO**](em-canredo.md)                 | Bestimmt, ob aktionen in der Wiederholungswarteschlange vorhanden sind.             |
    | [**EM \_ GETIMECOMPMODE**](em-getimecompmode.md)   | Ruft den aktuellen IME-Modus (Input Method Editor) ab.                   |
    | [**EM \_ GETLANGOPTIONS**](em-getlangoptions.md)   | Ruft Optionen für IME- und Unterstützung für asiatisch-englischsprachige Sprachen ab.                   |
    | [**EM \_ GETREDONAME**](em-getredoname.md)         | Ruft den Typnamen der nächsten Aktion in der Wiederholungswarteschlange ab.           |
    | [**EM \_ GETTEXTMODE**](em-gettextmode.md)         | Ruft den Textmodus oder die Rückgängigebene ab.                                  |
    | [**EM \_ GETUNDONAME**](em-getundoname.md)         | Ruft den Typnamen der nächsten Aktion in der Rückgängig-Warteschlange ab.           |
    | [**EM \_ REDO**](em-redo.md)                       | Wiederholen der nächsten Aktion in der Wiederholungswarteschlange.                               |
    | [**EM \_ SETLANGOPTIONS**](em-setlangoptions.md)   | Legt Optionen für DIE IME- und Asiatisch-Sprachunterstützung fest.                        |
    | [**EM \_ SETTEXTMODE**](em-settextmode.md)         | Legt den Textmodus oder die Rückgängigebene fest.                                       |
    | [**EM \_ SETUNDOLIMIT**](em-setundolimit.md)       | Legt die maximale Anzahl von Aktionen in der Rückgängig-Warteschlange fest.                   |
    | [**EM \_ STOPGROUPTYPING**](em-stopgrouptyping.md) | Beendet die Gruppierung aufeinanderfolgender Eingabeaktionen in die aktuelle Rückgängigaktion. |

    

     

-   In Microsoft Rich Edit 2.0 wurden die folgenden neuen Strukturen eingeführt. 

    | Struktur                          | BESCHREIBUNG                                      |
    |------------------------------------|--------------------------------------------------|
    | [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) | Enthält Informationen zur Zeichenformatierung. |
    | [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) | Enthält Informationen zur Absatzformatierung. |

    

     

-   Die folgenden Meldungen werden nur in asiatisch-sprachigen Versionen von Microsoft Rich Edit 1.0 unterstützt. Sie werden in späteren Versionen von Rich Edit nicht unterstützt.

    [**EM \_ CONVPOSITION**](em-convposition.md)

    [**EM \_ GETIMECOLOR**](em-getimecolor.md)

    [**EM \_ GETIMEOPTIONS**](em-getimeoptions.md)

    [**EM \_ GETPUNCTUATION**](em-getpunctuation.md)

    [**EM \_ GETWORDWRAPMODE**](em-getwordwrapmode.md)

    [**EM \_ SETIMECOLOR**](em-setimecolor.md)

    [**EM \_ SETIMEOPTIONS**](em-setimeoptions.md)

    [**EM \_ SETPUNCTUATION**](em-setpunctuation.md)

    [**EM \_ SETWORDWRAPMODE**](em-setwordwrapmode.md)

### <a name="rich-edit-version-30"></a>Rich Edit Version 3.0

Microsoft Rich Edit 3.0 ist eine einzelne, skalierbare, weltweite DLL, die hohe Leistung und Kompatibilität mit Word in einem kleinen Paket bietet. Neue Features für Microsoft Rich Edit 3.0 sind u.a. richer text, zoom, font binding, leistungsfähigere IME-Unterstützung und umfassende Unterstützung komplexer Skripts (bidirektional, indic und thailändisch).

Microsoft Rich Edit 3.0 enthält zusätzlich zu den Features von [Rich Edit Version 2.0](#rich-edit-version-20)die folgenden Features.



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
<td>Nummerierung von Absätzen (einzelne Ebene)</td>
<td>Numerische, obere und untere alphabetische oder lateinische Zahl.</td>
</tr>
<tr class="odd">
<td>Einfache Tabellen</td>
<td>Das Löschen und Einfügen von Zeilen ist möglich, aber weder die Größe noch das Umschließen in Zellen. Wenn die erweiterte Typografie aktiviert ist (siehe <a href="em-gettypographyoptions.md"><strong>EM_GETTYPOGRAPHYOPTIONS),</strong></a>kann Microsoft Rich Edit 3.0 Spalten rechts oder zentriert ausrichten und Dezimalstellen enthalten. Zellen werden durch Registerkarten simuliert, sodass Textregisterkarte und Wagenrücklauf durch Leerzeichen ersetzt werden.</td>
</tr>
<tr class="even">
<td>Normale Stile und Überschriftenstile</td>
<td>Integrierte normale Stil- und Überschriftenstile 1 <a href="em-setparaformat.md"><strong></strong></a> bis 9 werden von den Tom-Schnittstellen EM_SETPARAFORMAT und <a href="text-object-model.md">Textobjektmodell</a> (Text Object Model, Textobjektmodell) unterstützt.</td>
</tr>
<tr class="odd">
<td>Weitere Unterstreichungstypen</td>
<td>Dashed-, dash-dot-, dash-dot-dot- und dot-Underlining wurden hinzugefügt.</td>
</tr>
<tr class="even">
<td>Färbung unterstrichen</td>
<td>Unterstrichener Text kann mit einer von 15 Dokumentoptionen für Unterstreichungsfarben gekennzeichnet werden.</td>
</tr>
<tr class="odd">
<td>Ausgeblendeter Text</td>
<td>Gekennzeichnet durch das CHARFORMAT2-Attribut. Praktisch für das Roundtripping (Schreiben in eine Datei, was eingelesen wurde) von Informationen, die normalerweise nicht angezeigt werden sollten.</td>
</tr>
<tr class="even">
<td>Weitere Standard-Hot Keys</td>
<td>Diese hot-Schlüssel funktionieren genauso wie die in Word. Beispiel: Europäische Akzenttasten (nur US-Tastaturen). Number Hot Key (STRG+L) durchzyklen die verfügbaren Nummerierungsoptionen, beginnend mit aufzählungszeichen.</td>
</tr>
<tr class="odd">
<td>HexToUnicode IME</td>
<td>Ermöglicht einem Benutzer das Konvertieren zwischen Hexadezimal- und Unicode-Code mithilfe von Hot-Schlüsseln.</td>
</tr>
<tr class="even">
<td>Intelligente Anführungszeichen</td>
<td>Dieses Feature wird für US-Tastaturen durch STRG+ALT+' ein- und ausgeschaltet.</td>
</tr>
<tr class="odd">
<td>Weiche Bindestriche</td>
<td>Verwenden Sie für Nur-Text 0xAD. Verwenden Sie für RTF \- .</td>
</tr>
<tr class="even">
<td>Kursivcursor</td>
<td>Darüber hinaus ändert sich der Mauszeiger in eine Hand, wenn über URLs angezeigt wird.</td>
</tr>
<tr class="odd">
<td>Erweiterte Typografieoption</td>
<td>Microsoft Rich Edit 3.0 kann eine erweiterte Typografieoption für Zeilenumbruch und -anzeige verwenden (siehe <a href="em-gettypographyoptions.md"><strong>EM_GETTYPOGRAPHYOPTIONS</strong></a>). Diese elegante Option wurde in erster Linie hinzugefügt, um die Verarbeitung komplexer Skripts (bidirektional, indic und thailändisch) zu erleichtern. Darüber hinaus gibt es eine Reihe von Verbesserungen für einfache Skripts. Beispiele:
<ul>
<li>Registerkarten "Mitte", "Rechts", "Dezimal"</li>
<li>Vollständig gerechtfertigter Text</li>
<li>Unterstreichung der Mittelung, die eine einheitliche Unterstreichung bietet, auch wenn benachbarte Textläufe unterschiedliche Schriftgrößen haben.</li>
</ul></td>
</tr>
<tr class="even">
<td> Unterstützung komplexer Skripts</td>
<td>Microsoft Rich Edit 3.0 unterstützt bidirektional (Text mit arabischer und/oder hebräischer Mischung mit anderen Skripts), Indic (hebräische Skripts wie Devanvan) und thailischer Text. Zur Unterstützung dieser komplexen Skripts werden die erweiterten Typografie- und Uniscribe-Komponenten verwendet.</td>
</tr>
<tr class="odd">
<td>Schriftartbindung</td>
<td>Microsoft Rich Edit 3.0 wählt automatisch eine geeignete Schriftart für Zeichen aus, die eindeutig nicht zum aktuellen Zeichensatzstempel gehören. Dies erfolgt durch Zuweisen von Zeichensätzen zu Textläufen und Zuordnen von Schriftarten zu diesen Zeichensätzen. Weitere Informationen finden Sie unter <a href="using-rich-edit-controls.md">Schriftartbindung.</a></td>
</tr>
<tr class="even">
<td>Nur-Text-Lese-/Schreiboptionen speziell für Zeichensätze</td>
<td>Dies ermöglicht das Lesen einer Datei mit einem Zeichensatz und das Schreiben mit einem anderen Zeichensatz.</td>
</tr>
<tr class="odd">
<td>UTF-8 RTF</td>
<td>Dies wird zum Ausschneiden, Kopieren und Einfing von Vorgängen empfohlen. Dieses Dateiformat ist kompakter als normale RTF, schneller und kompatibel mit Unicode.</td>
</tr>
<tr class="even">
<td>Microsoft Office 9 IME-Unterstützung (IME98)</td>
<td>Diese leistungsfähigere IME-Funktion wurde in ein unabhängiges Modul getrennt. Folgende Features sind enthalten:
<ul>
<li>Reconversion In früheren Versionen musste der Benutzer zuerst die endgültige Zeichenfolge löschen und dann eine neue Zeichenfolge eingeben, um zum richtigen Kandidaten zu kommen. Mit diesem neuen Feature kann der Benutzer die endgültige Zeichenfolge wieder in den Kompositionsmodus konvertieren und so eine einfache Auswahl einer anderen Kandidatenzeichenfolge ermöglichen.<br/></li>
<li>Dokumentfeed Dieses Feature stellt IME98 den Text für den aktuellen Absatz zur Unterstützung von IME98 bei der genaueren Konvertierung während der Eingabe zur Auswahl.<br/></li>
<li>Mausvorgang: Dieses Feature bietet eine bessere Kontrolle über die Kandidaten- und Benutzeroberflächenfenster während der Eingabe.<br/></li>
<li>Position des Caretstrichs: Dieses Feature stellt die aktuellen Caret- und Zeileninformationen zur Verfügung, die IME98 zum Positionieren von Benutzeroberflächenfenstern verwendet (z. B. eine Kandidatenliste).<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Unterstützung des Aktiven Eingabemethode-Managers (ACTIVE Input Method Manager, IMM)</td>
<td>Benutzer können das Active IMM-Objekt aufrufen, das es Benutzern ermöglicht, in US-Systemen zeichenasiatische Zeichen ein-/aus zu geben.</td>
</tr>
<tr class="even">
<td>HexToUnicode-Unterstützung</td>
<td>Benutzer können mithilfe von Hot-Schlüsseln zwischen Hexadezimal-Notation und Unicode konvertieren.</td>
</tr>
<tr class="odd">
<td>Weitere RTF-Roundtrippings</td>
<td>RTF-Text, der aus einer Datei eingelesen wird, wird intakt zurückgeschrieben.</td>
</tr>
<tr class="even">
<td>Verbesserter Kompatibilitätsmodus 1.0</td>
<td>Microsoft Rich Edit 3.0 kann das Verhalten von Microsoft Rich Edit 1.0 emulieren. Beispielsweise ist es möglich, zwischen MBCS- und Unicode-Zeichenpositionszuordnungen (cp) zu wechseln.</td>
</tr>
<tr class="odd">
<td>Verbesserte Steuerung des Einfrierens</td>
<td>Die Anzeige kann über mehrere API-Aufrufe eingefroren und dann zur Anzeige der Updates nicht mehr gesperrt werden.</td>
</tr>
<tr class="even">
<td>Verbesserte Rückgängig-Steuerung</td>
<td>Rückgängig machen kann angehalten und fortgesetzt werden (eine IME-Anforderung).</td>
</tr>
<tr class="odd">
<td>Erhöhen/Verringern des Schriftgrads</td>
<td>Erhöht oder verringert den Schriftgrad auf einen von sechs Standardwerten (12, 28, 36, 48, 72 und 80 Punkte).</td>
</tr>
</tbody>
</table>



 

### <a name="rich-edit-version-41"></a>Rich Edit Version 4.1

Die Fensterklasse für Microsoft Rich Edit 4.1 ist MSFTEDIT \_ CLASS. Neue Features für Microsoft Rich Edit 4.1 sind Bindestriche, Seitenrotation und unterstützung Textdienstframework (TSF).

Microsoft Rich Edit 4.1 enthält zusätzlich zu den Features von [Rich Edit Version 3.0](#rich-edit-version-30)die folgenden Features.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Hyphenation</td>
<td>Bindestriche werden über die folgenden APIs unterstützt: <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphnateProc,</em></a> <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a>und <a href="em-gethyphenateinfo.md"><strong>EM_GETHYPHENATEINFO</strong></a>.</td>
</tr>
<tr class="even">
<td>Seitenrotation</td>
<td>Das Layout von oben nach unten und von unten nach oben wird durch <a href="em-setpagerotate.md"><strong>EM_SETPAGEROTATE</strong></a> <a href="em-getpagerotate.md"><strong>und</strong></a>EM_GETPAGEROTATE.</td>
</tr>
<tr class="odd">
<td>Textdienstframework-Unterstützung</td>
<td><ul>
<li>Um TSF und bestimmte TSF-Features zu aktivieren, verwenden Sie die folgenden Stile in <a href="em-seteditstyle.md"><strong>EM_SETEDITSTYLE:</strong></a>SES_USECTF, SES_CTFALLOWEMBED, SES_CTFALLOWPROOFING und SES_CTFALLOWSMARTTAG.</li>
<li>Verwenden Sie zum Festlegen und Erhalten des TSF-Modus bias <a href="em-setctfmodebias.md"><strong>EM_SETCTFMODEBIAS</strong></a> und <a href="em-getctfmodebias.md"><strong>EM_GETCTFMODEBIAS.</strong></a></li>
<li>Verwenden Sie zum Festlegen und Erhalten des TSF-Tastaturstatus <a href="em-setctfopenstatus.md"><strong>EM_SETCTFOPENSTATUS</strong></a> und <a href="em-getctfopenstatus.md"><strong>EM_GETCTFOPENSTATUS</strong></a>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Zusätzliche IME-Unterstützung</td>
<td><ul>
<li>Verwenden Sie zum Festlegen und Erhalten des IME-Modus bias <a href="em-setimemodebias.md"><strong>EM_SETIMEMODEBIAS</strong></a> und <a href="em-getimemodebias.md"><strong>EM_GETIMEMODEBIAS</strong></a>.</li>
<li>Um die Eigenschaften und Funktionen des IME zu erhalten, verwenden <a href="em-getimeproperty.md"><strong>Sie EM_GETIMEPROPERTY</strong></a>.</li>
<li>Verwenden Sie zum Erhalten des IME-Kompositionstexts <a href="em-getimecomptext.md"><strong>EM_GETIMECOMPTEXT</strong></a>.</li>
<li>Um zu bestimmen, ob das Locale ein ostasiatisches Locale ist, verwenden <a href="em-isime.md"><strong>Sie EM_ISIME</strong></a>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Zusätzliche <a href="em-seteditstyle.md"><strong>EM_SETEDITSTYLE einstellungen</strong></a></td>
<td>Neben den TSF-Einstellungen gibt es neue Einstellungen, die IMEs ausschließen, bidirektionalen Textfluss festlegen, Draftmode-Schriftarten verwenden und vieles mehr.</td>
</tr>
<tr class="even">
<td>Zusätzliche <a href="em-setcharformat.md"><strong>EM_SETCHARFORMAT einstellungen</strong></a></td>
<td>Neue Flags ermöglichen es dem Client, die Standardschriftart und schriftgraden für eine bestimmte LCID oder einen angegebenen Zeichensatz, die Standardschriftart für das Steuerelement, das Verhindern des Tastaturwechsels für die Schriftart und mehr festlegen.</td>
</tr>
<tr class="odd">
<td>Einschränken der Eingabe auf ANSI-Text</td>
<td>Die <a href="/windows/win32/api/richedit/ne-richedit-textmode"><strong>TM_SINGLECODEPAGE</strong></a> in <a href="em-settextmode.md"><strong>EM_SETTEXTMODE verhindert,</strong></a> dass Unicode-Eingaben in ein Rich Edit-Steuerelement eingegeben werden.</td>
</tr>
<tr class="even">
<td>Nicht unterstützte RTF-Schlüsselwortbenachrichtigung</td>
<td><a href="en-lowfirtf.md">EN_LOWFIRTF</a> eine Anwendung, wenn es ein nicht unterstütztes RTF-Schlüsselwort gibt.</td>
</tr>
<tr class="odd">
<td>Zusätzliche Sprachunterstützung</td>
<td>Zu den weiteren Sprachen zählen Dies sind", "Divehi", "Telugu" und andere.</td>
</tr>
<tr class="even">
<td>Verbesserte Tabellenunterstützung</td>
<td>Zu den Features gehören: Umschließen innerhalb von Zellen, verbesserte Verarbeitung über RTF und verbesserte Navigation.</td>
</tr>
<tr class="odd">
<td>ES_VERTICAL</td>
<td>Der <a href="rich-edit-control-styles.md"><strong></strong></a> ES_VERTICAL-Fensterstil wird unterstützt.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-unichar"><strong>WM_UNICHAR-Unterstützung</strong></a></td>
<td>Verwenden Sie zum Senden oder Posten von Unicode-Zeichen an ANSI-Fenster <a href="/windows/desktop/inputdev/wm-unichar"><strong>WM_UNICHAR</strong></a>. Es entspricht <a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a>, verwendet jedoch (UTF)-32.</td>
</tr>
</tbody>
</table>



 

## <a name="unsupported-edit-control-functionality"></a>Nicht unterstützte Funktionen zum Bearbeiten von Steuerelementen

Umfangreiche Bearbeitungssteuerelemente unterstützen die meisten, aber nicht alle Funktionen für mehrline-Bearbeitungssteuerelemente. In diesem Abschnitt werden die Bearbeitungssteuerelemente und Fensterstile aufgeführt, *die von* rich-Bearbeitungssteuerelementen nicht unterstützt werden.

Die folgenden Meldungen werden von Bearbeitungssteuerelementen *verarbeitet, jedoch nicht von* Rich-Edit-Steuerelementen.



| Nicht unterstützte Nachricht                         | Kommentare                                                                                                                    |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**EM \_ FMTLINES**](em-fmtlines.md)         | Wird nicht unterstützt.                                                                                                              |
| [**EM \_ GETHANDLE**](em-gethandle.md)       | Rich-Edit-Steuerelemente speichern Text nicht als einfaches Array von Zeichen.                                                       |
| [**EM \_ GETIMESTATUS**](em-getimestatus.md) | Wird nicht unterstützt.                                                                                                              |
| [**EM \_ GETMARGINS**](em-getmargins.md)     | Wird nicht unterstützt.                                                                                                              |
| [**EM \_ SETHANDLE**](em-sethandle.md)       | Rich-Edit-Steuerelemente speichern Text nicht als einfaches Array von Zeichen.                                                       |
| [**EM \_ SETIMESTATUS**](em-setimestatus.md) | Wird nicht unterstützt.                                                                                                              |
| [**EM \_ SETMARGINS**](em-setmargins.md)     | Wird in Microsoft Rich Edit 3.0 unterstützt.                                                                                       |
| [**EM \_ SETRECTNP**](em-setrectnp.md)       | Wird nicht unterstützt.                                                                                                              |
| [**EM \_ SETTABSTOPS**](em-settabstops.md)   | Stattdessen [**wird die EM \_ SETPARAFORMAT-Nachricht**](em-setparaformat.md) verwendet. Wird in Microsoft Rich Edit 3.0 unterstützt.<br/> |
| [**WM \_ CTLCOLOR**](/windows/desktop/DevNotes/wm-ctlcolor-)    | Stattdessen [**wird die EM \_ SETBKGNDCOLOR-Meldung**](em-setbkgndcolor.md) verwendet.                                                  |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)        | Stattdessen [**wird die EM \_ GETCHARFORMAT-Nachricht**](em-getcharformat.md) verwendet.                                                  |



 

Die folgenden Fensterstile werden mit mehrstufigen Bearbeitungssteuerelementen verwendet, jedoch nicht mit rich edit-Steuerelementen: [**ES \_ LOWERCASE,**](edit-control-styles.md) [**ES \_ UPPERCASE**](edit-control-styles.md)und [**ES \_ OEMCONVERT**](edit-control-styles.md).

## <a name="rich-edit-shortcut-keys"></a>Tastenkombinationen für rich edit

Umfangreiche Bearbeitungssteuerelemente unterstützen die folgenden Tastenkombinationen.



| Schlüssel                      | Operations                                                                                                                               | Kommentare                                                                                                                                                                                                                       |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UMSCHALT+RÜCKTASTE           | Generieren eines LRM/LRM auf einer Bidi-Tastatur                                                                                                    | BiDi-spezifisch                                                                                                                                                                                                                  |
| STRG+TAB                  | Registerkarte                                                                                                                                      |                                                                                                                                                                                                                                |
| STRG+LÖSCHEN                | Alle auswählen                                                                                                                               |                                                                                                                                                                                                                                |
| STRG+Zahlenpad 5         | Alle auswählen                                                                                                                               |                                                                                                                                                                                                                                |
| STRG+A                    | Alle auswählen                                                                                                                               |                                                                                                                                                                                                                                |
| STRG+E                    | Zentrierung                                                                                                                         |                                                                                                                                                                                                                                |
| STRG+J                    | Ausrichtung rechtfertigen                                                                                                                        |                                                                                                                                                                                                                                |
| STRG+R                    | Rechte Ausrichtung                                                                                                                          |                                                                                                                                                                                                                                |
| STRG+L                    | Linke Ausrichtung                                                                                                                           |                                                                                                                                                                                                                                |
| STRG+C                    | Kopieren                                                                                                                                     |                                                                                                                                                                                                                                |
| STRG+V                    | Einfügen                                                                                                                                    |                                                                                                                                                                                                                                |
| STRG+X                    | Ausschneiden                                                                                                                                      |                                                                                                                                                                                                                                |
| STRG+Z                    | Rückgängig                                                                                                                                     |                                                                                                                                                                                                                                |
| STRG+Y                    | Wiederholen                                                                                                                                     |                                                                                                                                                                                                                                |
| STRG+'+' (STRG+UMSCHALT+'=') | Hochgestellt                                                                                                                              |                                                                                                                                                                                                                                |
| STRG+'='                  | Tiefgestellt                                                                                                                                |                                                                                                                                                                                                                                |
| STRG+1                    | Zeilenabstand = 1 Zeile.                                                                                                                   |                                                                                                                                                                                                                                |
| STRG+2                    | Zeilenabstand = 2 Zeilen.                                                                                                                  |                                                                                                                                                                                                                                |
| STRG+5                    | Zeilenabstand = 1,5 Zeilen.                                                                                                                |                                                                                                                                                                                                                                |
| STRG+' (Apostroph)       | Akzente                                                                                                                             | Nachdem Sie die Kurztaste gedrückt haben, drücken Sie den entsprechenden Buchstaben (z. B. a, e oder u). Dies gilt nur für die Tastaturen Englisch, Französisch, Deutsch, Italienisch und Spanisch.                                                         |
| STRG+ \` (Tastenkombination)           | Akzent                                                                                                                             | Weitere Informationen finden Sie unter STRG+-Kommentare.                                                                                                                                                                                                           |
| STRG+~ (Tilde)            | Akzentkachel                                                                                                                             | Weitere Informationen finden Sie unter STRG+-Kommentare.                                                                                                                                                                                                           |
| STRG+; (Semikolon)        | Accent umlaut                                                                                                                            | Weitere Informationen finden Sie unter STRG+'-Kommentare.                                                                                                                                                                                                           |
| STRG+UMSCHALT+6              | Akzent-Caretzeichen (accentflex)                                                                                                                | Weitere Informationen finden Sie unter STRG+'-Kommentare.                                                                                                                                                                                                           |
| STRG+, (Komma)            | Akzent cedilla                                                                                                                           | Weitere Informationen finden Sie unter STRG+'-Kommentare.                                                                                                                                                                                                           |
| STRG+UMSCHALT+' (Apostroph) | Aktivieren intelligenter Anführungszeichen                                                                                                                    |                                                                                                                                                                                                                                |
| Rückschritt                 | Wenn Text geschützt ist, signalisieren Sie ihn, und löschen Sie ihn nicht. Löschen Sie andernfalls das vorherige Zeichen.                                                   |                                                                                                                                                                                                                                |
| STRG+RÜCKTASTE            | Löschen Sie das vorherige Wort. Dadurch wird ein \_ VK-F16-Code generiert.                                                                                     |                                                                                                                                                                                                                                |
| F16                       | Identisch mit Rücktaste.                                                                                                                       |                                                                                                                                                                                                                                |
| STRG+EINFG               | Kopieren                                                                                                                                     |                                                                                                                                                                                                                                |
| UMSCHALT + EINFG              | Einfügen                                                                                                                                    |                                                                                                                                                                                                                                |
| Einfügen                    | Overwrite                                                                                                                                | DBCS überschreibt nicht.                                                                                                                                                                                                       |
| STRG+NACH-LINKS           | Bewegen Sie den Cursor um ein Wort nach links.                                                                                                        | Auf der Bidi-Tastatur hängt dies von der Richtung des Texts ab.                                                                                                                                                                   |
| STRG+NACH-RECHTS          | Bewegen Sie den Cursor um ein Wort nach rechts.                                                                                                       | Weitere Informationen finden Sie unter Strg+Linkspfeilkommentare.                                                                                                                                                                                                  |
| STRG+NACH-LINKS-UMSCHALTTASTE           | Linke Ausrichtung                                                                                                                           | In BiDi-Dokumenten ist dies für die Lesereihenfolge von links nach rechts vorgesehen.                                                                                                                                                                    |
| STRG+NACH-RECHTS-TASTE          | Rechtsausrichtung                                                                                                                          | In BiDi-Dokumenten ist dies für die Lesereihenfolge von rechts nach links vorgesehen.                                                                                                                                                                    |
| STRG+NACH-OBEN             | Wechseln Sie zur obigen Zeile.                                                                                                                  |                                                                                                                                                                                                                                |
| STRG+NACH-UNTEN           | Wechseln Sie zur folgenden Zeile.                                                                                                                  |                                                                                                                                                                                                                                |
| STRG+POS1                 | Wechseln Sie zum Anfang des Dokuments.                                                                                                   |                                                                                                                                                                                                                                |
| STRG+ENDE                  | Springt zum Ende des Dokuments                                                                                                         |                                                                                                                                                                                                                                |
| STRG+NACH-OBEN              | Verschieben Sie eine Seite nach oben.                                                                                                                        | Wenn sie sich in SystemEditMode und dem Single Line-Steuerelement befindet, tun Sie nichts.                                                                                                                                                                      |
| STRG+SEITE NACH-UNTEN            | Verschieben Sie eine Seite nach unten.                                                                                                                      | Weitere Informationen finden Sie unter STRG+NACH-OBEN-Kommentare.                                                                                                                                                                                                     |
| STRG+ENTF               | Löschen Sie das nächste Wort oder ausgewählte Zeichen.                                                                                             |                                                                                                                                                                                                                                |
| UMSCHALT+ENTF              | Schneiden Sie die ausgewählten Zeichen aus.                                                                                                             |                                                                                                                                                                                                                                |
| Esc                       | Beenden Sie drag-drop.                                                                                                                          | Während sie einen Drag & Drop von Text durchführen.                                                                                                                                                                                               |
| ALT+ESC                   | Ändern Sie die aktive Anwendung.                                                                                                           |                                                                                                                                                                                                                                |
| ALT+X                     | Konvertiert den Unicode-Hexadezimalwert vor der Einfügemarke in das entsprechende Unicode-Zeichen.                             |                                                                                                                                                                                                                                |
| ALT+UMSCHALT+X               | Konvertiert das Unicode-Zeichen vor der Einfügemarke in den entsprechenden Unicode-Hexadezimalwert.                             |                                                                                                                                                                                                                                |
| ALT+0xxx (Zahlenpad)     | Fügt Unicode-Werte ein, wenn xxx größer als 255 ist. Wenn xxx kleiner als 256 ist, wird ASCI-Bereichstext basierend auf der aktuellen Tastatur eingefügt. | Muss Dezimalwerte eingeben.                                                                                                                                                                                                     |
| ALT+UMSCHALT+STRG+F12        | Hexadezimal zu Unicode.                                                                                                                          | Für den Fall, dass ALT+X bereits für eine andere Verwendung verwendet wird.                                                                                                                                                                                |
| ALT+UMSCHALT+STRG+F11        | Ausgewählter Text wird im Debuggerfenster ausgegeben und in %temp% \\DumpFontInfo.txt gespeichert.                                               | Nur für Debuggen (flag=8 muss in Win.ini festgelegt werden)                                                                                                                                                                                 |
| STRG + UMSCHALT + A              | Legen Sie alle Obergrenzen fest.                                                                                                                            |                                                                                                                                                                                                                                |
| STRG+UMSCHALT+L              | Fiddle Bullet-Stil.                                                                                                                     |                                                                                                                                                                                                                                |
| STRG+UMSCHALT+NACH-RECHTS    | Erhöhen Sie den Schriftgrad.                                                                                                                      | Der Schriftgrad ändert sich um 1 Punkt im Bereich 4pt-11pt; um 2 Punkt für 12pt-28pt; er ändert sich von 28pt -> 36pt -> 48pt -> 72pt -> 80pt; er ändert sich um 10 Punkte im Bereich von 80pt bis 1630pt; der Höchstwert ist 1638. |
| STRG+UMSCHALT+NACH-LINKS     | Verkleinern Sie den Schriftgrad.                                                                                                                      | Weitere Informationen finden Sie unter STRG+UMSCHALT+NACH-RECHTS-TASTE.                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Fensterlose Rich Edit-Steuerelemente](windowless-rich-edit-controls.md)
</dt> </dl>

