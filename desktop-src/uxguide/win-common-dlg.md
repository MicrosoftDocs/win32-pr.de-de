---
title: Allgemeine Dialogfelder
description: Die allgemeinen Microsoft Windows-Dialoge bestehen aus den Dialogfeldern Datei öffnen, Datei speichern, Ordner öffnen, suchen und ersetzen, drucken, Seite einrichten, Schriftart und Farbe.
ms.assetid: 3f9fb0c9-bc1a-48c4-b021-99f155f8ea9e
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 336cb368fa25bf68313e2bf336de68845a87e663
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104393841"
---
# <a name="common-dialogs"></a>Allgemeine Dialogfelder

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Die allgemeinen Microsoft Windows-Dialoge bestehen aus den Dialogfeldern Datei öffnen, Datei speichern, Ordner öffnen, suchen und ersetzen, drucken, Seite einrichten, Schriftart und Farbe.

## <a name="open-file"></a>Datei öffnen

![Screenshot des Dialog Felds "Öffnen" ](images/win-common-dlg-image1.png)

Open File ist für die schnelle Suche nach Elementen zur Verwendung mit einem Programm optimiert.

## <a name="save-file"></a>Datei speichern

![Screenshot des Dialog Felds "Speichern unter" ](images/win-common-dlg-image2.png)

Datei speichern schließt die Schleife, indem eine Datei mit Ihren Metadaten gespeichert wird.

## <a name="open-folder"></a>Ordner öffnen

![Screenshot des Dialog Felds zum Suchen nach Dateien/Ordnern ](images/win-common-dlg-image3.png)

"Ordner öffnen" dient speziell zum Auswählen von Ordnern.

## <a name="find-and-replace"></a>Suchen und ersetzen

![Screenshot der Dialogfelder "suchen und ersetzen" ](images/win-common-dlg-image4.png)

Suchen ermöglicht es Benutzern, nach Text Zeichenfolgen zu suchen, während mit der Replace-Version optional Übereinstimmungen durch eine andere Zeichenfolge ersetzt werden können.

## <a name="print"></a>Drucken

![Screenshot des Druck Dialogfelds ](images/win-common-dlg-image5.png)

Der Druck ermöglicht es Benutzern, die auszudruckenden Elemente, die Anzahl der zu druckenden Kopien und die Sortierreihenfolge sowie die Möglichkeit zum auswählen und Konfigurieren von Druckern auszuwählen.

## <a name="page-setup"></a>Seiteneinrichtung

![Screenshot des Dialog Felds "Seite einrichten" ](images/win-common-dlg-image6.png)

Das Einrichten der Seite ermöglicht es Benutzern, das Papierformat und die Quelle, die Seitenausrichtung und die Ränder auszuwählen.

## <a name="font"></a>Schriftart

![Screenshot der Schriftart (Dialogfeld) ](images/win-common-dlg-image7.png)

Schriftart zeigt die Schriftarten und Punktgrößen der verfügbaren installierten Schriftarten an.

## <a name="color"></a>Color

![Screenshot des Dialog Felds "Farben bearbeiten" ](images/win-common-dlg-image8.png)

Mit Color können Benutzer eine Farbe auswählen, entweder über eine vordefinierte Gruppe von Farben oder durch Auswahl einer benutzerdefinierten Farbe.

## <a name="design-concepts"></a>Entwurfskonzepte

Mithilfe der allgemeinen Dialogfelder können Sie Benutzern ein konsistentes Verhalten in verschiedenen Programmen ermöglichen. Durch die Verwendung der häufig verwendeten Dialogfelder können Sie Benutzern auch eine effiziente, angenehme benutzerfreundliche Darstellung bieten.

Mit diesen Dialogfeldern können Sie die Benutzer Funktionen von Benutzern erheblich verbessern, indem Sie die am besten geeigneten Standardwerte für folgende

-   Eingabewerte (Beispiele: Standardordner, Standard Dateinamen).
-   Ausgewählte Optionen (Beispiele: ausgewählter Drucker, Druckoptionen).
-   Sichten (Beispiele: Anzeigen von Bildern in der Miniaturansicht, Anzeigen von Bildern ohne Dateinamen, Sortieren nach Datum, Spaltenbreite).
-   Präsentation (Beispiele: Fenstergröße, Speicherort und Inhalt).

