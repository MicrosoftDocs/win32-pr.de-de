---
description: Gibt an, ob der Alpha Modus für Farb Medien-Video Typen vorab multipliziert oder gerade ist.
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: MF_MT_ALPHA_MODE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06b81da14bc0a9e089a5af4815e5bf97359a9cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042339"
---
# <a name="mf_mt_alpha_mode-attribute"></a><span data-ttu-id="06d5a-103">MF- \_ MT- \_ Alpha Mode- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="06d5a-103">MF\_MT\_ALPHA\_MODE attribute</span></span>

<span data-ttu-id="06d5a-104">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="06d5a-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="06d5a-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="06d5a-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="06d5a-106">Gibt an, ob der Alpha Modus für Farb Medien-Video Typen vorab multipliziert oder gerade ist.</span><span class="sxs-lookup"><span data-stu-id="06d5a-106">Specifies whether the alpha mode for color media video types is premultiplied or straight.</span></span>

## <a name="data-type"></a><span data-ttu-id="06d5a-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="06d5a-107">Data type</span></span>

<span data-ttu-id="06d5a-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="06d5a-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="06d5a-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06d5a-109">Remarks</span></span>

<span data-ttu-id="06d5a-110">Dieser Wert kann in einen Wert für den [**DXGI- \_ alpha \_ Modus**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="06d5a-110">This value can be cast to a [**DXGI\_ALPHA\_MODE**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) value.</span></span> <span data-ttu-id="06d5a-111">Wenn dieses Attribut nicht vorhanden ist, ist der Wert aus Gründen der Abwärtskompatibilität der **DXGI- \_ alpha- \_ Modus \_ direkt** für das Videoformat, der Alphakanal unterstützt, z. b. ARGB32, oder der **DXGI- \_ alpha \_ Modus \_ Ignore** für das Videoformat ohne Alphakanal, z. b.</span><span class="sxs-lookup"><span data-stu-id="06d5a-111">If this attribute isn’t present, for backward compatibility, the value is **DXGI\_ALPHA\_MODE\_STRAIGHT** for video format supporting alpha channel, such as ARGB32, or **DXGI\_ALPHA\_MODE\_IGNORE** for video format without alpha channel, such as RGB32.</span></span>

## <a name="requirements"></a><span data-ttu-id="06d5a-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06d5a-112">Requirements</span></span>



| <span data-ttu-id="06d5a-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06d5a-113">Requirement</span></span> | <span data-ttu-id="06d5a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="06d5a-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="06d5a-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06d5a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="06d5a-116">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06d5a-116">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="06d5a-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06d5a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="06d5a-118">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06d5a-118">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="06d5a-119">Header</span><span class="sxs-lookup"><span data-stu-id="06d5a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="06d5a-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="06d5a-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
