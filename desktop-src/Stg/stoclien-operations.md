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
# <a name="stoclien-operations"></a><span data-ttu-id="9ba4c-105">Stoclien-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="9ba4c-105">StoClien Operations</span></span>

<span data-ttu-id="9ba4c-106">Das [stoclien](structured-storage-client-sample--stoclien-.md) -Beispiel veranschaulicht, wie der Client strukturierte Speicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-106">The [StoClien](structured-storage-client-sample--stoclien-.md) sample demonstrates how the client uses structured storage.</span></span> <span data-ttu-id="9ba4c-107">Im folgenden werden die stoclien-Vorgänge zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-107">The following summarizes the StoClien operations.</span></span>

<span data-ttu-id="9ba4c-108">Der Client Bereich des Anwendungsfensters [stoclien](structured-storage-client-sample--stoclien-.md) wird zur visuellen Darstellung der mit einem Maus-oder Tablet-Gerät erstellten Freiformzeichnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-108">The [StoClien](structured-storage-client-sample--stoclien-.md) application window client area is used for visual display of freeform drawing created with a mouse or tablet device.</span></span> <span data-ttu-id="9ba4c-109">Wenn Sie mit der Maus zeichnen möchten, halten Sie die linke Maustaste gedrückt, während Sie die Maus bewegen.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-109">To draw with the mouse, press and hold the left mouse button while moving the mouse.</span></span> <span data-ttu-id="9ba4c-110">Wenn Sie die linke Maustaste loslassen, wird die Zeichnung einer Zeile beendet.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-110">Releasing the left mouse button ends the drawing of a line.</span></span>

<span data-ttu-id="9ba4c-111">Im folgenden finden Sie eine Zusammenfassung der Vorgänge aus der Sicht Stoclien.exe als com-Client des Stoserve.dll COM-Servers:</span><span class="sxs-lookup"><span data-stu-id="9ba4c-111">Here is a summary of operations from the standpoint of Stoclien.exe as a COM client of the Stoserve.dll COM server:</span></span>

<dl> <dt>

<span data-ttu-id="9ba4c-112"><span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>Datei/öffnen</span><span class="sxs-lookup"><span data-stu-id="9ba4c-112"><span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>File/Open</span></span>
</dt> <dd>

<span data-ttu-id="9ba4c-113">Zeigt das Dialogfeld Öffnen an, in dem Sie einen Namen und Pfad für eine vorhandene zu öffnende Papier Zeichnungs Datei abrufen können.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-113">Shows the Open dialog box to obtain a name and path for an existing paper drawing file to open.</span></span> <span data-ttu-id="9ba4c-114">Ein Standardwert. Die Dateinamenerweiterung PAP für diese Dateien wird angenommen.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-114">A default .PAP file name extension for these files is assumed.</span></span> <span data-ttu-id="9ba4c-115">Wenn an der vorhandenen Zeichnung Änderungen vorgenommen wurden, wenn dieses Menü Element ausgewählt wird, wird zunächst ein separates Dialogfeld mit der Frage angezeigt, ob die aktuelle Zeichnung in der zugehörigen Verbund Datei gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-115">If changes were made to the existing drawing when this menu item is chosen, a separate dialog will first be shown asking the user if the current drawing should be saved into its associated compound file.</span></span>

</dd> <dt>

<span data-ttu-id="9ba4c-116"><span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>Datei/speichern</span><span class="sxs-lookup"><span data-stu-id="9ba4c-116"><span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>File/Save</span></span>
</dt> <dd>

<span data-ttu-id="9ba4c-117">Speichert die aktuelle Zeichnung in der zugeordneten Verbund Datei.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-117">Saves the current drawing into its associated compound file.</span></span>

</dd> <dt>

<span data-ttu-id="9ba4c-118"><span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>Datei/speichern unter</span><span class="sxs-lookup"><span data-stu-id="9ba4c-118"><span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>File/Save As</span></span>
</dt> <dd>

<span data-ttu-id="9ba4c-119">Zeigt das Dialogfeld Speichern unter an, in dem Sie einen Namen und einen Pfad für eine neue zu erstellende Papier Zeichnungs Datei abrufen können.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-119">Shows the Save As dialog box to obtain a name and path for a new paper drawing file to create.</span></span> <span data-ttu-id="9ba4c-120">Die aktuelle Zeichnung wird zum gespeicherten Inhalt der neuen Datei, und die neue Datei wird zur neuen zugeordneten Verbund Datei für die Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-120">The current drawing becomes the saved content of the new file, and the new file becomes the new associated compound file for the drawing.</span></span>

</dd> <dt>

<span data-ttu-id="9ba4c-121"><span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>Datei/Exit</span><span class="sxs-lookup"><span data-stu-id="9ba4c-121"><span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>File/Exit</span></span>
</dt> <dd>

