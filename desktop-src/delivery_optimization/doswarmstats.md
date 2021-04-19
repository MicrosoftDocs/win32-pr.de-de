---
title: Doswarmstats-Struktur (deliveryoptimization. h)
description: Enthält Felder für das herunterladen und Hochladen von Statistiken für eine Datei.
ms.assetid: 66B2498A-38E0-44E4-96C1-F778BD9AA593
keywords:
- Doswarmstats-Struktur
topic_type:
- apiref
api_name:
- DOSwarmStats
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53d1702c25716ffe90c35727a258134311d5f427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346767"
---
# <a name="doswarmstats-structure"></a><span data-ttu-id="42543-104">Doswarmstats-Struktur</span><span class="sxs-lookup"><span data-stu-id="42543-104">DOSwarmStats structure</span></span>

<span data-ttu-id="42543-105">Enthält Felder für das herunterladen und Hochladen von Statistiken für eine Datei.</span><span class="sxs-lookup"><span data-stu-id="42543-105">Contains fields for download and upload statistics for a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="42543-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="42543-106">Syntax</span></span>


```C++
typedef struct _DOSwarmStats {
  LPWSTR       fileId;
  LPWSTR       sourceURL;
  UINT64       fileSize;
  UINT64       totalBytesDownloaded;
  UINT64       bytesFromLanPeers;
  UINT64       bytesFromGroupPeers;
  UINT64       bytesFromInternetPeers;
  UINT64       bytesFromHttp;
  UINT64       bytesFromDoinc;
  UINT64       bytesToLanPeers;
  UINT64       bytesToGroupPeers;
  UINT64       bytesToInternetPeers;
  UINT         httpConnectionCount;
  UINT         doincConnectionCount;
  UINT         lanConnectionCount;
  UINT         groupConnectionCount;
  UINT         internetConnectionCount;
  UINT         downloadDuration;
  DownloadMode downloadMode;
  SwarmStatus  status;
  BOOL         isBackground;
} DOSwarmStats;
```



## <a name="members"></a><span data-ttu-id="42543-107">Member</span><span class="sxs-lookup"><span data-stu-id="42543-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="42543-108">**fileId**</span><span class="sxs-lookup"><span data-stu-id="42543-108">**fileId**</span></span>
</dt> <dd>

<span data-ttu-id="42543-109">Eine mit NULL endend beendete Zeichenfolge, die mit dem **ADDFILEWITHRANGES** -Befehl angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="42543-109">Null-terminated string that was specified with the **AddFileWithRanges** call.</span></span>

</dd> <dt>

<span data-ttu-id="42543-110">**SourceURL**</span><span class="sxs-lookup"><span data-stu-id="42543-110">**sourceURL**</span></span>
</dt> <dd>

