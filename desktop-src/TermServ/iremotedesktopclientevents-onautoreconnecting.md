---
title: Iremotedesktopclientevents onautoreconnecting-Methode
description: Wird aufgerufen, wenn das Client Steuerelement versucht, eine Verbindung mit einer Remote Sitzung automatisch wiederherzustellen.
ms.assetid: 299408A9-ED14-42F4-B324-AF4C86FEDABE
ms.tgt_platform: multiple
keywords:
- Onautoreconnecting-Methode Remotedesktopdienste
- Onautoreconnecting-Methode Remotedesktopdienste, iremotedesktopclientevents-Schnittstelle
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste, onautoreconnecting-Methode
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74c37919384727fdf51aad004349478798a3ffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519007"
---
# <a name="iremotedesktopclienteventsonautoreconnecting-method"></a><span data-ttu-id="9b577-106">Iremotedesktopclientevents:: onautoreconnecting-Methode</span><span class="sxs-lookup"><span data-stu-id="9b577-106">IRemoteDesktopClientEvents::OnAutoReconnecting method</span></span>

<span data-ttu-id="9b577-107">Wird aufgerufen, wenn das Client Steuerelement versucht, eine Verbindung mit einer Remote Sitzung automatisch wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="9b577-107">Called when the client control attempts to automatically reestablish a connection to a remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b577-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b577-108">Syntax</span></span>


```C++
void OnAutoReconnecting(
  [in] long         disconnectReason,
  [in] long         ExtendedDisconnectReason,
  [in] BSTR         disconnectErrorMessage,
  [in] VARIANT_BOOL networkAvailable,
  [in] long         attemptCount,
  [in] long         maxAttemptCount
);
```



## <a name="parameters"></a><span data-ttu-id="9b577-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b577-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b577-110">*disconnecverrat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b577-110">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b577-111">Der Grund für das Trennungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9b577-111">The reason for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="9b577-112">*Extendeddisconnecverrat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b577-112">*ExtendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b577-113">Erweiterte Informationen für das Disconnect-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9b577-113">Extended information for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="9b577-114">*disconnecterrormessage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b577-114">*disconnectErrorMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b577-115">Die Fehlermeldung für das Disconnect-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9b577-115">The error message for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="9b577-116">*NetworkAvailable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b577-116">*networkAvailable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b577-117">Gibt an, ob das Netzwerk verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9b577-117">Whether the network is available.</span></span>

</dd> <dt>

<span data-ttu-id="9b577-118">*Anzahl* \[ der Versuche in\]</span><span class="sxs-lookup"><span data-stu-id="9b577-118">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b577-119">Der Versuch, dies zu tun.</span><span class="sxs-lookup"><span data-stu-id="9b577-119">Which attempt this is.</span></span>

</dd> <dt>

<span data-ttu-id="9b577-120">*maxder-Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b577-120">*maxAttemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b577-121">Die maximale Anzahl von Wiederholungs versuchen für die Verbindung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b577-121">The maximum number of reconnect attempts will be performed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b577-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b577-122">Return value</span></span>

<span data-ttu-id="9b577-123">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9b577-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b577-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b577-124">Requirements</span></span>



| <span data-ttu-id="9b577-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b577-125">Requirement</span></span> | <span data-ttu-id="9b577-126">Wert</span><span class="sxs-lookup"><span data-stu-id="9b577-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b577-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b577-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9b577-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9b577-128">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="9b577-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b577-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9b577-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9b577-130">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="9b577-131">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9b577-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="9b577-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b577-132"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="9b577-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9b577-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b577-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b577-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="9b577-135">IID</span><span class="sxs-lookup"><span data-stu-id="9b577-135">IID</span></span><br/>                      | <span data-ttu-id="9b577-136">Diid \_ iremotedesktopclientevents ist als 079863b7-6d47-4105-8bfe-0cdcb360e67d definiert.</span><span class="sxs-lookup"><span data-stu-id="9b577-136">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9b577-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b577-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b577-138">**Iremotedesktopclientevents**</span><span class="sxs-lookup"><span data-stu-id="9b577-138">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





