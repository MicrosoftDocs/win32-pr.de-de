---
title: MPTHREAT_INFOEX_NIS Struktur (mpclient. h)
description: Enthält NIS-spezifische Informationen.
ms.assetid: 3887C5BF-B1F6-4420-B40A-9585E44BE7A9
keywords:
- MPTHREAT_INFOEX_NIS Struktur Funktionen der Legacy-Windows-Umgebung
- PMPTHREAT_INFOEX_NIS Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_NIS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4ed68432a2d0ebe78535a139fcc7b0882b9ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040556"
---
# <a name="mpthreat_infoex_nis-structure"></a><span data-ttu-id="ae708-105">Mpthreat \_ INFOEX \_ NIS-Struktur</span><span class="sxs-lookup"><span data-stu-id="ae708-105">MPTHREAT\_INFOEX\_NIS structure</span></span>

<span data-ttu-id="ae708-106">Enthält NIS-spezifische Informationen.</span><span class="sxs-lookup"><span data-stu-id="ae708-106">Contains NIS-specific information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae708-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae708-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_NIS {
  MP_MIDL_STRING LPWSTR SourceIP;
  MP_MIDL_STRING LPWSTR DestinationIP;
  DWORD                 dwSourceport;
  DWORD                 dwDestinationport;
  MP_MIDL_STRING LPWSTR Protocol;
  MP_MIDL_STRING LPWSTR Link;
} MPTHREAT_INFOEX_NIS, *PMPTHREAT_INFOEX_NIS;
```



## <a name="members"></a><span data-ttu-id="ae708-108">Member</span><span class="sxs-lookup"><span data-stu-id="ae708-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ae708-109">**SourceIP**</span><span class="sxs-lookup"><span data-stu-id="ae708-109">**SourceIP**</span></span>
</dt> <dd>

<span data-ttu-id="ae708-110">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="ae708-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="ae708-111">**Destinationip**</span><span class="sxs-lookup"><span data-stu-id="ae708-111">**DestinationIP**</span></span>
</dt> <dd>

<span data-ttu-id="ae708-112">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="ae708-112">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="ae708-113">**dwsourceport**</span><span class="sxs-lookup"><span data-stu-id="ae708-113">**dwSourceport**</span></span>
</dt> <dd>

<span data-ttu-id="ae708-114">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ae708-114">Type: **DWORD**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="ae708-115">**dwdestinationport**</span><span class="sxs-lookup"><span data-stu-id="ae708-115">**dwDestinationport**</span></span>
</dt> <dd>

<span data-ttu-id="ae708-116">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ae708-116">Type: **DWORD**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="ae708-117">**Protokoll**</span><span class="sxs-lookup"><span data-stu-id="ae708-117">**Protocol**</span></span>
</dt> <dd>

<span data-ttu-id="ae708-118">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="ae708-118">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="ae708-119">**Link**</span><span class="sxs-lookup"><span data-stu-id="ae708-119">**Link**</span></span>
</dt> <dd>

<span data-ttu-id="ae708-120">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="ae708-120">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

<span data-ttu-id="ae708-121"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ae708-121"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ae708-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae708-122">Requirements</span></span>



| <span data-ttu-id="ae708-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae708-123">Requirement</span></span> | <span data-ttu-id="ae708-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ae708-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae708-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae708-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ae708-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae708-126">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ae708-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae708-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ae708-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae708-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae708-129">Header</span><span class="sxs-lookup"><span data-stu-id="ae708-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae708-130"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae708-130"><dt>MpClient.h</dt></span></span> </dl> |



 

 





