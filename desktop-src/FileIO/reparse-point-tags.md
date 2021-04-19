---
description: Jeder Analyse Punkt verfügt über ein bezeichnertag, sodass Sie effizient zwischen den verschiedenen Arten von Analyse Punkten unterscheiden können, ohne die benutzerdefinierten Daten im Analyse Punkt untersuchen zu müssen.
ms.assetid: d02a2f50-d374-4149-bc04-49b7db052f62
title: Analyse Punkt Tags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a53b65034347e2a2c07afcd6c1f03e31f73cef7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350379"
---
# <a name="reparse-point-tags"></a><span data-ttu-id="b07e2-103">Analyse Punkt Tags</span><span class="sxs-lookup"><span data-stu-id="b07e2-103">Reparse Point Tags</span></span>

<span data-ttu-id="b07e2-104">Jeder Analyse Punkt verfügt über ein bezeichnertag, sodass Sie effizient zwischen den verschiedenen Arten von Analyse Punkten unterscheiden können, ohne die benutzerdefinierten Daten im Analyse Punkt untersuchen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="b07e2-104">Each reparse point has an identifier tag so that you can efficiently differentiate between the different types of reparse points, without having to examine the user-defined data in the reparse point.</span></span> <span data-ttu-id="b07e2-105">Das System verwendet eine Reihe von vordefinierten Tags und einen für Microsoft reservierten Bereich von Tags.</span><span class="sxs-lookup"><span data-stu-id="b07e2-105">The system uses a set of predefined tags and a range of tags reserved for Microsoft.</span></span> <span data-ttu-id="b07e2-106">Wenn Sie einen der reservierten Tags verwenden, wenn Sie einen Analyse Punkt festlegen, schlägt der Vorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="b07e2-106">If you use any of the reserved tags when setting a reparse point, the operation fails.</span></span> <span data-ttu-id="b07e2-107">Tags, die nicht in diesen Bereichen enthalten sind, sind nicht reserviert und sind für Ihre Anwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b07e2-107">Tags not included in these ranges are not reserved and are available for your application.</span></span>

<span data-ttu-id="b07e2-108">Wenn Sie einen Analyse Punkt festlegen, müssen Sie die Daten markieren, die im Analyse Punkt platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b07e2-108">When you set a reparse point, you must tag the data to be placed in the reparse point.</span></span> <span data-ttu-id="b07e2-109">Nachdem der Analyse Punkt festgelegt wurde, schlägt ein neuer Set-Vorgang fehl, wenn das Tag für die neuen Daten nicht mit dem Tag für die vorhandenen Daten identisch ist.</span><span class="sxs-lookup"><span data-stu-id="b07e2-109">After the reparse point has been established, a new set operation fails if the tag for the new data does not match the tag for the existing data.</span></span> <span data-ttu-id="b07e2-110">Wenn die Tags Stimmen, überschreibt der Set-Vorgang den vorhandenen Analyse Punkt.</span><span class="sxs-lookup"><span data-stu-id="b07e2-110">If the tags match, the set operation overwrites the existing reparse point.</span></span>

