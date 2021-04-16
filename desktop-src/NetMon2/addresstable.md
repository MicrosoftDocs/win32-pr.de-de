---
description: Die "adresssstable"-Struktur enthält eine Tabelle mit Adress Paaren.
ms.assetid: 84577b6c-9d43-4e53-9f8d-33685329b11d
title: Adresssstable-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 41acab19f83fdcc88a384c0407b666a7f641a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485403"
---
# <a name="addresstable-structure"></a><span data-ttu-id="b5cc7-103">Adresssstable-Struktur</span><span class="sxs-lookup"><span data-stu-id="b5cc7-103">ADDRESSTABLE structure</span></span>

<span data-ttu-id="b5cc7-104">Die " **adresssstable** "-Struktur enthält eine Tabelle mit Adress Paaren.</span><span class="sxs-lookup"><span data-stu-id="b5cc7-104">The **ADDRESSTABLE** structure contains a table of address pairs.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5cc7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5cc7-105">Syntax</span></span>


```C++
typedef struct _ADDRESSTABLE {
  DWORD       nAddressPairs;
  DWORD       nNonMacAddressPairs;
  ADDRESSPAIR AddressPair[MAX_ADDRESS_PAIRS];
} ADDRESSTABLE, *LPADDRESSTABLE;
```



## <a name="members"></a><span data-ttu-id="b5cc7-106">Member</span><span class="sxs-lookup"><span data-stu-id="b5cc7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b5cc7-107">**nadresssspairs**</span><span class="sxs-lookup"><span data-stu-id="b5cc7-107">**nAddressPairs**</span></span>
</dt> <dd>

<span data-ttu-id="b5cc7-108">Anzahl der Adress Paare im **adresssspair** -Array.</span><span class="sxs-lookup"><span data-stu-id="b5cc7-108">Number of address pairs in the **AddressPair** array.</span></span>

</dd> <dt>

<span data-ttu-id="b5cc7-109">**nnonmacadresssspairs**</span><span class="sxs-lookup"><span data-stu-id="b5cc7-109">**nNonMacAddressPairs**</span></span>
</dt> <dd>

<span data-ttu-id="b5cc7-110">Anzahl der nicht-Mac-Adress Paare.</span><span class="sxs-lookup"><span data-stu-id="b5cc7-110">Number of non-MAC address pairs.</span></span>

</dd> <dt>

<span data-ttu-id="b5cc7-111">**Adresssspair**</span><span class="sxs-lookup"><span data-stu-id="b5cc7-111">**AddressPair**</span></span>
</dt> <dd>

<span data-ttu-id="b5cc7-112">Array von Adress Paaren.</span><span class="sxs-lookup"><span data-stu-id="b5cc7-112">Array of address pairs.</span></span> <span data-ttu-id="b5cc7-113">Beachten Sie, dass Sie nur bis zu acht Adress Paare pro adresstabiler Struktur speichern können.</span><span class="sxs-lookup"><span data-stu-id="b5cc7-113">Note that you may only store up to eight address pairs per ADDRESSTABLE structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5cc7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5cc7-114">Remarks</span></span>

<span data-ttu-id="b5cc7-115">Verwenden Sie diese Struktur als Teil des Erfassungs Filter Erstellungs Prozesses.</span><span class="sxs-lookup"><span data-stu-id="b5cc7-115">Use this structure as part of the capture filter construction process.</span></span> <span data-ttu-id="b5cc7-116">Weitere Informationen zum Implementieren dieser Struktur finden Sie unter [Erfassungs Filter](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="b5cc7-116">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5cc7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5cc7-117">Requirements</span></span>



| <span data-ttu-id="b5cc7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5cc7-118">Requirement</span></span> | <span data-ttu-id="b5cc7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b5cc7-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b5cc7-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5cc7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b5cc7-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5cc7-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b5cc7-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5cc7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b5cc7-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5cc7-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b5cc7-124">Header</span><span class="sxs-lookup"><span data-stu-id="b5cc7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5cc7-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5cc7-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5cc7-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5cc7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5cc7-127">Adresssspair</span><span class="sxs-lookup"><span data-stu-id="b5cc7-127">ADDRESSPAIR</span></span>](addresspair.md)
</dt> <dt>

[<span data-ttu-id="b5cc7-128">Capturefilter</span><span class="sxs-lookup"><span data-stu-id="b5cc7-128">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




