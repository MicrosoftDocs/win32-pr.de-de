---
title: Iremotedesktopclientevents-Methode (onremotedesktopsizechanged)
description: Wird aufgerufen, wenn sich die Remote Desktop Größe geändert hat.
ms.assetid: DA641CA7-3214-4DB6-9A7F-75903FE93DB4
ms.tgt_platform: multiple
keywords:
- Onremotedesktopsizechanged-Methode Remotedesktopdienste
- Onremotedesktopsizechanged-Methode Remotedesktopdienste, iremotedesktopclientevents-Schnittstelle
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste, onremotedesktopsizechanged-Methode
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnRemoteDesktopSizeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7431d1a6f41a6f87bb34fe1486c203168f2c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741320"
---
# <a name="iremotedesktopclienteventsonremotedesktopsizechanged-method"></a><span data-ttu-id="68844-106">Iremotedesktopclientevents:: onremotedesktopsizechanged-Methode</span><span class="sxs-lookup"><span data-stu-id="68844-106">IRemoteDesktopClientEvents::OnRemoteDesktopSizeChanged method</span></span>

<span data-ttu-id="68844-107">Wird aufgerufen, wenn sich die Remote Desktop Größe geändert hat.</span><span class="sxs-lookup"><span data-stu-id="68844-107">Called when the remote desktop size has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="68844-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="68844-108">Syntax</span></span>


```C++
void OnRemoteDesktopSizeChanged(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a><span data-ttu-id="68844-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="68844-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68844-110">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68844-110">*width* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="68844-111">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68844-111">*height* \[in\]</span></span>
<span data-ttu-id="68844-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="68844-112"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="68844-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68844-113">Return value</span></span>

<span data-ttu-id="68844-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="68844-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="68844-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68844-115">Requirements</span></span>



| <span data-ttu-id="68844-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68844-116">Requirement</span></span> | <span data-ttu-id="68844-117">Wert</span><span class="sxs-lookup"><span data-stu-id="68844-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68844-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68844-118">Minimum supported client</span></span><br/> | <span data-ttu-id="68844-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="68844-119">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="68844-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68844-120">Minimum supported server</span></span><br/> | <span data-ttu-id="68844-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="68844-121">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="68844-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="68844-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="68844-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68844-123"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="68844-124">DLL</span><span class="sxs-lookup"><span data-stu-id="68844-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68844-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68844-125"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="68844-126">IID</span><span class="sxs-lookup"><span data-stu-id="68844-126">IID</span></span><br/>                      | <span data-ttu-id="68844-127">Diid \_ iremotedesktopclientevents ist als 079863b7-6d47-4105-8bfe-0cdcb360e67d definiert.</span><span class="sxs-lookup"><span data-stu-id="68844-127">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="68844-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68844-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68844-129">**Iremotedesktopclientevents**</span><span class="sxs-lookup"><span data-stu-id="68844-129">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





