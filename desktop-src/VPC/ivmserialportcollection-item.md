---
title: Ivmserialportcollection-Element Eigenschaft (vpccominterfaces. h)
description: Ruft das serielle Port Objekt ab, das dem angegebenen Index entspricht.
ms.assetid: 24ce1404-d7aa-4125-b1f9-9c54418ea205
keywords:
- Element Eigenschaft virtueller PC
- Item-Eigenschaft Virtual PC, ivmserialportcollection-Schnittstelle
- Ivmserialportcollection-Schnittstelle Virtual PC, Item-Eigenschaft
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Item
- IVMSerialPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be44cc92507954848c369273ae27de49df8d0ad8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341804"
---
# <a name="ivmserialportcollectionitem-property"></a><span data-ttu-id="a5bb4-106">Ivmserialportcollection:: Item (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a5bb4-106">IVMSerialPortCollection::Item property</span></span>

<span data-ttu-id="a5bb4-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a5bb4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a5bb4-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a5bb4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a5bb4-109">Ruft das serielle Port Objekt ab, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="a5bb4-109">Retrieves the serial port object that corresponds to the specified index.</span></span>

<span data-ttu-id="a5bb4-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a5bb4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5bb4-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5bb4-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long          index,
  [out, retval] IVMSerialPort **serialPort
);
```



## <a name="property-value"></a><span data-ttu-id="a5bb4-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a5bb4-112">Property value</span></span>

<span data-ttu-id="a5bb4-113">Das [**ivmserialport**](ivmserialport.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a5bb4-113">The [**IVMSerialPort**](ivmserialport.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a5bb4-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a5bb4-114">Error codes</span></span>



| <span data-ttu-id="a5bb4-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="a5bb4-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a5bb4-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a5bb4-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a5bb4-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a5bb4-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a5bb4-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5bb4-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="a5bb4-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a5bb4-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a5bb4-120">Der *SerialPort* -Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="a5bb4-120">The *serialPort* parameter is NULL.</span></span> <br/>                                                |
| <dl> <span data-ttu-id="a5bb4-121"><dt>DISP \_ E \_ badindex</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="a5bb4-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="a5bb4-122">Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung.</span><span class="sxs-lookup"><span data-stu-id="a5bb4-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="a5bb4-123"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="a5bb4-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="a5bb4-124">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="a5bb4-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="a5bb4-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a5bb4-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a5bb4-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a5bb4-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="a5bb4-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5bb4-127">Requirements</span></span>



| <span data-ttu-id="a5bb4-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5bb4-128">Requirement</span></span> | <span data-ttu-id="a5bb4-129">Wert</span><span class="sxs-lookup"><span data-stu-id="a5bb4-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5bb4-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5bb4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a5bb4-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5bb4-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a5bb4-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5bb4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a5bb4-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a5bb4-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a5bb4-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a5bb4-134">End of client support</span></span><br/>    | <span data-ttu-id="a5bb4-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a5bb4-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a5bb4-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="a5bb4-136">Product</span></span><br/>                  | <span data-ttu-id="a5bb4-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a5bb4-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a5bb4-138">Header</span><span class="sxs-lookup"><span data-stu-id="a5bb4-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5bb4-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5bb4-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a5bb4-140">IID</span><span class="sxs-lookup"><span data-stu-id="a5bb4-140">IID</span></span><br/>                      | <span data-ttu-id="a5bb4-141">IID \_ ivmserialportcollection ist als dd3c6175-1F04-4341-9f85-104074880289 definiert.</span><span class="sxs-lookup"><span data-stu-id="a5bb4-141">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="a5bb4-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5bb4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5bb4-143">**Ivmserialport**</span><span class="sxs-lookup"><span data-stu-id="a5bb4-143">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> <dt>

[<span data-ttu-id="a5bb4-144">**Ivmserialportcollection**</span><span class="sxs-lookup"><span data-stu-id="a5bb4-144">**IVMSerialPortCollection**</span></span>](ivmserialportcollection.md)
</dt> </dl>

 

