---
title: SNB (objidl. h)
description: Ein String Name Block (SNB) ist ein Zeiger auf ein Array von Zeigern auf Zeichen folgen, die mit einem NULL-Zeiger enden.
ms.assetid: 8428a820-3d8a-41e0-9955-d355440e2ebc
keywords:
- SNB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d6860204d9f232c2ffafa4f1f16a1187fee8de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949650"
---
# <a name="snb"></a><span data-ttu-id="ab756-104">SNB</span><span class="sxs-lookup"><span data-stu-id="ab756-104">SNB</span></span>

<span data-ttu-id="ab756-105">Ein String Name Block (**SNB**) ist ein Zeiger auf ein Array von Zeigern auf Zeichen folgen, die mit einem **null** -Zeiger enden.</span><span class="sxs-lookup"><span data-stu-id="ab756-105">A string name block (**SNB**) is a pointer to an array of pointers to strings, that ends in a **NULL** pointer.</span></span> <span data-ttu-id="ab756-106">Zeichen folgen Namen Blöcke werden von der [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle und von Funktionsaufrufen verwendet, die Speicher Objekte öffnen.</span><span class="sxs-lookup"><span data-stu-id="ab756-106">String name blocks are used by the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface and by function calls that open storage objects.</span></span> <span data-ttu-id="ab756-107">Die Zeichen folgen zeigen auf enthaltene Speicher Objekte oder Streams, die in den geöffneten aufrufen ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ab756-107">The strings point to contained storage objects or streams that are to be excluded in the open calls.</span></span>


```C++
typedef OLESTR** SNB;
```



<dl> <dt>

<span data-ttu-id="ab756-108">**SNB**</span><span class="sxs-lookup"><span data-stu-id="ab756-108">**SNB**</span></span>
</dt> <dd>

<span data-ttu-id="ab756-109">\[Wire \_ Marshal (wiresnb)\]</span><span class="sxs-lookup"><span data-stu-id="ab756-109">\[wire\_marshal(wireSNB)\]</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab756-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab756-110">Remarks</span></span>

<span data-ttu-id="ab756-111">Die **SNB** sollte durch Zuordnen eines zusammenhängenden Speicherblocks erstellt werden, in dem auf die Zeiger auf Zeichen folgen ein **null** -Zeiger folgt, auf den dann die eigentlichen Zeichen folgen folgen.</span><span class="sxs-lookup"><span data-stu-id="ab756-111">The **SNB** should be created by allocating a contiguous block of memory in which the pointers to strings are followed by a **NULL** pointer, which is then followed by the actual strings.</span></span>

<span data-ttu-id="ab756-112">Das Marshalling einer **SNB** basiert auf der Annahme, dass die übergebene **SNB** auf diese Weise erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ab756-112">The marshaling of an **SNB** is based on the assumption that the **SNB** that was passed in was created in this way.</span></span> <span data-ttu-id="ab756-113">Obwohl es auf andere Weise gespeichert werden kann, hat die auf diese Weise erstellte **SNB** den Vorteil, dass nur ein Belegungs Vorgang und eine Freigabe des Arbeitsspeichers für alle Zeichen folgen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ab756-113">Although it could be stored in other ways, the **SNB** created in this manner has the advantage of requiring only one allocation operation and one freeing of memory for all the strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab756-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab756-114">Requirements</span></span>



| <span data-ttu-id="ab756-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab756-115">Requirement</span></span> | <span data-ttu-id="ab756-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ab756-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab756-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab756-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ab756-118">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ab756-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ab756-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab756-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ab756-120">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ab756-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ab756-121">Header</span><span class="sxs-lookup"><span data-stu-id="ab756-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab756-122"><dt>Objidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab756-122"><dt>Objidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="ab756-123">IDL</span><span class="sxs-lookup"><span data-stu-id="ab756-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ab756-124"><dt>Objidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ab756-124"><dt>Objidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab756-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab756-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab756-126">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="ab756-126">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> </dl>

 

 





