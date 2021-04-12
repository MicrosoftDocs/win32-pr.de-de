---
description: Eindeutiger Bezeichner, durch den der Server den Client identifiziert.
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: MFNETSOURCE_CLIENTGUID-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5df46741d4a0b9a6a125396b6f93dd32bfadf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130117"
---
# <a name="mfnetsource_clientguid-property"></a><span data-ttu-id="83385-103">MF NetSource- \_ clientguid (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="83385-103">MFNETSOURCE\_CLIENTGUID property</span></span>

<span data-ttu-id="83385-104">Eindeutiger Bezeichner, durch den der Server den Client identifiziert.</span><span class="sxs-lookup"><span data-stu-id="83385-104">Unique identifier by which the server identifies the client.</span></span>



<span data-ttu-id="83385-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="83385-105">Data type</span></span>

<span data-ttu-id="83385-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="83385-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="83385-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="83385-107">PROPVARIANT member</span></span>

<span data-ttu-id="83385-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="83385-108">**GUID**</span></span>

<span data-ttu-id="83385-109">VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="83385-109">VT\_CLSID</span></span>

<span data-ttu-id="83385-110">**puuid**</span><span class="sxs-lookup"><span data-stu-id="83385-110">**puuid**</span></span>



## <a name="remarks"></a><span data-ttu-id="83385-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83385-111">Remarks</span></span>

<span data-ttu-id="83385-112">Die **MF NetSource- \_ clientguid** -Konstante definiert die GUID für den Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="83385-112">The **MFNETSOURCE\_CLIENTGUID** constant defines the GUID for the property key.</span></span> <span data-ttu-id="83385-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="83385-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="83385-114">Um diese Eigenschaft für die Netzwerkquelle festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="83385-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="83385-115">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="83385-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="83385-116">Wenn Sie nicht als **GUID \_ null** festgelegt oder festgelegt ist, generiert Microsoft Media Foundation eine anonyme GUID pro Sitzung, die den Datenschutz für den Benutzer sicherstellt.</span><span class="sxs-lookup"><span data-stu-id="83385-116">If not set or set as **GUID\_NULL**, Microsoft Media Foundation generates an anonymous GUID per session that ensures the user's privacy.</span></span>

## <a name="requirements"></a><span data-ttu-id="83385-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83385-117">Requirements</span></span>



| <span data-ttu-id="83385-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83385-118">Requirement</span></span> | <span data-ttu-id="83385-119">Wert</span><span class="sxs-lookup"><span data-stu-id="83385-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="83385-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="83385-120">Minimum supported client</span></span><br/> | <span data-ttu-id="83385-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="83385-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="83385-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="83385-122">Minimum supported server</span></span><br/> | <span data-ttu-id="83385-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="83385-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="83385-124">Header</span><span class="sxs-lookup"><span data-stu-id="83385-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="83385-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="83385-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83385-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83385-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83385-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="83385-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="83385-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="83385-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




