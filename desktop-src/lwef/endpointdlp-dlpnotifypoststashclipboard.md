---
description: Stellt dem System Statusinformationen bereit, nachdem ein Stash-Zwischenablagevorgang abgeschlossen wurde.
title: DlpNotifyPostStashClipboard-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: e549593acab6d74edf838a0f82952d8f3034bfcc
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495646"
---
# <a name="dlpnotifypoststashclipboard-function"></a><span data-ttu-id="e91a3-103">DlpNotifyPostStashClipboard-Funktion</span><span class="sxs-lookup"><span data-stu-id="e91a3-103">DlpNotifyPostStashClipboard function</span></span>

<span data-ttu-id="e91a3-104">Stellt dem System Statusinformationen bereit, nachdem ein Stash-Zwischenablagevorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="e91a3-104">Provides the system with status information after a stash clipboard operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e91a3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e91a3-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="e91a3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e91a3-106">Parameters</span></span>


<dl> <dt>

<span data-ttu-id="e91a3-107">*OpStatus* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e91a3-107">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e91a3-108">Ein Zeiger [](enpointdlp-dlp_postop_status.md) auf eine DLP_POSTOP_STATUS-Struktur, die Statusinformationen zum Stash-Zwischenablagevorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="e91a3-108">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the stash clipboard operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="e91a3-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e91a3-109">Return value</span></span>

<span data-ttu-id="e91a3-110">Gibt void zurück.</span><span class="sxs-lookup"><span data-stu-id="e91a3-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="e91a3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e91a3-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="e91a3-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e91a3-112">Requirements</span></span>



| <span data-ttu-id="e91a3-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e91a3-113">Requirement</span></span>          |    <span data-ttu-id="e91a3-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e91a3-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e91a3-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e91a3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e91a3-116">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="e91a3-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="e91a3-117">DLL</span><span class="sxs-lookup"><span data-stu-id="e91a3-117">DLL</span></span><br/>                      | <span data-ttu-id="e91a3-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="e91a3-118">EndpointDlp.dll</span></span> |