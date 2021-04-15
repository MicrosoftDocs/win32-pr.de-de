---
title: Ivmvirtualmachine startcommunicationchannel-Methode (vpccominterfaces. h)
description: Richtet einen Kommunikationskanal zwischen dem Host und dem Gast Betriebssystem ein.
ms.assetid: e4b04aa8-8400-4aa4-ad54-71ef57dec82a
keywords:
- Startcommunicationchannel-Methode Virtual PC
- Startcommunicationchannel-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, startcommunicationchannel-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.StartCommunicationChannel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac6ab73b6a955b6810eaea280dc25732e2a6721
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478324"
---
# <a name="ivmvirtualmachinestartcommunicationchannel-method"></a><span data-ttu-id="220c0-106">Ivmvirtualmachine:: startcommunicationchannel-Methode</span><span class="sxs-lookup"><span data-stu-id="220c0-106">IVMVirtualMachine::StartCommunicationChannel method</span></span>

<span data-ttu-id="220c0-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="220c0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="220c0-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="220c0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="220c0-109">Richtet einen Kommunikationskanal zwischen dem Host und dem Gast Betriebssystem ein.</span><span class="sxs-lookup"><span data-stu-id="220c0-109">Sets up a communication channel between host and guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="220c0-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="220c0-110">Syntax</span></span>


```C++
HRESULT StartCommunicationChannel(
  [in] VMEndpointType inHostEndpointType,
  [in] BSTR           inHostEndPointName,
  [in] VMEndpointType inGuestEndpointType,
  [in] BSTR           inGuestEndpointName
);
```



## <a name="parameters"></a><span data-ttu-id="220c0-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="220c0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="220c0-112">*inhostendpointtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="220c0-112">*inHostEndpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220c0-113">Dieser Parameter muss **vmendpoint \_ NamedPipe** (0) sein.</span><span class="sxs-lookup"><span data-stu-id="220c0-113">This parameter must be **vmEndpoint\_NamedPipe** (0).</span></span>

</dd> <dt>

<span data-ttu-id="220c0-114">*inhostendpointname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="220c0-114">*inHostEndPointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220c0-115">Der eindeutige Pipename.</span><span class="sxs-lookup"><span data-stu-id="220c0-115">The unique pipe name.</span></span> <span data-ttu-id="220c0-116">Diese Zeichenfolge muss folgende Form aufweisen: " \\ \\ . \\ Pipe \\ *Pipename*".</span><span class="sxs-lookup"><span data-stu-id="220c0-116">This string must have the following form: "\\\\.\\pipe\\*pipename*".</span></span> <span data-ttu-id="220c0-117">Der *pitzame* -Teil des Namens kann ein beliebiges Zeichen enthalten, das kein umgekehrter Schrägstrich ist, einschließlich Ziffern und Sonderzeichen.</span><span class="sxs-lookup"><span data-stu-id="220c0-117">The *pipename* part of the name can include any character other than a backslash, including numbers and special characters.</span></span> <span data-ttu-id="220c0-118">Die Zeichenfolge für den gesamten Pipenamen kann bis zu 256 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="220c0-118">The entire pipe name string can be up to 256 characters long.</span></span> <span data-ttu-id="220c0-119">Bei Pipenamen wird die Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="220c0-119">Pipe names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="220c0-120">*inguestendpointtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="220c0-120">*inGuestEndpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220c0-121">Dieser Parameter muss **vmendpoint \_ tcpip** (1) sein.</span><span class="sxs-lookup"><span data-stu-id="220c0-121">This parameter must be **vmEndpoint\_TCPIP** (1).</span></span>

</dd> <dt>

<span data-ttu-id="220c0-122">*inguestendpointname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="220c0-122">*inGuestEndpointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220c0-123">Die Portnummer, die der TCP-Server im Gast abhört.</span><span class="sxs-lookup"><span data-stu-id="220c0-123">The port number on which the TCP server in the guest is listening.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="220c0-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="220c0-124">Return value</span></span>

<span data-ttu-id="220c0-125">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="220c0-125">This method can return one of these values.</span></span>



