---
description: Mit den Funktionen in diesem Abschnitt werden Druckertreiber auf einem Computer installiert und konfiguriert.
ms.assetid: e6aa8963-aa1a-4313-bc24-2aeb4f4b93c4
title: Referenz zur Druckertreiber Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1613725ec5c7e2dbb06710bff706ec5aa7e32dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362311"
---
# <a name="printer-driver-installation-reference"></a><span data-ttu-id="abc00-103">Referenz zur Druckertreiber Installation</span><span class="sxs-lookup"><span data-stu-id="abc00-103">Printer Driver Installation Reference</span></span>

<span data-ttu-id="abc00-104">Mit den Funktionen in diesem Abschnitt werden Druckertreiber auf einem Computer installiert und konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="abc00-104">The functions in this section install and configure printer drivers on a computer.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="abc00-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="abc00-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="abc00-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="abc00-106">Function</span></span></th>
<th><span data-ttu-id="abc00-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="abc00-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc00-108"><a href="addmonitor.md"><strong>Addmonitor</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-108"><a href="addmonitor.md"><strong>AddMonitor</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-109">Mit der <a href="/windows/desktop/printdocs/addmonitor"><strong>addmonitor</strong></a> -Funktion wird ein lokaler Port Monitor installiert, und die Konfigurations-, Daten-und Überwachungs Dateien werden verknüpft.</span><span class="sxs-lookup"><span data-stu-id="abc00-109">The <a href="/windows/desktop/printdocs/addmonitor"><strong>AddMonitor</strong></a> function installs a local port monitor and links the configuration, data, and monitor files.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abc00-110"><a href="addport.md"><strong>AddPort</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-110"><a href="addport.md"><strong>AddPort</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-111">Die Funktion <a href="/windows/desktop/printdocs/addport"><strong>AddPort</strong></a> fügt der Liste der unterstützten Ports den Namen eines Ports hinzu.</span><span class="sxs-lookup"><span data-stu-id="abc00-111">The <a href="/windows/desktop/printdocs/addport"><strong>AddPort</strong></a> function adds the name of a port to the list of supported ports.</span></span> <span data-ttu-id="abc00-112">Die Funktion <strong>AddPort</strong> wird vom Port Monitor exportiert.</span><span class="sxs-lookup"><span data-stu-id="abc00-112">The <strong>AddPort</strong> function is exported by the port monitor.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abc00-113"><a href="addprinterdriver.md"><strong>Addprinterdriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-113"><a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-114">Mit der <a href="/windows/desktop/printdocs/addprinterdriver"><strong>addprinterdriver</strong></a> -Funktion wird ein lokaler oder Remote Druckertreiber installiert, und die Konfigurations-, Daten-und Treiberdateien werden zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="abc00-114">The <a href="/windows/desktop/printdocs/addprinterdriver"><strong>AddPrinterDriver</strong></a> function installs a local or remote printer driver and associates the configuration, data, and driver files.</span></span><br/> <span data-ttu-id="abc00-115">Wenn Sie Druckertreiber installieren oder aktualisieren, können Sie die <a href="addprinterdriverex.md"><strong>addprinterdriverex</strong></a> -Funktion verwenden, da Sie strikte Upgrades, strikte Downgrade, das Kopieren von neueren Dateien und das Kopieren aller Dateien (unabhängig von den Dateizeitstempeln) zulässt.</span><span class="sxs-lookup"><span data-stu-id="abc00-115">For more flexibility in installing or upgrading printer drivers, use the <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> function because it allows strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of the file time stamps).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="abc00-116">Das Installieren eines Druckertreibers ohne Treiber Paket wird nicht mehr empfohlen.</span><span class="sxs-lookup"><span data-stu-id="abc00-116">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="abc00-117">Verwenden Sie stattdessen " <a href="installprinterdriverfrompackage.md"><strong>installprinterdriverfrompackage</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="abc00-117">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abc00-118"><a href="addprinterdriverex.md"><strong>Addprinterdriverex</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-118"><a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-119">Die Funktion <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>addprinterdriverex</strong></a> installiert einen lokalen oder Remote Druckertreiber und verknüpft die Konfigurations-, Daten-und Treiberdateien.</span><span class="sxs-lookup"><span data-stu-id="abc00-119">The <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>AddPrinterDriverEx</strong></a> function installs a local or remote printer driver and links the configuration, data, and driver files.</span></span> <span data-ttu-id="abc00-120">Neben den Funktionen von <a href="addprinterdriver.md"><strong>addprinterdriver</strong></a>bietet es auch Optionen, die das strikte Upgrade, das strikte Downgrade, das Kopieren von neueren Dateien und das Kopieren aller Dateien (unabhängig von Dateizeitstempeln) ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="abc00-120">Besides having the capabilities of <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a>, it also has options that permit strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of file time stamps).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="abc00-121">Das Installieren eines Druckertreibers ohne Treiber Paket wird nicht mehr empfohlen.</span><span class="sxs-lookup"><span data-stu-id="abc00-121">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="abc00-122">Verwenden Sie stattdessen " <a href="installprinterdriverfrompackage.md"><strong>installprinterdriverfrompackage</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="abc00-122">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abc00-123"><a href="addprintprocessor.md"><strong>Addprintprocessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-123"><a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-124">Die <a href="/windows/desktop/printdocs/addprintprocessor"><strong>addprintprocessor</strong></a> -Funktion installiert einen Druck Prozessor auf dem angegebenen Server und fügt der Liste der unterstützten Druck Prozessoren den Druck Prozessor Namen hinzu.</span><span class="sxs-lookup"><span data-stu-id="abc00-124">The <a href="/windows/desktop/printdocs/addprintprocessor"><strong>AddPrintProcessor</strong></a> function installs a print processor on the specified server and adds the print-processor name to the list of supported print processors.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abc00-125"><a href="addprintprovidor.md"><strong>Addprintprovidor</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-125"><a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-126">Die <a href="/windows/desktop/printdocs/addprintprovidor"><strong>addprintprovidor</strong></a> -Funktion installiert einen lokalen Druckanbieter und verknüpft die Konfigurations-, Daten-und Anbieter Dateien.</span><span class="sxs-lookup"><span data-stu-id="abc00-126">The <a href="/windows/desktop/printdocs/addprintprovidor"><strong>AddPrintProvidor</strong></a> function installs a local print provider and links the configuration, data, and provider files.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abc00-127"><a href="coreprinterdriverinstalled.md"><strong>Coreprinterdriverinstalliert</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-127"><a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-128">Die <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>coreprinterdriverinstallierte</strong></a> -Funktion meldet, ob ein Kern Druckertreiber mit der angegebenen GUID, dem angegebenen Datum und der angegebenen Version installiert ist.</span><span class="sxs-lookup"><span data-stu-id="abc00-128">The <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>CorePrinterDriverInstalled</strong></a> function reports whether a core printer driver with a specified GUID, date, and version is installed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abc00-129"><a href="deletemonitor.md"><strong>Deletemonitor</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-129"><a href="deletemonitor.md"><strong>DeleteMonitor</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-130">Die <a href="/windows/desktop/printdocs/deletemonitor"><strong>deletemonitor</strong></a> -Funktion entfernt einen von der <a href="addmonitor.md"><strong>addmonitor</strong></a> -Funktion hinzugefügten Port Monitor.</span><span class="sxs-lookup"><span data-stu-id="abc00-130">The <a href="/windows/desktop/printdocs/deletemonitor"><strong>DeleteMonitor</strong></a> function removes a port monitor added by the <a href="addmonitor.md"><strong>AddMonitor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abc00-131"><a href="deleteport.md"><strong>DeletePort</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-131"><a href="deleteport.md"><strong>DeletePort</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-132">Die Funktion <a href="/windows/desktop/printdocs/deleteport"><strong>deletePort</strong></a> zeigt ein Dialogfeld an, in dem der Benutzer einen Portnamen löschen kann.</span><span class="sxs-lookup"><span data-stu-id="abc00-132">The <a href="/windows/desktop/printdocs/deleteport"><strong>DeletePort</strong></a> function displays a dialog box that allows the user to delete a port name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abc00-133"><a href="deleteprinterdriver.md"><strong>Deleteprinterdriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-133"><a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-134">Die <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>deleteprinterdriver</strong></a> -Funktion entfernt den angegebenen Druckertreiber Namen aus der Liste der Namen unterstützter Treiber auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="abc00-134">The <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> function removes the specified printer-driver name from the list of names of supported drivers on a server.</span></span><br/> <span data-ttu-id="abc00-135">Um die dem Treiber zugeordneten Dateien zu löschen und den angegebenen Druckertreiber Namen aus der Liste der Namen unterstützter Treiber für einen Server zu entfernen, verwenden Sie die Funktion <a href="deleteprinterdriverex.md"><strong>deleteprinterdriverex</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="abc00-135">To delete the files associated with the driver in addition to removing the specified printer-driver name from the list of names of supported drivers for a server, use the <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> function.</span></span><br/> <span data-ttu-id="abc00-136"><a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>Deleteprinterdriver</strong></a> löscht einen Treiber nur dann, wenn keine Version des Treibers für die angegebene Umgebung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="abc00-136"><a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> deletes a driver only if no version of the driver is in use for the specified environment.</span></span> <span data-ttu-id="abc00-137"><a href="deleteprinterdriverex.md"><strong>Deleteprinterdriverex</strong></a> kann bestimmte Versionen des Treibers löschen.</span><span class="sxs-lookup"><span data-stu-id="abc00-137"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> can delete specific versions of the driver.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abc00-138"><a href="deleteprinterdriverex.md"><strong>Deleteprinterdriverex</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-138"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-139">Mit der <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>deleteprinterdriverex</strong></a> -Funktion wird der angegebene Druckertreiber Name aus der Liste mit den Namen unterstützter Treiber auf einem Server entfernt, und die dem Treiber zugeordneten Dateien werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="abc00-139">The <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>DeletePrinterDriverEx</strong></a> function removes the specified printer-driver name from the list of names of supported drivers on a server and deletes the files associated with the driver.</span></span> <span data-ttu-id="abc00-140">Mit dieser Funktion können auch bestimmte Versionen des Treibers gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="abc00-140">This function can also delete specific versions of the driver.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abc00-141"><a href="deleteprinterdriverpackage.md"><strong>Deleteprinterdriverpackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-141"><a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-142">Löscht ein Druckertreiber Paket aus dem Treiber Speicher.</span><span class="sxs-lookup"><span data-stu-id="abc00-142">Deletes a printer driver package from the driver store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abc00-143"><a href="deleteprintprocessor.md"><strong>Deleteprintprocessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-143"><a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-144">Die <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>deleteprintprocessor</strong></a> -Funktion entfernt einen von der <a href="addprintprocessor.md"><strong>addprintprocessor</strong></a> -Funktion hinzugefügten Druck Prozessor.</span><span class="sxs-lookup"><span data-stu-id="abc00-144">The <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>DeletePrintProcessor</strong></a> function removes a print processor added by the <a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abc00-145"><a href="deleteprintprovidor.md"><strong>Deleteprintprovidor</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-145"><a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-146">Die <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>deleteprintprovidor</strong></a> -Funktion entfernt einen von der <a href="addprintprovidor.md"><strong>addprintprovidor</strong></a> -Funktion hinzugefügten Druckanbieter.</span><span class="sxs-lookup"><span data-stu-id="abc00-146">The <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>DeletePrintProvidor</strong></a> function removes a print provider added by the <a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abc00-147"><a href="enummonitors.md"><strong>Enumüberwachungen</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-147"><a href="enummonitors.md"><strong>EnumMonitors</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-148">Die <a href="/windows/desktop/printdocs/enummonitors"><strong>enummonitors</strong></a> -Funktion Ruft Informationen zu den Port Monitoren ab, die auf dem angegebenen Server installiert sind.</span><span class="sxs-lookup"><span data-stu-id="abc00-148">The <a href="/windows/desktop/printdocs/enummonitors"><strong>EnumMonitors</strong></a> function retrieves information about the port monitors installed on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abc00-149"><a href="enumports.md"><strong>EnumPorts</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-149"><a href="enumports.md"><strong>EnumPorts</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-150">Die <a href="/windows/desktop/printdocs/enumports"><strong>enumports</strong></a> -Funktion Listet die Ports auf, die für den Druck auf einem angegebenen Server verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="abc00-150">The <a href="/windows/desktop/printdocs/enumports"><strong>EnumPorts</strong></a> function enumerates the ports that are available for printing on a specified server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abc00-151"><a href="enumprinterdrivers.md"><strong>Enumprinterdrivers</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-151"><a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-152">Die <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>enumprinterdrivers</strong></a> -Funktion Listet die Druckertreiber auf, die auf einem angegebenen Drucker Server installiert sind.</span><span class="sxs-lookup"><span data-stu-id="abc00-152">The <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>EnumPrinterDrivers</strong></a> function enumerates the printer drivers installed on a specified printer server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abc00-153"><a href="enumprintprocessordatatypes.md"><strong>Enumprintprocessordatatypes</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-153"><a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-154">Die <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>enumprintprocessordatatypes</strong></a> -Funktion Listet die Datentypen auf, die ein angegebener Druck Prozessor unterstützt.</span><span class="sxs-lookup"><span data-stu-id="abc00-154">The <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>EnumPrintProcessorDatatypes</strong></a> function enumerates the data types that a specified print processor supports.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abc00-155"><a href="enumprintprocessors.md"><strong>Enumprintprozessoren</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-155"><a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-156">Die Funktion <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>enumprintprozessoren</strong></a> listet die auf dem angegebenen Server installierten Druck Prozessoren auf.</span><span class="sxs-lookup"><span data-stu-id="abc00-156">The <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>EnumPrintProcessors</strong></a> function enumerates the print processors installed on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abc00-157"><a href="getcoreprinterdrivers.md"><strong>Getcoreprinterdrivers</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-157"><a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-158">Ruft die GUID, die Version und das Datum der angegebenen Haupt Druckertreiber und den Pfad zu ihren Paketen ab.</span><span class="sxs-lookup"><span data-stu-id="abc00-158">Retrieves GUID, version, and date of the specified core printer drivers and the path to their packages.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abc00-159"><a href="getprinterdriver.md"><strong>Getprinterdriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-159"><a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-160">Die <a href="/windows/desktop/printdocs/getprinterdriver"><strong>getprinterdriver</strong></a> -Funktion ruft Treiber Daten für den angegebenen Drucker ab.</span><span class="sxs-lookup"><span data-stu-id="abc00-160">The <a href="/windows/desktop/printdocs/getprinterdriver"><strong>GetPrinterDriver</strong></a> function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="abc00-161">Wenn der Treiber nicht auf dem lokalen Computer installiert ist, wird er von <strong>getprinterdriver</strong> installiert.</span><span class="sxs-lookup"><span data-stu-id="abc00-161">If the driver is not installed on the local computer, <strong>GetPrinterDriver</strong> installs it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abc00-162"><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-162"><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-163">Die <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> -Funktion ruft Treiber Daten für den angegebenen Drucker ab.</span><span class="sxs-lookup"><span data-stu-id="abc00-163">The <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="abc00-164">Wenn der Treiber nicht auf dem lokalen Computer installiert ist, installiert <strong>GetPrinterDriver2</strong> ihn und zeigt eine beliebige Benutzeroberfläche für das angegebene Fenster an.</span><span class="sxs-lookup"><span data-stu-id="abc00-164">If the driver is not installed on the local computer, <strong>GetPrinterDriver2</strong> installs it and displays any user interface to the specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abc00-165"><a href="getprinterdriverdirectory.md"><strong>Getprinterdriverdirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-165"><a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-166">Die <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>getprinterdriverdirectory</strong></a> -Funktion Ruft den Pfad des druckertreiberverzeichnisses ab.</span><span class="sxs-lookup"><span data-stu-id="abc00-166">The <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>GetPrinterDriverDirectory</strong></a> function retrieves the path of the printer-driver directory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abc00-167"><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-167"><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-168">Ruft den Pfad zum angegebenen Druckertreiber Paket auf einem Druckserver ab.</span><span class="sxs-lookup"><span data-stu-id="abc00-168">Retrieves the path to the specified printer driver package on a print server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abc00-169"><a href="getprintprocessordirectory.md"><strong>Getprintprocessordirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-169"><a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-170">Die <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>getprintprocessordirectory</strong></a> -Funktion Ruft den Pfad zum Druck Prozessor Verzeichnis auf dem angegebenen Server ab.</span><span class="sxs-lookup"><span data-stu-id="abc00-170">The <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>GetPrintProcessorDirectory</strong></a> function retrieves the path to the print processor directory on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abc00-171"><a href="installprinterdriverfrompackage.md"><strong>Installprinterdriverfrompackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-171"><a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-172">Installiert einen Druckertreiber aus einem Treiber Paket, das sich im Treiber Speicher des Druck Servers befindet.</span><span class="sxs-lookup"><span data-stu-id="abc00-172">Installs a printer driver from a driver package that is in the print server's driver store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abc00-173"><a href="uploadprinterdriverpackage.md"><strong>Uploadprinterdriverpackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="abc00-173"><a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="abc00-174">Lädt einen Druckertreiber in den Treiber Speicher des Druck Servers hoch, sodass er durch Aufrufen von <a href="installprinterdriverfrompackage.md"><strong>installprinterdriverfrompackage</strong></a>installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="abc00-174">Uploads a printer driver to the print server's driver store so that it can be installed by calling <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

