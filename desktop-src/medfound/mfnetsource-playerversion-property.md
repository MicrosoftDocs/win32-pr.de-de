---
description: Der Wert des Felds &\# 0034; c-Playerversion&\# 0034;, das die Netzwerkquelle für die Protokollierung verwendet.
ms.assetid: 7bc485de-345b-475c-bbae-0776aa63c93a
title: MFNETSOURCE_PLAYERVERSION-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddaee0fe3e476b2b6e078551b1191fe9fc96cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759667"
---
# <a name="mfnetsource_playerversion-property"></a><span data-ttu-id="39cb0-103">Eigenschaft "Playerversion" von MF NetSource \_</span><span class="sxs-lookup"><span data-stu-id="39cb0-103">MFNETSOURCE\_PLAYERVERSION property</span></span>

<span data-ttu-id="39cb0-104">Der Wert des Felds "c-Playerversion", das von der Netzwerkquelle für die Protokollierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="39cb0-104">The value of the "c-playerversion" field that the network source uses for logging.</span></span> <span data-ttu-id="39cb0-105">Anwendungen können diese Eigenschaft auf die Versionsnummer der Anwendung festlegen.</span><span class="sxs-lookup"><span data-stu-id="39cb0-105">Applications can set this property to the version number of the application.</span></span>



<span data-ttu-id="39cb0-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="39cb0-106">Data type</span></span>

<span data-ttu-id="39cb0-107">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="39cb0-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="39cb0-108">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="39cb0-108">PROPVARIANT member</span></span>

<span data-ttu-id="39cb0-109">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="39cb0-109">**LONGLONG**</span></span>

<span data-ttu-id="39cb0-110">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="39cb0-110">VT\_I8</span></span>

<span data-ttu-id="39cb0-111">**Hval**</span><span class="sxs-lookup"><span data-stu-id="39cb0-111">**hVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="39cb0-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39cb0-112">Remarks</span></span>

<span data-ttu-id="39cb0-113">Die Konstante **MF-Quelle \_ Playerversion** definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="39cb0-113">The constant **MFNETSOURCE\_PLAYERVERSION** defines the GUID for this property key.</span></span> <span data-ttu-id="39cb0-114">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="39cb0-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="39cb0-115">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="39cb0-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="39cb0-116">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="39cb0-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="39cb0-117">Weitere Informationen finden Sie unter [quellresolver](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="39cb0-117">For more information, see [Source Resolver](source-resolver.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39cb0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39cb0-118">Requirements</span></span>



| <span data-ttu-id="39cb0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39cb0-119">Requirement</span></span> | <span data-ttu-id="39cb0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="39cb0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39cb0-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39cb0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="39cb0-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39cb0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="39cb0-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39cb0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="39cb0-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39cb0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="39cb0-125">Header</span><span class="sxs-lookup"><span data-stu-id="39cb0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="39cb0-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="39cb0-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39cb0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39cb0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39cb0-128">Client Protokollierung</span><span class="sxs-lookup"><span data-stu-id="39cb0-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="39cb0-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="39cb0-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="39cb0-130">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="39cb0-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




