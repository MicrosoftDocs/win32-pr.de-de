---
description: Die FASTOEM-Eigenschaft ist so konzipiert, dass OEMs den Zeitaufwand für die Installation Windows Installer Anwendungen für ein bestimmtes Szenario verkürzen können.
ms.assetid: 4c0af524-eb2e-4d64-bb25-3dae488d236d
title: FASTOEM-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78993a4affed62baf7e15a2b7787d83cabb9429e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362133"
---
# <a name="fastoem-property"></a><span data-ttu-id="0f6c8-103">FASTOEM-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0f6c8-103">FASTOEM property</span></span>

<span data-ttu-id="0f6c8-104">Die **FASTOEM** -Eigenschaft ist so konzipiert, dass OEMs den Zeitaufwand für die Installation Windows Installer Anwendungen für ein bestimmtes Szenario verkürzen können.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-104">The **FASTOEM** property is designed to enable OEMs to reduce the time it takes to install Windows Installer applications for a specific scenario.</span></span> <span data-ttu-id="0f6c8-105">Erstellen Sie die **FASTOEM** -Eigenschaft nicht in der [Eigenschaften Tabelle](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="0f6c8-105">Do not author the **FASTOEM** property into the [Property Table](property-table.md).</span></span>

<span data-ttu-id="0f6c8-106">Die **FASTOEM** -Eigenschaft ist nur anwendbar, wenn alle folgenden Bedingungen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="0f6c8-106">The **FASTOEM** property is only applicable if all of these conditions are true:</span></span>

