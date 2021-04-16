---
description: Gibt an, welche Streams erfolgreich mit einer Medien Senke verbunden wurden.
ms.assetid: b5e45bfc-d91d-41b8-aaa4-72b3a23d869e
title: MFP_PKEY_StreamRenderingResults-Eigenschaft (MF Play. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6acf04f751e8611f3add3a62fc7b4406d757999e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343928"
---
# <a name="mfp_pkey_streamrenderingresults-property"></a><span data-ttu-id="d9d10-103">MFP \_ pkey \_ streamrenderingresults (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d9d10-103">MFP\_PKEY\_StreamRenderingResults property</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9d10-104">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="d9d10-104">Deprecated.</span></span> <span data-ttu-id="d9d10-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d9d10-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="d9d10-106">Anwendungen sollten die [Medien Sitzung](media-session.md) für die Wiedergabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="d9d10-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="d9d10-107">Gibt an, welche Streams erfolgreich mit einer Medien Senke verbunden wurden.</span><span class="sxs-lookup"><span data-stu-id="d9d10-107">Specifies which streams were connected successfully to a media sink.</span></span>



<span data-ttu-id="d9d10-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d9d10-108">Data type</span></span>

<span data-ttu-id="d9d10-109">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="d9d10-109">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d9d10-110">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="d9d10-110">PROPVARIANT member</span></span>

<span data-ttu-id="d9d10-111">Array von **DWORD** -Werten (**CAUL**)</span><span class="sxs-lookup"><span data-stu-id="d9d10-111">Array of **DWORD** values (**CAUL**)</span></span>

<span data-ttu-id="d9d10-112">VT \_ Vector \| VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="d9d10-112">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="d9d10-113">**CAUL**</span><span class="sxs-lookup"><span data-stu-id="d9d10-113">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="d9d10-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9d10-114">Remarks</span></span>

<span data-ttu-id="d9d10-115">Diese Eigenschaft kann mit dem **MFP- \_ \_ Ereignistyp \_ mediaitem \_ Set** Event gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9d10-115">This property can be sent with the **MFP\_EVENT\_TYPE\_MEDIAITEM\_SET** event.</span></span>

<span data-ttu-id="d9d10-116">Der Wert der Eigenschaft ist ein Array von **HRESULT** s.</span><span class="sxs-lookup"><span data-stu-id="d9d10-116">The value of the property is an array of **HRESULT** s.</span></span> <span data-ttu-id="d9d10-117">Die Array Einträge entsprechen Streams auf dem aktuellen Medien Element.</span><span class="sxs-lookup"><span data-stu-id="d9d10-117">The array entries correspond to streams on the current media item.</span></span> <span data-ttu-id="d9d10-118">Jeder Eintrag im Array gibt wie folgt an, ob der entsprechende Stream mit einer Medien Senke verbunden war:</span><span class="sxs-lookup"><span data-stu-id="d9d10-118">Each entry in the array indicates whether the corresponding stream was connected to a media sink, as follows:</span></span>

-   <span data-ttu-id="d9d10-119">Wenn der Stream mit einer Medien Senke verbunden ist, ist der Wert **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d9d10-119">If the stream is connected to a media sink, the value is **S\_OK**.</span></span>
-   <span data-ttu-id="d9d10-120">Wenn der Stream nicht ausgewählt ist, ist der Wert **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="d9d10-120">If the stream is not selected, the value is **S\_FALSE**.</span></span>
-   <span data-ttu-id="d9d10-121">Wenn beim Versuch, eine Verbindung mit dem Stream herzustellen, ein Fehler aufgetreten ist, ist der Wert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d9d10-121">If an error occurred while attempting to connect the stream, the value is an error code.</span></span>

<span data-ttu-id="d9d10-122">Wenn mindestens ein Stream erfolgreich verbunden wurde, kann die Wiedergabe durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d9d10-122">If at least one stream was connected successfully, playback is possible.</span></span> <span data-ttu-id="d9d10-123">Der Benutzer kann z. b. den Codec zum Wiedergeben des Audiostreams benötigen, aber nicht den Videostream abspielen.</span><span class="sxs-lookup"><span data-stu-id="d9d10-123">For example, the user might have the codec needed to play the audio stream but not to play the video stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9d10-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9d10-124">Requirements</span></span>



| <span data-ttu-id="d9d10-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9d10-125">Requirement</span></span> | <span data-ttu-id="d9d10-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d9d10-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d9d10-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9d10-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d9d10-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9d10-128">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d9d10-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9d10-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d9d10-130">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9d10-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d9d10-131">Header</span><span class="sxs-lookup"><span data-stu-id="d9d10-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9d10-132"><dt>"MF Play. h"</dt></span><span class="sxs-lookup"><span data-stu-id="d9d10-132"><dt>Mfplay.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9d10-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9d10-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9d10-134">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d9d10-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d9d10-135">**MFP- \_ mediaitem- \_ Set- \_ Ereignis**</span><span class="sxs-lookup"><span data-stu-id="d9d10-135">**MFP\_MEDIAITEM\_SET\_EVENT**</span></span>](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event)
</dt> </dl>

 

 




