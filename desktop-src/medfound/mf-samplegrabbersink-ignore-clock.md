---
description: Gibt an, ob die Beispiel-Grabber-Senke die Präsentationszeit zum Planen von Beispielen verwendet.
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: MF_SAMPLEGRABBERSINK_IGNORE_CLOCK-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ad5476779d958bdbf94af554d889dd8d174ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368012"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a><span data-ttu-id="73615-103">MF \_ samplegrabbersink \_ Ignore \_ Clock-Attribut</span><span class="sxs-lookup"><span data-stu-id="73615-103">MF\_SAMPLEGRABBERSINK\_IGNORE\_CLOCK attribute</span></span>

<span data-ttu-id="73615-104">Gibt an, ob die Beispiel-Grabber-Senke die Präsentationszeit zum Planen von Beispielen verwendet.</span><span class="sxs-lookup"><span data-stu-id="73615-104">Specifies whether the sample-grabber sink uses the presentation clock to schedule samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="73615-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="73615-105">Data type</span></span>

<span data-ttu-id="73615-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="73615-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="73615-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="73615-107">Get/set</span></span>

<span data-ttu-id="73615-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="73615-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="73615-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="73615-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="73615-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73615-110">Remarks</span></span>

<span data-ttu-id="73615-111">Sie können dieses Attribut für das Aktivierungs Objekt festlegen, das von der [**mfikreatesamplegrabbersink**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) Activation-Funktion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="73615-111">You can set this attribute on the activation object created by the [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) function.</span></span> <span data-ttu-id="73615-112">Legen Sie das-Attribut fest, bevor Sie die [**imfactivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) -Methode für das Aktivierungs Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="73615-112">Set the attribute before calling the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method on the activation object.</span></span>

<span data-ttu-id="73615-113">Wenn die Senke Sample-Grabber ein Beispiel erhält, wartet Sie standardmäßig, bis die Präsentationszeit des Beispiels den Rückruf der Anwendung aufruft.</span><span class="sxs-lookup"><span data-stu-id="73615-113">By default, when the sample-grabber sink receives a sample, it waits until the presentation time of the sample to invoke the application's callback.</span></span> <span data-ttu-id="73615-114">Wenn das Attribut "MF \_ samplegrabbersink \_ Ignore Clock" ungleich \_ NULL ist, ignoriert die Stichprobenentnahme "Sample-Grabber" die Präsentations Uhr und ruft den Rückruf auf, sobald die einzelnen Stichproben empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="73615-114">If the MF\_SAMPLEGRABBERSINK\_IGNORE\_CLOCK attribute is nonzero, the sample-grabber sink ignores the presentation clock and invokes the callback as soon as it receives each sample.</span></span>

<span data-ttu-id="73615-115">Empfohlene Verwendung:</span><span class="sxs-lookup"><span data-stu-id="73615-115">Recommended usage:</span></span>

-   <span data-ttu-id="73615-116">Wenn Sie Beispiele so schnell wie möglich verarbeiten möchten, legen Sie dieses Attribut auf " **true**" fest.</span><span class="sxs-lookup"><span data-stu-id="73615-116">If you want to process samples as quickly as possible, set this attribute to **TRUE**.</span></span>
-   <span data-ttu-id="73615-117">Wenn Sie möchten, dass die Aufrufe der Rückruf Methode mit der Uhr synchronisiert werden, legen Sie dieses Attribut entweder nicht fest, oder legen Sie es auf **false** fest.</span><span class="sxs-lookup"><span data-stu-id="73615-117">If you want the calls to the callback method to be synchronized with the clock, either do not set this attribute or set it to **FALSE**.</span></span> <span data-ttu-id="73615-118">Sie können die Beispiele leicht vor der Uhr erhalten, während Sie synchronisiert werden, indem Sie das [**\_ \_ Beispiel \_ Zeit \_ Offset-Attribut "MF samplegrabbersink**](mf-samplegrabbersink-sample-time-offset-attribute.md) " festlegen.</span><span class="sxs-lookup"><span data-stu-id="73615-118">You can get samples slightly ahead of the clock, while still remaining synchronized, by setting the [**MF\_SAMPLEGRABBERSINK\_SAMPLE\_TIME\_OFFSET**](mf-samplegrabbersink-sample-time-offset-attribute.md) attribute.</span></span>

<span data-ttu-id="73615-119">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="73615-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="73615-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73615-120">Requirements</span></span>



| <span data-ttu-id="73615-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73615-121">Requirement</span></span> | <span data-ttu-id="73615-122">Wert</span><span class="sxs-lookup"><span data-stu-id="73615-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73615-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73615-123">Minimum supported client</span></span><br/> | <span data-ttu-id="73615-124">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73615-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="73615-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73615-125">Minimum supported server</span></span><br/> | <span data-ttu-id="73615-126">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73615-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="73615-127">Header</span><span class="sxs-lookup"><span data-stu-id="73615-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="73615-128"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="73615-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73615-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73615-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73615-130">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="73615-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="73615-131">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="73615-131">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




