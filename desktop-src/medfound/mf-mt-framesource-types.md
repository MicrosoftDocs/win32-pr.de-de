---
description: Ein-Wert, der den Typ des Sensors angibt, der von einer Frame Quelle bereitgestellt wird, z. b. Farbe, Infrarot oder Tiefe.
ms.assetid: F327B9E9-C01C-4F5B-9A26-6404ECD7F27F
title: MF_MT_FRAMESOURCE_TYPES-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4475d66aea245ac9295a7996da2c37cabdb9627
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343779"
---
# <a name="mf_mt_framesource_types-attribute"></a><span data-ttu-id="04e05-103">Attribut "MF \_ MT \_ framesource \_ types"</span><span class="sxs-lookup"><span data-stu-id="04e05-103">MF\_MT\_FRAMESOURCE\_TYPES attribute</span></span>

<span data-ttu-id="04e05-104">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="04e05-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="04e05-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="04e05-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="04e05-106">Ein-Wert, der den Typ des Sensors angibt, der von einer Frame Quelle bereitgestellt wird, z. b. Farbe, Infrarot oder Tiefe.</span><span class="sxs-lookup"><span data-stu-id="04e05-106">A value that indicates the type of sensor provided by a frame source, such as color, infrared, or depth.</span></span>

## <a name="data-type"></a><span data-ttu-id="04e05-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="04e05-107">Data type</span></span>

<span data-ttu-id="04e05-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="04e05-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="04e05-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04e05-109">Remarks</span></span>

<span data-ttu-id="04e05-110">Dieser Wert muss ein Member der [**\_ mfframesourcetypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) -Enumeration sein.</span><span class="sxs-lookup"><span data-stu-id="04e05-110">This value should be a member of the [**\_MFFrameSourceTypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) enumeration.</span></span> <span data-ttu-id="04e05-111">Wenn dieses Attribut nicht für einen Medientyp definiert ist, wird aus Gründen der Abwärtskompatibilität angenommen, dass es **\_ mfframesourcetyes:: Color** ist.</span><span class="sxs-lookup"><span data-stu-id="04e05-111">For backward compatibility, when this attribute is not defined on a media type, it's assumed to be **\_MFFrameSourceTyes::Color**.</span></span>

## <a name="requirements"></a><span data-ttu-id="04e05-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04e05-112">Requirements</span></span>



| <span data-ttu-id="04e05-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04e05-113">Requirement</span></span> | <span data-ttu-id="04e05-114">Wert</span><span class="sxs-lookup"><span data-stu-id="04e05-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04e05-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04e05-115">Minimum supported client</span></span><br/> | <span data-ttu-id="04e05-116">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04e05-116">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="04e05-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04e05-117">Minimum supported server</span></span><br/> | <span data-ttu-id="04e05-118">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04e05-118">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="04e05-119">Header</span><span class="sxs-lookup"><span data-stu-id="04e05-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="04e05-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="04e05-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