-   <span data-ttu-id="0f6c8-107">Die Anwendung wird auf demselben Volume wie der Ordner installiert, der die Quelldateien enthält.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-107">The application is being installed on the same volume as the folder containing the source files.</span></span>
-   <span data-ttu-id="0f6c8-108">Die Quelldateien werden nach der Installation gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-108">The source files are deleted after the installation.</span></span>
-   <span data-ttu-id="0f6c8-109">Während der Installation wird keine Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-109">No user interface is displayed during the installation.</span></span> <span data-ttu-id="0f6c8-110">Die [Benutzeroberflächen Ebene](user-interface-levels.md) ist "None".</span><span class="sxs-lookup"><span data-stu-id="0f6c8-110">The [user interface level](user-interface-levels.md) is none.</span></span>
-   <span data-ttu-id="0f6c8-111">Die Installation wird im [Installations Kontext](installation-context.md)pro Computer durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-111">The installation is performed in the per-machine [installation context](installation-context.md).</span></span>
-   <span data-ttu-id="0f6c8-112">Auf dem Computer ist ausreichend Speicherplatz für eine erfolgreiche Installation vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-112">There is enough space on the computer for a successful installation.</span></span>
-   <span data-ttu-id="0f6c8-113">Dies ist die erstmalige Installation.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-113">This is first time installation.</span></span> <span data-ttu-id="0f6c8-114">Die Installation ist nicht Werbung, Neuinstallation, Entfernung oder Durchführung einer administrativen Installation.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-114">The installation is not advertising, reinstalling, removing, or doing an administrative installation.</span></span>
-   <span data-ttu-id="0f6c8-115">Es sind keine Features zum Ausführen von der Quelle installiert.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-115">No features are installed to run from source.</span></span>
-   <span data-ttu-id="0f6c8-116">Das Installationspaket enthält keine [isolierten Komponenten](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="0f6c8-116">The installation package contains no [isolated components](isolated-components.md).</span></span> <span data-ttu-id="0f6c8-117">Da für isolierte Komponenten das verbleiben der Quelldateien an der Quelle erforderlich ist, kann die **FASTOEM** -Eigenschaft derzeit nicht mit isolierten Komponenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-117">Because isolated components require source files to remain located at the source, the **FASTOEM** property cannot currently be used with isolated components.</span></span>

<span data-ttu-id="0f6c8-118">Wenn alle vorherigen Bedingungen zutreffen, ermöglicht das Festlegen der **FASTOEM** -Eigenschaft Windows Installer, die Leistung zu verbessern, indem die folgenden Schritte ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="0f6c8-118">If all of the previous conditions are true, setting the **FASTOEM** property enables Windows Installer to improve performance by doing the following:</span></span>

-   <span data-ttu-id="0f6c8-119">Verschieben Sie Dateien auf demselben Volume, anstatt Sie zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-119">Move rather than copy files on the same volume.</span></span> <span data-ttu-id="0f6c8-120">Dies garantiert nicht, dass alle Dateien verschoben und nicht kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-120">This does not guarantee that all files are moved rather than copied.</span></span> <span data-ttu-id="0f6c8-121">Beachten Sie Folgendes: Wenn der Computer über mehrere Festplatten verfügt, müssen Sie die Eigenschaft [**ROOTDRIVE**](rootdrive.md) in der Befehlszeile mit dem Laufwerk initialisieren, das die Installationsquelle enthält.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-121">Note that if the computer has multiple hard drives, you must initialize the [**ROOTDRIVE**](rootdrive.md) property on the command line to the same drive containing the installation source.</span></span>
-   <span data-ttu-id="0f6c8-122">Lassen Sie diese Quelle aus der Quell Liste der Anwendung Weg, damit nachfolgende Neuinstallations-oder Wartungs Installationen standardmäßig die in der [Medien Tabelle](media-table.md)angegebenen CD-ROM-Quellen enthalten.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-122">Omit this source from the application's source list so that subsequent reinstallation or maintenance installations default to the CD-ROM sources specified in the [Media Table](media-table.md).</span></span>
-   <span data-ttu-id="0f6c8-123">Optimieren Sie die [Datei Kosten](file-costing.md).</span><span class="sxs-lookup"><span data-stu-id="0f6c8-123">Streamline [file costing](file-costing.md).</span></span>
-   <span data-ttu-id="0f6c8-124">Unterdrücken von Windows Installer an den Client gesendete Fortschrittsmeldungen.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-124">Suppress progress messages sent from Windows Installer to the client.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f6c8-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f6c8-125">Remarks</span></span>

<span data-ttu-id="0f6c8-126">Da bei der Festlegung von **FASTOEM** keine Statusmeldungen gesendet werden, wird empfohlen, dass Autoren den Wert 1800 manuell für das Timeout in den Schlüssel schreiben.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-126">Because no progress messages are sent when **FASTOEM** is set, it is recommended that authors manually write a value of 1800 for Timeout into the key</span></span>

<span data-ttu-id="0f6c8-127">**HKLM** \\ **Software** \\ **Richtlinien** \\ **Microsoft** \\ **Windows** \\ **Installer** \\ **Timeout**</span><span class="sxs-lookup"><span data-stu-id="0f6c8-127">**HKLM**\\**SoftWare**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**\\**Timeout**</span></span>

<span data-ttu-id="0f6c8-128">Timeout ist ein **reg \_ DWORD** -Typ.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-128">Timeout is a **REG\_DWORD** type.</span></span>

<span data-ttu-id="0f6c8-129">Um die Größe der Anwendung in der Windows 2000-Systemsteuerung unter Software anzuzeigen, müssen Sie den Wert von EstimatedSize manuell in den Schlüssel schreiben.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-129">To display the size of the application in Add or Remove Programs in the Windows 2000 Control Panel, you must manually write the value of EstimatedSize into the key</span></span>

<span data-ttu-id="0f6c8-130">**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Deinstallieren** \\ **< *Produkt* Code >**</span><span class="sxs-lookup"><span data-stu-id="0f6c8-130">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\**<*Product Code*>**</span></span>

<span data-ttu-id="0f6c8-131">Dies ist ein **reg \_ DWORD** -Typ, der der Größe der Anwendung in kBytes entspricht.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-131">This is a **REG\_DWORD** type and equals to the size of the application in Kbytes.</span></span> <span data-ttu-id="0f6c8-132">Dieser Wert wird vom Installationsprogramm nicht automatisch geschrieben.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-132">The installer does not automatically write this value.</span></span>

<span data-ttu-id="0f6c8-133">Verwenden Sie die folgende Beispiel Befehlszeile, wenn die CD-ROM, die an Endbenutzer ausgeliefert wird, das Installationspaket der Anwendung im Stammverzeichnis der CD-ROM speichert.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-133">Use the following example command line if the CD-ROM shipped to end users stores the application's installation package at the root of the CD-ROM.</span></span> <span data-ttu-id="0f6c8-134">Beachten Sie, dass die Volumebezeichnung in der [Medien Tabelle](media-table.md) der MSI-Datei der Volumebezeichnung der CD-ROM entsprechen muss.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-134">Note that the volume label in the [Media Table](media-table.md) of the .msi file must match the volume label of the CD-ROM.</span></span>

<span data-ttu-id="0f6c8-135">**Msiexec/I C: \\ tempimage \\package.msi/Qn/Le logfile.txt ALLUSERS = 1 FASTOEM = 1 DISABLEROLLBACK = 1 ROOTDRIVE = C:\\**</span><span class="sxs-lookup"><span data-stu-id="0f6c8-135">**Msiexec /I C:\\TempImage\\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 ROOTDRIVE=C:\\**</span></span>

<span data-ttu-id="0f6c8-136">Verwenden Sie die folgende Beispiel Befehlszeile, wenn sich das Installationspaket nicht im Stammverzeichnis der CD-ROM befindet, die an Endbenutzer gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-136">Use the following example command line if the installation package is not located at the root of the CD-ROM shipped to end users.</span></span> <span data-ttu-id="0f6c8-137">Sie müssen die [**mediapackagepath**](mediapackagepath.md) -Eigenschaft in diesem Fall auf den Pfad zum Installationspaket festlegen.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-137">You must set the [**MEDIAPACKAGEPATH**](mediapackagepath.md) property in this case to the path to the installation package.</span></span> <span data-ttu-id="0f6c8-138">Die Volumebezeichnung in der [Medien Tabelle](media-table.md) der MSI-Datei muss mit der Volumebezeichnung der CD-ROM identisch sein.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-138">The volume label in the [Media Table](media-table.md) of the .msi file must match the volume label of the CD-ROM.</span></span> <span data-ttu-id="0f6c8-139">Beachten Sie in diesem Fall dieses Beispiel.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-139">In this case follow this example.</span></span>

<span data-ttu-id="0f6c8-140">**Msiexec/I C: \\ tempimage \\package.msi/Qn/Le logfile.txt ALLUSERS = 1 FASTOEM = 1 DISABLEROLLBACK = 1 mediapackagepath = C: \\ tempimage \\package.msi ROOTDRIVE = c:\\**</span><span class="sxs-lookup"><span data-stu-id="0f6c8-140">**Msiexec /I C:\\TempImage\\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 MEDIAPACKAGEPATH=C:\\TempImage\\package.msi ROOTDRIVE=C:\\**</span></span>

## <a name="requirements"></a><span data-ttu-id="0f6c8-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f6c8-141">Requirements</span></span>



| <span data-ttu-id="0f6c8-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f6c8-142">Requirement</span></span> | <span data-ttu-id="0f6c8-143">Wert</span><span class="sxs-lookup"><span data-stu-id="0f6c8-143">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f6c8-144">Version</span><span class="sxs-lookup"><span data-stu-id="0f6c8-144">Version</span></span><br/> | <span data-ttu-id="0f6c8-145">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0f6c8-146">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0f6c8-147">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-147">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="0f6c8-148">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="0f6c8-148">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0f6c8-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f6c8-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f6c8-150">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f6c8-150">Properties</span></span>](properties.md)
</dt> </dl>

 

 




