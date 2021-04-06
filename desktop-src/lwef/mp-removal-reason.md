---
title: MP_REMOVAL_REASON-Enumeration (mpclient. h)
description: Grund für das Entfernen der FastPath-Signatur.
ms.assetid: A09B4903-E53C-4DA1-BD0B-6DE0124FCAB3
keywords:
- MP_REMOVAL_REASON-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMP_REMOVAL_REASON enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MP_REMOVAL_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ce70f46bd95d4183343990b40594326ed5d3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743185"
---
# <a name="mp_removal_reason-enumeration"></a><span data-ttu-id="10b39-105">MP- \_ Entfernungs \_ Grund-Enumeration</span><span class="sxs-lookup"><span data-stu-id="10b39-105">MP\_REMOVAL\_REASON enumeration</span></span>

<span data-ttu-id="10b39-106">Grund für das Entfernen der FastPath-Signatur.</span><span class="sxs-lookup"><span data-stu-id="10b39-106">FastPath signature removal reason.</span></span>

## <a name="syntax"></a><span data-ttu-id="10b39-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="10b39-107">Syntax</span></span>


```C++
typedef enum tagMP_REMOVAL_REASON { 
  MP_REMOVAL_UNKNOWN    = 0,
  MP_REMOVAL_MANUAL     = 1,
  MP_REMOVAL_AUTOMATIC  = 2
} MP_REMOVAL_REASON, *PMP_REMOVAL_REASON;
```



## <a name="constants"></a><span data-ttu-id="10b39-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="10b39-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="10b39-109"><span id="MP_REMOVAL_UNKNOWN"></span><span id="mp_removal_unknown"></span>**MP- \_ Entfernung \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="10b39-109"><span id="MP_REMOVAL_UNKNOWN"></span><span id="mp_removal_unknown"></span>**MP\_REMOVAL\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="10b39-110">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="10b39-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="10b39-111"><span id="MP_REMOVAL_MANUAL"></span><span id="mp_removal_manual"></span>**MP- \_ Entfernungs \_ Handbuch**</span><span class="sxs-lookup"><span data-stu-id="10b39-111"><span id="MP_REMOVAL_MANUAL"></span><span id="mp_removal_manual"></span>**MP\_REMOVAL\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="10b39-112">Manuelle Aktion.</span><span class="sxs-lookup"><span data-stu-id="10b39-112">Manual.</span></span>

</dd> <dt>

<span data-ttu-id="10b39-113"><span id="MP_REMOVAL_AUTOMATIC"></span><span id="mp_removal_automatic"></span>**MP- \_ Entfernung \_ automatisch**</span><span class="sxs-lookup"><span data-stu-id="10b39-113"><span id="MP_REMOVAL_AUTOMATIC"></span><span id="mp_removal_automatic"></span>**MP\_REMOVAL\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="10b39-114">Automatisch.</span><span class="sxs-lookup"><span data-stu-id="10b39-114">Automatic.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10b39-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10b39-115">Requirements</span></span>



| <span data-ttu-id="10b39-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10b39-116">Requirement</span></span> | <span data-ttu-id="10b39-117">Wert</span><span class="sxs-lookup"><span data-stu-id="10b39-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10b39-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10b39-118">Minimum supported client</span></span><br/> | <span data-ttu-id="10b39-119">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10b39-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="10b39-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10b39-120">Minimum supported server</span></span><br/> | <span data-ttu-id="10b39-121">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10b39-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10b39-122">Header</span><span class="sxs-lookup"><span data-stu-id="10b39-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="10b39-123"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="10b39-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





