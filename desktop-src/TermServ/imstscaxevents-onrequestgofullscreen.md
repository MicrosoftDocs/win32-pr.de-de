---
title: Imstscaxevents onrequestgofullscreen-Methode
description: Wird aufgerufen, wenn der Client anfordert, in den Vollbildmodus zu wechseln, und die imstscadvancedsettings put \_ containerhandledfullscreen-Methode aufgerufen wird, um die containerhandledfullscreen-Eigenschaft auf einen Wert ungleich 0 (null) festzulegen.
ms.assetid: f61520dc-a72a-4205-8761-92aaf08b5f90
ms.tgt_platform: multiple
keywords:
- Onrequestgofullscreen-Methode Remotedesktopdienste
- Onrequestgofullscreen-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onrequestgofullscreen-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestGoFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c865cd27b447743f781b8563956e7fb2d7f5d703
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392021"
---
# <a name="imstscaxeventsonrequestgofullscreen-method"></a><span data-ttu-id="fc9b8-106">Imstscaxevents:: onrequestgofullscreen-Methode</span><span class="sxs-lookup"><span data-stu-id="fc9b8-106">IMsTscAxEvents::OnRequestGoFullScreen method</span></span>

<span data-ttu-id="fc9b8-107">Wird aufgerufen, wenn der Client anfordert, in den Vollbildmodus zu wechseln, und die [**imstscadvancedsettings::p UT \_ containerhandledfullscreen**](imstscadvancedsettings-containerhandledfullscreen.md) -Methode aufgerufen wird, um die **containerhandledfullscreen** -Eigenschaft auf einen Wert ungleich 0 (null) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="fc9b8-107">Called when the client requests to switch to full-screen mode and the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) method is called to set the **ContainerHandledFullScreen** property to a nonzero value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc9b8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc9b8-108">Syntax</span></span>


```C++
void OnRequestGoFullScreen();
```



## <a name="parameters"></a><span data-ttu-id="fc9b8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc9b8-109">Parameters</span></span>

<span data-ttu-id="fc9b8-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="fc9b8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc9b8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc9b8-111">Return value</span></span>

<span data-ttu-id="fc9b8-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fc9b8-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc9b8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc9b8-113">Remarks</span></span>

<span data-ttu-id="fc9b8-114">Im Container behandelten Vollbildmodus sollte der Container als Reaktion auf dieses Ereignis den Standardmodus für den Vollbildmodus eingeben.</span><span class="sxs-lookup"><span data-stu-id="fc9b8-114">In container-handled full-screen mode, the container should enter standard full-screen mode in response to this event.</span></span>

<span data-ttu-id="fc9b8-115">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fc9b8-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc9b8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc9b8-116">Requirements</span></span>



| <span data-ttu-id="fc9b8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc9b8-117">Requirement</span></span> | <span data-ttu-id="fc9b8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="fc9b8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc9b8-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc9b8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fc9b8-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc9b8-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fc9b8-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc9b8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fc9b8-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc9b8-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fc9b8-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="fc9b8-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="fc9b8-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc9b8-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fc9b8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fc9b8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc9b8-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc9b8-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fc9b8-127">IID</span><span class="sxs-lookup"><span data-stu-id="fc9b8-127">IID</span></span><br/>                      | <span data-ttu-id="fc9b8-128">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="fc9b8-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="fc9b8-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc9b8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc9b8-130">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="fc9b8-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





