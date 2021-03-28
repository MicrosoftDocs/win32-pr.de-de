---
description: Das Erstellen einer Autorun-fähigen Anwendung ist ein einfaches Verfahren. In diesem Thema wird CD-ROM als Beispiel verwendet (es war das erste Medium, um diese Technologie zu implementieren), aber heute gibt es viele verschiedene Medientypen, von denen es verwendet werden kann.
title: Erstellen einer AutoRun-Enabled Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0d01f4a2-64c4-4b31-9fc9-361da6825ab8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 24a944b011c926d1638e5d0bcb0d35fc348e5783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128468"
---
# <a name="creating-an-autorun-enabled-application"></a><span data-ttu-id="e4f77-104">Erstellen einer AutoRun-Enabled Anwendung</span><span class="sxs-lookup"><span data-stu-id="e4f77-104">Creating an AutoRun-Enabled Application</span></span>

<span data-ttu-id="e4f77-105">Das Erstellen einer Autorun-fähigen Anwendung ist ein einfaches Verfahren.</span><span class="sxs-lookup"><span data-stu-id="e4f77-105">Creating an AutoRun-enabled application is a straightforward procedure.</span></span> <span data-ttu-id="e4f77-106">In diesem Thema wird CD-ROM als Beispiel verwendet (es war das erste Medium, um diese Technologie zu implementieren), aber heute gibt es viele verschiedene Medientypen, von denen es verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e4f77-106">This topic uses CD-ROM as an example (it was the first medium to implement this technology) but today there are many different media types that can use it.</span></span>

<span data-ttu-id="e4f77-107">Um Autorun in Ihrer Anwendung zu aktivieren, schließen Sie einfach zwei wesentliche Dateien ein:</span><span class="sxs-lookup"><span data-stu-id="e4f77-107">To enable AutoRun in your application, you simply include two essential files:</span></span>

-   <span data-ttu-id="e4f77-108">Eine Autorun. inf-Datei</span><span class="sxs-lookup"><span data-stu-id="e4f77-108">An Autorun.inf file</span></span>
-   <span data-ttu-id="e4f77-109">Eine Start Anwendung</span><span class="sxs-lookup"><span data-stu-id="e4f77-109">A startup application</span></span>

