---
description: Legt die Anzahl von Arbeitsthreads fest, die von einem Video Decoder verwendet werden.
ms.assetid: A1570BB5-62BC-46C0-B9C9-61F99AA13BBE
title: CODECAPI_AVDecNumWorkerThreads-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d7c57d1b4176ad65313a5583a70f9ba4f7427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346669"
---
# <a name="codecapi_avdecnumworkerthreads-property"></a><span data-ttu-id="449ec-103">Codecapi \_ avdecnumworkerthreads (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="449ec-103">CODECAPI\_AVDecNumWorkerThreads property</span></span>

<span data-ttu-id="449ec-104">Legt die Anzahl von Arbeitsthreads fest, die von einem Video Decoder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="449ec-104">Sets the number of worker threads that are used by a video decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="449ec-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="449ec-105">Data type</span></span>

<span data-ttu-id="449ec-106">**Long** (**VT \_ I4**)</span><span class="sxs-lookup"><span data-stu-id="449ec-106">**LONG** (**VT\_I4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="449ec-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="449ec-107">Property GUID</span></span>

<span data-ttu-id="449ec-108">Codecapi \_ avdecnumworkerthreads</span><span class="sxs-lookup"><span data-stu-id="449ec-108">CODECAPI\_AVDecNumWorkerThreads</span></span>

## <a name="remarks"></a><span data-ttu-id="449ec-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="449ec-109">Remarks</span></span>

<span data-ttu-id="449ec-110">Wenn der Wert 1 ist, wählt der Decoder die Anzahl der Threads aus.</span><span class="sxs-lookup"><span data-stu-id="449ec-110">If the value is  1, the decoder selects the number of threads.</span></span>

<span data-ttu-id="449ec-111">Legen Sie diese Eigenschaft für die [**icodecapi**](/windows/desktop/api/strmif/nn-strmif-icodecapi) -Schnittstelle als **Long** -Wert fest (**VT \_ I4**).</span><span class="sxs-lookup"><span data-stu-id="449ec-111">For the [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) interface, set this property as a **LONG** value (**VT\_I4**).</span></span> <span data-ttu-id="449ec-112">Legen Sie diese Eigenschaft für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle als **UInt32** fest, obwohl der Wert signiert ist.</span><span class="sxs-lookup"><span data-stu-id="449ec-112">For the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface, set this property as a **UINT32**, although the value is signed.</span></span>

## <a name="requirements"></a><span data-ttu-id="449ec-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="449ec-113">Requirements</span></span>



| <span data-ttu-id="449ec-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="449ec-114">Requirement</span></span> | <span data-ttu-id="449ec-115">Wert</span><span class="sxs-lookup"><span data-stu-id="449ec-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="449ec-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="449ec-116">Minimum supported client</span></span><br/> | <span data-ttu-id="449ec-117">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="449ec-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="449ec-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="449ec-118">Minimum supported server</span></span><br/> | <span data-ttu-id="449ec-119">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="449ec-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="449ec-120">Header</span><span class="sxs-lookup"><span data-stu-id="449ec-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="449ec-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="449ec-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="449ec-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="449ec-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="449ec-123">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="449ec-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="449ec-124">**Icodecapi**</span><span class="sxs-lookup"><span data-stu-id="449ec-124">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

