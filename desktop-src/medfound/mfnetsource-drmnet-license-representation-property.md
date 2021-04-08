---
description: Speichert ein Bytearray, das die dem Bytestream zugeordnete DRM-Lizenz darstellt.
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92af9a17779381aaed2d2226e17023ca40bc9c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753128"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a><span data-ttu-id="aac86-103">MF-Quelle \_ drmnet- \_ Lizenz \_ Darstellung (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="aac86-103">MFNETSOURCE\_DRMNET\_LICENSE\_REPRESENTATION property</span></span>

<span data-ttu-id="aac86-104">Speichert ein Bytearray, das die dem Bytestream zugeordnete DRM-Lizenz darstellt.</span><span class="sxs-lookup"><span data-stu-id="aac86-104">Stores an array of bytes that represents the DRM license associated with the byte stream.</span></span>



<span data-ttu-id="aac86-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="aac86-105">Data type</span></span>

<span data-ttu-id="aac86-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="aac86-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="aac86-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="aac86-107">PROPVARIANT member</span></span>

<span data-ttu-id="aac86-108">Bytearray (**BLOB**)</span><span class="sxs-lookup"><span data-stu-id="aac86-108">Byte array (**BLOB**)</span></span>

<span data-ttu-id="aac86-109">VT- \_ BLOB</span><span class="sxs-lookup"><span data-stu-id="aac86-109">VT\_BLOB</span></span>

<span data-ttu-id="aac86-110">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="aac86-110">**blob**</span></span>



## <a name="remarks"></a><span data-ttu-id="aac86-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aac86-111">Remarks</span></span>

<span data-ttu-id="aac86-112">Die Konstante **MF-Quell- \_ drmnet- \_ Lizenz \_ Darstellung** definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="aac86-112">The constant **MFNETSOURCE\_DRMNET\_LICENSE\_REPRESENTATION** defines the GUID for this property key.</span></span> <span data-ttu-id="aac86-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="aac86-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="aac86-114">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="aac86-114">This property is read-only.</span></span> <span data-ttu-id="aac86-115">Um den Eigenschafts Wert aus dem netzwerkbytestream abzurufen, nennen Sie **IPropertyStore:: GetValue** , und übergeben Sie die **PropertyKey** -Struktur im *Key* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="aac86-115">To get the property value from the network byte stream, call **IPropertyStore::GetValue** and pass the **PROPERTYKEY** structure in the *key* parameter.</span></span> <span data-ttu-id="aac86-116">Der **fmtid** -Member von **PropertyKey** muss auf die GUID der Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="aac86-116">The **fmtid** member of **PROPERTYKEY** must be set to the property GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="aac86-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aac86-117">Requirements</span></span>



| <span data-ttu-id="aac86-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aac86-118">Requirement</span></span> | <span data-ttu-id="aac86-119">Wert</span><span class="sxs-lookup"><span data-stu-id="aac86-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aac86-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aac86-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aac86-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aac86-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="aac86-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aac86-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aac86-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aac86-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="aac86-124">Header</span><span class="sxs-lookup"><span data-stu-id="aac86-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aac86-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aac86-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aac86-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aac86-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aac86-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aac86-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="aac86-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aac86-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




