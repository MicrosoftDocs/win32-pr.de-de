---
title: Count. Selected-Eigenschaft
description: Ruft einen Wert ab, der angibt, ob der Leistungsindikators ausgewählt ist, oder legt ihn fest
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- Ausgewählte Eigenschaften-sysmon
- Ausgewählte Eigenschaft "sysmon", "zähltem"-Objekt
- Objekt "sysmon" für das-Objekt, ausgewählte Eigenschaft
topic_type:
- apiref
api_name:
- CounterItem.Selected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac707dfaf2ed379884395a08128ddaeda771fa00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956571"
---
# <a name="counteritemselected-property"></a><span data-ttu-id="74ae8-106">Count. Selected-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="74ae8-106">CounterItem.Selected property</span></span>

<span data-ttu-id="74ae8-107">Ruft einen Wert ab, der angibt, ob der Leistungsindikators ausgewählt ist, oder legt ihn fest</span><span class="sxs-lookup"><span data-stu-id="74ae8-107">Retrieves or sets a value that indicates if the counter is selected.</span></span>

<span data-ttu-id="74ae8-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="74ae8-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="74ae8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="74ae8-109">Syntax</span></span>


```VB
Property Selected As Boolean
```



## <a name="property-value"></a><span data-ttu-id="74ae8-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="74ae8-110">Property value</span></span>

<span data-ttu-id="74ae8-111">True, wenn der Counter ausgewählt ist. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="74ae8-111">True if the counter is selected; otherwise, false.</span></span>

## <a name="remarks"></a><span data-ttu-id="74ae8-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74ae8-112">Remarks</span></span>

<span data-ttu-id="74ae8-113">Sie können einen oder mehrere Indikatoren aus der Sammlung der Leistungsindikatoren auswählen.</span><span class="sxs-lookup"><span data-stu-id="74ae8-113">You can select one or more counters from the collection of counters.</span></span> <span data-ttu-id="74ae8-114">Wenn Sie einen Indikator auswählen, wählt den Indikator in der Legende aus, macht den Indikator in der Legende sichtbar und generiert ein [**oncounterselected**](-systemmonitor-oncounterselected.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="74ae8-114">Selecting a counter, selects the counter in the Legend, makes the counter visible in the Legend, and generates an [**OnCounterSelected**](-systemmonitor-oncounterselected.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="74ae8-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74ae8-115">Requirements</span></span>



| <span data-ttu-id="74ae8-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74ae8-116">Requirement</span></span> | <span data-ttu-id="74ae8-117">Wert</span><span class="sxs-lookup"><span data-stu-id="74ae8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74ae8-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74ae8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="74ae8-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74ae8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74ae8-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74ae8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="74ae8-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74ae8-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74ae8-122">DLL</span><span class="sxs-lookup"><span data-stu-id="74ae8-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74ae8-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="74ae8-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74ae8-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74ae8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74ae8-125">**Ratteritem**</span><span class="sxs-lookup"><span data-stu-id="74ae8-125">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





