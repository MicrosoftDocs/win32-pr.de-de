---
title: DO_DOWNLOAD_RANGE Struktur
description: Identifiziert einen einzelnen Bereich von Bytes, der aus einer Datei heruntergeladen werden soll.
keywords:
- DO_DOWNLOAD_RANGE Struktur
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0f328565c80350a05cbfb23f178ea3580586f326
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106341698"
---
# <a name="do_download_range-structure"></a><span data-ttu-id="563a0-104">DO_DOWNLOAD_RANGE Struktur</span><span class="sxs-lookup"><span data-stu-id="563a0-104">DO_DOWNLOAD_RANGE structure</span></span>

<span data-ttu-id="563a0-105">Die **DO_DOWNLOAD_RANGE** -Struktur identifiziert einen einzelnen Bereich von Bytes, der aus einer Datei heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="563a0-105">The **DO_DOWNLOAD_RANGE** structure identifies a single range of bytes to download from a file.</span></span> <span data-ttu-id="563a0-106">Die **DO_DOWNLOAD_RANGE** Struktur ist in **DO_DOWNLOAD_RANGES_INFO** Struktur enthalten, um ein Array von Bereichen zum Herunterladen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="563a0-106">The **DO_DOWNLOAD_RANGE** structure is included within **DO_DOWNLOAD_RANGES_INFO** structure to provide an array of ranges to download.</span></span>

## <a name="syntax"></a><span data-ttu-id="563a0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="563a0-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_RANGE
{
  UINT64 Offset;
  UINT64 Length;
} DO_DOWNLOAD_RANGE;
```

## <a name="members"></a><span data-ttu-id="563a0-108">Member</span><span class="sxs-lookup"><span data-stu-id="563a0-108">Members</span></span>

`Offset`

<span data-ttu-id="563a0-109">NULL basierter Offset am Anfang des Bereichs von Bytes, der aus einer Datei heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="563a0-109">Zero-based offset to the beginning of the range of bytes to download from a file.</span></span>

`Length`

<span data-ttu-id="563a0-110">Die Länge des Bereichs in Bytes.</span><span class="sxs-lookup"><span data-stu-id="563a0-110">The length of the range, in bytes.</span></span> <span data-ttu-id="563a0-111">Geben Sie keine Länge von 0 Byte an.</span><span class="sxs-lookup"><span data-stu-id="563a0-111">Do not specify a zero-byte length.</span></span> <span data-ttu-id="563a0-112">Um anzugeben, dass der Bereich bis zum Ende der Datei reicht, geben Sie **DO_LENGTH_TO_EOF** an.</span><span class="sxs-lookup"><span data-stu-id="563a0-112">To indicate that the range extends to the end of the file, specify **DO_LENGTH_TO_EOF**.</span></span>

## <a name="requirements"></a><span data-ttu-id="563a0-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="563a0-113">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="563a0-114">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="563a0-114">**Minimum supported client**</span></span> | <span data-ttu-id="563a0-115">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="563a0-115">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="563a0-116">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="563a0-116">**Minimum supported server**</span></span> | <span data-ttu-id="563a0-117">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="563a0-117">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="563a0-118">**Header**</span><span class="sxs-lookup"><span data-stu-id="563a0-118">**Header**</span></span> | <span data-ttu-id="563a0-119">Deliveryoptimizationdownloadtypes. h</span><span class="sxs-lookup"><span data-stu-id="563a0-119">DeliveryOptimizationDownloadTypes.h</span></span> |
