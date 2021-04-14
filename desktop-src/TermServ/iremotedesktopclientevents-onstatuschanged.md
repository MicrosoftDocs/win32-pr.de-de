---
title: Iremotedesktopclientevents-Methode (locationapi. h)
description: Wird aufgerufen, wenn das Client Steuerelement seinen Status aktualisiert hat.
ms.assetid: AAFBDC9E-C8B5-4924-AA69-82EF09996AF7
ms.tgt_platform: multiple
keywords:
- Onstatuschangi-Methode Remotedesktopdienste
- Onstatuschangimethode Remotedesktopdienste, iremotedesktopclientevents-Schnittstelle
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste, onstatuschangi-Methode
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b17e42e75072033f952c7ef790365d6a363a5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478879"
---
# <a name="iremotedesktopclienteventsonstatuschanged-method"></a><span data-ttu-id="16b17-106">Iremotedesktopclientevents:: onstatuschangi-Methode</span><span class="sxs-lookup"><span data-stu-id="16b17-106">IRemoteDesktopClientEvents::OnStatusChanged method</span></span>

<span data-ttu-id="16b17-107">Wird aufgerufen, wenn das Client Steuerelement seinen Status aktualisiert hat.</span><span class="sxs-lookup"><span data-stu-id="16b17-107">Called when the client control has updated its status.</span></span>

## <a name="syntax"></a><span data-ttu-id="16b17-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="16b17-108">Syntax</span></span>


```C++
void OnStatusChanged(
   long statusCode,
   BSTR statusMessage
);
```



## <a name="parameters"></a><span data-ttu-id="16b17-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="16b17-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16b17-110">*statusCode*</span><span class="sxs-lookup"><span data-stu-id="16b17-110">*statusCode*</span></span> 
</dt> <dd>

<span data-ttu-id="16b17-111">Der neue Statuscode.</span><span class="sxs-lookup"><span data-stu-id="16b17-111">The new status code.</span></span>

</dd> <dt>

<span data-ttu-id="16b17-112">*statusMessage*</span><span class="sxs-lookup"><span data-stu-id="16b17-112">*statusMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="16b17-113">Der Text der Statusmeldung.</span><span class="sxs-lookup"><span data-stu-id="16b17-113">The status message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16b17-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16b17-114">Return value</span></span>

<span data-ttu-id="16b17-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="16b17-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="16b17-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16b17-116">Requirements</span></span>



| <span data-ttu-id="16b17-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16b17-117">Requirement</span></span> | <span data-ttu-id="16b17-118">Wert</span><span class="sxs-lookup"><span data-stu-id="16b17-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16b17-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16b17-119">Minimum supported client</span></span><br/> | <span data-ttu-id="16b17-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="16b17-120">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="16b17-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16b17-121">Minimum supported server</span></span><br/> | <span data-ttu-id="16b17-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16b17-122">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="16b17-123">Header</span><span class="sxs-lookup"><span data-stu-id="16b17-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="16b17-124"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="16b17-124"><dt>Locationapi.h</dt></span></span> </dl>       |
| <span data-ttu-id="16b17-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="16b17-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="16b17-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16b17-126"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="16b17-127">DLL</span><span class="sxs-lookup"><span data-stu-id="16b17-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16b17-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16b17-128"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="16b17-129">IID</span><span class="sxs-lookup"><span data-stu-id="16b17-129">IID</span></span><br/>                      | <span data-ttu-id="16b17-130">Diid \_ iremotedesktopclientevents ist als 079863b7-6d47-4105-8bfe-0cdcb360e67d definiert.</span><span class="sxs-lookup"><span data-stu-id="16b17-130">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="16b17-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16b17-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16b17-132">**Iremotedesktopclientevents**</span><span class="sxs-lookup"><span data-stu-id="16b17-132">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





