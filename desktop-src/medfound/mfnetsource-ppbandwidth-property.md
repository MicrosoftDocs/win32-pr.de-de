---
description: Gibt die von der Netzwerkquelle erkannte Paket paar Bandbreite und Lauf Zeit Bandbreite an.
ms.assetid: 430de7fc-fe62-4b89-b3fc-7cd956e40892
title: MFNETSOURCE_PPBANDWIDTH-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f23f289f68e46bba726a4391023ce9001e2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347053"
---
# <a name="mfnetsource_ppbandwidth-property"></a><span data-ttu-id="25b3e-103">Eigenschaft "MF NetSource \_ ppbandwidth"</span><span class="sxs-lookup"><span data-stu-id="25b3e-103">MFNETSOURCE\_PPBANDWIDTH property</span></span>

<span data-ttu-id="25b3e-104">Gibt die von der Netzwerkquelle erkannte Paket paar Bandbreite und Lauf Zeit Bandbreite an.</span><span class="sxs-lookup"><span data-stu-id="25b3e-104">Specifies the packet-pair bandwidth and run-time bandwidth detected by the network source.</span></span> <span data-ttu-id="25b3e-105">Der Eigenschafts Wert ist ein Array mit zwei Werten:</span><span class="sxs-lookup"><span data-stu-id="25b3e-105">The property value is a array of two values:</span></span>

-   <span data-ttu-id="25b3e-106">Paket paar Bandbreite in Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="25b3e-106">Packet-pair bandwidth, in bits per second.</span></span>
-   <span data-ttu-id="25b3e-107">Lauf Zeit Bandbreite in Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="25b3e-107">Run-time bandwidth, in bits per second.</span></span>



<span data-ttu-id="25b3e-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="25b3e-108">Data type</span></span>

<span data-ttu-id="25b3e-109">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="25b3e-109">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="25b3e-110">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="25b3e-110">PROPVARIANT member</span></span>

<span data-ttu-id="25b3e-111">Array von **ulong** -Werten (**CAUL**)</span><span class="sxs-lookup"><span data-stu-id="25b3e-111">Array of **ULONG** values (**CAUL**)</span></span>

<span data-ttu-id="25b3e-112">VT \_ Vector \| VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="25b3e-112">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="25b3e-113">**CAUL**</span><span class="sxs-lookup"><span data-stu-id="25b3e-113">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="25b3e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25b3e-114">Remarks</span></span>

<span data-ttu-id="25b3e-115">Die Konstante " **MF NetSource \_ ppbandwidth** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="25b3e-115">The constant **MFNETSOURCE\_PPBANDWIDTH** defines the GUID for this property key.</span></span> <span data-ttu-id="25b3e-116">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="25b3e-116">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="25b3e-117">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="25b3e-117">This property is read-only.</span></span> <span data-ttu-id="25b3e-118">Um diese Eigenschaft abzurufen, Fragen Sie die Netzwerkquelle nach der **IPropertyStore** -Schnittstelle ab, und rufen Sie **IPropertyStore:: GetValue** auf.</span><span class="sxs-lookup"><span data-stu-id="25b3e-118">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="25b3e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25b3e-119">Requirements</span></span>



| <span data-ttu-id="25b3e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25b3e-120">Requirement</span></span> | <span data-ttu-id="25b3e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="25b3e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="25b3e-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25b3e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="25b3e-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25b3e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="25b3e-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25b3e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="25b3e-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25b3e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="25b3e-126">Header</span><span class="sxs-lookup"><span data-stu-id="25b3e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="25b3e-127"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="25b3e-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25b3e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25b3e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25b3e-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="25b3e-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="25b3e-130">Netzwerk Quell Features</span><span class="sxs-lookup"><span data-stu-id="25b3e-130">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="25b3e-131">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="25b3e-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




