---
description: Legt die Datenstrom Konfiguration für die WTV-Medienquelle fest.
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: MFPKEY_SBESourceMode-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82835a4cfc363e3ae2d054cce68f95c655447dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959412"
---
# <a name="mfpkey_sbesourcemode-property"></a><span data-ttu-id="11834-103">Mfpkey \_ sbesourcemode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="11834-103">MFPKEY\_SBESourceMode property</span></span>

<span data-ttu-id="11834-104">Legt die Datenstrom Konfiguration für die WTV-Medienquelle fest.</span><span class="sxs-lookup"><span data-stu-id="11834-104">Sets the stream configuration for the WTV media source.</span></span>



<span data-ttu-id="11834-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="11834-105">Data type</span></span>

<span data-ttu-id="11834-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="11834-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="11834-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="11834-107">PROPVARIANT member</span></span>

<span data-ttu-id="11834-108">**INT**</span><span class="sxs-lookup"><span data-stu-id="11834-108">**INT**</span></span>

<span data-ttu-id="11834-109">VT \_ int</span><span class="sxs-lookup"><span data-stu-id="11834-109">VT\_INT</span></span>

<span data-ttu-id="11834-110">**intval**</span><span class="sxs-lookup"><span data-stu-id="11834-110">**intVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="11834-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11834-111">Remarks</span></span>

<span data-ttu-id="11834-112">Verwenden Sie diese Eigenschaft, um die WTV-Medienquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="11834-112">Use this property to configure the WTV media source.</span></span> <span data-ttu-id="11834-113">Um die-Eigenschaft festzulegen, übergeben Sie einen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="11834-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="11834-114">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="11834-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="11834-115">Die WTV-Medienquelle liest in Windows aufgezeichnete TV Show-Dateien (WTV und MS-drv).</span><span class="sxs-lookup"><span data-stu-id="11834-115">The WTV media source reads Windows Recorded TV Show (.wtv and .ms-drv) files.</span></span>

<span data-ttu-id="11834-116">Diese Eigenschaft muss einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="11834-116">This property must have one of the following values.</span></span>

-   <span data-ttu-id="11834-117">1: Ordnen Sie verfügbare Audiodatenströme einer einzelnen Ausgabe zu, basierend auf dem lokalen System.</span><span class="sxs-lookup"><span data-stu-id="11834-117">1: Map available audio streams to a single output, based on the system local.</span></span> <span data-ttu-id="11834-118">Dieser Modus eignet sich für die Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="11834-118">This mode is appropriate for playback.</span></span> <span data-ttu-id="11834-119">(Standardeinstellung)</span><span class="sxs-lookup"><span data-stu-id="11834-119">(Default.)</span></span>
-   2. <span data-ttu-id="11834-120">Alle Audiostreams und unter Ströme (z. b. Beschriftung und Datenströme) werden ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="11834-120">All audio streams and substreams (such as caption and data streams) are selected.</span></span> <span data-ttu-id="11834-121">Dieser Modus eignet sich für die Umgestaltung oder die Transcodierung.</span><span class="sxs-lookup"><span data-stu-id="11834-121">This mode is appropriate for remuxing or transcoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="11834-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11834-122">Requirements</span></span>



| <span data-ttu-id="11834-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11834-123">Requirement</span></span> | <span data-ttu-id="11834-124">Wert</span><span class="sxs-lookup"><span data-stu-id="11834-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="11834-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11834-125">Minimum supported client</span></span><br/> | <span data-ttu-id="11834-126">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="11834-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="11834-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11834-127">Minimum supported server</span></span><br/> | <span data-ttu-id="11834-128">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="11834-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="11834-129">Header</span><span class="sxs-lookup"><span data-stu-id="11834-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="11834-130"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="11834-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11834-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11834-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11834-132">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="11834-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
