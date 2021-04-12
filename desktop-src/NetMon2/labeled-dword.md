---
description: Die Bezeichnung \_ DWORD-Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter DWORD-Eigenschafts Wert erkannt wird.
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: LABELED_DWORD Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_DWORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0bec068622683172116bf8c4f6e88450d5752920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217171"
---
# <a name="labeled_dword-structure"></a><span data-ttu-id="ef723-103">Bezeichnete \_ DWORD-Struktur</span><span class="sxs-lookup"><span data-stu-id="ef723-103">LABELED\_DWORD structure</span></span>

<span data-ttu-id="ef723-104">Die **Bezeichnung \_ DWORD** -Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter DWORD-Eigenschafts Wert erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="ef723-104">The **LABELED\_DWORD** structure defines a label that is displayed when a specific DWORD property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef723-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef723-105">Syntax</span></span>


```C++
typedef struct _LABELED_DWORD {
  DWORD Value;
  LPSTR Label;
} LABELED_DWORD, *LPLABELED_DWORD;
```



## <a name="members"></a><span data-ttu-id="ef723-106">Member</span><span class="sxs-lookup"><span data-stu-id="ef723-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ef723-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ef723-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="ef723-108">Der DWORD-Wert der Eigenschaft, die Sie erkennen möchten.</span><span class="sxs-lookup"><span data-stu-id="ef723-108">DWORD value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="ef723-109">**Label**</span><span class="sxs-lookup"><span data-stu-id="ef723-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="ef723-110">Die Textbeschreibung oder Bezeichnung, die angezeigt wird, wenn der im **Wertmember** angegebene DWORD-Wert erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="ef723-110">Textual description or label that is displayed when the DWORD value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef723-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef723-111">Remarks</span></span>

<span data-ttu-id="ef723-112">Der **lplabeleddwordtable** -Member der [set](set.md) -Struktur verweist auf ein Array von **set** -Strukturen, die ein **oder mehrere** Bezeichnungs Member der DWORD-Wertpaare definieren.</span><span class="sxs-lookup"><span data-stu-id="ef723-112">The **lpLabeledDwordTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the DWORD value pairs.</span></span> <span data-ttu-id="ef723-113">Die Paare werden verwendet, wenn Sie eine Bezeichnung anstelle eines bestimmten DWORD-Werts anzeigen möchten, der im Protokoll Paket enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ef723-113">The pairs are used when you want to display a label in place of a specific DWORD value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef723-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef723-114">Requirements</span></span>



| <span data-ttu-id="ef723-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef723-115">Requirement</span></span> | <span data-ttu-id="ef723-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ef723-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ef723-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef723-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ef723-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef723-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ef723-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef723-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ef723-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef723-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ef723-121">Header</span><span class="sxs-lookup"><span data-stu-id="ef723-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef723-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef723-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef723-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef723-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef723-124">SET</span><span class="sxs-lookup"><span data-stu-id="ef723-124">SET</span></span>](set.md)
</dt> </dl>

 

 




