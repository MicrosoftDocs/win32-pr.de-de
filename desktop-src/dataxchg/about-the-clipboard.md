---
title: Informationen zur Zwischenablage
description: In diesem Abschnitt wird die Zwischenablage erläutert.
ms.assetid: 14c91730-a668-495b-9ec6-b835234821a5
keywords:
- Zwischenablage, Info
- Zwischenablage, Formate
- Zwischenablage, Befehle
- Zwischenablage, Fenster
- Zwischenablage, Sequenznummern
- Zwischenablage, Viewer
- Zwischenablage, Viewer-Fenster
- Zwischenablage, Anzeige Formate
- Zwischenablage, Anzeige Formate von Besitzern
- Zwischenablage Formate anzeigen
- Besitzer Anzeige von Zwischenablage Formaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94757a95fb8c40152a0018d04cef64e8efae624
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316101"
---
# <a name="about-the-clipboard"></a>Informationen zur Zwischenablage

Die *Zwischenablage* besteht aus einem Satz von Funktionen und Nachrichten, mit denen Anwendungen Daten übertragen können. Da alle Anwendungen auf die Zwischenablage zugreifen können, können Daten problemlos zwischen Anwendungen oder innerhalb einer Anwendung übertragen werden.

Die Zwischenablage ist Benutzer gesteuert. Ein Fenster sollte Daten nur als Reaktion auf einen Befehl des Benutzers in die oder aus der Zwischenablage übertragen. Ein Fenster darf die Zwischenablage nicht verwenden, um Daten ohne das Wissen des Benutzers zu übertragen.

Ein Speicher Objekt in der Zwischenablage kann ein beliebiges Datenformat aufweisen, das als Zwischenablage Format bezeichnet wird. Jedes Format wird durch einen ganzzahligen Wert ohne Vorzeichen identifiziert. Bei standardmäßigen (vordefinierten) Zwischenablage Formaten ist dieser Wert eine Konstante, die in winuser. h definiert ist. bei registrierten Zwischenablage Formaten ist dies der Rückgabewert der [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) -Funktion.

Mit Ausnahme der Registrierung von Zwischenablage Formaten führen einzelne Fenster die meisten Zwischenablage Vorgänge aus. Normalerweise überträgt eine Fenster Prozedur Informationen als Antwort auf die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht in die oder aus der Zwischenablage.

In diesem Abschnitt wird Folgendes erläutert:

