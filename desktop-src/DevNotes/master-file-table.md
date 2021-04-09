---
description: Die Master Dateitabelle (MFT) speichert die Informationen, die erforderlich sind, um Dateien aus einer NTFS-Partition abzurufen.
ms.assetid: 673fb4d0-7b6f-44fe-bfd6-1962e14ccdf5
title: Master Dateitabelle (Entwickler Hinweise)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae8656a44b6dadd7d4ff601ddc64623935f5881
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958167"
---
# <a name="master-file-table"></a><span data-ttu-id="222a2-103">Master Dateitabelle</span><span class="sxs-lookup"><span data-stu-id="222a2-103">Master File Table</span></span>

<span data-ttu-id="222a2-104">\[Dieses Dokument gilt nur für Version 3 von NTFS-Volumes.\]</span><span class="sxs-lookup"><span data-stu-id="222a2-104">\[This document applies only to version 3 of NTFS volumes.\]</span></span>

<span data-ttu-id="222a2-105">Die Master Dateitabelle (MFT) speichert die Informationen, die erforderlich sind, um Dateien aus einer NTFS-Partition abzurufen.</span><span class="sxs-lookup"><span data-stu-id="222a2-105">The master file table (MFT) stores the information required to retrieve files from an NTFS partition.</span></span>

