---
description: Gibt die CLSID eines Nachbearbeitungs-Plug-Ins für ein Video Erfassungsgerät an.
ms.assetid: 8F626FAA-C7B8-4DBA-BD65-7CE97CBF3A86
title: MF_DEVICESTREAM_EXTENSION_PLUGIN_CLSID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25c7ea9973b73cf6f1157eb19609293f2766d38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356519"
---
# <a name="mf_devicestream_extension_plugin_clsid-attribute"></a><span data-ttu-id="bfcb1-103">\_CLSID-Attribut "MF devicestream \_ Extension \_ Plugin \_ "</span><span class="sxs-lookup"><span data-stu-id="bfcb1-103">MF\_DEVICESTREAM\_EXTENSION\_PLUGIN\_CLSID attribute</span></span>

<span data-ttu-id="bfcb1-104">Gibt die CLSID eines Nachbearbeitungs-Plug-Ins für ein Video Erfassungsgerät an.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-104">Specifies the CLSID of a post-processing plug-in for a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="bfcb1-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bfcb1-105">Data type</span></span>

<span data-ttu-id="bfcb1-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="bfcb1-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="bfcb1-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfcb1-107">Remarks</span></span>

<span data-ttu-id="bfcb1-108">Ein nachträglich verarbeitetes Plug-in ist eine MFT, die das Video Bild nach der Erfassung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-108">A post-processing plug-in is an MFT that processes the video image after it is captured.</span></span> <span data-ttu-id="bfcb1-109">Der Hardwarehersteller kann ein nachträglich verarbeitetes Plug-in als Teil des Installationspakets einschließen.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-109">The hardware vendor can include a post-processing plug-in as part of the installation package.</span></span> <span data-ttu-id="bfcb1-110">Wenn dies der Fall ist, legt die Video Erfassungs Quelle das \_ CLSID-Attribut "MF devicestream \_ Extension \_ Plugin" \_ auf die CLSID des Plug-ins fest.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-110">If so, the video capture source sets the MF\_DEVICESTREAM\_EXTENSION\_PLUGIN\_CLSID attribute to the CLSID of the plug-in.</span></span>

<span data-ttu-id="bfcb1-111">Gehen Sie folgendermaßen vor, um dieses Attribut zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="bfcb1-111">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="bfcb1-112">Fragen Sie die Medienquelle für die [**imfmediasourceex**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-112">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="bfcb1-113">Aufrufen von [**imfmediasourceex:: getstreamattributs**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) , um einen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger für den Stream zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-113">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="bfcb1-114">Aufrufen Sie [**imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) , um das Attribut abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-114">Call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) to get the attribute.</span></span>

<span data-ttu-id="bfcb1-115">Um das Plug-in zu erstellen, rufen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)auf.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-115">To create the plug-in, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfcb1-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfcb1-116">Requirements</span></span>



| <span data-ttu-id="bfcb1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfcb1-117">Requirement</span></span> | <span data-ttu-id="bfcb1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="bfcb1-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bfcb1-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfcb1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bfcb1-120">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfcb1-120">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bfcb1-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfcb1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bfcb1-122">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfcb1-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bfcb1-123">Header</span><span class="sxs-lookup"><span data-stu-id="bfcb1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfcb1-124"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfcb1-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfcb1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfcb1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfcb1-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="bfcb1-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
