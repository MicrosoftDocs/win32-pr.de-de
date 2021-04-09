---
description: Die bezeichnete \_ largeint-Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter largeint-Eigenschafts Wert erkannt wird.
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: LABELED_LARGEINT Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_LARGEINT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4de92c3e67567ef86bb3d46905e595bd9d54c194
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042325"
---
# <a name="labeled_largeint-structure"></a><span data-ttu-id="cc937-103">Bezeichnung \_ largeint-Struktur</span><span class="sxs-lookup"><span data-stu-id="cc937-103">LABELED\_LARGEINT structure</span></span>

<span data-ttu-id="cc937-104">Die **bezeichnete \_ largeint** -Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter largeint-Eigenschafts Wert erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="cc937-104">The **LABELED\_LARGEINT** structure defines a label that is displayed when a specific LARGEINT property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc937-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc937-105">Syntax</span></span>


```C++
typedef struct _LABELED_LARGEINT {
  LARGE_INTEGER Value;
  LPSTR         Label;
} LABELED_LARGEINT, *LPLABELED_LARGEINT;
```



## <a name="members"></a><span data-ttu-id="cc937-106">Member</span><span class="sxs-lookup"><span data-stu-id="cc937-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cc937-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="cc937-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="cc937-108">Largeint-Wert der Eigenschaft, die Sie erkennen möchten.</span><span class="sxs-lookup"><span data-stu-id="cc937-108">LARGEINT value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="cc937-109">**Label**</span><span class="sxs-lookup"><span data-stu-id="cc937-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="cc937-110">Die Textbeschreibung oder Bezeichnung, die angezeigt wird, wenn der im **Wertmember** angegebene largeint-Wert erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="cc937-110">Textual description or label that is displayed when the LARGEINT value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc937-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc937-111">Remarks</span></span>

<span data-ttu-id="cc937-112">Der **lplabeledlargeintting** -Member der [set](set.md) -Struktur verweist auf ein Array von **set** -Strukturen, die ein **oder mehrere** Bezeichnungs Member der largeint-Wertpaare definieren.</span><span class="sxs-lookup"><span data-stu-id="cc937-112">The **lpLabeledLargeIntTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the LARGEINT value pairs.</span></span> <span data-ttu-id="cc937-113">Die Paare werden verwendet, wenn Sie eine Bezeichnung anstelle eines bestimmten largeint-Werts anzeigen möchten, der in einem Protokoll Paket enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="cc937-113">The pairs are used when you want to display a label in place of a specific LARGEINT value that is found in a protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc937-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc937-114">Requirements</span></span>



| <span data-ttu-id="cc937-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc937-115">Requirement</span></span> | <span data-ttu-id="cc937-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cc937-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cc937-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc937-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cc937-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc937-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cc937-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc937-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cc937-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc937-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cc937-121">Header</span><span class="sxs-lookup"><span data-stu-id="cc937-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc937-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc937-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc937-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc937-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc937-124">SET</span><span class="sxs-lookup"><span data-stu-id="cc937-124">SET</span></span>](set.md)
</dt> </dl>

 

 