Sie müssen sowohl die ursprünglichen als auch die nachfolgenden Standardwerte bestimmen. Anfängliche Standardwerte werden von Ihrem Programm bestimmt und basieren auf der erwarteten Verwendung des Ziel Benutzers, während die nachfolgenden Standardwerte auf der tatsächlichen Verwendung basieren. Die frühere Verwendung ist der beste Indikator für die zukünftige Verwendung.

Sind die Standardeinstellungen Ihres Programms effizient? Überwachen Sie die Anzahl der Schritte, die Benutzer ausführen müssen, um die gängigsten Aufgaben auszuführen. Wenn Benutzer bei jedem Ausführen einer Aufgabe die gleichen, möglicherweise unnötigen Schritte wiederholen müssen, können die Standardwerte verbessert werden.

**Wenn Sie nur eine Aktion ausführen...**

Ermöglichen Sie Benutzern eine effiziente, angenehme Benutzererlebnis, indem Sie die entsprechenden anfänglichen und nachfolgenden Standardwerte auswählen.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

**Zwar! Verwenden Sie die allgemeinen Dialogfelder für eine konsistente Benutzer Darstellung. Erstellen Sie keine eigenen.** Es ist besonders schwierig, benutzerdefinierte Benutzeroberflächen zu erstellen, die ordnungsgemäß und sicher im Namespace navigieren. Beachten Sie, dass Sie bei Bedarf die allgemeinen Dialogfelder anpassen können.

Für Windows Vista verfügen die Dateien "Öffnen" und "Speichern" über eine neue erweiterbare Architektur, um das Bereitstellen zusätzlicher Funktionen zu vereinfachen. Dieser Mechanismus ist flexibel genug, um die Mindestanforderungen an unabhängige Softwareanbieter (ISVs) zu erfüllen, aber nicht in zukünftigen Versionen von Windows.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   Stellen Sie ggf. mehr direkte [oder nicht](glossary.md) modere Alternativen bereit. Benutzern gestatten:
    -   Öffnen Sie Dateien, indem Sie Sie in Ihrem Programm ablegen.
    -   Speichern Sie Dateien mit dem aktuellen Namen und Speicherort mit einem Befehl zum Speichern.
    -   Suchen des nächsten Vorkommens einer Zeichenfolge mithilfe der F3-Taste.
    -   Druckt eine Kopie eines gesamten Dokuments mit einem Print-Befehl auf dem Standarddrucker.
    -   Ändern von Schriftarten und Schriftart Attributen mithilfe einer Symbolleiste oder eines Palettenfensters.
    -   Ändern Sie die Farben mithilfe einer Symbolleiste oder eines Palettenfensters.
-   Verwenden Sie die folgenden Befehle, um allgemeine Dialoge anzuzeigen (die zusammen mit Ihren bevorzugten [Zugriffs Schlüsseln](glossary.md)angegeben sind):



|                              |                                               |
|------------------------------|-----------------------------------------------|
| **Allgemeine Dialogfeld**<br/> | **Befehl**<br/>                        |
| Datei öffnen<br/>         | Öffnen...<br/>                            |
| Datei speichern<br/>         | Speichern unter...<br/>                         |
| Ordner öffnen<br/>       | Ordner öffnen... oder Ordner auswählen...<br/> |
| Suchen und Ersetzen<br/>  | Suchen... oder ersetzen Sie...<br/>              |
| Drucken<br/>             | Drucken...<br/>                           |
| Seite einrichten<br/>        | Seite einrichten...<br/>                      |
| Schriftart<br/>              | Schriftart... oder wählen Sie Schriftart...<br/>          |
| Color<br/>             | Farbe... oder wählen Sie Farbe...<br/>        |



 

-   Sie können je nach Bedarf spezifischere Befehle verwenden. Beispiel: Verwenden Sie zum Exportieren einer Datei die Befehls Export Datei anstelle von "Speichern unter".
-   Legen Sie den Titel des Dialog Felds auf den Befehl wieder Beispiel: Wenn Datei speichern über einen Befehl zum Exportieren einer Datei gestartet wird, benennen Sie das Dialogfeld in Export File um.

