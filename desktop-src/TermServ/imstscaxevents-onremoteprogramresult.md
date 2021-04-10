---
title: Imstscaxevents onremoteprogramresult-Methode
description: Wird aufgerufen, wenn ein RemoteApp-Programm ein Ergebnis an das Client Steuerelement zurückgibt.
ms.assetid: 5bc9570f-14fb-4b6f-a7dd-c1bce3ef19e0
ms.tgt_platform: multiple
keywords:
- Onremoteprogramresult-Methode Remotedesktopdienste
- Onremoteprogramresult-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onremoteprogramresult-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramResult
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880e4fb3f6453114415f5bcc07a0afb9c176a1bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104313"
---
# <a name="imstscaxeventsonremoteprogramresult-method"></a><span data-ttu-id="ad20c-106">Imstscaxevents:: onremoteprogramresult-Methode</span><span class="sxs-lookup"><span data-stu-id="ad20c-106">IMsTscAxEvents::OnRemoteProgramResult method</span></span>

<span data-ttu-id="ad20c-107">Wird aufgerufen, wenn ein RemoteApp-Programm ein Ergebnis an das Client Steuerelement zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ad20c-107">Called when a RemoteApp program returns a result to the client control.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad20c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad20c-108">Syntax</span></span>


```C++
VOID OnRemoteProgramResult(
  [in] BSTR                bstrRemoteProgram,
  [in] RemoteProgramResult lError,
  [in] VARIANT_BOOL        vbIsExecutable
);
```



## <a name="parameters"></a><span data-ttu-id="ad20c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad20c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad20c-110">*bstrauremoteprogram* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad20c-110">*bstrRemoteProgram* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad20c-111">Der Name des RemoteApp-Programms.</span><span class="sxs-lookup"><span data-stu-id="ad20c-111">The name of the RemoteApp program.</span></span>

</dd> <dt>

<span data-ttu-id="ad20c-112">*lerror* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad20c-112">*lError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad20c-113">Das Ergebnis des Versuchs, das RemoteApp-Programm zu starten.</span><span class="sxs-lookup"><span data-stu-id="ad20c-113">The result of the attempt to launch the RemoteApp program.</span></span>

<dt>

<span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>

<span data-ttu-id="ad20c-114"><span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**remoteappresultok** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="ad20c-114"><span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**remoteAppResultOk** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="ad20c-115">Das RemoteApp-Programm wurde erfolgreich gestartet.</span><span class="sxs-lookup"><span data-stu-id="ad20c-115">The RemoteApp program launched successfully.</span></span>

</dd> <dt>

<span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>

<span data-ttu-id="ad20c-116"><span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**remoteappresultlocked** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="ad20c-116"><span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**remoteAppResultLocked** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="ad20c-117">Die Remote Sitzung ist gesperrt, und das RemoteApp-Programm kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="ad20c-117">The remote session is locked and the RemoteApp program cannot be launched.</span></span> <span data-ttu-id="ad20c-118">Der Benutzer muss seine Anmelde Informationen eingeben, um die Sitzung zu entsperren, und dann das RemoteApp-Programm starten.</span><span class="sxs-lookup"><span data-stu-id="ad20c-118">The user must enter their credentials to unlock the session, and then launch the RemoteApp program.</span></span>

</dd> <dt>

<span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>

<span data-ttu-id="ad20c-119"><span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**remoteappresultprotocolerror** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="ad20c-119"><span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**remoteAppResultProtocolError** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="ad20c-120">Das RemoteApp-Programm hat einen Protokollfehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ad20c-120">The RemoteApp program returned a protocol error.</span></span>

</dd> <dt>

<span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>

<span data-ttu-id="ad20c-121"><span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**remoteappresultnotinwhitelist** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="ad20c-121"><span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**remoteAppResultNotInWhitelist** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="ad20c-122">Das RemoteApp-Programm ist nicht in der genehmigten Liste der RD-Sitzungshost Server enthalten.</span><span class="sxs-lookup"><span data-stu-id="ad20c-122">The RemoteApp program is not in the approved list of the RD Session Host server.</span></span>

