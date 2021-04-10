---
title: Imstscaxevents onmouseinputmodechanged-Methode
description: Wird aufgerufen, wenn sich der Mauseingabe Modus geändert hat.
ms.assetid: d0554c59-967d-4181-98cd-9e88dde32752
ms.tgt_platform: multiple
keywords:
- Onmouseinputmodechanged-Methode Remotedesktopdienste
- Onmouseinputmodechanged-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onmouseinputmodechanged-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnMouseInputModeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dbfef19aa79ba634a13d92b8d11866b8016e893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104319"
---
# <a name="imstscaxeventsonmouseinputmodechanged-method"></a><span data-ttu-id="40481-106">Imstscaxevents:: onmouseinputmodechanged-Methode</span><span class="sxs-lookup"><span data-stu-id="40481-106">IMsTscAxEvents::OnMouseInputModeChanged method</span></span>

<span data-ttu-id="40481-107">Wird aufgerufen, wenn sich der Mauseingabe Modus geändert hat.</span><span class="sxs-lookup"><span data-stu-id="40481-107">Called when the mouse input mode has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="40481-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="40481-108">Syntax</span></span>


```C++
void OnMouseInputModeChanged(
  [in] VARIANT_BOOL fMouseModeRelative
);
```



## <a name="parameters"></a><span data-ttu-id="40481-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="40481-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40481-110">*"f"* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40481-110">*fMouseModeRelative* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40481-111">Gibt an, ob sich die Maus im relativen Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="40481-111">Indicates whether the mouse is in relative mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40481-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40481-112">Return value</span></span>

<span data-ttu-id="40481-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="40481-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="40481-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40481-114">Remarks</span></span>

<span data-ttu-id="40481-115">Implementieren Sie diese Methode in der Ereignis Senke, um die Benachrichtigung zu erhalten, dass sich der Mauseingabe Modus geändert hat.</span><span class="sxs-lookup"><span data-stu-id="40481-115">Implement this method in your event sink to receive notification that the mouse input mode has changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="40481-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40481-116">Requirements</span></span>



| <span data-ttu-id="40481-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40481-117">Requirement</span></span> | <span data-ttu-id="40481-118">Wert</span><span class="sxs-lookup"><span data-stu-id="40481-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40481-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40481-119">Minimum supported client</span></span><br/> | <span data-ttu-id="40481-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40481-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="40481-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40481-121">Minimum supported server</span></span><br/> | <span data-ttu-id="40481-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40481-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="40481-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="40481-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="40481-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40481-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="40481-125">DLL</span><span class="sxs-lookup"><span data-stu-id="40481-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40481-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40481-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="40481-127">IID</span><span class="sxs-lookup"><span data-stu-id="40481-127">IID</span></span><br/>                      | <span data-ttu-id="40481-128">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="40481-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="40481-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40481-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40481-130">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="40481-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





