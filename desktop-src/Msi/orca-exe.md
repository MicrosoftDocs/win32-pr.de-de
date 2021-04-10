---
description: Orca.exe ist ein Datenbanktabellen-Editor zum Erstellen und Bearbeiten von Windows Installer Paketen und Mergemodulen.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f17874e08fcdbfdbab38c480219579897b9896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041674"
---
# <a name="orcaexe"></a><span data-ttu-id="fbbdc-103">Orca.exe</span><span class="sxs-lookup"><span data-stu-id="fbbdc-103">Orca.exe</span></span>

<span data-ttu-id="fbbdc-104">Orca.exe ist ein Datenbanktabellen-Editor zum Erstellen und Bearbeiten von Windows Installer Paketen und Mergemodulen.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-104">Orca.exe is a database table editor for creating and editing Windows Installer packages and merge modules.</span></span> <span data-ttu-id="fbbdc-105">Das Tool stellt eine grafische Benutzeroberfläche für die Validierung bereit und hebt die einzelnen Einträge hervor, bei denen Validierungs Fehler oder Warnungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-105">The tool provides a graphical interface for validation, highlighting the particular entries where validation errors or warnings occur.</span></span>

<span data-ttu-id="fbbdc-106">Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-106">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="fbbdc-107">Sie wird als Orca.msi Datei bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-107">It is provided as an Orca.msi file.</span></span> <span data-ttu-id="fbbdc-108">Nachdem Sie die Windows SDK Komponenten für Windows Installer Entwickler installiert haben, doppelklicken Sie auf Orca.msi, um die Orca.exe-Datei zu installieren.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-108">After installing the Windows SDK Components for Windows Installer Developers, double click Orca.msi to install the Orca.exe file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbbdc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbbdc-109">Syntax</span></span>

