---
title: Iremotedesktopclientevents-Methode (nicht getrennt)
description: Wird aufgerufen, wenn das Client Steuerelement von einer Remote Sitzung getrennt wurde.
ms.assetid: EA26B530-0AA8-49D6-8E3C-E53179FC5104
ms.tgt_platform: multiple
keywords:
- Ongetrennte Methode Remotedesktopdienste
- Ongetrennte Methode Remotedesktopdienste, iremotedesktopclientevents-Schnittstelle
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste, ongetrennte-Methode
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd59b03fe9cb23309d53773289291c8a791935a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742384"
---
# <a name="iremotedesktopclienteventsondisconnected-method"></a><span data-ttu-id="7ff00-106">Iremotedesktopclientevents:: ongetrennte-Methode</span><span class="sxs-lookup"><span data-stu-id="7ff00-106">IRemoteDesktopClientEvents::OnDisconnected method</span></span>

<span data-ttu-id="7ff00-107">Wird aufgerufen, wenn das Client Steuerelement von einer Remote Sitzung getrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="7ff00-107">Called when the client control has been disconnected from a remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff00-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ff00-108">Syntax</span></span>


```C++
void OnDisconnected(
  [in] long disconnectReason,
  [in] long ExtendedDisconnectReason,
  [in] BSTR disconnectErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="7ff00-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ff00-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ff00-110">*disconnecverrat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ff00-110">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff00-111">Der Grund für das Trennungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7ff00-111">The reason for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="7ff00-112">*Extendeddisconnecverrat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ff00-112">*ExtendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff00-113">Erweiterte Informationen für das Disconnect-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7ff00-113">Extended information for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="7ff00-114">*disconnecterrormessage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ff00-114">*disconnectErrorMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff00-115">Die Fehlermeldung für das Disconnect-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7ff00-115">The error message for the disconnect event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ff00-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ff00-116">Return value</span></span>

<span data-ttu-id="7ff00-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7ff00-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ff00-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ff00-118">Requirements</span></span>



| <span data-ttu-id="7ff00-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ff00-119">Requirement</span></span> | <span data-ttu-id="7ff00-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7ff00-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff00-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ff00-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7ff00-122">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7ff00-122">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="7ff00-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ff00-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7ff00-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ff00-124">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="7ff00-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7ff00-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="7ff00-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ff00-126"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="7ff00-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7ff00-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ff00-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ff00-128"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="7ff00-129">IID</span><span class="sxs-lookup"><span data-stu-id="7ff00-129">IID</span></span><br/>                      | <span data-ttu-id="7ff00-130">Diid \_ iremotedesktopclientevents ist als 079863b7-6d47-4105-8bfe-0cdcb360e67d definiert.</span><span class="sxs-lookup"><span data-stu-id="7ff00-130">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ff00-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ff00-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff00-132">**Iremotedesktopclientevents**</span><span class="sxs-lookup"><span data-stu-id="7ff00-132">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





