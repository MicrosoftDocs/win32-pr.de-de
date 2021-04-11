---
description: Gibt die Geräte Rolle für ein audioerfassungs-Gerät an.
ms.assetid: 4f2885b6-c771-4577-880d-5feea671432e
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148ae6697151698eef58d3c0148de3ed81822a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041960"
---
# <a name="mf_devsource_attribute_source_type_audcap_role-attribute"></a><span data-ttu-id="18442-103">MF \_ devsource \_ - \_ Attribut \_ Quelltyp ( \_ audcap- \_ Rollen Attribut)</span><span class="sxs-lookup"><span data-stu-id="18442-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ROLE attribute</span></span>

<span data-ttu-id="18442-104">Gibt die Geräte Rolle für ein audioerfassungs-Gerät an.</span><span class="sxs-lookup"><span data-stu-id="18442-104">Specifies the device role for an audio capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="18442-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="18442-105">Data type</span></span>

<span data-ttu-id="18442-106">**Erole** als **UInt32** gespeichert</span><span class="sxs-lookup"><span data-stu-id="18442-106">**ERole** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="18442-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="18442-107">Get/set</span></span>

<span data-ttu-id="18442-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="18442-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="18442-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="18442-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="18442-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18442-110">Remarks</span></span>

<span data-ttu-id="18442-111">Der **erole-Enumerationstyp** ist in der Dokumentation zur kernton-API dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="18442-111">The **eRole** enumeration type is documented in the Core Audio API documentation.</span></span>

<span data-ttu-id="18442-112">Der Wert des-Attributs gibt eine Geräte Rolle an.</span><span class="sxs-lookup"><span data-stu-id="18442-112">The value of the attribute specifies a device role.</span></span> <span data-ttu-id="18442-113">Dieses Attribut wird mit den folgenden Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="18442-113">This attribute is used with the following functions.</span></span>

<span data-ttu-id="18442-114">Dieses Attribut kann als Eingabe für die Funktionen [**mfkreatedevicesource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) und [**mfkreatedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18442-114">This attribute can be used as input to the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) and [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) functions.</span></span> <span data-ttu-id="18442-115">Wenn das-Attribut angegeben wird, erstellt die Funktion eine Medienquelle, die das standardaudioerfassungs-Gerät für die angegebene Geräte Rolle verwendet.</span><span class="sxs-lookup"><span data-stu-id="18442-115">If the attribute is specified, the function creates a media source that uses the default audio capture device for the specified device role.</span></span>

<span data-ttu-id="18442-116">Dieses Attribut kann auch als Eingabe für die [**mfenumschlag**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) -Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18442-116">This attribute can also be used as input to the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span> <span data-ttu-id="18442-117">Wenn das-Attribut angegeben wird, ist die-Enumeration auf die angegebene Geräte Rolle beschränkt.</span><span class="sxs-lookup"><span data-stu-id="18442-117">If the attribute is specified, the enumeration is restricted to the specified device role.</span></span> <span data-ttu-id="18442-118">Außerdem enthält jedes Aktivierungs Objekt, das von der **mfenenumervicesources** -Funktion zurückgegeben wird, dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="18442-118">In addition, each activation object returned by the **MFEnumDeviceSources** function contains this attribute.</span></span> <span data-ttu-id="18442-119">Das-Attribut wird dann intern vom Aktivierungs Objekt verwendet, wenn es die Medienquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="18442-119">The attribute is then used internally by the activation object when it creates the media source.</span></span>

<span data-ttu-id="18442-120">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="18442-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="18442-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18442-121">Requirements</span></span>



| <span data-ttu-id="18442-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18442-122">Requirement</span></span> | <span data-ttu-id="18442-123">Wert</span><span class="sxs-lookup"><span data-stu-id="18442-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18442-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18442-124">Minimum supported client</span></span><br/> | <span data-ttu-id="18442-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18442-125">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="18442-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18442-126">Minimum supported server</span></span><br/> | <span data-ttu-id="18442-127">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18442-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="18442-128">Header</span><span class="sxs-lookup"><span data-stu-id="18442-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="18442-129"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="18442-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18442-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18442-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18442-131">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="18442-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="18442-132">Audio-/Videoaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="18442-132">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="18442-133">Geräte Attribute erfassen</span><span class="sxs-lookup"><span data-stu-id="18442-133">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




