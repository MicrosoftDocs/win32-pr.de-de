---
title: Vmserialporttype-Enumeration (vpccominterfaces. h)
description: Gibt den Typ des seriellen Anschlusses an.
ms.assetid: 1385292b-ee3c-41f0-805a-df126f33cabb
keywords:
- Vmserialporttype-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMSerialPortType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9b6171053e980f1f5dbdc52ef28deed177edba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518371"
---
# <a name="vmserialporttype-enumeration"></a><span data-ttu-id="cf5aa-104">Vmserialporttype-Enumeration</span><span class="sxs-lookup"><span data-stu-id="cf5aa-104">VMSerialPortType enumeration</span></span>

<span data-ttu-id="cf5aa-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cf5aa-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cf5aa-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cf5aa-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cf5aa-107">Gibt den Typ des seriellen Anschlusses an.</span><span class="sxs-lookup"><span data-stu-id="cf5aa-107">Specifies the type of serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf5aa-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf5aa-108">Syntax</span></span>


```C++
typedef enum  { 
  vmSerialPort_HostPort   = 0,
  vmSerialPort_TextFile   = 1,
  vmSerialPort_NamedPipe  = 2,
  vmSerialPort_Null       = 3
} VMSerialPortType;
```



## <a name="constants"></a><span data-ttu-id="cf5aa-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="cf5aa-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cf5aa-110"><span id="vmSerialPort_HostPort"></span><span id="vmserialport_hostport"></span><span id="VMSERIALPORT_HOSTPORT"></span>**vmserialport- \_ hostport**</span><span class="sxs-lookup"><span data-stu-id="cf5aa-110"><span id="vmSerialPort_HostPort"></span><span id="vmserialport_hostport"></span><span id="VMSERIALPORT_HOSTPORT"></span>**vmSerialPort\_HostPort**</span></span>
</dt> <dd>

<span data-ttu-id="cf5aa-111">Einen seriellen Port für den Host.</span><span class="sxs-lookup"><span data-stu-id="cf5aa-111">A host serial port.</span></span>

</dd> <dt>

<span data-ttu-id="cf5aa-112"><span id="vmSerialPort_TextFile"></span><span id="vmserialport_textfile"></span><span id="VMSERIALPORT_TEXTFILE"></span>**vmserialport- \_ Textdatei**</span><span class="sxs-lookup"><span data-stu-id="cf5aa-112"><span id="vmSerialPort_TextFile"></span><span id="vmserialport_textfile"></span><span id="VMSERIALPORT_TEXTFILE"></span>**vmSerialPort\_TextFile**</span></span>
</dt> <dd>

<span data-ttu-id="cf5aa-113">Eine Host Textdatei.</span><span class="sxs-lookup"><span data-stu-id="cf5aa-113">A host text file.</span></span>

</dd> <dt>

<span data-ttu-id="cf5aa-114"><span id="vmSerialPort_NamedPipe"></span><span id="vmserialport_namedpipe"></span><span id="VMSERIALPORT_NAMEDPIPE"></span>**vmserialport- \_ NamedPipe**</span><span class="sxs-lookup"><span data-stu-id="cf5aa-114"><span id="vmSerialPort_NamedPipe"></span><span id="vmserialport_namedpipe"></span><span id="VMSERIALPORT_NAMEDPIPE"></span>**vmSerialPort\_NamedPipe**</span></span>
</dt> <dd>

<span data-ttu-id="cf5aa-115">Eine Named Pipe.</span><span class="sxs-lookup"><span data-stu-id="cf5aa-115">A named pipe.</span></span>

</dd> <dt>

<span data-ttu-id="cf5aa-116"><span id="vmSerialPort_Null"></span><span id="vmserialport_null"></span><span id="VMSERIALPORT_NULL"></span>**vmserialport \_ null**</span><span class="sxs-lookup"><span data-stu-id="cf5aa-116"><span id="vmSerialPort_Null"></span><span id="vmserialport_null"></span><span id="VMSERIALPORT_NULL"></span>**vmSerialPort\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="cf5aa-117">Ein serieller **null** -Anschluss (verwirft alle an ihn gesendeten Bits).</span><span class="sxs-lookup"><span data-stu-id="cf5aa-117">A **NULL** serial port (discards all bits sent to it).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf5aa-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf5aa-118">Requirements</span></span>



| <span data-ttu-id="cf5aa-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf5aa-119">Requirement</span></span> | <span data-ttu-id="cf5aa-120">Wert</span><span class="sxs-lookup"><span data-stu-id="cf5aa-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf5aa-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf5aa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cf5aa-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf5aa-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cf5aa-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf5aa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cf5aa-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cf5aa-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cf5aa-125">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="cf5aa-125">End of client support</span></span><br/>    | <span data-ttu-id="cf5aa-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cf5aa-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cf5aa-127">Produkt</span><span class="sxs-lookup"><span data-stu-id="cf5aa-127">Product</span></span><br/>                  | <span data-ttu-id="cf5aa-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cf5aa-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cf5aa-129">Header</span><span class="sxs-lookup"><span data-stu-id="cf5aa-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf5aa-130"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf5aa-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf5aa-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf5aa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf5aa-132">**Ivmserialport**</span><span class="sxs-lookup"><span data-stu-id="cf5aa-132">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

