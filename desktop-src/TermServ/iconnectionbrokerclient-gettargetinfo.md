---
title: Iconnectionbrokerclient gettargetinfo-Methode (cbclient. h)
description: Fordert Informationen über den Zielcomputer an, an den die Verbindung umgeleitet werden soll.
ms.assetid: 43970B06-8CBD-4204-94AE-090A63918A90
ms.tgt_platform: multiple
keywords:
- Gettargetinfo-Methode Remotedesktopdienste
- Gettargetinfo-Methode Remotedesktopdienste, iconnectionbrokerclient-Schnittstelle
- Iconnectionbrokerclient-Schnittstelle Remotedesktopdienste, gettargetinfo-Methode
topic_type:
- apiref
api_name:
- IConnectionBrokerClient.GetTargetInfo
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 366bebf398c5c776e43d5cdee4b99e28e8c580fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517369"
---
# <a name="iconnectionbrokerclientgettargetinfo-method"></a><span data-ttu-id="6a6f3-106">Iconnectionbrokerclient:: gettargetinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="6a6f3-106">IConnectionBrokerClient::GetTargetInfo method</span></span>

<span data-ttu-id="6a6f3-107">Fordert Informationen über den Zielcomputer an, an den die Verbindung umgeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-107">Requests information about the target computer where the connection should be redirected.</span></span> <span data-ttu-id="6a6f3-108">Diese Methode wird vom Redirector verwendet, um Umleitungs Informationen für die eingehende Verbindungsanforderung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-108">This method is used by the redirector to get redirection information for the incoming connection request.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a6f3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a6f3-109">Syntax</span></span>


```C++
HRESULT GetTargetInfo(
  [in]  CB_CONNECTION_INFO       *pConnectionInfo,
  [in]  DWORD                    Reserved,
  [in]  HANDLE                   hStatusEvent,
  [out] CB_TARGET_INFO           *pTargetInfo,
  [out] DWORD                    *pResult,
  [out] IConnectionBrokerRequest **ppCbReq
);
```



## <a name="parameters"></a><span data-ttu-id="6a6f3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a6f3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a6f3-111">*pconnectioninfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a6f3-111">*pConnectionInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-112">Die Adresse einer [**CB- \_ Verbindungs \_**](cb-connection-info.md) Informationsstruktur, die Informationen über die eingehende Verbindungsanforderung enthält.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-112">The address of a [**CB\_CONNECTION\_INFO**](cb-connection-info.md) structure that contains information about the incoming connection request.</span></span>

</dd> <dt>

<span data-ttu-id="6a6f3-113">*Reserviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a6f3-113">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-114">Dieser Parameter ist für die zukünftige Verwendung reserviert und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-114">This parameter is reserved for future use and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6a6f3-115">*hstatus usevent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a6f3-115">*hStatusEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-116">Das Handle eines Ereignisses, das festgelegt wird, wenn ein Update für den Fortschritt der Anforderung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-116">The handle of an event that will get set whenever there is an update to the progress of the request.</span></span> <span data-ttu-id="6a6f3-117">Sie sind dafür verantwortlich, dieses Ereignis zu erstellen und zu schließen.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-117">You are responsible for creating and closing this event.</span></span>

</dd> <dt>

<span data-ttu-id="6a6f3-118">*ptargetinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6a6f3-118">*pTargetInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-119">Die Adresse einer [**CB- \_ Ziel \_**](cb-target-info.md) Informationsstruktur, die Informationen über den Zielcomputer empfängt, an den die eingehende Verbindung umgeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-119">The address of a [**CB\_TARGET\_INFO**](cb-target-info.md) structure that receives information about the target computer where the incoming connection should be redirected.</span></span> <span data-ttu-id="6a6f3-120">Da es sich hierbei um eine asynchrone Methode handelt, muss dieser Arbeitsspeicher verfügbar bleiben, bis die Anforderung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-120">Because this is an asynchronous method, this memory must remain available until the request is complete.</span></span> <span data-ttu-id="6a6f3-121">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-121">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6a6f3-122">*pResult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6a6f3-122">*pResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-123">Die Adresse einer **DWORD** -Variablen, die einen Ergebniscode empfängt.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-123">The address of a **DWORD** variable that receives a result code.</span></span> <span data-ttu-id="6a6f3-124">Da es sich hierbei um eine asynchrone Methode handelt, muss dieser Arbeitsspeicher verfügbar bleiben, bis die Anforderung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-124">Because this is an asynchronous method, this memory must remain available until the request is complete.</span></span> <span data-ttu-id="6a6f3-125">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-125">For more information, see Remarks.</span></span>

<span data-ttu-id="6a6f3-126">Bei diesem Ergebniscode handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-126">This result code will be one of the following values.</span></span>

<dt>

<span data-ttu-id="6a6f3-127">0</span><span class="sxs-lookup"><span data-stu-id="6a6f3-127">0</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-128">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-128">Success.</span></span>

</dd> <dt>

<span data-ttu-id="6a6f3-129">0x0000400</span><span class="sxs-lookup"><span data-stu-id="6a6f3-129">0x0000400</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-130">Der Zielcomputer konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-130">The destination computer could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="6a6f3-131">0x0000401</span><span class="sxs-lookup"><span data-stu-id="6a6f3-131">0x0000401</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-132">Der Zielcomputer ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-132">The destination computer is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6a6f3-133">0x0000402</span><span class="sxs-lookup"><span data-stu-id="6a6f3-133">0x0000402</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-134">Fehler beim Laden des Ziel Computers.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-134">Error loading destination computer.</span></span>

