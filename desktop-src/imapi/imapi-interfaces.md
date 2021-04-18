---
title: IMAPI-Schnittstellen
description: In den folgenden Tabellen werden die Schnittstellen, die C/C++-Entwickler verwendet haben, und das zugehörige Skript Objekt kurz beschrieben. Stellen Sie dem Objektnamen in der Tabelle den Namen \ 0034; IMAPI2. \ 0034; , um den Objektnamen vollständig zu qualifizieren, wenn das Objekt im Skript erstellt wird.
ms.assetid: dba81a45-34a8-4b49-9ccb-d61a7e7ee1f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac989a9871b761a1f1700ec599cc51affd30b2e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "106338645"
---
# <a name="imapi-interfaces"></a><span data-ttu-id="f6af0-105">IMAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f6af0-105">IMAPI Interfaces</span></span>

<span data-ttu-id="f6af0-106">In den folgenden Tabellen werden die Schnittstellen, die C/C++-Entwickler verwendet haben, und das zugehörige Skript Objekt kurz beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f6af0-106">The following tables identify and briefly describe the interfaces used C/C++ developers and the associated scripting object.</span></span> <span data-ttu-id="f6af0-107">Stellen Sie dem Objektnamen in der Tabelle den Namen "IMAPI2" als Präfix voran.</span><span class="sxs-lookup"><span data-stu-id="f6af0-107">Prefix the object name in the table with "IMAPI2."</span></span> <span data-ttu-id="f6af0-108">, um den Objektnamen vollständig zu qualifizieren, wenn das Objekt im Skript erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f6af0-108">to fully qualify the object name when creating the object in script.</span></span>

