---
description: Ein Rückruf, der den Host von Frame Puffer-Informationen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.
MS-HAID: vspixengine.IFrameBufferCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_double\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iframebuffercallback:: resultCallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F0276125-2DA9-45BC-A295-BD67C21EE601
api_name:
- IFrameBufferCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5433c7bbf5fe67455b60fd754eecb2c2877c5d6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124616"
---
# <a name="span-idvspixengineiframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arrspaniframebuffercallbackresultcallback-method"></a><span data-ttu-id="c6b6e-103"><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>Iframebuffercallback:: resultCallback-Methode</span><span class="sxs-lookup"><span data-stu-id="c6b6e-103"><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>IFrameBufferCallback::ResultCallback method</span></span>

<span data-ttu-id="c6b6e-104">Ein Rückruf, der den Host von Frame Puffer-Informationen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-104">A callback that notifies the host of framebuffer information returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6b6e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6b6e-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD   frameNumber,
   DWORD   width,
   DWORD   height,
   DWORD   renderTargetPtr,
   double  frameDuraction,
   DWORD   size,
   BYTE [] count5_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="c6b6e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6b6e-106">Parameters</span></span>

<span data-ttu-id="c6b6e-107">*Framezahl* </span><span class="sxs-lookup"><span data-stu-id="c6b6e-107">*frameNumber* </span></span>  
<span data-ttu-id="c6b6e-108">Die Rahmennummer.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-108">The frame number.</span></span>

<span data-ttu-id="c6b6e-109">*Breite* </span><span class="sxs-lookup"><span data-stu-id="c6b6e-109">*width* </span></span>  
<span data-ttu-id="c6b6e-110">Die Breite des Frames.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-110">The width of the frame.</span></span>

<span data-ttu-id="c6b6e-111">*Flugh* </span><span class="sxs-lookup"><span data-stu-id="c6b6e-111">*height* </span></span>  
<span data-ttu-id="c6b6e-112">Die Höhe des Frames.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-112">The height of the frame.</span></span>

<span data-ttu-id="c6b6e-113">*rendertargetptr* </span><span class="sxs-lookup"><span data-stu-id="c6b6e-113">*renderTargetPtr* </span></span>  
<span data-ttu-id="c6b6e-114">Das Renderziel, von dem die Ergebnisse stammen.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-114">The render target that the results come from.</span></span> <span data-ttu-id="c6b6e-115">Es ist immer ein Slot, der von der Frame Puffer Anforderung angegeben wird, oder wenn es sich nicht um einen Draw-Befehl handelt, springt der erste RTV-Befehl zur Ausgabe Quelle.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-115">It is always a slot specified by the frame buffer request, or if not a draw call, then the first RTV bount to the output source.</span></span>

<span data-ttu-id="c6b6e-116">*frameduraction* </span><span class="sxs-lookup"><span data-stu-id="c6b6e-116">*frameDuraction* </span></span>  
<span data-ttu-id="c6b6e-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-117">Not used.</span></span>

<span data-ttu-id="c6b6e-118">*Größe* </span><span class="sxs-lookup"><span data-stu-id="c6b6e-118">*size* </span></span>  
<span data-ttu-id="c6b6e-119">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-119">The size of the output buffer in bytes.</span></span>

<span data-ttu-id="c6b6e-120">*count5- \_ Puffer* </span><span class="sxs-lookup"><span data-stu-id="c6b6e-120">*count5\_buffer* </span></span>  
<span data-ttu-id="c6b6e-121">Der Inhalt des Renderziels im \_ unorm-Format R8G8B8A8.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-121">The contents of the render target in R8G8B8A8\_UNORM format.</span></span>

## <a name="return-value"></a><span data-ttu-id="c6b6e-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6b6e-122">Return value</span></span>

<span data-ttu-id="c6b6e-123">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c6b6e-124">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6b6e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6b6e-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c6b6e-126">Header</span><span class="sxs-lookup"><span data-stu-id="c6b6e-126">Header</span></span></p></td><td><span data-ttu-id="c6b6e-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c6b6e-127">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c6b6e-128"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6b6e-128"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c6b6e-129">**Iframebuffercallback**</span><span class="sxs-lookup"><span data-stu-id="c6b6e-129">**IFrameBufferCallback**</span></span>](/windows/desktop/direct3dtools/iframebuffercallback)

 

 
