---
description: Gibt an, ob die Netzwerkquelle Inhalte zwischenspeichert.
ms.assetid: f9a36315-083c-4ebb-9d36-d55fc1f21621
title: MFNETSOURCE_CACHEENABLED-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6f38398e44eaa25da7a5b1f88a76edb8e40924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863163"
---
# <a name="mfnetsource_cacheenabled-property"></a><span data-ttu-id="92c24-103">Cacheaktivierte Eigenschaft "MF NetSource" \_</span><span class="sxs-lookup"><span data-stu-id="92c24-103">MFNETSOURCE\_CACHEENABLED property</span></span>

<span data-ttu-id="92c24-104">Gibt an, ob die Netzwerkquelle Inhalte zwischenspeichert.</span><span class="sxs-lookup"><span data-stu-id="92c24-104">Specifies whether the network source caches content.</span></span>



<span data-ttu-id="92c24-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="92c24-105">Data type</span></span>

<span data-ttu-id="92c24-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="92c24-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="92c24-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="92c24-107">PROPVARIANT member</span></span>

<span data-ttu-id="92c24-108">Boolescher Wert (**Long**)</span><span class="sxs-lookup"><span data-stu-id="92c24-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="92c24-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="92c24-109">VT\_I4</span></span>

<span data-ttu-id="92c24-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="92c24-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="92c24-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92c24-111">Remarks</span></span>

<span data-ttu-id="92c24-112">Die Konstante " **MF NetSource \_ cacheaktivierte** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="92c24-112">The constant **MFNETSOURCE\_CACHEENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="92c24-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="92c24-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="92c24-114">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="92c24-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="92c24-115">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="92c24-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="92c24-116">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="92c24-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="92c24-117">Der Standardwert dieser Eigenschaft ist **true**.</span><span class="sxs-lookup"><span data-stu-id="92c24-117">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="92c24-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92c24-118">Requirements</span></span>



| <span data-ttu-id="92c24-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92c24-119">Requirement</span></span> | <span data-ttu-id="92c24-120">Wert</span><span class="sxs-lookup"><span data-stu-id="92c24-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92c24-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92c24-121">Minimum supported client</span></span><br/> | <span data-ttu-id="92c24-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92c24-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="92c24-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92c24-123">Minimum supported server</span></span><br/> | <span data-ttu-id="92c24-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92c24-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="92c24-125">Header</span><span class="sxs-lookup"><span data-stu-id="92c24-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="92c24-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="92c24-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92c24-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92c24-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92c24-128">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="92c24-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="92c24-129">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="92c24-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




