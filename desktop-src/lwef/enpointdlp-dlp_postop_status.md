---
description: Gibt Statusinformationen zu einem Endpunkt-DLP-Vorgang an.
title: DLP_POSTOP_STATUS-Struktur (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_POSTOP_STATUS
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: c0221926700fc8960de5ef4d25c36136c3fc9737
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495581"
---
# <a name="dlp_postop_status-structure"></a><span data-ttu-id="12c05-103">DLP_POSTOP_STATUS-Struktur</span><span class="sxs-lookup"><span data-stu-id="12c05-103">DLP_POSTOP_STATUS structure</span></span>

<span data-ttu-id="12c05-104">Gibt Statusinformationen zu einem Endpunkt-DLP-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="12c05-104">Specifies status information about an endpoint DLP operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="12c05-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="12c05-105">Syntax</span></span>


```C++
typedef struct _DLP_POSTOP_STATUS {
    
    DWORD Version;    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS; 
```


## <a name="members"></a><span data-ttu-id="12c05-106">Members</span><span class="sxs-lookup"><span data-stu-id="12c05-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="12c05-107">*Version* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="12c05-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12c05-108">Ein DWORD, das die API-Version angibt.</span><span class="sxs-lookup"><span data-stu-id="12c05-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="12c05-109">Dieser Wert sollte immer **DLP_POSTOP_STATUS_V_LATEST** sein.</span><span class="sxs-lookup"><span data-stu-id="12c05-109">This value should always be **DLP_POSTOP_STATUS_V_LATEST**.</span></span> <span data-ttu-id="12c05-110">Diese Konstante wird in der Beispielheaderdatei endpointdlp.h im Artikel Verhindern von [Endpunktdatenverlust](endpointdlp-endpoint-data-loss-prevention.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="12c05-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md)</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="12c05-111">*OperationSuccess* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="12c05-111">*OperationSuccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12c05-112">Eine BOOL, die angibt, ob der Öffnungsvorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="12c05-112">A BOOL indicating whether the open operation was successful.</span></span>

</dd> </dl>





## <a name="remarks"></a><span data-ttu-id="12c05-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12c05-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="12c05-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="12c05-114">Requirements</span></span>



| <span data-ttu-id="12c05-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12c05-115">Requirement</span></span>          |    <span data-ttu-id="12c05-116">Wert</span><span class="sxs-lookup"><span data-stu-id="12c05-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12c05-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12c05-117">Minimum supported client</span></span><br/> | <span data-ttu-id="12c05-118">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="12c05-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
