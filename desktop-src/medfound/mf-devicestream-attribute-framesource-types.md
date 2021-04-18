---
description: Stellt den Rahmen Quelltyp dar.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8823a828a81290fe3b039c8959d694c62331622f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357452"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a><span data-ttu-id="eaf1f-103">Attribut für das MF- \_ \_ Attribut " \_ framesource" \_</span><span class="sxs-lookup"><span data-stu-id="eaf1f-103">MF\_DEVICESTREAM\_ATTRIBUTE\_FRAMESOURCE\_TYPES attribute</span></span>

<span data-ttu-id="eaf1f-104">Stellt den Rahmen Quelltyp dar.</span><span class="sxs-lookup"><span data-stu-id="eaf1f-104">Represents the frame source type.</span></span>

## <a name="data-type"></a><span data-ttu-id="eaf1f-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="eaf1f-105">Data type</span></span>

<span data-ttu-id="eaf1f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="eaf1f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="eaf1f-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eaf1f-107">Remarks</span></span>

<span data-ttu-id="eaf1f-108">Dieser Wert dieses Attributs muss eine Bitmaske von einem oder mehreren Werten aus der Enumeration " [**mfframesourcetypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) " sein.</span><span class="sxs-lookup"><span data-stu-id="eaf1f-108">This value of this attribute should be a bitmask of one or more values from the [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) enumeration.</span></span> <span data-ttu-id="eaf1f-109">Wenn dieses Attribut nicht für einen Medientyp definiert ist, wird angenommen, dass es den Wert **mfframesourcetypes:: Color** hat, um die Abwärtskompatibilität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="eaf1f-109">To support backward compatibility, when this attribute is not defined for a media type, it is assumed to have the value **MFFrameSourceTypes::Color**.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaf1f-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eaf1f-110">Requirements</span></span>



| <span data-ttu-id="eaf1f-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eaf1f-111">Requirement</span></span> | <span data-ttu-id="eaf1f-112">Wert</span><span class="sxs-lookup"><span data-stu-id="eaf1f-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf1f-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eaf1f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="eaf1f-114">Windows 10, Version 1607, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eaf1f-114">Windows 10, version 1607 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="eaf1f-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eaf1f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="eaf1f-116">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eaf1f-116">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="eaf1f-117">Header</span><span class="sxs-lookup"><span data-stu-id="eaf1f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaf1f-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaf1f-118"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




