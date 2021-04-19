---
description: Die bezeichnete \_ Wort Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter Word-Eigenschafts Wert erkannt wird.
ms.assetid: bfb1d34e-4a07-493f-8e43-508b77cce581
title: LABELED_WORD Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_WORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 445b24245d2e9d15c1c2b6d69de20c464cbf1724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363627"
---
# <a name="labeled_word-structure"></a><span data-ttu-id="5441c-103">Bezeichnete \_ Wort Struktur</span><span class="sxs-lookup"><span data-stu-id="5441c-103">LABELED\_WORD structure</span></span>

<span data-ttu-id="5441c-104">Die **bezeichnete \_ Wort** Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter Word-Eigenschafts Wert erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="5441c-104">The **LABELED\_WORD** structure defines a label that is displayed when a specific WORD property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="5441c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5441c-105">Syntax</span></span>


```C++
typedef struct _LABELED_WORD {
  WORD  Value;
  LPSTR Label;
} LABELED_WORD, *LPLABELED_WORD;
```



## <a name="members"></a><span data-ttu-id="5441c-106">Member</span><span class="sxs-lookup"><span data-stu-id="5441c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5441c-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5441c-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="5441c-108">Der Wortwert der Eigenschaft, die Sie erkennen möchten.</span><span class="sxs-lookup"><span data-stu-id="5441c-108">WORD value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="5441c-109">**Label**</span><span class="sxs-lookup"><span data-stu-id="5441c-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="5441c-110">Die Textbeschreibung oder Bezeichnung, die angezeigt wird, wenn der im **Wertmember** angegebene Wortwert erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="5441c-110">Textual description or label that is displayed when the WORD value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5441c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5441c-111">Remarks</span></span>

<span data-ttu-id="5441c-112">Der **lplabeledwordtable** -Member der [set](set.md) -Struktur verweist auf ein Array von Set-Strukturen, um ein oder mehrere Bezeichnungs Wert Paare zu definieren.</span><span class="sxs-lookup"><span data-stu-id="5441c-112">The **lpLabeledWordTable** member of the [SET](set.md) structure points to an array of SET structures to define one or more label value pairs.</span></span> <span data-ttu-id="5441c-113">Diese Paare werden verwendet, wenn Sie eine Bezeichnung anstelle eines bestimmten Wort Werts anzeigen möchten, der in einem Protokoll Paket enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="5441c-113">These pairs are used when you want to display a label in place of a specific WORD value that is found in a protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="5441c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5441c-114">Requirements</span></span>



| <span data-ttu-id="5441c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5441c-115">Requirement</span></span> | <span data-ttu-id="5441c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5441c-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5441c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5441c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5441c-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5441c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5441c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5441c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5441c-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5441c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5441c-121">Header</span><span class="sxs-lookup"><span data-stu-id="5441c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5441c-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5441c-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5441c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5441c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5441c-124">SET</span><span class="sxs-lookup"><span data-stu-id="5441c-124">SET</span></span>](set.md)
</dt> </dl>

 

 




