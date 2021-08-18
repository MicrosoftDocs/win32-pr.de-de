---
title: Informationen zur Zwischenablage
description: In diesem Abschnitt wird die Zwischenablage erläutert.
ms.assetid: 14c91730-a668-495b-9ec6-b835234821a5
keywords:
- Zwischenablage, Informationen
- Zwischenablage, Formate
- Zwischenablage,Befehle
- Zwischenablage,Fenster
- Zwischenablage, Sequenznummern
- Zwischenablage,Viewer
- Zwischenablage, Viewerfenster
- Zwischenablage, Anzeigeformate
- Zwischenablage,Anzeigeformate für Besitzer
- Anzeigen von Zwischenablageformaten
- Anzeigeformate für Die Zwischenablage des Besitzers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86a3ddc96cbc1d440fda5e6484f1bc72a53b4b36b709c7ad80c77e203dadcef1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128632"
---
# <a name="about-the-clipboard"></a>Informationen zur Zwischenablage

Die *Zwischenablage* ist ein Satz von Funktionen und Meldungen, mit denen Anwendungen Daten übertragen können. Da alle Anwendungen Zugriff auf die Zwischenablage haben, können Daten problemlos zwischen Anwendungen oder innerhalb einer Anwendung übertragen werden.

Die Zwischenablage ist benutzergesteuert. Ein Fenster sollte Daten nur als Reaktion auf einen Befehl des Benutzers in die oder aus der Zwischenablage übertragen. Ein Fenster darf die Zwischenablage nicht verwenden, um Daten ohne das Wissen des Benutzers zu übertragen.

Ein Speicherobjekt in der Zwischenablage kann in einem beliebigen Datenformat vorliegen, das als Zwischenablageformat bezeichnet wird. Jedes Format wird durch einen ganzzahligen Wert ohne Vorzeichen identifiziert. Bei standardmäßigen (vordefinierten) Zwischenablageformaten ist dieser Wert eine Konstante, die in Winuser.h definiert ist. bei registrierten Zwischenablageformaten ist dies der Rückgabewert der [**RegisterClipboardFormat-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata)

Mit Ausnahme der Registrierung von Zwischenablageformaten führen einzelne Fenster die meisten Zwischenablagevorgänge aus. In der Regel überträgt eine Fensterprozedur Informationen in die oder aus der Zwischenablage als Reaktion auf die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)

In diesem Abschnitt wird Folgendes erläutert:

-   [Befehle der Zwischenablage](#clipboard-commands)
-   [Sequenznummer der Zwischenablage](#clipboard-sequence-number)
-   [Zwischenablage-Viewer](#clipboard-viewers)
    -   [Viewer-Windows](#clipboard-viewer-windows)
    -   [Anzeigeformate](#display-formats)
    -   [Anzeigeformat des Besitzers](#owner-display-format)
-   [Zugehörige Themen](#related-topics)

## <a name="clipboard-commands"></a>Befehle der Zwischenablage

Ein Benutzer führt in der Regel Zwischenablagevorgänge durch, indem er Befehle aus dem Menü Bearbeiten **einer Anwendung auswählt.** Im Folgenden finden Sie eine kurze Beschreibung der Standardbefehle für die Zwischenablage.



|  Befehl        |  Beschreibung                                                                                                                                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ausschneiden**    | Platziert eine Kopie der aktuellen Auswahl in der Zwischenablage und löscht die Auswahl aus dem Dokument. Der vorherige Inhalt der Zwischenablage wird zerstört.                                                          |
| **Kopieren**   | Platziert eine Kopie der aktuellen Auswahl in der Zwischenablage. Das Dokument bleibt unverändert. Der vorherige Inhalt der Zwischenablage wird zerstört.                                                                      |
| **Einfügen**  | Ersetzt die aktuelle Auswahl durch den Inhalt der Zwischenablage. Der Inhalt der Zwischenablage wird nicht geändert.                                                                                                    |
| **Löschen** | Löscht die aktuelle Auswahl aus dem Dokument. Der Inhalt der Zwischenablage wird nicht geändert. Dieser Befehl umfasst nicht die Zwischenablage, sollte aber mit den Zwischenablagebefehlen im Menü **Bearbeiten angezeigt** werden. |



 

## <a name="clipboard-sequence-number"></a>Sequenznummer der Zwischenablage

Der Zwischenablage für jede Fensterstation ist eine Sequenznummer der Zwischenablage zugeordnet. Diese Zahl wird erhöht, wenn sich der Inhalt der Zwischenablage ändert. Um die Sequenznummer der Zwischenablage zu erhalten, rufen Sie die [**GetClipboardSequenceNumber-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) auf.

## <a name="clipboard-viewers"></a>Zwischenablage-Viewer

Ein Zwischenablage-Viewer ist ein Fenster, in dem der aktuelle Inhalt der Zwischenablage angezeigt wird. Das Zwischenablage-Viewer-Fenster ist eine Benutzerfreundlichkeit und wirkt sich nicht auf die Datentransaktionsfunktionen der Zwischenablage aus.

In der Regel können in einem Zwischenablage-Viewerfenster mindestens die drei gängigsten Formate angezeigt werden: **CF \_ TEXT**, **CF \_ BITMAP** und **CF \_ METAFILEPICT**. Wenn ein Fenster keine Daten in einem dieser drei Formate verfügbar macht, sollte es Daten in einem Anzeigeformat bereitstellen oder das Format für die Besitzeranzeige verwenden.

Eine *Zwischenablage-Viewer-Kette* ist die Verknüpfung von zwei oder mehr Entitäten, sodass sie für den Vorgang von einander abhängig sind. Diese Abhängigkeit (Kette) ermöglicht es allen ausgeführten Anwendungen des Zwischenablage-Viewers, die an die aktuelle Zwischenablage gesendeten Nachrichten zu empfangen.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Viewer-Windows](#clipboard-viewer-windows)
-   [Anzeigeformate](#display-formats)
-   [Anzeigeformat des Besitzers](#owner-display-format)

### <a name="clipboard-viewer-windows"></a>Viewer-Windows

Ein Fenster fügt sich der Viewer-Kette der Zwischenablage durch Aufrufen der [**SetClipboardViewer-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) hinzu. Der Rückgabewert ist das Handle für das nächste Fenster in der Kette. Um das Handle für das erste Fenster in der Kette abzurufen, rufen Sie die [**GetClipboardViewer-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getclipboardviewer) auf.

Jedes Zwischenablageanzeigefenster muss das nächste Fenster in der Zwischenablageanzeigekette nachverfolgen. Wenn sich der Inhalt der Zwischenablage ändert, sendet das System eine [**WM \_ DRAWCLIPBOARD-Nachricht**](wm-drawclipboard.md) an das erste Fenster in der Kette. Nach dem Aktualisieren der Anzeige muss jedes Zwischenablageanzeigefenster diese Meldung an das nächste Fenster in der Kette übergeben.

Vor dem Schließen muss ein Zwischenablage-Viewer-Fenster sich selbst aus der Zwischenablage-Viewerkette entfernen, indem die [**ChangeClipboardChain-Funktion aufruft.**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) Das System sendet dann eine [**WM \_ CHANGECBCHAIN-Nachricht**](wm-changecbchain.md) an das erste Fenster in der Kette.

Weitere Informationen zum Verarbeiten der [**WM \_ DRAWCLIPBOARD-**](wm-drawclipboard.md) und [**WM \_ CHANGECBCHAIN-Nachrichten**](wm-changecbchain.md) finden Sie unter [Creating a Clipboard Viewer Window](using-the-clipboard.md).

### <a name="display-formats"></a>Anzeigeformate

Ein Anzeigeformat ist ein Zwischenablageformat, das zum Anzeigen von Informationen in einem Zwischenablage-Viewer-Fenster verwendet wird. Ein Besitzer der Zwischenablage, der ein privates oder registriertes Zwischenablageformat und keines der gängigsten Standardformate verwendet, muss Daten in einem Anzeigeformat für die Anzeige in einem Zwischenablage-Viewerfenster bereitstellen. Die Anzeigeformate sind nur für die Anzeige vorgesehen und dürfen nicht in ein Dokument einfingen.

Die vier Anzeigeformate sind: **CF \_ DSPBITMAP**, **CF \_ DSPMETAFILEPICT**, **CF \_ DSPTEXT** und **CF \_ DSPENHMETAFILE**. Diese Anzeigeformate werden auf die gleiche Weise gerendert wie die Standardformate: **CF \_ BITMAP**, **CF \_ TEXT**, **CF \_ METAFILEPICT** und **CF \_ ENHMETAFILE**.

### <a name="owner-display-format"></a>Anzeigeformat des Besitzers

Für einen Besitzer der Zwischenablage, der keines der gängigen Standardformate für die Zwischenablage verwendet, besteht eine Alternative zum Bereitstellen eines Anzeigeformats in der Verwendung des Zwischenablageformats für die Besitzeranzeige **(CF \_ OWNERDISPLAY).**

Mithilfe des Besitzeranzeigeformats kann ein Besitzer der Zwischenablage den Mehraufwand für das Rendern von Daten in einem zusätzlichen Format vermeiden, indem er die direkte Kontrolle über das Malen des Viewerfensters der Zwischenablage übernimmt. Das Zwischenablage-Viewer-Fenster sendet Meldungen an den Besitzer der Zwischenablage, wenn ein Teil des Fensters neu gepaint werden muss oder wenn das Fenster gescrollt oder seine Größe geändert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Standardformate für die Zwischenablage](standard-clipboard-formats.md)
</dt> </dl>

 

 