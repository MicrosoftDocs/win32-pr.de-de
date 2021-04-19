---
description: VDS-Konstanten
ms.assetid: a3a8b549-51bc-48eb-9215-04c7311e03a3
title: VDS-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9979cd4416b5305c61f6275612422b1f4cfe43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363748"
---
# <a name="vds-constants"></a><span data-ttu-id="1a157-103">VDS-Konstanten</span><span class="sxs-lookup"><span data-stu-id="1a157-103">VDS Constants</span></span>

<span data-ttu-id="1a157-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="1a157-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="1a157-105">VDS-Konstanten werden wie folgt kategorisiert:</span><span class="sxs-lookup"><span data-stu-id="1a157-105">VDS constants are categorized as follows:</span></span>

-   [<span data-ttu-id="1a157-106">Objekt Status Konstanten</span><span class="sxs-lookup"><span data-stu-id="1a157-106">Object Status Constants</span></span>](#object-status-constants)
-   [<span data-ttu-id="1a157-107">Automatisierungs Hinweise-Konstanten</span><span class="sxs-lookup"><span data-stu-id="1a157-107">Automagic Hints Constants</span></span>](#automagic-hints-constants)
-   [<span data-ttu-id="1a157-108">Sonstige Konstanten</span><span class="sxs-lookup"><span data-stu-id="1a157-108">Miscellaneous Constants</span></span>](#miscellaneous-constants)

### <a name="object-status-constants"></a><span data-ttu-id="1a157-109">Objekt Status Konstanten</span><span class="sxs-lookup"><span data-stu-id="1a157-109">Object Status Constants</span></span>



| <span data-ttu-id="1a157-110">Konstante</span><span class="sxs-lookup"><span data-stu-id="1a157-110">Constant</span></span>           | <span data-ttu-id="1a157-111">Wert</span><span class="sxs-lookup"><span data-stu-id="1a157-111">Value</span></span> |
|--------------------|-------|
| <span data-ttu-id="1a157-112">\_Unbekannter Status</span><span class="sxs-lookup"><span data-stu-id="1a157-112">STATUS\_UNKNOWN</span></span>    | <span data-ttu-id="1a157-113">0</span><span class="sxs-lookup"><span data-stu-id="1a157-113">0</span></span>     |
| <span data-ttu-id="1a157-114">Status \_ Online</span><span class="sxs-lookup"><span data-stu-id="1a157-114">STATUS\_ONLINE</span></span>     | <span data-ttu-id="1a157-115">1</span><span class="sxs-lookup"><span data-stu-id="1a157-115">1</span></span>     |
| <span data-ttu-id="1a157-116">Status \_ nicht \_ bereit</span><span class="sxs-lookup"><span data-stu-id="1a157-116">STATUS\_NOT\_READY</span></span> | <span data-ttu-id="1a157-117">2</span><span class="sxs-lookup"><span data-stu-id="1a157-117">2</span></span>     |
| <span data-ttu-id="1a157-118">Status " \_ kein \_ Medium"</span><span class="sxs-lookup"><span data-stu-id="1a157-118">STATUS\_NO\_MEDIA</span></span>  | <span data-ttu-id="1a157-119">3</span><span class="sxs-lookup"><span data-stu-id="1a157-119">3</span></span>     |
| <span data-ttu-id="1a157-120">Status \_ Offline</span><span class="sxs-lookup"><span data-stu-id="1a157-120">STATUS\_OFFLINE</span></span>    | <span data-ttu-id="1a157-121">4</span><span class="sxs-lookup"><span data-stu-id="1a157-121">4</span></span>     |
| <span data-ttu-id="1a157-122">Status \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="1a157-122">STATUS\_FAILED</span></span>     | <span data-ttu-id="1a157-123">5</span><span class="sxs-lookup"><span data-stu-id="1a157-123">5</span></span>     |
| <span data-ttu-id="1a157-124">Status \_ fehlt</span><span class="sxs-lookup"><span data-stu-id="1a157-124">STATUS\_MISSING</span></span>    | <span data-ttu-id="1a157-125">6</span><span class="sxs-lookup"><span data-stu-id="1a157-125">6</span></span>     |



 

### <a name="automagic-hints-constants"></a><span data-ttu-id="1a157-126">Automatisierungs Hinweise-Konstanten</span><span class="sxs-lookup"><span data-stu-id="1a157-126">Automagic Hints Constants</span></span>



| <span data-ttu-id="1a157-127">Konstante</span><span class="sxs-lookup"><span data-stu-id="1a157-127">Constant</span></span>                               | <span data-ttu-id="1a157-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1a157-128">Value</span></span>   |
|----------------------------------------|---------|
| <span data-ttu-id="1a157-129">VDS- \_ Hinweis " \_ mustlyreads"</span><span class="sxs-lookup"><span data-stu-id="1a157-129">VDS\_HINT\_MOSTLYREADS</span></span>                 | <span data-ttu-id="1a157-130">0x0002l</span><span class="sxs-lookup"><span data-stu-id="1a157-130">0x0002L</span></span> |
| <span data-ttu-id="1a157-131">VDS- \_ Hinweis \_ optimizeforsequentialreads</span><span class="sxs-lookup"><span data-stu-id="1a157-131">VDS\_HINT\_OPTIMIZEFORSEQUENTIALREADS</span></span>  | <span data-ttu-id="1a157-132">0x0004l</span><span class="sxs-lookup"><span data-stu-id="1a157-132">0x0004L</span></span> |
| <span data-ttu-id="1a157-133">VDS- \_ Hinweis \_ optimizeforsequentialschreib Vorgänge</span><span class="sxs-lookup"><span data-stu-id="1a157-133">VDS\_HINT\_OPTIMIZEFORSEQUENTIALWRITES</span></span> | <span data-ttu-id="1a157-134">0x0008l</span><span class="sxs-lookup"><span data-stu-id="1a157-134">0x0008L</span></span> |
| <span data-ttu-id="1a157-135">VDS-Hinweis neu zuordnen \_ \_</span><span class="sxs-lookup"><span data-stu-id="1a157-135">VDS\_HINT\_REMAPENABLED</span></span>                | <span data-ttu-id="1a157-136">0x0020l</span><span class="sxs-lookup"><span data-stu-id="1a157-136">0x0020L</span></span> |
| <span data-ttu-id="1a157-137">VDS- \_ Hinweis " \_ Write-Through cachingenabled"</span><span class="sxs-lookup"><span data-stu-id="1a157-137">VDS\_HINT\_WRITETHROUGHCACHINGENABLED</span></span>  | <span data-ttu-id="1a157-138">0x0040l</span><span class="sxs-lookup"><span data-stu-id="1a157-138">0x0040L</span></span> |
| <span data-ttu-id="1a157-139">VDS- \_ Hinweis \_ hardwarechecksumenabled</span><span class="sxs-lookup"><span data-stu-id="1a157-139">VDS\_HINT\_HARDWARECHECKSUMENABLED</span></span>     | <span data-ttu-id="1a157-140">0x0080l</span><span class="sxs-lookup"><span data-stu-id="1a157-140">0x0080L</span></span> |
| <span data-ttu-id="1a157-141">VDS- \_ Hinweis ist \_ isyankable</span><span class="sxs-lookup"><span data-stu-id="1a157-141">VDS\_HINT\_ISYANKABLE</span></span>                  | <span data-ttu-id="1a157-142">0x0100l</span><span class="sxs-lookup"><span data-stu-id="1a157-142">0x0100L</span></span> |



 

### <a name="miscellaneous-constants"></a><span data-ttu-id="1a157-143">Sonstige Konstanten</span><span class="sxs-lookup"><span data-stu-id="1a157-143">Miscellaneous Constants</span></span>



| <span data-ttu-id="1a157-144">Konstante</span><span class="sxs-lookup"><span data-stu-id="1a157-144">Constant</span></span>                     | <span data-ttu-id="1a157-145">Wert</span><span class="sxs-lookup"><span data-stu-id="1a157-145">Value</span></span>      |
|------------------------------|------------|
| <span data-ttu-id="1a157-146">VDS-Neuerstellung \_ \_ Priorität \_ Min.</span><span class="sxs-lookup"><span data-stu-id="1a157-146">VDS\_REBUILD\_PRIORITY\_MIN</span></span>  | <span data-ttu-id="1a157-147">0x0001l</span><span class="sxs-lookup"><span data-stu-id="1a157-147">0x0001L</span></span>    |
| <span data-ttu-id="1a157-148">\_VDS- \_ LUN- \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="1a157-148">VER\_VDS\_LUN\_INFORMATION</span></span>   | <span data-ttu-id="1a157-149">1</span><span class="sxs-lookup"><span data-stu-id="1a157-149">1</span></span>          |
| <span data-ttu-id="1a157-150">maximale \_ Länge des Computer namens \_</span><span class="sxs-lookup"><span data-stu-id="1a157-150">MAX\_COMPUTERNAME\_LENGTH</span></span>    | <span data-ttu-id="1a157-151">15</span><span class="sxs-lookup"><span data-stu-id="1a157-151">15</span></span>         |
| <span data-ttu-id="1a157-152">maximale \_ Länge von ProviderName \_</span><span class="sxs-lookup"><span data-stu-id="1a157-152">MAX\_PROVIDERNAME\_LENGTH</span></span>    | <span data-ttu-id="1a157-153">200</span><span class="sxs-lookup"><span data-stu-id="1a157-153">200</span></span>        |
| <span data-ttu-id="1a157-154">maximale \_ Länge der Versions Zeichenfolge \_</span><span class="sxs-lookup"><span data-stu-id="1a157-154">MAX\_VERSIONSTRING\_LENGTH</span></span>   | <span data-ttu-id="1a157-155">16</span><span class="sxs-lookup"><span data-stu-id="1a157-155">16</span></span>         |
| <span data-ttu-id="1a157-156">Laufwerk \_ Buchstaben- \_ Prop</span><span class="sxs-lookup"><span data-stu-id="1a157-156">DRIVE\_LETTER\_PROP</span></span>          | <span data-ttu-id="1a157-157">–</span><span class="sxs-lookup"><span data-stu-id="1a157-157">N/A</span></span>        |
| <span data-ttu-id="1a157-158">maximale \_ Größe des FS- \_ namens \_</span><span class="sxs-lookup"><span data-stu-id="1a157-158">MAX\_FS\_NAME\_SIZE</span></span>          | <span data-ttu-id="1a157-159">8</span><span class="sxs-lookup"><span data-stu-id="1a157-159">8</span></span>          |
| <span data-ttu-id="1a157-160">Ungültiger \_ IDX-Member. \_</span><span class="sxs-lookup"><span data-stu-id="1a157-160">INVALID\_MEMBER\_IDX</span></span>         | <span data-ttu-id="1a157-161">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="1a157-161">0xFFFFFFFF</span></span> |
| <span data-ttu-id="1a157-162">Länge des GPT- \_ Partitions \_ namens \_</span><span class="sxs-lookup"><span data-stu-id="1a157-162">GPT\_PARTITION\_NAME\_LENGTH</span></span> | <span data-ttu-id="1a157-163">36</span><span class="sxs-lookup"><span data-stu-id="1a157-163">36</span></span>         |
| <span data-ttu-id="1a157-164">Maximaler \_ Pfad</span><span class="sxs-lookup"><span data-stu-id="1a157-164">MAX\_PATH</span></span>                    | <span data-ttu-id="1a157-165">260</span><span class="sxs-lookup"><span data-stu-id="1a157-165">260</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1a157-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1a157-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a157-167">VDS-Referenz</span><span class="sxs-lookup"><span data-stu-id="1a157-167">VDS Reference</span></span>](vds-reference.md)
</dt> </dl>

 

 
