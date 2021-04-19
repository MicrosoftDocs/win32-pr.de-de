---
description: Aktiviert den privaten Download Modus in der Netzwerkquelle.
ms.assetid: 679661A7-1D31-43F3-A64E-16ADCB5414B0
title: MFNETSOURCE_ENABLE_PRIVATEMODE-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53aa0bde3bf76ded278e0e3ee37465adb717972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348232"
---
# <a name="mfnetsource_enable_privatemode-property"></a><span data-ttu-id="1aed6-103">MF NetSource \_ - \_ Eigenschaft ' privatemode ' aktivieren</span><span class="sxs-lookup"><span data-stu-id="1aed6-103">MFNETSOURCE\_ENABLE\_PRIVATEMODE property</span></span>

<span data-ttu-id="1aed6-104">Aktiviert den privaten Download Modus in der Netzwerkquelle.</span><span class="sxs-lookup"><span data-stu-id="1aed6-104">Enables private download mode in the network source.</span></span>



<span data-ttu-id="1aed6-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1aed6-105">Data type</span></span>

<span data-ttu-id="1aed6-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="1aed6-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="1aed6-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="1aed6-107">PROPVARIANT member</span></span>

<span data-ttu-id="1aed6-108">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="1aed6-108">**BOOL**</span></span>

<span data-ttu-id="1aed6-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1aed6-109">VT\_I4</span></span>

<span data-ttu-id="1aed6-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="1aed6-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="1aed6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1aed6-111">Remarks</span></span>

<span data-ttu-id="1aed6-112">Wenn diese Eigenschaft den Wert **true** hat, wird der Cache gelöscht, wenn die Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="1aed6-112">If this property is **TRUE**, the cache is cleared when the session ends.</span></span>

<span data-ttu-id="1aed6-113">Die **MF NetSource- \_ clientguid** -Konstante definiert die GUID für den Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="1aed6-113">The **MFNETSOURCE\_CLIENTGUID** constant defines the GUID for the property key.</span></span> <span data-ttu-id="1aed6-114">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1aed6-114">The property identifier (PID) is zero.</span></span> <span data-ttu-id="1aed6-115">Um diese Eigenschaft für die Netzwerkquelle festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="1aed6-115">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="1aed6-116">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="1aed6-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1aed6-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1aed6-117">Requirements</span></span>



| <span data-ttu-id="1aed6-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1aed6-118">Requirement</span></span> | <span data-ttu-id="1aed6-119">Wert</span><span class="sxs-lookup"><span data-stu-id="1aed6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1aed6-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1aed6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1aed6-121">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1aed6-121">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1aed6-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1aed6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1aed6-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1aed6-123">None supported</span></span><br/>                                                          |
| <span data-ttu-id="1aed6-124">Header</span><span class="sxs-lookup"><span data-stu-id="1aed6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1aed6-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1aed6-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aed6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1aed6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aed6-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1aed6-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="1aed6-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1aed6-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




