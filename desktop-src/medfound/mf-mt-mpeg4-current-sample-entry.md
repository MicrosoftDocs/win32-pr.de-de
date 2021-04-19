---
description: Gibt den aktuellen Eintrag im Feld für die Beispiel Beschreibung für einen MPEG-4-Medientyp an.
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c1f2a43eef1a520a49f5cfbb889f13149fa249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362608"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a><span data-ttu-id="e1ff3-103">"MF \_ MT \_ MPEG4 \_ Current \_ Sample Entry \_ "-Attribut</span><span class="sxs-lookup"><span data-stu-id="e1ff3-103">MF\_MT\_MPEG4\_CURRENT\_SAMPLE\_ENTRY attribute</span></span>

<span data-ttu-id="e1ff3-104">Gibt den aktuellen Eintrag im Feld für die Beispiel Beschreibung für einen MPEG-4-Medientyp an.</span><span class="sxs-lookup"><span data-stu-id="e1ff3-104">Specifies the current entry in the sample description box for an MPEG-4 media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="e1ff3-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e1ff3-105">Data type</span></span>

<span data-ttu-id="e1ff3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e1ff3-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e1ff3-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="e1ff3-107">Get/set</span></span>

<span data-ttu-id="e1ff3-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e1ff3-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e1ff3-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e1ff3-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e1ff3-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="e1ff3-110">Applies to</span></span>

[<span data-ttu-id="e1ff3-111">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="e1ff3-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="e1ff3-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1ff3-112">Remarks</span></span>

<span data-ttu-id="e1ff3-113">In einer MP4-oder 3GP-Datei beschreibt das Feld Beispiel Beschreibung die Codierung, die für einen Datenstrom in der Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e1ff3-113">In an MP4 or 3GP file, the sample description box describes the encoding used for a stream in the file.</span></span> <span data-ttu-id="e1ff3-114">Das Feld für die Beispiel Beschreibung kann mehrere Einträge enthalten.</span><span class="sxs-lookup"><span data-stu-id="e1ff3-114">The sample description box can contain multiple entries.</span></span> <span data-ttu-id="e1ff3-115">Dieses Attribut gibt an, welcher Eintrag verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1ff3-115">This attribute specifies which entry to use.</span></span> <span data-ttu-id="e1ff3-116">Der Wert ist ein NULL basierter Index in der Liste.</span><span class="sxs-lookup"><span data-stu-id="e1ff3-116">The value is a zero-based index into the list.</span></span>

<span data-ttu-id="e1ff3-117">Derzeit ist der einzige unterstützte Wert 0.</span><span class="sxs-lookup"><span data-stu-id="e1ff3-117">Currently, the only supported value is 0.</span></span> <span data-ttu-id="e1ff3-118">Das-Attribut wurde für die spätere Erweiterbarkeit definiert.</span><span class="sxs-lookup"><span data-stu-id="e1ff3-118">The attribute has been defined for future extensibility.</span></span>

<span data-ttu-id="e1ff3-119">Die MPEG-4-Datei Quelle legt den Wert immer auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="e1ff3-119">The MPEG-4 file source always sets the value to 0.</span></span> <span data-ttu-id="e1ff3-120">Die MP4-und 3GP-Datei senken ignorieren den Wert dieses Attributs, wenn dieser vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e1ff3-120">The MP4 and 3GP file sinks ignore the value of this attribute if it is present.</span></span>

<span data-ttu-id="e1ff3-121">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="e1ff3-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1ff3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1ff3-122">Requirements</span></span>



| <span data-ttu-id="e1ff3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1ff3-123">Requirement</span></span> | <span data-ttu-id="e1ff3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e1ff3-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ff3-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e1ff3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e1ff3-126">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e1ff3-126">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="e1ff3-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e1ff3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e1ff3-128">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e1ff3-128">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="e1ff3-129">Header</span><span class="sxs-lookup"><span data-stu-id="e1ff3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1ff3-130"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1ff3-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1ff3-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1ff3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1ff3-132">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="e1ff3-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e1ff3-133">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="e1ff3-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="e1ff3-134">\_ \_ \_ Beispiel Beschreibung für MF MT MPEG4 \_</span><span class="sxs-lookup"><span data-stu-id="e1ff3-134">MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION</span></span>](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




