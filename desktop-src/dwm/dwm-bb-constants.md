---
title: DWM-weich-hinter Konstanten (dwmapi. h)
description: Flags, die von der DWM- \_ blurbehind-Struktur verwendet werden, um anzugeben, welche der Member gültige Informationen enthalten.
ms.assetid: d6dd552c-1f3b-4f16-8705-f5016ed55d9e
topic_type:
- apiref
api_name:
- DWM_BB_ENABLE
- DWM_BB_BLURREGION
- DWM_BB_TRANSITIONONMAXIMIZED
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe08e0315d4c4b906cdb897ac7ad5dd34d50fbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518131"
---
# <a name="dwm-blur-behind-constants"></a><span data-ttu-id="60911-103">DWM-weich-hinter Konstanten</span><span class="sxs-lookup"><span data-stu-id="60911-103">DWM Blur Behind Constants</span></span>

<span data-ttu-id="60911-104">Flags, die von der [**DWM- \_ blurbehind**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) -Struktur verwendet werden, um anzugeben, welche der Member gültige Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="60911-104">Flags used by the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure to indicate which of its members contain valid information.</span></span>

<dl> <dt>

<span data-ttu-id="60911-105"><span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**Aktivieren von DWM \_ BB \_**</span><span class="sxs-lookup"><span data-stu-id="60911-105"><span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**DWM\_BB\_ENABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60911-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="60911-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="60911-107">Es wurde ein Wert für das festleg **Bare** Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="60911-107">A value for the **fEnable** member has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="60911-108"><span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**DWM \_ BB- \_ Blur-Region**</span><span class="sxs-lookup"><span data-stu-id="60911-108"><span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**DWM\_BB\_BLURREGION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60911-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="60911-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="60911-110">Ein Wert für den **hRgnBlur** -Member wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="60911-110">A value for the **hRgnBlur** member has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="60911-111"><span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**DWM \_ BB \_ transitiononmaximized**</span><span class="sxs-lookup"><span data-stu-id="60911-111"><span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**DWM\_BB\_TRANSITIONONMAXIMIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60911-112">0x00000004</span><span class="sxs-lookup"><span data-stu-id="60911-112">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="60911-113">Ein Wert für den Member " **fTransitionOnMaximized** " wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="60911-113">A value for the **fTransitionOnMaximized** member has been specified.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60911-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60911-114">Requirements</span></span>



| <span data-ttu-id="60911-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60911-115">Requirement</span></span> | <span data-ttu-id="60911-116">Wert</span><span class="sxs-lookup"><span data-stu-id="60911-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="60911-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60911-117">Minimum supported client</span></span><br/> | <span data-ttu-id="60911-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60911-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="60911-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60911-119">Minimum supported server</span></span><br/> | <span data-ttu-id="60911-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60911-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="60911-121">Header</span><span class="sxs-lookup"><span data-stu-id="60911-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="60911-122"><dt>Dwmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="60911-122"><dt>Dwmapi.h</dt></span></span> </dl> |



 

 





