---
title: Ivmserialport-Typeigenschaft (vpccominterfaces. h)
description: Ruft den Typ des seriellen Anschlusses ab.
ms.assetid: 0ec9c9d7-9387-458e-befe-42d58c38df35
keywords:
- Type-Eigenschaft Virtual PC
- Type-Eigenschaft Virtual PC, ivmserialport-Schnittstelle
- Ivmserialport Interface Virtual PC, Type-Eigenschaft
topic_type:
- apiref
api_name:
- IVMSerialPort.Type
- IVMSerialPort.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ab32ba6e205911fca85474c047e24b7ad7f1f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477061"
---
# <a name="ivmserialporttype-property"></a><span data-ttu-id="130c1-106">Ivmserialport:: Type-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="130c1-106">IVMSerialPort::Type property</span></span>

<span data-ttu-id="130c1-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="130c1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="130c1-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="130c1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="130c1-109">Ruft den Typ des seriellen Anschlusses ab.</span><span class="sxs-lookup"><span data-stu-id="130c1-109">Retrieves the type of the serial port.</span></span>

<span data-ttu-id="130c1-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="130c1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="130c1-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="130c1-111">Syntax</span></span>


```C++
HRESULT get_Type(
  [out, retval] VMSerialPortType *portType
);
```



## <a name="property-value"></a><span data-ttu-id="130c1-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="130c1-112">Property value</span></span>

<span data-ttu-id="130c1-113">Der Typ des seriellen Anschlusses.</span><span class="sxs-lookup"><span data-stu-id="130c1-113">The type of serial port.</span></span> <span data-ttu-id="130c1-114">Eine Liste der Werte finden Sie unter [**vmserialporttype**](vmserialporttype.md).</span><span class="sxs-lookup"><span data-stu-id="130c1-114">For a list of values, see [**VMSerialPortType**](vmserialporttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="130c1-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="130c1-115">Error codes</span></span>



| <span data-ttu-id="130c1-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="130c1-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="130c1-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="130c1-117">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="130c1-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="130c1-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="130c1-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="130c1-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="130c1-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="130c1-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="130c1-121">Der-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="130c1-121">The parameter is NULL.</span></span><br/>                                   |
| <dl> <span data-ttu-id="130c1-122"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="130c1-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="130c1-123">Die Konfiguration für diesen virtuellen Computer ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="130c1-123">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="130c1-124"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="130c1-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="130c1-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="130c1-125">An unexpected error has occurred.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="130c1-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="130c1-126">Requirements</span></span>



| <span data-ttu-id="130c1-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="130c1-127">Requirement</span></span> | <span data-ttu-id="130c1-128">Wert</span><span class="sxs-lookup"><span data-stu-id="130c1-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="130c1-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="130c1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="130c1-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="130c1-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="130c1-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="130c1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="130c1-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="130c1-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="130c1-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="130c1-133">End of client support</span></span><br/>    | <span data-ttu-id="130c1-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="130c1-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="130c1-135">Produkt</span><span class="sxs-lookup"><span data-stu-id="130c1-135">Product</span></span><br/>                  | <span data-ttu-id="130c1-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="130c1-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="130c1-137">Header</span><span class="sxs-lookup"><span data-stu-id="130c1-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="130c1-138"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="130c1-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="130c1-139">IID</span><span class="sxs-lookup"><span data-stu-id="130c1-139">IID</span></span><br/>                      | <span data-ttu-id="130c1-140">IID \_ ivmserialport ist als 2ce4460d-1d3f-4458-bf8b-44084b816815 definiert.</span><span class="sxs-lookup"><span data-stu-id="130c1-140">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="130c1-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="130c1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="130c1-142">**Ivmserialport**</span><span class="sxs-lookup"><span data-stu-id="130c1-142">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

