---
description: Gibt an, ob der Datenstrom Wechsel in der Netzwerkquelle aktiviert ist.
ms.assetid: 691a3549-eaf8-4e3d-ad0e-e5b013658f78
title: MFNETSOURCE_THINNINGENABLED-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d5b1b362f8776e80e3d12b591dbf2116217846
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958647"
---
# <a name="mfnetsource_thinningenabled-property"></a><span data-ttu-id="1dd96-103">MF-Quelle \_ thinningenabled (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1dd96-103">MFNETSOURCE\_THINNINGENABLED property</span></span>

<span data-ttu-id="1dd96-104">Gibt an, ob der Datenstrom Wechsel in der Netzwerkquelle aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1dd96-104">Specifies whether stream switching is enabled on the network source.</span></span> <span data-ttu-id="1dd96-105">Der Datenstrom Wechsel ermöglicht es dem Medienserver, Datenströme in einer MBR-Datei (Multiple Bitrate) basierend auf der verfügbaren Bandbreite zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1dd96-105">Stream switching enables the media server to change streams in a multiple bit-rate (MBR) file, based on available bandwidth.</span></span>



<span data-ttu-id="1dd96-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1dd96-106">Data type</span></span>

<span data-ttu-id="1dd96-107">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="1dd96-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="1dd96-108">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="1dd96-108">PROPVARIANT member</span></span>

<span data-ttu-id="1dd96-109">Boolescher Wert (**Long**)</span><span class="sxs-lookup"><span data-stu-id="1dd96-109">Boolean (**LONG**)</span></span>

<span data-ttu-id="1dd96-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1dd96-110">VT\_I4</span></span>

<span data-ttu-id="1dd96-111">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="1dd96-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="1dd96-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1dd96-112">Remarks</span></span>

<span data-ttu-id="1dd96-113">Die Konstante **MF-Quelle \_ thinningenabled** definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="1dd96-113">The constant **MFNETSOURCE\_THINNINGENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="1dd96-114">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1dd96-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="1dd96-115">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1dd96-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="1dd96-116">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="1dd96-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="1dd96-117">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="1dd96-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="1dd96-118">Der Standardwert dieser Eigenschaft ist **true**.</span><span class="sxs-lookup"><span data-stu-id="1dd96-118">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dd96-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1dd96-119">Requirements</span></span>



| <span data-ttu-id="1dd96-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1dd96-120">Requirement</span></span> | <span data-ttu-id="1dd96-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1dd96-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd96-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1dd96-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1dd96-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1dd96-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1dd96-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1dd96-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1dd96-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1dd96-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1dd96-126">Header</span><span class="sxs-lookup"><span data-stu-id="1dd96-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dd96-127"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dd96-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dd96-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dd96-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dd96-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1dd96-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="1dd96-130">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1dd96-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




