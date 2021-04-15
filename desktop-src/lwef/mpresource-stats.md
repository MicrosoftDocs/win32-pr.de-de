---
title: MPRESOURCE_STATS Struktur (mpclient. h)
description: Ressourcenbezogene Statistiken.
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- MPRESOURCE_STATS Struktur Funktionen der Legacy-Windows-Umgebung
- PMPRESOURCE_STATS Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPRESOURCE_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afbe1ce6734aabd1093f7acd886af757c51ed83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477658"
---
# <a name="mpresource_stats-structure"></a><span data-ttu-id="46741-105">Mpresource- \_ Statistik Struktur</span><span class="sxs-lookup"><span data-stu-id="46741-105">MPRESOURCE\_STATS structure</span></span>

<span data-ttu-id="46741-106">Ressourcenbezogene Statistiken.</span><span class="sxs-lookup"><span data-stu-id="46741-106">Resource-related statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="46741-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="46741-107">Syntax</span></span>


```C++
typedef struct tagMPRESOURCE_STATS {
  DWORD  PPMProgress;
  UINT64 ProcessCount;
  UINT64 FileCount;
  UINT64 FileBytesCount;
  UINT64 RegKeyCount;
  UINT64 Reserved[4];
} MPRESOURCE_STATS, *PMPRESOURCE_STATS;
```



## <a name="members"></a><span data-ttu-id="46741-108">Member</span><span class="sxs-lookup"><span data-stu-id="46741-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="46741-109">**Ppmprogress**</span><span class="sxs-lookup"><span data-stu-id="46741-109">**PPMProgress**</span></span>
</dt> <dd>

<span data-ttu-id="46741-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="46741-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="46741-111">Der ungefähre Fortschritt für die Überprüfung in ppm (Teile pro Million).</span><span class="sxs-lookup"><span data-stu-id="46741-111">Approximate progress for scan in ppm (parts per million).</span></span> <span data-ttu-id="46741-112">Legen Sie auf **mpprogress \_ ungültig** fest, wenn keine Fortschrittsinformationen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="46741-112">Set to **MPPROGRESS\_INVALID** if progress information is not available.</span></span>

</dd> <dt>

<span data-ttu-id="46741-113">**ProcessCount**</span><span class="sxs-lookup"><span data-stu-id="46741-113">**ProcessCount**</span></span>
</dt> <dd>

<span data-ttu-id="46741-114">Typ: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="46741-114">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="46741-115">Anzahl der gescannten Prozesse.</span><span class="sxs-lookup"><span data-stu-id="46741-115">Number of processes scanned.</span></span>

</dd> <dt>

<span data-ttu-id="46741-116">**FileCount**</span><span class="sxs-lookup"><span data-stu-id="46741-116">**FileCount**</span></span>
</dt> <dd>

<span data-ttu-id="46741-117">Typ: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="46741-117">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="46741-118">Anzahl der gescannten Dateien.</span><span class="sxs-lookup"><span data-stu-id="46741-118">Number of files scanned.</span></span>

</dd> <dt>

<span data-ttu-id="46741-119">**Filebytescount**</span><span class="sxs-lookup"><span data-stu-id="46741-119">**FileBytesCount**</span></span>
</dt> <dd>

<span data-ttu-id="46741-120">Typ: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="46741-120">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="46741-121">Anzahl von Bytes, die für Dateien gescannt wurden.</span><span class="sxs-lookup"><span data-stu-id="46741-121">Number of bytes scanned for files.</span></span>

</dd> <dt>

<span data-ttu-id="46741-122">**Regkeycount**</span><span class="sxs-lookup"><span data-stu-id="46741-122">**RegKeyCount**</span></span>
</dt> <dd>

<span data-ttu-id="46741-123">Typ: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="46741-123">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="46741-124">Anzahl der gescannten Regkeys.</span><span class="sxs-lookup"><span data-stu-id="46741-124">Number of RegKeys scanned.</span></span>

</dd> <dt>

<span data-ttu-id="46741-125">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="46741-125">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="46741-126">Typ: **UINT64 \[ 4 \]**</span><span class="sxs-lookup"><span data-stu-id="46741-126">Type: **UINT64\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="46741-127">Felder, die für die zukünftige Verwendung reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="46741-127">Fields reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46741-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46741-128">Requirements</span></span>



| <span data-ttu-id="46741-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46741-129">Requirement</span></span> | <span data-ttu-id="46741-130">Wert</span><span class="sxs-lookup"><span data-stu-id="46741-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46741-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46741-131">Minimum supported client</span></span><br/> | <span data-ttu-id="46741-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46741-132">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="46741-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46741-133">Minimum supported server</span></span><br/> | <span data-ttu-id="46741-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46741-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46741-135">Header</span><span class="sxs-lookup"><span data-stu-id="46741-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="46741-136"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="46741-136"><dt>MpClient.h</dt></span></span> </dl> |



 

 