| <span data-ttu-id="220c0-126">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="220c0-126">Return code/value</span></span>                                                                                                                                                                                  | <span data-ttu-id="220c0-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="220c0-127">Description</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="220c0-128"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="220c0-128"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                        | <span data-ttu-id="220c0-129">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="220c0-129">The operation was successful.</span></span><br/>                                                                                                                    |
| <dl> <span data-ttu-id="220c0-130"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="220c0-130"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                       | <span data-ttu-id="220c0-131">Der *inhostendpointtype* -Parameter ist nicht **vmendpoint \_ NamedPipe** (0), oder der *inguestendpointtype* -Parameter ist nicht **vmendpoint \_ tcpip** (1).</span><span class="sxs-lookup"><span data-stu-id="220c0-131">The *inHostEndpointType* parameter is not **vmEndpoint\_NamedPipe** (0) or the *inGuestEndpointType* parameter is not **vmEndpoint\_TCPIP** (1).</span></span><br/> |
| <dl> <span data-ttu-id="220c0-132"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="220c0-132"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                          | <span data-ttu-id="220c0-133">Der *inhostendpointname* -Parameter oder der *inguestendpointname* -Parameter ist **null** oder kein gültiger Wert.</span><span class="sxs-lookup"><span data-stu-id="220c0-133">The *inHostEndPointName* or *inGuestEndpointName* parameter is **NULL** or not a valid value.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="220c0-134"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="220c0-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                                  | <span data-ttu-id="220c0-135">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="220c0-135">An unexpected error has occurred.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="220c0-136"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ ungültiges \_ handle)**</dt> <dt>0x80070006</dt></span><span class="sxs-lookup"><span data-stu-id="220c0-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_HANDLE)**</dt> <dt>0x80070006</dt></span></span> </dl>        | <span data-ttu-id="220c0-137">Ein Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="220c0-137">A handle is not valid.</span></span><br/>                                                                                                                           |
| <dl> <span data-ttu-id="220c0-138"><dt>**HRESULT \_ Von \_ Win32 (Error \_ outo-Memory)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="220c0-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>            | <span data-ttu-id="220c0-139">Es ist nicht genügend Arbeitsspeicher verfügbar, um diese Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="220c0-139">There is not enough memory available to complete this request.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="220c0-140"><dt>**HRESULT \_ Aus \_ Win32 (Fehler \_ nicht \_ bereit)**</dt> <dt>0x80070015</dt></span><span class="sxs-lookup"><span data-stu-id="220c0-140"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_READY)**</dt> <dt>0x80070015</dt></span></span> </dl>             | <span data-ttu-id="220c0-141">Das zugrunde liegende System, das für die Bereitstellung von Netzwerkdiensten verwendet wird, wird zurzeit initialisiert.</span><span class="sxs-lookup"><span data-stu-id="220c0-141">The underlying system it uses to provide network services is currently being initialized.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="220c0-142"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ bereits \_ vorhanden)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="220c0-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>        | <span data-ttu-id="220c0-143">Der Pipename wird bereits verwendet.</span><span class="sxs-lookup"><span data-stu-id="220c0-143">The pipe name is already in use.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="220c0-144"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Pipe \_ ausgelastet)**</dt> <dt>0x800700e7</dt></span><span class="sxs-lookup"><span data-stu-id="220c0-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PIPE\_BUSY)**</dt> <dt>0x800700e7</dt></span></span> </dl>             | <span data-ttu-id="220c0-145">Ein oder mehrere Kanäle werden herunterlaufen und werden möglicherweise in Kürze verfügbar.</span><span class="sxs-lookup"><span data-stu-id="220c0-145">One or more channels are running down and may become available shortly.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="220c0-146"><dt>**HRESULT \_ Von \_ Win32 (Fehler bei \_ maximalen \_ Sitzungen \_ erreicht)**</dt> <dt>0x80070161</dt></span><span class="sxs-lookup"><span data-stu-id="220c0-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_MAX\_SESSIONS\_REACHED)**</dt> <dt>0x80070161</dt></span></span> </dl> | <span data-ttu-id="220c0-147">Die maximale Anzahl verfügbarer Kommunikationskanäle ist in Gebrauch.</span><span class="sxs-lookup"><span data-stu-id="220c0-147">The maximum numbers of communication channels available are in-use.</span></span> <span data-ttu-id="220c0-148">Ein anderer Kanal kann zu diesem Zeitpunkt nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="220c0-148">Another channel cannot be started at this time.</span></span><br/>                              |
| <dl> <span data-ttu-id="220c0-149"><dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Revisions Konflikt \_ )**</dt> <dt>0x8007051a</dt></span><span class="sxs-lookup"><span data-stu-id="220c0-149"><dt>**HRESULT\_FROM\_WIN32(ERROR\_REVISION\_MISMATCH)**</dt> <dt>0x8007051a</dt></span></span> </dl>     | <span data-ttu-id="220c0-150">Die Version des Host-und Gast Subsystems stimmt nicht überein.</span><span class="sxs-lookup"><span data-stu-id="220c0-150">There is a mismatch between the version of the host and guest subsystems.</span></span> <span data-ttu-id="220c0-151">Weitere Details finden Sie im Windows-Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="220c0-151">See the Windows Event Log for more detail.</span></span><br/>                             |
| <dl> <span data-ttu-id="220c0-152"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="220c0-152"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                             | <span data-ttu-id="220c0-153">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="220c0-153">The VM is not running.</span></span><br/>                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="220c0-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="220c0-154">Remarks</span></span>

<span data-ttu-id="220c0-155">Die aktuelle Implementierung unterstützt nur Named Pipe-Schnittstelle auf dem Host und die TCP/IP-Schnittstelle auf dem Gast Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="220c0-155">The current implementation supports only named pipe interface on the host and TCP/IP interface on the guest operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="220c0-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="220c0-156">Requirements</span></span>



| <span data-ttu-id="220c0-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="220c0-157">Requirement</span></span> | <span data-ttu-id="220c0-158">Wert</span><span class="sxs-lookup"><span data-stu-id="220c0-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="220c0-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="220c0-159">Minimum supported client</span></span><br/> | <span data-ttu-id="220c0-160">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="220c0-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="220c0-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="220c0-161">Minimum supported server</span></span><br/> | <span data-ttu-id="220c0-162">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="220c0-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="220c0-163">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="220c0-163">End of client support</span></span><br/>    | <span data-ttu-id="220c0-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="220c0-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="220c0-165">Produkt</span><span class="sxs-lookup"><span data-stu-id="220c0-165">Product</span></span><br/>                  | <span data-ttu-id="220c0-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="220c0-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="220c0-167">Header</span><span class="sxs-lookup"><span data-stu-id="220c0-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="220c0-168"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="220c0-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="220c0-169">IID</span><span class="sxs-lookup"><span data-stu-id="220c0-169">IID</span></span><br/>                      | <span data-ttu-id="220c0-170">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="220c0-170">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="220c0-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="220c0-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="220c0-172">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="220c0-172">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="220c0-173">**Vmendpointtype**</span><span class="sxs-lookup"><span data-stu-id="220c0-173">**VMEndpointType**</span></span>](vmendpointtype.md)
</dt> </dl>

 

