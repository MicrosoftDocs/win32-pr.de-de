---
description: Stellt eine Rückruf Schnittstelle bereit, damit die Anwendung ein Content Wegbereiter-Objekt von der PMP-Sitzung (Protected Media Path) empfängt.
ms.assetid: 66482541-63d4-439b-862f-7507605af5d8
title: MF_SESSION_CONTENT_PROTECTION_MANAGER-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90321ae3c10fd7fa2ec39a4fb478e256291b049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347493"
---
# <a name="mf_session_content_protection_manager-attribute"></a><span data-ttu-id="3ddc9-103">MF- \_ Sitzungs \_ Inhalts Schutz-Manager- \_ \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="3ddc9-103">MF\_SESSION\_CONTENT\_PROTECTION\_MANAGER attribute</span></span>

<span data-ttu-id="3ddc9-104">Stellt eine Rückruf Schnittstelle bereit, damit die Anwendung ein Content Wegbereiter-Objekt von der PMP-Sitzung (Protected Media Path) empfängt.</span><span class="sxs-lookup"><span data-stu-id="3ddc9-104">Provides a callback interface for the application to receive a content enabler object from the protected media path (PMP) session.</span></span>

## <a name="data-type"></a><span data-ttu-id="3ddc9-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3ddc9-105">Data type</span></span>

<span data-ttu-id="3ddc9-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="3ddc9-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="3ddc9-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ddc9-107">Remarks</span></span>

<span data-ttu-id="3ddc9-108">Der Wert dieses Attributs ist ein Zeiger auf die [_ *imfcontentschutzmanager* \*](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) -Schnittstelle der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3ddc9-108">The value of this attribute is a pointer to the application's [_ *IMFContentProtectionManager*\*](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

<span data-ttu-id="3ddc9-109">Legen Sie dieses Attribut für die PMP-Sitzung fest, indem Sie den *pconfiguration* -Parameter der [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ddc9-109">Set this attribute on the PMP session by using the *pConfiguration* parameter of the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="3ddc9-110">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="3ddc9-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ddc9-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ddc9-111">Requirements</span></span>



| <span data-ttu-id="3ddc9-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ddc9-112">Requirement</span></span> | <span data-ttu-id="3ddc9-113">Wert</span><span class="sxs-lookup"><span data-stu-id="3ddc9-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3ddc9-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ddc9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3ddc9-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ddc9-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3ddc9-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ddc9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3ddc9-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ddc9-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3ddc9-118">Header</span><span class="sxs-lookup"><span data-stu-id="3ddc9-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ddc9-119"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ddc9-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ddc9-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ddc9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ddc9-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="3ddc9-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3ddc9-122">**Imfattributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="3ddc9-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="3ddc9-123">\**Imfattributes:: *-Known**</span><span class="sxs-lookup"><span data-stu-id="3ddc9-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="3ddc9-124">Medien Sitzungs Attribute</span><span class="sxs-lookup"><span data-stu-id="3ddc9-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="3ddc9-125">Wiedergeben geschützter Mediendateien</span><span class="sxs-lookup"><span data-stu-id="3ddc9-125">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)
</dt> </dl>

 

 




