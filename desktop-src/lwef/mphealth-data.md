---
title: MPHEALTH_DATA Struktur (mpclient. h)
description: Integritäts Benachrichtigungs Daten.
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- MPHEALTH_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPHEALTH_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPHEALTH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e729bdea82b6a885b64e95ecd77f9deae6bff4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343052"
---
# <a name="mphealth_data-structure"></a><span data-ttu-id="812ad-105">Mphealth- \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="812ad-105">MPHEALTH\_DATA structure</span></span>

<span data-ttu-id="812ad-106">Integritäts Benachrichtigungs Daten.</span><span class="sxs-lookup"><span data-stu-id="812ad-106">Health notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="812ad-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="812ad-107">Syntax</span></span>


```C++
typedef struct tagMPHEALTH_DATA {
  DWORD dwNotificationType;
  DWORD dwNotificationFlag;
} MPHEALTH_DATA, *PMPHEALTH_DATA;
```



## <a name="members"></a><span data-ttu-id="812ad-108">Member</span><span class="sxs-lookup"><span data-stu-id="812ad-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="812ad-109">**dwnotificationtype**</span><span class="sxs-lookup"><span data-stu-id="812ad-109">**dwNotificationType**</span></span>
</dt> <dd>

<span data-ttu-id="812ad-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="812ad-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="812ad-111">Hier wird der Benachrichtigungstyp angegeben.</span><span class="sxs-lookup"><span data-stu-id="812ad-111">Type of notification.</span></span>

</dd> <dt>

<span data-ttu-id="812ad-112">**dwnotificationflag**</span><span class="sxs-lookup"><span data-stu-id="812ad-112">**dwNotificationFlag**</span></span>
</dt> <dd>

<span data-ttu-id="812ad-113">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="812ad-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="812ad-114">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="812ad-114">Unused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="812ad-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="812ad-115">Requirements</span></span>



| <span data-ttu-id="812ad-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="812ad-116">Requirement</span></span> | <span data-ttu-id="812ad-117">Wert</span><span class="sxs-lookup"><span data-stu-id="812ad-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="812ad-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="812ad-118">Minimum supported client</span></span><br/> | <span data-ttu-id="812ad-119">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="812ad-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="812ad-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="812ad-120">Minimum supported server</span></span><br/> | <span data-ttu-id="812ad-121">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="812ad-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="812ad-122">Header</span><span class="sxs-lookup"><span data-stu-id="812ad-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="812ad-123"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="812ad-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





