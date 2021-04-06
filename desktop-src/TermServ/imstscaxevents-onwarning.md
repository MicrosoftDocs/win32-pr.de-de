---
title: Imstscaxevents OnWarning-Methode
description: Wird aufgerufen, wenn das Client Steuerelement einen Fehlerzustand erkennt, der nicht schwerwiegend ist.
ms.assetid: af43d3aa-0ae8-4721-b85d-bb043b20dc40
ms.tgt_platform: multiple
keywords:
- OnWarning-Methode Remotedesktopdienste
- OnWarning-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, OnWarning-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnWarning
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadc7013f34c93406f93841896a9041bbb1b7cfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742081"
---
# <a name="imstscaxeventsonwarning-method"></a><span data-ttu-id="74007-106">Imstscaxevents:: OnWarning-Methode</span><span class="sxs-lookup"><span data-stu-id="74007-106">IMsTscAxEvents::OnWarning method</span></span>

<span data-ttu-id="74007-107">Wird aufgerufen, wenn das Client Steuerelement einen Fehlerzustand erkennt, der nicht schwerwiegend ist.</span><span class="sxs-lookup"><span data-stu-id="74007-107">Called when the client control encounters an error condition that is not fatal.</span></span>

## <a name="syntax"></a><span data-ttu-id="74007-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="74007-108">Syntax</span></span>


```C++
void OnWarning(
  [in] long warningCode
);
```



## <a name="parameters"></a><span data-ttu-id="74007-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="74007-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74007-110">*warningCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74007-110">*warningCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74007-111">Der Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="74007-111">The error code.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="74007-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="74007-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="74007-113">Der Bitmap-Cache ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="74007-113">Bitmap cache is corrupt.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74007-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74007-114">Return value</span></span>

<span data-ttu-id="74007-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="74007-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74007-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74007-116">Remarks</span></span>

<span data-ttu-id="74007-117">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="74007-117">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74007-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74007-118">Requirements</span></span>



| <span data-ttu-id="74007-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74007-119">Requirement</span></span> | <span data-ttu-id="74007-120">Wert</span><span class="sxs-lookup"><span data-stu-id="74007-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74007-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74007-121">Minimum supported client</span></span><br/> | <span data-ttu-id="74007-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74007-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="74007-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74007-123">Minimum supported server</span></span><br/> | <span data-ttu-id="74007-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74007-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="74007-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="74007-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="74007-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74007-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="74007-127">DLL</span><span class="sxs-lookup"><span data-stu-id="74007-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74007-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74007-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="74007-129">IID</span><span class="sxs-lookup"><span data-stu-id="74007-129">IID</span></span><br/>                      | <span data-ttu-id="74007-130">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="74007-130">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="74007-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74007-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74007-132">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="74007-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





