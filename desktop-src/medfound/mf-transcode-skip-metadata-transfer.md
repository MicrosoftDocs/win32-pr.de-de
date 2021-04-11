---
description: Gibt an, ob Metadaten in die transcodierte Datei geschrieben werden.
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: MF_TRANSCODE_SKIP_METADATA_TRANSFER-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54978d76ec1392c3be731e1452a653d1423976a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214879"
---
# <a name="mf_transcode_skip_metadata_transfer-attribute"></a><span data-ttu-id="7d968-103">MF- \_ transcode \_ Skip- \_ \_ metadatenübertragungs-Attribut</span><span class="sxs-lookup"><span data-stu-id="7d968-103">MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER attribute</span></span>

<span data-ttu-id="7d968-104">Gibt an, ob Metadaten in die transcodierte Datei geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7d968-104">Specifies whether metadata is written to the transcoded file.</span></span> <span data-ttu-id="7d968-105">Dieses Container Attribut wird im transcodieren-Profil gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7d968-105">This container attribute is stored in the transcode profile.</span></span>

## <a name="data-type"></a><span data-ttu-id="7d968-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7d968-106">Data type</span></span>

<span data-ttu-id="7d968-107">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7d968-107">**UINT32**</span></span>

<span data-ttu-id="7d968-108">Mögliche Werte für das MF \_ transcode \_ Skip \_ - \_ metadatenübertragungs-Attribut werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7d968-108">Possible values for the MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER attribute are described in the following table.</span></span>



| <span data-ttu-id="7d968-109">Wert</span><span class="sxs-lookup"><span data-stu-id="7d968-109">Value</span></span>                                                                        | <span data-ttu-id="7d968-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7d968-110">Meaning</span></span>                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7d968-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7d968-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="7d968-112">Überträgt automatisch Metadaten auf Dateiebene aus der Quelldatei in die transcodierte Datei.</span><span class="sxs-lookup"><span data-stu-id="7d968-112">Automatically transfers file-level metadata from the source file to the transcoded file.</span></span><br/> |
| <dl> <span data-ttu-id="7d968-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7d968-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="7d968-114">Die Metadaten der Quelldatei werden nicht in die transcodierten Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="7d968-114">The source file metadata is not written to the transcoded file.</span></span><br/>                          |



 

## <a name="getset"></a><span data-ttu-id="7d968-115">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="7d968-115">Get/set</span></span>

<span data-ttu-id="7d968-116">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="7d968-116">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7d968-117">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="7d968-117">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="7d968-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d968-118">Remarks</span></span>

<span data-ttu-id="7d968-119">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="7d968-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d968-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d968-120">Requirements</span></span>



| <span data-ttu-id="7d968-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d968-121">Requirement</span></span> | <span data-ttu-id="7d968-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7d968-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7d968-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d968-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7d968-124">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d968-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7d968-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d968-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7d968-126">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d968-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7d968-127">Header</span><span class="sxs-lookup"><span data-stu-id="7d968-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d968-128"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d968-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d968-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d968-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d968-130">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="7d968-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7d968-131">**IMF transcodeprofile:: getcontainerattribute**</span><span class="sxs-lookup"><span data-stu-id="7d968-131">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[<span data-ttu-id="7d968-132">**IMF transcodeprofile:: setcontainerattribute**</span><span class="sxs-lookup"><span data-stu-id="7d968-132">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




