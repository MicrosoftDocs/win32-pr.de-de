---
title: MPSIGUPDATE_DATA Struktur (mpclient. h)
description: Benachrichtigungs Daten werden an die Rückruffunktion der Signatur Aktualisierung übermittelt.
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- MPSIGUPDATE_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPSIGUPDATE_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPSIGUPDATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442b19da394043b6fc6b8693f51c5f150233f970
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104540"
---
# <a name="mpsigupdate_data-structure"></a><span data-ttu-id="f6f98-105">Mpsigupdate- \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="f6f98-105">MPSIGUPDATE\_DATA structure</span></span>

<span data-ttu-id="f6f98-106">Benachrichtigungs Daten werden an die Rückruffunktion der Signatur Aktualisierung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="f6f98-106">Notification data passed to the signature update callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6f98-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6f98-107">Syntax</span></span>


```C++
typedef struct tagMPSIGUPDATE_DATA {
  DWORD                 dwPercentComplete;
  DWORD                 dwTotalUpdates;
  DWORD                 dwCurrentUpdateIndex;
  MPSIGUPDATE_TYPE      eType;
  MP_UPDATE_STAGE       Stage;
  MP_MIDL_STRING LPWSTR Path;
} MPSIGUPDATE_DATA, *PMPSIGUPDATE_DATA;
```



## <a name="members"></a><span data-ttu-id="f6f98-108">Member</span><span class="sxs-lookup"><span data-stu-id="f6f98-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f6f98-109">**dwprozentucomplete**</span><span class="sxs-lookup"><span data-stu-id="f6f98-109">**dwPercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="f6f98-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f6f98-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f6f98-111">Eine Schätzung des Prozentsatzes für alle Updates, die heruntergeladen und/oder installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="f6f98-111">An estimate of the percentage across all the updates that have been downloaded and/or installed.</span></span>

</dd> <dt>

<span data-ttu-id="f6f98-112">**dwtotalupdates**</span><span class="sxs-lookup"><span data-stu-id="f6f98-112">**dwTotalUpdates**</span></span>
</dt> <dd>

<span data-ttu-id="f6f98-113">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f6f98-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f6f98-114">Gesamtzahl der herunter zuladenden und/oder zu installierenden Updates.</span><span class="sxs-lookup"><span data-stu-id="f6f98-114">Total number of updates to download and/or install.</span></span>

</dd> <dt>

<span data-ttu-id="f6f98-115">**dwcurrentupdateingedex**</span><span class="sxs-lookup"><span data-stu-id="f6f98-115">**dwCurrentUpdateIndex**</span></span>
</dt> <dd>

<span data-ttu-id="f6f98-116">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f6f98-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f6f98-117">NULL basierter Indexwert, der angibt, welches Update zwischen den erforderlichen zurzeit heruntergeladen und/oder installiert wird.</span><span class="sxs-lookup"><span data-stu-id="f6f98-117">Zero-based index value that specifies which update among those required is currently being downloaded and/or installed.</span></span>

</dd> <dt>

<span data-ttu-id="f6f98-118">**ETYPE**</span><span class="sxs-lookup"><span data-stu-id="f6f98-118">**eType**</span></span>
</dt> <dd>

<span data-ttu-id="f6f98-119">Typ: **mpsigupdate- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="f6f98-119">Type: **MPSIGUPDATE\_TYPE**</span></span>

</dd> <dd>

<span data-ttu-id="f6f98-120">Aktualisieren Sie den Typ.</span><span class="sxs-lookup"><span data-stu-id="f6f98-120">Update type.</span></span> <span data-ttu-id="f6f98-121">Einer der folgenden möglichen Werte:</span><span class="sxs-lookup"><span data-stu-id="f6f98-121">One of the following possible values:</span></span>



