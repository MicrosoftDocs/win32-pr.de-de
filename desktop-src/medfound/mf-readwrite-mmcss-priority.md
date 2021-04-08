---
description: Legt die Basis Thread Priorität für den Quell-oder senderwriter fest.
ms.assetid: 9513AE28-2AF4-45EC-AC19-C0718540E26F
title: MF_READWRITE_MMCSS_PRIORITY-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7b83485b49e6ae584a38024e180f37c878d27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050459"
---
# <a name="mf_readwrite_mmcss_priority-attribute"></a><span data-ttu-id="b1bc1-103">MF- \_ Attribut zum Lesen von \_ MMCSS- \_ Priorität</span><span class="sxs-lookup"><span data-stu-id="b1bc1-103">MF\_READWRITE\_MMCSS\_PRIORITY attribute</span></span>

<span data-ttu-id="b1bc1-104">Legt die Basis Thread Priorität für den Quell-oder senderwriter fest.</span><span class="sxs-lookup"><span data-stu-id="b1bc1-104">Sets the base thread priority for the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="b1bc1-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b1bc1-105">Data type</span></span>

<span data-ttu-id="b1bc1-106">**Int32** als **UInt32** gespeichert</span><span class="sxs-lookup"><span data-stu-id="b1bc1-106">**INT32** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b1bc1-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="b1bc1-107">Get/set</span></span>

<span data-ttu-id="b1bc1-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b1bc1-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b1bc1-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b1bc1-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b1bc1-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1bc1-110">Remarks</span></span>

<span data-ttu-id="b1bc1-111">Legen Sie dieses Attribut optional fest, wenn Sie eine Instanz des [Quell](source-reader.md) -oder [Senke Writers](sink-writer.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="b1bc1-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="b1bc1-112">Wenn Sie dieses Attribut festlegen, legen Sie auch das MF-Attribut der Klasse "read [ \_ Write \_ MMCSS \_ Class](mf-readwrite-mmcss-class.md) " fest.</span><span class="sxs-lookup"><span data-stu-id="b1bc1-112">If you set this attribute, also set the [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md) attribute.</span></span> <span data-ttu-id="b1bc1-113">Andernfalls wird dieses Attribut ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b1bc1-113">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="b1bc1-114">Wenn der Quell-oder senkenwriter Threads beim [Multimedia Class Scheduler-Dienst](../procthread/multimedia-class-scheduler-service.md)registriert, gibt der Wert dieses Attributs die Basis Thread Priorität an.</span><span class="sxs-lookup"><span data-stu-id="b1bc1-114">When the Source Reader or Sink Writer registers threads with the [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md), the value of this attribute specifies the base thread priority.</span></span> <span data-ttu-id="b1bc1-115">Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b1bc1-115">If this attribute is not set, the default value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1bc1-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1bc1-116">Requirements</span></span>



| <span data-ttu-id="b1bc1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1bc1-117">Requirement</span></span> | <span data-ttu-id="b1bc1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b1bc1-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1bc1-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1bc1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b1bc1-120">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b1bc1-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b1bc1-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1bc1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b1bc1-122">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b1bc1-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b1bc1-123">Header</span><span class="sxs-lookup"><span data-stu-id="b1bc1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1bc1-124"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b1bc1-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1bc1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1bc1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1bc1-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="b1bc1-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
