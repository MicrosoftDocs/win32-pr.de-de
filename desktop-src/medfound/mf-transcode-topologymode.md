---
description: Gibt für eine transcodetopologie an, ob das topologielader hardwarebasierte Transformationen lädt.
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: MF_TRANSCODE_TOPOLOGYMODE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f700397914faf7fee35e7f82027d8f8771e8b099
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863171"
---
# <a name="mf_transcode_topologymode-attribute"></a><span data-ttu-id="ed8ba-103">MF- \_ transcode- \_ topologymode-Attribut</span><span class="sxs-lookup"><span data-stu-id="ed8ba-103">MF\_TRANSCODE\_TOPOLOGYMODE attribute</span></span>

<span data-ttu-id="ed8ba-104">Gibt für eine transcodetopologie an, ob das topologielader hardwarebasierte Transformationen lädt.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-104">Specifies for a transcode topology whether the topology loader will load hardware-based transforms.</span></span>

<span data-ttu-id="ed8ba-105">Der topologiemodus gibt an, ob Hardware Transformationen (z. b. Hardware Codecs) in der transcodieren-Topologie verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-105">The topology mode specifies whether hardware transforms (such as hardware codecs) may be used in the transcode topology.</span></span> <span data-ttu-id="ed8ba-106">Die Anwendung kann dieses Attribut in einem transcodieren-Profil speichern, indem [**imftranscodeprofile:: setcontainerattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-106">The application can store this attribute in a transcode profile by calling [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span></span>

## <a name="data-type"></a><span data-ttu-id="ed8ba-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ed8ba-107">Data type</span></span>

<span data-ttu-id="ed8ba-108">**[**MF \_ Transcode- \_ topologymode- \_ Flags**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** , die als **UInt32** gespeichert sind</span><span class="sxs-lookup"><span data-stu-id="ed8ba-108">**[**MF\_TRANSCODE\_TOPOLOGYMODE\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="ed8ba-109">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="ed8ba-109">Get/set</span></span>

<span data-ttu-id="ed8ba-110">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ed8ba-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="ed8ba-111">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="ed8ba-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="ed8ba-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed8ba-112">Remarks</span></span>

<span data-ttu-id="ed8ba-113">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-113">This attribute is optional.</span></span> <span data-ttu-id="ed8ba-114">Er muss einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-114">It must have one of the following values.</span></span>



| <span data-ttu-id="ed8ba-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ed8ba-115">Value</span></span>                                              | <span data-ttu-id="ed8ba-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed8ba-116">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed8ba-117">**MF- \_ transcode- \_ topologymode- \_ Hardware \_ zulässig**</span><span class="sxs-lookup"><span data-stu-id="ed8ba-117">**MF\_TRANSCODE\_TOPOLOGYMODE\_HARDWARE\_ALLOWED**</span></span> | <span data-ttu-id="ed8ba-118">Das topologielader lädt hardwarebasierte MFTs (z. b. Hardware Decoder), wenn diese verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-118">The Topology Loader will load hardware-based MFTs, such as hardware decoders, when available.</span></span><br/> <span data-ttu-id="ed8ba-119">Das topologielader greift automatisch auf Software Decodierung zurück, wenn kein Hardware Decoder gefunden wird oder wenn ein Hardware Decoder aus irgendeinem Grund keine Verbindung herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-119">The Topology Loader automatically falls back to software decoding if no hardware decoder is found, or if a hardware decoder fails to connect for some reason.</span></span><br/> |
| <span data-ttu-id="ed8ba-120">**nur für die MF- \_ transcode- \_ topologymode- \_ Software \_**</span><span class="sxs-lookup"><span data-stu-id="ed8ba-120">**MF\_TRANSCODE\_TOPOLOGYMODE\_SOFTWARE\_ONLY**</span></span>    | <span data-ttu-id="ed8ba-121">Das topologielader lädt nur Software-MFTs, einschließlich Software Decoder.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-121">The Topology Loader will load only software MFTs, including software decoders.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="ed8ba-122">Der Standardwert ist **nur für die MF- \_ transcode- \_ topologymode- \_ Software \_**.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-122">The default value is **MF\_TRANSCODE\_TOPOLOGYMODE\_SOFTWARE\_ONLY**.</span></span>

<span data-ttu-id="ed8ba-123">Wenn das topologielader eine Hardware-MFT in die Topologie einfügt, wird das Attribut Attribut der [MFT- \_ Enum- \_ Hardware- \_ \_ URL](mft-enum-hardware-url-attribute.md) für den topologieknoten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-123">If the Topology Loader inserts a hardware MFT into the topology, it sets the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the topology node.</span></span> <span data-ttu-id="ed8ba-124">Um zu überprüfen, ob eine Hardware-MFT vorhanden ist, müssen Sie die Knoten in der aufgelösten Topologie auflisten und überprüfen, ob dieses Attribut vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-124">To check whether a hardware MFT is present, enumerate the nodes in the resolved topology and check whether this attribute is present.</span></span>

<span data-ttu-id="ed8ba-125">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-125">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed8ba-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed8ba-126">Requirements</span></span>



| <span data-ttu-id="ed8ba-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed8ba-127">Requirement</span></span> | <span data-ttu-id="ed8ba-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ed8ba-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed8ba-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed8ba-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ed8ba-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed8ba-130">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ed8ba-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed8ba-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ed8ba-132">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed8ba-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ed8ba-133">Header</span><span class="sxs-lookup"><span data-stu-id="ed8ba-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed8ba-134"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed8ba-134"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed8ba-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed8ba-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed8ba-136">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="ed8ba-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ed8ba-137">Transcode-API</span><span class="sxs-lookup"><span data-stu-id="ed8ba-137">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="ed8ba-138">**IMF transcodeprofile:: getcontainerattribute**</span><span class="sxs-lookup"><span data-stu-id="ed8ba-138">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[<span data-ttu-id="ed8ba-139">**IMF transcodeprofile:: setcontainerattribute**</span><span class="sxs-lookup"><span data-stu-id="ed8ba-139">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




