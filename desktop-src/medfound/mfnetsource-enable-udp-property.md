---
description: Gibt an, ob der UDP (User Datagram Protocol)-Transport in der Netzwerkquelle aktiviert ist.
ms.assetid: d46a59e6-8abc-484b-aecc-edf57ffff512
title: MFNETSOURCE_ENABLE_UDP-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d326cbd375a7d7e22ea2afc121dd4af9086e60c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959046"
---
# <a name="mfnetsource_enable_udp-property"></a><span data-ttu-id="aed90-103">MF-Quell \_ Eigenschaft "UDP aktivieren" \_</span><span class="sxs-lookup"><span data-stu-id="aed90-103">MFNETSOURCE\_ENABLE\_UDP property</span></span>

<span data-ttu-id="aed90-104">Gibt an, ob der UDP (User Datagram Protocol)-Transport in der Netzwerkquelle aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="aed90-104">Specifies whether User Datagram Protocol (UDP) transport is enabled in the network source.</span></span>



<span data-ttu-id="aed90-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="aed90-105">Data type</span></span>

<span data-ttu-id="aed90-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="aed90-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="aed90-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="aed90-107">PROPVARIANT member</span></span>

<span data-ttu-id="aed90-108">Boolescher Wert (**Long**)</span><span class="sxs-lookup"><span data-stu-id="aed90-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="aed90-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="aed90-109">VT\_I4</span></span>

<span data-ttu-id="aed90-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="aed90-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="aed90-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aed90-111">Remarks</span></span>

<span data-ttu-id="aed90-112">Die Konstante " **MF NetSource \_ enable \_ UDP** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="aed90-112">The constant **MFNETSOURCE\_ENABLE\_UDP** defines the GUID for this property key.</span></span> <span data-ttu-id="aed90-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="aed90-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="aed90-114">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="aed90-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="aed90-115">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="aed90-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="aed90-116">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="aed90-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aed90-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aed90-117">Requirements</span></span>



| <span data-ttu-id="aed90-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aed90-118">Requirement</span></span> | <span data-ttu-id="aed90-119">Wert</span><span class="sxs-lookup"><span data-stu-id="aed90-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aed90-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aed90-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aed90-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aed90-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="aed90-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aed90-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aed90-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aed90-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="aed90-124">Header</span><span class="sxs-lookup"><span data-stu-id="aed90-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aed90-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aed90-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aed90-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aed90-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aed90-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aed90-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="aed90-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aed90-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="aed90-129">Unterstützte Protokolle</span><span class="sxs-lookup"><span data-stu-id="aed90-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