### <a name="open-file"></a>Datei öffnen

-   Verwenden Sie für den anfänglichen Standardordner einen spezialisierten Ordner (Bilder, Musik, Videos) nach Bedarf, und verwenden Sie andernfalls Dokumente.
-   Verwenden Sie für nachfolgende Standardordner den letzten Ordner, der vom Benutzer mithilfe des Programms geöffnet wurde.
-   Wenn Sie Fotodateien öffnen, unterdrücken Sie standardmäßig die Dateinamen. Fotos werden normalerweise durch Ihre Miniaturansichten identifiziert, und ihre Namen sind in der Regel nicht sinnvoll.

### <a name="save-file"></a>Datei speichern

-   Verwenden Sie für den anfänglichen Standardordner (wenn eine neue Datei zum ersten Mal gespeichert wird) den spezialisierten Ordner (Bilder, Musik, Videos) nach Bedarf, und verwenden Sie andernfalls Dokumente.
-   Verwenden Sie für temporäre Dateien den temporären Ordner des aktuellen Benutzers. Wählen Sie einfache, aber eindeutige Dateinamen aus. Beispiel: Verwenden Sie File0001. tmp anstelle von ~ DF1A92. tmp.
    -   **Entwickler:** Sie können den temporären Ordner des aktuellen Benutzers mithilfe der GetTempPath-API-Funktion erhalten.
-   Verwenden Sie für den anfänglichen Standard Dateinamen einen eindeutigen Standardnamen basierend auf:
    -   Der Inhalt der Datei, sofern bekannt. Beispiel: die ersten Wörter in einem Dokument.
    -   Ein Muster, das vom Benutzer ausgewählt wird. Beispiel: Wenn die vorherige Datei "Hawaii 1.jpg" genannt wurde, wählen Sie "Hawaii 2.jpg" als nächste Datei aus.
    -   Ein generisches Muster, das auf dem Dateityp basiert. Beispiel: "Photo1.jpg".
-   Verwenden Sie für nachfolgende Standardwerte (wenn die Datei bereits vorhanden ist) den aktuellen Ordner und Namen der Datei.
-   Behalten Sie beim Speichern einer Datei das Erstellungsdatum bei. Wenn das Programmdateien durch Erstellen einer temporären Datei speichert, löscht das Original und benennt die temporäre Datei in den ursprünglichen Dateinamen um. Achten Sie darauf, das Erstellungsdatum aus der ursprünglichen Datei zu kopieren.
-   Verwenden Sie Datei speichern, wenn der Benutzer den Befehl Speichern auswählt, ohne einen Dateinamen anzugeben.

### <a name="file-types-lists"></a>Liste der Dateitypen

**Hinweis:** Dateitypen Listen werden von "Datei öffnen" und "Datei speichern" verwendet, um die Typen der angezeigten Dateien und die standardmäßige Dateierweiterung zu bestimmen.

-   Wenn die Liste der Dateitypen kurz (höchstens fünf) ist, ordnen Sie die Liste nach Wahrscheinlichkeit der Verwendung zu. Wenn die Liste lang (sechs oder mehr) ist, verwenden Sie eine alphabetische Reihenfolge, damit die Typen leicht zu finden sind.
-   Schließen Sie für Save File alle Variationen der unterstützten Dateierweiterungen ein, auch wenn dies nicht üblich ist, und fügen Sie zuerst die häufigste Erweiterung ein. Die Datei Behandlungs Logik prüft diese Liste, um festzustellen, ob der Benutzer eine unterstützte Dateierweiterung angegeben hat. Beispiel: Wenn eine Liste der JPEG-Dateitypen nur jpg-und JPEG-Dateien enthält, wird die Datei Test. jpe möglicherweise als test.jpe.jpg gespeichert.
-   Beim Speichern von Dateien ist der anfängliche Standard Dateityp der wahrscheinlichste, der vom Ziel Benutzer ausgewählt wird. Der nachfolgende Standardwert ist der aktuelle Typ der Datei.
-   Für geöffnete Dateien ist der anfängliche Standard Dateityp der wahrscheinlichste, der vom Ziel Benutzer ausgewählt wird. Der nachfolgende Standardwert sollte der letzte verwendete Dateityp sein.
-   Fügen Sie für geöffnete Datei den Eintrag "alle Dateien" als erstes Element ein, wenn Benutzer einen beliebigen Dateityp öffnen können oder alle Dateien in einem Ordner gleichzeitig angezeigt werden müssen. Sie sollten weitere Meta-Filter bereitstellen, z. b. "alle Bilder", "alle Musik" und "alle Videos". Platzieren Sie diese unmittelbar nach "alle Dateien".
-   Verwenden Sie das Format "Dateityp Name ( \* . EXT1;) \* . ext2). " Der Dateityp Name muss der registrierte Dateityp Name sein, den Sie im System Steuerungselement der Ordneroptionen anzeigen können. Beispiel: "HTML-Dokument ( \* . htm; \* . HTML). "
    -   **Ausnahme:** Entfernen Sie für MetaFilter die Liste der Dateierweiterungen, um die Übersichtlichkeit auszuschließen. Beispiele: "alle Dateien", "alle Bilder", "alle Musik" und "alle Videos".