<span data-ttu-id="fbbdc-110">\**Orca\*\*\*\[<options>\]\[<source file>\]*</span><span class="sxs-lookup"><span data-stu-id="fbbdc-110">**orca** *\[<options>\]\[<source file>\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="fbbdc-111">Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="fbbdc-111">Command Line Options</span></span>

<span data-ttu-id="fbbdc-112">Orca.exe verwendet die folgenden Befehlszeilenoptionen für die Groß-und Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-112">Orca.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="fbbdc-113">Ein Schrägstrich kann auch anstelle eines Bindestrichs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-113">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="fbbdc-114">Option</span><span class="sxs-lookup"><span data-stu-id="fbbdc-114">Option</span></span> | <span data-ttu-id="fbbdc-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbbdc-115">Description</span></span>                                                 |
|--------|-------------------------------------------------------------|
| <span data-ttu-id="fbbdc-116">-q</span><span class="sxs-lookup"><span data-stu-id="fbbdc-116">-q</span></span>     | <span data-ttu-id="fbbdc-117">Stiller Modus</span><span class="sxs-lookup"><span data-stu-id="fbbdc-117">Quiet mode</span></span>                                                  |
| <span data-ttu-id="fbbdc-118">-S</span><span class="sxs-lookup"><span data-stu-id="fbbdc-118">-s</span></span>     | <span data-ttu-id="fbbdc-119"><*Datenbank* -> Schema \[ -Datenbank "Orca. dat"-Default\]</span><span class="sxs-lookup"><span data-stu-id="fbbdc-119"><*database*> Schema database \["orca.dat" - default\]</span></span> |
| <span data-ttu-id="fbbdc-120">-?</span><span class="sxs-lookup"><span data-stu-id="fbbdc-120">-?</span></span>     | <span data-ttu-id="fbbdc-121">Hilfe Dialogfeld</span><span class="sxs-lookup"><span data-stu-id="fbbdc-121">Help dialog</span></span>                                                 |



 

<span data-ttu-id="fbbdc-122">Orca.exe verwendet die folgenden Befehlszeilenoptionen für die Groß-und Kleinschreibung mit Mergemodulen.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-122">Orca.exe uses the following case-insensitive command line options with merge modules.</span></span> <span data-ttu-id="fbbdc-123">Ein Schrägstrich kann auch anstelle eines Bindestrichs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-123">A slash delimiter may also be used in place of a dash.</span></span> <span data-ttu-id="fbbdc-124">Beim Ausführen einer Zusammenführung sind alle> der Datei "-f", "-m" und "<*SourceFile* " erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-124">When performing a merge the -f, -m and <*sourcefile*> are all required.</span></span>



| <span data-ttu-id="fbbdc-125">Option</span><span class="sxs-lookup"><span data-stu-id="fbbdc-125">Option</span></span>     | <span data-ttu-id="fbbdc-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbbdc-126">Description</span></span>                                                                |
|------------|----------------------------------------------------------------------------|
| <span data-ttu-id="fbbdc-127">-c</span><span class="sxs-lookup"><span data-stu-id="fbbdc-127">-c</span></span>         | <span data-ttu-id="fbbdc-128">Commit in Datenbank zusammenführen, wenn keine Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-128">Commit merge to database if no errors.</span></span>                                     |
| <span data-ttu-id="fbbdc-129">-!</span><span class="sxs-lookup"><span data-stu-id="fbbdc-129">-!</span></span>         | <span data-ttu-id="fbbdc-130">Commit in eine Datenbank zusammenführen, auch wenn Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-130">Commit merge to a database even if there are errors.</span></span>                       |
| <span data-ttu-id="fbbdc-131">-M</span><span class="sxs-lookup"><span data-stu-id="fbbdc-131">-m</span></span>         | <span data-ttu-id="fbbdc-132"><*Modul*> Mergemodul zum Zusammenführen in die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-132"><*module*> Merge Module to merge into database.</span></span>                      |
| <span data-ttu-id="fbbdc-133">-f</span><span class="sxs-lookup"><span data-stu-id="fbbdc-133">-f</span></span>         | <span data-ttu-id="fbbdc-134">Feature \[ : Feature2 \] Feature (e) zum Herstellen einer Verbindung mit dem Mergemodul.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-134">Feature\[:Feature2\] Feature(s) to connect to Merge Module.</span></span>                |
| <span data-ttu-id="fbbdc-135">-r</span><span class="sxs-lookup"><span data-stu-id="fbbdc-135">-r</span></span>         | <span data-ttu-id="fbbdc-136"><*Verzeichnis-ID*> Verzeichniseintrag für die Modul Stamm Umleitung.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-136"><*directory id*> Directory entry for the module root redirection.</span></span>    |
| <span data-ttu-id="fbbdc-137">-X</span><span class="sxs-lookup"><span data-stu-id="fbbdc-137">-x</span></span>         | <span data-ttu-id="fbbdc-138"><*Verzeichnis*> Dateien in ein Bild unter dem Verzeichnis extrahieren.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-138"><*directory*> Extract files to an image under the directory.</span></span>         |
| <span data-ttu-id="fbbdc-139">-g</span><span class="sxs-lookup"><span data-stu-id="fbbdc-139">-g</span></span>         | <span data-ttu-id="fbbdc-140"><*Sprache*> Sprache, mit der ein Modul geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-140"><*language*> Language used to open a module.</span></span>                         |
| <span data-ttu-id="fbbdc-141">-l</span><span class="sxs-lookup"><span data-stu-id="fbbdc-141">-l</span></span>         | <span data-ttu-id="fbbdc-142"><*Protokolldatei*> Datei, die als Protokoll verwendet werden soll, fügen Sie an, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-142"><*log file*> File to use as a log, append if it already exists.</span></span>      |
| <span data-ttu-id="fbbdc-143">-i</span><span class="sxs-lookup"><span data-stu-id="fbbdc-143">-i</span></span>         | <span data-ttu-id="fbbdc-144"><*Verzeichnis*> Dateien in das Quell Abbild im Verzeichnis extrahieren.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-144"><*directory*> Extract files to the source image under the directory.</span></span> |
| <span data-ttu-id="fbbdc-145">-CAB</span><span class="sxs-lookup"><span data-stu-id="fbbdc-145">-cab</span></span>       | <span data-ttu-id="fbbdc-146"><*Dateiname*> den MSM-CAB in eine Datei extrahieren.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-146"><*filename*> Extract the MSM cabinet to file.</span></span>                        |
| <span data-ttu-id="fbbdc-147">-LFN</span><span class="sxs-lookup"><span data-stu-id="fbbdc-147">-lfn</span></span>       | <span data-ttu-id="fbbdc-148">Verwenden Sie lange Dateinamen während der Extraktion.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-148">Use Long File Names during the extraction.</span></span>                                 |
| <span data-ttu-id="fbbdc-149">-Konfigurieren</span><span class="sxs-lookup"><span data-stu-id="fbbdc-149">-configure</span></span> | <span data-ttu-id="fbbdc-150"><*Dateiname*> konfigurieren Sie das Modul mithilfe von Daten aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-150"><*filename*> Configure the module using data from a file.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="fbbdc-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fbbdc-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbbdc-152">Entwicklungs Tools für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="fbbdc-152">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="fbbdc-153">Veröffentlichte Versionen, Tools und verteilbare Dateien</span><span class="sxs-lookup"><span data-stu-id="fbbdc-153">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



