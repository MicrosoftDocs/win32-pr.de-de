---
description: Gibt eine MMCSS-Klasse (Multimedia Class Scheduler Service) für den Quell Reader oder den senkenwriter an.
ms.assetid: A3A295E8-AC9C-4641-ADDA-B97D5AB13A9A
title: MF_READWRITE_MMCSS_CLASS-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2088ba09bf4f8ad9516d9b2117ab54161d7ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759078"
---
# <a name="mf_readwrite_mmcss_class-attribute"></a><span data-ttu-id="a6c16-103">MF- \_ \_ Attribut der MMCSS- \_ Klasse "Read Write"</span><span class="sxs-lookup"><span data-stu-id="a6c16-103">MF\_READWRITE\_MMCSS\_CLASS attribute</span></span>

<span data-ttu-id="a6c16-104">Gibt eine MMCSS-Klasse ( [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) ) für den Quell Reader oder den senkenwriter an.</span><span class="sxs-lookup"><span data-stu-id="a6c16-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) class for the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="a6c16-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a6c16-105">Data type</span></span>

<span data-ttu-id="a6c16-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a6c16-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="a6c16-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="a6c16-107">Get/set</span></span>

<span data-ttu-id="a6c16-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="a6c16-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="a6c16-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a6c16-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="a6c16-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6c16-110">Remarks</span></span>

<span data-ttu-id="a6c16-111">Legen Sie dieses Attribut optional fest, wenn Sie eine Instanz des [Quell](source-reader.md) -oder [Senke Writers](sink-writer.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="a6c16-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="a6c16-112">Der Wert des-Attributs muss ein gültiger MMCSS-Klassenname sein.</span><span class="sxs-lookup"><span data-stu-id="a6c16-112">The value of the attribute must be a valid MMCSS class name.</span></span>

<span data-ttu-id="a6c16-113">Wenn dieses Attribut festgelegt ist, registriert der Quell-oder sendenden Writer alle zugehörigen Threads bei der angegebenen MMCSS-Klasse.</span><span class="sxs-lookup"><span data-stu-id="a6c16-113">If this attribute is set, the Source Reader or Sink Writer registers all of its threads with the specified MMCSS class.</span></span> <span data-ttu-id="a6c16-114">Das MMCSS stellt sicher, dass die Datenverarbeitung im Quell-oder sendenden Writer Vorrang vor anderen System Tasks hat.</span><span class="sxs-lookup"><span data-stu-id="a6c16-114">The MMCSS ensures that data processing in the Source Reader or Sink Writer has priority over other system tasks.</span></span>

<span data-ttu-id="a6c16-115">Um die Basis Priorität anzugeben, legen Sie das MF-Attribut "read [ \_ Write \_ MMCSS \_ Priority](mf-readwrite-mmcss-priority.md) " fest.</span><span class="sxs-lookup"><span data-stu-id="a6c16-115">To specify the base priority, set the [MF\_READWRITE\_MMCSS\_PRIORITY](mf-readwrite-mmcss-priority.md) attribute.</span></span> <span data-ttu-id="a6c16-116">Wenn dieses Attribut nicht festgelegt ist, ist die Basis Priorität 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a6c16-116">If that attribute is not set, the base priority is zero.</span></span>

<span data-ttu-id="a6c16-117">Bei audioverarbeitungsthreads überschreibt das audioattribut für die MF-Klasse "read [ \_ Write \_ MMCSS \_ Class \_ ](mf-readwrite-mmcss-class-audio.md) " (falls festgelegt) dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="a6c16-117">For audio-processing threads, the [MF\_READWRITE\_MMCSS\_CLASS\_AUDIO](mf-readwrite-mmcss-class-audio.md) attribute (if set) overrides this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6c16-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6c16-118">Requirements</span></span>



| <span data-ttu-id="a6c16-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6c16-119">Requirement</span></span> | <span data-ttu-id="a6c16-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a6c16-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6c16-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6c16-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a6c16-122">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a6c16-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="a6c16-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6c16-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a6c16-124">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a6c16-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a6c16-125">Header</span><span class="sxs-lookup"><span data-stu-id="a6c16-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6c16-126"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a6c16-126"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6c16-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6c16-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6c16-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a6c16-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
