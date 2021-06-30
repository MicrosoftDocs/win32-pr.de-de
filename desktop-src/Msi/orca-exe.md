---
description: Orca.exe ist ein Datenbanktabellen-Editor zum Erstellen und Bearbeiten Windows Installer Paketen und Mergemodulen.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4647b137650bfba521dba3976ea7a1ae66451ce
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102159"
---
# <a name="orcaexe"></a><span data-ttu-id="ec985-103">Orca.exe</span><span class="sxs-lookup"><span data-stu-id="ec985-103">Orca.exe</span></span>

<span data-ttu-id="ec985-104">Orca.exe ist ein Datenbanktabellen-Editor zum Erstellen und Bearbeiten Windows Installer Paketen und Mergemodulen.</span><span class="sxs-lookup"><span data-stu-id="ec985-104">Orca.exe is a database table editor for creating and editing Windows Installer packages and merge modules.</span></span> <span data-ttu-id="ec985-105">Das Tool stellt eine grafische Benutzeroberfläche für die Validierung bereit, die die bestimmten Einträge hervorhebt, in denen Validierungsfehler oder Warnungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="ec985-105">The tool provides a graphical interface for validation, highlighting the particular entries where validation errors or warnings occur.</span></span>

<span data-ttu-id="ec985-106">Dieses Tool ist nur in der Windows SDK [Components for Windows Installer Developers verfügbar.](platform-sdk-components-for-windows-installer-developers.md)</span><span class="sxs-lookup"><span data-stu-id="ec985-106">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="ec985-107">Sie wird als Orca.msi bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ec985-107">It is provided as an Orca.msi file.</span></span> <span data-ttu-id="ec985-108">Doppelklicken Sie nach der Windows SDK Components for Windows Installer Developers auf Orca.msi, um die Orca.exe zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ec985-108">After installing the Windows SDK Components for Windows Installer Developers, double click Orca.msi to install the Orca.exe file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec985-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec985-109">Syntax</span></span>