-   Verwenden Sie die Groß-/Kleinschreibung im [Satz Stil](glossary.md) für die Dateityp Namen und für die Dateityp Erweiterungen Kleinbuchstaben.

### <a name="open-folder"></a>Ordner öffnen

-   **Verwenden Sie für neue Programme das Dialogfeld Dateien öffnen im Modus "Auswahl Ordner".** Hierfür ist Windows Vista oder höher erforderlich. verwenden Sie daher das Dialogfeld "Ordner öffnen" für Programme, die in früheren Versionen von Windows ausgeführt werden.
    -   **Entwickler:** Sie können das Dialogfeld Dateien öffnen im Modus "Pick Folders" (Ordner auswählen) verwenden, indem Sie das Fos \_ pickfolders-Flag verwenden.

### <a name="font"></a>Schriftart

-   Wenn erforderlich, können Sie die Schriftart Liste filtern, um nur die Schriftarten anzuzeigen, die für das Programm verfügbar sind.

### <a name="persistence"></a>Persistenz

-   Beachten Sie, dass die folgenden Werte dauerhaft als nachfolgende Standardwerte verwendet werden:
    -   Eingabewerte (Beispiele: Standardordner, Standard Dateinamen).
    -   Ausgewählte Optionen (Beispiele: ausgewählter Drucker, Druckoptionen).
    -   Sichten (Beispiele: Anzeigen von Bildern in der Miniaturansicht, Anzeigen von Bildern ohne Dateinamen, Sortieren nach Datum, Spaltenbreite).
    -   Präsentation (Beispiele: Fenstergröße, Speicherort und Inhalt).

**Ausnahme:** Legen Sie diese Werte für gängige Dialogfelder nicht dauerhaft fest, wenn ihre Verwendung so ist, dass es sehr wahrscheinlich ist, dass Benutzer ganz wahrscheinlich vollständig anfangen möchten.

-   Beachten Sie beim Bestimmen der Standardwerte, welche Ziel Benutzer höchstwahrscheinlich basierend auf den wichtigen Szenarien benötigen. Beachten Sie auch, dass Szenarien innerhalb einer Programm Instanz über mehrere Instanzen hinweg (sowohl aufeinander folgende oder gleichzeitige) als auch über mehrere Dokumente hinweg in Erwägung gezogen werden. Nehmen Sie keine Werte in Situationen vor, in denen Sie wahrscheinlich nicht hilfreich sind.
    -   **Beispiel:** Bei einer typischen Dokument basierten Anwendung ist es hilfreich, persistente geöffnete Dateien zu verwenden und Datei Einstellungen innerhalb einer Programm Instanz und über aufeinander folgende Instanzen zu speichern. gleichzeitige Instanzen bleiben jedoch unabhängig voneinander. Auf diese Weise können Benutzer effizient mit mehreren Dokumenten gleichzeitig arbeiten.
-   Sorgen Sie dafür, dass die Einstellungen für Programm bezogen und pro Benutzer persistent gespeichert werden.

 

