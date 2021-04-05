---
description: Gibt an, ob alle Download Protokolle aktiviert sind.
ms.assetid: c178693f-44ea-481e-b7f2-2ec94eea1994
title: MFNETSOURCE_ENABLE_DOWNLOAD-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1b57d8ab984f7c198d1c1b43455f2d0d5dda68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041851"
---
# <a name="mfnetsource_enable_download-property"></a><span data-ttu-id="bf114-103">MF-Quelle zum \_ Aktivieren der \_ Download Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bf114-103">MFNETSOURCE\_ENABLE\_DOWNLOAD property</span></span>

<span data-ttu-id="bf114-104">Gibt an, ob alle Download Protokolle aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="bf114-104">Specifies whether all download protocols are enabled.</span></span>



<span data-ttu-id="bf114-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bf114-105">Data type</span></span>

<span data-ttu-id="bf114-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="bf114-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="bf114-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="bf114-107">PROPVARIANT member</span></span>

<span data-ttu-id="bf114-108">Boolescher Wert (**Long**)</span><span class="sxs-lookup"><span data-stu-id="bf114-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="bf114-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="bf114-109">VT\_I4</span></span>

<span data-ttu-id="bf114-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="bf114-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="bf114-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf114-111">Remarks</span></span>

<span data-ttu-id="bf114-112">Durch den Konstanten **\_ \_ Download von MF-Quelle aktivieren** wird die GUID für diesen Eigenschafts Schlüssel definiert.</span><span class="sxs-lookup"><span data-stu-id="bf114-112">The constant **MFNETSOURCE\_ENABLE\_DOWNLOAD** defines the GUID for this property key.</span></span> <span data-ttu-id="bf114-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="bf114-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="bf114-114">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="bf114-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="bf114-115">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an die [Konfiguration einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="bf114-115">To set the property, pass an **IPropertyStore** pointer to the [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf114-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf114-116">Requirements</span></span>



| <span data-ttu-id="bf114-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf114-117">Requirement</span></span> | <span data-ttu-id="bf114-118">Wert</span><span class="sxs-lookup"><span data-stu-id="bf114-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf114-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bf114-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bf114-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf114-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bf114-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bf114-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bf114-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf114-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bf114-123">Header</span><span class="sxs-lookup"><span data-stu-id="bf114-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf114-124"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf114-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf114-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf114-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf114-126">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bf114-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="bf114-127">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bf114-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="bf114-128">Unterstützte Protokolle</span><span class="sxs-lookup"><span data-stu-id="bf114-128">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




