---
title: Datenträger
description: IMAPI unterstützt die drei Dateisystem Formate ISO 9660, Joliet und UDF.
ms.assetid: 9cd782c0-203b-452c-9d04-3464d39453b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9b4d4c5c5b6aa3e0c4c96598486a531c297b61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310084"
---
# <a name="disc-formats"></a><span data-ttu-id="db881-103">Datenträger</span><span class="sxs-lookup"><span data-stu-id="db881-103">Disc Formats</span></span>

<span data-ttu-id="db881-104">IMAPI unterstützt drei Dateisystem Formate: [ISO 9660](#iso-9660), [Joliet](#joliet)und [UDF](#universal-disk-format-udf).</span><span class="sxs-lookup"><span data-stu-id="db881-104">IMAPI supports three file system formats: [ISO 9660](#iso-9660), [Joliet](#joliet), and [UDF](#universal-disk-format-udf).</span></span>

## <a name="iso-9660"></a><span data-ttu-id="db881-105">ISO 9660</span><span class="sxs-lookup"><span data-stu-id="db881-105">ISO 9660</span></span>

<span data-ttu-id="db881-106">Das ISO 9660-Format ist das ursprüngliche Standarddatei System für CD-Datenscheiben.</span><span class="sxs-lookup"><span data-stu-id="db881-106">The ISO 9660 format is the original standard file system for CD data discs.</span></span> <span data-ttu-id="db881-107">Das Format wird auf verschiedenen Betriebssystemen erkannt, einschließlich MSDOS, der Mac OS, UNIX und des Windows-Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="db881-107">The format is recognized on several operating systems, including MSDOS, the Mac OS, UNIX, and the Windows operating system.</span></span> <span data-ttu-id="db881-108">Das ISO 9660-Format wird vom internationale Organisation für Normung (ISO) veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="db881-108">The ISO 9660 format is published by the International Organization for Standardization (ISO).</span></span>

<span data-ttu-id="db881-109">Das Format beginnt bei Sektor 16 mit dem volumeheader CD0001; der Rest des Headers folgt.</span><span class="sxs-lookup"><span data-stu-id="db881-109">The format begins at sector 16 with the volume header, CD0001; the remainder of the header follows.</span></span> <span data-ttu-id="db881-110">Andere abgeleitete Formate beginnen auch bei Sektor 16, aber verwenden eine andere Zeichenfolge für den volumeheader.</span><span class="sxs-lookup"><span data-stu-id="db881-110">Other derived formats also begin at sector 16, but use another string for the volume header.</span></span> <span data-ttu-id="db881-111">Beispielsweise verwenden hohe Sierra Disks die Zeichenfolge CD-ROM0001 und das interaktive Format Compact Disc verwendet CD-I0001.</span><span class="sxs-lookup"><span data-stu-id="db881-111">For example, High Sierra discs use the string CD-ROM0001 and Compact Disc Interactive format uses CD-I0001.</span></span>

<span data-ttu-id="db881-112">Der-Header verweist auf die Bereiche der Festplatte, die die Dateinamen im ISO 9660-Format speichern.</span><span class="sxs-lookup"><span data-stu-id="db881-112">The header points to areas of the disc that store the file names in ISO 9660 format.</span></span> <span data-ttu-id="db881-113">Die Benennungs Konvention für Dateien und Verzeichnisse besteht aus 8 Zeichen, einem Zeitraum und 3 weiteren Zeichen.</span><span class="sxs-lookup"><span data-stu-id="db881-113">The file and directory naming convention consists of 8 characters, a period, and 3 more characters.</span></span> <span data-ttu-id="db881-114">Dabei handelt es sich um die gleiche Namenskonvention, die vom MSDOS-Betriebssystem verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db881-114">This is the same naming convention used by the MSDOS operating system.</span></span>

<span data-ttu-id="db881-115">Weitere Dateisystem Header können für Formate wie Joliet und UDF auf einem Datenträger nebeneinander vorhanden sein, ohne dass sich dies auf die Lesbarkeit des ISO 9660-Formats auswirkt.</span><span class="sxs-lookup"><span data-stu-id="db881-115">Additional file system headers, for formats such as Joliet and UDF, can co-exist on a disc without affecting the readability of the ISO 9660 format.</span></span> <span data-ttu-id="db881-116">Nach den Indizes belegt ein Satz von Datendateien die Festplatte. Die Indizes für die einzelnen Dateisysteme verweisen unabhängig auf Datendateien auf der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="db881-116">After the indexes, a set of data files occupy the disc. The indexes for each file system independently reference data files on the disc.</span></span>

<span data-ttu-id="db881-117">Die Spezifikation ISO 9660 definiert drei Ebenen des Formats:</span><span class="sxs-lookup"><span data-stu-id="db881-117">The ISO 9660 specification defines three levels of the format:</span></span>

-   <span data-ttu-id="db881-118">Ebene 1 definiert Dateinamen, um das 8,3-Zeichenformat zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="db881-118">Level 1 defines file names to use the 8.3 character format.</span></span>
-   <span data-ttu-id="db881-119">Auf Ebene 2 sind längere Dateinamen zulässig, die auf DOS 6. xx-, Macintosh-und UNIX-Plattformen zu finden sind.</span><span class="sxs-lookup"><span data-stu-id="db881-119">Level 2 permits longer file names, as found on DOS 6.xx, MacIntosh, and UNIX platforms.</span></span>
-   <span data-ttu-id="db881-120">Ebene 3 ermöglicht überlappende Daten und Audiodateien, um die Abruf Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="db881-120">Level 3 allows interleaved data and audio files to improve retrieval (playback) performance.</span></span> <span data-ttu-id="db881-121">Diese Ebene entfernt auch das Limit von 2 GB.</span><span class="sxs-lookup"><span data-stu-id="db881-121">This level also removes the 2GB file limit.</span></span> <span data-ttu-id="db881-122">Diese Ebene wird von der Image-Mastering-API **nicht** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db881-122">This level is **not** supported by the Image Mastering API.</span></span>

<span data-ttu-id="db881-123">DVD-CDs können auch ISO 9660 verwenden; das UDF-Dateisystem ist jedoch das gängigste Dateisystem, das mit DVD-Medien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db881-123">DVD discs can also use ISO 9660; however, the UDF file system is the most prevalent file system used with DVD media.</span></span>

## <a name="joliet"></a><span data-ttu-id="db881-124">Joliet</span><span class="sxs-lookup"><span data-stu-id="db881-124">Joliet</span></span>

<span data-ttu-id="db881-125">Das Joliet-Format ist eine Ableitung von ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="db881-125">The Joliet format is a derivative of ISO 9660.</span></span> <span data-ttu-id="db881-126">Dieses Format schreibt den Joliet-Dateisystem Index zusätzlich zum ISO 9660-Dateisystem Index in das Festplatten Abbild.</span><span class="sxs-lookup"><span data-stu-id="db881-126">This format writes the Joliet file system index to the disc image in addition to the ISO 9660 file system index.</span></span>

<span data-ttu-id="db881-127">Der Joliet-Index bietet die folgenden Verbesserungen am Dateisystem Index:</span><span class="sxs-lookup"><span data-stu-id="db881-127">The Joliet index provides the following improvements to the file system index:</span></span>

-   <span data-ttu-id="db881-128">Erkennt lange Dateinamen mit bis zu 32 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="db881-128">Recognizes long file names up to 32 characters.</span></span>
-   <span data-ttu-id="db881-129">Unterscheidet zwischen Groß-und Kleinbuchstaben in den Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="db881-129">Distinguishes between upper and lower case letters in the file names.</span></span>
-   <span data-ttu-id="db881-130">Unterstützt Unicode-Zeichen im Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="db881-130">Supports Unicode characters in the filename.</span></span>

<span data-ttu-id="db881-131">Der Joliet-Format Header beginnt in Sektor 17 der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="db881-131">The Joliet format header begins at sector 17 of the disc.</span></span>

<span data-ttu-id="db881-132">Da das Joliet-Format das ISO 9660-Dateisystem auf einem Datenträger beibehält, wird die Kompatibilität mit ISO 9660-kompatiblen Geräten beibehalten.</span><span class="sxs-lookup"><span data-stu-id="db881-132">Because the Joliet format preserves the ISO 9660 file system on a disc, compatibility with ISO 9660-compliant devices is retained.</span></span>

## <a name="universal-disk-format-udf"></a><span data-ttu-id="db881-133">Universal Disk Format (UDF)</span><span class="sxs-lookup"><span data-stu-id="db881-133">Universal Disk Format (UDF)</span></span>

<span data-ttu-id="db881-134">Das Universal Disk Format (UDF) ist ein neueres Dateisystem, das von der optischen Speichertechnologie Zuordnung (OSTA) für optische Medien entwickelt wurde.</span><span class="sxs-lookup"><span data-stu-id="db881-134">The Universal Disk Format (UDF) is a newer file system developed for optical media by the Optical Storage Technology Association (OSTA).</span></span> <span data-ttu-id="db881-135">UDF ist ein tragbares Format, das von mehreren Betriebssystemen erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="db881-135">UDF is a portable format that is recognized by several operating systems.</span></span> <span data-ttu-id="db881-136">UDF ersetzt ISO 9660 als neuen Standard, insbesondere bei Lese-/schreibmedien.</span><span class="sxs-lookup"><span data-stu-id="db881-136">UDF is replacing ISO 9660 as the new standard, especially with read/write media.</span></span>

<span data-ttu-id="db881-137">UDF bietet folgende Features:</span><span class="sxs-lookup"><span data-stu-id="db881-137">Features of UDF include the following:</span></span>

-   <span data-ttu-id="db881-138">Unterstützt Medien mit einer Größe von bis zu 2 TB.</span><span class="sxs-lookup"><span data-stu-id="db881-138">Supports media up to 2TB in size.</span></span>
-   <span data-ttu-id="db881-139">Unterstützt Flash Medien, Iomega-und CD-MRW-Scheiben.</span><span class="sxs-lookup"><span data-stu-id="db881-139">Supports flash media, Iomega REV discs, and CD-MRW discs.</span></span>
-   <span data-ttu-id="db881-140">Speichert Dateien, die kleiner als 2 KB sind, im Datei Eintrags Block.</span><span class="sxs-lookup"><span data-stu-id="db881-140">Stores files less than 2 KB in length in the File Entry block.</span></span>
-   <span data-ttu-id="db881-141">Unterstützt Dateien mit bis zu 2 TB mit Dateinamen, die länger als 255 Zeichen sind.</span><span class="sxs-lookup"><span data-stu-id="db881-141">Supports files up to 2TB with filenames as long as 255 characters.</span></span>
-   <span data-ttu-id="db881-142">Unterstützt einen umfangreichen Satz von Dateiattributen, die für verschiedene Betriebssysteme geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="db881-142">Supports a rich set of file attributes that suit various operating systems.</span></span>
-   <span data-ttu-id="db881-143">Unterstützt ein Bridge Format, bei dem sich alle Formate von ISO 9660, Joliet und UDF auf derselben Festplatte befinden. Diese wird in Videoanwendungen wie DVD-Video, DVD + VR und DVD-VR verwendet.</span><span class="sxs-lookup"><span data-stu-id="db881-143">Supports a bridge format where ISO 9660, Joliet, and UDF formats all reside on the same disc. This is used in video applications, such as DVD-Video, DVD+VR, and DVD-VR.</span></span>
-   <span data-ttu-id="db881-144">Unterstützt benannte Streams und "Echt Zeit Dateien".</span><span class="sxs-lookup"><span data-stu-id="db881-144">Supports named streams and 'Real-Time' files.</span></span>

 

 




