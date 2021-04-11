---
description: Ruft den Verdienst Wert eines Hardware Codecs ab.
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: OPM_GET_CODEC_INFO (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf310ae3dafee7823119b2d5d5bd2c6b61fe822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215028"
---
# <a name="opm_get_codec_info"></a><span data-ttu-id="67947-103">OPM- \_ get- \_ Codec- \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="67947-103">OPM\_GET\_CODEC\_INFO</span></span>

<span data-ttu-id="67947-104">Ruft den Verdienst Wert eines Hardware Codecs ab.</span><span class="sxs-lookup"><span data-stu-id="67947-104">Gets the merit value of a hardware codec.</span></span>



| <span data-ttu-id="67947-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67947-105">Requirement</span></span> | <span data-ttu-id="67947-106">Wert</span><span class="sxs-lookup"><span data-stu-id="67947-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="67947-107">Anforderungs-GUID</span><span class="sxs-lookup"><span data-stu-id="67947-107">Request GUID</span></span> | <span data-ttu-id="67947-108">**OPM- \_ get- \_ Codec- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="67947-108">**OPM\_GET\_CODEC\_INFO**</span></span>                                                                 |
| <span data-ttu-id="67947-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="67947-109">Input data</span></span>   | <span data-ttu-id="67947-110">Eine [**OPM- \_ get \_ Codec \_ Info \_ Parameters**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) -Struktur</span><span class="sxs-lookup"><span data-stu-id="67947-110">An [**OPM\_GET\_CODEC\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) structure</span></span>   |
| <span data-ttu-id="67947-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="67947-111">Return data</span></span>  | <span data-ttu-id="67947-112">Eine [**OPM- \_ get- \_ Codec- \_ \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) Struktur</span><span class="sxs-lookup"><span data-stu-id="67947-112">An [**OPM\_GET\_CODEC\_INFO\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="67947-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67947-113">Remarks</span></span>

<span data-ttu-id="67947-114">Obwohl dieser Befehl die Schnittstelle des [Output Protection Managers](output-protection-manager.md) (OPM) verwendet, gilt er nur für Hardware Encoder und-Decoder.</span><span class="sxs-lookup"><span data-stu-id="67947-114">Although this command uses the [Output Protection Manager](output-protection-manager.md) (OPM) interface, it applies only to hardware encoders and decoders.</span></span> <span data-ttu-id="67947-115">Dies gilt nicht für Videoausgabe Geräte.</span><span class="sxs-lookup"><span data-stu-id="67947-115">It does not apply to video output devices.</span></span>

<span data-ttu-id="67947-116">Im Allgemeinen sollten Sie diesen Befehl nicht direkt verwenden.</span><span class="sxs-lookup"><span data-stu-id="67947-116">Generally, you should not use this command directly.</span></span> <span data-ttu-id="67947-117">Um den Wert für einen Hardwarecodec zu erhalten, müssen Sie die Funktion [**mfgetmftmerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="67947-117">To get the merit value for a hardware codec, call the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function.</span></span> <span data-ttu-id="67947-118">Diese Funktion führt alle OPM-Aufrufe aus, die erforderlich sind, um den **OPM \_ get \_ Codec \_ Info** -Befehl zu senden.</span><span class="sxs-lookup"><span data-stu-id="67947-118">This function performs all of the OPM calls needed to send the **OPM\_GET\_CODEC\_INFO** command.</span></span>

## <a name="requirements"></a><span data-ttu-id="67947-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67947-119">Requirements</span></span>



| <span data-ttu-id="67947-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67947-120">Requirement</span></span> | <span data-ttu-id="67947-121">Wert</span><span class="sxs-lookup"><span data-stu-id="67947-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="67947-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67947-122">Minimum supported client</span></span><br/> | <span data-ttu-id="67947-123">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67947-123">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="67947-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67947-124">Minimum supported server</span></span><br/> | <span data-ttu-id="67947-125">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67947-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="67947-126">Header</span><span class="sxs-lookup"><span data-stu-id="67947-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="67947-127"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="67947-127"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67947-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67947-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67947-129">OPM-Status Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67947-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> <dt>

[<span data-ttu-id="67947-130">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="67947-130">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> <dt>

[<span data-ttu-id="67947-131">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="67947-131">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 