| <span data-ttu-id="f6f98-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f6f98-122">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="f6f98-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f6f98-123">Meaning</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <span data-ttu-id="f6f98-124"><dt>**mpsigupdate- \_ Typ " \_ None"**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f98-124"><dt>**MPSIGUPDATE\_TYPE\_NONE**</dt></span></span> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <span data-ttu-id="f6f98-125"><dt>**verwalteter mpsigupdate- \_ Typ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f98-125"><dt>**MPSIGUPDATE\_TYPE\_MANAGED**</dt></span></span> </dl>                                   | <span data-ttu-id="f6f98-126">WSUS-Update</span><span class="sxs-lookup"><span data-stu-id="f6f98-126">WSUS update.</span></span> <span data-ttu-id="f6f98-127">Abbrechen erfordert Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="f6f98-127">Cancel requires administrator rights.</span></span><br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <span data-ttu-id="f6f98-128"><dt>**mpsigupdate- \_ Typ \_ http**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f98-128"><dt>**MPSIGUPDATE\_TYPE\_HTTP**</dt></span></span> </dl>                                            | <span data-ttu-id="f6f98-129">HTTP-Update.</span><span class="sxs-lookup"><span data-stu-id="f6f98-129">HTTP update.</span></span> <span data-ttu-id="f6f98-130">Zum Abbrechen sind keine Administrator Rechte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f6f98-130">Administrator rights not needed to cancel.</span></span><br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <span data-ttu-id="f6f98-131"><dt>**mpsigupdate- \_ Typ \_ http \_ SRV**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f98-131"><dt>**MPSIGUPDATE\_TYPE\_HTTP\_SRV**</dt></span></span> </dl>                               | <span data-ttu-id="f6f98-132">HTTP vom Dienst.</span><span class="sxs-lookup"><span data-stu-id="f6f98-132">HTTP from service.</span></span> <span data-ttu-id="f6f98-133">Abbrechen erfordert Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="f6f98-133">Cancel requires administrator rights.</span></span><br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <span data-ttu-id="f6f98-134"><dt>**mpsigupdate- \_ Typ \_ UNC**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f98-134"><dt>**MPSIGUPDATE\_TYPE\_UNC**</dt></span></span> </dl>                                               | <span data-ttu-id="f6f98-135">UNC-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="f6f98-135">UNC share.</span></span> <span data-ttu-id="f6f98-136">Zum Abbrechen sind keine Administrator Rechte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f6f98-136">Administrator rights not needed to cancel.</span></span><br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <span data-ttu-id="f6f98-137"><dt>**mpsigupdate- \_ Typ \_ nicht verwaltet**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f98-137"><dt>**MPSIGUPDATE\_TYPE\_UNMANAGED**</dt></span></span> </dl>                             | <span data-ttu-id="f6f98-138">MU/wu-Update.</span><span class="sxs-lookup"><span data-stu-id="f6f98-138">MU/WU update.</span></span> <span data-ttu-id="f6f98-139">Abbrechen erfordert Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="f6f98-139">Cancel requires administrator rights.</span></span><br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <span data-ttu-id="f6f98-140"><dt>**\_ \_ verwaltete \_ Plattform für mpsigupdate-Typ**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f98-140"><dt>**MPSIGUPDATE\_TYPE\_MANAGED\_PLATFORM**</dt></span></span> </dl>       | <span data-ttu-id="f6f98-141">WSUS-Update für Plattform.</span><span class="sxs-lookup"><span data-stu-id="f6f98-141">WSUS update for PLATFORM.</span></span> <span data-ttu-id="f6f98-142">Abbrechen erfordert Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="f6f98-142">Cancel requires administrator rights.</span></span><br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <span data-ttu-id="f6f98-143"><dt>**mpsigupdate- \_ Typ \_ nicht verwaltete \_ Plattform**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f98-143"><dt>**MPSIGUPDATE\_TYPE\_UNMANAGED\_PLATFORM**</dt></span></span> </dl> | <span data-ttu-id="f6f98-144">MU/wu-Update für Plattform.</span><span class="sxs-lookup"><span data-stu-id="f6f98-144">MU/WU update for PLATFORM.</span></span> <span data-ttu-id="f6f98-145">Abbrechen erfordert Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="f6f98-145">Cancel requires administrator rights.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f6f98-146">**Phase**</span><span class="sxs-lookup"><span data-stu-id="f6f98-146">**Stage**</span></span>
</dt> <dd>

<span data-ttu-id="f6f98-147">Typ: **MP- \_ Aktualisierungs \_ Phase**</span><span class="sxs-lookup"><span data-stu-id="f6f98-147">Type: **MP\_UPDATE\_STAGE**</span></span>

</dd> <dd>

<span data-ttu-id="f6f98-148">Aktualisierungs Phase.</span><span class="sxs-lookup"><span data-stu-id="f6f98-148">Update stage.</span></span> <span data-ttu-id="f6f98-149">Einer der folgenden möglichen Werte:</span><span class="sxs-lookup"><span data-stu-id="f6f98-149">One of the following possible values:</span></span>



| <span data-ttu-id="f6f98-150">Wert</span><span class="sxs-lookup"><span data-stu-id="f6f98-150">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="f6f98-151">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f6f98-151">Meaning</span></span>                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <span data-ttu-id="f6f98-152"><dt>**MP- \_ Stufe \_ unbekannt**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f98-152"><dt>**MP\_STAGE\_UNKNOWN**</dt></span></span> </dl>       | <span data-ttu-id="f6f98-153">Die Aktualisierungs Phase ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="f6f98-153">Update stage unknown.</span></span><br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <span data-ttu-id="f6f98-154"><dt>**MP- \_ Suche- \_ Update**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f98-154"><dt>**MP\_SEARCH\_UPDATE**</dt></span></span> </dl>       | <span data-ttu-id="f6f98-155">Aktualisierungs Phase aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f6f98-155">Update search stage.</span></span><br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <span data-ttu-id="f6f98-156"><dt>**MP- \_ Download \_ Update**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f98-156"><dt>**MP\_DOWNLOAD\_UPDATE**</dt></span></span> </dl> | <span data-ttu-id="f6f98-157">Download Stufe aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f6f98-157">Update download stage.</span></span><br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <span data-ttu-id="f6f98-158"><dt>**MP- \_ Installations \_ Update**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f98-158"><dt>**MP\_INSTALL\_UPDATE**</dt></span></span> </dl>    | <span data-ttu-id="f6f98-159">Aktualisieren Sie die Installationsphase.</span><span class="sxs-lookup"><span data-stu-id="f6f98-159">Update install stage.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="f6f98-160">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="f6f98-160">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="f6f98-161">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="f6f98-161">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f6f98-162">Aktualisieren Sie den Pfad.</span><span class="sxs-lookup"><span data-stu-id="f6f98-162">Update path.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6f98-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6f98-163">Requirements</span></span>



| <span data-ttu-id="f6f98-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6f98-164">Requirement</span></span> | <span data-ttu-id="f6f98-165">Wert</span><span class="sxs-lookup"><span data-stu-id="f6f98-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f98-166">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6f98-166">Minimum supported client</span></span><br/> | <span data-ttu-id="f6f98-167">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6f98-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f6f98-168">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6f98-168">Minimum supported server</span></span><br/> | <span data-ttu-id="f6f98-169">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6f98-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6f98-170">Header</span><span class="sxs-lookup"><span data-stu-id="f6f98-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6f98-171"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6f98-171"><dt>MpClient.h</dt></span></span> </dl> |



 

 





