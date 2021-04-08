---
description: Konfiguriert die ASF-Medienquelle für die Verwendung von iterativer Suche, wenn die Quelldatei über keinen Index verfügt.
ms.assetid: 0dd6f202-cdbc-4a28-8907-5530a0a2141b
title: MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cdc22f0b4f5490c7691cc40166cf929a16ba64
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761448"
---
# <a name="mfpkey_asfmediasource_iterativeseekifnoindex-property"></a><span data-ttu-id="562de-103">Mfpkey \_ asfmediasource \_ iterativeseekifnoindex (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="562de-103">MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex property</span></span>

<span data-ttu-id="562de-104">Konfiguriert die ASF-Medienquelle für die Verwendung von iterativer Suche, wenn die Quelldatei über keinen Index verfügt.</span><span class="sxs-lookup"><span data-stu-id="562de-104">Configures the ASF media source to use iterative seeking if the source file has no index.</span></span>



<span data-ttu-id="562de-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="562de-105">Data type</span></span>

<span data-ttu-id="562de-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="562de-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="562de-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="562de-107">PROPVARIANT member</span></span>

<span data-ttu-id="562de-108">**Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="562de-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="562de-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="562de-109">VT\_BOOL</span></span>

<span data-ttu-id="562de-110">**Boolesche Werte**</span><span class="sxs-lookup"><span data-stu-id="562de-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="562de-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="562de-111">Remarks</span></span>

<span data-ttu-id="562de-112">Verwenden Sie diese Eigenschaft, um die ASF-Medienquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="562de-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="562de-113">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den *quellresolver*.</span><span class="sxs-lookup"><span data-stu-id="562de-113">To set the property, pass an **IPropertyStore** pointer to the *source resolver*.</span></span> <span data-ttu-id="562de-114">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="562de-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="562de-115">*Iteratives suchen* ist ein Algorithmus, mit dem eine Position in einer ASF-Datei ohne Index gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="562de-115">*Iterative seeking* is an algorithm to find a position in an ASF file with no index.</span></span> <span data-ttu-id="562de-116">Es verwendet eine Reihe von Näherungen, die auf der durchschnittlichen Bitrate basieren, um die Ziel Suchzeit progressiv näher zu bringen.</span><span class="sxs-lookup"><span data-stu-id="562de-116">It uses a series of approximations, based on the average bit rate, to get progressively closer to the target seek time.</span></span> <span data-ttu-id="562de-117">(Der Algorithmus ähnelt einer binären Suche.) Das iterative suchen kann länger dauern als die Suche nach Index, daher ist es standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="562de-117">(The algorithm is similar to a binary search.) Iterative seeking can take longer than seeking by index, so it is disabled by default.</span></span>

<span data-ttu-id="562de-118">Wenn Sie diese Eigenschaft festlegen, verwenden Sie die folgenden Eigenschaften, um die Suchparameter festzulegen:</span><span class="sxs-lookup"><span data-stu-id="562de-118">If you set this property, use the following properties to set the search parameters:</span></span>

-   [<span data-ttu-id="562de-119">Mfpkey \_ asfmediasource \_ iterativeseek \_ Maximale \_ Anzahl</span><span class="sxs-lookup"><span data-stu-id="562de-119">MFPKEY\_ASFMediaSource\_IterativeSeek\_Max\_Count</span></span>](mfpkey-asfmediasource-iterativeseek-max-count.md)
-   [<span data-ttu-id="562de-120">Mfpkey \_ asfmediasource \_ iterativeseek \_ Tolerance \_ in \_ Millisekunde</span><span class="sxs-lookup"><span data-stu-id="562de-120">MFPKEY\_ASFMediaSource\_IterativeSeek\_Tolerance\_In\_MilliSecond</span></span>](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md)

<span data-ttu-id="562de-121">Diese Eigenschaften legen die maximale Anzahl von Iterationen bzw. die Toleranz fest.</span><span class="sxs-lookup"><span data-stu-id="562de-121">These properties set the maximum number of iterations and the tolerance, respectively.</span></span> <span data-ttu-id="562de-122">Der Algorithmus wird angehalten, wenn die maximale Anzahl von Iterationen erreicht wird, oder wenn ein Paket gefunden wird, dessen Entfernung von der Suchzeit innerhalb der angegebenen Toleranz liegt.</span><span class="sxs-lookup"><span data-stu-id="562de-122">The algorithm halts when it reaches the maximum number of iterations, or when it finds a packet whose distance from the seek time is within the specified tolerance.</span></span>

## <a name="requirements"></a><span data-ttu-id="562de-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="562de-123">Requirements</span></span>



| <span data-ttu-id="562de-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="562de-124">Requirement</span></span> | <span data-ttu-id="562de-125">Wert</span><span class="sxs-lookup"><span data-stu-id="562de-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="562de-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="562de-126">Minimum supported client</span></span><br/> | <span data-ttu-id="562de-127">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="562de-127">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="562de-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="562de-128">Minimum supported server</span></span><br/> | <span data-ttu-id="562de-129">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="562de-129">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="562de-130">Header</span><span class="sxs-lookup"><span data-stu-id="562de-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="562de-131"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="562de-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="562de-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="562de-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="562de-133">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="562de-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




