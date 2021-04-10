---
description: Maximale Dauer des beschleunigten Streamings in Millisekunden, wenn die Netzwerkquelle UDP-Transport verwendet.
ms.assetid: d5f3064a-b222-4f72-b889-cd88c14a239c
title: MFNETSOURCE_MAXUDPACCELERATEDSTREAMINGDURATION-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2621e01203ba81b54e565f86953df64304c9bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050457"
---
# <a name="mfnetsource_maxudpacceleratedstreamingduration-property"></a><span data-ttu-id="b74f1-103">MF NetSource \_ maxudpacceleratedstreamingduration (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b74f1-103">MFNETSOURCE\_MAXUDPACCELERATEDSTREAMINGDURATION property</span></span>

<span data-ttu-id="b74f1-104">Maximale Dauer des beschleunigten Streamings in Millisekunden, wenn die Netzwerkquelle UDP-Transport verwendet.</span><span class="sxs-lookup"><span data-stu-id="b74f1-104">Maximum duration of accelerated streaming, in milliseconds, when the network source uses UDP transport.</span></span>



<span data-ttu-id="b74f1-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b74f1-105">Data type</span></span>

<span data-ttu-id="b74f1-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="b74f1-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="b74f1-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="b74f1-107">PROPVARIANT member</span></span>

<span data-ttu-id="b74f1-108">**DWORD** (als **Long** gespeichert)</span><span class="sxs-lookup"><span data-stu-id="b74f1-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="b74f1-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="b74f1-109">VT\_I4</span></span>

<span data-ttu-id="b74f1-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="b74f1-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="b74f1-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b74f1-111">Remarks</span></span>

<span data-ttu-id="b74f1-112">Die Konstante " **MF NetSource \_ maxudpacceleratedstreamingduration** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="b74f1-112">The constant **MFNETSOURCE\_MAXUDPACCELERATEDSTREAMINGDURATION** defines the GUID for this property key.</span></span> <span data-ttu-id="b74f1-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b74f1-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="b74f1-114">Für den UDP-Transport überschreibt diese Eigenschaft die Eigenschaft [**msnetsource \_ acceleratedstreamingduration**](mfnetsource-acceleratedstreamingduration-property.md) , wenn der Wert dieser Eigenschaft niedriger ist.</span><span class="sxs-lookup"><span data-stu-id="b74f1-114">For UDP transport, this property overrides the [**MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) property if the value of this property is lower.</span></span>

<span data-ttu-id="b74f1-115">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b74f1-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="b74f1-116">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="b74f1-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="b74f1-117">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="b74f1-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="b74f1-118">Der Standardwert dieser Eigenschaft ist 8.000 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="b74f1-118">The default value of this property is 8,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="b74f1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b74f1-119">Requirements</span></span>



| <span data-ttu-id="b74f1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b74f1-120">Requirement</span></span> | <span data-ttu-id="b74f1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b74f1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b74f1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b74f1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b74f1-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b74f1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b74f1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b74f1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b74f1-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b74f1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b74f1-126">Header</span><span class="sxs-lookup"><span data-stu-id="b74f1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b74f1-127"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b74f1-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b74f1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b74f1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b74f1-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b74f1-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="b74f1-130">Netzwerk Quell Features</span><span class="sxs-lookup"><span data-stu-id="b74f1-130">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="b74f1-131">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b74f1-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




