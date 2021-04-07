---
description: Gibt an, wie eine Media Foundation Transformation (MFT) einen Videodaten Strom mit 3D-Stereotyp ausgeben soll.
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: MF_ENABLE_3DVIDEO_OUTPUT-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0123a574ec74ed4aa9fa0aea3b2cabecbb29da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863591"
---
# <a name="mf_enable_3dvideo_output-attribute"></a><span data-ttu-id="a53e2-103">MF \_ \_ -Attribut "3dvideo-Ausgabe" aktivieren \_</span><span class="sxs-lookup"><span data-stu-id="a53e2-103">MF\_ENABLE\_3DVIDEO\_OUTPUT attribute</span></span>

<span data-ttu-id="a53e2-104">Gibt an, wie eine Media Foundation Transformation (MFT) einen Videodaten Strom mit 3D-Stereotyp ausgeben soll.</span><span class="sxs-lookup"><span data-stu-id="a53e2-104">Specifies how a Media Foundation transform (MFT) should output a 3D stereoscopic video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="a53e2-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a53e2-105">Data type</span></span>

<span data-ttu-id="a53e2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a53e2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a53e2-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a53e2-107">Remarks</span></span>

<span data-ttu-id="a53e2-108">Der Wert des-Attributs ist ein Member der [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="a53e2-108">The value of the attribute is a member of the [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) enumeration.</span></span>

<span data-ttu-id="a53e2-109">Dieses Attribut ist nur gültig, wenn die MFT-Eigenschaft für das [ \_ \_ 3dvideo-Attribut der MFT-Unterstützung](mft-support-3dvideo.md) **true** zurückgibt</span><span class="sxs-lookup"><span data-stu-id="a53e2-109">This attribute applies only if the MFT returns **TRUE** for the [MFT\_SUPPORT\_3DVIDEO](mft-support-3dvideo.md) attribute.</span></span>

<span data-ttu-id="a53e2-110">Zum Abrufen oder Festlegen dieses Attributs müssen Sie [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) aufrufen, um den globalen Attribut Speicher des MFT abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a53e2-110">To get or set this attribute call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="a53e2-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a53e2-111">Requirements</span></span>



| <span data-ttu-id="a53e2-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a53e2-112">Requirement</span></span> | <span data-ttu-id="a53e2-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a53e2-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a53e2-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a53e2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a53e2-115">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a53e2-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="a53e2-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a53e2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a53e2-117">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a53e2-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a53e2-118">Header</span><span class="sxs-lookup"><span data-stu-id="a53e2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a53e2-119"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a53e2-119"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a53e2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a53e2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a53e2-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a53e2-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




