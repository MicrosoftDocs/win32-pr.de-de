---
title: Stoclien-Vorgänge
description: Das stoclien-Beispiel veranschaulicht, wie der Client strukturierte Speicher verwendet. Im folgenden werden die stoclien-Vorgänge zusammengefasst.
ms.assetid: 55498665-520b-4a83-a3d1-22d3ed15863e
keywords:
- Stoclien-Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1068fcf1e377456211e08020f41279be9b5e3b0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729065"
---
# <a name="stoclien-operations"></a>Stoclien-Vorgänge

Das [stoclien](structured-storage-client-sample--stoclien-.md) -Beispiel veranschaulicht, wie der Client strukturierte Speicher verwendet. Im folgenden werden die stoclien-Vorgänge zusammengefasst.

Der Client Bereich des Anwendungsfensters [stoclien](structured-storage-client-sample--stoclien-.md) wird zur visuellen Darstellung der mit einem Maus-oder Tablet-Gerät erstellten Freiformzeichnung verwendet. Wenn Sie mit der Maus zeichnen möchten, halten Sie die linke Maustaste gedrückt, während Sie die Maus bewegen. Wenn Sie die linke Maustaste loslassen, wird die Zeichnung einer Zeile beendet.

Im folgenden finden Sie eine Zusammenfassung der Vorgänge aus der Sicht Stoclien.exe als com-Client des Stoserve.dll COM-Servers:

<dl> <dt>

<span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>Datei/öffnen
</dt> <dd>

Zeigt das Dialogfeld Öffnen an, in dem Sie einen Namen und Pfad für eine vorhandene zu öffnende Papier Zeichnungs Datei abrufen können. Ein Standardwert. Die Dateinamenerweiterung PAP für diese Dateien wird angenommen. Wenn an der vorhandenen Zeichnung Änderungen vorgenommen wurden, wenn dieses Menü Element ausgewählt wird, wird zunächst ein separates Dialogfeld mit der Frage angezeigt, ob die aktuelle Zeichnung in der zugehörigen Verbund Datei gespeichert werden soll.

</dd> <dt>

<span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>Datei/speichern
</dt> <dd>

Speichert die aktuelle Zeichnung in der zugeordneten Verbund Datei.

</dd> <dt>

<span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>Datei/speichern unter
</dt> <dd>

Zeigt das Dialogfeld Speichern unter an, in dem Sie einen Namen und einen Pfad für eine neue zu erstellende Papier Zeichnungs Datei abrufen können. Die aktuelle Zeichnung wird zum gespeicherten Inhalt der neuen Datei, und die neue Datei wird zur neuen zugeordneten Verbund Datei für die Zeichnung.

</dd> <dt>

<span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>Datei/Exit
</dt> <dd>

Beendet [stoclien](structured-storage-client-sample--stoclien-.md).

</dd> <dt>

<span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Zeichnen/zeichnen auf
</dt> <dd>

Schaltet das Zeichnen zwischen dem [stoclien](structured-storage-client-sample--stoclien-.md) -Client und dem copaper-Objekt auf dem Server um. Dieser Befehl sperrt das copaper-Objekt für die exklusive Verwendung durch diesen Client und verhindert, dass andere Clients auf die gleiche copaper-Instanz auf dem Server zugreifen.

</dd> <dt>

<span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Zeichnen/zeichnen aus
</dt> <dd>

Deaktiviert das Zeichnen zwischen dem [stoclien](structured-storage-client-sample--stoclien-.md) -Client und dem copaper-Objekt auf dem Server. Dieser Befehl entsperrt den copaper für die exklusive Verwendung durch diesen Client und ermöglicht anderen Clients den Zugriff auf dieselbe copaper-Instanz auf dem Server.

</dd> <dt>

<span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Zeichnen/neu zeichnen
</dt> <dd>

Zeichnet die aktuellen Zeichnungsdaten, die im copaper-Objekt auf dem Server gespeichert sind, im Client neu.

</dd> <dt>

<span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Zeichnen/löschen
</dt> <dd>

Löscht den aktuellen Zeichnungs Inhalt und löscht das Fenster Bild. Menü Auswahl: Stift/Farbe zeigt das Dialogfeld Farbe auswählen an, um eine neue Stift Farbe zum Zeichnen zu erhalten.

</dd> <dt>

<span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Stift/Mittel
</dt> <dd>

Wählt die mittlere Breite für das Zeichnen aus. Ein Häkchen in dieser Menüoption gibt an, dass "Medium" die aktuelle Stift Breite ist.

</dd> <dt>

<span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Stift/Thick
</dt> <dd>

Wählt die Dicke Breite für das Zeichnen aus. Ein Häkchen in dieser Menüoption gibt an, dass "Thick" die aktuelle Stift Breite ist.

</dd> <dt>

<span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Stift/schlank
</dt> <dd>

Wählt die schmale Breite für das Zeichnen aus. Ein Häkchen in dieser Menüoption gibt an, dass schlank die aktuelle Stift Breite ist.

</dd> <dt>

<span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Senke/Verbindung
</dt> <dd>

Verbindet die copapersink ipapersink-Schnittstelle mit dem copaper-objekttaschen-Verbindungspunkt. Das erneute Zeichnen des aktuellen Zeichnungs Bilds in [stoclien](structured-storage-client-sample--stoclien-.md) basiert auf der Senke-Verbindung. Ein Häkchen in dieser Menüoption gibt an, dass das Neuzeichnen verbunden ist.

</dd> <dt>

<span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Senke/Verbindung trennen
</dt> <dd>

Trennt die copapersink ipapersink-Schnittstelle vom copaper-Objekt Taschenbuch-Verbindungspunkt. Das erneute Zeichnen des aktuellen Zeichnungs Bilds in [stoclien](structured-storage-client-sample--stoclien-.md) basiert auf der Senke-Verbindung. Ein Häkchen in dieser Menüoption gibt an, dass das erneute zeichnen getrennt ist.

</dd> <dt>

<span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Tutorial zu Hilfe/stoclien
</dt> <dd>

Öffnet die STOCLIEN.HTM Tutorial-Datei im Webbrowser.

</dd> <dt>

<span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Hilfe/stobedient-Tutorial
</dt> <dd>

Öffnet die STOSERVE.HTM Tutorial-Datei im Webbrowser.

</dd> <dt>

<span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Hilfe/lesen der Quelldatei
</dt> <dd>

Zeigt das Dialogfeld Öffnen an, sodass Sie eine Quelldatei aus dieser Lektion oder eine andere in Windows Notepad öffnen können.

</dd> <dt>

<span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Hilfe/Informationen zu stoclien
</dt> <dd>

Zeigt das Dialogfeld Info für diese Anwendung an.

</dd> </dl>

Das [stoclien](structured-storage-client-sample--stoclien-.md) -Beispiel verwendet viele der Hilfsprogrammklassen und-Dienste, die von [apputil](./using-visual-studio.md)bereitgestellt werden. Weitere Informationen zu [apputil](./using-visual-studio.md)finden Sie im Quellcode der [apputil](./using-visual-studio.md) -Bibliothek im neben geordneten [apputil](./using-visual-studio.md) -Verzeichnis und in apputil.MD im haupttutorial-Verzeichnis. Weitere Informationen zu [apputil](./using-visual-studio.md)finden Sie unter [Erstellen von Beispielen](how-to-build-samples.md).

 

 