---
title: Allgemeine Dialogfelder
description: Die microsoft Windows-Dialogfelder bestehen aus den Dialogfeldern Datei öffnen, Datei speichern, Ordner öffnen, Suchen und Ersetzen, Drucken, Seiteneinrichtung, Schriftart und Farbe.
ms.assetid: 3f9fb0c9-bc1a-48c4-b021-99f155f8ea9e
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 9ddd0bf5af0a609c07550ec91e7482ce35270c85b81d553d4a5e262db6ed3683
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935605"
---
# <a name="common-dialogs"></a>Allgemeine Dialogfelder

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Die microsoft Windows-Dialogfelder bestehen aus den Dialogfeldern Datei öffnen, Datei speichern, Ordner öffnen, Suchen und Ersetzen, Drucken, Seiteneinrichtung, Schriftart und Farbe.

## <a name="open-file"></a>Datei öffnen

![Screenshot des geöffneten Dialogfelds ](images/win-common-dlg-image1.png)

Open File ist für die schnelle Suche nach Elementen optimiert, die mit einem Programm verwendet werden können.

## <a name="save-file"></a>Datei speichern

![Screenshot des Dialogfelds "Speichern unter" ](images/win-common-dlg-image2.png)

Datei speichern schließt die Schleife, indem eine Datei mit ihren Metadaten gespeichert wird.

## <a name="open-folder"></a>Ordner öffnen

![Screenshot des Dialogfelds "Nach Dateien/Ordnern suchen" ](images/win-common-dlg-image3.png)

Ordner öffnen ist speziell für die Auswahl von Ordnern.

## <a name="find-and-replace"></a>Suchen und ersetzen

![Screenshot der Dialogfelder "Suchen und Ersetzen" ](images/win-common-dlg-image4.png)

Mit find können Benutzer nach Textzeichenfolgen suchen, während die Replace-Version benutzern optional ermöglicht, Übereinstimmungen durch eine andere Zeichenfolge zu ersetzen.

## <a name="print"></a>Drucken

![Screenshot des Dialogfelds "Drucken" ](images/win-common-dlg-image5.png)

Mit drucken können Benutzer auswählen, was gedruckt werden soll, wie viele Kopien gedruckt werden und welche Sortierungssequenz sie zusammen mit der Möglichkeit haben, Drucker auszuwählen und zu konfigurieren.

## <a name="page-setup"></a>Seiteneinrichtung

![Screenshot des Dialogfelds "Seiteneinrichtung" ](images/win-common-dlg-image6.png)

Mithilfe der Seiteneinrichtung können Benutzer die Papiergröße, Quelle, Seitenausrichtung und Ränder auswählen.

## <a name="font"></a>Schriftart

![Screenshot des Dialogfelds "Schriftart" ](images/win-common-dlg-image7.png)

Die Schriftart zeigt die Schriftarten und Punktgrößen der verfügbaren installierten Schriftarten an.

## <a name="color"></a>Color

![Screenshot des Dialogfelds "Farben bearbeiten" ](images/win-common-dlg-image8.png)

Mit Farbe können Benutzer eine Farbe auswählen, entweder über einen vordefinierten Satz von Farben oder durch Auswählen einer "benutzerdefinierten" Farbe.

## <a name="design-concepts"></a>Entwurfskonzepte

Mithilfe der gängigen Dialoge können Sie Benutzern eine konsistente Erfahrung in verschiedenen Programmen bieten. Und durch die Verwendung der gängigen Dialoge können Sie benutzern auch ein effizientes, gängiges Erlebnis bieten.

Sie können die Benutzererfahrung mit diesen Dialogen erheblich verbessern, indem Sie die am besten geeigneten Standardwerte für:

-   Eingabewerte (Beispiele: Standardordner, Standarddateinamen).
-   Ausgewählte Optionen (Beispiele: ausgewählter Drucker, Druckoptionen).
-   Ansichten (Beispiele: Anzeigen von Bildern in der Miniaturansicht, Anzeigen von Bildern ohne Dateinamen, Sortieren nach Datum, Spaltenbreiten).
-   Präsentation (Beispiele: Fenstergröße, Position und Inhalt).

