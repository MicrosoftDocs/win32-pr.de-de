---
description: Der Wert des Felds &\# 0034; c-hostexe&\# 0034;, das die Netzwerkquelle für die Protokollierung verwendet.
ms.assetid: 82a49719-b9b3-4868-bbcf-9e376f35d4c4
title: MFNETSOURCE_HOSTEXE-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ac786fe08ede556537703d2eb886b30be39207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759073"
---
# <a name="mfnetsource_hostexe-property"></a><span data-ttu-id="de7a3-103">MF NetSource- \_ hostexe (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="de7a3-103">MFNETSOURCE\_HOSTEXE property</span></span>

<span data-ttu-id="de7a3-104">Der Wert des Felds "c-hostexe", das von der Netzwerkquelle für die Protokollierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="de7a3-104">The value of the "c-hostexe" field that the network source uses for logging.</span></span> <span data-ttu-id="de7a3-105">Anwendungen können diese Eigenschaft auf den Namen der Host Anwendung festlegen.</span><span class="sxs-lookup"><span data-stu-id="de7a3-105">Applications can set this property to the name of the host application.</span></span> <span data-ttu-id="de7a3-106">Der Wert könnte z. b. "iexplore.exe" lauten, wenn die Anwendung auf einer Webseite gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="de7a3-106">For example, the value could be "iexplore.exe" if the application is hosted in a webpage.</span></span>



<span data-ttu-id="de7a3-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="de7a3-107">Data type</span></span>

<span data-ttu-id="de7a3-108">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="de7a3-108">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="de7a3-109">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="de7a3-109">PROPVARIANT member</span></span>

<span data-ttu-id="de7a3-110">Breit Zeichen-Zeichenfolge (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="de7a3-110">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="de7a3-111">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="de7a3-111">VT\_LPWSTR</span></span>

<span data-ttu-id="de7a3-112">**pwszval**</span><span class="sxs-lookup"><span data-stu-id="de7a3-112">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="de7a3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de7a3-113">Remarks</span></span>

<span data-ttu-id="de7a3-114">Die Konstante **MF-Quell- \_ hostexe** definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="de7a3-114">The constant **MFNETSOURCE\_HOSTEXE** defines the GUID for this property key.</span></span> <span data-ttu-id="de7a3-115">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="de7a3-115">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="de7a3-116">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="de7a3-116">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="de7a3-117">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="de7a3-117">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="de7a3-118">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="de7a3-118">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de7a3-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de7a3-119">Requirements</span></span>



| <span data-ttu-id="de7a3-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de7a3-120">Requirement</span></span> | <span data-ttu-id="de7a3-121">Wert</span><span class="sxs-lookup"><span data-stu-id="de7a3-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="de7a3-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de7a3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="de7a3-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de7a3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="de7a3-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de7a3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="de7a3-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de7a3-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="de7a3-126">Header</span><span class="sxs-lookup"><span data-stu-id="de7a3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="de7a3-127"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="de7a3-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de7a3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de7a3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de7a3-129">Client Protokollierung</span><span class="sxs-lookup"><span data-stu-id="de7a3-129">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="de7a3-130">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="de7a3-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="de7a3-131">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="de7a3-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




