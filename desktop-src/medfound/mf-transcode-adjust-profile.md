---
description: Profilflags, die die streameinstellungen für die transcodieren-Topologie definieren. Die Flags werden in der MF- \_ Enumeration für das transcodeanpassungsecodeumeration definiert \_ \_ \_ .
ms.assetid: 6782e080-284b-458d-8bc0-6e131a529e7b
title: MF_TRANSCODE_ADJUST_PROFILE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd492cfc7981ca1a36a1cb54a440bec4783fe1b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348829"
---
# <a name="mf_transcode_adjust_profile-attribute"></a><span data-ttu-id="84041-104">MF- \_ transcode- \_ Anpassungs \_ Profil Attribut</span><span class="sxs-lookup"><span data-stu-id="84041-104">MF\_TRANSCODE\_ADJUST\_PROFILE attribute</span></span>

<span data-ttu-id="84041-105">Profilflags, die die streameinstellungen für die transcodieren-Topologie definieren.</span><span class="sxs-lookup"><span data-stu-id="84041-105">Profile flags that define the stream settings for the transcode topology.</span></span> <span data-ttu-id="84041-106">Die Flags werden in der MF-Enumeration für das [**\_ \_ \_ \_ transcodeanpassungsecodeumeration**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) definiert.</span><span class="sxs-lookup"><span data-stu-id="84041-106">The flags are defined in the [**MF\_TRANSCODE\_ADJUST\_PROFILE\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) enumeration.</span></span>

## <a name="data-type"></a><span data-ttu-id="84041-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="84041-107">Data type</span></span>

<span data-ttu-id="84041-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="84041-108">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="84041-109">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="84041-109">Get/set</span></span>

<span data-ttu-id="84041-110">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="84041-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="84041-111">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="84041-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="84041-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84041-112">Remarks</span></span>

<span data-ttu-id="84041-113">Eine Anwendung kann dieses Attribut auf Container Ebene für das transcodieren-Profil festlegen.</span><span class="sxs-lookup"><span data-stu-id="84041-113">An application can set this attribute at the container level on the transcode profile.</span></span> <span data-ttu-id="84041-114">Wenn dieses Attribut festgelegt ist, ändert die MF-Funktion die Stream-Attribute bei der [**topologiebildung**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) abhängig vom angegebenen Flag.</span><span class="sxs-lookup"><span data-stu-id="84041-114">If this attribute is set, the [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function changes the stream attributes during topology building, depending on the specified flag.</span></span> <span data-ttu-id="84041-115">Wenn die Anwendung z. b. das kennflag für das **MF- \_ transcode- \_ Anpassungs \_ Profil \_** angibt, werden die von der Anwendung angegebenen streameinstellungen verwendet, um das Profil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84041-115">For example, if the application specifies the **MF\_TRANSCODE\_ADJUST\_PROFILE\_DEFAULT** flag, the application-specified stream settings are used to create the profile.</span></span>

<span data-ttu-id="84041-116">Für den Videostream wird die Framerate basierend auf der Medienquelle aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="84041-116">For the video stream, the frame rate is updated based on the media source.</span></span> <span data-ttu-id="84041-117">Wenn die Anwendung den Zeilen Sprung Modus nicht angibt, wird das Profil so aktualisiert, dass standardmäßig progressive Frames verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84041-117">If the application does not specify the interlaced mode, the profile is updated to use progressive frames by default.</span></span>

<span data-ttu-id="84041-118">Wenn in der Anwendung das Flag für die **\_ Verwendung der \_ \_ \_ \_ Quell \_ Attribute für das MF-transcodieren-Profil** angegeben ist, werden fehlende Datenstrom Attribute aus der Eingabemedien Quelle in die streameinstellungen im transcodieren-Profil kopiert.</span><span class="sxs-lookup"><span data-stu-id="84041-118">If the application specifies the **MF\_TRANSCODE\_ADJUST\_PROFILE\_USE\_SOURCE\_ATTRIBUTES** flag, then missing stream attributes are copied from the input media source to the stream settings in the transcode profile.</span></span>

<span data-ttu-id="84041-119">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="84041-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="84041-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84041-120">Requirements</span></span>



| <span data-ttu-id="84041-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84041-121">Requirement</span></span> | <span data-ttu-id="84041-122">Wert</span><span class="sxs-lookup"><span data-stu-id="84041-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="84041-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84041-123">Minimum supported client</span></span><br/> | <span data-ttu-id="84041-124">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84041-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="84041-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84041-125">Minimum supported server</span></span><br/> | <span data-ttu-id="84041-126">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84041-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="84041-127">Header</span><span class="sxs-lookup"><span data-stu-id="84041-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="84041-128"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="84041-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84041-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84041-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84041-130">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="84041-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="84041-131">Transcode-API</span><span class="sxs-lookup"><span data-stu-id="84041-131">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="84041-132">**IMF transcodeprofile:: setcontainerattribute**</span><span class="sxs-lookup"><span data-stu-id="84041-132">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




