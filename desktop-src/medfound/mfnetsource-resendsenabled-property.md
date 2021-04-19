---
description: Gibt an, ob die Netzwerkquelle als Reaktion auf verlorene Pakete UDP-erneut senden-Anforderungen sendet.
ms.assetid: 7956536d-9f3d-4875-8006-17e2cd577b61
title: MFNETSOURCE_RESENDSENABLED-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2646a9ef3e23fbcc9b3dff205f87d268115177
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350546"
---
# <a name="mfnetsource_resendsenabled-property"></a><span data-ttu-id="977b1-103">MF-Quelle \_ resendsenabled (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="977b1-103">MFNETSOURCE\_RESENDSENABLED property</span></span>

<span data-ttu-id="977b1-104">Gibt an, ob die Netzwerkquelle als Reaktion auf verlorene Pakete UDP-erneut senden-Anforderungen sendet.</span><span class="sxs-lookup"><span data-stu-id="977b1-104">Specifies whether the network source sends UDP resend requests in response to lost packets.</span></span>



<span data-ttu-id="977b1-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="977b1-105">Data type</span></span>

<span data-ttu-id="977b1-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="977b1-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="977b1-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="977b1-107">PROPVARIANT member</span></span>

<span data-ttu-id="977b1-108">Boolescher Wert (**Long**)</span><span class="sxs-lookup"><span data-stu-id="977b1-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="977b1-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="977b1-109">VT\_I4</span></span>

<span data-ttu-id="977b1-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="977b1-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="977b1-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="977b1-111">Remarks</span></span>

<span data-ttu-id="977b1-112">Die Konstante " **MF NetSource \_ resendsenabled** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="977b1-112">The constant **MFNETSOURCE\_RESENDSENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="977b1-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="977b1-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="977b1-114">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="977b1-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="977b1-115">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="977b1-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="977b1-116">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="977b1-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="977b1-117">Der Standardwert dieser Eigenschaft ist **true**.</span><span class="sxs-lookup"><span data-stu-id="977b1-117">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="977b1-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="977b1-118">Requirements</span></span>



| <span data-ttu-id="977b1-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="977b1-119">Requirement</span></span> | <span data-ttu-id="977b1-120">Wert</span><span class="sxs-lookup"><span data-stu-id="977b1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="977b1-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="977b1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="977b1-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="977b1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="977b1-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="977b1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="977b1-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="977b1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="977b1-125">Header</span><span class="sxs-lookup"><span data-stu-id="977b1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="977b1-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="977b1-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="977b1-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="977b1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="977b1-128">Client Protokollierung</span><span class="sxs-lookup"><span data-stu-id="977b1-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="977b1-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="977b1-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="977b1-130">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="977b1-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




