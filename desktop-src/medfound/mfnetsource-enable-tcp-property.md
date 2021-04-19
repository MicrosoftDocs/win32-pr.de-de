---
description: Gibt an, ob der TCP-Transport für die Netzwerkquelle aktiviert ist.
ms.assetid: ba655505-dcac-4cea-8ad5-ccd1b55ee9d4
title: MFNETSOURCE_ENABLE_TCP-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37d5d43fad2ef7132007a9eb037c383ccc2ac9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360097"
---
# <a name="mfnetsource_enable_tcp-property"></a><span data-ttu-id="5c1eb-103">MF-Quell \_ - \_ TCP-Eigenschaft aktivieren</span><span class="sxs-lookup"><span data-stu-id="5c1eb-103">MFNETSOURCE\_ENABLE\_TCP property</span></span>

<span data-ttu-id="5c1eb-104">Gibt an, ob der TCP-Transport für die Netzwerkquelle aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-104">Specifies whether TCP transport is enabled for the network source.</span></span>



<span data-ttu-id="5c1eb-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5c1eb-105">Data type</span></span>

<span data-ttu-id="5c1eb-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="5c1eb-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="5c1eb-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="5c1eb-107">PROPVARIANT member</span></span>

<span data-ttu-id="5c1eb-108">Boolescher Wert (**Long**)</span><span class="sxs-lookup"><span data-stu-id="5c1eb-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="5c1eb-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="5c1eb-109">VT\_I4</span></span>

<span data-ttu-id="5c1eb-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="5c1eb-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="5c1eb-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c1eb-111">Remarks</span></span>

<span data-ttu-id="5c1eb-112">Die Konstante " **MF-Quelle \_ acceleratedstreamingduration** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-112">The constant **MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION** defines the GUID for this property key.</span></span> <span data-ttu-id="5c1eb-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="5c1eb-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="5c1eb-114">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="5c1eb-115">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="5c1eb-116">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="5c1eb-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c1eb-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c1eb-117">Requirements</span></span>



| <span data-ttu-id="5c1eb-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c1eb-118">Requirement</span></span> | <span data-ttu-id="5c1eb-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5c1eb-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c1eb-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c1eb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5c1eb-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c1eb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5c1eb-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c1eb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5c1eb-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c1eb-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5c1eb-124">Header</span><span class="sxs-lookup"><span data-stu-id="5c1eb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c1eb-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c1eb-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c1eb-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c1eb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c1eb-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5c1eb-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="5c1eb-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5c1eb-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="5c1eb-129">Unterstützte Protokolle</span><span class="sxs-lookup"><span data-stu-id="5c1eb-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




