---
description: 'Die waitforreceivetocomplete-Methode wartet auf den Abschluss der cbaserdenderer:: Receive-Methode.'
ms.assetid: 3c722680-e54b-4ba1-8e98-36647cd027bc
title: Cbaserderderer. waitforreceivetocomplete-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForReceiveToComplete
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9033474c71d23fed106205839071bad200df6a23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358202"
---
# <a name="cbaserendererwaitforreceivetocomplete-method"></a><span data-ttu-id="61b14-103">Cbaserderderer. waitforreceivetocomplete-Methode</span><span class="sxs-lookup"><span data-stu-id="61b14-103">CBaseRenderer.WaitForReceiveToComplete method</span></span>

<span data-ttu-id="61b14-104">Die- `WaitForReceiveToComplete` Methode wartet auf den Abschluss der [**cbaserdenderer:: Receive**](cbaserenderer-receive.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="61b14-104">The `WaitForReceiveToComplete` method waits for the [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method to complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="61b14-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="61b14-105">Syntax</span></span>


```C++
void WaitForReceiveToComplete();
```



## <a name="parameters"></a><span data-ttu-id="61b14-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="61b14-106">Parameters</span></span>

<span data-ttu-id="61b14-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="61b14-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="61b14-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61b14-108">Return value</span></span>

<span data-ttu-id="61b14-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="61b14-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="61b14-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61b14-110">Remarks</span></span>

<span data-ttu-id="61b14-111">Mit den [**cbaserenderer::**](cbaserenderer-stop.md) und [**cbaserenderer:: beginflush**](cbaserenderer-beginflush.md) -Methoden wird diese Methode aufgerufen, um die Zustandsänderung mit der **Receive** -Methode zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="61b14-111">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call this method to synchronize the state change with the **Receive** method.</span></span>

<span data-ttu-id="61b14-112">Diese Methode sendet Nachrichten, während Sie darauf wartet, dass das [**cbaserdenderer:: m \_ binreceive**](cbaserenderer-m-binreceive.md) -Flag auf " **false**" wird.</span><span class="sxs-lookup"><span data-stu-id="61b14-112">Specifically, this method dispatches messages while it waits for the [**CBaseRenderer::m\_bInReceive**](cbaserenderer-m-binreceive.md) flag to become **FALSE**.</span></span> <span data-ttu-id="61b14-113">Das Flag wird in der [**cbaserererererererermethode**](cbaserenderer-preparereceive.md) " **true** "::P der Analysemethode "" und wechselt zurück zu " **false** ", nachdem die **Receive** -Methode die [**cbasererderderer**](cbaserenderer-preparerender.md) -Methode aufgerufen hat::P</span><span class="sxs-lookup"><span data-stu-id="61b14-113">The flag becomes **TRUE** in the [**CBaseRenderer::PrepareReceive**](cbaserenderer-preparereceive.md) method and switches back to **FALSE** after the **Receive** method calls the [**CBaseRenderer::PrepareRender**](cbaserenderer-preparerender.md) method.</span></span> <span data-ttu-id="61b14-114">Die abgeleitete Klasse kann **preparerender** zum Festlegen der Palette verwenden.</span><span class="sxs-lookup"><span data-stu-id="61b14-114">The derived class can use **PrepareRender** to set the palette.</span></span> <span data-ttu-id="61b14-115">Durch das warten auf den Abschluss der **Vorbereitung** wird sichergestellt, dass palettenänderungs Meldungen vor der Zustandsänderung weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="61b14-115">Waiting for **PrepareRender** to complete ensures that palette-change messages are dispatched before the state change occurs.</span></span> <span data-ttu-id="61b14-116">Dadurch wird ein potenzieller Deadlock vermieden.</span><span class="sxs-lookup"><span data-stu-id="61b14-116">This avoids a potential deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="61b14-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61b14-117">Requirements</span></span>



| <span data-ttu-id="61b14-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61b14-118">Requirement</span></span> | <span data-ttu-id="61b14-119">Wert</span><span class="sxs-lookup"><span data-stu-id="61b14-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61b14-120">Header</span><span class="sxs-lookup"><span data-stu-id="61b14-120">Header</span></span><br/>  | <dl> <span data-ttu-id="61b14-121"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61b14-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="61b14-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="61b14-122">Library</span></span><br/> | <dl> <span data-ttu-id="61b14-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="61b14-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61b14-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61b14-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61b14-125">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="61b14-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




