---
title: MPDETECTION_ORIGIN-Enumeration (mpclient. h)
description: Der Erkennungs Ursprung.
ms.assetid: 9FEE2FAD-3E44-4134-B968-53E971F6B092
keywords:
- MPDETECTION_ORIGIN-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPDETECTION_ORIGIN enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPDETECTION_ORIGIN
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4224aafef2c72db2a8d3b27f338ca83feaf64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338722"
---
# <a name="mpdetection_origin-enumeration"></a><span data-ttu-id="ec2ec-105">Mperkennungs- \_ Ursprungs Enumeration</span><span class="sxs-lookup"><span data-stu-id="ec2ec-105">MPDETECTION\_ORIGIN enumeration</span></span>

<span data-ttu-id="ec2ec-106">Der Erkennungs Ursprung.</span><span class="sxs-lookup"><span data-stu-id="ec2ec-106">Detection origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec2ec-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec2ec-107">Syntax</span></span>


```C++
typedef enum tagMPDETECTION_ORIGIN { 
  MPDETECTION_ORIGIN_UNKNOWN        = 0,
  MPDETECTION_ORIGIN_LOCAL_MACHINE  = 1 << 0,
  MPDETECTION_ORIGIN_NETWORKSHARE   = 1 << 1,
  MPDETECTION_ORIGIN_INTERNET       = 1 << 2,
  MPDETECTION_ORIGIN_OUTBOUND       = 1 << 3,
  MPDETECTION_ORIGIN_INBOUND        = 1 << 4
} MPDETECTION_ORIGIN, *PMPDETECTION_ORIGIN;
```



## <a name="constants"></a><span data-ttu-id="ec2ec-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="ec2ec-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ec2ec-109"><span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**mperkennungs- \_ Ursprung \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="ec2ec-109"><span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**MPDETECTION\_ORIGIN\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="ec2ec-110">Die Bedrohung hat den Ursprung unbekannt erkannt.</span><span class="sxs-lookup"><span data-stu-id="ec2ec-110">Threat detected origin unknown.</span></span>

</dd> <dt>

<span data-ttu-id="ec2ec-111"><span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**mperkennungs- \_ Ursprungs \_ lokaler \_ Computer**</span><span class="sxs-lookup"><span data-stu-id="ec2ec-111"><span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**MPDETECTION\_ORIGIN\_LOCAL\_MACHINE**</span></span>
</dt> <dd>

<span data-ttu-id="ec2ec-112">Auf dem lokalen Computer wurde eine Bedrohung erkannt.</span><span class="sxs-lookup"><span data-stu-id="ec2ec-112">Threat detected on local machine.</span></span>

</dd> <dt>

<span data-ttu-id="ec2ec-113"><span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**mperkennungs- \_ Ursprung \_ networkshare**</span><span class="sxs-lookup"><span data-stu-id="ec2ec-113"><span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION\_ORIGIN\_NETWORKSHARE**</span></span>
</dt> <dd>

<span data-ttu-id="ec2ec-114">Bedrohungserkennung auf Netzwerkfreigabe.</span><span class="sxs-lookup"><span data-stu-id="ec2ec-114">Threat detected on network share.</span></span>

</dd> <dt>

<span data-ttu-id="ec2ec-115"><span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**mperkennungs- \_ Ursprungs \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="ec2ec-115"><span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**MPDETECTION\_ORIGIN\_INTERNET**</span></span>
</dt> <dd>

<span data-ttu-id="ec2ec-116">Die Bedrohung wurde im Internet erkannt.</span><span class="sxs-lookup"><span data-stu-id="ec2ec-116">Threat detected on internet.</span></span>

</dd> <dt>

<span data-ttu-id="ec2ec-117"><span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**mperkennungs- \_ Ursprungs \_ Ausgangspunkt**</span><span class="sxs-lookup"><span data-stu-id="ec2ec-117"><span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**MPDETECTION\_ORIGIN\_OUTBOUND**</span></span>
</dt> <dd>

<span data-ttu-id="ec2ec-118">Bedrohungserkennung für ausgehende Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="ec2ec-118">Threat detected on an outbound connection.</span></span>

</dd> <dt>

<span data-ttu-id="ec2ec-119"><span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**mperkennungs- \_ Ursprungs \_ Eingangs**</span><span class="sxs-lookup"><span data-stu-id="ec2ec-119"><span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**MPDETECTION\_ORIGIN\_INBOUND**</span></span>
</dt> <dd>

<span data-ttu-id="ec2ec-120">Die Bedrohung für eine eingehende Verbindung wurde erkannt.</span><span class="sxs-lookup"><span data-stu-id="ec2ec-120">Threat detected on an inbound connection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec2ec-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec2ec-121">Requirements</span></span>



| <span data-ttu-id="ec2ec-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec2ec-122">Requirement</span></span> | <span data-ttu-id="ec2ec-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ec2ec-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec2ec-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec2ec-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ec2ec-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec2ec-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ec2ec-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec2ec-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ec2ec-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec2ec-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec2ec-128">Header</span><span class="sxs-lookup"><span data-stu-id="ec2ec-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec2ec-129"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec2ec-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