</dd> <dt>

<span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>

<span data-ttu-id="ad20c-123"><span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**remoteappresultnetworkpathdenied** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="ad20c-123"><span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**remoteAppResultNetworkPathDenied** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="ad20c-124">Der Netzwerkpfad zum RemoteApp-Programm wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="ad20c-124">The network path to the RemoteApp program was denied.</span></span>

</dd> <dt>

<span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>

<span data-ttu-id="ad20c-125"><span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**remoteappresultfilename-found** (5 (0x5))</span><span class="sxs-lookup"><span data-stu-id="ad20c-125"><span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**remoteAppResultFileNotFound** (5 (0x5))</span></span>


</dt> <dd>

<span data-ttu-id="ad20c-126">Die RemoteApp-Programmdatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="ad20c-126">The RemoteApp program file was not found.</span></span>

</dd> <dt>

<span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>

<span data-ttu-id="ad20c-127"><span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**remoteappresultfailure** (6 (0x6))</span><span class="sxs-lookup"><span data-stu-id="ad20c-127"><span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**remoteAppResultFailure** (6 (0x6))</span></span>


</dt> <dd>

<span data-ttu-id="ad20c-128">Das RemoteApp-Programm konnte nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="ad20c-128">The RemoteApp program failed to launch.</span></span>

</dd> <dt>

<span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>

<span data-ttu-id="ad20c-129"><span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**remoteappresulthooklotloaded** (7 (0x7))</span><span class="sxs-lookup"><span data-stu-id="ad20c-129"><span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**remoteAppResultHookNotLoaded** (7 (0x7))</span></span>


</dt> <dd>

<span data-ttu-id="ad20c-130">Das RemoteApp-Programm kann nicht gestartet werden, da die Sitzung aktuell den sicheren Desktop anzeigt.</span><span class="sxs-lookup"><span data-stu-id="ad20c-130">The RemoteApp program cannot be launched because the session is currently displaying the secure desktop.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ad20c-131">*vbisexecutable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad20c-131">*vbIsExecutable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad20c-132">Gibt an, ob das RemoteApp-Programm direkt mit dem Namen der ausführbaren Datei oder indirekt mithilfe einer Datei Zuordnung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="ad20c-132">Indicates whether the RemoteApp program was launched directly, by using the executable name or indirectly, by using a file association.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad20c-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad20c-133">Return value</span></span>

<span data-ttu-id="ad20c-134">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ad20c-134">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad20c-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad20c-135">Remarks</span></span>

<span data-ttu-id="ad20c-136">Implementieren Sie diese Methode in der Ereignis Senke, um Benachrichtigungen zu erhalten, dass ein RemoteApp-Programm ein Ergebnis zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="ad20c-136">Implement this method in your event sink to receive notification that a RemoteApp program returned a result.</span></span>

<span data-ttu-id="ad20c-137">Diese Methode wird unmittelbar nach dem Versuch des ActiveX-Steuer Elements aufgerufen, das RemoteApp-Programm zu starten, und der *lerror* -Parameter gibt das Ergebnis des Versuchs an.</span><span class="sxs-lookup"><span data-stu-id="ad20c-137">This method is called immediately after the ActiveX control attempts to launch the RemoteApp program, and the *lError* parameter indicates the result of the attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad20c-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad20c-138">Requirements</span></span>



| <span data-ttu-id="ad20c-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad20c-139">Requirement</span></span> | <span data-ttu-id="ad20c-140">Wert</span><span class="sxs-lookup"><span data-stu-id="ad20c-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad20c-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad20c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ad20c-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad20c-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ad20c-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad20c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ad20c-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad20c-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ad20c-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ad20c-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="ad20c-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad20c-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ad20c-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ad20c-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad20c-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad20c-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ad20c-149">IID</span><span class="sxs-lookup"><span data-stu-id="ad20c-149">IID</span></span><br/>                      | <span data-ttu-id="ad20c-150">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="ad20c-150">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="ad20c-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad20c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad20c-152">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="ad20c-152">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





