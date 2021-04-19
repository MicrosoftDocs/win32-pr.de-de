---
description: Gibt an, ob der senderwriter die Rate eingehender Daten einschränkt.
ms.assetid: eb79bda7-ece0-4977-a0f9-d40bd5d220ab
title: MF_SINK_WRITER_DISABLE_THROTTLING-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e01c34b51726135516fb6547679db3ba3d48ebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369035"
---
# <a name="mf_sink_writer_disable_throttling-attribute"></a><span data-ttu-id="65022-103">MF \_ Sink \_ Writer \_ deaktivierte \_ Drosselungs Attribut</span><span class="sxs-lookup"><span data-stu-id="65022-103">MF\_SINK\_WRITER\_DISABLE\_THROTTLING attribute</span></span>

<span data-ttu-id="65022-104">Gibt an, ob der senderwriter die Rate eingehender Daten einschränkt.</span><span class="sxs-lookup"><span data-stu-id="65022-104">Specifies whether the sink writer limits the rate of incoming data.</span></span>

## <a name="data-type"></a><span data-ttu-id="65022-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="65022-105">Data type</span></span>

<span data-ttu-id="65022-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="65022-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="65022-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="65022-107">Get/set</span></span>

<span data-ttu-id="65022-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="65022-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="65022-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="65022-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="65022-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65022-110">Remarks</span></span>

<span data-ttu-id="65022-111">Standardmäßig schränkt die [**imfsinkwriter:: schreitesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) -Methode des Sink Writer die Datenrate durch Blockieren des aufrufenden Threads ein.</span><span class="sxs-lookup"><span data-stu-id="65022-111">By default, the sink writer's [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) method limits the data rate by blocking the calling thread.</span></span> <span data-ttu-id="65022-112">Dadurch wird verhindert, dass die Anwendung Stichproben zu schnell bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="65022-112">This prevents the application from delivering samples too quickly.</span></span> <span data-ttu-id="65022-113">Um dieses Verhalten zu deaktivieren, legen \_ Sie beim \_ \_ \_ Erstellen des senderwriter den Wert  für das einschränelnde Attribut für die MF-Senke auf true fest.</span><span class="sxs-lookup"><span data-stu-id="65022-113">To disable this behavior, set the MF\_SINK\_WRITER\_DISABLE\_THROTTLING attribute to **TRUE** when you create the sink writer.</span></span>

<span data-ttu-id="65022-114">Verwenden Sie dieses Attribut mit den folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="65022-114">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="65022-115">**Mfkreatesinkschreiterfrommediasink**</span><span class="sxs-lookup"><span data-stu-id="65022-115">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="65022-116">**MF | atesinkschreiterfromurl**</span><span class="sxs-lookup"><span data-stu-id="65022-116">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="65022-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65022-117">Requirements</span></span>



| <span data-ttu-id="65022-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65022-118">Requirement</span></span> | <span data-ttu-id="65022-119">Wert</span><span class="sxs-lookup"><span data-stu-id="65022-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="65022-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="65022-120">Minimum supported client</span></span><br/> | <span data-ttu-id="65022-121">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="65022-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="65022-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="65022-122">Minimum supported server</span></span><br/> | <span data-ttu-id="65022-123">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="65022-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="65022-124">Header</span><span class="sxs-lookup"><span data-stu-id="65022-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="65022-125"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="65022-125"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65022-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65022-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65022-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="65022-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="65022-128">Senkenwriter-Attribute</span><span class="sxs-lookup"><span data-stu-id="65022-128">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 




