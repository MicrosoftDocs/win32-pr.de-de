---
description: Der Bereich gültiger UDP-Ports, die von der Netzwerkquelle zum Empfangen von Streaminginhalten verwendet werden können.
ms.assetid: 97fe2d11-70f7-4baa-b49f-513d90146591
title: MFNETSOURCE_UDP_PORT_RANGE-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04db8c450bd20adc8c03ec3b964b543f1500aa51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359880"
---
# <a name="mfnetsource_udp_port_range-property"></a><span data-ttu-id="9118e-103">MF-Quell- \_ UDP- \_ Port Bereich ( \_ Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9118e-103">MFNETSOURCE\_UDP\_PORT\_RANGE property</span></span>

<span data-ttu-id="9118e-104">Der Bereich gültiger UDP-Ports, die von der Netzwerkquelle zum Empfangen von Streaminginhalten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9118e-104">The range of valid UDP ports that the network source can use to receive streaming content.</span></span> <span data-ttu-id="9118e-105">Der Wert dieser Eigenschaft ist eine Zeichenfolge mit der Form " *m*–*n* ", wobei " *m* " und " *n* " Portnummern sind.</span><span class="sxs-lookup"><span data-stu-id="9118e-105">The value of this property is a string with the form " *m*–*n* " where *m* and *n* are port numbers.</span></span>



<span data-ttu-id="9118e-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9118e-106">Data type</span></span>

<span data-ttu-id="9118e-107">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="9118e-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="9118e-108">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="9118e-108">PROPVARIANT member</span></span>

<span data-ttu-id="9118e-109">Breit Zeichen-Zeichenfolge (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="9118e-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="9118e-110">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="9118e-110">VT\_LPWSTR</span></span>

<span data-ttu-id="9118e-111">**pwszval**</span><span class="sxs-lookup"><span data-stu-id="9118e-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="9118e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9118e-112">Remarks</span></span>

<span data-ttu-id="9118e-113">Der Konstante **msnetsource- \_ UDP- \_ Port \_ Bereich** definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="9118e-113">The constant **MFNETSOURCE\_UDP\_PORT\_RANGE** defines the GUID for this property key.</span></span> <span data-ttu-id="9118e-114">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9118e-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="9118e-115">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="9118e-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="9118e-116">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="9118e-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="9118e-117">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="9118e-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9118e-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9118e-118">Requirements</span></span>



| <span data-ttu-id="9118e-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9118e-119">Requirement</span></span> | <span data-ttu-id="9118e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9118e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9118e-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9118e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9118e-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9118e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9118e-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9118e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9118e-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9118e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9118e-125">Header</span><span class="sxs-lookup"><span data-stu-id="9118e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9118e-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9118e-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9118e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9118e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9118e-128">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9118e-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="9118e-129">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9118e-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




