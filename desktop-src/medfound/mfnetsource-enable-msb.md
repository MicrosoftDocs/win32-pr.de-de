---
description: Gibt an, ob das Multicast Protokoll von Media Stream Broadcast (MSB) in der Netzwerkquelle aktiviert ist.
ms.assetid: a46e3b4c-60be-4470-b9dc-041902c2563c
title: MFNETSOURCE_ENABLE_MSB-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6b2a49876cf504bfc4e086ab1e064e6835283a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360098"
---
# <a name="mfnetsource_enable_msb-property"></a><span data-ttu-id="60e9c-103">MF-Quell \_ \_ Eigenschaft "MSB-Eigenschaft aktivieren"</span><span class="sxs-lookup"><span data-stu-id="60e9c-103">MFNETSOURCE\_ENABLE\_MSB property</span></span>

<span data-ttu-id="60e9c-104">Gibt an, ob das Multicast Protokoll von Media Stream Broadcast (MSB) in der Netzwerkquelle aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="60e9c-104">Specifies whether the Media Stream Broadcast (MSB) multicast protocol is enabled in the network source.</span></span>



<span data-ttu-id="60e9c-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="60e9c-105">Data type</span></span>

<span data-ttu-id="60e9c-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="60e9c-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="60e9c-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="60e9c-107">PROPVARIANT member</span></span>

<span data-ttu-id="60e9c-108">**LONG**</span><span class="sxs-lookup"><span data-stu-id="60e9c-108">**LONG**</span></span>

<span data-ttu-id="60e9c-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="60e9c-109">VT\_I4</span></span>

<span data-ttu-id="60e9c-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="60e9c-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="60e9c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60e9c-111">Remarks</span></span>

<span data-ttu-id="60e9c-112">Die Konstante " **MF NetSource" zum \_ Aktivieren von \_ MSB** definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="60e9c-112">The constant **MFNETSOURCE\_ENABLE\_MSB** defines the GUID for this property key.</span></span> <span data-ttu-id="60e9c-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="60e9c-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="60e9c-114">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="60e9c-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="60e9c-115">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="60e9c-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="60e9c-116">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="60e9c-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60e9c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60e9c-117">Requirements</span></span>



| <span data-ttu-id="60e9c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60e9c-118">Requirement</span></span> | <span data-ttu-id="60e9c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="60e9c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="60e9c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60e9c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="60e9c-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60e9c-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="60e9c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60e9c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="60e9c-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60e9c-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="60e9c-124">Header</span><span class="sxs-lookup"><span data-stu-id="60e9c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="60e9c-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="60e9c-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60e9c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60e9c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e9c-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="60e9c-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="60e9c-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="60e9c-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="60e9c-129">Unterstützte Protokolle</span><span class="sxs-lookup"><span data-stu-id="60e9c-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




