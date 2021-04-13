---
title: Idodownloadstatus Callback-Schnittstelle
description: Wird zum Empfangen von Benachrichtigungen zu einem Download verwendet.
keywords:
- Idodownloadstatus Callback-Schnittstelle
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0917b73939535854469a1fe02ea89acc904cf055
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390370"
---
# <a name="idodownloadstatuscallback-interface"></a><span data-ttu-id="1a23f-104">Idodownloadstatus Callback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1a23f-104">IDODownloadStatusCallback interface</span></span>

<span data-ttu-id="1a23f-105">Die **idodownloadstatus Callback** -Schnittstelle wird verwendet, um Benachrichtigungen zu einem Download zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="1a23f-105">The **IDODownloadStatusCallback** interface is used to receive notifications about a download.</span></span>

## <a name="methods"></a><span data-ttu-id="1a23f-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="1a23f-106">Methods</span></span>

<span data-ttu-id="1a23f-107">Die **idodownloadstatus Callback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1a23f-107">The **IDODownloadStatusCallback** interface has these methods.</span></span>

| <span data-ttu-id="1a23f-108">Methode</span><span class="sxs-lookup"><span data-stu-id="1a23f-108">Method</span></span> | <span data-ttu-id="1a23f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a23f-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="1a23f-110">Idodownloadstatucallback:: onstatuschge</span><span class="sxs-lookup"><span data-stu-id="1a23f-110">IDODownloadStatusCallback::OnStatusChanged</span></span>](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | <span data-ttu-id="1a23f-111">Ruft die Implementierung dieser Methode immer dann auf, wenn sich ein Download Status geändert hat.</span><span class="sxs-lookup"><span data-stu-id="1a23f-111">DO calls your implementation of this method any time a download status has changed.</span></span> |

## <a name="requirements"></a><span data-ttu-id="1a23f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a23f-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="1a23f-113">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="1a23f-113">**Minimum supported client**</span></span> | <span data-ttu-id="1a23f-114">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="1a23f-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="1a23f-115">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="1a23f-115">**Minimum supported server**</span></span> | <span data-ttu-id="1a23f-116">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="1a23f-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="1a23f-117">**Header**</span><span class="sxs-lookup"><span data-stu-id="1a23f-117">**Header**</span></span> | <span data-ttu-id="1a23f-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="1a23f-118">Do.h</span></span> |