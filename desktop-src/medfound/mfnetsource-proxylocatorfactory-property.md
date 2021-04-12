---
description: Enthält einen Zeiger auf die imfnetproxyloerfactory-Schnittstelle.
ms.assetid: 455325c0-5116-4e81-9729-fab9c6a367c7
title: MFNETSOURCE_PROXYLOCATORFACTORY-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1199333e9eb343ab9d8f96864372b2dc385ab7d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130712"
---
# <a name="mfnetsource_proxylocatorfactory-property"></a><span data-ttu-id="66f47-103">Eigenschaft "MF NetSource \_ proxylo. Factory"</span><span class="sxs-lookup"><span data-stu-id="66f47-103">MFNETSOURCE\_PROXYLOCATORFACTORY property</span></span>

<span data-ttu-id="66f47-104">Enthält einen Zeiger auf die [**imfnetproxyloerfactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="66f47-104">Contains a pointer to the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span>



<span data-ttu-id="66f47-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="66f47-105">Data type</span></span>

<span data-ttu-id="66f47-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="66f47-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="66f47-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="66f47-107">PROPVARIANT member</span></span>

<span data-ttu-id="66f47-108">**IUnknown** -Zeiger</span><span class="sxs-lookup"><span data-stu-id="66f47-108">**IUnknown** pointer</span></span>

<span data-ttu-id="66f47-109">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="66f47-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="66f47-110">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="66f47-110">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="66f47-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66f47-111">Remarks</span></span>

<span data-ttu-id="66f47-112">Die Konstante " **MF NetSource \_ proxyloskiorfactory** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="66f47-112">The constant **MFNETSOURCE\_PROXYLOCATORFACTORY** defines the GUID for this property key.</span></span> <span data-ttu-id="66f47-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="66f47-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="66f47-114">Anwendungen können diese Eigenschaft verwenden, um einen benutzerdefinierten proxylocator für die Netzwerkquelle bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="66f47-114">Applications can use this property to provide a custom proxy locator for the network source.</span></span> <span data-ttu-id="66f47-115">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="66f47-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="66f47-116">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="66f47-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66f47-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66f47-117">Requirements</span></span>



| <span data-ttu-id="66f47-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66f47-118">Requirement</span></span> | <span data-ttu-id="66f47-119">Wert</span><span class="sxs-lookup"><span data-stu-id="66f47-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66f47-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66f47-120">Minimum supported client</span></span><br/> | <span data-ttu-id="66f47-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66f47-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="66f47-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66f47-122">Minimum supported server</span></span><br/> | <span data-ttu-id="66f47-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66f47-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="66f47-124">Header</span><span class="sxs-lookup"><span data-stu-id="66f47-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="66f47-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66f47-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66f47-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66f47-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f47-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66f47-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="66f47-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66f47-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="66f47-129">Proxy Unterstützung für Netzwerk Quellen</span><span class="sxs-lookup"><span data-stu-id="66f47-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




