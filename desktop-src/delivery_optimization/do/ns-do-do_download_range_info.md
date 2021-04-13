---
title: DO_DOWNLOAD_RANGE_INFO Struktur
description: Gibt ein Array von Byte Bereichen an, das aus einer Datei heruntergeladen werden soll.
keywords:
- DO_DOWNLOAD_RANGE_INFO Struktur
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE_INFO
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 01628ea29895012f60552e696b7f68854f426f8d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104389648"
---
# <a name="do_download_range_info-structure"></a><span data-ttu-id="ceadf-104">DO_DOWNLOAD_RANGE_INFO Struktur</span><span class="sxs-lookup"><span data-stu-id="ceadf-104">DO_DOWNLOAD_RANGE_INFO structure</span></span>

<span data-ttu-id="ceadf-105">Die **DO_DOWNLOAD_RANGE_INFO** -Struktur identifiziert ein Array von Byte Bereichen, die aus einer Datei heruntergeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ceadf-105">The **DO_DOWNLOAD_RANGE_INFO** structure identifies an array of ranges of bytes to download from a file.</span></span> <span data-ttu-id="ceadf-106">Sie wird in der Regel als optionales Argument an die **idodownload:: Start** -Funktion übermittelt.</span><span class="sxs-lookup"><span data-stu-id="ceadf-106">It is typically passed as an optional argument to the **IDODownload::Start** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceadf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ceadf-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_RANGES_INFO
{
  UINT RangeCount;
  [size_is(RangeCount)] DO_DOWNLOAD_RANGE Ranges[];
} DO_DOWNLOAD_RANGES_INFO;
```

## <a name="members"></a><span data-ttu-id="ceadf-108">Member</span><span class="sxs-lookup"><span data-stu-id="ceadf-108">Members</span></span>

`RangeCount`

<span data-ttu-id="ceadf-109">Anzahl der Elemente in Bereichen.</span><span class="sxs-lookup"><span data-stu-id="ceadf-109">Number of elements in Ranges.</span></span>

`Ranges`

<span data-ttu-id="ceadf-110">Array aus mindestens einer **DO_DOWNLOAD_RANGE** -Struktur, die die Bereiche angeben, die heruntergeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ceadf-110">Array of one or more **DO_DOWNLOAD_RANGE** structures that specify the ranges to download.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceadf-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ceadf-111">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ceadf-112">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="ceadf-112">**Minimum supported client**</span></span> | <span data-ttu-id="ceadf-113">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="ceadf-113">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="ceadf-114">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="ceadf-114">**Minimum supported server**</span></span> | <span data-ttu-id="ceadf-115">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="ceadf-115">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="ceadf-116">**Header**</span><span class="sxs-lookup"><span data-stu-id="ceadf-116">**Header**</span></span> | <span data-ttu-id="ceadf-117">Do. h</span><span class="sxs-lookup"><span data-stu-id="ceadf-117">Do.h</span></span> |