Sie müssen sowohl die anfänglichen als auch die nachfolgenden Standardwerte bestimmen. Anfängliche Standardwerte werden von Ihrem Programm und basierend auf der erwarteten Nutzung des Zielbenutzers bestimmt, während nachfolgende Standardwerte auf der tatsächlichen Nutzung basieren. Die frühere Nutzung ist der beste Indikator für die zukünftige Nutzung.

Sind die Standardwerte Ihres Programms effizient? Überwachen Sie die Anzahl der Schritte, die Benutzer ausführen müssen, um die gängigsten Aufgaben auszuführen. Wenn Benutzer die gleichen, möglicherweise unnötigen Schritte jedes Mal wiederholen müssen, wenn sie eine Aufgabe ausführen, können Ihre Standardwerte verbessert werden.

**Wenn Sie nur eins tun...**

Ermöglichen Sie Benutzern ein effizientes, leistungsfähigeres Erlebnis, indem Sie die entsprechenden anfänglichen und nachfolgenden Standardwerte auswählen.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

**Ja! Verwenden Sie die allgemeinen Dialoge, um eine konsistente Benutzererfahrung zu gewährleisten. Erstellen Sie keine eigenen.** Es ist besonders schwierig, benutzerdefinierte Benutzerdefinierte Beis zu erstellen, die ordnungsgemäß und sicher durch den Namespace navigieren. Beachten Sie, dass Sie die häufigen Dialoge bei Bedarf anpassen können.

Für Windows Vista verfügen die Open File and Save File (Datei öffnen und Datei speichern) über eine neue erweiterbare Architektur, mit der zusätzliche Funktionen einfacher verfügbar gemacht werden können. Dieser Mechanismus ist flexibel genug, um die Mindestanforderungen der großen unabhängigen Softwarehersteller (ISVs) zu erfüllen, wird jedoch nicht durch zukünftige Releases von Windows.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   Stellen Sie gegebenenfalls direktere oder [moduslose Alternativen](glossary.md) zur Verfügung. Benutzern dies erlauben:
    -   Öffnen Sie Dateien, indem Sie sie in Ihrem Programm ablegen.
    -   Speichern Sie Dateien mit ihrem aktuellen Namen und Speicherort mit dem Befehl Speichern.
    -   Suchen Sie das nächste Vorkommen einer Zeichenfolge mithilfe der F3-Taste.
    -   Drucken Sie mit dem Befehl Drucken eine Kopie eines gesamten Dokuments auf dem Standarddrucker.
    -   Ändern sie Schriftarten und Schriftartattribute mithilfe einer Symbolleiste oder eines Palettenfensters.
    -   Ändern Sie farben mithilfe einer Symbolleiste oder eines Palettenfensters.
-   Verwenden Sie die folgenden Befehle, um allgemeine Dialoge (zusammen mit ihren bevorzugten [Zugriffsschlüsseln) anzuzeigen:](glossary.md)



| Allgemeines Dialogfeld          | Befehl                                 |
|------------------------|-----------------------------------------|
| Datei öffnen<br/>         | Öffnen...<br/>                            |
| Datei speichern<br/>         | Speichern unter...<br/>                         |
| Ordner öffnen<br/>       | Ordner öffnen... oder Ordner auswählen...<br/> |
| Suchen und Ersetzen<br/>  | Finden... oder Ersetzen...<br/>              |
| Drucken<br/>             | Drucken...<br/>                           |
| Seite einrichten<br/>        | Seiteneinrichtung...<br/>                      |
| Schriftart<br/>              | Schriftart... oder Schriftart auswählen...<br/>          |
| Color<br/>             | Farbe... oder Farbe auswählen...<br/>        |



 

-   Sie können spezifischere Befehle verwenden, wenn dies angemessen ist. Beispiel: Verwenden Sie zum Exportieren einer Datei den Befehl Datei exportieren anstelle von Speichern unter.
-   Legen Sie den Titel des Dialogfelds auf den Befehl fest, mit dem er gestartet wurde. Beispiel: Wenn Datei speichern über den Befehl Datei exportieren gestartet wird, benennen Sie das Dialogfeld in Datei exportieren um.

