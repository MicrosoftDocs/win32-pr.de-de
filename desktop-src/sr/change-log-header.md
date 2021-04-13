---
title: CHANGE_LOG_HEADER Struktur
description: Der Änderungsprotokoll Header.
ms.assetid: 24fee9a5-b073-474f-afd5-d81f66399936
keywords:
- CHANGE_LOG_HEADER Struktur System Wiederherstellung
- PCHANGE_LOG_HEADER Struktur Zeiger System Wiederherstellung
topic_type:
- apiref
api_name:
- CHANGE_LOG_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5512ff9c9e708095f38e3ae1dcf80ce2e0e4443b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391580"
---
# <a name="change_log_header-structure"></a><span data-ttu-id="1d451-105">\_Struktur der Protokoll \_ Kopfzeile ändern</span><span class="sxs-lookup"><span data-stu-id="1d451-105">CHANGE\_LOG\_HEADER structure</span></span>

<span data-ttu-id="1d451-106">\[Diese Informationen gelten nur für Windows XP mit Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="1d451-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="1d451-107">Der Änderungsprotokoll Header.</span><span class="sxs-lookup"><span data-stu-id="1d451-107">The change log header.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d451-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d451-108">Syntax</span></span>


```C++
typedef struct _CHANGE_LOG_HEADER {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwLogVersion;
  RECORD_HEADER DataHeader;
  BYTE          byteData[1];
} CHANGE_LOG_HEADER, *PCHANGE_LOG_HEADER;
```



## <a name="members"></a><span data-ttu-id="1d451-109">Member</span><span class="sxs-lookup"><span data-stu-id="1d451-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="1d451-110">**Recordheader**</span><span class="sxs-lookup"><span data-stu-id="1d451-110">**RecordHeader**</span></span>
</dt> <dd>

<span data-ttu-id="1d451-111">Eine [**Daten Satz \_ Header**](record-header.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1d451-111">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="1d451-112">Der **dwrecordtype** -Member sollte auf recordtypelogheader (0) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1d451-112">The **dwRecordType** member should be set to RecordTypeLogHeader (0).</span></span> <span data-ttu-id="1d451-113">Das **dwrecordsize** -Element muss alle Member sowie den zusätzlichen **DWORD** -Wert berücksichtigen, der diesem Header folgt.</span><span class="sxs-lookup"><span data-stu-id="1d451-113">The **dwRecordSize** member should account for all the members, plus the extra **DWORD** value that follows this header.</span></span> <span data-ttu-id="1d451-114">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="1d451-114">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1d451-115">**dwmagicnum**</span><span class="sxs-lookup"><span data-stu-id="1d451-115">**dwMagicNum**</span></span>
</dt> <dd>

<span data-ttu-id="1d451-116">Dieser Member sollte auf 0xabcdef12 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1d451-116">This member should be set to 0xabcdef12.</span></span>

</dd> <dt>

<span data-ttu-id="1d451-117">**dwlogversion**</span><span class="sxs-lookup"><span data-stu-id="1d451-117">**dwLogVersion**</span></span>
</dt> <dd>

<span data-ttu-id="1d451-118">Dieser Member sollte auf 2 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1d451-118">This member should be set to 2.</span></span>

</dd> <dt>

<span data-ttu-id="1d451-119">**Dataheader**</span><span class="sxs-lookup"><span data-stu-id="1d451-119">**DataHeader**</span></span>
</dt> <dd>

<span data-ttu-id="1d451-120">Eine [**Daten Satz \_ Header**](record-header.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1d451-120">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="1d451-121">Der **dwrecordtype** -Member sollte auf **recordtypevolumepath** (2) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1d451-121">The **dwRecordType** member should be set to **RecordTypeVolumePath** (2).</span></span>

</dd> <dt>

<span data-ttu-id="1d451-122">**bytedata**</span><span class="sxs-lookup"><span data-stu-id="1d451-122">**byteData**</span></span>
</dt> <dd>

<span data-ttu-id="1d451-123">Der Start einer auf NULL endenden Zeichenfolge, die den Volumepfad angibt.</span><span class="sxs-lookup"><span data-stu-id="1d451-123">The start of a null-terminated string that specifies the volume path.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d451-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d451-124">Remarks</span></span>

<span data-ttu-id="1d451-125">Auf diesen Header folgt ein **DWORD** -Wert, der mit dem Wert des **dwrecordsize** -Members von **recordheader** identisch sein sollte.</span><span class="sxs-lookup"><span data-stu-id="1d451-125">This header is followed by a **DWORD** value that should be identical to the value of the **dwRecordSize** member of **RecordHeader**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d451-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d451-126">Requirements</span></span>



| <span data-ttu-id="1d451-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d451-127">Requirement</span></span> | <span data-ttu-id="1d451-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1d451-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1d451-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d451-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1d451-130">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d451-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1d451-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d451-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1d451-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1d451-132">None supported</span></span><br/>                            |
| <span data-ttu-id="1d451-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="1d451-133">End of client support</span></span><br/>    | <span data-ttu-id="1d451-134">Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="1d451-134">Windows XP with SP2</span></span><br/>                       |



 

 





