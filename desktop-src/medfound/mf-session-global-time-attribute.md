---
description: Gibt an, ob Topologien eine globale Start-und Endzeit haben.
ms.assetid: 6810a22c-f091-423c-97dd-c04fdabdb9bb
title: MF_SESSION_GLOBAL_TIME-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b930ed47c5f314b12aba0075cdc9120d2179325
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362336"
---
# <a name="mf_session_global_time-attribute"></a><span data-ttu-id="5eb4c-103">\_ \_ Globales \_ Zeit Attribut der MF-Sitzung</span><span class="sxs-lookup"><span data-stu-id="5eb4c-103">MF\_SESSION\_GLOBAL\_TIME attribute</span></span>

<span data-ttu-id="5eb4c-104">Gibt an, ob Topologien eine globale Start-und Endzeit haben.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-104">Specifies whether topologies have a global start and stop time.</span></span>

## <a name="data-type"></a><span data-ttu-id="5eb4c-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5eb4c-105">Data type</span></span>

<span data-ttu-id="5eb4c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5eb4c-106">**UINT32**</span></span>

<span data-ttu-id="5eb4c-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5eb4c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5eb4c-108">Remarks</span></span>

<span data-ttu-id="5eb4c-109">Sie können dieses Attribut festlegen, wenn Sie das Medium "sesison" mit dem *pconfiguration* -Parameter der Funktion " [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) " oder " [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) " erstellen.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-109">You can set this attribute when you create the media sesison by using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="5eb4c-110">Wenn dieses Attribut vorhanden und ungleich NULL ist, müssen alle Topologien, die an die Medien Sitzung übermittelt werden, über das Projekt " [**MF \_ Topology \_ ProjectStart**](mf-topology-projectstart-attribute.md) " und " [**MF \_ Topology \_ projectstoppt**](mf-topology-projectstop-attribute.md) " verfügen.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-110">If this attribute is present and nonzero, then all topologies passed to the Media Session must have the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) and [**MF\_TOPOLOGY\_PROJECTSTOP**](mf-topology-projectstop-attribute.md) attributes.</span></span> <span data-ttu-id="5eb4c-111">Diese Attribute geben die Start-und Endzeit Zeiten für die Topologie relativ zur gesamten Präsentation an.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-111">These attributes specify the start and stop times for the topology relative to the entire presentation.</span></span>

<span data-ttu-id="5eb4c-112">Wenn dieses Attribut nicht vorhanden oder **falsch** ist, dürfen die Topologien nicht über das Projekt für die [**MF- \_ TopologieTopologie \_ ProjectStart**](mf-topology-projectstart-attribute.md) oder die [**MF- \_ Topologie \_ projectstoppt**](mf-topology-projectstop-attribute.md) verfügen.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-112">If this attribute is absent or **FALSE**, the topologies must not have the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) or [**MF\_TOPOLOGY\_PROJECTSTOP**](mf-topology-projectstop-attribute.md) attribute.</span></span>

<span data-ttu-id="5eb4c-113">Verwenden Sie dieses Attribut, um Bearbeitungs Sequenzen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-113">Use this attribute to create editing sequences.</span></span> <span data-ttu-id="5eb4c-114">Weitere Informationen finden Sie unter [Sequenz Präsentations Zeiten](sequence-presentation-times.md).</span><span class="sxs-lookup"><span data-stu-id="5eb4c-114">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="5eb4c-115">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eb4c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5eb4c-116">Requirements</span></span>



| <span data-ttu-id="5eb4c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5eb4c-117">Requirement</span></span> | <span data-ttu-id="5eb4c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5eb4c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5eb4c-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5eb4c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5eb4c-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5eb4c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5eb4c-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5eb4c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5eb4c-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5eb4c-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5eb4c-123">Header</span><span class="sxs-lookup"><span data-stu-id="5eb4c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5eb4c-124"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5eb4c-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eb4c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5eb4c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eb4c-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="5eb4c-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5eb4c-127">Medien Sitzungs Attribute</span><span class="sxs-lookup"><span data-stu-id="5eb4c-127">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="5eb4c-128">Sequenz Präsentations Zeiten</span><span class="sxs-lookup"><span data-stu-id="5eb4c-128">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="5eb4c-129">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5eb4c-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5eb4c-130">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5eb4c-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5eb4c-131">**MF- \_ Topologie \_ ProjectStart**</span><span class="sxs-lookup"><span data-stu-id="5eb4c-131">**MF\_TOPOLOGY\_PROJECTSTART**</span></span>](mf-topology-projectstart-attribute.md)
</dt> <dt>

[<span data-ttu-id="5eb4c-132">**MF- \_ Topologie \_ projectstoppt**</span><span class="sxs-lookup"><span data-stu-id="5eb4c-132">**MF\_TOPOLOGY\_PROJECTSTOP**</span></span>](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