### <a name="open-file"></a>Datei öffnen

-   Verwenden Sie für den anfänglichen Standardordner einen speziellen Ordner (Bilder, Musik, Videos), andernfalls Dokumente.
-   Verwenden Sie für nachfolgende Standardordner den letzten Ordner, den der Benutzer mithilfe des Programms geöffnet hat.
-   Unterdrücken Sie beim Öffnen von Fotodateien standardmäßig Dateinamen. Fotos werden in der Regel anhand ihrer Miniaturansichten identifiziert, und ihre Namen sind in der Regel nicht aussagekräftig.

### <a name="save-file"></a>Datei speichern

-   Verwenden Sie für den anfänglichen Standardordner (wenn eine neue Datei zum ersten Mal gespeichert wird) den speziellen Ordner (Bilder, Musik, Videos), andernfalls Dokumente.
-   Verwenden Sie für temporäre Dateien den temporären Ordner des aktuellen Benutzers. Wählen Sie einfache, aber eindeutige Dateinamen aus. Beispiel: Verwenden Sie File0001.tmp anstelle von ~DF1A92.tmp.
    -   **Entwickler:** Sie können den temporären Ordner des aktuellen Benutzers mithilfe der GetTempPath-API-Funktion abrufen.
-   Verwenden Sie für den anfänglichen Standarddateinamen einen eindeutigen Standardnamen, der auf Folgenden basiert:
    -   Der Inhalt der Datei, sofern bekannt. Beispiel: Die ersten Wörter in einem Dokument.
    -   Ein vom Benutzer ausgewähltes Muster. Beispiel: Wenn die vorherige Datei den Namen "" 1.jpg, wählen Sie als nächste Datei "2.jpg" aus.
    -   Ein generisches Muster, das auf dem Dateityp basiert. Beispiel: "Photo1.jpg".
-   Verwenden Sie für nachfolgende Standardwerte (wenn die Datei bereits vorhanden ist) den aktuellen Ordner und Namen der Datei.
-   Behalten Sie beim Speichern einer Datei das Erstellungsdatum bei. Wenn Das Programm Dateien durch Erstellen einer temporären Datei speichert, die ursprüngliche Datei löscht und die temporäre Datei in den ursprünglichen Dateinamen umbenennt, kopieren Sie das Erstellungsdatum aus der ursprünglichen Datei.
-   Verwenden Sie Datei speichern, wenn der Benutzer den Befehl Speichern auswählt, ohne einen Dateinamen anzugeben.

### <a name="file-types-lists"></a>Dateityplisten

**Hinweis:** Dateityplisten werden von Datei öffnen und Datei speichern verwendet, um die angezeigten Dateitypen und die Standarddateierweiterung zu bestimmen.