-   [Zwischenablage Befehle](#clipboard-commands)
-   [Sequenznummer der Zwischenablage](#clipboard-sequence-number)
-   [Zwischenablage-Viewer](#clipboard-viewers)
    -   [Fenster der Zwischenablage Anzeige](#clipboard-viewer-windows)
    -   [Anzeige Formate](#display-formats)
    -   [Anzeige Format des Besitzers](#owner-display-format)
-   [Zugehörige Themen](#related-topics)

## <a name="clipboard-commands"></a>Zwischenablage Befehle

Ein Benutzer führt normalerweise Zwischenablage Vorgänge durch Auswählen von Befehlen im Menü **Bearbeiten** der Anwendung aus. Im folgenden finden Sie eine kurze Beschreibung der Standard Befehle für die Zwischenablage.



|            |                                                                                                                                                                                                                   |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ausschneiden**    | Platziert eine Kopie der aktuellen Auswahl in der Zwischenablage und löscht die Auswahl aus dem Dokument. Der vorherige Inhalt der Zwischenablage wird zerstört.                                                          |
| **Kopieren**   | Platziert eine Kopie der aktuellen Auswahl in der Zwischenablage. Das Dokument bleibt unverändert. Der vorherige Inhalt der Zwischenablage wird zerstört.                                                                      |
| **Einfügen**  | Ersetzt die aktuelle Auswahl durch den Inhalt der Zwischenablage. Der Inhalt der Zwischenablage wird nicht geändert.                                                                                                    |
| **Löschen** | Löscht die aktuelle Auswahl aus dem Dokument. Der Inhalt der Zwischenablage wird nicht geändert. Dieser Befehl umfasst nicht die Zwischenablage, sollte jedoch im Menü **Bearbeiten** mit den Befehlen der Zwischenablage angezeigt werden. |



 

## <a name="clipboard-sequence-number"></a>Sequenznummer der Zwischenablage

Die Zwischenablage für jede Fenster Station verfügt über eine zugehörige Zwischenablage Sequenznummer. Diese Zahl wird erhöht, wenn der Inhalt der Zwischenablage geändert wird. Um die Sequenznummer der Zwischenablage abzurufen, rufen Sie die [**getclipboardsequencenenumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) -Funktion auf.

## <a name="clipboard-viewers"></a>Zwischenablage-Viewer

Ein Zwischenablage-Viewer ist ein Fenster, in dem der aktuelle Inhalt der Zwischenablage angezeigt wird. Das Fenster der Zwischenablage Anzeige ist für den Benutzer benutzerfreundlicher und wirkt sich nicht auf die Daten Transaktionsfunktionen der Zwischenablage aus.

In der Regel kann ein Fenster der Zwischenablage Anzeige mindestens die drei gängigsten Formate anzeigen: **CF \_ Text**, **CF \_ Bitmap** und **CF \_ MetafilePict**. Wenn ein Fenster keine Daten in einem dieser drei Formate verfügbar macht, sollte es Daten in einem Anzeige Format bereitstellen oder das Anzeige Format des Besitzers verwenden.

Eine *Zwischenablage-Viewer-Kette* besteht aus der Verknüpfung von zwei oder mehr Entitäten, sodass Sie für den Vorgang voneinander abhängig sind. Mit dieser interabhängigkeit (Kette) können alle ausgelaufenden Zwischenablage-Viewer-Anwendungen die an die aktuelle Zwischenablage gesendeten Nachrichten empfangen.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Fenster der Zwischenablage Anzeige](#clipboard-viewer-windows)
-   [Anzeige Formate](#display-formats)
-   [Anzeige Format des Besitzers](#owner-display-format)

### <a name="clipboard-viewer-windows"></a>Fenster der Zwischenablage Anzeige

Durch Aufrufen der [**setclipboardviewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) -Funktion wird ein Fenster zur Kette der Zwischenablage-Viewer hinzugefügt. Der Rückgabewert ist das Handle für das nächste Fenster in der Kette. Um das Handle zum ersten Fenster in der Kette abzurufen, rufen Sie die [**getclipboardviewer**](/windows/desktop/api/Winuser/nf-winuser-getclipboardviewer) -Funktion auf.

Jedes Fenster der Zwischenablage Anzeige muss das nächste Fenster in der Zwischenablage-Viewer-Kette nachverfolgen. Wenn sich der Inhalt der Zwischenablage ändert, sendet das System eine [**WM- \_ drawclipboard**](wm-drawclipboard.md) -Nachricht an das erste Fenster in der Kette. Nach dem Aktualisieren der Anzeige muss jedes Fenster der Zwischenablage Anzeige an das nächste Fenster in der Kette übergeben werden.

Vor dem schließen muss sich das Fenster der Zwischenablage Anzeige durch Aufrufen der [**changeclipboardchain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) -Funktion aus der Zwischenablage-Viewer-Kette entfernen. Das System sendet dann eine [**WM- \_ CHANGECBCHAIN**](wm-changecbchain.md) -Nachricht an das erste Fenster in der Kette.

Weitere Informationen zum Verarbeiten der Nachrichten " [**WM \_ drawclipboard**](wm-drawclipboard.md) " und " [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) " finden Sie unter [Erstellen eines Zwischenablage-Viewer-Fensters](using-the-clipboard.md).

### <a name="display-formats"></a>Anzeige Formate

Ein Anzeige Format ist ein Zwischenablage Format, mit dem Informationen in einem Fenster der Zwischenablage Anzeige angezeigt werden. Ein Besitzer der Zwischenablage, der ein privates oder registriertes Zwischenablage Format und keines der gängigsten Standardformate verwendet, muss Daten in einem Anzeige Format zur Anzeige in einem Zwischenablage-Viewer-Fenster bereitstellen. Die Anzeige Formate dienen nur zur Anzeige und dürfen nicht in ein Dokument eingefügt werden.

Die vier Anzeige Formate sind: **CF \_ dspbitmap**, **CF \_ dspmetafilepict**, **CF \_ dsptext** und **CF \_ dspenhmetafile**. Diese Anzeige Formate werden auf die gleiche Weise gerendert wie die Standardformate: **CF \_ Bitmap**, **CF \_ Text**, **CF \_ MetafilePict** und **CF \_ enhmetafile**.

### <a name="owner-display-format"></a>Anzeige Format des Besitzers

Für einen Besitzer der Zwischenablage, der keines der allgemeinen Standard-Zwischenablage Formate verwendet, besteht eine Alternative zur Bereitstellung eines Anzeige Formats darin, das Format "Besitzer Anzeige" (CF-Besitzer **\_ Anzeige**) zu verwenden.

Mit dem Format "Besitzer Anzeige" kann ein Besitzer der Zwischenablage den mehr Aufwand für das Rendern von Daten in einem zusätzlichen Format vermeiden, indem Sie die direkte Kontrolle über das Zeichnen des Fensters der Zwischenablage Anzeige übernimmt. Das Fenster der Zwischenablage Anzeige sendet Nachrichten an den Besitzer der Zwischenablage, wenn ein Teil des Fensters neu gezeichnet werden muss oder wenn für das Fenster ein Rollup oder eine Größenänderung durchgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Standard Formate für Zwischenablage](standard-clipboard-formats.md)
</dt> </dl>

 

 