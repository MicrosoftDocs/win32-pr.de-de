---
title: IWMPControls2 Step-Methode
description: Die Step-Methode bewirkt, dass das aktuelle Video Medien Element in den nächsten Frame oder den vorherigen Frame geht und die Wiedergabe fixiert.
ms.assetid: c5cb720f-527f-45b6-ae8a-4da0e3e34618
keywords:
- Step-Methode (Windows Media Player)
- Step-Methode, Windows Media Player, IWMPControls2-Schnittstelle
- IWMPControls2 Interface, Windows Media Player, Step-Methode
topic_type:
- apiref
api_name:
- IWMPControls2.step
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cfb65dd20de506a8f303121b23668e2fbf14dc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371747"
---
# <a name="iwmpcontrols2step-method"></a><span data-ttu-id="80706-106">IWMPControls2:: Step-Methode</span><span class="sxs-lookup"><span data-stu-id="80706-106">IWMPControls2::step method</span></span>

<span data-ttu-id="80706-107">Die **Step** -Methode bewirkt, dass das aktuelle Video Medien Element in den nächsten Frame oder den vorherigen Frame geht und die Wiedergabe fixiert.</span><span class="sxs-lookup"><span data-stu-id="80706-107">The **step** method causes the current video media item to step to the next frame or the previous frame and freeze playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="80706-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="80706-108">Syntax</span></span>


```CSharp
public void step(
  System.Int32 lStep
);
```


```VB

Public Sub step( _
  ByVal lStep As System.Int32 _
)
Implements IWMPControls2.step
```





## <a name="parameters"></a><span data-ttu-id="80706-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="80706-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80706-110">*LStep* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80706-110">*lStep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80706-111">Ein **System. Int32** -Wert, der angibt, wie viele Frames vor dem Einfrieren durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="80706-111">A **System.Int32** value indicating how many frames to step before freezing.</span></span> <span data-ttu-id="80706-112">Muss auf 1 oder-1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="80706-112">Must be set to 1 or -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80706-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80706-113">Return value</span></span>

<span data-ttu-id="80706-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="80706-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="80706-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80706-115">Remarks</span></span>

<span data-ttu-id="80706-116">Diese Methode unterstützt derzeit nur die Parameter 1 oder-1, sodass Sie nur einen Frame gleichzeitig ausführen können.</span><span class="sxs-lookup"><span data-stu-id="80706-116">This method currently supports only the parameters 1 or -1, so you can only step one frame at a time.</span></span>

## <a name="requirements"></a><span data-ttu-id="80706-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80706-117">Requirements</span></span>



| <span data-ttu-id="80706-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80706-118">Requirement</span></span> | <span data-ttu-id="80706-119">Wert</span><span class="sxs-lookup"><span data-stu-id="80706-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80706-120">Version</span><span class="sxs-lookup"><span data-stu-id="80706-120">Version</span></span><br/>   | <span data-ttu-id="80706-121">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="80706-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="80706-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="80706-122">Namespace</span></span><br/> | <span data-ttu-id="80706-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="80706-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="80706-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="80706-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="80706-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="80706-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80706-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80706-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80706-127">**IWMPControls2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="80706-127">**IWMPControls2 Interface (VB and C#)**</span></span>](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="80706-128">**Iwmpdvd-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="80706-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





