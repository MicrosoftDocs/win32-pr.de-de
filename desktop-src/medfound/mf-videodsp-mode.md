---
description: Legt den Verarbeitungsmodus der Videostabilisierung MFT fest.
ms.assetid: 0D49892A-8628-4F2B-B41B-51160A19DC9B
title: MF_VIDEODSP_MODE-Attribut (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88383e6bdd197e4912c660657eefa6b9e812fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130128"
---
# <a name="mf_videodsp_mode-attribute"></a><span data-ttu-id="08bde-103">MF \_ videodsp \_ mode-Attribut</span><span class="sxs-lookup"><span data-stu-id="08bde-103">MF\_VIDEODSP\_MODE attribute</span></span>

<span data-ttu-id="08bde-104">Legt den Verarbeitungsmodus der [**Videostabilisierung MFT**](video-stabilization-mft.md)fest.</span><span class="sxs-lookup"><span data-stu-id="08bde-104">Sets the processing mode of the [**Video Stabilization MFT**](video-stabilization-mft.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="08bde-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="08bde-105">Data type</span></span>

<span data-ttu-id="08bde-106">**MF videodspmode** gespeichert als **UIINT32**</span><span class="sxs-lookup"><span data-stu-id="08bde-106">**MFVideoDSPMode** stored as **UIINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="08bde-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08bde-107">Remarks</span></span>

<span data-ttu-id="08bde-108">Der Wert dieses Attributs ist ein [**MF videodspmode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) -Enumerationswert.</span><span class="sxs-lookup"><span data-stu-id="08bde-108">The value of this attribute is an [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) enumeration value.</span></span> <span data-ttu-id="08bde-109">Dieses Attribut kann verwendet werden, um die Bildstabilisierung zu aktivieren oder zu deaktivieren, und kann für jedes Ausgabe Beispiel aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="08bde-109">This attribute can be used to enable or disable the image stabilization, and can be updated for each output sample.</span></span>

<span data-ttu-id="08bde-110">So legen Sie dieses Attribut fest:</span><span class="sxs-lookup"><span data-stu-id="08bde-110">To set this attribute:</span></span>

1.  <span data-ttu-id="08bde-111">Aufrufen von [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) auf der Video Stabilisierungs-MFT, um einen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="08bde-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video stabilization MFT to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="08bde-112">Zum Festlegen des-Attributs wird [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="08bde-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to set the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="08bde-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08bde-113">Requirements</span></span>



| <span data-ttu-id="08bde-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08bde-114">Requirement</span></span> | <span data-ttu-id="08bde-115">Wert</span><span class="sxs-lookup"><span data-stu-id="08bde-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08bde-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08bde-116">Minimum supported client</span></span><br/> | <span data-ttu-id="08bde-117">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08bde-117">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="08bde-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08bde-118">Minimum supported server</span></span><br/> | <span data-ttu-id="08bde-119">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08bde-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="08bde-120">Header</span><span class="sxs-lookup"><span data-stu-id="08bde-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="08bde-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="08bde-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08bde-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08bde-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08bde-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="08bde-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="08bde-124">**Videostabilisierung-MFT**</span><span class="sxs-lookup"><span data-stu-id="08bde-124">**Video Stabilization MFT**</span></span>](video-stabilization-mft.md)
</dt> </dl>

 

 




