---
description: Gibt den anzeigen Amen für ein Gerät an.
ms.assetid: 3f6c7faf-2ecd-4510-adc2-252c3619d70f
title: MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab0d2bb3c0e75d547e1249a83261b7c804743ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345147"
---
# <a name="mf_devsource_attribute_friendly_name-attribute"></a><span data-ttu-id="a4c08-103">Attribut Anzeige Name für das MF- \_ devsource- \_ Attribut \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4c08-103">MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME attribute</span></span>

<span data-ttu-id="a4c08-104">Gibt den anzeigen Amen für ein Gerät an.</span><span class="sxs-lookup"><span data-stu-id="a4c08-104">Specifies the display name for a device.</span></span> <span data-ttu-id="a4c08-105">Der *Anzeige Name* ist eine lesbare Zeichenfolge, die für die Anzeige in einer Benutzeroberfläche geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="a4c08-105">The *display name* is a human-readable string, suitable for display in a user interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="a4c08-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a4c08-106">Data type</span></span>

<span data-ttu-id="a4c08-107">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="a4c08-107">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="a4c08-108">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="a4c08-108">Get/set</span></span>

<span data-ttu-id="a4c08-109">Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="a4c08-109">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="a4c08-110">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a4c08-110">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="a4c08-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4c08-111">Remarks</span></span>

<span data-ttu-id="a4c08-112">Dieses Attribut wird für die Aktivierungs Objekte festgelegt, die von den folgenden Funktionen zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="a4c08-112">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="a4c08-113">**MF | atedevicesourceaktivierungs**</span><span class="sxs-lookup"><span data-stu-id="a4c08-113">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="a4c08-114">**Mfenumschlag**</span><span class="sxs-lookup"><span data-stu-id="a4c08-114">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="a4c08-115">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="a4c08-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4c08-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4c08-116">Requirements</span></span>



| <span data-ttu-id="a4c08-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4c08-117">Requirement</span></span> | <span data-ttu-id="a4c08-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a4c08-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c08-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4c08-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a4c08-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4c08-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a4c08-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4c08-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a4c08-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4c08-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a4c08-123">Header</span><span class="sxs-lookup"><span data-stu-id="a4c08-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4c08-124"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4c08-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4c08-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4c08-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c08-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a4c08-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a4c08-127">Audio-/Videoaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="a4c08-127">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="a4c08-128">Geräte Attribute erfassen</span><span class="sxs-lookup"><span data-stu-id="a4c08-128">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