<span data-ttu-id="9ba4c-122">Beendet [stoclien](structured-storage-client-sample--stoclien-.md).</span><span class="sxs-lookup"><span data-stu-id="9ba4c-122">Exits [StoClien](structured-storage-client-sample--stoclien-.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ba4c-123"><span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Zeichnen/zeichnen auf</span><span class="sxs-lookup"><span data-stu-id="9ba4c-123"><span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Draw/Drawing On</span></span>
</dt> <dd>

<span data-ttu-id="9ba4c-124">Schaltet das Zeichnen zwischen dem [stoclien](structured-storage-client-sample--stoclien-.md) -Client und dem copaper-Objekt auf dem Server um.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-124">Turns on drawing between the [StoClien](structured-storage-client-sample--stoclien-.md) client and the COPaper object in the server.</span></span> <span data-ttu-id="9ba4c-125">Dieser Befehl sperrt das copaper-Objekt für die exklusive Verwendung durch diesen Client und verhindert, dass andere Clients auf die gleiche copaper-Instanz auf dem Server zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-125">This command locks the COPaper object for exclusive use by this client and prevents other clients from accessing the same COPaper instance in the server.</span></span>

</dd> <dt>

<span data-ttu-id="9ba4c-126"><span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Zeichnen/zeichnen aus</span><span class="sxs-lookup"><span data-stu-id="9ba4c-126"><span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Draw/Drawing Off</span></span>
</dt> <dd>

<span data-ttu-id="9ba4c-127">Deaktiviert das Zeichnen zwischen dem [stoclien](structured-storage-client-sample--stoclien-.md) -Client und dem copaper-Objekt auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-127">Turns off drawing between the [StoClien](structured-storage-client-sample--stoclien-.md) client and the COPaper object in the server.</span></span> <span data-ttu-id="9ba4c-128">Dieser Befehl entsperrt den copaper für die exklusive Verwendung durch diesen Client und ermöglicht anderen Clients den Zugriff auf dieselbe copaper-Instanz auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-128">This command unlocks the COPaper for exclusive use by this client and allows other clients to access the same COPaper instance in the server.</span></span>

</dd> <dt>

<span data-ttu-id="9ba4c-129"><span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Zeichnen/neu zeichnen</span><span class="sxs-lookup"><span data-stu-id="9ba4c-129"><span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Draw/Redraw</span></span>
</dt> <dd>

<span data-ttu-id="9ba4c-130">Zeichnet die aktuellen Zeichnungsdaten, die im copaper-Objekt auf dem Server gespeichert sind, im Client neu.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-130">Redraws in the client the current drawing data held in the COPaper object in the server.</span></span>

</dd> <dt>

<span data-ttu-id="9ba4c-131"><span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Zeichnen/löschen</span><span class="sxs-lookup"><span data-stu-id="9ba4c-131"><span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Draw/Erase</span></span>
</dt> <dd>

<span data-ttu-id="9ba4c-132">Löscht den aktuellen Zeichnungs Inhalt und löscht das Fenster Bild.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-132">Erases the current drawing content and clears the window image.</span></span> <span data-ttu-id="9ba4c-133">Menü Auswahl: Stift/Farbe zeigt das Dialogfeld Farbe auswählen an, um eine neue Stift Farbe zum Zeichnen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-133">Menu Selection: Pen/Color Shows the Choose Color dialog box to obtain a new pen color for drawing.</span></span>

</dd> <dt>

<span data-ttu-id="9ba4c-134"><span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Stift/Mittel</span><span class="sxs-lookup"><span data-stu-id="9ba4c-134"><span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Pen/Medium</span></span>
</dt> <dd>

<span data-ttu-id="9ba4c-135">Wählt die mittlere Breite für das Zeichnen aus.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-135">Chooses the medium width for drawing.</span></span> <span data-ttu-id="9ba4c-136">Ein Häkchen in dieser Menüoption gibt an, dass "Medium" die aktuelle Stift Breite ist.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-136">A check mark on this menu choice indicates that medium is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="9ba4c-137"><span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Stift/Thick</span><span class="sxs-lookup"><span data-stu-id="9ba4c-137"><span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Pen/Thick</span></span>
</dt> <dd>

<span data-ttu-id="9ba4c-138">Wählt die Dicke Breite für das Zeichnen aus.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-138">Chooses the thick width for drawing.</span></span> <span data-ttu-id="9ba4c-139">Ein Häkchen in dieser Menüoption gibt an, dass "Thick" die aktuelle Stift Breite ist.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-139">A check mark on this menu choice indicates that thick is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="9ba4c-140"><span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Stift/schlank</span><span class="sxs-lookup"><span data-stu-id="9ba4c-140"><span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Pen/Thin</span></span>
</dt> <dd>

<span data-ttu-id="9ba4c-141">Wählt die schmale Breite für das Zeichnen aus.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-141">Chooses the thin width for drawing.</span></span> <span data-ttu-id="9ba4c-142">Ein Häkchen in dieser Menüoption gibt an, dass schlank die aktuelle Stift Breite ist.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-142">A check mark on this menu choice indicates that thin is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="9ba4c-143"><span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Senke/Verbindung</span><span class="sxs-lookup"><span data-stu-id="9ba4c-143"><span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Sink/Connect</span></span>
</dt> <dd>

<span data-ttu-id="9ba4c-144">Verbindet die copapersink ipapersink-Schnittstelle mit dem copaper-objekttaschen-Verbindungspunkt.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-144">Connects the COPaperSink IPaperSink interface to the COPaper object PaperSink connection point.</span></span> <span data-ttu-id="9ba4c-145">Das erneute Zeichnen des aktuellen Zeichnungs Bilds in [stoclien](structured-storage-client-sample--stoclien-.md) basiert auf der Senke-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-145">Repainting of the current drawing image in [StoClien](structured-storage-client-sample--stoclien-.md) relies on the sink connection.</span></span> <span data-ttu-id="9ba4c-146">Ein Häkchen in dieser Menüoption gibt an, dass das Neuzeichnen verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-146">A check mark on this menu choice indicates that repainting is connected.</span></span>

</dd> <dt>

<span data-ttu-id="9ba4c-147"><span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Senke/Verbindung trennen</span><span class="sxs-lookup"><span data-stu-id="9ba4c-147"><span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Sink/Disconnect</span></span>
</dt> <dd>

<span data-ttu-id="9ba4c-148">Trennt die copapersink ipapersink-Schnittstelle vom copaper-Objekt Taschenbuch-Verbindungspunkt.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-148">Disconnects the COPaperSink IPaperSink interface from the COPaper object PaperSink connection point.</span></span> <span data-ttu-id="9ba4c-149">Das erneute Zeichnen des aktuellen Zeichnungs Bilds in [stoclien](structured-storage-client-sample--stoclien-.md) basiert auf der Senke-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-149">Repainting of the current drawing image in [StoClien](structured-storage-client-sample--stoclien-.md) relies on the sink connection.</span></span> <span data-ttu-id="9ba4c-150">Ein Häkchen in dieser Menüoption gibt an, dass das erneute zeichnen getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-150">A check mark on this menu choice indicates that repainting is disconnected.</span></span>

</dd> <dt>

<span data-ttu-id="9ba4c-151"><span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Tutorial zu Hilfe/stoclien</span><span class="sxs-lookup"><span data-stu-id="9ba4c-151"><span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Help/StoClien Tutorial</span></span>
</dt> <dd>

<span data-ttu-id="9ba4c-152">Öffnet die STOCLIEN.HTM Tutorial-Datei im Webbrowser.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-152">Opens the STOCLIEN.HTM tutorial file in the Web browser.</span></span>

</dd> <dt>

<span data-ttu-id="9ba4c-153"><span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Hilfe/stobedient-Tutorial</span><span class="sxs-lookup"><span data-stu-id="9ba4c-153"><span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Help/StoServe Tutorial</span></span>
</dt> <dd>

<span data-ttu-id="9ba4c-154">Öffnet die STOSERVE.HTM Tutorial-Datei im Webbrowser.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-154">Opens the STOSERVE.HTM tutorial file in the Web browser.</span></span>

</dd> <dt>

<span data-ttu-id="9ba4c-155"><span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Hilfe/lesen der Quelldatei</span><span class="sxs-lookup"><span data-stu-id="9ba4c-155"><span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Help/Read Source File</span></span>
</dt> <dd>

<span data-ttu-id="9ba4c-156">Zeigt das Dialogfeld Öffnen an, sodass Sie eine Quelldatei aus dieser Lektion oder eine andere in Windows Notepad öffnen können.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-156">Displays the Open dialog box so you can open a source file from this lesson or another one in the Windows Notepad.</span></span>

</dd> <dt>

<span data-ttu-id="9ba4c-157"><span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Hilfe/Informationen zu stoclien</span><span class="sxs-lookup"><span data-stu-id="9ba4c-157"><span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Help/About StoClien</span></span>
</dt> <dd>

<span data-ttu-id="9ba4c-158">Zeigt das Dialogfeld Info für diese Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-158">Displays the About dialog box for this application.</span></span>

</dd> </dl>

<span data-ttu-id="9ba4c-159">Das [stoclien](structured-storage-client-sample--stoclien-.md) -Beispiel verwendet viele der Hilfsprogrammklassen und-Dienste, die von [apputil](./using-visual-studio.md)bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-159">The [StoClien](structured-storage-client-sample--stoclien-.md) sample uses many of the utility classes and services provided by [APPUTIL](./using-visual-studio.md).</span></span> <span data-ttu-id="9ba4c-160">Weitere Informationen zu [apputil](./using-visual-studio.md)finden Sie im Quellcode der [apputil](./using-visual-studio.md) -Bibliothek im neben geordneten [apputil](./using-visual-studio.md) -Verzeichnis und in apputil.MD im haupttutorial-Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="9ba4c-160">For more information about [APPUTIL](./using-visual-studio.md), see the [APPUTIL](./using-visual-studio.md) library source code in the sibling [APPUTIL](./using-visual-studio.md) directory and Apputil.md in the main tutorial directory.</span></span> <span data-ttu-id="9ba4c-161">Weitere Informationen zu [apputil](./using-visual-studio.md)finden Sie unter [Erstellen von Beispielen](how-to-build-samples.md).</span><span class="sxs-lookup"><span data-stu-id="9ba4c-161">For more information about [APPUTIL](./using-visual-studio.md), see [How to Build Samples](how-to-build-samples.md).</span></span>

 

 