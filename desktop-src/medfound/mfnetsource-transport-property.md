---
description: Gibt das Transportprotokoll an, das von der Netzwerkquelle verwendet wird.
ms.assetid: 7c8598ff-f408-42d0-9eee-3ef1e82f0466
title: MFNETSOURCE_TRANSPORT-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd41653f2b5ea0686527af4d6ee8c8b9962005aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863156"
---
# <a name="mfnetsource_transport-property"></a><span data-ttu-id="79678-103">MF-Quell- \_ Transport Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="79678-103">MFNETSOURCE\_TRANSPORT property</span></span>

<span data-ttu-id="79678-104">Gibt das Transportprotokoll an, das von der Netzwerkquelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="79678-104">Specifies the transport protocol used by the network source.</span></span> <span data-ttu-id="79678-105">Der Wert dieser Eigenschaft ist ein Member der [**mfnetsource- \_ \_ Transporttyp**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="79678-105">The value of this property is a member of the [**MFNETSOURCE\_TRANSPORT\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) enumeration.</span></span>



<span data-ttu-id="79678-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="79678-106">Data type</span></span>

<span data-ttu-id="79678-107">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="79678-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="79678-108">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="79678-108">PROPVARIANT member</span></span>

<span data-ttu-id="79678-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="79678-109">**LONG**</span></span>

<span data-ttu-id="79678-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="79678-110">VT\_I4</span></span>

<span data-ttu-id="79678-111">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="79678-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="79678-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79678-112">Remarks</span></span>

<span data-ttu-id="79678-113">Der Konstante **MF-Quell \_ Transport** definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="79678-113">The constant **MFNETSOURCE\_TRANSPORT** defines the GUID for this property key.</span></span> <span data-ttu-id="79678-114">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="79678-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="79678-115">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="79678-115">This property is read-only.</span></span> <span data-ttu-id="79678-116">Um diese Eigenschaft abzurufen, Fragen Sie die Netzwerkquelle nach der **IPropertyStore** -Schnittstelle ab, und rufen Sie **IPropertyStore:: GetValue** auf.</span><span class="sxs-lookup"><span data-stu-id="79678-116">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="79678-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79678-117">Requirements</span></span>



| <span data-ttu-id="79678-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79678-118">Requirement</span></span> | <span data-ttu-id="79678-119">Wert</span><span class="sxs-lookup"><span data-stu-id="79678-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="79678-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79678-120">Minimum supported client</span></span><br/> | <span data-ttu-id="79678-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79678-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="79678-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79678-122">Minimum supported server</span></span><br/> | <span data-ttu-id="79678-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79678-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="79678-124">Header</span><span class="sxs-lookup"><span data-stu-id="79678-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="79678-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="79678-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79678-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79678-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79678-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="79678-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="79678-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="79678-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="79678-129">Unterstützte Protokolle</span><span class="sxs-lookup"><span data-stu-id="79678-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




