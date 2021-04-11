---
description: Der Wert des Felds &\# 0034; c-playerid&\# 0034;, das die Netzwerkquelle für die Protokollierung verwendet.
ms.assetid: de52cc34-9b88-41ae-b8b8-ef5dff85892c
title: MFNETSOURCE_PLAYERID-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d20754c93057ef3f000fc9c7201cda7ec287eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042640"
---
# <a name="mfnetsource_playerid-property"></a><span data-ttu-id="00dc3-103">\_Playerid-Eigenschaft von MF NetSource</span><span class="sxs-lookup"><span data-stu-id="00dc3-103">MFNETSOURCE\_PLAYERID property</span></span>

<span data-ttu-id="00dc3-104">Der Wert des Felds "c-playerid", das von der Netzwerkquelle für die Protokollierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00dc3-104">The value of the "c-playerid" field that the network source uses for logging.</span></span> <span data-ttu-id="00dc3-105">Anwendungen können diese Eigenschaft auf einen beliebigen Zeichen folgen Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="00dc3-105">Applications can set this property to any string value.</span></span>



<span data-ttu-id="00dc3-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="00dc3-106">Data type</span></span>

<span data-ttu-id="00dc3-107">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="00dc3-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="00dc3-108">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="00dc3-108">PROPVARIANT member</span></span>

<span data-ttu-id="00dc3-109">Breit Zeichen-Zeichenfolge (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="00dc3-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="00dc3-110">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="00dc3-110">VT\_LPWSTR</span></span>

<span data-ttu-id="00dc3-111">**pwszval**</span><span class="sxs-lookup"><span data-stu-id="00dc3-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="00dc3-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00dc3-112">Remarks</span></span>

<span data-ttu-id="00dc3-113">Die Konstante " **MF NetSource \_ playerid** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="00dc3-113">The constant **MFNETSOURCE\_PLAYERID** defines the GUID for this property key.</span></span> <span data-ttu-id="00dc3-114">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="00dc3-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="00dc3-115">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="00dc3-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="00dc3-116">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="00dc3-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="00dc3-117">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="00dc3-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00dc3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00dc3-118">Requirements</span></span>



| <span data-ttu-id="00dc3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00dc3-119">Requirement</span></span> | <span data-ttu-id="00dc3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="00dc3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00dc3-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00dc3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="00dc3-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00dc3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="00dc3-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00dc3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="00dc3-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00dc3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="00dc3-125">Header</span><span class="sxs-lookup"><span data-stu-id="00dc3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="00dc3-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="00dc3-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00dc3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00dc3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00dc3-128">Client Protokollierung</span><span class="sxs-lookup"><span data-stu-id="00dc3-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="00dc3-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="00dc3-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="00dc3-130">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="00dc3-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




