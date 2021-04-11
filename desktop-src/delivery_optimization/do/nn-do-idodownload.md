---
title: Idodownload-Schnittstelle
description: Wird verwendet, um einen Download zu starten und zu verwalten.
keywords:
- Idodownload-Schnittstelle
topic_type:
- apiref
api_name:
- IDODownload
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: ec2f74ce7daae6f612297d21e15e6993fcd78382
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315261"
---
# <a name="idodownload-interface"></a><span data-ttu-id="d05e3-104">Idodownload-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d05e3-104">IDODownload interface</span></span>

<span data-ttu-id="d05e3-105">Die **idodownload** -Schnittstelle wird verwendet, um einen Download zu starten und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="d05e3-105">The **IDODownload** interface is used to start and manage a download.</span></span>

## <a name="methods"></a><span data-ttu-id="d05e3-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="d05e3-106">Methods</span></span>

<span data-ttu-id="d05e3-107">Die **idodownload** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d05e3-107">The **IDODownload** interface has these methods.</span></span>

| <span data-ttu-id="d05e3-108">Methode</span><span class="sxs-lookup"><span data-stu-id="d05e3-108">Method</span></span> | <span data-ttu-id="d05e3-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d05e3-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="d05e3-110">Idodownload:: Abort</span><span class="sxs-lookup"><span data-stu-id="d05e3-110">IDODownload::Abort</span></span>](./nf-do-idomanager-createdownload.md) | <span data-ttu-id="d05e3-111">Bricht den Download ab.</span><span class="sxs-lookup"><span data-stu-id="d05e3-111">Aborts the download.</span></span> |
| [<span data-ttu-id="d05e3-112">Idodownload:: Finalize</span><span class="sxs-lookup"><span data-stu-id="d05e3-112">IDODownload::Finalize</span></span>](./nf-do-idodownload-finalize.md) | <span data-ttu-id="d05e3-113">Schließt den Download ab.</span><span class="sxs-lookup"><span data-stu-id="d05e3-113">Finalizes the download.</span></span> |
| [<span data-ttu-id="d05e3-114">Idodownload:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="d05e3-114">IDODownload::GetProperty</span></span>](./nf-do-idodownload-getproperty.md) | <span data-ttu-id="d05e3-115">Ruft einen Zeiger auf eine **Variante** ab, die eine bestimmte Download Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="d05e3-115">Retrieves a pointer to a **VARIANT** that contains a specific download property.</span></span> |
| [<span data-ttu-id="d05e3-116">Idodownload:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="d05e3-116">IDODownload::GetStatus</span></span>](./nf-do-idodownload-getstatus.md) | <span data-ttu-id="d05e3-117">Ruft einen Zeiger auf eine **DO_DOWNLOAD_STATUS** -Struktur ab, die den aktuellen Status des Downloads widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="d05e3-117">Retrieves a pointer to a **DO_DOWNLOAD_STATUS** structure that reflects the current status of the download.</span></span> |
| [<span data-ttu-id="d05e3-118">Idodownload::P ause</span><span class="sxs-lookup"><span data-stu-id="d05e3-118">IDODownload::Pause</span></span>](./nf-do-idodownload-pause.md) | <span data-ttu-id="d05e3-119">Hält den Download an.</span><span class="sxs-lookup"><span data-stu-id="d05e3-119">Pauses the download.</span></span> |
| [<span data-ttu-id="d05e3-120">Idodownload:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="d05e3-120">IDODownload::SetProperty</span></span>](./nf-do-idodownload-setproperty.md) | <span data-ttu-id="d05e3-121">Legt eine Download Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="d05e3-121">Sets a download property.</span></span> |
| [<span data-ttu-id="d05e3-122">Idodownload:: Start</span><span class="sxs-lookup"><span data-stu-id="d05e3-122">IDODownload::Start</span></span>](./nf-do-idodownload-start.md) | <span data-ttu-id="d05e3-123">Startet einen Download oder nimmt diesen wieder auf.</span><span class="sxs-lookup"><span data-stu-id="d05e3-123">Starts or resumes a download.</span></span> |

## <a name="requirements"></a><span data-ttu-id="d05e3-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d05e3-124">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d05e3-125">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="d05e3-125">**Minimum supported client**</span></span> | <span data-ttu-id="d05e3-126">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="d05e3-126">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="d05e3-127">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="d05e3-127">**Minimum supported server**</span></span> | <span data-ttu-id="d05e3-128">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="d05e3-128">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="d05e3-129">**Header**</span><span class="sxs-lookup"><span data-stu-id="d05e3-129">**Header**</span></span> | <span data-ttu-id="d05e3-130">Do. h</span><span class="sxs-lookup"><span data-stu-id="d05e3-130">Do.h</span></span> |