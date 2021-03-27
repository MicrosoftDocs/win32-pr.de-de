---
description: Wenn die Shell das Einfügen neuer Medien oder die Anlage eines Hot-Plug-Geräts erkennt, wird der Inhalt des Geräts oder der Medien bestimmt. Die automatische Wiedergabe führt in Abhängigkeit von den aktuellen Einstellungen eine der folgenden Bedingungen aus.
title: Verwenden und Konfigurieren von AutoPlay
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 096c7042-8cf0-4e4f-934f-274564218f4c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 04a4f6dd09e03f26b13649e860beb7f2621ce952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750304"
---
# <a name="using-and-configuring-autoplay"></a><span data-ttu-id="7d0f0-104">Verwenden und Konfigurieren von AutoPlay</span><span class="sxs-lookup"><span data-stu-id="7d0f0-104">Using and Configuring AutoPlay</span></span>

<span data-ttu-id="7d0f0-105">Wenn die Shell das Einfügen neuer Medien oder die Anlage eines Hot-Plug-Geräts erkennt, wird der Inhalt des Geräts oder der Medien bestimmt.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-105">When the Shell detects the insertion of new media or the attachment of a hot-plug device, the contents of the device or media are determined.</span></span> <span data-ttu-id="7d0f0-106">Die automatische Wiedergabe führt in Abhängigkeit von den aktuellen Einstellungen eine der folgenden Bedingungen aus.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-106">AutoPlay, depending on its current settings, does one of the following.</span></span>

-   <span data-ttu-id="7d0f0-107">Gibt den Inhalt automatisch wieder.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-107">Plays the content automatically.</span></span>
-   <span data-ttu-id="7d0f0-108">Zeigt ein Dialogfeld an, in dem der Benutzer zur Auswahl eines Standard Handlers für einen einzelnen Inhaltstyp aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-108">Displays a dialog box prompting the user to choose a default handler for a single content type.</span></span>
-   <span data-ttu-id="7d0f0-109">Zeigt eine Liste der verfügbaren handleranwendungen an, die im Fall gemischter Inhalte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-109">Presents, in the case of mixed content, a list of available handler applications to launch.</span></span> <span data-ttu-id="7d0f0-110">Der ausgewählte Handler übernimmt dann automatisch den zugehörigen Inhaltstyp.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-110">The chosen handler then automatically plays its associated content type.</span></span>
-   <span data-ttu-id="7d0f0-111">Zeigt eine Standardordner Ansicht der Dateien an.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-111">Displays a standard folder view of the files.</span></span>
-   <span data-ttu-id="7d0f0-112">Führt keine Aktion aus, wenn der Benutzer zuvor **keine Aktion** für diesen Inhaltstyp ausführen und **die Option immer die ausgewählte Aktion** ausführen ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-112">Does nothing if, earlier, the user had chosen **Take no action** for that content type as well as specified **Always do the selected action**.</span></span>

<span data-ttu-id="7d0f0-113">Wenn der Inhalt die Kriterien für die automatische Wiedergabe nicht erfüllt, wird das Ereignis an die Windows-Abbild Beschaffung (WIA) weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-113">If the contents do not meet the criteria for AutoPlay, the event is then passed to Windows Image Acquisition (WIA).</span></span>

<span data-ttu-id="7d0f0-114">In den folgenden Themen wird das Setup und die Verwendung von AutoPlay erläutert.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-114">The following topics discuss the setup and use of AutoPlay.</span></span>

