---
description: Liste der URLs, an die die Netzwerkquelle Protokollierungs Informationen sendet.
ms.assetid: 772c5b57-273d-4289-9229-ef7a199c6473
title: MFNETSOURCE_LOGURL-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6956a7deb251ee9a25261a1b6c6a723973f7a03b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129781"
---
# <a name="mfnetsource_logurl-property"></a><span data-ttu-id="d0083-103">MF NetSource- \_ LogURL (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d0083-103">MFNETSOURCE\_LOGURL property</span></span>

<span data-ttu-id="d0083-104">Liste der URLs, an die die Netzwerkquelle Protokollierungs Informationen sendet.</span><span class="sxs-lookup"><span data-stu-id="d0083-104">List of URLs to which the network source will send logging information.</span></span>



<span data-ttu-id="d0083-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d0083-105">Data type</span></span>

<span data-ttu-id="d0083-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="d0083-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d0083-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="d0083-107">PROPVARIANT member</span></span>

<span data-ttu-id="d0083-108">Array von Zeichen folgen mit breit Zeichen (**calpwstr**)</span><span class="sxs-lookup"><span data-stu-id="d0083-108">Array of wide-character strings (**CALPWSTR**)</span></span>

<span data-ttu-id="d0083-109">VT \_ Vector \| VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="d0083-109">VT\_VECTOR \| VT\_LPWSTR</span></span>

<span data-ttu-id="d0083-110">**calpwstr**</span><span class="sxs-lookup"><span data-stu-id="d0083-110">**calpwstr**</span></span>



## <a name="remarks"></a><span data-ttu-id="d0083-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0083-111">Remarks</span></span>

<span data-ttu-id="d0083-112">Die Konstante " **MF NetSource \_ LogURL** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="d0083-112">The constant **MFNETSOURCE\_LOGURL** defines the GUID for this property key.</span></span> <span data-ttu-id="d0083-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d0083-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="d0083-114">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d0083-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="d0083-115">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="d0083-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="d0083-116">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="d0083-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0083-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0083-117">Requirements</span></span>



| <span data-ttu-id="d0083-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0083-118">Requirement</span></span> | <span data-ttu-id="d0083-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d0083-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d0083-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0083-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d0083-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0083-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d0083-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0083-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d0083-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0083-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d0083-124">Header</span><span class="sxs-lookup"><span data-stu-id="d0083-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0083-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0083-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0083-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0083-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0083-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0083-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d0083-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0083-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




