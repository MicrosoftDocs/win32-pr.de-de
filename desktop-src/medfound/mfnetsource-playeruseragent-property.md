---
description: Der Wert des zweiten Teils des \# Felds &0034; CS (User-Agent) &\# 0034;, das die Netzwerkquelle für die Protokollierung verwendet.
ms.assetid: c662a6d6-5e0b-4c28-841d-5774d4103d4b
title: MFNETSOURCE_PLAYERUSERAGENT-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f4d06eaea566e22e1239ed04594f2f592c7cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357380"
---
# <a name="mfnetsource_playeruseragent-property"></a><span data-ttu-id="97680-103">Eigenschaft "playeruseragent" von MF NetSource \_</span><span class="sxs-lookup"><span data-stu-id="97680-103">MFNETSOURCE\_PLAYERUSERAGENT property</span></span>

<span data-ttu-id="97680-104">Der Wert des zweiten Teils des Felds "CS (User-Agent)", das die Netzwerkquelle für die Protokollierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="97680-104">The value of the second portion of the "cs(User-Agent)" field that the network source uses for logging.</span></span> <span data-ttu-id="97680-105">Anwendungen können diese Eigenschaft auf einen beliebigen Zeichen folgen Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="97680-105">Applications can set this property to any string value.</span></span>



<span data-ttu-id="97680-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="97680-106">Data type</span></span>

<span data-ttu-id="97680-107">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="97680-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="97680-108">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="97680-108">PROPVARIANT member</span></span>

<span data-ttu-id="97680-109">Breit Zeichen-Zeichenfolge (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="97680-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="97680-110">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="97680-110">VT\_LPWSTR</span></span>

<span data-ttu-id="97680-111">**pwszval**</span><span class="sxs-lookup"><span data-stu-id="97680-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="97680-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97680-112">Remarks</span></span>

<span data-ttu-id="97680-113">Der Konstante **MF-Quell- \_ playeruseragent** definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="97680-113">The constant **MFNETSOURCE\_PLAYERUSERAGENT** defines the GUID for this property key.</span></span> <span data-ttu-id="97680-114">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="97680-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="97680-115">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="97680-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="97680-116">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="97680-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="97680-117">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="97680-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97680-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97680-118">Requirements</span></span>



| <span data-ttu-id="97680-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97680-119">Requirement</span></span> | <span data-ttu-id="97680-120">Wert</span><span class="sxs-lookup"><span data-stu-id="97680-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="97680-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97680-121">Minimum supported client</span></span><br/> | <span data-ttu-id="97680-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97680-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="97680-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97680-123">Minimum supported server</span></span><br/> | <span data-ttu-id="97680-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97680-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="97680-125">Header</span><span class="sxs-lookup"><span data-stu-id="97680-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="97680-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="97680-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97680-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97680-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97680-128">Client Protokollierung</span><span class="sxs-lookup"><span data-stu-id="97680-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="97680-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97680-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="97680-130">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97680-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="97680-131">**MF-Quelle \_ browseruseragent**</span><span class="sxs-lookup"><span data-stu-id="97680-131">**MFNETSOURCE\_BROWSERUSERAGENT**</span></span>](mfnetsource-browseruseragent-property.md)
</dt> </dl>

 

 




