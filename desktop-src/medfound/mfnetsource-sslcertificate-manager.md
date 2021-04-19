---
description: Speichert den IUnknown-Zeiger der Klasse, die die IMF-Klasse "imssslcertifitoremanager" implementiert.
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: MFNETSOURCE_SSLCERTIFICATE_MANAGER-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf6e21962e3d521e8c5781d59b2e0fe6fed04aa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346659"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a><span data-ttu-id="edfb1-103">MF-Quelle \_ sslcertificate \_ Manager (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="edfb1-103">MFNETSOURCE\_SSLCERTIFICATE\_MANAGER property</span></span>

<span data-ttu-id="edfb1-104">Speichert den **IUnknown** -Zeiger der Klasse, die die [**IMF-Klasse "imssslcertifitoremanager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) " implementiert.</span><span class="sxs-lookup"><span data-stu-id="edfb1-104">Stores the **IUnknown** pointer of the class that implements the [**IMFSSLCertificateManager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) interface.</span></span> <span data-ttu-id="edfb1-105">Die Client Implementierung stellt Methoden bereit, um das Client-SSL-Zertifikat zu erhalten, wenn es vom Server angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="edfb1-105">The client implemention provides methods to get the client SSL certificate when it is requested by the server.</span></span>



<span data-ttu-id="edfb1-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="edfb1-106">Data type</span></span>

<span data-ttu-id="edfb1-107">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="edfb1-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="edfb1-108">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="edfb1-108">PROPVARIANT member</span></span>

<span data-ttu-id="edfb1-109">**IUnknown-Zeiger**</span><span class="sxs-lookup"><span data-stu-id="edfb1-109">**IUnknown pointer**</span></span>

<span data-ttu-id="edfb1-110">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="edfb1-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="edfb1-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="edfb1-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="edfb1-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="edfb1-112">Remarks</span></span>

<span data-ttu-id="edfb1-113">Die **MF-Quelle \_ sslcertificate \_ Manager** -Konstante definiert die GUID für den Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="edfb1-113">The **MFNETSOURCE\_SSLCERTIFICATE\_MANAGER** constant defines the GUID for the property key.</span></span> <span data-ttu-id="edfb1-114">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="edfb1-114">The property identifier (PID) is zero.</span></span> <span data-ttu-id="edfb1-115">Um diese Eigenschaft für die Netzwerkquelle festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="edfb1-115">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="edfb1-116">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="edfb1-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="edfb1-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="edfb1-117">Requirements</span></span>



| <span data-ttu-id="edfb1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="edfb1-118">Requirement</span></span> | <span data-ttu-id="edfb1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="edfb1-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="edfb1-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="edfb1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="edfb1-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="edfb1-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="edfb1-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="edfb1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="edfb1-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="edfb1-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="edfb1-124">Header</span><span class="sxs-lookup"><span data-stu-id="edfb1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="edfb1-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="edfb1-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edfb1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edfb1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edfb1-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="edfb1-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="edfb1-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="edfb1-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




