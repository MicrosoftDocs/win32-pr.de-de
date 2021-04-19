---
title: Iwmpcdromburn-startburn-Methode
description: Die startburn-Methode verbrennt die CD.
ms.assetid: e852c011-5f54-469f-aead-37fa711ef876
keywords:
- startburn-Methode (Windows Media Player)
- startburn-Methode, Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, startburn-Methode
topic_type:
- apiref
api_name:
- IWMPCdromBurn.startBurn
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe185d8993286e4be3935b43f6c1e9757623309d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369131"
---
# <a name="iwmpcdromburnstartburn-method"></a><span data-ttu-id="8c6ff-106">Iwmpcdromburn:: startburn-Methode</span><span class="sxs-lookup"><span data-stu-id="8c6ff-106">IWMPCdromBurn::startBurn method</span></span>

<span data-ttu-id="8c6ff-107">Die **startburn** -Methode verbrennt die CD.</span><span class="sxs-lookup"><span data-stu-id="8c6ff-107">The **startBurn** method burns the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c6ff-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c6ff-108">Syntax</span></span>


```CSharp
public void startBurn();
```


```VB

Public Sub startBurn()
Implements IWMPCdromBurn.startBurn
```





## <a name="parameters"></a><span data-ttu-id="8c6ff-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c6ff-109">Parameters</span></span>

<span data-ttu-id="8c6ff-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8c6ff-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c6ff-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c6ff-111">Return value</span></span>

<span data-ttu-id="8c6ff-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8c6ff-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c6ff-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c6ff-113">Remarks</span></span>

<span data-ttu-id="8c6ff-114">Vor dem Aufruf dieser Methode sollte " **burnstate** " den Wert "wmpbsready" oder "wmpbsbeendet" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8c6ff-114">The value of **burnstate** should be wmpbsReady or wmpbsStopped before calling this method.</span></span>

<span data-ttu-id="8c6ff-115">Diese Methode funktioniert nicht, wenn das CD-Laufwerk kein Brenner ist, oder wenn die Festplatte im Laufwerk nicht beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="8c6ff-115">This method will not work if the CD drive is not a burner, or if the disc in the drive is not writable.</span></span> <span data-ttu-id="8c6ff-116">Verwenden Sie **IsAvailable** , um zu bestimmen, ob eine CD gebrannt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8c6ff-116">Use **isAvailable** to determine whether a CD can be burned.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c6ff-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c6ff-117">Requirements</span></span>



| <span data-ttu-id="8c6ff-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c6ff-118">Requirement</span></span> | <span data-ttu-id="8c6ff-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8c6ff-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c6ff-120">Version</span><span class="sxs-lookup"><span data-stu-id="8c6ff-120">Version</span></span><br/>   | <span data-ttu-id="8c6ff-121">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="8c6ff-121">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="8c6ff-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="8c6ff-122">Namespace</span></span><br/> | <span data-ttu-id="8c6ff-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8c6ff-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8c6ff-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="8c6ff-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8c6ff-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8c6ff-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c6ff-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c6ff-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c6ff-127">**Iwmpcdromburn-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="8c6ff-127">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8c6ff-128">**Iwmpcdromburn. burnstate (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="8c6ff-128">**IWMPCdromBurn.burnState (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8c6ff-129">**Iwmpcdromburn. IsAvailable (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="8c6ff-129">**IWMPCdromBurn.isAvailable (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8c6ff-130">**Iwmpcdromburn. stopburn (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="8c6ff-130">**IWMPCdromBurn.stopBurn (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)
</dt> </dl>

 

 