</dd> <dt>

<span data-ttu-id="6a6f3-135">0x0000403</span><span class="sxs-lookup"><span data-stu-id="6a6f3-135">0x0000403</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-136">Fehler beim Online schalten des Ziel Computers.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-136">Error bringing destination computer online.</span></span>

</dd> <dt>

<span data-ttu-id="6a6f3-137">0x0000404</span><span class="sxs-lookup"><span data-stu-id="6a6f3-137">0x0000404</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-138">Fehler beim Umleiten an den Zielcomputer.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-138">Error redirecting to destination computer.</span></span>

</dd> <dt>

<span data-ttu-id="6a6f3-139">0x0000405</span><span class="sxs-lookup"><span data-stu-id="6a6f3-139">0x0000405</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-140">Fehler beim Reaktivieren des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-140">Error waking virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="6a6f3-141">0x0000406</span><span class="sxs-lookup"><span data-stu-id="6a6f3-141">0x0000406</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-142">Fehler beim Starten des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-142">Error booting virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="6a6f3-143">0x0000407</span><span class="sxs-lookup"><span data-stu-id="6a6f3-143">0x0000407</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-144">Fehler beim Ermitteln der IP-Adresse des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-144">Error finding the IP address of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="6a6f3-145">0x0000408</span><span class="sxs-lookup"><span data-stu-id="6a6f3-145">0x0000408</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-146">Der Sitzungs Broker konnte keine verfügbaren Computer im Pool finden.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-146">The session broker could not find any available computers in the pool.</span></span>

</dd> <dt>

<span data-ttu-id="6a6f3-147">0x0000409</span><span class="sxs-lookup"><span data-stu-id="6a6f3-147">0x0000409</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-148">Der Sitzungs Broker hat die Verbindung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-148">The session broker canceled the connection.</span></span>

</dd> <dt>

<span data-ttu-id="6a6f3-149">0x0000410</span><span class="sxs-lookup"><span data-stu-id="6a6f3-149">0x0000410</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-150">Der Sitzungs Broker konnte die Verbindungseinstellungen nicht überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-150">The session broker could not validate the connection settings.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6a6f3-151">*ppcbreq* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6a6f3-151">*ppCbReq* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a6f3-152">Die Adresse eines [**iconnectionbrokerrequest**](iconnectionbrokerrequest.md) -Schnittstellen Zeigers, den Sie zum Abrufen von Statusaktualisierungen für einen asynchronen Vorgang verwenden.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-152">The address of an [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) interface pointer that you use to obtain status updates for an asynchronous operation.</span></span> <span data-ttu-id="6a6f3-153">Diese Schnittstelle wird in Verbindung mit dem *hstatus usevent* -Parameter verwendet, um darauf zu warten und die Ergebnisse dieses asynchronen Vorgangs zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-153">This interface is used in conjunction with the *hStatusEvent* parameter to wait for and get the results of this asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a6f3-154">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a6f3-154">Return value</span></span>

<span data-ttu-id="6a6f3-155">Gibt " **E \_ Pending** " zurück, wenn die asynchrone Anforderung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-155">Returns **E\_PENDING** if the asynchronous request is created.</span></span> <span data-ttu-id="6a6f3-156">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-156">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a6f3-157">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a6f3-157">Remarks</span></span>

<span data-ttu-id="6a6f3-158">Diese Methode ist asynchron.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-158">This method is asynchronous.</span></span> <span data-ttu-id="6a6f3-159">Der *ptargetinfo* -Parameter und der *pResult* -Parameter müssen gültig bleiben, bis die **CB- \_ Status \_ Anforderung \_** von der [**iconnectionbrokerrequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) -Methode abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="6a6f3-159">The *pTargetInfo* and *pResult* parameters must remain valid until the [**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md) method obtains **CB\_STATUS\_REQUEST\_COMPLETED**.</span></span>

<span data-ttu-id="6a6f3-160">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Verwenden der Remotedesktopverbindung Broker-Client-API](use-the-remote-desktop-connection-broker-client-api.md).</span><span class="sxs-lookup"><span data-stu-id="6a6f3-160">For more information about how to use this method, see [How to use the Remote Desktop Connection Broker client API](use-the-remote-desktop-connection-broker-client-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a6f3-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a6f3-161">Requirements</span></span>



| <span data-ttu-id="6a6f3-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a6f3-162">Requirement</span></span> | <span data-ttu-id="6a6f3-163">Wert</span><span class="sxs-lookup"><span data-stu-id="6a6f3-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a6f3-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a6f3-164">Minimum supported client</span></span><br/> | <span data-ttu-id="6a6f3-165">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6a6f3-165">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="6a6f3-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a6f3-166">Minimum supported server</span></span><br/> | <span data-ttu-id="6a6f3-167">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a6f3-167">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="6a6f3-168">Header</span><span class="sxs-lookup"><span data-stu-id="6a6f3-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a6f3-169"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a6f3-169"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a6f3-170">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6a6f3-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="6a6f3-171"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a6f3-171"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="6a6f3-172">DLL</span><span class="sxs-lookup"><span data-stu-id="6a6f3-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a6f3-173"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a6f3-173"><dt>Cbclient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a6f3-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a6f3-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a6f3-175">**Iconnectionbrokerclient**</span><span class="sxs-lookup"><span data-stu-id="6a6f3-175">**IConnectionBrokerClient**</span></span>](iconnectionbrokerclient.md)
</dt> </dl>

 

 





