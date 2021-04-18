---
title: Ivmfloppydriveevents onmediainsert-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass Medien in das Laufwerk eingefügt wurden. | Ivmfloppydriveevents onmediainsert-Methode (vpccominterfaces. h)
ms.assetid: 922fca14-8ef6-4d3d-b1b6-72d2ea83e8ef
keywords:
- Onmediainsert-Methode Virtual PC
- Onmediainsert-Methode Virtual PC, ivmfloppydriveevents-Schnittstelle
- Ivmfloppydriveevents Interface Virtual PC, onmediainsert-Methode
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d607a2f63836ca1cb151e602b2d3b2021f4e3913
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106351911"
---
# <a name="ivmfloppydriveeventsonmediainsert-method"></a><span data-ttu-id="ed208-107">Ivmfloppydriveevents:: onmediainsert-Methode</span><span class="sxs-lookup"><span data-stu-id="ed208-107">IVMFloppyDriveEvents::OnMediaInsert method</span></span>

<span data-ttu-id="ed208-108">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ed208-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ed208-109">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ed208-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ed208-110">Empfängt eine Benachrichtigung, dass Medien in das Laufwerk eingefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="ed208-110">Receives notification that media has been inserted into the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed208-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed208-111">Syntax</span></span>


```C++
HRESULT OnMediaInsert(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="ed208-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed208-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed208-113">*mediapath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed208-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed208-114">Der Buchstabe des Host Laufwerks bzw. der Pfad des Disketten Bilds.</span><span class="sxs-lookup"><span data-stu-id="ed208-114">The host drive letter, or path, to floppy image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed208-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed208-115">Return value</span></span>

<span data-ttu-id="ed208-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ed208-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ed208-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ed208-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed208-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed208-118">Remarks</span></span>

<span data-ttu-id="ed208-119">Diese Methode wird aufgerufen, wenn Medien (ein Disketten Image oder eine Diskette in einem Host Laufwerk) eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ed208-119">This method is called when media (a floppy disk image or a floppy disk in a host drive) is inserted.</span></span> <span data-ttu-id="ed208-120">Das Client Programm muss diese Schnittstellen Methode implementieren, um Benachrichtigungen über das vmfloppydriveevent \_ onmediainsert-Ereignis zu erhalten, das von [**ivmfloppydrive**](ivmfloppydrive.md)stammt.</span><span class="sxs-lookup"><span data-stu-id="ed208-120">The client program must implement this interface method to receive notification of the vmFloppyDriveEvent\_OnMediaInsert event originating from [**IVMFloppyDrive**](ivmfloppydrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed208-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed208-121">Requirements</span></span>



| <span data-ttu-id="ed208-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed208-122">Requirement</span></span> | <span data-ttu-id="ed208-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ed208-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed208-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed208-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ed208-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed208-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ed208-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed208-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ed208-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ed208-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ed208-128">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ed208-128">End of client support</span></span><br/>    | <span data-ttu-id="ed208-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ed208-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ed208-130">Produkt</span><span class="sxs-lookup"><span data-stu-id="ed208-130">Product</span></span><br/>                  | <span data-ttu-id="ed208-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ed208-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ed208-132">Header</span><span class="sxs-lookup"><span data-stu-id="ed208-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed208-133"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed208-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ed208-134">IID</span><span class="sxs-lookup"><span data-stu-id="ed208-134">IID</span></span><br/>                      | <span data-ttu-id="ed208-135">Diid \_ ivmfloppydriveevents ist als a9ed3401-4e09-4177-86ec-a13bf9fa7d4e definiert.</span><span class="sxs-lookup"><span data-stu-id="ed208-135">DIID\_IVMFloppyDriveEvents is defined as a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="ed208-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed208-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed208-137">**Ivmfloppydriveevents**</span><span class="sxs-lookup"><span data-stu-id="ed208-137">**IVMFloppyDriveEvents**</span></span>](ivmfloppydriveevents.md)
</dt> </dl>

 

