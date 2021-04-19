---
description: Maximale Datenmenge, die der Netzwerk Quell Puffer in Millisekunden angibt.
ms.assetid: bd776dc2-341a-4d87-8a06-8063daf53ede
title: MFNETSOURCE_MAXBUFFERTIMEMS-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f98cd17f33bb893dacd02b2a00669f3d2355e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360079"
---
# <a name="mfnetsource_maxbuffertimems-property"></a><span data-ttu-id="be7c9-103">MF-Quelle \_ maxbuffertimems (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="be7c9-103">MFNETSOURCE\_MAXBUFFERTIMEMS property</span></span>

<span data-ttu-id="be7c9-104">Maximale Datenmenge, die der Netzwerk Quell Puffer in Millisekunden angibt.</span><span class="sxs-lookup"><span data-stu-id="be7c9-104">Maximum amount of data the network source buffers, in milliseconds.</span></span>



<span data-ttu-id="be7c9-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="be7c9-105">Data type</span></span>

<span data-ttu-id="be7c9-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="be7c9-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="be7c9-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="be7c9-107">PROPVARIANT member</span></span>

<span data-ttu-id="be7c9-108">**DWORD** (als **Long** gespeichert)</span><span class="sxs-lookup"><span data-stu-id="be7c9-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="be7c9-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="be7c9-109">VT\_I4</span></span>

<span data-ttu-id="be7c9-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="be7c9-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="be7c9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be7c9-111">Remarks</span></span>

<span data-ttu-id="be7c9-112">Die Konstante " **MF NetSource \_ maxbuffertimems** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="be7c9-112">The constant **MFNETSOURCE\_MAXBUFFERTIMEMS** defines the GUID for this property key.</span></span> <span data-ttu-id="be7c9-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="be7c9-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="be7c9-114">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="be7c9-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="be7c9-115">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="be7c9-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="be7c9-116">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="be7c9-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="be7c9-117">Der Standardwert dieser Eigenschaft ist 40.000 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="be7c9-117">The default value of this property is 40,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="be7c9-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be7c9-118">Requirements</span></span>



| <span data-ttu-id="be7c9-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be7c9-119">Requirement</span></span> | <span data-ttu-id="be7c9-120">Wert</span><span class="sxs-lookup"><span data-stu-id="be7c9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be7c9-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be7c9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="be7c9-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be7c9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="be7c9-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be7c9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="be7c9-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be7c9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="be7c9-125">Header</span><span class="sxs-lookup"><span data-stu-id="be7c9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="be7c9-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="be7c9-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be7c9-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be7c9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be7c9-128">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="be7c9-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="be7c9-129">Netzwerk Quell Features</span><span class="sxs-lookup"><span data-stu-id="be7c9-129">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="be7c9-130">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="be7c9-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