<span data-ttu-id="222a2-106">Eine Datei kann über einen oder mehrere MFT-Einträge verfügen und ein oder mehrere Attribute enthalten.</span><span class="sxs-lookup"><span data-stu-id="222a2-106">A file may have one or more MFT records, and can contain one or more attributes.</span></span> <span data-ttu-id="222a2-107">In NTFS ist ein Datei Verweis der MFT-Segment Verweis auf den Basisdatei Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="222a2-107">In NTFS, a file reference is the MFT segment reference of the base file record.</span></span> <span data-ttu-id="222a2-108">Weitere Informationen finden Sie unter [**\_ \_ Referenz zu MFT-Segmenten**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="222a2-108">For more information, see [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

<span data-ttu-id="222a2-109">Die MFT enthält Datei Daten Satz Segmente. die ersten 16 dieser sind für spezielle Dateien reserviert, z. b. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="222a2-109">The MFT contains file record segments; the first 16 of these are reserved for special files, such as the following:</span></span>

-   <span data-ttu-id="222a2-110">0: MFT ($MFT)</span><span class="sxs-lookup"><span data-stu-id="222a2-110">0: MFT ($Mft)</span></span>
-   <span data-ttu-id="222a2-111">5: Stammverzeichnis ( \\ )</span><span class="sxs-lookup"><span data-stu-id="222a2-111">5: root directory (\\)</span></span>
-   <span data-ttu-id="222a2-112">6: volumecluster-Zuordnungs Datei ($Bitmap)</span><span class="sxs-lookup"><span data-stu-id="222a2-112">6: volume cluster allocation file ($Bitmap)</span></span>
-   <span data-ttu-id="222a2-113">8: fehlerhafte Cluster Datei ($BadClus)</span><span class="sxs-lookup"><span data-stu-id="222a2-113">8: bad-cluster file ($BadClus)</span></span>

<span data-ttu-id="222a2-114">Jedes Datei Daten Satz Segment beginnt mit einem Datei Daten Satz Segment-Header.</span><span class="sxs-lookup"><span data-stu-id="222a2-114">Each file record segment starts with a file record segment header.</span></span> <span data-ttu-id="222a2-115">Weitere Informationen finden Sie unter [**Header des Datei \_ Daten Satz \_ Segments \_**](file-record-segment-header.md).</span><span class="sxs-lookup"><span data-stu-id="222a2-115">For more information, see [**FILE\_RECORD\_SEGMENT\_HEADER**](file-record-segment-header.md).</span></span> <span data-ttu-id="222a2-116">Auf jedes Datei Daten Satz Segment folgt mindestens ein Attribut.</span><span class="sxs-lookup"><span data-stu-id="222a2-116">Each file record segment is followed by one or more attributes.</span></span> <span data-ttu-id="222a2-117">Jedes Attribut beginnt mit einem Attributdaten Satz Header.</span><span class="sxs-lookup"><span data-stu-id="222a2-117">Each attribute starts with an attribute record header.</span></span> <span data-ttu-id="222a2-118">Weitere Informationen finden Sie unter [**Attribut \_ Daten Satz \_ Header**](attribute-record-header.md).</span><span class="sxs-lookup"><span data-stu-id="222a2-118">For more information, see [**ATTRIBUTE\_RECORD\_HEADER**](attribute-record-header.md).</span></span> <span data-ttu-id="222a2-119">Der Attributdaten Satz enthält den Attributtyp (z. b. $Data oder $Bitmap), einen optionalen Namen und den Attribut Wert.</span><span class="sxs-lookup"><span data-stu-id="222a2-119">The attribute record includes the attribute type (such as $DATA or $BITMAP), an optional name, and the attribute value.</span></span> <span data-ttu-id="222a2-120">Der Benutzerdaten Strom ist ein Attribut, ebenso wie alle Datenströme.</span><span class="sxs-lookup"><span data-stu-id="222a2-120">The user data stream is an attribute, as are all streams.</span></span> <span data-ttu-id="222a2-121">Die Attribut Liste wird mit 0xFFFFFFFF ($End) beendet.</span><span class="sxs-lookup"><span data-stu-id="222a2-121">The attribute list is terminated with 0xFFFFFFFF ($END).</span></span>

<span data-ttu-id="222a2-122">Im folgenden finden Sie einige Beispiel Attribute.</span><span class="sxs-lookup"><span data-stu-id="222a2-122">The following are some example attributes.</span></span>

-   <span data-ttu-id="222a2-123">Die $MFT Datei enthält ein unbenanntes $Data Attribut, bei dem es sich um die Reihenfolge der MFT-Daten Satz Segmente handelt.</span><span class="sxs-lookup"><span data-stu-id="222a2-123">The $Mft file contains an unnamed $DATA attribute that is the sequence of MFT record segments, in order.</span></span>
-   <span data-ttu-id="222a2-124">Die $MFT Datei enthält ein unbenanntes $Bitmap Attribut, das angibt, welche MFT-Datensätze verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="222a2-124">The $Mft file contains an unnamed $BITMAP attribute that indicates which MFT records are in use.</span></span>
-   <span data-ttu-id="222a2-125">Die $Bitmap Datei enthält ein unbenanntes $Data Attribut, das angibt, welche Cluster verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="222a2-125">The $Bitmap file contains an unnamed $DATA attribute that indicates which clusters are in use.</span></span>
-   <span data-ttu-id="222a2-126">Die $BadClus Datei enthält ein $Data Attribut mit dem Namen $Bad, das einen Eintrag enthält, der jedem fehlerhaften Cluster entspricht.</span><span class="sxs-lookup"><span data-stu-id="222a2-126">The $BadClus file contains a $DATA attribute named $BAD that contains an entry that corresponds to each bad cluster.</span></span>

<span data-ttu-id="222a2-127">Wenn kein Speicherplatz mehr für das Speichern von Attributen im Datei Daten Satz Segment vorhanden ist, werden zusätzliche Datei Daten Satz Segmente zugeordnet und in das erste (oder Basis-) Datei Daten Satz Segment in einem Attribut eingefügt, das als Attribut Liste bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="222a2-127">When there is no more space for storing attributes in the file record segment, additional file record segments are allocated and inserted in the first (or base) file record segment in an attribute called the attribute list.</span></span> <span data-ttu-id="222a2-128">Die Attribut Liste gibt an, wo sich die einzelnen Attribute befinden, die der Datei zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="222a2-128">The attribute list indicates where each attribute associated with the file can be found.</span></span> <span data-ttu-id="222a2-129">Dies schließt alle Attribute im Basisdatei Daten Satz ein, mit Ausnahme der Attribut Liste selbst.</span><span class="sxs-lookup"><span data-stu-id="222a2-129">This includes all attributes in the base file record, except for the attribute list itself.</span></span> <span data-ttu-id="222a2-130">Weitere Informationen finden Sie unter [**Attribut \_ Listen \_ Eintrag**](attribute-list-entry.md).</span><span class="sxs-lookup"><span data-stu-id="222a2-130">For more information, see [**ATTRIBUTE\_LIST\_ENTRY**](attribute-list-entry.md).</span></span>

<span data-ttu-id="222a2-131">Zu den zu MFT Gehör Ende Strukturen gehören die folgenden:</span><span class="sxs-lookup"><span data-stu-id="222a2-131">Structures related to the MFT include the following:</span></span>

-   [<span data-ttu-id="222a2-132">**Attribut \_ Listen \_ Eintrag**</span><span class="sxs-lookup"><span data-stu-id="222a2-132">**ATTRIBUTE\_LIST\_ENTRY**</span></span>](attribute-list-entry.md)
-   [<span data-ttu-id="222a2-133">**Attribut \_ Daten Satz \_ Header**</span><span class="sxs-lookup"><span data-stu-id="222a2-133">**ATTRIBUTE\_RECORD\_HEADER**</span></span>](attribute-record-header.md)
-   [<span data-ttu-id="222a2-134">**\_Dateiname**</span><span class="sxs-lookup"><span data-stu-id="222a2-134">**FILE\_NAME**</span></span>](file-name.md)
-   [<span data-ttu-id="222a2-135">**Header des Datei \_ Daten Satz \_ Segments \_**</span><span class="sxs-lookup"><span data-stu-id="222a2-135">**FILE\_RECORD\_SEGMENT\_HEADER**</span></span>](file-record-segment-header.md)
-   [<span data-ttu-id="222a2-136">**MFT- \_ Segment \_ Verweis**</span><span class="sxs-lookup"><span data-stu-id="222a2-136">**MFT\_SEGMENT\_REFERENCE**</span></span>](mft-segment-reference.md)
-   [<span data-ttu-id="222a2-137">**\_ \_ multisektorheader**</span><span class="sxs-lookup"><span data-stu-id="222a2-137">**MULTI\_SECTOR\_HEADER**</span></span>](multi-sector-header.md)
-   [<span data-ttu-id="222a2-138">**Standard \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="222a2-138">**STANDARD\_INFORMATION**</span></span>](standard-information.md)

## <a name="related-topics"></a><span data-ttu-id="222a2-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="222a2-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="222a2-140">[Technische Referenz zu NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="222a2-140">[NTFS Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span></span>
</dt> </dl>

 

 