<span data-ttu-id="f6af0-109">In der folgenden Tabelle sind die Schnittstellen, die Geräten zugeordnet sind, das Burn-Engine und das Format Writer und Radierer aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6af0-109">The following table lists the interfaces associated with devices, the burn engine, and the format writers and eraser.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f6af0-110">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f6af0-110">Interface</span></span></td>
<td><span data-ttu-id="f6af0-111">Object</span><span class="sxs-lookup"><span data-stu-id="f6af0-111">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6af0-112">Low-Level-Burn-Engine.</span><span class="sxs-lookup"><span data-stu-id="f6af0-112">Low-level burn engine.</span></span>
<ul>
<li><span data-ttu-id="f6af0-113"><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-113"><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-114"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-114"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-115"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-115"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-116">MsftWriteEngine2</span><span class="sxs-lookup"><span data-stu-id="f6af0-116">MsftWriteEngine2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6af0-117">Hauptbildwriter.</span><span class="sxs-lookup"><span data-stu-id="f6af0-117">Main image writer.</span></span>
<ul>
<li><span data-ttu-id="f6af0-118"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-118"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-119"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-119"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-120"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-120"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-121">MsftDiscFormat2Data</span><span class="sxs-lookup"><span data-stu-id="f6af0-121">MsftDiscFormat2Data</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6af0-122">Datenträger.</span><span class="sxs-lookup"><span data-stu-id="f6af0-122">Disc eraser.</span></span>
<ul>
<li><span data-ttu-id="f6af0-123"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-123"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-124"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-124"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-125">MsftDiscFormat2Erase</span><span class="sxs-lookup"><span data-stu-id="f6af0-125">MsftDiscFormat2Erase</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6af0-126">Rohbildwriter.</span><span class="sxs-lookup"><span data-stu-id="f6af0-126">Raw image writer.</span></span>
<ul>
<li><span data-ttu-id="f6af0-127"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-127"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-128"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-128"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-129"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-129"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-130">MsftDiscFormat2RawCD</span><span class="sxs-lookup"><span data-stu-id="f6af0-130">MsftDiscFormat2RawCD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6af0-131">Track-at-Once-bildwriter.</span><span class="sxs-lookup"><span data-stu-id="f6af0-131">Track-At-Once image writer.</span></span>
<ul>
<li><span data-ttu-id="f6af0-132"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-132"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-133"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-133"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-134"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-134"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-135">MsftDiscFormat2TrackAtOnce</span><span class="sxs-lookup"><span data-stu-id="f6af0-135">MsftDiscFormat2TrackAtOnce</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6af0-136">Enumeration von Festplatten Geräten in der System Hardware Liste.</span><span class="sxs-lookup"><span data-stu-id="f6af0-136">Enumeration of disc devices in the system hardware list.</span></span>
<ul>
<li><span data-ttu-id="f6af0-137"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-137"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-138">MsftDiscMaster2</span><span class="sxs-lookup"><span data-stu-id="f6af0-138">MsftDiscMaster2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6af0-139">Benachrichtigungs Delegat für das MsftDiscMaster2-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f6af0-139">Notification delegate for the MsftDiscMaster2 object.</span></span>
<ul>
<li><span data-ttu-id="f6af0-140"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-140"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-141">DDiscMaster2Events</span><span class="sxs-lookup"><span data-stu-id="f6af0-141">DDiscMaster2Events</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6af0-142">Einzelnes Aufzeichnungsgerät.</span><span class="sxs-lookup"><span data-stu-id="f6af0-142">Individual recording device.</span></span>
<ul>
<li><span data-ttu-id="f6af0-143"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-143"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-144"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-144"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-145">MsftDiscRecorder2</span><span class="sxs-lookup"><span data-stu-id="f6af0-145">MsftDiscRecorder2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6af0-146">Geräte Schreib Attribute, einschließlich Medientyp, Schreibgeschwindigkeit und Typ der Angular Velocity-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="f6af0-146">Device writing attributes, including the media type, writing speed, and type of angular velocity control.</span></span>
<ul>
<li><span data-ttu-id="f6af0-147"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>Iwrite-espeeddescriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-147"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-148">Msftschreitespeeddescriptor</span><span class="sxs-lookup"><span data-stu-id="f6af0-148">MsftWriteSpeedDescriptor</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f6af0-149">In der folgenden Tabelle sind die Dateisystem Schnittstellen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6af0-149">The following table lists the file system interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f6af0-150">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f6af0-150">Interface</span></span></td>
<td><span data-ttu-id="f6af0-151">Object</span><span class="sxs-lookup"><span data-stu-id="f6af0-151">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6af0-152">Start Abbild Datenstrom und Eigenschaften für die Integration des Start baren Bilds in das Festplatten Abbild.</span><span class="sxs-lookup"><span data-stu-id="f6af0-152">Boot image stream and properties for integrating the bootable image in the disc image.</span></span>
<ul>
<li><span data-ttu-id="f6af0-153"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>Ibootoptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-153"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-154">Bootoptions</span><span class="sxs-lookup"><span data-stu-id="f6af0-154">BootOptions</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6af0-155">Dateisystem Abbild und-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f6af0-155">File system image and properties.</span></span> <span data-ttu-id="f6af0-156">Dieses Objekt enthält alle Spuren und Verweise auf das Startimage und das Ergebnisbild.</span><span class="sxs-lookup"><span data-stu-id="f6af0-156">This object includes all tracks, and references to the boot image and result image.</span></span>
<ul>
<li><span data-ttu-id="f6af0-157"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>Dfilesystemmageevents</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-157"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-158"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>Dfilesystemimageimportevents</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-158"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-159"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>Ifilesystemimage</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-159"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-160"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-160"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-161"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-161"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-162">Cfilesystemimage</span><span class="sxs-lookup"><span data-stu-id="f6af0-162">CFileSystemImage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6af0-163">Der Container des Datenstroms, der vom Dateisystem Objekt bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f6af0-163">Container of the data stream provided by the file system object.</span></span>
<ul>
<li><span data-ttu-id="f6af0-164"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>Ifilesystemimageresult</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-164"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-165">Filesystemimageresult</span><span class="sxs-lookup"><span data-stu-id="f6af0-165">FileSystemImageResult</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6af0-166">Verzeichnis Element im Dateisystem Abbild.</span><span class="sxs-lookup"><span data-stu-id="f6af0-166">Directory item in the file system image.</span></span>
<ul>
<li><span data-ttu-id="f6af0-167"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>Ifsidirectoriyitem</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-167"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-168"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-168"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-169">"F"</span><span class="sxs-lookup"><span data-stu-id="f6af0-169">FsiDirectoryItem</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6af0-170">Datei Element im Dateisystem Abbild.</span><span class="sxs-lookup"><span data-stu-id="f6af0-170">File item in the file system image.</span></span>
<ul>
<li><span data-ttu-id="f6af0-171"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>Ifsifleitem</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-171"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-172"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-172"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-173">Fsifleitem</span><span class="sxs-lookup"><span data-stu-id="f6af0-173">FsiFileItem</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6af0-174">Schnittstelle, die Eigenschaften enthält, die für Datei-und Verzeichnis Elemente gemeinsam sind</span><span class="sxs-lookup"><span data-stu-id="f6af0-174">Interface containing properties common to both file and directory items.</span></span>
<ul>
<li><span data-ttu-id="f6af0-175"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>Ifsiitem</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-175"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-176">"F"</span><span class="sxs-lookup"><span data-stu-id="f6af0-176">FsiItem</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6af0-177">Rohdaten-CD-Image Erstellung.</span><span class="sxs-lookup"><span data-stu-id="f6af0-177">RAW CD image creation.</span></span>
<ul>
<li><span data-ttu-id="f6af0-178"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>Irawcdimagecreator</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-178"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-179"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>Irawcdimagetrackinfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-179"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-180">Msctrawcdimagecreator</span><span class="sxs-lookup"><span data-stu-id="f6af0-180">MsftRawCDImageCreator</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6af0-181">Objekt-Hilfsobjekt zum Verketten mehrerer Streams.</span><span class="sxs-lookup"><span data-stu-id="f6af0-181">Stream object helper object to concatenate multiple streams.</span></span>
<ul>
<li><span data-ttu-id="f6af0-182"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>Istreamconcatenate</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-182"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-183">Msftstreamconcatenate</span><span class="sxs-lookup"><span data-stu-id="f6af0-183">MsftStreamConcatenate</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6af0-184">Der überlappende Stream, der dem Festplatten Abbild hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6af0-184">Interleaved stream to add to the disc image.</span></span>
<ul>
<li><span data-ttu-id="f6af0-185"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>Istreaminterleave</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-185"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-186">Msftstreaminterleave</span><span class="sxs-lookup"><span data-stu-id="f6af0-186">MsftStreamInterleave</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6af0-187">Pseudo zufälliger generierter Stream.</span><span class="sxs-lookup"><span data-stu-id="f6af0-187">Pseudo-random generated stream.</span></span>
<ul>
<li><span data-ttu-id="f6af0-188"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>Istreampseudorandombased</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-188"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-189">MsftStreamPrgn001</span><span class="sxs-lookup"><span data-stu-id="f6af0-189">MsftStreamPrgn001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6af0-190">Das Skript Objekt <strong>msftstreamzero</strong> ist nicht als Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="f6af0-190">The <strong>MsftStreamZero</strong> scripting object is not implemented as an interface.</span></span></td>
<td><span data-ttu-id="f6af0-191"><a href="msftstreamzero.md"><strong>Msftstreamzero</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-191"><a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f6af0-192">In der folgenden Tabelle sind hilfsschnittstellen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f6af0-192">The following table lists helper interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f6af0-193">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f6af0-193">Interface</span></span></td>
<td><span data-ttu-id="f6af0-194">Object</span><span class="sxs-lookup"><span data-stu-id="f6af0-194">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6af0-195">Sammlung von sektorbereichen innerhalb eines Dateisystem Images.</span><span class="sxs-lookup"><span data-stu-id="f6af0-195">Collection of sector ranges within a file system image.</span></span>
<ul>
<li><span data-ttu-id="f6af0-196"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>Iblockrange</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-196"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-197"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>Iblockrangelist</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-197"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-198">Kein entsprechendes Objekt</span><span class="sxs-lookup"><span data-stu-id="f6af0-198">No corresponding object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6af0-199">Unterstützung der Verbrauchs Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="f6af0-199">Burn verification support.</span></span>
<ul>
<li><span data-ttu-id="f6af0-200"><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>Iburnverification</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-200"><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>IBurnVerification</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-201">Kein entsprechendes Objekt</span><span class="sxs-lookup"><span data-stu-id="f6af0-201">No corresponding object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6af0-202">Enumerator von "ssiitems" für C/C++-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="f6af0-202">Enumerator of FsiItems for C/C++ applications.</span></span>
<ul>
<li><span data-ttu-id="f6af0-203"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>Ienumssiitems</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-203"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-204">Enummamaitems</span><span class="sxs-lookup"><span data-stu-id="f6af0-204">EnumFsiItems</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6af0-205">Enumerator von progressitems für C/C++-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="f6af0-205">Enumerator of ProgressItems for C/C++ applications.</span></span>
<ul>
<li><span data-ttu-id="f6af0-206"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>Ienumprogressitems</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-206"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-207">Enumprogressitems</span><span class="sxs-lookup"><span data-stu-id="f6af0-207">EnumProgressItems</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="f6af0-208"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>Ifsinamedstreams</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-208"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-209">FsiFileItem2</span><span class="sxs-lookup"><span data-stu-id="f6af0-209">FsiFileItem2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6af0-210">Unterstützung der ISO-Abbild Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="f6af0-210">.iso image verification support.</span></span>
<ul>
<li><span data-ttu-id="f6af0-211"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>Iisoimagemanager</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-211"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-212">Kein entsprechendes Objekt</span><span class="sxs-lookup"><span data-stu-id="f6af0-212">No corresponding object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6af0-213">Unterstützung mehrerer Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="f6af0-213">Multiple session support.</span></span>
<ul>
<li><span data-ttu-id="f6af0-214"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>Imultisession</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-214"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-215">Kein entsprechendes Objekt</span><span class="sxs-lookup"><span data-stu-id="f6af0-215">No corresponding object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6af0-216">Sequenzielle Unterstützung mehrerer Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="f6af0-216">Sequential multiple session support.</span></span>
<ul>
<li><span data-ttu-id="f6af0-217"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>Imultisessionsequential</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-217"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></span></span></li>
<li><span data-ttu-id="f6af0-218"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-218"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-219">Msftmultisessionsequential</span><span class="sxs-lookup"><span data-stu-id="f6af0-219">MsftMultisessionSequential</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6af0-220">Der Dateiname und die zugehörigen Blöcke im Ergebnisbild.</span><span class="sxs-lookup"><span data-stu-id="f6af0-220">File name and associated blocks in the result image.</span></span>
<ul>
<li><span data-ttu-id="f6af0-221"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>Iprogressitem</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-221"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-222">Progressitem</span><span class="sxs-lookup"><span data-stu-id="f6af0-222">ProgressItem</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6af0-223">Ergebnis Bildliste, aufgeschlüsselt nach Dateiname und zugeordneten Blöcken.</span><span class="sxs-lookup"><span data-stu-id="f6af0-223">Result image listing, broken down by file name and associated blocks.</span></span>
<ul>
<li><span data-ttu-id="f6af0-224"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>Iprogressitems</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6af0-224"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="f6af0-225">Progressitems</span><span class="sxs-lookup"><span data-stu-id="f6af0-225">ProgressItems</span></span></td>
</tr>
</tbody>
</table>



 

 

 




