---
title: Iwmpcdromburn-Löschmethode
description: Die Löschmethode löscht die aktuelle CD.
ms.assetid: ed0fbd7e-61a6-445a-bca5-ed2969d5cadc
keywords:
- Löschmethode für Windows-Media Player
- Löschmethode Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, Löschmethode
topic_type:
- apiref
api_name:
- IWMPCdromBurn.erase
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4e168142a6ee77081871bb7dbefa79de8031d71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365501"
---
# <a name="iwmpcdromburnerase-method"></a><span data-ttu-id="0ce8e-106">Iwmpcdromburn:: Erase-Methode</span><span class="sxs-lookup"><span data-stu-id="0ce8e-106">IWMPCdromBurn::erase method</span></span>

<span data-ttu-id="0ce8e-107">Die **Lösch** Methode löscht die aktuelle CD.</span><span class="sxs-lookup"><span data-stu-id="0ce8e-107">The **erase** method erases the current CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ce8e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ce8e-108">Syntax</span></span>


```CSharp
public void erase();
```


```VB

Public Sub erase()
Implements IWMPCdromBurn.erase
```





## <a name="parameters"></a><span data-ttu-id="0ce8e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ce8e-109">Parameters</span></span>

<span data-ttu-id="0ce8e-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0ce8e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ce8e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ce8e-111">Return value</span></span>

<span data-ttu-id="0ce8e-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0ce8e-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ce8e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ce8e-113">Remarks</span></span>

<span data-ttu-id="0ce8e-114">Diese Methode funktioniert nicht, wenn die Festplatte im Laufwerk nicht neu geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="0ce8e-114">This method will not work if the disc in the drive is not rewritable.</span></span> <span data-ttu-id="0ce8e-115">Verwenden Sie [iwmpcdromburn. IsAvailable](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) , um zu bestimmen, ob eine CD gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="0ce8e-115">Use [IWMPCdromBurn.isAvailable](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) to determine whether a CD can be erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ce8e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ce8e-116">Requirements</span></span>



| <span data-ttu-id="0ce8e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ce8e-117">Requirement</span></span> | <span data-ttu-id="0ce8e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="0ce8e-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ce8e-119">Version</span><span class="sxs-lookup"><span data-stu-id="0ce8e-119">Version</span></span><br/>   | <span data-ttu-id="0ce8e-120">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="0ce8e-120">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="0ce8e-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ce8e-121">Namespace</span></span><br/> | <span data-ttu-id="0ce8e-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0ce8e-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0ce8e-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="0ce8e-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0ce8e-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0ce8e-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ce8e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ce8e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ce8e-126">**Iwmpcdromburn-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0ce8e-126">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





