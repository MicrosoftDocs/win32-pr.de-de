---
title: D2D1_SIZE_F (D2DBaseTypes. h)
description: Speichert ein geordnetes Paar von Gleit Komma Zahlen, in der Regel die Breite und Höhe eines Rechtecks.
ms.assetid: c2fd41fb-72b3-418b-ad87-65549b04657d
keywords:
- D2D1_SIZE_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a031e1e6a1e9ad7d6975f3dea63427655aa92f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475867"
---
# <a name="d2d1_size_f"></a><span data-ttu-id="53d4b-104">D2D1 \_ size \_ F</span><span class="sxs-lookup"><span data-stu-id="53d4b-104">D2D1\_SIZE\_F</span></span>

<span data-ttu-id="53d4b-105">Speichert ein geordnetes Paar von Gleit Komma Zahlen, in der Regel die Breite und Höhe eines Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="53d4b-105">Stores an ordered pair of floats, typically the width and height of a rectangle.</span></span>


```C++
typedef D2D_SIZE_F D2D1_SIZE_F;
```



## <a name="remarks"></a><span data-ttu-id="53d4b-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53d4b-106">Remarks</span></span>

<span data-ttu-id="53d4b-107">Ebenso wie Punkte sind Größen ein weiteres wichtiges Grafikkonzept.</span><span class="sxs-lookup"><span data-stu-id="53d4b-107">Like points, sizes are another important graphics concept.</span></span> <span data-ttu-id="53d4b-108">In Direct2D werden Größen durch die Strukturen **D2D1 \_ size \_ F** oder [**D2D1 \_ size \_ U**](d2d1-size-u.md) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="53d4b-108">In Direct2D, sizes are represented by the **D2D1\_SIZE\_F** or [**D2D1\_SIZE\_U**](d2d1-size-u.md) structures.</span></span> <span data-ttu-id="53d4b-109">Beide enthalten ein geordnetes Paar von Zahlen, in der Regel die Breite und Höhe eines Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="53d4b-109">Both contain an ordered pair of numbers, typically the width and height of a rectangle.</span></span> <span data-ttu-id="53d4b-110">Die **D2D1 \_ size \_ F** -Struktur enthält ein geordnetes Paar von Gleit **Komma Werten,** und die Struktur **D2D1 \_ size \_ U** enthält ein geordnetes Paar von **UInt32** -Werten.</span><span class="sxs-lookup"><span data-stu-id="53d4b-110">The **D2D1\_SIZE\_F** structure contains an ordered pair of **FLOAT** values, and the **D2D1\_SIZE\_U** structure contains an ordered pair of **UINT32** values.</span></span>

<span data-ttu-id="53d4b-111">**D2D1 \_ Size \_ f** ist ein neuer Name für einen bereits definierten Typ **D2D \_ size \_ f**.</span><span class="sxs-lookup"><span data-stu-id="53d4b-111">**D2D1\_SIZE\_F** is a new name for an already defined type **D2D\_SIZE\_F**.</span></span> <span data-ttu-id="53d4b-112">Eine Liste der von **D2D1 \_ size \_ f** bereitgestellten Felder finden Sie unter **D2D \_ size \_ f**.</span><span class="sxs-lookup"><span data-stu-id="53d4b-112">For a list of the fields provided by **D2D1\_SIZE\_F**, see **D2D\_SIZE\_F**.</span></span>

## <a name="requirements"></a><span data-ttu-id="53d4b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53d4b-113">Requirements</span></span>



| <span data-ttu-id="53d4b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53d4b-114">Requirement</span></span> | <span data-ttu-id="53d4b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="53d4b-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53d4b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53d4b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="53d4b-117">Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="53d4b-117">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="53d4b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53d4b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="53d4b-119">Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="53d4b-119">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="53d4b-120">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="53d4b-120">Minimum supported phone</span></span><br/>  | <span data-ttu-id="53d4b-121">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="53d4b-121">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="53d4b-122">Header</span><span class="sxs-lookup"><span data-stu-id="53d4b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="53d4b-123"><dt>D2DBaseTypes. h (Include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53d4b-123"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="53d4b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53d4b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53d4b-125">**D2D \_ size \_ F**</span><span class="sxs-lookup"><span data-stu-id="53d4b-125">**D2D\_SIZE\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f)
</dt> <dt>

[<span data-ttu-id="53d4b-126">**D2D1 \_ Größe \_ U**</span><span class="sxs-lookup"><span data-stu-id="53d4b-126">**D2D1\_SIZE\_U**</span></span>](d2d1-size-u.md)
</dt> <dt>

[<span data-ttu-id="53d4b-127">**D2D1 \_ Punkt \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="53d4b-127">**D2D1\_POINT\_2F**</span></span>](d2d1-point-2f.md)
</dt> </dl>

 

