---
title: Ivmharddiskconnection-Eigenschaft undoharddisk (vpccominterfaces. h)
description: Ruft ein Festplatten Objekt ab, das dem Rückgängig-Datenträger Image dieser Verbindung entspricht.
ms.assetid: 0daec200-0bda-44cf-b97d-b9a179cb63f8
keywords:
- Undoharddisk-Eigenschaft virtueller PC
- Undoharddisk-Eigenschaft Virtual PC, ivmharddiskconnection-Schnittstelle
- Ivmharddiskconnection-Schnittstelle Virtual PC, undoharddisk (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.UndoHardDisk
- IVMHardDiskConnection.get_UndoHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0fcbd6535c0cf91e1b42549047c131c1804215c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102819"
---
# <a name="ivmharddiskconnectionundoharddisk-property"></a><span data-ttu-id="9227d-106">Ivmharddiskconnection:: undoharddisk (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9227d-106">IVMHardDiskConnection::UndoHardDisk property</span></span>

<span data-ttu-id="9227d-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9227d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9227d-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9227d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9227d-109">Ruft ein Festplatten Objekt ab, das dem Rückgängig-Datenträger Image dieser Verbindung entspricht.</span><span class="sxs-lookup"><span data-stu-id="9227d-109">Retrieves a hard disk object corresponding to this connection's undo disk image.</span></span>

<span data-ttu-id="9227d-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9227d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9227d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="9227d-111">Syntax</span></span>


```C++
HRESULT get_UndoHardDisk(
  [out, retval] IVMHardDisk **undoHardDisk
);
```



## <a name="property-value"></a><span data-ttu-id="9227d-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9227d-112">Property value</span></span>

<span data-ttu-id="9227d-113">Ein [**ivmharddisk**](ivmharddisk.md) -Objekt, das die mit dieser Verbindung verknüpfte rückgängig-Festplatte beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9227d-113">An [**IVMHardDisk**](ivmharddisk.md) object that describes the undo hard disk associated with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9227d-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="9227d-114">Error codes</span></span>



| <span data-ttu-id="9227d-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="9227d-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="9227d-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9227d-116">Meaning</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9227d-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9227d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="9227d-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="9227d-118">The operation was successful.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="9227d-119"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9227d-119"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="9227d-120">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="9227d-120">An unexpected error has occurred.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="9227d-121"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9227d-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="9227d-122">Der-Parameter ist **null** oder ungültig.</span><span class="sxs-lookup"><span data-stu-id="9227d-122">The parameter is **NULL** or not valid.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="9227d-123"><dt>HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="9227d-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="9227d-124">Der Rückgängig-Datenträger für diese Verbindung wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="9227d-124">The undo disk for this connection was not found.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="9227d-125"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="9227d-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="9227d-126">Die aktuelle Konfiguration der virtuellen Maschine ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9227d-126">The current virtual machine configuration is not valid.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="9227d-127"><dt>VM \_ E \_ Laufwerk \_ ungültige</dt> <dt>0xa0040502</dt></span><span class="sxs-lookup"><span data-stu-id="9227d-127"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="9227d-128">Der Busstandort für diese Verbindung wurde nicht ordnungsgemäß initialisiert, oder das Gerät an diesem Speicherort ist keine gültige Festplatte.</span><span class="sxs-lookup"><span data-stu-id="9227d-128">The bus location for this connection has not been properly initialized, or the device at this location is not a valid hard disk.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9227d-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9227d-129">Requirements</span></span>



| <span data-ttu-id="9227d-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9227d-130">Requirement</span></span> | <span data-ttu-id="9227d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="9227d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9227d-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9227d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9227d-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9227d-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9227d-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9227d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9227d-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9227d-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9227d-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9227d-136">End of client support</span></span><br/>    | <span data-ttu-id="9227d-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9227d-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9227d-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="9227d-138">Product</span></span><br/>                  | <span data-ttu-id="9227d-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9227d-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9227d-140">Header</span><span class="sxs-lookup"><span data-stu-id="9227d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9227d-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9227d-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9227d-142">IID</span><span class="sxs-lookup"><span data-stu-id="9227d-142">IID</span></span><br/>                      | <span data-ttu-id="9227d-143">IID \_ ivmharddiskconnection ist als aefa36a5-463a-46AE-9e6c-a1fb4e12e671 definiert.</span><span class="sxs-lookup"><span data-stu-id="9227d-143">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="9227d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9227d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9227d-145">**Ivmharddiskconnection**</span><span class="sxs-lookup"><span data-stu-id="9227d-145">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

