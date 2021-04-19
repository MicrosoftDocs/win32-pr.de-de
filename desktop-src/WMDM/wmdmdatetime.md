---
title: Wmdmdatetime-Struktur
description: Die wmdmdatetime-Struktur enthält ein Datum und eine Uhrzeit.
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- Wmdmdatetime-Struktur Windows Media Device Manager
- Pwmdmdatetime-Struktur Zeiger Windows Media-Device Manager
topic_type:
- apiref
api_name:
- WMDMDATETIME
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07acf706aa63a21edd27fb2ac206db3039249055
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359212"
---
# <a name="wmdmdatetime-structure"></a><span data-ttu-id="26f9f-105">Wmdmdatetime-Struktur</span><span class="sxs-lookup"><span data-stu-id="26f9f-105">WMDMDATETIME structure</span></span>

<span data-ttu-id="26f9f-106">Die **wmdmdatetime** -Struktur enthält ein Datum und eine Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="26f9f-106">The **WMDMDATETIME** structure contains a date and time of day.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f9f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="26f9f-107">Syntax</span></span>


```C++
typedef struct _WMDMDATETIME {
  WORD wYear;
  WORD wMonth;
  WORD wDay;
  WORD wHour;
  WORD wMinute;
  WORD wSecond;
} WMDMDATETIME, *PWMDMDATETIME;
```



## <a name="members"></a><span data-ttu-id="26f9f-108">Member</span><span class="sxs-lookup"><span data-stu-id="26f9f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="26f9f-109">**wYear**</span><span class="sxs-lookup"><span data-stu-id="26f9f-109">**wYear**</span></span>
</dt> <dd>

<span data-ttu-id="26f9f-110">Word, das die vierstellige Jahres Angabe enthält.</span><span class="sxs-lookup"><span data-stu-id="26f9f-110">Word containing the four-digit year.</span></span>

</dd> <dt>

<span data-ttu-id="26f9f-111">**wMonth**</span><span class="sxs-lookup"><span data-stu-id="26f9f-111">**wMonth**</span></span>
</dt> <dd>

<span data-ttu-id="26f9f-112">Word, das den Monat (1-12) enthält.</span><span class="sxs-lookup"><span data-stu-id="26f9f-112">Word containing the month (1-12).</span></span>

</dd> <dt>

<span data-ttu-id="26f9f-113">**wDay**</span><span class="sxs-lookup"><span data-stu-id="26f9f-113">**wDay**</span></span>
</dt> <dd>

<span data-ttu-id="26f9f-114">Word, das den Tag des Monats enthält (1-31).</span><span class="sxs-lookup"><span data-stu-id="26f9f-114">Word containing the day of the month (1-31).</span></span>

</dd> <dt>

<span data-ttu-id="26f9f-115">**wHour**</span><span class="sxs-lookup"><span data-stu-id="26f9f-115">**wHour**</span></span>
</dt> <dd>

<span data-ttu-id="26f9f-116">Word, das die Stunde (0-23) enthält.</span><span class="sxs-lookup"><span data-stu-id="26f9f-116">Word containing the hour (0-23).</span></span>

</dd> <dt>

<span data-ttu-id="26f9f-117">**wMinute**</span><span class="sxs-lookup"><span data-stu-id="26f9f-117">**wMinute**</span></span>
</dt> <dd>

<span data-ttu-id="26f9f-118">Word, das die Minute (0-59) enthält.</span><span class="sxs-lookup"><span data-stu-id="26f9f-118">Word containing the minute (0-59).</span></span>

</dd> <dt>

<span data-ttu-id="26f9f-119">**wSecond**</span><span class="sxs-lookup"><span data-stu-id="26f9f-119">**wSecond**</span></span>
</dt> <dd>

<span data-ttu-id="26f9f-120">Word, das das zweite enthält (0-59).</span><span class="sxs-lookup"><span data-stu-id="26f9f-120">Word containing the second (0-59).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26f9f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26f9f-121">Requirements</span></span>



| <span data-ttu-id="26f9f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26f9f-122">Requirement</span></span> | <span data-ttu-id="26f9f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="26f9f-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="26f9f-124">Header</span><span class="sxs-lookup"><span data-stu-id="26f9f-124">Header</span></span><br/> | <dl> <span data-ttu-id="26f9f-125"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="26f9f-125"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26f9f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26f9f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f9f-127">**Imdspstorage:: GETDATE**</span><span class="sxs-lookup"><span data-stu-id="26f9f-127">**IMDSPStorage::GetDate**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[<span data-ttu-id="26f9f-128">**Iwmdmstorage:: GETDATE**</span><span class="sxs-lookup"><span data-stu-id="26f9f-128">**IWMDMStorage::GetDate**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[<span data-ttu-id="26f9f-129">**Wmdmrights**</span><span class="sxs-lookup"><span data-stu-id="26f9f-129">**WMDMRIGHTS**</span></span>](wmdmrights.md)
</dt> <dt>

[<span data-ttu-id="26f9f-130">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="26f9f-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





