---
title: Dodownloadstate-Enumeration
description: Gibt die ID des aktuellen Download Status an, der Teil der **DO_DOWNLOAD_STATUS** Struktur ist.
keywords:
- Dodownloadstate-Enumeration, dodownloadstate
topic_type:
- apiref
api_name:
- DODownloadState
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 4fb882a26d20de3094aa46763d6e1538ccf0c643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518545"
---
# <a name="dodownloadstate-enumeration"></a><span data-ttu-id="60161-104">Dodownloadstate-Enumeration</span><span class="sxs-lookup"><span data-stu-id="60161-104">DODownloadState enumeration</span></span>

<span data-ttu-id="60161-105">Die **dodownloadstate** -Enumeration gibt die ID des aktuellen Download Status an, der Teil der **DO_DOWNLOAD_STATUS** Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="60161-105">The **DODownloadState** enumeration specifies the ID of the current download state, which is part of the **DO_DOWNLOAD_STATUS** structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="60161-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="60161-106">Syntax</span></span>

```cpp
typedef enum _DODownloadState
{
  DODownloadState_Created = 0, 
  DODownloadState_Transferring,
  DODownloadState_Transferred, 
  DODownloadState_Finalized,   
  DODownloadState_Aborted,     
  DODownloadState_Paused
} DODownloadState;
```

## <a name="constants"></a><span data-ttu-id="60161-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="60161-107">Constants</span></span>

| <span data-ttu-id="60161-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60161-108">Requirement</span></span> | <span data-ttu-id="60161-109">Wert</span><span class="sxs-lookup"><span data-stu-id="60161-109">Value</span></span> |
|-|-|
| <span data-ttu-id="60161-110">DODownloadState_Created</span><span class="sxs-lookup"><span data-stu-id="60161-110">DODownloadState_Created</span></span> | <span data-ttu-id="60161-111">Das Download Objekt wurde erstellt, aber noch nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="60161-111">Download object is created but hasn't been started yet.</span></span> |
| <span data-ttu-id="60161-112">DODownloadState_Transferring</span><span class="sxs-lookup"><span data-stu-id="60161-112">DODownloadState_Transferring</span></span> | <span data-ttu-id="60161-113">Der Download wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60161-113">Download is in progress.</span></span> |
| <span data-ttu-id="60161-114">DODownloadState_Transferred</span><span class="sxs-lookup"><span data-stu-id="60161-114">DODownloadState_Transferred</span></span> | <span data-ttu-id="60161-115">Der Download wird übertragen und kann erneut gestartet werden, indem ein anderer Teil der Datei heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="60161-115">Download is transferred and can start again by downloading another portion of the file.</span></span> |
| <span data-ttu-id="60161-116">DODownloadState_Finalized</span><span class="sxs-lookup"><span data-stu-id="60161-116">DODownloadState_Finalized</span></span> | <span data-ttu-id="60161-117">Der Download wurde abgeschlossen und kann nicht erneut gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="60161-117">Download is finalized and cannot be started again.</span></span> |
| <span data-ttu-id="60161-118">DODownloadState_Aborted</span><span class="sxs-lookup"><span data-stu-id="60161-118">DODownloadState_Aborted</span></span> | <span data-ttu-id="60161-119">Der Download wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="60161-119">Download was aborted.</span></span> |
| <span data-ttu-id="60161-120">DODownloadState_Paused</span><span class="sxs-lookup"><span data-stu-id="60161-120">DODownloadState_Paused</span></span> | <span data-ttu-id="60161-121">Der Download wurde bei Bedarf oder aufgrund eines vorübergehenden Fehlers angehalten.</span><span class="sxs-lookup"><span data-stu-id="60161-121">Download has been paused on demand or due to transient error.</span></span> |

## <a name="requirements"></a><span data-ttu-id="60161-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60161-122">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="60161-123">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="60161-123">**Minimum supported client**</span></span> | <span data-ttu-id="60161-124">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="60161-124">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="60161-125">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="60161-125">**Minimum supported server**</span></span> | <span data-ttu-id="60161-126">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="60161-126">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="60161-127">**Header**</span><span class="sxs-lookup"><span data-stu-id="60161-127">**Header**</span></span> | <span data-ttu-id="60161-128">Deliveryoptimizationdownloadtypes. h</span><span class="sxs-lookup"><span data-stu-id="60161-128">DeliveryOptimizationDownloadTypes.h</span></span> |
