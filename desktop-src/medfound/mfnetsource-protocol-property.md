---
description: Gibt das Steuerungs Protokoll an, das von der Netzwerkquelle verwendet wird.
ms.assetid: 4de8b8ba-97d9-4269-a16c-1853dc02f674
title: MFNETSOURCE_PROTOCOL-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b188eeb1f6669544291f4dca95db8a4a45a50d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525979"
---
# <a name="mfnetsource_protocol-property"></a><span data-ttu-id="3d847-103">MF-Quell \_ Protokoll Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3d847-103">MFNETSOURCE\_PROTOCOL property</span></span>

<span data-ttu-id="3d847-104">Gibt das Steuerungs Protokoll an, das von der Netzwerkquelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3d847-104">Specifies the control protocol used by the network source.</span></span> <span data-ttu-id="3d847-105">Der Wert dieser Eigenschaft ist ein Member der Enumeration des [**mfnetsource- \_ Protokoll \_ Typs**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .</span><span class="sxs-lookup"><span data-stu-id="3d847-105">The value of this property is a member of the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span>



<span data-ttu-id="3d847-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3d847-106">Data type</span></span>

<span data-ttu-id="3d847-107">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="3d847-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="3d847-108">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="3d847-108">PROPVARIANT member</span></span>

<span data-ttu-id="3d847-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="3d847-109">**LONG**</span></span>

<span data-ttu-id="3d847-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="3d847-110">VT\_I4</span></span>

<span data-ttu-id="3d847-111">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="3d847-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="3d847-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d847-112">Remarks</span></span>

<span data-ttu-id="3d847-113">Das Konstante **MF-Quell \_ Protokoll** definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="3d847-113">The constant **MFNETSOURCE\_PROTOCOL** defines the GUID for this property key.</span></span> <span data-ttu-id="3d847-114">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="3d847-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="3d847-115">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3d847-115">This property is read-only.</span></span> <span data-ttu-id="3d847-116">Um diese Eigenschaft abzurufen, Fragen Sie die Netzwerkquelle nach der **IPropertyStore** -Schnittstelle ab, und rufen Sie **IPropertyStore:: GetValue** auf.</span><span class="sxs-lookup"><span data-stu-id="3d847-116">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d847-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d847-117">Requirements</span></span>



| <span data-ttu-id="3d847-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d847-118">Requirement</span></span> | <span data-ttu-id="3d847-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3d847-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d847-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d847-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3d847-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d847-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3d847-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d847-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3d847-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d847-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3d847-124">Header</span><span class="sxs-lookup"><span data-stu-id="3d847-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d847-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d847-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d847-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d847-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d847-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3d847-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="3d847-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3d847-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="3d847-129">Unterstützte Protokolle</span><span class="sxs-lookup"><span data-stu-id="3d847-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