<span data-ttu-id="ec985-110">\**orca\*\*\*\[\<options>\]\[\<source file>\]*</span><span class="sxs-lookup"><span data-stu-id="ec985-110">**orca** *\[\<options>\]\[\<source file>\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="ec985-111">Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="ec985-111">Command Line Options</span></span>

<span data-ttu-id="ec985-112">Orca.exe verwendet die folgenden Befehlszeilenoptionen, bei der die Groß-/Kleinschreibung nicht beachtet wird.</span><span class="sxs-lookup"><span data-stu-id="ec985-112">Orca.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="ec985-113">Ein Schrägstrichtrennzeichen kann auch statt eines Bindestrichs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec985-113">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="ec985-114">Option</span><span class="sxs-lookup"><span data-stu-id="ec985-114">Option</span></span> | <span data-ttu-id="ec985-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec985-115">Description</span></span>                                                 |
|--------|-------------------------------------------------------------|
| <span data-ttu-id="ec985-116">-q</span><span class="sxs-lookup"><span data-stu-id="ec985-116">-q</span></span>     | <span data-ttu-id="ec985-117">Stiller Modus</span><span class="sxs-lookup"><span data-stu-id="ec985-117">Quiet mode</span></span>                                                  |
| <span data-ttu-id="ec985-118">-S</span><span class="sxs-lookup"><span data-stu-id="ec985-118">-s</span></span>     | <span data-ttu-id="ec985-119"><*Datenbank*> Schemadatenbank \[ "orca.dat" – Standard\]</span><span class="sxs-lookup"><span data-stu-id="ec985-119"><*database*> Schema database \["orca.dat" - default\]</span></span> |
| <span data-ttu-id="ec985-120">-?</span><span class="sxs-lookup"><span data-stu-id="ec985-120">-?</span></span>     | <span data-ttu-id="ec985-121">Hilfedialogfeld</span><span class="sxs-lookup"><span data-stu-id="ec985-121">Help dialog</span></span>                                                 |



 

<span data-ttu-id="ec985-122">Orca.exe verwendet die folgenden Befehlszeilenoptionen, bei der die Groß-/Kleinschreibung nicht beachtet wird, mit Mergemodulen.</span><span class="sxs-lookup"><span data-stu-id="ec985-122">Orca.exe uses the following case-insensitive command line options with merge modules.</span></span> <span data-ttu-id="ec985-123">Ein Schrägstrichtrennzeichen kann auch statt eines Bindestrichs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec985-123">A slash delimiter may also be used in place of a dash.</span></span> <span data-ttu-id="ec985-124">Beim Mergen sind die Quelldateidateien -f, -m und -m <*alle*> erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec985-124">When performing a merge the -f, -m and <*sourcefile*> are all required.</span></span>



| <span data-ttu-id="ec985-125">Option</span><span class="sxs-lookup"><span data-stu-id="ec985-125">Option</span></span>     | <span data-ttu-id="ec985-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec985-126">Description</span></span>                                                                |
|------------|----------------------------------------------------------------------------|
| <span data-ttu-id="ec985-127">-c</span><span class="sxs-lookup"><span data-stu-id="ec985-127">-c</span></span>         | <span data-ttu-id="ec985-128">Führen Sie einen Commit für die Zusammenführung in die Datenbank aus, wenn keine Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="ec985-128">Commit merge to database if no errors.</span></span>                                     |
| <span data-ttu-id="ec985-129">-!</span><span class="sxs-lookup"><span data-stu-id="ec985-129">-!</span></span>         | <span data-ttu-id="ec985-130">Führen Sie auch dann einen Commit für die Zusammenführung in eine Datenbank durch, wenn Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="ec985-130">Commit merge to a database even if there are errors.</span></span>                       |
| <span data-ttu-id="ec985-131">-M</span><span class="sxs-lookup"><span data-stu-id="ec985-131">-m</span></span>         | <span data-ttu-id="ec985-132"><*modul*> Merge Module to merge into database (Modul zum Zusammenführen mit der Datenbank).</span><span class="sxs-lookup"><span data-stu-id="ec985-132"><*module*> Merge Module to merge into database.</span></span>                      |
| <span data-ttu-id="ec985-133">-f</span><span class="sxs-lookup"><span data-stu-id="ec985-133">-f</span></span>         | <span data-ttu-id="ec985-134">\[Feature:Feature2-Funktionen \] zum Herstellen einer Verbindung mit dem Mergemodul.</span><span class="sxs-lookup"><span data-stu-id="ec985-134">Feature\[:Feature2\] Feature(s) to connect to Merge Module.</span></span>                |
| <span data-ttu-id="ec985-135">-r</span><span class="sxs-lookup"><span data-stu-id="ec985-135">-r</span></span>         | <span data-ttu-id="ec985-136"><*Verzeichnis-ID*> Verzeichniseintrag für die Stammumleitung des Moduls.</span><span class="sxs-lookup"><span data-stu-id="ec985-136"><*directory id*> Directory entry for the module root redirection.</span></span>    |
| <span data-ttu-id="ec985-137">-X</span><span class="sxs-lookup"><span data-stu-id="ec985-137">-x</span></span>         | <span data-ttu-id="ec985-138"><*Verzeichnis>* Dateien in ein Image unter dem Verzeichnis extrahieren.</span><span class="sxs-lookup"><span data-stu-id="ec985-138"><*directory*> Extract files to an image under the directory.</span></span>         |
| <span data-ttu-id="ec985-139">-g</span><span class="sxs-lookup"><span data-stu-id="ec985-139">-g</span></span>         | <span data-ttu-id="ec985-140"><*Language*> Sprache, die zum Öffnen eines Moduls verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ec985-140"><*language*> Language used to open a module.</span></span>                         |
| <span data-ttu-id="ec985-141">-l</span><span class="sxs-lookup"><span data-stu-id="ec985-141">-l</span></span>         | <span data-ttu-id="ec985-142"><*Protokolldatei>* Datei, die als Protokoll verwendet werden soll, fügen Sie an, wenn sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ec985-142"><*log file*> File to use as a log, append if it already exists.</span></span>      |
| <span data-ttu-id="ec985-143">-i</span><span class="sxs-lookup"><span data-stu-id="ec985-143">-i</span></span>         | <span data-ttu-id="ec985-144"><*Verzeichnis>* Dateien in das Quellimage unter dem Verzeichnis extrahieren.</span><span class="sxs-lookup"><span data-stu-id="ec985-144"><*directory*> Extract files to the source image under the directory.</span></span> |
| <span data-ttu-id="ec985-145">-cab</span><span class="sxs-lookup"><span data-stu-id="ec985-145">-cab</span></span>       | <span data-ttu-id="ec985-146"><*Dateiname>* MsM-Schränkung in Datei extrahieren.</span><span class="sxs-lookup"><span data-stu-id="ec985-146"><*filename*> Extract the MSM cabinet to file.</span></span>                        |
| <span data-ttu-id="ec985-147">-lfn</span><span class="sxs-lookup"><span data-stu-id="ec985-147">-lfn</span></span>       | <span data-ttu-id="ec985-148">Verwenden Sie lange Dateinamen während der Extraktion.</span><span class="sxs-lookup"><span data-stu-id="ec985-148">Use Long File Names during the extraction.</span></span>                                 |
| <span data-ttu-id="ec985-149">-configure</span><span class="sxs-lookup"><span data-stu-id="ec985-149">-configure</span></span> | <span data-ttu-id="ec985-150"><*filename>* Konfigurieren sie das Modul mithilfe von Daten aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="ec985-150"><*filename*> Configure the module using data from a file.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="ec985-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ec985-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec985-152">Windows Installer-Entwicklungstools</span><span class="sxs-lookup"><span data-stu-id="ec985-152">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="ec985-153">Veröffentlichte Versionen, Tools und Redistributables</span><span class="sxs-lookup"><span data-stu-id="ec985-153">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



