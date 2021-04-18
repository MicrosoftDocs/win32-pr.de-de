---
description: Gibt die Bandbreite der Verbindung für die Netzwerkquelle in Bits pro Sekunde an.
ms.assetid: 1b71dce1-8744-4114-9629-2a9d0afb7c43
title: MFNETSOURCE_CONNECTIONBANDWIDTH-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b852b3eb8dbfe5d3abc85e2223e868c5be708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527383"
---
# <a name="mfnetsource_connectionbandwidth-property"></a><span data-ttu-id="d685f-103">MF NetSource \_ connectionbandwidth (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d685f-103">MFNETSOURCE\_CONNECTIONBANDWIDTH property</span></span>

<span data-ttu-id="d685f-104">Gibt die Bandbreite der Verbindung für die Netzwerkquelle in Bits pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="d685f-104">Specifies the link bandwidth for the network source, in bits per second.</span></span>



<span data-ttu-id="d685f-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d685f-105">Data type</span></span>

<span data-ttu-id="d685f-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="d685f-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d685f-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="d685f-107">PROPVARIANT member</span></span>

<span data-ttu-id="d685f-108">**DWORD** (als **Long** gespeichert)</span><span class="sxs-lookup"><span data-stu-id="d685f-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="d685f-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="d685f-109">VT\_I4</span></span>

<span data-ttu-id="d685f-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="d685f-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="d685f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d685f-111">Remarks</span></span>

<span data-ttu-id="d685f-112">Die Konstante " **MF NetSource \_ connectionbandwidth** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="d685f-112">The constant **MFNETSOURCE\_CONNECTIONBANDWIDTH** defines the GUID for this property key.</span></span> <span data-ttu-id="d685f-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d685f-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="d685f-114">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d685f-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="d685f-115">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="d685f-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="d685f-116">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="d685f-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d685f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d685f-117">Requirements</span></span>



| <span data-ttu-id="d685f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d685f-118">Requirement</span></span> | <span data-ttu-id="d685f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d685f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d685f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d685f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d685f-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d685f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d685f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d685f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d685f-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d685f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d685f-124">Header</span><span class="sxs-lookup"><span data-stu-id="d685f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d685f-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d685f-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d685f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d685f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d685f-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d685f-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d685f-128">Netzwerk Quell Features</span><span class="sxs-lookup"><span data-stu-id="d685f-128">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="d685f-129">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d685f-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




