---
title: Benutzerdefinierte Zeichnungs Werte (kommctrl. h)
description: In diesem Abschnitt werden die Werte aufgelistet, die zum Identifizieren der Teile eines TrackBar-Steuer Elements verwendet werden.
ms.assetid: 154321c7-99f8-4ed5-a5ff-fb96126b43c7
topic_type:
- apiref
api_name:
- TBCD_CHANNEL
- TBCD_THUMB
- TBCD_TICS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccf05ab951fdc83ec5be414688be56d710ba0d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370657"
---
# <a name="custom-draw-values"></a><span data-ttu-id="5367e-103">Benutzerdefinierte Zeichnungs Werte</span><span class="sxs-lookup"><span data-stu-id="5367e-103">Custom Draw Values</span></span>

<span data-ttu-id="5367e-104">In diesem Abschnitt werden die Werte aufgelistet, die zum Identifizieren der Teile eines TrackBar-Steuer Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5367e-104">This section lists the values used to identify a Trackbar control's parts.</span></span>



| <span data-ttu-id="5367e-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="5367e-105">Constant</span></span>                                                                                                                                                   | <span data-ttu-id="5367e-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5367e-106">Description</span></span>                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <span data-ttu-id="5367e-107"><dt>**TBCD- \_ Kanal**</dt></span><span class="sxs-lookup"><span data-stu-id="5367e-107"><dt>**TBCD\_CHANNEL**</dt></span></span> </dl> | <span data-ttu-id="5367e-108">Gibt den Kanal an, entlang dem der Ziehpunkt des TrackBar-Steuer Elements bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="5367e-108">Identifies the channel that the trackbar control's thumb marker slides along.</span></span><br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <span data-ttu-id="5367e-109"><dt>**TBCD- \_ Thumb**</dt></span><span class="sxs-lookup"><span data-stu-id="5367e-109"><dt>**TBCD\_THUMB**</dt></span></span> </dl>       | <span data-ttu-id="5367e-110">Identifiziert den Zieh Punkt Marker des TrackBar-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="5367e-110">Identifies the trackbar control's thumb marker.</span></span> <span data-ttu-id="5367e-111">Dies ist der Teil des-Steuer Elements, den der Benutzer verschiebt.</span><span class="sxs-lookup"><span data-stu-id="5367e-111">This is the part of the control that the user moves.</span></span><br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <span data-ttu-id="5367e-112"><dt>**TBCD- \_ tik**</dt></span><span class="sxs-lookup"><span data-stu-id="5367e-112"><dt>**TBCD\_TICS**</dt></span></span> </dl>          | <span data-ttu-id="5367e-113">Identifiziert die Teil Striche, die entlang der Kante des TrackBar-Steuer Elements angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5367e-113">Identifies the tick marks that are displayed along the trackbar control's edge.</span></span><br/>                      |



## <a name="remarks"></a><span data-ttu-id="5367e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5367e-114">Remarks</span></span>

<span data-ttu-id="5367e-115">Benutzerdefinierte Zeichnungs Werte werden z. b. im **dwitemspec** -Member der [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="5367e-115">Custom Draw values, for example, are specified in the **dwItemSpec** member of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5367e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5367e-116">Requirements</span></span>



| <span data-ttu-id="5367e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5367e-117">Requirement</span></span> | <span data-ttu-id="5367e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5367e-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5367e-119">Header</span><span class="sxs-lookup"><span data-stu-id="5367e-119">Header</span></span><br/> | <dl> <span data-ttu-id="5367e-120"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5367e-120"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





