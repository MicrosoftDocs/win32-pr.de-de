---
title: DO_DOWNLOAD_STATUS Struktur
description: Dient zum Abrufen des Status eines bestimmten Downloads.
keywords:
- DO_DOWNLOAD_STATUS Struktur
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_STATUS
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5e113bb4866ef1033886dbb1579d21aa296d0e5e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106338642"
---
# <a name="do_download_status-structure"></a><span data-ttu-id="47304-104">DO_DOWNLOAD_STATUS Struktur</span><span class="sxs-lookup"><span data-stu-id="47304-104">DO_DOWNLOAD_STATUS structure</span></span>

<span data-ttu-id="47304-105">Die **DO_DOWNLOAD_STATUS** Struktur wird verwendet, um den Status eines bestimmten Downloads abzurufen.</span><span class="sxs-lookup"><span data-stu-id="47304-105">The **DO_DOWNLOAD_STATUS** structure is used to obtain the status of a specific download.</span></span> <span data-ttu-id="47304-106">Sie wird durch Aufrufen der **idodownload:: GetStatus** -Funktion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="47304-106">It is obtained by calling the **IDODownload::GetStatus** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="47304-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="47304-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_STATUS
{
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  DODownloadState State;
  HRESULT Error;
  HRESULT ExtendedError;
} DO_DOWNLOAD_STATUS;
```

## <a name="members"></a><span data-ttu-id="47304-108">Member</span><span class="sxs-lookup"><span data-stu-id="47304-108">Members</span></span>

`BytesTotal`

<span data-ttu-id="47304-109">Die Gesamtzahl der herunter zuladenden bytes.</span><span class="sxs-lookup"><span data-stu-id="47304-109">The total number of bytes to download.</span></span>

`BytesTransferred`

<span data-ttu-id="47304-110">Die Anzahl von Bytes, die bereits heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="47304-110">The number of bytes that have already been downloaded.</span></span>

`State`

<span data-ttu-id="47304-111">Der aktuelle Download Zustand, wie von der **dodownloadstate** -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="47304-111">The current download state as defined by the **DODownloadState** enumeration.</span></span>

`Error`

<span data-ttu-id="47304-112">Die Fehlerinformationen (sofern vorhanden), die dem aktuellen Download zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="47304-112">The error information (if it exists) that is associated with the current download.</span></span>

`ExtendedError`

<span data-ttu-id="47304-113">Die erweiterten Fehlerinformationen (sofern vorhanden), die dem aktuellen Download zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="47304-113">The extended error information (if it exists) that is associated with the current download.</span></span>

## <a name="requirements"></a><span data-ttu-id="47304-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47304-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="47304-115">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="47304-115">**Minimum supported client**</span></span> | <span data-ttu-id="47304-116">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="47304-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="47304-117">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="47304-117">**Minimum supported server**</span></span> | <span data-ttu-id="47304-118">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="47304-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="47304-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="47304-119">**Header**</span></span> | <span data-ttu-id="47304-120">Do. h</span><span class="sxs-lookup"><span data-stu-id="47304-120">Do.h</span></span> |
