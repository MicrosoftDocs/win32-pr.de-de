---
description: Anzahl von Sekunden, die die Netzwerkquelle beim Start puffert.
ms.assetid: 186b55fc-d1b1-4187-a748-efaee114eca9
title: MFNETSOURCE_BUFFERINGTIME-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21c165e58ebd5f2aec0f1ca7ce38281f8c94896d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130120"
---
# <a name="mfnetsource_bufferingtime-property"></a><span data-ttu-id="00d7f-103">MF NetSource \_ BufferingTime (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="00d7f-103">MFNETSOURCE\_BUFFERINGTIME property</span></span>

<span data-ttu-id="00d7f-104">Anzahl von Sekunden, die die Netzwerkquelle beim Start puffert.</span><span class="sxs-lookup"><span data-stu-id="00d7f-104">Number of seconds of data that the network source buffers at startup.</span></span>



<span data-ttu-id="00d7f-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="00d7f-105">Data type</span></span>

<span data-ttu-id="00d7f-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="00d7f-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="00d7f-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="00d7f-107">PROPVARIANT member</span></span>

<span data-ttu-id="00d7f-108">**DWORD** (als **Long** gespeichert)</span><span class="sxs-lookup"><span data-stu-id="00d7f-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="00d7f-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="00d7f-109">VT\_I4</span></span>

<span data-ttu-id="00d7f-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="00d7f-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="00d7f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00d7f-111">Remarks</span></span>

<span data-ttu-id="00d7f-112">Die Konstante " **MF NetSource \_ BufferingTime** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="00d7f-112">The constant **MFNETSOURCE\_BUFFERINGTIME** defines the GUID for this property key.</span></span> <span data-ttu-id="00d7f-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="00d7f-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="00d7f-114">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="00d7f-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="00d7f-115">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="00d7f-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="00d7f-116">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="00d7f-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="00d7f-117">Der Standardwert dieser Eigenschaft ist 5 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="00d7f-117">The default value of this property is 5 seconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="00d7f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00d7f-118">Requirements</span></span>



| <span data-ttu-id="00d7f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00d7f-119">Requirement</span></span> | <span data-ttu-id="00d7f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="00d7f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00d7f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00d7f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="00d7f-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00d7f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="00d7f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00d7f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="00d7f-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00d7f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="00d7f-125">Header</span><span class="sxs-lookup"><span data-stu-id="00d7f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="00d7f-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="00d7f-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00d7f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00d7f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00d7f-128">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="00d7f-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="00d7f-129">Netzwerk Quell Features</span><span class="sxs-lookup"><span data-stu-id="00d7f-129">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="00d7f-130">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="00d7f-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




