---
description: Speichert den Hostnamen und den Port des Proxy Servers, der von der Netzwerkquelle verwendet wird.
ms.assetid: 164f8ac3-08ce-40a8-ac8d-4c2a267d9db5
title: MFNETSOURCE_PROXYINFO-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f73ceedf71e567e026c5e9af67a67c5d84bebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360638"
---
# <a name="mfnetsource_proxyinfo-property"></a><span data-ttu-id="d5f91-103">Eigenschaft "MF NetSource \_ proxyinfo"</span><span class="sxs-lookup"><span data-stu-id="d5f91-103">MFNETSOURCE\_PROXYINFO property</span></span>

<span data-ttu-id="d5f91-104">Speichert den Hostnamen und den Port des Proxy Servers, der von der Netzwerkquelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d5f91-104">Stores the host name and the port of the proxy server used by the network source.</span></span>



<span data-ttu-id="d5f91-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d5f91-105">Data type</span></span>

<span data-ttu-id="d5f91-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="d5f91-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d5f91-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="d5f91-107">PROPVARIANT member</span></span>

<span data-ttu-id="d5f91-108">Breit Zeichen-Zeichenfolge (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="d5f91-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="d5f91-109">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="d5f91-109">VT\_LPWSTR</span></span>

<span data-ttu-id="d5f91-110">**pwszval**</span><span class="sxs-lookup"><span data-stu-id="d5f91-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="d5f91-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5f91-111">Remarks</span></span>

<span data-ttu-id="d5f91-112">Die Konstante **MF-Quelle \_ proxyinfo** definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="d5f91-112">The constant **MFNETSOURCE\_PROXYINFO** defines the GUID for this property key.</span></span> <span data-ttu-id="d5f91-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d5f91-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="d5f91-114">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d5f91-114">This property is read-only.</span></span> <span data-ttu-id="d5f91-115">Um den Eigenschafts Wert aus der Netzwerkquelle abzurufen, nennen Sie **IPropertyStore:: GetValue** , und übergeben Sie die **PropertyKey** -Struktur im *Key* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="d5f91-115">To get the property value from the network source, call **IPropertyStore::GetValue** and pass the **PROPERTYKEY** structure in the *key* parameter.</span></span> <span data-ttu-id="d5f91-116">Der **fmtid** -Member von **PropertyKey** muss auf die GUID der Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d5f91-116">The **fmtid** member of **PROPERTYKEY** must be set to the property GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5f91-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5f91-117">Requirements</span></span>



| <span data-ttu-id="d5f91-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5f91-118">Requirement</span></span> | <span data-ttu-id="d5f91-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d5f91-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f91-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5f91-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f91-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5f91-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d5f91-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5f91-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f91-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5f91-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d5f91-124">Header</span><span class="sxs-lookup"><span data-stu-id="d5f91-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5f91-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5f91-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5f91-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5f91-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f91-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5f91-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d5f91-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5f91-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="d5f91-129">Proxy Unterstützung für Netzwerk Quellen</span><span class="sxs-lookup"><span data-stu-id="d5f91-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




