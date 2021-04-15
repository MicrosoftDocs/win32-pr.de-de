---
description: Der Wert des Felds &\# 0034; c-hostexever&\# 0034;, das die Netzwerkquelle für die Protokollierung verwendet.
ms.assetid: eee93457-483d-41dc-91c5-c12382d03152
title: MFNETSOURCE_HOSTVERSION-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f10c1a66bc2ab52455140733a6b60f25863c8f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485203"
---
# <a name="mfnetsource_hostversion-property"></a><span data-ttu-id="92e48-103">Mbernetsource- \_ Hostversion (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="92e48-103">MFNETSOURCE\_HOSTVERSION property</span></span>

<span data-ttu-id="92e48-104">Der Wert des Felds "c-hostexever", das von der Netzwerkquelle für die Protokollierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="92e48-104">The value of the "c-hostexever" field that the network source uses for logging.</span></span> <span data-ttu-id="92e48-105">Anwendungen können diese Eigenschaft auf die Versionsnummer der Host Anwendung festlegen.</span><span class="sxs-lookup"><span data-stu-id="92e48-105">Applications can set this property to the version number of the host application.</span></span> <span data-ttu-id="92e48-106">Die Host Anwendung ist die exe-Datei, die durch das Feld "c-hostexe" identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="92e48-106">The host application is the .exe file identified by the c-hostexe field.</span></span>



<span data-ttu-id="92e48-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="92e48-107">Data type</span></span>

<span data-ttu-id="92e48-108">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="92e48-108">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="92e48-109">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="92e48-109">PROPVARIANT member</span></span>

<span data-ttu-id="92e48-110">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="92e48-110">**LONGLONG**</span></span>

<span data-ttu-id="92e48-111">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="92e48-111">VT\_I8</span></span>

<span data-ttu-id="92e48-112">**Hval**</span><span class="sxs-lookup"><span data-stu-id="92e48-112">**hVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="92e48-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92e48-113">Remarks</span></span>

<span data-ttu-id="92e48-114">Die Konstante **mbernetsource- \_ Hostversion** definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="92e48-114">The constant **MFNETSOURCE\_HOSTVERSION** defines the GUID for this property key.</span></span> <span data-ttu-id="92e48-115">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="92e48-115">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="92e48-116">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="92e48-116">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="92e48-117">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="92e48-117">To set the property, pass an **IPropertyStore** pointer to the Source resolver.</span></span> <span data-ttu-id="92e48-118">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="92e48-118">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="92e48-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92e48-119">Requirements</span></span>



| <span data-ttu-id="92e48-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92e48-120">Requirement</span></span> | <span data-ttu-id="92e48-121">Wert</span><span class="sxs-lookup"><span data-stu-id="92e48-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92e48-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92e48-122">Minimum supported client</span></span><br/> | <span data-ttu-id="92e48-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92e48-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="92e48-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92e48-124">Minimum supported server</span></span><br/> | <span data-ttu-id="92e48-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92e48-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="92e48-126">Header</span><span class="sxs-lookup"><span data-stu-id="92e48-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="92e48-127"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="92e48-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92e48-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92e48-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92e48-129">Client Protokollierung</span><span class="sxs-lookup"><span data-stu-id="92e48-129">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="92e48-130">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="92e48-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="92e48-131">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="92e48-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




