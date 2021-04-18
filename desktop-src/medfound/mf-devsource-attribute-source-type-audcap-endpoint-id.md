---
description: Gibt die Endpunkt-ID für ein audioerfassungs-Gerät an.
ms.assetid: a0d8b54b-7a05-4307-a756-a34bb22f1afd
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1448dc753a8e3b8221fa040309d3f5b60c4879
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372283"
---
# <a name="mf_devsource_attribute_source_type_audcap_endpoint_id-attribute"></a><span data-ttu-id="ed759-103">MF \_ devsource \_ - \_ Attribut \_ Quelltyp " \_ audcap \_ EndPoint \_ ID"-Attribut</span><span class="sxs-lookup"><span data-stu-id="ed759-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID attribute</span></span>

<span data-ttu-id="ed759-104">Gibt die Endpunkt-ID für ein audioerfassungs-Gerät an.</span><span class="sxs-lookup"><span data-stu-id="ed759-104">Specifies the endpoint ID for an audio capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="ed759-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ed759-105">Data type</span></span>

<span data-ttu-id="ed759-106">**WCHAR\***</span><span class="sxs-lookup"><span data-stu-id="ed759-106">**WCHAR\***</span></span>

## <a name="getset"></a><span data-ttu-id="ed759-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="ed759-107">Get/set</span></span>

<span data-ttu-id="ed759-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="ed759-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="ed759-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ed759-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="ed759-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed759-110">Remarks</span></span>

<span data-ttu-id="ed759-111">Der Wert des-Attributs ist eine Endpunkt-ID.</span><span class="sxs-lookup"><span data-stu-id="ed759-111">The value of the attribute is an endpoint ID.</span></span> <span data-ttu-id="ed759-112">Dieses Attribut wird mit den folgenden Funktionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="ed759-112">This attribute is used with the following functions:</span></span>

-   <span data-ttu-id="ed759-113">Sie kann als Eingabe für die Funktionen [**mfkreatedevicesource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) und [**mfkreatedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed759-113">It can be used as input to the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) and [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) functions.</span></span> <span data-ttu-id="ed759-114">In diesem Kontext gibt das-Attribut das audioerfassungs Gerät für die-Funktion an.</span><span class="sxs-lookup"><span data-stu-id="ed759-114">In this context, the attribute specifies the audio capture device for the function.</span></span> <span data-ttu-id="ed759-115">Sie können die Endpunkt-ID für ein bestimmtes Gerät abrufen, indem Sie die [**immdevice:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ed759-115">You can get the endpoint ID for a given device by calling the [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) method.</span></span> <span data-ttu-id="ed759-116">Weitere Informationen finden Sie in der Dokumentation zur kernton-API.</span><span class="sxs-lookup"><span data-stu-id="ed759-116">See the Core Audio API documentation for more information.</span></span>
-   <span data-ttu-id="ed759-117">Wenn die [**mfenumtovicesources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) -Funktion Audiogeräte auflistet, enthalten die zurückgegebenen Aktivierungs Objekte dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="ed759-117">When the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function enumerates audio devices, the returned activation objects contain this attribute.</span></span> <span data-ttu-id="ed759-118">Das-Attribut wird vom Aktivierungs Objekt intern verwendet, wenn es die Medienquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed759-118">The attribute is used internally by the activation object when it creates the media source.</span></span>

<span data-ttu-id="ed759-119">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="ed759-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed759-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed759-120">Requirements</span></span>



| <span data-ttu-id="ed759-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed759-121">Requirement</span></span> | <span data-ttu-id="ed759-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ed759-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed759-123">Header</span><span class="sxs-lookup"><span data-stu-id="ed759-123">Header</span></span><br/> | <dl> <span data-ttu-id="ed759-124"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed759-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed759-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed759-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed759-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="ed759-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ed759-127">Audio-/Videoaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="ed759-127">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="ed759-128">Geräte Attribute erfassen</span><span class="sxs-lookup"><span data-stu-id="ed759-128">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 