<span data-ttu-id="42543-111">NULL-terminierte Zeichenfolge, die den Namen der Datei auf dem Server enthält (z &lt; . b. https://Server &gt; / &lt; path &gt; /file.ext).</span><span class="sxs-lookup"><span data-stu-id="42543-111">Null-terminated string that contains the name of the file on the server (for example, https://&lt;server&gt;/&lt;path&gt;/file.ext).</span></span>

</dd> <dt>

<span data-ttu-id="42543-112">**Filesize**</span><span class="sxs-lookup"><span data-stu-id="42543-112">**fileSize**</span></span>
</dt> <dd>

<span data-ttu-id="42543-113">Die Länge der Datei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="42543-113">Size of the file in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="42543-114">**totalbytesherunter geladen**</span><span class="sxs-lookup"><span data-stu-id="42543-114">**totalBytesDownloaded**</span></span>
</dt> <dd>

<span data-ttu-id="42543-115">Gesamtanzahl der übertragenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="42543-115">Total number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="42543-116">**bytesfromlanpeers**</span><span class="sxs-lookup"><span data-stu-id="42543-116">**bytesFromLanPeers**</span></span>
</dt> <dd>

<span data-ttu-id="42543-117">Anzahl der von LAN-Peers übertragenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="42543-117">Number of bytes transferred from LAN peers.</span></span>

</dd> <dt>

<span data-ttu-id="42543-118">**bytesfromgrouppeers**</span><span class="sxs-lookup"><span data-stu-id="42543-118">**bytesFromGroupPeers**</span></span>
</dt> <dd>

<span data-ttu-id="42543-119">Anzahl von Bytes, die von Gruppen Peers übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="42543-119">Number of bytes transferred from group peers.</span></span>

</dd> <dt>

<span data-ttu-id="42543-120">**bytesfrominternetpeers**</span><span class="sxs-lookup"><span data-stu-id="42543-120">**bytesFromInternetPeers**</span></span>
</dt> <dd>

<span data-ttu-id="42543-121">Anzahl von Bytes, die von Internet Peers übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="42543-121">Number of bytes transferred from Internet peers.</span></span>

</dd> <dt>

<span data-ttu-id="42543-122">**bytesfromhttp**</span><span class="sxs-lookup"><span data-stu-id="42543-122">**bytesFromHttp**</span></span>
</dt> <dd>

<span data-ttu-id="42543-123">Anzahl von Bytes, die von http übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="42543-123">Number of bytes transferred from http.</span></span>

</dd> <dt>

<span data-ttu-id="42543-124">**bytesfromdoinc**</span><span class="sxs-lookup"><span data-stu-id="42543-124">**bytesFromDoinc**</span></span>
</dt> <dd>

<span data-ttu-id="42543-125">Nur zur internen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="42543-125">For internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="42543-126">**bytestolanpeers**</span><span class="sxs-lookup"><span data-stu-id="42543-126">**bytesToLanPeers**</span></span>
</dt> <dd>

<span data-ttu-id="42543-127">Anzahl der an LAN-Peers übertragenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="42543-127">Number of bytes transferred to LAN peers.</span></span>

</dd> <dt>

<span data-ttu-id="42543-128">**bytestogrouppeers**</span><span class="sxs-lookup"><span data-stu-id="42543-128">**bytesToGroupPeers**</span></span>
</dt> <dd>

<span data-ttu-id="42543-129">Anzahl von Bytes, die an Gruppen Peers übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="42543-129">Number of bytes transferred to group peers.</span></span>

</dd> <dt>

<span data-ttu-id="42543-130">**bytestointernetpeers**</span><span class="sxs-lookup"><span data-stu-id="42543-130">**bytesToInternetPeers**</span></span>
</dt> <dd>

<span data-ttu-id="42543-131">Anzahl von Bytes, die an Internet Peers übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="42543-131">Number of bytes transferred to Internet peers.</span></span>

</dd> <dt>

<span data-ttu-id="42543-132">**httpconnectioncount**</span><span class="sxs-lookup"><span data-stu-id="42543-132">**httpConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="42543-133">Anzahl der HTTP-Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="42543-133">Count of http connections.</span></span>

</dd> <dt>

<span data-ttu-id="42543-134">**doincconnectioncount**</span><span class="sxs-lookup"><span data-stu-id="42543-134">**doincConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="42543-135">Nur zur internen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="42543-135">For internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="42543-136">**lanconnectioncount**</span><span class="sxs-lookup"><span data-stu-id="42543-136">**lanConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="42543-137">Anzahl der LAN-Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="42543-137">Count of LAN connections.</span></span>

</dd> <dt>

<span data-ttu-id="42543-138">**groupconnectioncount**</span><span class="sxs-lookup"><span data-stu-id="42543-138">**groupConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="42543-139">Anzahl der Gruppen Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="42543-139">Count of group connections.</span></span>

</dd> <dt>

<span data-ttu-id="42543-140">**internetconnectioncount**</span><span class="sxs-lookup"><span data-stu-id="42543-140">**internetConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="42543-141">Anzahl der Internet Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="42543-141">Count of Internet connections.</span></span>

</dd> <dt>

<span data-ttu-id="42543-142">**Download Dauer**</span><span class="sxs-lookup"><span data-stu-id="42543-142">**downloadDuration**</span></span>
</dt> <dd>

<span data-ttu-id="42543-143">Dauer der Dateiübertragung in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="42543-143">Duration of the file transfer in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="42543-144">**Download Mode**</span><span class="sxs-lookup"><span data-stu-id="42543-144">**downloadMode**</span></span>
</dt> <dd>

<span data-ttu-id="42543-145">Der verwendete Download Modus finden Sie unter [**Download Mode**](downloadmode.md).</span><span class="sxs-lookup"><span data-stu-id="42543-145">The download mode used, see [**DownloadMode**](downloadmode.md).</span></span>

</dd> <dt>

<span data-ttu-id="42543-146">**status**</span><span class="sxs-lookup"><span data-stu-id="42543-146">**status**</span></span>
</dt> <dd>

<span data-ttu-id="42543-147">Zum Status einer Dateiübertragung finden Sie unter [**swarmstatus**](swarmstatus.md).</span><span class="sxs-lookup"><span data-stu-id="42543-147">The status of a file transfer, see [**SwarmStatus**](swarmstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="42543-148">**IsBackground**</span><span class="sxs-lookup"><span data-stu-id="42543-148">**isBackground**</span></span>
</dt> <dd>

<span data-ttu-id="42543-149">True, wenn es sich um eine Hintergrund Übertragung handelt.</span><span class="sxs-lookup"><span data-stu-id="42543-149">True, if this is a background transfer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42543-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42543-150">Requirements</span></span>



| <span data-ttu-id="42543-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42543-151">Requirement</span></span> | <span data-ttu-id="42543-152">Wert</span><span class="sxs-lookup"><span data-stu-id="42543-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42543-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42543-153">Minimum supported client</span></span><br/> | <span data-ttu-id="42543-154">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42543-154">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="42543-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42543-155">Minimum supported server</span></span><br/> | <span data-ttu-id="42543-156">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42543-156">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="42543-157">Header</span><span class="sxs-lookup"><span data-stu-id="42543-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="42543-158"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="42543-158"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





