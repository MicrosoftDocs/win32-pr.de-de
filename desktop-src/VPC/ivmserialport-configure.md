---
title: Methode zum Konfigurieren von ivmserialport (vpccominterfaces. h)
description: Konfiguriert den seriellen Anschluss.
ms.assetid: fee2e373-8e7c-4f1d-84d0-f0f187a41e9f
keywords:
- Konfigurieren des virtuellen Computers für die Methode
- Konfigurieren Sie die Methode Virtual PC, ivmserialport Interface.
- Ivmserialport Interface Virtual PC, Methode konfigurieren
topic_type:
- apiref
api_name:
- IVMSerialPort.Configure
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99440263dbf52282b6f3c2756ff7dd76151ff73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040678"
---
# <a name="ivmserialportconfigure-method"></a><span data-ttu-id="3a795-106">Ivmserialport:: Configure-Methode</span><span class="sxs-lookup"><span data-stu-id="3a795-106">IVMSerialPort::Configure method</span></span>

<span data-ttu-id="3a795-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3a795-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3a795-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3a795-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3a795-109">Konfiguriert den seriellen Anschluss.</span><span class="sxs-lookup"><span data-stu-id="3a795-109">Configures the serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a795-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a795-110">Syntax</span></span>


```C++
HRESULT Configure(
  [in] VMSerialPortType portType,
  [in] BSTR             portName,
  [in] VARIANT_BOOL     vmConnectImmediately
);
```



## <a name="parameters"></a><span data-ttu-id="3a795-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a795-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a795-112">*portType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a795-112">*portType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a795-113">Der Typ des seriellen Anschlusses.</span><span class="sxs-lookup"><span data-stu-id="3a795-113">The type of serial port.</span></span> <span data-ttu-id="3a795-114">Eine Liste der Werte finden Sie unter [**vmserialporttype**](vmserialporttype.md).</span><span class="sxs-lookup"><span data-stu-id="3a795-114">For a list of values, see [**VMSerialPortType**](vmserialporttype.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a795-115">*Portname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a795-115">*portName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a795-116">Der Name des seriellen Anschlusses.</span><span class="sxs-lookup"><span data-stu-id="3a795-116">The name of the serial port.</span></span> <span data-ttu-id="3a795-117">Beispiel: "COM1" for **vmserialport \_ hostport**, "C: \\SerialPort.txt" for **vmserialport \_ Textfile** oder " \\ \\ *Servername* \\ Pipe \\ *Pipename*" für **vmserialport \_ NamedPipe**.</span><span class="sxs-lookup"><span data-stu-id="3a795-117">For example, "COM1" for **vmSerialPort\_HostPort**, "C:\\SerialPort.txt" for **vmSerialPort\_TextFile**, or "\\\\*servername*\\pipe\\*pipename*" for **vmSerialPort\_NamedPipe**.</span></span>

</dd> <dt>

<span data-ttu-id="3a795-118">*vmconnectimmediately* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a795-118">*vmConnectImmediately* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a795-119">**True** , wenn der serielle Host-Port sofort geöffnet werden soll, wenn der virtuelle Computer gestartet wird, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="3a795-119">**TRUE** if the host serial port should be opened immediately when the virtual machine is started and **FALSE** otherwise.</span></span> <span data-ttu-id="3a795-120">Wird ignoriert, wenn der *portType* nicht der **vmserialport- \_ hostport** ist.</span><span class="sxs-lookup"><span data-stu-id="3a795-120">Ignored if *portType* is not **vmSerialPort\_HostPort**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a795-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a795-121">Return value</span></span>

<span data-ttu-id="3a795-122">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3a795-122">This method can return one of these values.</span></span>



| <span data-ttu-id="3a795-123">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="3a795-123">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="3a795-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a795-124">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3a795-125"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3a795-125"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="3a795-126">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a795-126">The operation was successful.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="3a795-127"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="3a795-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="3a795-128">Der *portType* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="3a795-128">The *portType* parameter is not valid.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="3a795-129"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3a795-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="3a795-130">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="3a795-130">An unexpected error has occurred.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="3a795-131"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3a795-131"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="3a795-132">Der *Portname* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="3a795-132">The *portName* parameter is **NULL**.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="3a795-133"><dt>**HRESULT \_ Von \_ Win32 (Error \_ outo-Memory)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="3a795-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>      | <span data-ttu-id="3a795-134">Es ist nicht genügend Arbeitsspeicher verfügbar, um diese Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="3a795-134">There is not enough memory available to complete this request.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="3a795-135"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="3a795-135"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="3a795-136">Der vom *Portname* -Parameter angegebene Pfad ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="3a795-136">The path specified by the *portName* parameter is too long.</span></span> <span data-ttu-id="3a795-137">Der Pfad muss kleiner als der **Maximale \_ Pfad** (260) sein.</span><span class="sxs-lookup"><span data-stu-id="3a795-137">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="3a795-138"><dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="3a795-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="3a795-139">Der *Portname* -Parameter enthält ein ungültiges Zeichen (eines der " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="3a795-139">The *portName* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="3a795-140"><dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="3a795-140"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="3a795-141">Der *Portname* -Parameter gibt einen leeren oder relativen Pfad an.</span><span class="sxs-lookup"><span data-stu-id="3a795-141">The *portName* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="3a795-142">Ein absoluter Pfad ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3a795-142">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="3a795-143"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="3a795-143"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="3a795-144">Die Konfiguration für diesen virtuellen Computer ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="3a795-144">The configuration for this virtual machine is not valid.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="3a795-145"><dt>**VM \_ E \_ Pref \_ \_**</dt> unzulässiger Wert <dt>0xa0040301</dt></span><span class="sxs-lookup"><span data-stu-id="3a795-145"><dt>**VM\_E\_PREF\_ILLEGAL\_VALUE**</dt> <dt>0xA0040301</dt></span></span> </dl>                   | <span data-ttu-id="3a795-146">Der angegebene Port wird bereits verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a795-146">The specified port is already in use.</span></span><br/>                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="3a795-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a795-147">Requirements</span></span>



| <span data-ttu-id="3a795-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a795-148">Requirement</span></span> | <span data-ttu-id="3a795-149">Wert</span><span class="sxs-lookup"><span data-stu-id="3a795-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a795-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a795-150">Minimum supported client</span></span><br/> | <span data-ttu-id="3a795-151">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a795-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a795-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a795-152">Minimum supported server</span></span><br/> | <span data-ttu-id="3a795-153">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3a795-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3a795-154">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3a795-154">End of client support</span></span><br/>    | <span data-ttu-id="3a795-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a795-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3a795-156">Produkt</span><span class="sxs-lookup"><span data-stu-id="3a795-156">Product</span></span><br/>                  | <span data-ttu-id="3a795-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3a795-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3a795-158">Header</span><span class="sxs-lookup"><span data-stu-id="3a795-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a795-159"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a795-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3a795-160">IID</span><span class="sxs-lookup"><span data-stu-id="3a795-160">IID</span></span><br/>                      | <span data-ttu-id="3a795-161">IID \_ ivmserialport ist als 2ce4460d-1d3f-4458-bf8b-44084b816815 definiert.</span><span class="sxs-lookup"><span data-stu-id="3a795-161">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="3a795-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a795-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a795-163">**Ivmserialport**</span><span class="sxs-lookup"><span data-stu-id="3a795-163">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

