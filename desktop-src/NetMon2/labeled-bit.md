---
description: Die bezeichnete \_ bitstruktur definiert ein Bezeichnungs bitpaar.
ms.assetid: 500b5159-bf9f-49d4-8567-d8e462015eb0
title: LABELED_BIT Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BIT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 24a56e832600b551dd3ab43ea93d59c5805af630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354529"
---
# <a name="labeled_bit-structure"></a><span data-ttu-id="fef7d-103">Bezeichnete \_ bitstruktur</span><span class="sxs-lookup"><span data-stu-id="fef7d-103">LABELED\_BIT structure</span></span>

<span data-ttu-id="fef7d-104">Die **bezeichnete \_ bitstruktur** definiert ein Bezeichnungs bitpaar.</span><span class="sxs-lookup"><span data-stu-id="fef7d-104">The **LABELED\_BIT** structure defines a label BIT pair.</span></span>

## <a name="syntax"></a><span data-ttu-id="fef7d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fef7d-105">Syntax</span></span>


```C++
typedef struct _LABELED_BIT {
  BYTE  BitNumber;
  LPSTR LabelOff;
  LPSTR LabelOn;
} LABELED_BIT, *LPLABELED_BIT;
```



## <a name="members"></a><span data-ttu-id="fef7d-106">Member</span><span class="sxs-lookup"><span data-stu-id="fef7d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fef7d-107">**Bitzahl**</span><span class="sxs-lookup"><span data-stu-id="fef7d-107">**BitNumber**</span></span>
</dt> <dd>

<span data-ttu-id="fef7d-108">Bitnummer des Bezeichnungs bitpaars.</span><span class="sxs-lookup"><span data-stu-id="fef7d-108">BIT number of the label BIT pair.</span></span> <span data-ttu-id="fef7d-109">Die Werte reichen von 0 bis 255.</span><span class="sxs-lookup"><span data-stu-id="fef7d-109">Values range from 0 to 255.</span></span> <span data-ttu-id="fef7d-110">Legen Sie den **bitnumber** -Member auf das Bit fest, das beim Vergleich des Eigenschafts Werts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fef7d-110">Set the **Bitnumber** member to the BIT used in the comparison of the property value.</span></span>

</dd> <dt>

<span data-ttu-id="fef7d-111">**Labeloff**</span><span class="sxs-lookup"><span data-stu-id="fef7d-111">**LabelOff**</span></span>
</dt> <dd>

<span data-ttu-id="fef7d-112">Eine Zeichenfolge oder Bezeichnung, die angezeigt wird, wenn das in **bitnumber** angegebene Bit 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="fef7d-112">String or label that is displayed when the BIT specified in **BitNumber** equals zero.</span></span> <span data-ttu-id="fef7d-113">Eine mögliche Bezeichnung ist beispielsweise "Bit Off".</span><span class="sxs-lookup"><span data-stu-id="fef7d-113">For example, a possible label is "Bit OFF".</span></span>

</dd> <dt>

<span data-ttu-id="fef7d-114">**Labelon**</span><span class="sxs-lookup"><span data-stu-id="fef7d-114">**LabelOn**</span></span>
</dt> <dd>

<span data-ttu-id="fef7d-115">Eine Zeichenfolge oder Bezeichnung, die angezeigt wird, wenn das in **bitnumber** angegebene Bit 1 entspricht.</span><span class="sxs-lookup"><span data-stu-id="fef7d-115">String or label that is displayed when the BIT specified in **BitNumber** equals 1.</span></span> <span data-ttu-id="fef7d-116">Eine mögliche Bezeichnung ist beispielsweise "Bit ein".</span><span class="sxs-lookup"><span data-stu-id="fef7d-116">For example, a possible label is "Bit ON".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fef7d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fef7d-117">Remarks</span></span>

<span data-ttu-id="fef7d-118">Ein Array mit **beschrifteten \_ bitstrukturen** wird verwendet, um einen Satz von Bezeichnungs Bit Paaren zu definieren.</span><span class="sxs-lookup"><span data-stu-id="fef7d-118">An array of **LABELED\_BIT** structures is used to define a set of label BIT pairs.</span></span> <span data-ttu-id="fef7d-119">Ein Zeiger auf das Array wird im **lplabeledbit** -Member der [set](set.md) -Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="fef7d-119">A pointer to the array is specified in the **lpLabeledBit** member of the [SET](set.md) structure.</span></span> <span data-ttu-id="fef7d-120">Die Paare werden verwendet, wenn Sie eine Bezeichnung auf der Grundlage der Einstellung der einzelnen Bits anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="fef7d-120">The pairs are used when you want to display a label based on the setting of each BIT.</span></span> <span data-ttu-id="fef7d-121">In der Regel wird dieser Typ von Set verwendet, um den ein-oder ausschalten-Wert von Bits anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fef7d-121">Typically, this type of set is used to indicate the ON or OFF value of BITs.</span></span>

<span data-ttu-id="fef7d-122">Wenn ein Bit festgelegt wird, zeigt Netzwerkmonitor nur die Bits an, die im Array der **Mengen Strukturen enthalten** sind.</span><span class="sxs-lookup"><span data-stu-id="fef7d-122">When a BIT set is specified, Network Monitor displays only the BITs included in the array of **SET** structures.</span></span> <span data-ttu-id="fef7d-123">Bits, die sich nicht in der **Set** -Struktur befinden, werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fef7d-123">BITs that are not in the **SET** structure are not displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="fef7d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fef7d-124">Requirements</span></span>



| <span data-ttu-id="fef7d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fef7d-125">Requirement</span></span> | <span data-ttu-id="fef7d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="fef7d-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fef7d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fef7d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fef7d-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fef7d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fef7d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fef7d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fef7d-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fef7d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fef7d-131">Header</span><span class="sxs-lookup"><span data-stu-id="fef7d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="fef7d-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="fef7d-132"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fef7d-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fef7d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fef7d-134">SET</span><span class="sxs-lookup"><span data-stu-id="fef7d-134">SET</span></span>](set.md)
</dt> </dl>

 

 




