---
title: MPEXPIRATION_DATA Struktur (mpclient. h)
description: Status Benachrichtigung zum Produktablauf.
ms.assetid: BF464FFD-16AE-4F46-83CD-E0355478180C
keywords:
- MPEXPIRATION_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPEXPIRATION_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPEXPIRATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df5e417b1ce6b1d1f4c15d646b44b0ea6c1fade2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341358"
---
# <a name="mpexpiration_data-structure"></a><span data-ttu-id="066fc-105">Mpablauf- \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="066fc-105">MPEXPIRATION\_DATA structure</span></span>

<span data-ttu-id="066fc-106">Status Benachrichtigung zum Produktablauf.</span><span class="sxs-lookup"><span data-stu-id="066fc-106">Product expiration status notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="066fc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="066fc-107">Syntax</span></span>


```C++
typedef struct tagMPEXPIRATION_DATA {
  MP_EXPIRE_REASON       Reason;
  MP_EXPIRE_STATE_REPORT State;
} MPEXPIRATION_DATA, *PMPEXPIRATION_DATA;
```



## <a name="members"></a><span data-ttu-id="066fc-108">Member</span><span class="sxs-lookup"><span data-stu-id="066fc-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="066fc-109">**`Reason`**</span><span class="sxs-lookup"><span data-stu-id="066fc-109">**Reason**</span></span>
</dt> <dd>

<span data-ttu-id="066fc-110">Typ: **MP \_ läuft \_** ab</span><span class="sxs-lookup"><span data-stu-id="066fc-110">Type: **MP\_EXPIRE\_REASON**</span></span>

</dd> <dd>

<span data-ttu-id="066fc-111">Grund für den Ablauf.</span><span class="sxs-lookup"><span data-stu-id="066fc-111">Expiration reason.</span></span> <span data-ttu-id="066fc-112">Dies ist einer der folgenden möglichen Werte:</span><span class="sxs-lookup"><span data-stu-id="066fc-112">This is one of the following possible values:</span></span>



| <span data-ttu-id="066fc-113">Wert</span><span class="sxs-lookup"><span data-stu-id="066fc-113">Value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="066fc-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="066fc-114">Meaning</span></span>                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| <span id="MP_EXPIRED_UNKNOWN"></span><span id="mp_expired_unknown"></span><dl> <span data-ttu-id="066fc-115"><dt>**MP \_ Abgelaufenes \_ unbekannter**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="066fc-115"><dt>**MP\_EXPIRED\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="066fc-116">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="066fc-116">Unknown.</span></span><br/>    |
| <span id="MP_EXPIRED_EVAL"></span><span id="mp_expired_eval"></span><dl> <span data-ttu-id="066fc-117"><dt>**MP \_ Abgelaufene \_ eval**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="066fc-117"><dt>**MP\_EXPIRED\_EVAL**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="066fc-118">Beurteilung.</span><span class="sxs-lookup"><span data-stu-id="066fc-118">Evaluation.</span></span><br/> |
| <span id="MP_EXPIRED_WAT"></span><span id="mp_expired_wat"></span><dl> <span data-ttu-id="066fc-119"><dt>**MP \_ Abgelaufenes \_ Wat**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="066fc-119"><dt>**MP\_EXPIRED\_WAT**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="066fc-120">Wat.</span><span class="sxs-lookup"><span data-stu-id="066fc-120">WAT.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="066fc-121">**State**</span><span class="sxs-lookup"><span data-stu-id="066fc-121">**State**</span></span>
</dt> <dd>

<span data-ttu-id="066fc-122">Typ: **\_ Bericht zum \_ Status \_ "MP läuft** ab"</span><span class="sxs-lookup"><span data-stu-id="066fc-122">Type: **MP\_EXPIRE\_STATE\_REPORT**</span></span>

</dd> <dd>

<span data-ttu-id="066fc-123">Ablauf Status.</span><span class="sxs-lookup"><span data-stu-id="066fc-123">Expiration state.</span></span> <span data-ttu-id="066fc-124">Dies ist einer der folgenden möglichen Werte:</span><span class="sxs-lookup"><span data-stu-id="066fc-124">This is one of the following possible values:</span></span>



| <span data-ttu-id="066fc-125">Wert</span><span class="sxs-lookup"><span data-stu-id="066fc-125">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="066fc-126">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="066fc-126">Meaning</span></span>                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| <span id="MP_EXPIRE_STATE_REPORT_UNKNOWN"></span><span id="mp_expire_state_report_unknown"></span><dl> <span data-ttu-id="066fc-127"><dt>**MP \_ Ablauf \_ Status \_ Bericht \_ unbekannt**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="066fc-127"><dt>**MP\_EXPIRE\_STATE\_REPORT\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="066fc-128">Unbekannter Zustand.</span><span class="sxs-lookup"><span data-stu-id="066fc-128">State unknown.</span></span><br/> |
| <span id="MP_EXPIRE_STATE_REPORT_VALID"></span><span id="mp_expire_state_report_valid"></span><dl> <span data-ttu-id="066fc-129"><dt>**MP \_ Ablauf \_ Status \_ Bericht \_ gültig**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="066fc-129"><dt>**MP\_EXPIRE\_STATE\_REPORT\_VALID**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="066fc-130">Kein Ablauf.</span><span class="sxs-lookup"><span data-stu-id="066fc-130">No expiration.</span></span><br/> |
| <span id="MP_EXPIRE_STATE_REPORT_WARNING"></span><span id="mp_expire_state_report_warning"></span><dl> <span data-ttu-id="066fc-131"><dt>**MP \_ Ablauf \_ Status \_ Bericht \_ Warnung**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="066fc-131"><dt>**MP\_EXPIRE\_STATE\_REPORT\_WARNING**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="066fc-132">Fast abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="066fc-132">Near expired.</span></span><br/>  |
| <span id="MP_EXPIRE_STATE_REPORT_EXPIRED"></span><span id="mp_expire_state_report_expired"></span><dl> <span data-ttu-id="066fc-133"><dt>**MP \_ Ablauf \_ Status \_ Bericht \_ abgelaufen**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="066fc-133"><dt>**MP\_EXPIRE\_STATE\_REPORT\_EXPIRED**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="066fc-134">Frist.</span><span class="sxs-lookup"><span data-stu-id="066fc-134">Expired.</span></span><br/>       |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="066fc-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="066fc-135">Requirements</span></span>



| <span data-ttu-id="066fc-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="066fc-136">Requirement</span></span> | <span data-ttu-id="066fc-137">Wert</span><span class="sxs-lookup"><span data-stu-id="066fc-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="066fc-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="066fc-138">Minimum supported client</span></span><br/> | <span data-ttu-id="066fc-139">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="066fc-139">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="066fc-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="066fc-140">Minimum supported server</span></span><br/> | <span data-ttu-id="066fc-141">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="066fc-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="066fc-142">Header</span><span class="sxs-lookup"><span data-stu-id="066fc-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="066fc-143"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="066fc-143"><dt>MpClient.h</dt></span></span> </dl> |



 

 





