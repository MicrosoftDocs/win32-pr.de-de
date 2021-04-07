---
description: Dauer des beschleunigten Streamings für die Netzwerkquelle in Millisekunden.
ms.assetid: 3f9cd762-f393-4130-ba25-d16da0642093
title: MFNETSOURCE_ACCELERATEDSTREAMINGDURATION-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57980fbe08d3c6f48cf2638b35e88c455e566e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863167"
---
# <a name="mfnetsource_acceleratedstreamingduration-property"></a><span data-ttu-id="aec03-103">MF-Quelle \_ acceleratedstreamingduration (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="aec03-103">MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION property</span></span>

<span data-ttu-id="aec03-104">Dauer des beschleunigten Streamings für die Netzwerkquelle in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="aec03-104">Duration of accelerated streaming for the network source, in milliseconds.</span></span>



<span data-ttu-id="aec03-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="aec03-105">Data type</span></span>

<span data-ttu-id="aec03-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="aec03-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="aec03-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="aec03-107">PROPVARIANT member</span></span>

<span data-ttu-id="aec03-108">**DWORD** (als **Long** gespeichert)</span><span class="sxs-lookup"><span data-stu-id="aec03-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="aec03-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="aec03-109">VT\_I4</span></span>

<span data-ttu-id="aec03-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="aec03-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="aec03-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aec03-111">Remarks</span></span>

<span data-ttu-id="aec03-112">Die Konstante " **MF-Quelle \_ acceleratedstreamingduration** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="aec03-112">The constant **MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION** defines the GUID for this property key.</span></span> <span data-ttu-id="aec03-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="aec03-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="aec03-114">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="aec03-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="aec03-115">Um die-Eigenschaft festzulegen, übergeben Sie ein **IPropertyStore** -Objekt an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="aec03-115">To set the property, pass an **IPropertyStore** object to the source resolver.</span></span> <span data-ttu-id="aec03-116">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="aec03-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="aec03-117">Diese Eigenschaft gilt für das schnell Start Feature von Windows Media Services, das Inhalte schnell wieder gibt, ohne auf eine lange anfängliche Pufferung zu warten.</span><span class="sxs-lookup"><span data-stu-id="aec03-117">This property applies to the Fast Start feature of Windows Media Services, which plays content quickly without waiting for lengthy initial buffering.</span></span> <span data-ttu-id="aec03-118">Wenn Sie den schnell Start verwenden, sendet der Server, auf dem Windows Media Services ausgeführt wird, Daten am Anfang der Geschwindigkeit schneller als durch die Bitrate des Inhalts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aec03-118">When using Fast Start, the server running Windows Media Services will send some data at the beginning of the content at a faster rate than that specified by the bit rate of the content.</span></span>

<span data-ttu-id="aec03-119">Der Standardwert dieser Eigenschaft ist 10.000 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="aec03-119">The default value of this property is 10,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="aec03-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aec03-120">Requirements</span></span>



| <span data-ttu-id="aec03-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aec03-121">Requirement</span></span> | <span data-ttu-id="aec03-122">Wert</span><span class="sxs-lookup"><span data-stu-id="aec03-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aec03-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aec03-123">Minimum supported client</span></span><br/> | <span data-ttu-id="aec03-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aec03-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="aec03-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aec03-125">Minimum supported server</span></span><br/> | <span data-ttu-id="aec03-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aec03-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="aec03-127">Header</span><span class="sxs-lookup"><span data-stu-id="aec03-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="aec03-128"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aec03-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aec03-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aec03-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aec03-130">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aec03-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="aec03-131">Netzwerk Quell Features</span><span class="sxs-lookup"><span data-stu-id="aec03-131">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="aec03-132">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aec03-132">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




