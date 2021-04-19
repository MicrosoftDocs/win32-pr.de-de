---
description: Legt die Basis Priorität für die audioverarbeitungsthreads fest, die vom Quell-und senkwriter erstellt werden.
ms.assetid: C0E3A472-959F-4F74-8906-03630DE4CB8C
title: MF_READWRITE_MMCSS_PRIORITY_AUDIO-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c33f3e4cab26a448c3b5a28c6f3cfe631a7c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372887"
---
# <a name="mf_readwrite_mmcss_priority_audio-attribute"></a><span data-ttu-id="0fe64-103">MF \_ \_ -audioattribut für die MMCSS \_ \_ -Priorität</span><span class="sxs-lookup"><span data-stu-id="0fe64-103">MF\_READWRITE\_MMCSS\_PRIORITY\_AUDIO attribute</span></span>

<span data-ttu-id="0fe64-104">Legt die Basis Priorität für die audioverarbeitungsthreads fest, die vom Quell-und senkwriter erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0fe64-104">Sets the base priority for audio-processing threads created by the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="0fe64-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0fe64-105">Data type</span></span>

<span data-ttu-id="0fe64-106">**Int32** als **UInt32** gespeichert</span><span class="sxs-lookup"><span data-stu-id="0fe64-106">**INT32** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="0fe64-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="0fe64-107">Get/set</span></span>

<span data-ttu-id="0fe64-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="0fe64-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="0fe64-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="0fe64-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="0fe64-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fe64-110">Remarks</span></span>

<span data-ttu-id="0fe64-111">Legen Sie dieses Attribut optional fest, wenn Sie eine Instanz des [Quell](source-reader.md) -oder [Senke Writers](sink-writer.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="0fe64-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="0fe64-112">Wenn Sie dieses Attribut festlegen, legen Sie auch [das \_ audioattribut der MF \_ \_ \_ -Klasse "Read Write MMCSS Class](mf-readwrite-mmcss-class-audio.md) " fest.</span><span class="sxs-lookup"><span data-stu-id="0fe64-112">If you set this attribute, also set the [MF\_READWRITE\_MMCSS\_CLASS\_AUDIO](mf-readwrite-mmcss-class-audio.md) attribute.</span></span> <span data-ttu-id="0fe64-113">Andernfalls wird dieses Attribut ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0fe64-113">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="0fe64-114">Wenn der Quell-oder senkenwriter audioverarbeitungsthreads beim [Multimedia Class Scheduler-Dienst](../procthread/multimedia-class-scheduler-service.md)registriert, gibt der Wert dieses Attributs die Basis Thread Priorität an.</span><span class="sxs-lookup"><span data-stu-id="0fe64-114">When the Source Reader or Sink Writer registers audio-processing threads with the [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md), the value of this attribute specifies the base thread priority.</span></span> <span data-ttu-id="0fe64-115">Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0fe64-115">If this attribute is not set, the default value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fe64-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fe64-116">Requirements</span></span>



| <span data-ttu-id="0fe64-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fe64-117">Requirement</span></span> | <span data-ttu-id="0fe64-118">Wert</span><span class="sxs-lookup"><span data-stu-id="0fe64-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fe64-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fe64-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0fe64-120">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0fe64-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0fe64-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fe64-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0fe64-122">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0fe64-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="0fe64-123">Header</span><span class="sxs-lookup"><span data-stu-id="0fe64-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fe64-124"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="0fe64-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fe64-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fe64-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fe64-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="0fe64-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
