---
title: Wtnca-Werte (uxtheme. h)
description: Gibt Flags an, die visuelle Fenster Stil Attribute ändern. Verwenden Sie eine oder eine bitweise Kombination der folgenden Werte.
ms.assetid: C71D1957-6572-4242-B715-C54BDFBBD6B7
topic_type:
- apiref
api_name:
- WTNCA_NODRAWCAPTION
- WTNCA_NODRAWICON
- WTNCA_NOSYSMENU
- WTNCA_NOMIRRORHELP
- WTNCA_VALIDBITS
api_location:
- Uxtheme.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaf543b688d0b403962da43029ac9aa85422bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105939"
---
# <a name="wtnca-values"></a><span data-ttu-id="7c065-104">Wtnca-Werte</span><span class="sxs-lookup"><span data-stu-id="7c065-104">WTNCA Values</span></span>

<span data-ttu-id="7c065-105">Gibt Flags an, die visuelle Fenster Stil Attribute ändern.</span><span class="sxs-lookup"><span data-stu-id="7c065-105">Specifies flags that modify window visual style attributes.</span></span> <span data-ttu-id="7c065-106">Verwenden Sie eine oder eine bitweise Kombination der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="7c065-106">Use one, or a bitwise combination of the following values.</span></span>



| <span data-ttu-id="7c065-107">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="7c065-107">Constant/value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="7c065-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c065-108">Description</span></span>                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="WTNCA_NODRAWCAPTION"></span><span id="wtnca_nodrawcaption"></span><dl> <span data-ttu-id="7c065-109"><dt>**Wtnca \_ Nodrawcaption**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="7c065-109"><dt>**WTNCA\_NODRAWCAPTION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="7c065-110">Verhindert, dass die Beschriftung des Fensters gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="7c065-110">Prevents the window caption from being drawn.</span></span><br/>                                |
| <span id="WTNCA_NODRAWICON"></span><span id="wtnca_nodrawicon"></span><dl> <span data-ttu-id="7c065-111"><dt>**Wtnca \_ Nodrawicon**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="7c065-111"><dt>**WTNCA\_NODRAWICON**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="7c065-112">Verhindert, dass das System Symbol gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="7c065-112">Prevents the system icon from being drawn.</span></span><br/>                                   |
| <span id="WTNCA_NOSYSMENU"></span><span id="wtnca_nosysmenu"></span><dl> <span data-ttu-id="7c065-113"><dt>**Wtnca \_ Nosysmenu**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="7c065-113"><dt>**WTNCA\_NOSYSMENU**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="7c065-114">Verhindert, dass das System Symbolmenü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7c065-114">Prevents the system icon menu from appearing.</span></span><br/>                                |
| <span id="WTNCA_NOMIRRORHELP"></span><span id="wtnca_nomirrorhelp"></span><dl> <span data-ttu-id="7c065-115"><dt>**Wtnca \_ Nomirrorhelp**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="7c065-115"><dt>**WTNCA\_NOMIRRORHELP**</dt> <dt>0x00000008</dt></span></span> </dl>    | <span data-ttu-id="7c065-116">Verhindert die Spiegelung des Fragezeichens, auch in einem Layout von rechts nach links (RTL).</span><span class="sxs-lookup"><span data-stu-id="7c065-116">Prevents mirroring of the question mark, even in right-to-left (RTL) layout.</span></span><br/> |
| <span id="WTNCA_VALIDBITS"></span><span id="wtnca_validbits"></span><dl> <span data-ttu-id="7c065-117"><dt>**wtnca- \_ validbits**</dt></span><span class="sxs-lookup"><span data-stu-id="7c065-117"><dt>**WTNCA\_VALIDBITS**</dt></span></span> </dl>                                                                             | <span data-ttu-id="7c065-118">Eine Maske, die alle gültigen Bits enthält.</span><span class="sxs-lookup"><span data-stu-id="7c065-118">A mask that contains all the valid bits.</span></span><br/>                                     |



## <a name="requirements"></a><span data-ttu-id="7c065-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c065-119">Requirements</span></span>



| <span data-ttu-id="7c065-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c065-120">Requirement</span></span> | <span data-ttu-id="7c065-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7c065-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7c065-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c065-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7c065-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c065-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7c065-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c065-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7c065-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c065-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7c065-126">Header</span><span class="sxs-lookup"><span data-stu-id="7c065-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c065-127"><dt>Uxtheme. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c065-127"><dt>Uxtheme.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c065-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c065-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c065-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="7c065-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7c065-130">**WTA- \_ Optionen**</span><span class="sxs-lookup"><span data-stu-id="7c065-130">**WTA\_OPTIONS**</span></span>](/windows/desktop/api/Uxtheme/ns-uxtheme-wta_options)
</dt> <dt>

[<span data-ttu-id="7c065-131">**Setwindowthemumonclientattribute**</span><span class="sxs-lookup"><span data-stu-id="7c065-131">**SetWindowThemeNonClientAttributes**</span></span>](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowthemenonclientattributes)
</dt> </dl>

 

 





