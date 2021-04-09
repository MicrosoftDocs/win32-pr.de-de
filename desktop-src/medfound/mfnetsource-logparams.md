---
description: Array von Zeichen folgen mit den Parametern, die an den Protokollserver gesendet werden sollen.
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: MFNETSOURCE_LOGPARAMS-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec30f3f4d85f44905288601ba73ee6c246d8a9db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959284"
---
# <a name="mfnetsource_logparams-property"></a><span data-ttu-id="4a804-103">Eigenschaft "MF NetSource \_ logparameams"</span><span class="sxs-lookup"><span data-stu-id="4a804-103">MFNETSOURCE\_LOGPARAMS property</span></span>

<span data-ttu-id="4a804-104">Array von Zeichen folgen mit den Parametern, die an den Protokollserver gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4a804-104">Array of strings with the parameters to send to the log server.</span></span>



<span data-ttu-id="4a804-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4a804-105">Data type</span></span>

<span data-ttu-id="4a804-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="4a804-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="4a804-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="4a804-107">PROPVARIANT member</span></span>

<span data-ttu-id="4a804-108">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="4a804-108">\**WCHAR\** _</span></span>

<span data-ttu-id="4a804-109">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="4a804-109">VT\_LPWSTR</span></span>

<span data-ttu-id="4a804-110">_ *pwszval*\*</span><span class="sxs-lookup"><span data-stu-id="4a804-110">_ *pwszVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="4a804-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a804-111">Remarks</span></span>

<span data-ttu-id="4a804-112">Die **MF NetSource \_ LogParser** -Konstante definiert die GUID für den Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="4a804-112">The **MFNETSOURCE\_LOGPARAMS** constant defines the GUID for the property key.</span></span> <span data-ttu-id="4a804-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="4a804-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="4a804-114">Um diese Eigenschaft für die Netzwerkquelle festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="4a804-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="4a804-115">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="4a804-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a804-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a804-116">Requirements</span></span>



| <span data-ttu-id="4a804-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a804-117">Requirement</span></span> | <span data-ttu-id="4a804-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4a804-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a804-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a804-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4a804-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a804-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4a804-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a804-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4a804-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a804-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4a804-123">Header</span><span class="sxs-lookup"><span data-stu-id="4a804-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a804-124"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a804-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a804-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a804-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a804-126">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4a804-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="4a804-127">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4a804-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




