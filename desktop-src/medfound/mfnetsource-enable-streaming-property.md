---
description: Gibt an, ob alle Streamingprotokolle aktiviert sind.
ms.assetid: cf072572-58f7-429a-954a-8808d05248f0
title: MFNETSOURCE_ENABLE_STREAMING-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29fc8ae10dedd5cb904e43ee79ff64e8f451e37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527377"
---
# <a name="mfnetsource_enable_streaming-property"></a><span data-ttu-id="60b54-103">MF-Quell \_ Eigenschaft "Streaming aktivieren" \_</span><span class="sxs-lookup"><span data-stu-id="60b54-103">MFNETSOURCE\_ENABLE\_STREAMING property</span></span>

<span data-ttu-id="60b54-104">Gibt an, ob alle Streamingprotokolle aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="60b54-104">Specifies whether all streaming protocols are enabled.</span></span>



<span data-ttu-id="60b54-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="60b54-105">Data type</span></span>

<span data-ttu-id="60b54-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="60b54-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="60b54-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="60b54-107">PROPVARIANT member</span></span>

<span data-ttu-id="60b54-108">Boolescher Wert (**Long**)</span><span class="sxs-lookup"><span data-stu-id="60b54-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="60b54-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="60b54-109">VT\_I4</span></span>

<span data-ttu-id="60b54-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="60b54-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="60b54-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60b54-111">Remarks</span></span>

<span data-ttu-id="60b54-112">Die Konstante " **MF NetSource \_ enable \_ Streaming** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="60b54-112">The constant **MFNETSOURCE\_ENABLE\_STREAMING** defines the GUID for this property key.</span></span> <span data-ttu-id="60b54-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="60b54-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="60b54-114">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="60b54-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="60b54-115">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an die [Konfiguration einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="60b54-115">To set the property, pass an **IPropertyStore** pointer to the [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60b54-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60b54-116">Requirements</span></span>



| <span data-ttu-id="60b54-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60b54-117">Requirement</span></span> | <span data-ttu-id="60b54-118">Wert</span><span class="sxs-lookup"><span data-stu-id="60b54-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="60b54-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60b54-119">Minimum supported client</span></span><br/> | <span data-ttu-id="60b54-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60b54-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="60b54-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60b54-121">Minimum supported server</span></span><br/> | <span data-ttu-id="60b54-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60b54-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="60b54-123">Header</span><span class="sxs-lookup"><span data-stu-id="60b54-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="60b54-124"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="60b54-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b54-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60b54-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b54-126">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="60b54-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="60b54-127">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="60b54-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="60b54-128">Unterstützte Protokolle</span><span class="sxs-lookup"><span data-stu-id="60b54-128">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




