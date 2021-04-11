---
description: Enthält den symbolischen Link für einen Video Erfassungs Treiber.
ms.assetid: 3d256dec-ec8c-4c62-883b-e2c292fd90eb
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48e1c854ee070713462676482cc04690c2bdde2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130721"
---
# <a name="mf_devsource_attribute_source_type_vidcap_symbolic_link-attribute"></a><span data-ttu-id="db5cb-103">MF \_ devsource \_ - \_ Attribut \_ Quelltyp \_ VidCap \_ symbolischen \_ Link Attribut</span><span class="sxs-lookup"><span data-stu-id="db5cb-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK attribute</span></span>

<span data-ttu-id="db5cb-104">Enthält den symbolischen Link für einen Video Erfassungs Treiber.</span><span class="sxs-lookup"><span data-stu-id="db5cb-104">Contains the symbolic link for a video capture driver.</span></span>

## <a name="data-type"></a><span data-ttu-id="db5cb-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="db5cb-105">Data type</span></span>

<span data-ttu-id="db5cb-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="db5cb-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="db5cb-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="db5cb-107">Get/set</span></span>

<span data-ttu-id="db5cb-108">Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="db5cb-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="db5cb-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="db5cb-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="db5cb-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db5cb-110">Remarks</span></span>

<span data-ttu-id="db5cb-111">Verwenden Sie dieses Attribut als Eingabe für die [**mfkreatedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="db5cb-111">Use this attribute as input to the [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span>

<span data-ttu-id="db5cb-112">Außerdem wird dieses Attribut für die Aktivierungs Objekte festgelegt, die von den folgenden Funktionen zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="db5cb-112">In addition, this attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="db5cb-113">**MF | atedevicesourceaktivierungs**</span><span class="sxs-lookup"><span data-stu-id="db5cb-113">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="db5cb-114">**Mfenumschlag**</span><span class="sxs-lookup"><span data-stu-id="db5cb-114">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="db5cb-115">Die symbolische Verknüpfung sollte als nicht transparente Zeichenfolge betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="db5cb-115">The symbolic link should be considered an opaque string.</span></span> <span data-ttu-id="db5cb-116">Der lesbare Anzeige Name für ein Gerät ist in dem Attribut "Anzeige Name" des [MF- \_ devsource- \_ Attributs \_ \_ ](mf-devsource-attribute-friendly-name.md) enthalten.</span><span class="sxs-lookup"><span data-stu-id="db5cb-116">The human-readable display name for a device is contained in the [MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME](mf-devsource-attribute-friendly-name.md) attribute.</span></span>

<span data-ttu-id="db5cb-117">Das Attribut "MF \_ devsource \_ Attribute \_ Source \_ Type \_ VidCap \_ symbolischen \_ Link" kann als Wert des DevicePath-Arguments der [**setupdiopendeviceinterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) -Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="db5cb-117">The MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK attribute can be passed in as the value of the DevicePath argument of the [**SetupDiOpenDeviceInterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) function.</span></span>

<span data-ttu-id="db5cb-118">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="db5cb-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="db5cb-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db5cb-119">Requirements</span></span>



| <span data-ttu-id="db5cb-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db5cb-120">Requirement</span></span> | <span data-ttu-id="db5cb-121">Wert</span><span class="sxs-lookup"><span data-stu-id="db5cb-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db5cb-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db5cb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="db5cb-123">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db5cb-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="db5cb-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db5cb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="db5cb-125">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db5cb-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="db5cb-126">Header</span><span class="sxs-lookup"><span data-stu-id="db5cb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="db5cb-127"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="db5cb-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db5cb-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db5cb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db5cb-129">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="db5cb-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="db5cb-130">Audio-/Videoaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="db5cb-130">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="db5cb-131">Geräte Attribute erfassen</span><span class="sxs-lookup"><span data-stu-id="db5cb-131">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 