-   [<span data-ttu-id="7d0f0-115">Vorbereiten von Hardware und Software für die Verwendung mit Autoplay</span><span class="sxs-lookup"><span data-stu-id="7d0f0-115">Preparing Hardware and Software for Use with AutoPlay</span></span>](#preparing-hardware-and-software-for-use-with-autoplay)
-   [<span data-ttu-id="7d0f0-116">Suchen von Medien durch AutoPlay</span><span class="sxs-lookup"><span data-stu-id="7d0f0-116">How AutoPlay Searches Media</span></span>](#how-autoplay-searches-media)
-   [<span data-ttu-id="7d0f0-117">Definieren von einzelnen und gemischten Inhaltstypen</span><span class="sxs-lookup"><span data-stu-id="7d0f0-117">Defining Single and Mixed Content Types</span></span>](#defining-single-and-mixed-content-types)
-   [<span data-ttu-id="7d0f0-118">Beispielszenarien</span><span class="sxs-lookup"><span data-stu-id="7d0f0-118">Sample Scenarios</span></span>](#sample-scenarios)
    -   [<span data-ttu-id="7d0f0-119">AutoPlay für Speichergeräte mit Bildmedien</span><span class="sxs-lookup"><span data-stu-id="7d0f0-119">AutoPlay for Storage Devices with Picture Media</span></span>](#autoplay-for-storage-devices-with-picture-media)
    -   [<span data-ttu-id="7d0f0-120">Automatische Wiedergabe von Musikdateien und Speichergeräten mit Musik Medien</span><span class="sxs-lookup"><span data-stu-id="7d0f0-120">AutoPlay for Music File Playback Devices and Storage Devices Containing Music Media</span></span>](#autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media)
    -   [<span data-ttu-id="7d0f0-121">AutoPlay für die Video Wiedergabe bei der ersten Präsentation</span><span class="sxs-lookup"><span data-stu-id="7d0f0-121">AutoPlay for Video Playback on First Presentation</span></span>](#autoplay-for-video-playback-on-first-presentation)
-   [<span data-ttu-id="7d0f0-122">Zuweisen von standardhandleranwendungen</span><span class="sxs-lookup"><span data-stu-id="7d0f0-122">Assigning Default Handler Applications</span></span>](#assigning-default-handler-applications)
-   [<span data-ttu-id="7d0f0-123">Verarbeiten von Medien mit gemischten Inhaltstypen</span><span class="sxs-lookup"><span data-stu-id="7d0f0-123">Handling Media Containing Mixed Content Types</span></span>](#handling-media-containing-mixed-content-types)
-   [<span data-ttu-id="7d0f0-124">Wiedergabe von Benutzeroberflächen</span><span class="sxs-lookup"><span data-stu-id="7d0f0-124">AutoPlay User Interfaces</span></span>](#autoplay-user-interfaces)
    -   [<span data-ttu-id="7d0f0-125">Dialog Feld "einzelner Inhaltstyp"</span><span class="sxs-lookup"><span data-stu-id="7d0f0-125">Single Content Type Dialog Box</span></span>](#single-content-type-dialog-box)
    -   [<span data-ttu-id="7d0f0-126">Dialog Feld ' Gemischte Medien '</span><span class="sxs-lookup"><span data-stu-id="7d0f0-126">Mixed Media Dialog Box</span></span>](#mixed-media-dialog-box)
    -   [<span data-ttu-id="7d0f0-127">Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="7d0f0-127">Property Page</span></span>](#property-page)

## <a name="preparing-hardware-and-software-for-use-with-autoplay"></a><span data-ttu-id="7d0f0-128">Vorbereiten von Hardware und Software für die Verwendung mit Autoplay</span><span class="sxs-lookup"><span data-stu-id="7d0f0-128">Preparing Hardware and Software for Use with AutoPlay</span></span>

<span data-ttu-id="7d0f0-129">Mehrere Informationen müssen in der Registrierung angezeigt werden, damit die automatische Wiedergabe funktioniert.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-129">Several pieces of information need to appear in the registry for AutoPlay to function.</span></span> <span data-ttu-id="7d0f0-130">Diese Informationen interagieren und verweisen aufeinander, um die vollständige AutoPlay-Umgebung zu bilden.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-130">These pieces of information interact and reference each other to form the full AutoPlay environment.</span></span> <span data-ttu-id="7d0f0-131">In diesem Dokument wird das Einrichten der einzelnen Informationen als einzelner eigenständiger Vorgang dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-131">This document presents the setup of each of these pieces of information as an individual stand-alone procedure.</span></span>

<span data-ttu-id="7d0f0-132">Weitere Anweisungen finden Sie in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-132">See the following topics for additional instructions.</span></span>

-   [<span data-ttu-id="7d0f0-133">Zuweisen eines Geräte Handlers zu einem Gerät</span><span class="sxs-lookup"><span data-stu-id="7d0f0-133">How To Assign a Device Handler to a Device</span></span>](how-to-assign-a-device-handler-to-a-device.md)
-   [<span data-ttu-id="7d0f0-134">Angeben eines Symbols, einer Bezeichnung oder eines Geräte Handlers für ein Gerät mithilfe einer Gerätegruppe</span><span class="sxs-lookup"><span data-stu-id="7d0f0-134">How To Specify an Icon, Label, or Device Handler for a Device Using a Device Group</span></span>](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md)
-   [<span data-ttu-id="7d0f0-135">Angeben eines Symbols, einer Bezeichnung oder eines Geräte Handlers für ein Gerät mithilfe einer Geräteklasse</span><span class="sxs-lookup"><span data-stu-id="7d0f0-135">How To Specify an Icon, Label, or Device Handler for a Device Using a Device Class</span></span>](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md)
-   [<span data-ttu-id="7d0f0-136">Verhindern von AutoPlay für eine Komponente</span><span class="sxs-lookup"><span data-stu-id="7d0f0-136">How To Prevent AutoPlay for a Component</span></span>](how-to-prevent-autoplay-for-a-component.md)
-   [<span data-ttu-id="7d0f0-137">Registrieren eines Handlers für ein Geräte Ereignis</span><span class="sxs-lookup"><span data-stu-id="7d0f0-137">How To Register a Handler for a Device Event</span></span>](how-to-register-a-handler-for-a-device-event.md)
-   [<span data-ttu-id="7d0f0-138">Verwenden von AutoPlay-Ereignissen in laufenden Anwendungen</span><span class="sxs-lookup"><span data-stu-id="7d0f0-138">How To Use AutoPlay Events in Running Applications</span></span>](how-to-use-autoplay-events-in-running-applications.md)
-   [<span data-ttu-id="7d0f0-139">Registrieren eines Ereignis Handlers</span><span class="sxs-lookup"><span data-stu-id="7d0f0-139">How To Register an Event Handler</span></span>](how-to-register-an-event-handler.md)

## <a name="how-autoplay-searches-media"></a><span data-ttu-id="7d0f0-140">Suchen von Medien durch AutoPlay</span><span class="sxs-lookup"><span data-stu-id="7d0f0-140">How AutoPlay Searches Media</span></span>

<span data-ttu-id="7d0f0-141">Bei der automatischen Suche werden Medien mit vier Verzeichnis Ebenen unter dem Stammverzeichnis gesucht, um bekannte Dateitypen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-141">AutoPlay searches for media four directory levels below the root directory to find known file types.</span></span> <span data-ttu-id="7d0f0-142">Er verwendet den Wert "wahrnehmvedtype", der einer Dateinamenerweiterung in der Registrierung zugeordnet ist, um die Datei Kategorie zu bestimmen, ob es sich um ein Bild, eine Audiodatei oder eine Videodatei handelt.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-142">It uses the PerceivedType value associated with a file name extension in the registry to determine the file category, whether it is an image, an audio file, or a video file.</span></span> <span data-ttu-id="7d0f0-143">Mit diesen Informationen wird durch die automatische Wiedergabe der entsprechende Handler für das Gerät und den Dateityp gestartet.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-143">With this information, AutoPlay launches the appropriate handler for that device and file type.</span></span> <span data-ttu-id="7d0f0-144">Weitere Informationen finden Sie unter [wahrgenommene Typen und Anwendungs Registrierung](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="7d0f0-144">For more information, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="defining-single-and-mixed-content-types"></a><span data-ttu-id="7d0f0-145">Definieren von einzelnen und gemischten Inhaltstypen</span><span class="sxs-lookup"><span data-stu-id="7d0f0-145">Defining Single and Mixed Content Types</span></span>

<span data-ttu-id="7d0f0-146">Die Autoplay definiert drei Hauptinhalts Kategorien.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-146">AutoPlay defines three main content categories.</span></span>

-   <span data-ttu-id="7d0f0-147">Bilder</span><span class="sxs-lookup"><span data-stu-id="7d0f0-147">Pictures</span></span>
-   <span data-ttu-id="7d0f0-148">Musik</span><span class="sxs-lookup"><span data-stu-id="7d0f0-148">Music</span></span>
-   <span data-ttu-id="7d0f0-149">Video</span><span class="sxs-lookup"><span data-stu-id="7d0f0-149">Video</span></span>

<span data-ttu-id="7d0f0-150">Ein Medium wird als einzelner Inhaltstyp betrachtet, wenn alle Dateien auf dem Medium nur in eine dieser drei Kategorien fallen.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-150">A medium is considered to contain a single content type if all of the files on the medium fall into only one of these three categories.</span></span> <span data-ttu-id="7d0f0-151">Beachten Sie, dass dies nicht bedeutet, dass die Dateien denselben *Dateityp* aufweisen müssen. jpg, GIF und BMP sind unterschiedliche Dateitypen, aber ein Inhaltstyp (Bilder).</span><span class="sxs-lookup"><span data-stu-id="7d0f0-151">Note that this does not mean that the files must be of the same *file* type; .jpg, .gif, and .bmp are different file types, but one content type (pictures).</span></span>

<span data-ttu-id="7d0f0-152">Wenn unterstützte Inhaltstypen auf dem Medium vorhanden sind, aber kein einzelner Inhaltstyp 100 Prozent der Gesamtsumme berücksichtigen kann, wird das Medium als gemischter Inhaltstyp angesehen und entsprechend behandelt.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-152">If supported content types are present on the medium, but no single content type can account for 100 percent of the total, then the medium is considered to contain mixed content type and is handled accordingly.</span></span> <span data-ttu-id="7d0f0-153">Weitere Informationen finden Sie unter [Verarbeiten von Medien, die gemischte Inhaltstypen enthalten](#handling-media-containing-mixed-content-types).</span><span class="sxs-lookup"><span data-stu-id="7d0f0-153">For more information, see [Handling Media Containing Mixed Content Types](#handling-media-containing-mixed-content-types).</span></span>

## <a name="sample-scenarios"></a><span data-ttu-id="7d0f0-154">Beispielszenarien</span><span class="sxs-lookup"><span data-stu-id="7d0f0-154">Sample Scenarios</span></span>

<span data-ttu-id="7d0f0-155">In den folgenden Szenarien wird erläutert, was von der automatischen Wiedergabe zu erwarten ist.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-155">The following scenarios provide a basic understanding of what to expect from AutoPlay.</span></span>

### <a name="autoplay-for-storage-devices-with-picture-media"></a><span data-ttu-id="7d0f0-156">AutoPlay für Speichergeräte mit Bildmedien</span><span class="sxs-lookup"><span data-stu-id="7d0f0-156">AutoPlay for Storage Devices with Picture Media</span></span>

1.  <span data-ttu-id="7d0f0-157">Der Benutzer fügt ein USB-Gerät mit einem USB-Lese Gerät an, auf das bereits ein Medium eingefügt wurde, das 100% Bild Inhaltstyp in Form von JPG-Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-157">The user attaches a USB SanDisk CompactFlash reader device that already has media inserted containing 100 percent picture content type in the form of .jpg files.</span></span>
2.  <span data-ttu-id="7d0f0-158">Benachrichtigung zeigt **neue Hardware-SanDisk ImageMate gefunden**.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-158">Notification displays **Found New Hardware - SanDisk ImageMate**.</span></span>
3.  <span data-ttu-id="7d0f0-159">Die automatische Abbild Anwendung wird von der automatischen Wiedergabe gestartet</span><span class="sxs-lookup"><span data-stu-id="7d0f0-159">AutoPlay launches the appropriate image application.</span></span>

<span data-ttu-id="7d0f0-160">Analog dazu bewirkt das Medien Einfügungs Ereignis auch dann, dass das Media INSERT-Ereignis zum Starten der Bild Folie Show-Anwendung eine automatische Wiedergabe der Bild Folie anzeigt, wenn der Benutzer das gleiche "CompactFlash"-Medium in den Reader einfügt.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-160">Similarly, when the user inserts that same CompactFlash media into the reader when the reader is already attached to the system, the media insert event also causes AutoPlay to launch the image slide show application.</span></span> <span data-ttu-id="7d0f0-161">Der Benutzer hat die Möglichkeit, auf der Seite "Eigenschaften" des SanDisk Media-Geräts den Standardwert in eine andere registrierte AutoPlay-Anwendung zu ändern, wie z. b. den Scanner für Scanner und Kameras.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-161">The user has the option of going to the Properties page of the SanDisk media device to change the default to another registered AutoPlay application, such as the Scanner and Camera Wizard or Picture It!.</span></span>

### <a name="autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media"></a><span data-ttu-id="7d0f0-162">Automatische Wiedergabe von Musikdateien und Speichergeräten mit Musik Medien</span><span class="sxs-lookup"><span data-stu-id="7d0f0-162">AutoPlay for Music File Playback Devices and Storage Devices Containing Music Media</span></span>

1.  <span data-ttu-id="7d0f0-163">Der Benutzer fügt einen USB-Diamant-MP3-Player an.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-163">The user attaches a USB Diamond Rio MP3 Player.</span></span>
2.  <span data-ttu-id="7d0f0-164">In der Benachrichtigung **finden Sie neue Hardware-Diamant Rio MP3 Player**.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-164">Notification displays **Found New Hardware - Diamond Rio MP3 Player**.</span></span>
3.  <span data-ttu-id="7d0f0-165">AutoPlay gibt die Dateien mithilfe Ihres registrierten Standard Handlers wieder – beispielsweise Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-165">AutoPlay plays the files using its registered default handler—for instance, Windows Media Player.</span></span>

<span data-ttu-id="7d0f0-166">Wenn der Benutzer beispielsweise ein Medium mit. MP3-Dateien (z. b. "CompactFlash", "SmartMedia", "Memory Stick" oder CD-ROM) einfügt, das 100 Prozent der gesamten unterstützten Inhalte in ein Speichergerät einfügt, würde das Media INSERT-Ereignis auch zur Wiedergabe der Dateien mit dem Windows-Media Player führen.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-166">Similarly, if the user inserts any media containing .mp3 files (for example, CompactFlash, SmartMedia, Memory Stick, or CD-ROM) that account for 100 percent of the total supported content into a storage device, the media insert event would also cause AutoPlay to play the files using the Windows Media Player.</span></span> <span data-ttu-id="7d0f0-167">Der Benutzer kann auf das Eigenschaften Blatt des Speichergeräts zugreifen und die Standardaktion in eine andere registrierte AutoPlay-Anwendung wie z. b. "Winamp" oder "Real Player" ändern.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-167">The user can access the property sheet of the storage device and change the default action to another registered AutoPlay application, such as WinAmp or Real Player.</span></span>

### <a name="autoplay-for-video-playback-on-first-presentation"></a><span data-ttu-id="7d0f0-168">AutoPlay für die Video Wiedergabe bei der ersten Präsentation</span><span class="sxs-lookup"><span data-stu-id="7d0f0-168">AutoPlay for Video Playback on First Presentation</span></span>

1.  <span data-ttu-id="7d0f0-169">Der Benutzer ist zum ersten Mal eine digitale 1394-Videokamera angeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-169">The user plugs in a 1394 digital video camera for the first time.</span></span>
2.  <span data-ttu-id="7d0f0-170">Dem Benutzer wird ein einfaches Dialogfeld angezeigt, in dem Sie gefragt werden, welche Anwendung ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-170">The user is presented with a simple dialog box that asks what application to run.</span></span> <span data-ttu-id="7d0f0-171">Die Auswahl besteht darin, eine der registrierten AutoPlay-Anwendungen auszuführen oder einen Ordner zum Anzeigen von Dateien zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-171">The choices are to run one of the registered AutoPlay applications or to open a folder to view files.</span></span> <span data-ttu-id="7d0f0-172">Der Benutzer kann das ausgewählte Verhalten so festlegen, dass es als Standardaktion für spätere Hot-Plug-Ereignisse der digitalen Videokamera gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-172">The user may set the selected behavior to be saved as the default action for later digital video camera hot-plug events.</span></span>

## <a name="assigning-default-handler-applications"></a><span data-ttu-id="7d0f0-173">Zuweisen von standardhandleranwendungen</span><span class="sxs-lookup"><span data-stu-id="7d0f0-173">Assigning Default Handler Applications</span></span>

<span data-ttu-id="7d0f0-174">Eine Neuinstallation von Windows findet eine automatische Wiedergabe mit einem Satz registrierter handleranwendungen.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-174">A fresh installation of Windows finds AutoPlay with a set of registered handler applications.</span></span> <span data-ttu-id="7d0f0-175">Anwendungen, die während einer Windows-Installation standardmäßig registriert sind, lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-175">Applications registered by default during a Windows installation are as follows.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7d0f0-176">Medientyp</span><span class="sxs-lookup"><span data-stu-id="7d0f0-176">Media Type</span></span></th>
<th><span data-ttu-id="7d0f0-177">Anwendungen</span><span class="sxs-lookup"><span data-stu-id="7d0f0-177">Applications</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d0f0-178">Bilder</span><span class="sxs-lookup"><span data-stu-id="7d0f0-178">Pictures</span></span></td>
<td><ul>
<li><span data-ttu-id="7d0f0-179">Folien Anzeige (Standard)</span><span class="sxs-lookup"><span data-stu-id="7d0f0-179">Slide Show (default)</span></span></li>
<li><span data-ttu-id="7d0f0-180">Kamera-und Scanner-Assistent</span><span class="sxs-lookup"><span data-stu-id="7d0f0-180">Camera and Scanner Wizard</span></span></li>
<li><span data-ttu-id="7d0f0-181">Druck-Assistent</span><span class="sxs-lookup"><span data-stu-id="7d0f0-181">Printing Wizard</span></span></li>
<li><span data-ttu-id="7d0f0-182">Ordner öffnen</span><span class="sxs-lookup"><span data-stu-id="7d0f0-182">Open folder</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d0f0-183">Musik</span><span class="sxs-lookup"><span data-stu-id="7d0f0-183">Music</span></span></td>
<td><ul>
<li><span data-ttu-id="7d0f0-184">Windows-Media Player (Standard)</span><span class="sxs-lookup"><span data-stu-id="7d0f0-184">Windows Media Player (default)</span></span></li>
<li><span data-ttu-id="7d0f0-185">Ordner öffnen</span><span class="sxs-lookup"><span data-stu-id="7d0f0-185">Open folder</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d0f0-186">Video</span><span class="sxs-lookup"><span data-stu-id="7d0f0-186">Video</span></span></td>
<td><ul>
<li><span data-ttu-id="7d0f0-187">Windows-Media Player (Standard)</span><span class="sxs-lookup"><span data-stu-id="7d0f0-187">Windows Media Player (default)</span></span></li>
<li><span data-ttu-id="7d0f0-188">Ordner öffnen</span><span class="sxs-lookup"><span data-stu-id="7d0f0-188">Open folder</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7d0f0-189">Bei nicht unterstützten Typen werden Benutzer aufgefordert, die Standardeinstellung für die Autoplay-Aktion zuzuweisen, die den einzelnen Speichergeräten bei der ersten Einführung in das System zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-189">In the case of non-supported types, users are asked to assign the default setting for the AutoPlay action associated with each storage device on its first introduction to the system.</span></span> <span data-ttu-id="7d0f0-190">Zu diesem Zeitpunkt wird der Benutzer aufgefordert, eine Aktion aus einer bereitgestellten Liste registrierter Anwendungen auszuwählen oder eine Ordneransicht anzuzeigen, in der der Medieninhalt aufgelistet ist.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-190">At that time, the user is prompted to choose an action from a provided list of registered applications or to display a folder view listing the media content.</span></span> <span data-ttu-id="7d0f0-191">Der Benutzer hat auch die Möglichkeit, jedes Mal, wenn der Medientyp erkannt wird, aufgefordert zu werden, anstatt eine bestimmte Anwendung als Standard zu speichern.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-191">The user also has the option of choosing to be prompted each time the media type is detected rather than saving any particular application as a default.</span></span>

> [!Note]  
> <span data-ttu-id="7d0f0-192">Gerätehersteller können Standardanwendungen registrieren und zuweisen, die für ihre jeweiligen Produkte verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-192">Device manufacturers have the option of registering and assigning default applications to be used with their particular products.</span></span> <span data-ttu-id="7d0f0-193">In diesen Fällen wird das Dialogfeld, das dem Benutzer eine Auswahl bietet, nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-193">In these cases, the dialog box offering a choice to the user is not displayed.</span></span>

 

<span data-ttu-id="7d0f0-194">Um von der automatischen Wiedergabe als handleroption angeboten zu werden, müssen sich neu installierte Anwendungen selbst in der Registrierung registrieren.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-194">To be offered as a handler option by AutoPlay, newly installed applications must register themselves in the registry.</span></span> <span data-ttu-id="7d0f0-195">Weitere Informationen finden Sie unter [Vorbereiten von Hardware und Software für die Verwendung mit Autoplay](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="7d0f0-195">For details, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

<span data-ttu-id="7d0f0-196">Benutzer können den standardmäßigen AutoPlay-Handler für beliebige Speichergeräte oder Inhaltstyp jederzeit ändern.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-196">Users can always change the default AutoPlay handler for any storage device or content type.</span></span> <span data-ttu-id="7d0f0-197">Der Zugriff auf die Eigenschaften Seite "AutoPlay" kann im Eigenschaften Blatt des Speichergeräts in **Arbeitsplatz** geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-197">The AutoPlay property page is accessible for change in the property sheet of the storage device in **My Computer**.</span></span>

<span data-ttu-id="7d0f0-198">Beispiele für Benutzer Aufforderungen und Eigenschaften Seiten finden Sie unter [AutoPlay User Interfaces](#autoplay-user-interfaces).</span><span class="sxs-lookup"><span data-stu-id="7d0f0-198">For examples of user prompts and property pages, see [AutoPlay User Interfaces](#autoplay-user-interfaces).</span></span>

## <a name="handling-media-containing-mixed-content-types"></a><span data-ttu-id="7d0f0-199">Verarbeiten von Medien mit gemischten Inhaltstypen</span><span class="sxs-lookup"><span data-stu-id="7d0f0-199">Handling Media Containing Mixed Content Types</span></span>

<span data-ttu-id="7d0f0-200">Wenn die automatische Wiedergabe mit einem gemischten Inhalts Medium erfolgt, ist eine Benutzereingabe erforderlich, bevor Sie Maßnahmen ergreifen kann.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-200">When AutoPlay is presented with a mixed content medium, it requires user input before it can take action.</span></span> <span data-ttu-id="7d0f0-201">In diesem Fall wird dem Benutzer ein Dialogfeld angezeigt, das eine gefilterte Liste aller entsprechenden registrierten Anwendungen enthält, die für die auf dem Medium vorhandenen Inhaltstypen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-201">In this case, the user is presented with a dialog box containing a filtered list of all appropriate registered applications available for the content types present on the media.</span></span> <span data-ttu-id="7d0f0-202">Der Benutzer kann eine dieser Anwendungen auswählen, um diesen bestimmten Inhaltstyp zu wiedergeben, während der Rest unverändert bleibt.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-202">The user can choose one of these applications to AutoPlay that particular content type, while the rest remain untouched.</span></span> <span data-ttu-id="7d0f0-203">Wenn die Komposition gemischter Inhalts Medien mit den einzelnen einzelnen CDs variiert, ist es nicht möglich, diese Auswahl als Standard zu speichern.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-203">As the composition of mixed content media varies with each individual disc, there is no option to save this choice as a default.</span></span>

<span data-ttu-id="7d0f0-204">Beispiele für Benutzer Aufforderungen finden Sie unter [AutoPlay User Interfaces](#autoplay-user-interfaces).</span><span class="sxs-lookup"><span data-stu-id="7d0f0-204">For examples of user prompts, see [AutoPlay User Interfaces](#autoplay-user-interfaces).</span></span>

## <a name="autoplay-user-interfaces"></a><span data-ttu-id="7d0f0-205">Wiedergabe von Benutzeroberflächen</span><span class="sxs-lookup"><span data-stu-id="7d0f0-205">AutoPlay User Interfaces</span></span>

<span data-ttu-id="7d0f0-206">Es gibt drei mögliche Benutzeroberflächen.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-206">There are three possible user interfaces.</span></span>

-   <span data-ttu-id="7d0f0-207">Ein Dialogfeld, in dem der Benutzer aufgefordert wird, eine Aktion für einen einzelnen Inhaltstyp einzugeben.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-207">A dialog box that prompts the user to enter an action for a single content type</span></span>
-   <span data-ttu-id="7d0f0-208">Ein Dialogfeld, in dem der Benutzer aufgefordert wird, eine Aktion für gemischte Inhaltstypen einzugeben</span><span class="sxs-lookup"><span data-stu-id="7d0f0-208">A dialog box that prompts the user to enter an action for mixed content types</span></span>
-   <span data-ttu-id="7d0f0-209">Eine Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="7d0f0-209">A property page</span></span>

### <a name="single-content-type-dialog-box"></a><span data-ttu-id="7d0f0-210">Dialog Feld "einzelner Inhaltstyp"</span><span class="sxs-lookup"><span data-stu-id="7d0f0-210">Single Content Type Dialog Box</span></span>

<span data-ttu-id="7d0f0-211">Ein Dialogfeld ähnlich dem folgenden wird angezeigt, wenn ein unterstütztes Medium, dem noch keine Standardaktion für die automatische Wiedergabe zugewiesen wurde, dem System angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-211">A dialog box similar to the following is displayed when any supported media not yet assigned a default AutoPlay action is presented to the system.</span></span>

![Screenshot des Dialog Felds "einzelner Inhaltstyp"](images/pix.png)

<span data-ttu-id="7d0f0-213">Benutzer können eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="7d0f0-213">Users can do one of the following.</span></span>

-   <span data-ttu-id="7d0f0-214">Wählen Sie in der Liste der registrierten Anwendungen eine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-214">Choose an action from the list of registered applications.</span></span>
-   <span data-ttu-id="7d0f0-215">Listet die Dateien auf dem Medium in einer normalen Ordneransicht auf.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-215">List the files on the medium in a normal folder view.</span></span>
-   <span data-ttu-id="7d0f0-216">Führen Sie keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-216">Take no action.</span></span>

<span data-ttu-id="7d0f0-217">Ein Benutzer kann auch eine Auswahl als Standardaktion für dieses Medium speichern, indem Sie auf das Feld **ausgewählte Aktion immer** ausführen klicken.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-217">A user can also save a choice as the default action for this medium by clicking the **Always do the selected action** box.</span></span> <span data-ttu-id="7d0f0-218">Nachdem diese Auswahl getroffen wurde, wird das Dialogfeld nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-218">Once this choice is made, the dialog is not shown again.</span></span> <span data-ttu-id="7d0f0-219">Wenn jedoch in Windows XP Service Pack 1 (SP1) eine neue Anwendung, die einen bestimmten Medientyp verarbeiten kann, dem Computer hinzugefügt wird, wird das Dialogfeld dem Benutzer erneut angezeigt, sodass die neue Anwendung als Standardaktion für die automatische Wiedergabe ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-219">However, in Windows XP Service Pack 1 (SP1), if a new application that can handle a particular media type is added to the computer, the dialog is once again presented to the user, giving them the opportunity to select the new application as the default AutoPlay action.</span></span> <span data-ttu-id="7d0f0-220">Anwendungen können sich auch selbst als Standardauswahl festlegen, wenn Sie installiert werden.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-220">Applications can also set themselves as the default selection when they are installed.</span></span>

<span data-ttu-id="7d0f0-221">Windows XP SP1 fügt auch eine Funktion hinzu, die die Auswahl der Aktion für die automatische Wiedergabe durch den Benutzer beibehält, wenn Sie nicht auf das Feld **ausgewählte Aktion immer** ausführen klicken.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-221">Windows XP SP1 also adds a feature that retains the user's choice of AutoPlay action if they do not click the **Always do the selected action** box.</span></span> <span data-ttu-id="7d0f0-222">Wenn ein Benutzer eine Autoplay-Aktion für eine einzelne Instanz auswählt, wird bei der nächsten Anzeige des Dialog Felds für den Medientyp dieselbe Aktion als Standardauswahl angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-222">If a user chooses an AutoPlay action for a single instance, the next time that dialog is presented for that media type, the same action is the default selection.</span></span>

<span data-ttu-id="7d0f0-223">Damit eine Anwendung in die Liste der möglichen Aktionen eingeschlossen werden kann, muss Sie bei der automatischen Wiedergabe registriert werden.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-223">For an application to be included in the list of possible actions, it must be registered with AutoPlay.</span></span> <span data-ttu-id="7d0f0-224">Weitere Informationen finden Sie unter [Vorbereiten von Hardware und Software für die Verwendung mit Autoplay](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="7d0f0-224">For more information, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

### <a name="mixed-media-dialog-box"></a><span data-ttu-id="7d0f0-225">Dialog Feld ' Gemischte Medien '</span><span class="sxs-lookup"><span data-stu-id="7d0f0-225">Mixed Media Dialog Box</span></span>

<span data-ttu-id="7d0f0-226">Das folgende Dialogfeld wird angezeigt, wenn ein Medium, das eine Mischung aus unterstützten Dateitypen enthält, dem System angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-226">The following dialog box is displayed when any medium containing a mix of supported file types is presented to the system.</span></span> <span data-ttu-id="7d0f0-227">Dies ist im Wesentlichen das gleiche wie das einzelne Inhalts Medium (Dialogfeld), jedoch mit zwei signifikanten Unterschieden.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-227">This is essentially the same as the single content medium dialog box but with two significant differences.</span></span> <span data-ttu-id="7d0f0-228">Zuerst bestehen die verfügbaren Aktions Optionen aus einer gefilterten Liste von Anwendungen, die für alle auf dem Medium vorhandenen Inhaltstypen relevant sind.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-228">First, the available action options consist of a filtered list of applications relevant to all content types present on the medium.</span></span> <span data-ttu-id="7d0f0-229">Zweitens gibt es keine Option zum Auswählen einer permanenten Standardaktion, da die Inhaltstypen und Prozentsätze gemischter Inhalts Medien zu unvorhersehbar sind.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-229">Second, there is no option to choose a permanent default action because the content types and percentages of mixed content media are too unpredictable.</span></span>

![Screenshot des Dialog Felds "Gemischte Medien"](images/mix.png)

<span data-ttu-id="7d0f0-231">Damit eine Anwendung in die Liste der möglichen Aktionen eingeschlossen werden kann, muss Sie bei der automatischen Wiedergabe registriert werden.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-231">For an application to be included in the list of possible actions, it must be registered with AutoPlay.</span></span> <span data-ttu-id="7d0f0-232">Weitere Informationen finden Sie unter [Vorbereiten von Hardware und Software für die Verwendung mit Autoplay](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="7d0f0-232">For more information, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

### <a name="property-page"></a><span data-ttu-id="7d0f0-233">Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="7d0f0-233">Property Page</span></span>

<span data-ttu-id="7d0f0-234">Im folgenden finden Sie ein Beispiel für eine Autoplay-Eigenschaften Seite für ein DVD/CD-ROM-Gerät.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-234">The following is a sample AutoPlay property page for a DVD/CD-ROM device.</span></span>

![Screenshot der Eigenschaften Seite](images/apdlg.png)

<span data-ttu-id="7d0f0-236">Jeder Gerätetyp bietet eine geeignete Teilmenge der Inhaltstypen für die automatische Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-236">Each device type offers an appropriate subset of content types for AutoPlay configuration.</span></span> <span data-ttu-id="7d0f0-237">Jeder Inhaltstyp, wenn er ausgewählt wird, bietet wiederum eine passende Liste von Aktions Optionen im Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-237">In turn, each content type, when selected, offers an appropriate list of action options in the list box.</span></span> <span data-ttu-id="7d0f0-238">Für jeden Inhaltstyp kann eine andere Aktion ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="7d0f0-238">A different action can be chosen for each content type.</span></span>

 

 



