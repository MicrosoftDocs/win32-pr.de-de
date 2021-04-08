---
title: Ivmserialportcollection-Schnittstelle (vpccominterfaces. h)
description: Definiert die Sammlung von seriellen Anschlüssen innerhalb des virtuellen Computers. Zum Abrufen eines ivmserialportcollection-Objekts verwenden Sie die Eigenschaft "ivmvirtualmachine serialports".
ms.assetid: c0ee9799-f3f7-477e-b33b-52f424752aad
keywords:
- Ivmserialportcollection-Schnittstelle virtueller PC
- Ivmserialportcollection Interface Virtual PC, beschrieben
topic_type:
- apiref
api_name:
- IVMSerialPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d2ec37789423b5f9446d667da69eca346a2286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741737"
---
# <a name="ivmserialportcollection-interface"></a><span data-ttu-id="17c04-106">Ivmserialportcollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="17c04-106">IVMSerialPortCollection interface</span></span>

<span data-ttu-id="17c04-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="17c04-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="17c04-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="17c04-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="17c04-109">Definiert die Sammlung von seriellen Anschlüssen innerhalb des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="17c04-109">Defines the collection of serial ports within the virtual machine.</span></span> <span data-ttu-id="17c04-110">Zum Abrufen eines **ivmserialportcollection** -Objekts verwenden Sie die [**ivmvirtualmachine:: serialports**](ivmvirtualmachine-serialports.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="17c04-110">To obtain an **IVMSerialPortCollection** object, use the [**IVMVirtualMachine::SerialPorts**](ivmvirtualmachine-serialports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="17c04-111">Member</span><span class="sxs-lookup"><span data-stu-id="17c04-111">Members</span></span>

<span data-ttu-id="17c04-112">Die **ivmserialportcollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="17c04-112">The **IVMSerialPortCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="17c04-113">**Ivmserialportcollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="17c04-113">**IVMSerialPortCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="17c04-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17c04-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17c04-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17c04-115">Properties</span></span>

<span data-ttu-id="17c04-116">Die **ivmserialportcollection** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="17c04-116">The **IVMSerialPortCollection** interface has these properties.</span></span>



| <span data-ttu-id="17c04-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="17c04-117">Property</span></span>                                                         | <span data-ttu-id="17c04-118">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="17c04-118">Access type</span></span>          | <span data-ttu-id="17c04-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17c04-119">Description</span></span>                                                                |
|:-----------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="17c04-120">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="17c04-120">**\_NewEnum**</span></span>](ivmserialportcollection--newenum.md)<br/> | <span data-ttu-id="17c04-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="17c04-121">Read-only</span></span><br/> | <span data-ttu-id="17c04-122">Ein Enumerator für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="17c04-122">An enumerator for the collection.</span></span><br/>                               |
| [<span data-ttu-id="17c04-123">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="17c04-123">**Count**</span></span>](ivmserialportcollection-count.md)<br/>        | <span data-ttu-id="17c04-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="17c04-124">Read-only</span></span><br/> | <span data-ttu-id="17c04-125">Die Anzahl der seriellen Anschlüsse in dieser Sammlung.</span><span class="sxs-lookup"><span data-stu-id="17c04-125">The number of serial ports in this collection.</span></span><br/>                  |
| [<span data-ttu-id="17c04-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="17c04-126">**Item**</span></span>](ivmserialportcollection-item.md)<br/>          | <span data-ttu-id="17c04-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="17c04-127">Read-only</span></span><br/> | <span data-ttu-id="17c04-128">Das serielle Port Objekt, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="17c04-128">The serial port object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="17c04-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17c04-129">Requirements</span></span>



| <span data-ttu-id="17c04-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17c04-130">Requirement</span></span> | <span data-ttu-id="17c04-131">Wert</span><span class="sxs-lookup"><span data-stu-id="17c04-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="17c04-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17c04-132">Minimum supported client</span></span><br/> | <span data-ttu-id="17c04-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17c04-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="17c04-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17c04-134">Minimum supported server</span></span><br/> | <span data-ttu-id="17c04-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="17c04-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="17c04-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="17c04-136">End of client support</span></span><br/>    | <span data-ttu-id="17c04-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="17c04-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="17c04-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="17c04-138">Product</span></span><br/>                  | <span data-ttu-id="17c04-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="17c04-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="17c04-140">Header</span><span class="sxs-lookup"><span data-stu-id="17c04-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="17c04-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="17c04-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="17c04-142">IID</span><span class="sxs-lookup"><span data-stu-id="17c04-142">IID</span></span><br/>                      | <span data-ttu-id="17c04-143">IID \_ ivmserialportcollection ist als dd3c6175-1F04-4341-9f85-104074880289 definiert.</span><span class="sxs-lookup"><span data-stu-id="17c04-143">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="17c04-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17c04-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17c04-145">**Ivmserialport**</span><span class="sxs-lookup"><span data-stu-id="17c04-145">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> <dt>

[<span data-ttu-id="17c04-146">**Ivmvirtualmachine:: serialports**</span><span class="sxs-lookup"><span data-stu-id="17c04-146">**IVMVirtualMachine::SerialPorts**</span></span>](ivmvirtualmachine-serialports.md)
</dt> </dl>

 

