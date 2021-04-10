---
description: Der Wert des Felds &\# 0034; CS (Referer) &\# 0034;, das die Netzwerkquelle für die Protokollierung verwendet.
ms.assetid: 328544b3-0d5f-4d1a-9ad1-ac38402d5898
title: MFNETSOURCE_BROWSERWEBPAGE-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e8222761299cad229b692ef400f69d0968ebd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959140"
---
# <a name="mfnetsource_browserwebpage-property"></a><span data-ttu-id="8eca0-103">Eigenschaft "browserwebseite" in MF NetSource \_</span><span class="sxs-lookup"><span data-stu-id="8eca0-103">MFNETSOURCE\_BROWSERWEBPAGE property</span></span>

<span data-ttu-id="8eca0-104">Der Wert des Felds "CS (Referer)", das die Netzwerkquelle für die Protokollierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="8eca0-104">The value of the "cs(Referer)" field that the network source uses for logging.</span></span> <span data-ttu-id="8eca0-105">Anwendungen können diese Eigenschaft auf die URL der Webseite festlegen, in der die Anwendung eingebettet wurde.</span><span class="sxs-lookup"><span data-stu-id="8eca0-105">Applications can set this property to the URL of the webpage in which the application was embedded.</span></span>



<span data-ttu-id="8eca0-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8eca0-106">Data type</span></span>

<span data-ttu-id="8eca0-107">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="8eca0-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="8eca0-108">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="8eca0-108">PROPVARIANT member</span></span>

<span data-ttu-id="8eca0-109">Breit Zeichen-Zeichenfolge (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="8eca0-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="8eca0-110">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="8eca0-110">VT\_LPWSTR</span></span>

<span data-ttu-id="8eca0-111">**pwszval**</span><span class="sxs-lookup"><span data-stu-id="8eca0-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="8eca0-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8eca0-112">Remarks</span></span>

<span data-ttu-id="8eca0-113">Die Konstante " **MF NetSource \_ browserwebseite** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="8eca0-113">The constant **MFNETSOURCE\_BROWSERWEBPAGE** defines the GUID for this property key.</span></span> <span data-ttu-id="8eca0-114">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="8eca0-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="8eca0-115">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8eca0-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="8eca0-116">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="8eca0-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="8eca0-117">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="8eca0-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8eca0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8eca0-118">Requirements</span></span>



| <span data-ttu-id="8eca0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8eca0-119">Requirement</span></span> | <span data-ttu-id="8eca0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8eca0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8eca0-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8eca0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8eca0-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8eca0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8eca0-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8eca0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8eca0-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8eca0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8eca0-125">Header</span><span class="sxs-lookup"><span data-stu-id="8eca0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eca0-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eca0-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eca0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8eca0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eca0-128">Client Protokollierung</span><span class="sxs-lookup"><span data-stu-id="8eca0-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="8eca0-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8eca0-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="8eca0-130">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8eca0-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