-   Wenn die Liste der Dateitypen kurz (fünf oder weniger) ist, geordnet die Liste nach der Wahrscheinlichkeit der Verwendung. Wenn die Liste lang ist (sechs oder mehr), verwenden Sie eine alphabetische Reihenfolge, damit die Typen leicht zu finden sind.
-   Schließen Sie für Datei speichern alle Varianten der unterstützten Dateierweiterungen ein, auch wenn dies ungewöhnlich ist, und legen Sie die gängigste Erweiterung an erster Stelle. Die Dateiverarbeitungslogik untersucht diese Liste, um zu ermitteln, ob der Benutzer eine unterstützte Dateierweiterung angegeben hat. Beispiel: Wenn eine JPEG-Dateitypliste nur .jpg .jpeg enthält, wird die Datei test.jpe möglicherweise als test.jpe.jpg.
-   Für Datei speichern ist der anfängliche Standarddateityp der wahrscheinlichste, der vom Zielbenutzer ausgewählt wird. Der nachfolgende Standardwert ist der aktuelle Typ der Datei.
-   Für Datei öffnen ist der anfängliche Standarddateityp der wahrscheinlichste, der vom Zielbenutzer ausgewählt wird. Der nachfolgende Standardwert sollte der letzte verwendete Dateityp sein.
-   Fügen Sie für Datei öffnen den Eintrag "Alle Dateien" als erstes Element ein, wenn Benutzer einen beliebigen Dateityp öffnen können oder alle Dateien in einem Ordner gleichzeitig sehen müssen. Erwägen Sie die Bereitstellung anderer Metafilter, z. B. "Alle Bilder", "Alle Musik" und "Alle Videos". Platzieren Sie diese unmittelbar nach "Alle Dateien".
-   Verwenden Sie das Format "Dateitypname ( \* .ext1; \* . ext2). Der Dateitypname sollte der registrierte Dateitypname sein, den Sie im Systemsteuerungselement Ordneroptionen anzeigen können. Beispiel: "HTML-Dokument ( \*.htm; \*.html).
    -   **Ausnahme:** Entfernen Sie bei Metafiltern die Dateierweiterungsliste, um unübersichtlich zu sein. Beispiele: "Alle Dateien", "Alle Bilder", "Alle Musik" und "Alle Videos".
-   Verwenden [Sie die Groß-/Kleinschreibung](glossary.md) im Satzformat für die Dateitypnamen und Kleinbuchstaben für die Dateityperweiterungen.

### <a name="open-folder"></a>Ordner öffnen

-   **Verwenden Sie für neue Programme das Dialogfeld Dateien öffnen im Modus "Ordner auswählen".** Dies erfordert Windows Vista oder höher. Verwenden Sie daher das Dialogfeld Ordner öffnen für Programme, die in früheren Versionen von Windows.
    -   **Entwickler:** Sie können das Dialogfeld Dateien öffnen im Modus "Ordner auswählen" verwenden, indem Sie das FOS \_ PICKFOLDERS-Flag verwenden.

### <a name="font"></a>Schriftart

-   Bei Bedarf können Sie die Schriftartliste filtern, um nur die Schriftarten anzuzeigen, die für Ihr Programm verfügbar sind.

### <a name="persistence"></a>Persistenz

-   Erwägen Sie, die folgenden Werte dauerhaft als nachfolgende Standardwerte zu verwenden:
    -   Eingabewerte (Beispiele: Standardordner, Standarddateinamen).
    -   Ausgewählte Optionen (Beispiele: ausgewählter Drucker, Druckoptionen).
    -   Ansichten (Beispiele: Anzeigen von Bildern in der Miniaturansicht, Anzeigen von Bildern ohne Dateinamen, Sortieren nach Datum, Spaltenbreiten).
    -   Präsentation (Beispiele: Fenstergröße, Position und Inhalt).

**Ausnahme:** Lassen Sie diese Werte nicht für gängige Dialoge erhalten, wenn ihre Verwendung so ist, dass Benutzer viel wahrscheinlicher von vorn beginnen möchten.

-   Berücksichtigen Sie bei der Festlegung von Standardwerten basierend auf den wichtigen Szenarien, welche Zielbenutzer am wahrscheinlichsten möchten. Berücksichtigen Sie außerdem Szenarien innerhalb einer Programminstanz, über mehrere Instanzen (aufeinanderfolgende oder gleichzeitige Instanzen) und über mehrere Dokumente hinweg. Sorgen Sie nicht dafür, dass Werte in Situationen beibehalten werden, die wahrscheinlich nicht hilfreich sind.
    -   **Beispiel:** Für eine typische dokumentbasierte Anwendung ist es hilfreich, persistente Einstellungen für Datei öffnen und Datei speichern innerhalb einer Programminstanz und über aufeinanderfolgende Instanzen hinweg zu verwenden, gleichzeitige Instanzen jedoch unabhängig zu halten. Auf diese Weise können Benutzer effizient mit mehreren Dokumenten gleichzeitig arbeiten.
-   Sorgen Sie dafür, dass die Einstellungen pro Programm und pro Benutzer beibehalten werden.

 

