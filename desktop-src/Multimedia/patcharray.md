---
title: Patcharray (MMSYSTEM. h)
description: Patcharray ist ein Typ, der verwendet wird, um ein Array von MIDI-Patches zu definieren.
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- patcharray midipatchsize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e07af0e878fc0d2fc79d6d17aafd48fbd991fb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859306"
---
# <a name="patcharray"></a><span data-ttu-id="debcd-104">Patcharray</span><span class="sxs-lookup"><span data-stu-id="debcd-104">PATCHARRAY</span></span>

<span data-ttu-id="debcd-105">Patcharray ist ein Typ, der verwendet wird, um ein Array von MIDI-Patches zu definieren.</span><span class="sxs-lookup"><span data-stu-id="debcd-105">PATCHARRAY is a type used to define an array of MIDI patches.</span></span>


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

<span data-ttu-id="debcd-106">**patcharray \[ midipatchsize\]**</span><span class="sxs-lookup"><span data-stu-id="debcd-106">**PATCHARRAY\[MIDIPATCHSIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="debcd-107">Jedes Element im Array entspricht einem Patch, wobei jedes der 16 Bits einen der 16-MIDI-Kanäle darstellt.</span><span class="sxs-lookup"><span data-stu-id="debcd-107">Each element in the array corresponds to a patch with each of the 16 bits representing one of the 16 MIDI channels.</span></span> <span data-ttu-id="debcd-108">Bits werden für jeden der Kanäle festgelegt, die diesen bestimmten Patch verwenden.</span><span class="sxs-lookup"><span data-stu-id="debcd-108">Bits are set for each of the channels that use that particular patch.</span></span> <span data-ttu-id="debcd-109">Wenn beispielsweise die Patchnummer 0 von den physischen MIDI-Kanälen 0 und 8 verwendet wird, sollte Element 0 des Arrays auf 0x0101 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="debcd-109">For example, if patch number 0 is used by physical MIDI channels 0 and 8, element 0 of the array should be set to 0x0101.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="debcd-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="debcd-110">Requirements</span></span>



| <span data-ttu-id="debcd-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="debcd-111">Requirement</span></span> | <span data-ttu-id="debcd-112">Wert</span><span class="sxs-lookup"><span data-stu-id="debcd-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="debcd-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="debcd-113">Minimum supported client</span></span><br/> | <span data-ttu-id="debcd-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="debcd-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="debcd-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="debcd-115">Minimum supported server</span></span><br/> | <span data-ttu-id="debcd-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="debcd-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="debcd-117">Version</span><span class="sxs-lookup"><span data-stu-id="debcd-117">Version</span></span><br/>                  | <span data-ttu-id="debcd-118">Digital Instrumentation Digital Interface (MIDI), MIDI-Typen</span><span class="sxs-lookup"><span data-stu-id="debcd-118">Musical Instrument Digital Interface (MIDI), MIDI Types</span></span><br/>                                        |
| <span data-ttu-id="debcd-119">Header</span><span class="sxs-lookup"><span data-stu-id="debcd-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="debcd-120"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="debcd-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="debcd-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="debcd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="debcd-122">MIDI-Typen</span><span class="sxs-lookup"><span data-stu-id="debcd-122">MIDI Types</span></span>](midi-event-types.md)
</dt> </dl>

 

 





