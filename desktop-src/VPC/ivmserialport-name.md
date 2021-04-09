---
title: Ivmserialport-Namenseigenschaft (vpccominterfaces. h)
description: Der Name des seriellen Anschlusses.
ms.assetid: 4d3fe008-f089-4a1b-9c90-2e0b3ded58fa
keywords:
- Name-Eigenschaft virtueller PC
- Name-Eigenschaft Virtual PC, ivmserialport-Schnittstelle
- Ivmserialport Interface Virtual PC, Name-Eigenschaft
topic_type:
- apiref
api_name:
- IVMSerialPort.Name
- IVMSerialPort.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 540540e2af91647b9c77735a1c601ed62aecdbdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859181"
---
# <a name="ivmserialportname-property"></a><span data-ttu-id="d57e3-106">Ivmserialport:: Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d57e3-106">IVMSerialPort::Name property</span></span>

<span data-ttu-id="d57e3-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d57e3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d57e3-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d57e3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d57e3-109">Ruft den Namen des seriellen Anschlusses ab.</span><span class="sxs-lookup"><span data-stu-id="d57e3-109">Retrieves the name of the serial port.</span></span>

<span data-ttu-id="d57e3-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d57e3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d57e3-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d57e3-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a><span data-ttu-id="d57e3-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d57e3-112">Property value</span></span>

<span data-ttu-id="d57e3-113">Der Name des seriellen Anschlusses.</span><span class="sxs-lookup"><span data-stu-id="d57e3-113">The name of the serial port.</span></span> <span data-ttu-id="d57e3-114">Beispiel: "COM1" for **vmserialport \_ hostport**, "C: \\SerialPort.txt" for **vmserialport \_ Textfile** oder " \\ \\ *Servername* \\ Pipe \\ *Pipename*" für **vmserialport \_ NamedPipe**.</span><span class="sxs-lookup"><span data-stu-id="d57e3-114">For example, "COM1" for **vmSerialPort\_HostPort**, "C:\\SerialPort.txt" for **vmSerialPort\_TextFile**, or "\\\\*servername*\\pipe\\*pipename*" for **vmSerialPort\_NamedPipe**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d57e3-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d57e3-115">Error codes</span></span>



| <span data-ttu-id="d57e3-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="d57e3-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d57e3-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d57e3-117">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="d57e3-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d57e3-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d57e3-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d57e3-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="d57e3-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d57e3-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d57e3-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="d57e3-121">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="d57e3-122"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="d57e3-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="d57e3-123">Die Konfiguration für diesen virtuellen Computer ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d57e3-123">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="d57e3-124"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d57e3-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d57e3-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d57e3-125">An unexpected error has occurred.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="d57e3-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d57e3-126">Requirements</span></span>



| <span data-ttu-id="d57e3-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d57e3-127">Requirement</span></span> | <span data-ttu-id="d57e3-128">Wert</span><span class="sxs-lookup"><span data-stu-id="d57e3-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d57e3-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d57e3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d57e3-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d57e3-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d57e3-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d57e3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d57e3-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d57e3-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d57e3-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d57e3-133">End of client support</span></span><br/>    | <span data-ttu-id="d57e3-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d57e3-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d57e3-135">Produkt</span><span class="sxs-lookup"><span data-stu-id="d57e3-135">Product</span></span><br/>                  | <span data-ttu-id="d57e3-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d57e3-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d57e3-137">Header</span><span class="sxs-lookup"><span data-stu-id="d57e3-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d57e3-138"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d57e3-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d57e3-139">IID</span><span class="sxs-lookup"><span data-stu-id="d57e3-139">IID</span></span><br/>                      | <span data-ttu-id="d57e3-140">IID \_ ivmserialport ist als 2ce4460d-1d3f-4458-bf8b-44084b816815 definiert.</span><span class="sxs-lookup"><span data-stu-id="d57e3-140">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="d57e3-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d57e3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57e3-142">**Ivmserialport**</span><span class="sxs-lookup"><span data-stu-id="d57e3-142">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

