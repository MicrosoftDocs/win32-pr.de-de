---
description: Aktiviert oder deaktiviert den Read-Ahead-Vorgang in einer Medienquelle.
ms.assetid: b2b8711f-ba63-4fba-bb88-8d254135eb21
title: MFPKEY_MediaSource_DisableReadAhead-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d06fe354431a24e15152268ba0ea6352e535c5e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359377"
---
# <a name="mfpkey_mediasource_disablereadahead-property"></a><span data-ttu-id="79e71-103">Eigenschaft "mfpkey \_ MediaSource \_ disablereadahead"</span><span class="sxs-lookup"><span data-stu-id="79e71-103">MFPKEY\_MediaSource\_DisableReadAhead property</span></span>

<span data-ttu-id="79e71-104">Aktiviert oder deaktiviert den Read-Ahead-Vorgang in einer Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="79e71-104">Enables or disables read-ahead in a media source.</span></span>



<span data-ttu-id="79e71-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="79e71-105">Data type</span></span>

<span data-ttu-id="79e71-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="79e71-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="79e71-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="79e71-107">PROPVARIANT member</span></span>

<span data-ttu-id="79e71-108">**Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="79e71-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="79e71-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="79e71-109">VT\_BOOL</span></span>

<span data-ttu-id="79e71-110">**Boolesche Werte**</span><span class="sxs-lookup"><span data-stu-id="79e71-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="79e71-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79e71-111">Remarks</span></span>

<span data-ttu-id="79e71-112">Anwendungen können diese Eigenschaft verwenden, um einige Medienquellen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="79e71-112">Applications can use this property to configure some media sources.</span></span> <span data-ttu-id="79e71-113">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="79e71-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="79e71-114">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="79e71-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="79e71-115">Wenn der Wert **Variant \_ true** ist, wird die Medienquelle nicht im Bytestream eingelesen.</span><span class="sxs-lookup"><span data-stu-id="79e71-115">If the value is **VARIANT\_TRUE**, the media source will not read ahead in the byte stream.</span></span> <span data-ttu-id="79e71-116">Diese Einstellung kann die Leistung optimieren, wenn Sie eine begrenzte Menge von Daten aus der Medienquelle lesen möchten, z. –. um ein Miniaturbild aus einer Videodatei zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="79e71-116">This setting can optimize performance if you plan to read a limited amount of data from the media source—for example, to get a thumbnail image from a video file.</span></span>

<span data-ttu-id="79e71-117">Für eine typische Audiowiedergabe und Videowiedergabe sollte diese Eigenschaft auf **Variant \_ false** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="79e71-117">For typical audio/video playback, this property should be set to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="79e71-118">Der Standardwert ist **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="79e71-118">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="79e71-119">Nicht jede Medienquelle unterstützt diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="79e71-119">Not every media source supports this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="79e71-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79e71-120">Requirements</span></span>



| <span data-ttu-id="79e71-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79e71-121">Requirement</span></span> | <span data-ttu-id="79e71-122">Wert</span><span class="sxs-lookup"><span data-stu-id="79e71-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="79e71-123">Client</span><span class="sxs-lookup"><span data-stu-id="79e71-123">Client</span></span><br/> | <span data-ttu-id="79e71-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="79e71-124">Windows 7</span></span><br/>                                                               |
| <span data-ttu-id="79e71-125">Header</span><span class="sxs-lookup"><span data-stu-id="79e71-125">Header</span></span><br/> | <dl> <span data-ttu-id="79e71-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="79e71-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79e71-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79e71-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e71-128">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="79e71-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




