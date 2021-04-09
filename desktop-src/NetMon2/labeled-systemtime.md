---
description: Die bezeichnete \_ SYSTEMTIME-Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter SYSTEMTIME-Eigenschafts Wert erkannt wird.
ms.assetid: 307b490a-af8e-4f2a-a45a-33a84fcb4d5c
title: LABELED_SYSTEMTIME Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_SYSTEMTIME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4484d5ec55f700410eb80d11d2249cceceef43ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868827"
---
# <a name="labeled_systemtime-structure"></a><span data-ttu-id="e9a67-103">Bezeichnete \_ SYSTEMTIME-Struktur</span><span class="sxs-lookup"><span data-stu-id="e9a67-103">LABELED\_SYSTEMTIME structure</span></span>

<span data-ttu-id="e9a67-104">Die **bezeichnete \_ SYSTEMTIME** -Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter SYSTEMTIME-Eigenschafts Wert erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="e9a67-104">The **LABELED\_SYSTEMTIME** structure defines a label that is displayed when a specific SYSTEMTIME property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9a67-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9a67-105">Syntax</span></span>


```C++
typedef struct _LABELED_SYSTEMTIME {
  SYSTEMTIME Value;
  LPSTR      Label;
} LABELED_SYSTEMTIME, *LPLABELED_SYSTEMTIME;
```



## <a name="members"></a><span data-ttu-id="e9a67-106">Member</span><span class="sxs-lookup"><span data-stu-id="e9a67-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9a67-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e9a67-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="e9a67-108">Der SystemTime-Wert einer Eigenschaft, die Sie erkennen möchten.</span><span class="sxs-lookup"><span data-stu-id="e9a67-108">SYSTEMTIME value of a property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="e9a67-109">**Label**</span><span class="sxs-lookup"><span data-stu-id="e9a67-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="e9a67-110">Die Textbeschreibung oder Bezeichnung, die angezeigt wird, wenn der im **Wertmember** angegebene SYSTEMTIME-Wert erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="e9a67-110">Textual description or label that is displayed when the SYSTEMTIME value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9a67-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9a67-111">Remarks</span></span>

<span data-ttu-id="e9a67-112">Der **lplabeledsystemtimetable** -Member der [set](set.md) -Struktur verweist auf ein Array von **set** -Strukturen, die ein oder mehrere Bezeichnungs Wert Paare definieren.</span><span class="sxs-lookup"><span data-stu-id="e9a67-112">The **lpLabeledSystemTimeTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more label value pairs.</span></span> <span data-ttu-id="e9a67-113">Die Paare werden verwendet, wenn Sie eine Bezeichnung anstelle eines bestimmten largeint-Werts anzeigen möchten, der im Protokoll Paket enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e9a67-113">The pairs are used when you want to display a label in place of a specific LARGEINT value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9a67-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9a67-114">Requirements</span></span>



| <span data-ttu-id="e9a67-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9a67-115">Requirement</span></span> | <span data-ttu-id="e9a67-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e9a67-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a67-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9a67-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e9a67-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9a67-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e9a67-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9a67-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e9a67-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9a67-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e9a67-121">Header</span><span class="sxs-lookup"><span data-stu-id="e9a67-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9a67-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9a67-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9a67-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9a67-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9a67-124">SET</span><span class="sxs-lookup"><span data-stu-id="e9a67-124">SET</span></span>](set.md)
</dt> </dl>

 

 




