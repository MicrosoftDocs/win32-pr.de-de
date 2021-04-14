---
title: D2D1_TAG (D2D1. h)
description: Ein Anwendungs definierter 64-Bit-Wert, der für \ 160; verwendet wird, markiert einen Satz von Renderingvorgängen.
ms.assetid: 4f363295-f140-4149-ba78-3abbc56eebe8
keywords:
- D2D1_TAG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacd11aa016e64ed463f1809595c865ae7e1f124
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340577"
---
# <a name="d2d1_tag"></a><span data-ttu-id="1efaa-104">D2D1- \_ Tag</span><span class="sxs-lookup"><span data-stu-id="1efaa-104">D2D1\_TAG</span></span>

<span data-ttu-id="1efaa-105">Ein von der Anwendung definierter 64-Bit-Wert, mit dem ein Satz von Renderingvorgängen markiert wird.</span><span class="sxs-lookup"><span data-stu-id="1efaa-105">An application-defined 64-bit value used to mark a set of rendering operations.</span></span>


```C++
typedef UINT64 D2D1_TAG;
```



## <a name="remarks"></a><span data-ttu-id="1efaa-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1efaa-106">Remarks</span></span>

<span data-ttu-id="1efaa-107">Verwenden Sie die [**ID2D1RenderTarget:: settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) -Methode, um ein Tag vor einer Reihe von Renderingvorgängen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1efaa-107">To set a tag before a series of rendering operations, use the [**ID2D1RenderTarget::SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) method.</span></span> <span data-ttu-id="1efaa-108">Um das aktuelle Tag abzurufen, verwenden Sie die [**ID2D1RenderTarget:: gettags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1efaa-108">To retrieve the current tag, use the [**ID2D1RenderTarget::GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1efaa-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1efaa-109">Requirements</span></span>



| <span data-ttu-id="1efaa-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1efaa-110">Requirement</span></span> | <span data-ttu-id="1efaa-111">Wert</span><span class="sxs-lookup"><span data-stu-id="1efaa-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1efaa-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1efaa-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1efaa-113">Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1efaa-113">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="1efaa-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1efaa-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1efaa-115">Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1efaa-115">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="1efaa-116">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="1efaa-116">Minimum supported phone</span></span><br/>  | <span data-ttu-id="1efaa-117">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="1efaa-117">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="1efaa-118">Header</span><span class="sxs-lookup"><span data-stu-id="1efaa-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1efaa-119"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="1efaa-119"><dt>D2d1.h</dt></span></span> </dl>                                                        |



## <a name="see-also"></a><span data-ttu-id="1efaa-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1efaa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1efaa-121">**GetTags**</span><span class="sxs-lookup"><span data-stu-id="1efaa-121">**GetTags**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)
</dt> <dt>

[<span data-ttu-id="1efaa-122">**Settags**</span><span class="sxs-lookup"><span data-stu-id="1efaa-122">**SetTags**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)
</dt> </dl>

 

