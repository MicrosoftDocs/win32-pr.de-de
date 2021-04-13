---
title: Ivmserialport-Schnittstelle (vpccominterfaces. h)
description: Definiert einen seriellen Anschluss innerhalb eines virtuellen Computers.
ms.assetid: a6568885-bfdf-4559-8886-02ca59096ca0
keywords:
- Ivmserialport Interface Virtual PC
- Ivmserialport Interface Virtual PC, beschrieben
topic_type:
- apiref
api_name:
- IVMSerialPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6edc758ffecca9a0d4788e5586c902cf0b21dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518395"
---
# <a name="ivmserialport-interface"></a><span data-ttu-id="2efa5-105">Ivmserialport-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2efa5-105">IVMSerialPort interface</span></span>

<span data-ttu-id="2efa5-106">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2efa5-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2efa5-107">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2efa5-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2efa5-108">Definiert einen seriellen Anschluss innerhalb eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="2efa5-108">Defines a serial port inside a virtual machine.</span></span> <span data-ttu-id="2efa5-109">Diese Schnittstelle ermöglicht Ihnen das Konfigurieren von seriellen Anschlüssen innerhalb eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="2efa5-109">This interface allows you to configure serial ports inside a virtual machine.</span></span> <span data-ttu-id="2efa5-110">Sie können ein **ivmserialport** -Objekt aus dem [**ivmserialportcollection**](ivmserialportcollection.md) -Objekt abrufen, das von der [**ivmvirtualmachine:: serialports**](ivmvirtualmachine-serialports.md) -Eigenschaft zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2efa5-110">You can retrieve an **IVMSerialPort** object from the [**IVMSerialPortCollection**](ivmserialportcollection.md) object returned from the [**IVMVirtualMachine::SerialPorts**](ivmvirtualmachine-serialports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="2efa5-111">Member</span><span class="sxs-lookup"><span data-stu-id="2efa5-111">Members</span></span>

<span data-ttu-id="2efa5-112">Die **ivmserialport** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2efa5-112">The **IVMSerialPort** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="2efa5-113">**Ivmserialport** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2efa5-113">**IVMSerialPort** also has these types of members:</span></span>

-   [<span data-ttu-id="2efa5-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="2efa5-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="2efa5-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2efa5-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2efa5-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="2efa5-116">Methods</span></span>

<span data-ttu-id="2efa5-117">Die **ivmserialport** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2efa5-117">The **IVMSerialPort** interface has these methods.</span></span>



| <span data-ttu-id="2efa5-118">Methode</span><span class="sxs-lookup"><span data-stu-id="2efa5-118">Method</span></span>                                       | <span data-ttu-id="2efa5-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2efa5-119">Description</span></span>                                                      |
|:---------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="2efa5-120">**\_id**</span><span class="sxs-lookup"><span data-stu-id="2efa5-120">**\_ID**</span></span>](ivmserialport--id.md)            | <span data-ttu-id="2efa5-121">Ruft den internen Bezeichner des seriellen Anschlusses ab.</span><span class="sxs-lookup"><span data-stu-id="2efa5-121">Retrieves the internal identifier of the serial port.</span></span><br/> |
| [<span data-ttu-id="2efa5-122">**Konfigurieren**</span><span class="sxs-lookup"><span data-stu-id="2efa5-122">**Configure**</span></span>](ivmserialport-configure.md) | <span data-ttu-id="2efa5-123">Konfiguriert den seriellen Anschluss.</span><span class="sxs-lookup"><span data-stu-id="2efa5-123">Configures the serial port.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="2efa5-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2efa5-124">Properties</span></span>

<span data-ttu-id="2efa5-125">Die **ivmserialport** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2efa5-125">The **IVMSerialPort** interface has these properties.</span></span>



| <span data-ttu-id="2efa5-126">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2efa5-126">Property</span></span>                                                                  | <span data-ttu-id="2efa5-127">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="2efa5-127">Access type</span></span>          | <span data-ttu-id="2efa5-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2efa5-128">Description</span></span>                                                                                                       |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2efa5-129">**Connectimmediately**</span><span class="sxs-lookup"><span data-stu-id="2efa5-129">**ConnectImmediately**</span></span>](ivmserialport-connectimmediately.md)<br/> | <span data-ttu-id="2efa5-130">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2efa5-130">Read-only</span></span><br/> | <span data-ttu-id="2efa5-131">Gibt an, ob der serielle Anschluss geöffnet werden soll, ohne darauf zu warten, dass ein Modem Befehl empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="2efa5-131">Indicates whether the serial port should be opened without waiting for a modem command to be received.</span></span><br/> |
| [<span data-ttu-id="2efa5-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="2efa5-132">**Name**</span></span>](ivmserialport-name.md)<br/>                             | <span data-ttu-id="2efa5-133">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2efa5-133">Read-only</span></span><br/> | <span data-ttu-id="2efa5-134">Der Name des seriellen Anschlusses.</span><span class="sxs-lookup"><span data-stu-id="2efa5-134">The name of the serial port.</span></span><br/>                                                                           |
| [<span data-ttu-id="2efa5-135">**type**</span><span class="sxs-lookup"><span data-stu-id="2efa5-135">**Type**</span></span>](ivmserialport-type.md)<br/>                             | <span data-ttu-id="2efa5-136">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2efa5-136">Read-only</span></span><br/> | <span data-ttu-id="2efa5-137">Der Typ des seriellen Anschlusses.</span><span class="sxs-lookup"><span data-stu-id="2efa5-137">The type of the serial port.</span></span><br/>                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="2efa5-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2efa5-138">Requirements</span></span>



| <span data-ttu-id="2efa5-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2efa5-139">Requirement</span></span> | <span data-ttu-id="2efa5-140">Wert</span><span class="sxs-lookup"><span data-stu-id="2efa5-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2efa5-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2efa5-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2efa5-142">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2efa5-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2efa5-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2efa5-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2efa5-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2efa5-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2efa5-145">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="2efa5-145">End of client support</span></span><br/>    | <span data-ttu-id="2efa5-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2efa5-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2efa5-147">Produkt</span><span class="sxs-lookup"><span data-stu-id="2efa5-147">Product</span></span><br/>                  | <span data-ttu-id="2efa5-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2efa5-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2efa5-149">Header</span><span class="sxs-lookup"><span data-stu-id="2efa5-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="2efa5-150"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2efa5-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2efa5-151">IID</span><span class="sxs-lookup"><span data-stu-id="2efa5-151">IID</span></span><br/>                      | <span data-ttu-id="2efa5-152">IID \_ ivmserialport ist als 2ce4460d-1d3f-4458-bf8b-44084b816815 definiert.</span><span class="sxs-lookup"><span data-stu-id="2efa5-152">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



 

