---
description: Gibt eine MMCSS-Klasse (Multimedia Class Scheduler Service) für audioverarbeitungsthreads im Quell-oder senkenwriter an.
ms.assetid: F1B8A8C8-2E41-4321-A94D-C50447C69941
title: MF_READWRITE_MMCSS_CLASS_AUDIO-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa35db710c6b72c103855fa2c0a9f169f49c4511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368149"
---
# <a name="mf_readwrite_mmcss_class_audio-attribute"></a><span data-ttu-id="7ec41-103">MF \_ \_ -Attribut der MMCSS \_ -Klasse für die \_ Audioerstellung</span><span class="sxs-lookup"><span data-stu-id="7ec41-103">MF\_READWRITE\_MMCSS\_CLASS\_AUDIO attribute</span></span>

<span data-ttu-id="7ec41-104">Gibt eine MMCSS-Klasse ( [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) ) für audioverarbeitungsthreads im Quell-oder senkenwriter an.</span><span class="sxs-lookup"><span data-stu-id="7ec41-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) class for audio-processing threads in the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="7ec41-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7ec41-105">Data type</span></span>

<span data-ttu-id="7ec41-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7ec41-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="7ec41-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="7ec41-107">Get/set</span></span>

<span data-ttu-id="7ec41-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="7ec41-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="7ec41-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7ec41-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ec41-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ec41-110">Remarks</span></span>

<span data-ttu-id="7ec41-111">Legen Sie dieses Attribut optional fest, wenn Sie eine Instanz des [Quell](source-reader.md) -oder [Senke Writers](sink-writer.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="7ec41-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="7ec41-112">Der Wert des-Attributs muss ein gültiger MMCSS-Klassenname sein.</span><span class="sxs-lookup"><span data-stu-id="7ec41-112">The value of the attribute must be a valid MMCSS class name.</span></span>

<span data-ttu-id="7ec41-113">Wenn dieses Attribut festgelegt ist, registriert der Quell-oder sendenden Writer seine audioverarbeitungsthreads bei der angegebenen MMCSS-Klasse.</span><span class="sxs-lookup"><span data-stu-id="7ec41-113">If this attribute is set, the Source Reader or Sink Writer registers its audio-processing threads with the specified MMCSS class.</span></span> <span data-ttu-id="7ec41-114">Das MMCSS stellt sicher, dass die Datenverarbeitung im Quell-oder sendenden Writer Vorrang vor anderen System Tasks hat.</span><span class="sxs-lookup"><span data-stu-id="7ec41-114">The MMCSS ensures that data processing in the Source Reader or Sink Writer has priority over other system tasks.</span></span>

<span data-ttu-id="7ec41-115">Wenn Sie die Basis Priorität für audiothreads angeben möchten, legen Sie das [audioattribut für die MF \_ -Read Write \_ MMCSS \_ \_ -Priorität](mf-readwrite-mmcss-priority-audio.md) fest.</span><span class="sxs-lookup"><span data-stu-id="7ec41-115">To specify the base priority for audio threads, set the [MF\_READWRITE\_MMCSS\_PRIORITY\_AUDIO](mf-readwrite-mmcss-priority-audio.md) attribute.</span></span> <span data-ttu-id="7ec41-116">Wenn dieses Attribut nicht festgelegt ist, ist die Basis Priorität für audiothreads 0 (null).</span><span class="sxs-lookup"><span data-stu-id="7ec41-116">If that attribute is not set, the base priority for audio threads is zero.</span></span>

<span data-ttu-id="7ec41-117">Dieses Attribut überschreibt das MF-Attribut der Klasse "read [ \_ Write \_ MMCSS \_ ](mf-readwrite-mmcss-class.md) " für audioverarbeitungsthreads.</span><span class="sxs-lookup"><span data-stu-id="7ec41-117">This attribute overrides the [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md) attribute for audio-processing threads.</span></span> <span data-ttu-id="7ec41-118">Wenn keines der Attribute festgelegt ist, werden audiothreads nicht bei MCSS registriert.</span><span class="sxs-lookup"><span data-stu-id="7ec41-118">If neither attribute is set, audio threads are not registered with MCSS.</span></span>

<span data-ttu-id="7ec41-119">Bei den meisten Anwendungen ist das Audiomaterial für den Benutzer deutlich deutlicher als das Video-und somit weniger akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="7ec41-119">For most applications, audio glitching is much more noticeable to the user than video glitching, and therefore less acceptable.</span></span> <span data-ttu-id="7ec41-120">Aus diesem Grund sollte eine Anwendung in der Regel die MF-Klasse "read \_ Write \_ MMCSS \_ Class" \_ auf eine MMCSS-Klasse mit höherer Priorität festlegen als die "MF-Klasse" read [ \_ Write \_ MMCSS \_ ](mf-readwrite-mmcss-class.md)".</span><span class="sxs-lookup"><span data-stu-id="7ec41-120">For this reason, an application should typically set MF\_READWRITE\_MMCSS\_CLASS\_AUDIO to a higher-priority MMCSS class than [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md).</span></span> <span data-ttu-id="7ec41-121">Dadurch wird sichergestellt, dass die Audioverarbeitung höhere Priorität hat als andere Tasks.</span><span class="sxs-lookup"><span data-stu-id="7ec41-121">This ensures that audio processing is given higher priority than other tasks.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ec41-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ec41-122">Requirements</span></span>



| <span data-ttu-id="7ec41-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ec41-123">Requirement</span></span> | <span data-ttu-id="7ec41-124">Wert</span><span class="sxs-lookup"><span data-stu-id="7ec41-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec41-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ec41-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7ec41-126">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7ec41-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="7ec41-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ec41-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7ec41-128">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7ec41-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="7ec41-129">Header</span><span class="sxs-lookup"><span data-stu-id="7ec41-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ec41-130"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7ec41-130"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ec41-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ec41-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ec41-132">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="7ec41-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