<span data-ttu-id="e4f77-110">Wenn ein Benutzer eine CD in ein CD-ROM-Laufwerk auf einem automatisch nicht kompatiblen Computer einfügt, prüft das System sofort, ob die Festplatte über ein persönliches Computerdatei System verfügt.</span><span class="sxs-lookup"><span data-stu-id="e4f77-110">When a user inserts a disc into a CD-ROM drive on a AutoRun-compatible computer, the system immediately checks to see if the disc has a personal computer file system.</span></span> <span data-ttu-id="e4f77-111">Wenn dies der Fall ist, sucht das System nach einer Datei namens " [Autorun. inf](#creating-an-autoruninf-file)".</span><span class="sxs-lookup"><span data-stu-id="e4f77-111">If it does, the system searches for a file named [Autorun.inf](#creating-an-autoruninf-file).</span></span> <span data-ttu-id="e4f77-112">Diese Datei gibt eine Setup Anwendung an, die ausgeführt wird, sowie eine Reihe optionaler Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="e4f77-112">This file specifies a setup application that will be run, along with a variety of optional settings.</span></span> <span data-ttu-id="e4f77-113">Die Start Anwendung installiert, deinstalliert, konfiguriert und führt die Anwendung möglicherweise aus.</span><span class="sxs-lookup"><span data-stu-id="e4f77-113">The startup application typically installs, uninstalls, configures, and perhaps runs the application.</span></span>

-   [<span data-ttu-id="e4f77-114">Erstellen einer Autorun. inf-Datei</span><span class="sxs-lookup"><span data-stu-id="e4f77-114">Creating an Autorun.inf File</span></span>](#creating-an-autoruninf-file)
-   <span data-ttu-id="e4f77-115">[Der \[ Abschnitt "de viceingestall" \]](#the-deviceinstall-section)</span><span class="sxs-lookup"><span data-stu-id="e4f77-115">[The \[DeviceInstall\] Section](#the-deviceinstall-section)</span></span>
-   [<span data-ttu-id="e4f77-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4f77-116">Related topics</span></span>](#related-topics)

## <a name="creating-an-autoruninf-file"></a><span data-ttu-id="e4f77-117">Erstellen einer Autorun. inf-Datei</span><span class="sxs-lookup"><span data-stu-id="e4f77-117">Creating an Autorun.inf File</span></span>

<span data-ttu-id="e4f77-118">Autorun. inf ist eine Textdatei im Stammverzeichnis der CD-ROM, die Ihre Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="e4f77-118">Autorun.inf is a text file located in the root directory of the CD-ROM that contains your application.</span></span> <span data-ttu-id="e4f77-119">Die primäre Funktion besteht darin, dem System den Namen und den Speicherort des Start Programms der Anwendung zur Verfügung zu stellen, das beim Einfügen der Festplatte ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4f77-119">Its primary function is to provide the system with the name and location of the application's startup program that will be run when the disc is inserted.</span></span>

> [!Note]  
> <span data-ttu-id="e4f77-120">Autorun. inf-Dateien werden unter Windows XP nicht für Laufwerke unterstützt, die das Laufwerk \_ von [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea)zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="e4f77-120">Autorun.inf files are not supported under Windows XP for drives that return DRIVE\_REMOVABLE from [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).</span></span>

 

<span data-ttu-id="e4f77-121">Die Datei Autorun. inf kann auch optionale Informationen enthalten, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="e4f77-121">The Autorun.inf file can also contain optional information including:</span></span>

-   <span data-ttu-id="e4f77-122">Der Name einer Datei, die ein Symbol enthält, das das CD-ROM-Laufwerk der Anwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="e4f77-122">The name of a file that contains an icon that will represent your application's CD-ROM drive.</span></span> <span data-ttu-id="e4f77-123">Dieses Symbol wird von Windows-Explorer anstelle des Standard Laufwerks Symbols angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e4f77-123">This icon will be displayed by Windows Explorer in place of the standard drive icon.</span></span>
-   <span data-ttu-id="e4f77-124">Zusätzliche Befehle für das Kontextmenü, das angezeigt wird, wenn der Benutzer mit der rechten Maustaste auf das CD-ROM-Symbol klickt.</span><span class="sxs-lookup"><span data-stu-id="e4f77-124">Additional commands for the shortcut menu that is displayed when the user right-clicks the CD-ROM icon.</span></span> <span data-ttu-id="e4f77-125">Sie können auch den Standardbefehl angeben, der ausgeführt wird, wenn der Benutzer auf das Symbol doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="e4f77-125">You can also specify the default command that is run when the user double-clicks the icon.</span></span>

<span data-ttu-id="e4f77-126">Autorun. inf-Dateien ähneln den INI-Dateien.</span><span class="sxs-lookup"><span data-stu-id="e4f77-126">Autorun.inf files are similar to .ini files.</span></span> <span data-ttu-id="e4f77-127">Sie bestehen aus mindestens einem Abschnitt, wobei jeder mit einem Namen in eckigen Klammern steht.</span><span class="sxs-lookup"><span data-stu-id="e4f77-127">They consist of one or more sections, each headed by a name enclosed in square brackets.</span></span> <span data-ttu-id="e4f77-128">Jeder Abschnitt enthält eine Reihe von Befehlen, die von der Shell ausgeführt werden, wenn die Festplatte eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e4f77-128">Each section contains a series of commands that will be run by the Shell when the disc is inserted.</span></span> <span data-ttu-id="e4f77-129">Es gibt zwei Abschnitte, die derzeit für Autorun. inf-Dateien definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e4f77-129">There are two sections that are currently defined for Autorun.inf files.</span></span>

-   <span data-ttu-id="e4f77-130">Der **\[ Auto ausführen \]** -Abschnitt enthält die Standard Befehle Auto ausführen.</span><span class="sxs-lookup"><span data-stu-id="e4f77-130">The **\[autorun\]** section contains the default AutoRun commands.</span></span> <span data-ttu-id="e4f77-131">Alle Auto ausführen. inf-Dateien müssen über einen **\[ Auto ausführen- \]** Abschnitt verfügen.</span><span class="sxs-lookup"><span data-stu-id="e4f77-131">All Autorun.inf files must have an **\[autorun\]** section.</span></span>
-   <span data-ttu-id="e4f77-132">Ein optionaler Abschnitt " **\[ Autorun. alpha \]** " kann für Systeme eingeschlossen werden, die auf RISC-basierten Computern ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e4f77-132">An optional **\[autorun.alpha\]** section can be included for systems running on RISC-based computers.</span></span> <span data-ttu-id="e4f77-133">Wenn ein CD-ROM-Laufwerk auf einem RISC-basierten System in ein CD-ROM-Laufwerk eingefügt wird, führt die Shell die Befehle in diesem Abschnitt anstelle der im Abschnitt **\[ Auto ausführen \]** .</span><span class="sxs-lookup"><span data-stu-id="e4f77-133">When a disc is inserted in a CD-ROM drive on a RISC-based system, the Shell will run the commands in this section instead of those in the **\[autorun\]** section.</span></span>

> [!Note]  
> <span data-ttu-id="e4f77-134">Die Shell prüft zuerst nach einem architekturspezifischen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="e4f77-134">The Shell checks for an architecture-specific section first.</span></span> <span data-ttu-id="e4f77-135">Wenn eine solche nicht gefunden wird, werden die Informationen im Abschnitt **\[ Auto ausführen \]** verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4f77-135">If it does not find one, it uses the information in the **\[autorun\]** section.</span></span> <span data-ttu-id="e4f77-136">Nachdem die Shell einen Abschnitt gefunden hat, ignoriert Sie alle anderen, sodass jeder Abschnitt in sich selbst enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="e4f77-136">After the Shell finds a section, it ignores all others, so each section must be self-contained.</span></span>

 

<span data-ttu-id="e4f77-137">Jeder Abschnitt enthält eine Reihe von Befehlen, die bestimmen, wie der Autorun-Vorgang stattfindet.</span><span class="sxs-lookup"><span data-stu-id="e4f77-137">Each section contains a series of commands that determine how the Autorun operation takes place.</span></span> <span data-ttu-id="e4f77-138">Es stehen fünf Befehle zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e4f77-138">There are five commands available.</span></span>



| <span data-ttu-id="e4f77-139">Befehl</span><span class="sxs-lookup"><span data-stu-id="e4f77-139">Command</span></span>                         | <span data-ttu-id="e4f77-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4f77-140">Description</span></span>                                                                            |
|---------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4f77-141">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="e4f77-141">defaulticon</span></span>](autorun-cmds.md) | <span data-ttu-id="e4f77-142">Gibt das Standard Symbol für die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="e4f77-142">Specifies the default icon for the application.</span></span>                                        |
| [<span data-ttu-id="e4f77-143">angezeigt</span><span class="sxs-lookup"><span data-stu-id="e4f77-143">icon</span></span>](autorun-cmds.md)        | <span data-ttu-id="e4f77-144">Gibt den Pfad und den Dateinamen eines anwendungsspezifischen Symbols für das CD-ROM-Laufwerk an.</span><span class="sxs-lookup"><span data-stu-id="e4f77-144">Specifies the path and file name of an application-specific icon for the CD-ROM drive.</span></span> |
| [<span data-ttu-id="e4f77-145">open</span><span class="sxs-lookup"><span data-stu-id="e4f77-145">open</span></span>](autorun-cmds.md)        | <span data-ttu-id="e4f77-146">Gibt den Pfad und den Dateinamen der Start Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="e4f77-146">Specifies the path and file name of the startup application.</span></span>                           |
| [<span data-ttu-id="e4f77-147">useautorun</span><span class="sxs-lookup"><span data-stu-id="e4f77-147">useautorun</span></span>](autorun-cmds.md)  | <span data-ttu-id="e4f77-148">Gibt an, dass AutoPlay v2-Features verwendet werden sollen, wenn unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e4f77-148">Specifies that Autoplay V2 features should be used if supported.</span></span>                       |
| [<span data-ttu-id="e4f77-149">schel</span><span class="sxs-lookup"><span data-stu-id="e4f77-149">shell</span></span>](autorun-cmds.md)       | <span data-ttu-id="e4f77-150">Definiert den Standardbefehl im Kontextmenü der CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="e4f77-150">Defines the default command in the CD-ROM's shortcut menu.</span></span>                             |
| [<span data-ttu-id="e4f77-151">\_shellverb</span><span class="sxs-lookup"><span data-stu-id="e4f77-151">shell\_verb</span></span>](autorun-cmds.md) | <span data-ttu-id="e4f77-152">Fügt Befehle zum Kontextmenü der CD-ROM hinzu.</span><span class="sxs-lookup"><span data-stu-id="e4f77-152">Adds commands to the CD-ROM's shortcut menu.</span></span>                                           |



 

<span data-ttu-id="e4f77-153">Im folgenden finden Sie ein Beispiel für eine einfache INF-Datei.</span><span class="sxs-lookup"><span data-stu-id="e4f77-153">The following is an example of a simple Autorun.inf file.</span></span> <span data-ttu-id="e4f77-154">Gibt Filename.exe als Start Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="e4f77-154">It specifies Filename.exe as the startup application.</span></span> <span data-ttu-id="e4f77-155">Das zweite Symbol in Filename.exe stellt das CD-ROM-Laufwerk anstelle des Standard-Laufwerk Symbols dar.</span><span class="sxs-lookup"><span data-stu-id="e4f77-155">The second icon in Filename.exe will represent the CD-ROM drive instead of the standard drive icon.</span></span>


```
[autorun] 
open=Filename.exe 
icon=Filename.exe,1
```



<span data-ttu-id="e4f77-156">In diesem Autorun. inf-Beispiel werden je nach Computertyp verschiedene Start Anwendungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4f77-156">This Autorun.inf sample runs different startup applications depending on the type of computer.</span></span>


```
[autorun] 
open=Filename_x86.exe 
icon=IconFile.ico 

[autorun.alpha] 
open=Filename_RISC.exe 
icon=IconFile.ico
```



## <a name="the-deviceinstall-section"></a><span data-ttu-id="e4f77-157">Der \[ Abschnitt "de viceingestall" \]</span><span class="sxs-lookup"><span data-stu-id="e4f77-157">The \[DeviceInstall\] Section</span></span>

<span data-ttu-id="e4f77-158">Sie können den Abschnitt " **\[ de vicabstall \]** " auf allen Wechselmedien verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4f77-158">You can use the **\[DeviceInstall\]** section on any removable media.</span></span> <span data-ttu-id="e4f77-159">Sie wird nur unter Windows XP unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e4f77-159">It is supported only under Windows XP.</span></span> <span data-ttu-id="e4f77-160">Mit **DriverPath** geben Sie einen Verzeichnispfad an, in dem Windows XP nach Treiberdateien sucht, was eine lange Suche durch den gesamten Inhalt verhindert.</span><span class="sxs-lookup"><span data-stu-id="e4f77-160">You use **DriverPath** to specify a directory path where Windows XP searches for driver files, which prevents a lengthy search through the entire contents.</span></span>

<span data-ttu-id="e4f77-161">Verwenden Sie den Abschnitt **\[ deviceinstall \]** mit einer Treiberinstallation, um Verzeichnisse anzugeben, in denen Windows XP die Medien nach Treiberdateien durchsuchen soll.</span><span class="sxs-lookup"><span data-stu-id="e4f77-161">You use the **\[DeviceInstall\]** section with a driver installation to specify directories where Windows XP should search the media for driver files.</span></span> <span data-ttu-id="e4f77-162">Unter Windows XP werden die gesamten Medien nicht mehr standardmäßig durchsucht, daher muss **\[ devicinstall \]** zum Angeben von Such Standorten erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="e4f77-162">Under Windows XP, entire media are no longer searched by default, therefore requiring **\[DeviceInstall\]** to specify search locations.</span></span> <span data-ttu-id="e4f77-163">Folgendes ist das einzige Wechselmedium, das in Windows XP vollständig ohne einen **\[ deviceinstall \]** -Abschnitt in der Datei "Autorun. inf" durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="e4f77-163">The following are the only removable media that Windows XP fully searches without a **\[DeviceInstall\]** section in an Autorun.inf file.</span></span>

-   <span data-ttu-id="e4f77-164">Disketten in den Laufwerken A oder B.</span><span class="sxs-lookup"><span data-stu-id="e4f77-164">Floppy disks found in drives A or B.</span></span>
-   <span data-ttu-id="e4f77-165">CD/DVD-Medien weniger als 1 Gigabyte (GB).</span><span class="sxs-lookup"><span data-stu-id="e4f77-165">CD/DVD media less that 1 gigabyte (GB) in size.</span></span>

<span data-ttu-id="e4f77-166">Alle anderen Medien müssen einen **\[ deviceinstall \]** -Abschnitt für Windows XP enthalten, um Treiber zu ermitteln, die auf diesem Medium gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="e4f77-166">All other media must include a **\[DeviceInstall\]** section for Windows XP to detect any drivers stored on that media.</span></span>

> [!Note]  
> <span data-ttu-id="e4f77-167">Wie beim **\[ Autorun \]** -Abschnitt kann der Abschnitt " **\[ de viceinstall \]** " architekturspezifisch sein.</span><span class="sxs-lookup"><span data-stu-id="e4f77-167">As with the **\[AutoRun\]** section, the **\[DeviceInstall\]** section can be architecture-specific.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e4f77-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4f77-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4f77-169">Implementieren von Autorun-Start Anwendungen</span><span class="sxs-lookup"><span data-stu-id="e4f77-169">How to Implement Autorun Startup Applications</span></span>](how-to-implement-autorun-startup-applications.md)
</dt> <dt>

[<span data-ttu-id="e4f77-170">Schreiben einer Geräte Installationsanwendung</span><span class="sxs-lookup"><span data-stu-id="e4f77-170">Writing a Device Installation Application</span></span>](/windows-hardware/drivers/install/writing-a-device-installation-application)
</dt> </dl>

 

 
