---
title: Keyarray (MMSYSTEM. h)
description: Keyarray gibt einen Typ an, der verwendet wird, um ein Array von Schlüsseln zu definieren.
ms.assetid: af1a1d2f-4558-4374-93ab-5a705fc879ca
keywords:
- keyarray midipatchsize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e45e46417fb3b6653ecae605aa60f775c1d654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346716"
---
# <a name="keyarray"></a><span data-ttu-id="77a1b-104">Keyarray</span><span class="sxs-lookup"><span data-stu-id="77a1b-104">KEYARRAY</span></span>

<span data-ttu-id="77a1b-105">Keyarray gibt einen Typ an, der verwendet wird, um ein Array von Schlüsseln zu definieren.</span><span class="sxs-lookup"><span data-stu-id="77a1b-105">KEYARRAY specifies a type used to define an array of keys.</span></span>


```C++
typedef WORD KEYARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

<span data-ttu-id="77a1b-106">**keyarray \[ midipatchsize\]**</span><span class="sxs-lookup"><span data-stu-id="77a1b-106">**KEYARRAY\[MIDIPATCHSIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="77a1b-107">Jedes Element im Array entspricht einem Key-basierten Percussion-Patch, wobei jede der 16 Bits einen der 16 MIDI-Kanäle darstellt.</span><span class="sxs-lookup"><span data-stu-id="77a1b-107">Each element in the array corresponds to a key-based percussion patch with each of the 16 bits representing one of the 16 MIDI channels.</span></span> <span data-ttu-id="77a1b-108">Bits werden für jeden der Kanäle festgelegt, die diesen bestimmten Patch verwenden.</span><span class="sxs-lookup"><span data-stu-id="77a1b-108">Bits are set for each of the channels that use that particular patch.</span></span> <span data-ttu-id="77a1b-109">Wenn beispielsweise der Percussion-Patch für die Schlüsselnummer 60 von den physischen MIDI-Kanälen 9 und 15 verwendet wird, sollte das Element 60 des Arrays auf 0x8200 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="77a1b-109">For example, if the percussion patch for key number 60 is used by physical MIDI channels 9 and 15, element 60 of the array should be set to 0x8200.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77a1b-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77a1b-110">Requirements</span></span>



| <span data-ttu-id="77a1b-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77a1b-111">Requirement</span></span> | <span data-ttu-id="77a1b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="77a1b-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77a1b-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77a1b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="77a1b-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77a1b-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="77a1b-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77a1b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="77a1b-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77a1b-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="77a1b-117">Version</span><span class="sxs-lookup"><span data-stu-id="77a1b-117">Version</span></span><br/>                  | <span data-ttu-id="77a1b-118">Digital Instrumentation Digital Interface (MIDI), MIDI-Typen</span><span class="sxs-lookup"><span data-stu-id="77a1b-118">Musical Instrument Digital Interface (MIDI), MIDI Types</span></span><br/>                                        |
| <span data-ttu-id="77a1b-119">Header</span><span class="sxs-lookup"><span data-stu-id="77a1b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="77a1b-120"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="77a1b-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77a1b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77a1b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77a1b-122">MIDI-Typen</span><span class="sxs-lookup"><span data-stu-id="77a1b-122">MIDI Types</span></span>](midi-event-types.md)
</dt> </dl>

 

 