<span data-ttu-id="b07e2-111">Um das Analyse Punkt-Tag abzurufen, verwenden Sie die [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b07e2-111">To retrieve the reparse point tag, use the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) function.</span></span> <span data-ttu-id="b07e2-112">Wenn das Element **dwfileattribute** das Attribut "File Attribute Analyse **\_ \_ \_ Point** " enthält, gibt das **dwReserved0** -Element den Analyse Punkt an.</span><span class="sxs-lookup"><span data-stu-id="b07e2-112">If the **dwFileAttributes** member includes the **FILE\_ATTRIBUTE\_REPARSE\_POINT** attribute, then the **dwReserved0** member specifies the reparse point.</span></span>

## <a name="tag-contents"></a><span data-ttu-id="b07e2-113">Taginhalt</span><span class="sxs-lookup"><span data-stu-id="b07e2-113">Tag Contents</span></span>

<span data-ttu-id="b07e2-114">Analyse Tags werden als **DWORD** -Werte gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b07e2-114">Reparse tags are stored as **DWORD** values.</span></span> <span data-ttu-id="b07e2-115">Die Bits definieren bestimmte Attribute, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b07e2-115">The bits define certain attributes, as shown in the following diagram.</span></span>

``` syntax
   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
  +-+-+-+-+-----------------------+-------------------------------+
  |M|R|N|R|     Reserved bits     |      Reparse tag value        |
  +-+-+-+-+-----------------------+-------------------------------+
```

<span data-ttu-id="b07e2-116">Die unteren 16 Bits bestimmen die Art des Analyse Punkts.</span><span class="sxs-lookup"><span data-stu-id="b07e2-116">The low 16 bits determine the kind of reparse point.</span></span> <span data-ttu-id="b07e2-117">Die hohen 16 Bits verfügen über 12 Bits, die für die zukünftige Verwendung reserviert sind, und 4 Bits, die bestimmte Attribute der Tags und die durch den Analyse Punkt dargestellten Daten kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="b07e2-117">The high 16 bits have 12 bits reserved for future use and 4 bits that denote specific attributes of the tags and the data represented by the reparse point.</span></span> <span data-ttu-id="b07e2-118">In der folgenden Tabelle werden diese Bits beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b07e2-118">The following table describes these bits.</span></span>



| <span data-ttu-id="b07e2-119">bit</span><span class="sxs-lookup"><span data-stu-id="b07e2-119">Bit</span></span> | <span data-ttu-id="b07e2-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b07e2-120">Description</span></span>                                                                                                  |
|-----|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b07e2-121">M</span><span class="sxs-lookup"><span data-stu-id="b07e2-121">M</span></span>   | <span data-ttu-id="b07e2-122">Microsoft-Bit.</span><span class="sxs-lookup"><span data-stu-id="b07e2-122">Microsoft bit.</span></span> <span data-ttu-id="b07e2-123">Wenn dieses Bit festgelegt ist, befindet sich das Tag im Besitz von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b07e2-123">If this bit is set, the tag is owned by Microsoft.</span></span> <span data-ttu-id="b07e2-124">Alle anderen Tags müssen für dieses Bit 0 (null) verwenden.</span><span class="sxs-lookup"><span data-stu-id="b07e2-124">All other tags must use zero for this bit.</span></span> |
| <span data-ttu-id="b07e2-125">R</span><span class="sxs-lookup"><span data-stu-id="b07e2-125">R</span></span>   | <span data-ttu-id="b07e2-126">Bleiben muss für alle nicht-Microsoft-Tags NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b07e2-126">Reserved; must be zero for all non-Microsoft tags.</span></span>                                                           |
| <span data-ttu-id="b07e2-127">N</span><span class="sxs-lookup"><span data-stu-id="b07e2-127">N</span></span>   | <span data-ttu-id="b07e2-128">Name Ersatz Zeichen Bit.</span><span class="sxs-lookup"><span data-stu-id="b07e2-128">Name surrogate bit.</span></span> <span data-ttu-id="b07e2-129">Wenn dieses Bit festgelegt ist, stellt die Datei oder das Verzeichnis eine andere benannte Entität im System dar.</span><span class="sxs-lookup"><span data-stu-id="b07e2-129">If this bit is set, the file or directory represents another named entity in the system.</span></span> |



 

<span data-ttu-id="b07e2-130">Die folgenden Makros sind zur Unterstützung beim Testen von Tags vorhanden:</span><span class="sxs-lookup"><span data-stu-id="b07e2-130">The following macros exist to assist in testing tags:</span></span>

-   [<span data-ttu-id="b07e2-131">**Isanalyse-tagmicrosoft**</span><span class="sxs-lookup"><span data-stu-id="b07e2-131">**IsReparseTagMicrosoft**</span></span>](/windows/desktop/api/Winnt/nf-winnt-isreparsetagmicrosoft)
-   [<span data-ttu-id="b07e2-132">**Isreparsetagnamesurrogate**</span><span class="sxs-lookup"><span data-stu-id="b07e2-132">**IsReparseTagNameSurrogate**</span></span>](/windows/desktop/api/Winnt/nf-winnt-isreparsetagnamesurrogate)

<span data-ttu-id="b07e2-133">Jedes Makro gibt einen Wert ungleich NULL zurück, wenn das zugeordnete Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b07e2-133">Each macro returns a nonzero value if the associated bit is set.</span></span>

<span data-ttu-id="b07e2-134">Es folgen die vordefinierten Analyse Tagwerte von Microsoft. Sie sind in "Winnt. h" definiert:</span><span class="sxs-lookup"><span data-stu-id="b07e2-134">The following are Microsoft's predefined reparse tag values; they are defined in WinNT.h:</span></span>

-   <span data-ttu-id="b07e2-135">**IO_REPARSE_TAG_AF_UNIX**</span><span class="sxs-lookup"><span data-stu-id="b07e2-135">**IO_REPARSE_TAG_AF_UNIX**</span></span>
-   <span data-ttu-id="b07e2-136">**IO_REPARSE_TAG_APPEXECLINK**</span><span class="sxs-lookup"><span data-stu-id="b07e2-136">**IO_REPARSE_TAG_APPEXECLINK**</span></span>
-   <span data-ttu-id="b07e2-137">**IO_REPARSE_TAG_CLOUD**</span><span class="sxs-lookup"><span data-stu-id="b07e2-137">**IO_REPARSE_TAG_CLOUD**</span></span>
-   <span data-ttu-id="b07e2-138">**IO_REPARSE_TAG_CLOUD_1**</span><span class="sxs-lookup"><span data-stu-id="b07e2-138">**IO_REPARSE_TAG_CLOUD_1**</span></span>
-   <span data-ttu-id="b07e2-139">**IO_REPARSE_TAG_CLOUD_2**</span><span class="sxs-lookup"><span data-stu-id="b07e2-139">**IO_REPARSE_TAG_CLOUD_2**</span></span>
-   <span data-ttu-id="b07e2-140">**IO_REPARSE_TAG_CLOUD_3**</span><span class="sxs-lookup"><span data-stu-id="b07e2-140">**IO_REPARSE_TAG_CLOUD_3**</span></span>
-   <span data-ttu-id="b07e2-141">**IO_REPARSE_TAG_CLOUD_4**</span><span class="sxs-lookup"><span data-stu-id="b07e2-141">**IO_REPARSE_TAG_CLOUD_4**</span></span>
-   <span data-ttu-id="b07e2-142">**IO_REPARSE_TAG_CLOUD_5**</span><span class="sxs-lookup"><span data-stu-id="b07e2-142">**IO_REPARSE_TAG_CLOUD_5**</span></span>
-   <span data-ttu-id="b07e2-143">**IO_REPARSE_TAG_CLOUD_6**</span><span class="sxs-lookup"><span data-stu-id="b07e2-143">**IO_REPARSE_TAG_CLOUD_6**</span></span>
-   <span data-ttu-id="b07e2-144">**IO_REPARSE_TAG_CLOUD_7**</span><span class="sxs-lookup"><span data-stu-id="b07e2-144">**IO_REPARSE_TAG_CLOUD_7**</span></span>
-   <span data-ttu-id="b07e2-145">**IO_REPARSE_TAG_CLOUD_8**</span><span class="sxs-lookup"><span data-stu-id="b07e2-145">**IO_REPARSE_TAG_CLOUD_8**</span></span>
-   <span data-ttu-id="b07e2-146">**IO_REPARSE_TAG_CLOUD_9**</span><span class="sxs-lookup"><span data-stu-id="b07e2-146">**IO_REPARSE_TAG_CLOUD_9**</span></span>
-   <span data-ttu-id="b07e2-147">**IO_REPARSE_TAG_CLOUD_A**</span><span class="sxs-lookup"><span data-stu-id="b07e2-147">**IO_REPARSE_TAG_CLOUD_A**</span></span>
-   <span data-ttu-id="b07e2-148">**IO_REPARSE_TAG_CLOUD_B**</span><span class="sxs-lookup"><span data-stu-id="b07e2-148">**IO_REPARSE_TAG_CLOUD_B**</span></span>
-   <span data-ttu-id="b07e2-149">**IO_REPARSE_TAG_CLOUD_C**</span><span class="sxs-lookup"><span data-stu-id="b07e2-149">**IO_REPARSE_TAG_CLOUD_C**</span></span>
-   <span data-ttu-id="b07e2-150">**IO_REPARSE_TAG_CLOUD_D**</span><span class="sxs-lookup"><span data-stu-id="b07e2-150">**IO_REPARSE_TAG_CLOUD_D**</span></span>
-   <span data-ttu-id="b07e2-151">**IO_REPARSE_TAG_CLOUD_E**</span><span class="sxs-lookup"><span data-stu-id="b07e2-151">**IO_REPARSE_TAG_CLOUD_E**</span></span>
-   <span data-ttu-id="b07e2-152">**IO_REPARSE_TAG_CLOUD_F**</span><span class="sxs-lookup"><span data-stu-id="b07e2-152">**IO_REPARSE_TAG_CLOUD_F**</span></span>
-   <span data-ttu-id="b07e2-153">**IO_REPARSE_TAG_CLOUD_MASK**</span><span class="sxs-lookup"><span data-stu-id="b07e2-153">**IO_REPARSE_TAG_CLOUD_MASK**</span></span>
-   <span data-ttu-id="b07e2-154">**IO_REPARSE_TAG_CSV**</span><span class="sxs-lookup"><span data-stu-id="b07e2-154">**IO_REPARSE_TAG_CSV**</span></span>
-   <span data-ttu-id="b07e2-155">**IO_REPARSE_TAG_DEDUP**</span><span class="sxs-lookup"><span data-stu-id="b07e2-155">**IO_REPARSE_TAG_DEDUP**</span></span>
-   <span data-ttu-id="b07e2-156">**IO_REPARSE_TAG_DFS**</span><span class="sxs-lookup"><span data-stu-id="b07e2-156">**IO_REPARSE_TAG_DFS**</span></span>
-   <span data-ttu-id="b07e2-157">**IO_REPARSE_TAG_DFSR**</span><span class="sxs-lookup"><span data-stu-id="b07e2-157">**IO_REPARSE_TAG_DFSR**</span></span>
-   <span data-ttu-id="b07e2-158">**IO_REPARSE_TAG_FILE_PLACEHOLDER**</span><span class="sxs-lookup"><span data-stu-id="b07e2-158">**IO_REPARSE_TAG_FILE_PLACEHOLDER**</span></span>
-   <span data-ttu-id="b07e2-159">**IO_REPARSE_TAG_GLOBAL_REPARSE**</span><span class="sxs-lookup"><span data-stu-id="b07e2-159">**IO_REPARSE_TAG_GLOBAL_REPARSE**</span></span>
-   <span data-ttu-id="b07e2-160">**IO_REPARSE_TAG_HSM**</span><span class="sxs-lookup"><span data-stu-id="b07e2-160">**IO_REPARSE_TAG_HSM**</span></span>
-   <span data-ttu-id="b07e2-161">**IO_REPARSE_TAG_HSM2**</span><span class="sxs-lookup"><span data-stu-id="b07e2-161">**IO_REPARSE_TAG_HSM2**</span></span>
-   <span data-ttu-id="b07e2-162">**IO_REPARSE_TAG_MOUNT_POINT**</span><span class="sxs-lookup"><span data-stu-id="b07e2-162">**IO_REPARSE_TAG_MOUNT_POINT**</span></span>
-   <span data-ttu-id="b07e2-163">**IO_REPARSE_TAG_NFS**</span><span class="sxs-lookup"><span data-stu-id="b07e2-163">**IO_REPARSE_TAG_NFS**</span></span>
-   <span data-ttu-id="b07e2-164">**IO_REPARSE_TAG_ONEDRIVE**</span><span class="sxs-lookup"><span data-stu-id="b07e2-164">**IO_REPARSE_TAG_ONEDRIVE**</span></span>
-   <span data-ttu-id="b07e2-165">**IO_REPARSE_TAG_PROJFS**</span><span class="sxs-lookup"><span data-stu-id="b07e2-165">**IO_REPARSE_TAG_PROJFS**</span></span>
-   <span data-ttu-id="b07e2-166">**IO_REPARSE_TAG_PROJFS_TOMBSTONE**</span><span class="sxs-lookup"><span data-stu-id="b07e2-166">**IO_REPARSE_TAG_PROJFS_TOMBSTONE**</span></span>
-   <span data-ttu-id="b07e2-167">**IO_REPARSE_TAG_SIS**</span><span class="sxs-lookup"><span data-stu-id="b07e2-167">**IO_REPARSE_TAG_SIS**</span></span>
-   <span data-ttu-id="b07e2-168">**IO_REPARSE_TAG_STORAGE_SYNC**</span><span class="sxs-lookup"><span data-stu-id="b07e2-168">**IO_REPARSE_TAG_STORAGE_SYNC**</span></span>
-   <span data-ttu-id="b07e2-169">**IO_REPARSE_TAG_SYMLINK**</span><span class="sxs-lookup"><span data-stu-id="b07e2-169">**IO_REPARSE_TAG_SYMLINK**</span></span>
-   <span data-ttu-id="b07e2-170">**IO_REPARSE_TAG_UNHANDLED**</span><span class="sxs-lookup"><span data-stu-id="b07e2-170">**IO_REPARSE_TAG_UNHANDLED**</span></span>
-   <span data-ttu-id="b07e2-171">**IO_REPARSE_TAG_WCI**</span><span class="sxs-lookup"><span data-stu-id="b07e2-171">**IO_REPARSE_TAG_WCI**</span></span>
-   <span data-ttu-id="b07e2-172">**IO_REPARSE_TAG_WCI_1**</span><span class="sxs-lookup"><span data-stu-id="b07e2-172">**IO_REPARSE_TAG_WCI_1**</span></span>
-   <span data-ttu-id="b07e2-173">**IO_REPARSE_TAG_WCI_LINK**</span><span class="sxs-lookup"><span data-stu-id="b07e2-173">**IO_REPARSE_TAG_WCI_LINK**</span></span>
-   <span data-ttu-id="b07e2-174">**IO_REPARSE_TAG_WCI_LINK_1**</span><span class="sxs-lookup"><span data-stu-id="b07e2-174">**IO_REPARSE_TAG_WCI_LINK_1**</span></span>
-   <span data-ttu-id="b07e2-175">**IO_REPARSE_TAG_WCI_TOMBSTONE**</span><span class="sxs-lookup"><span data-stu-id="b07e2-175">**IO_REPARSE_TAG_WCI_TOMBSTONE**</span></span>
-   <span data-ttu-id="b07e2-176">**IO_REPARSE_TAG_WIM**</span><span class="sxs-lookup"><span data-stu-id="b07e2-176">**IO_REPARSE_TAG_WIM**</span></span>
-   <span data-ttu-id="b07e2-177">**IO_REPARSE_TAG_WOF**</span><span class="sxs-lookup"><span data-stu-id="b07e2-177">**IO_REPARSE_TAG_WOF**</span></span>

<span data-ttu-id="b07e2-178">Um die Eindeutigkeit von Tags sicherzustellen, bietet Microsoft einen Mechanismus zum Verteilen neuer Tags.</span><span class="sxs-lookup"><span data-stu-id="b07e2-178">To ensure uniqueness of tags, Microsoft provides a mechanism to distribute new tags.</span></span> <span data-ttu-id="b07e2-179">Weitere Informationen finden Sie im [IFS-Kit (Installable File System, installier bares Datei System)](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).</span><span class="sxs-lookup"><span data-stu-id="b07e2-179">For more information, see the [Installable File System (IFS) Kit](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).</span></span>

 

 



