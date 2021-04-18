---
title: Steuerelement Zustände des Registerkarten Steuer Elements (kommstrg. h)
description: Registerkarten-Steuerelemente unterstützen nun einen Element Zustand zur Unterstützung der TCM- \_ DeselectAll-Nachricht. Außerdem unterstützt die TCITEM-Strukturelement Zustands Werte.
ms.assetid: c4181fe6-0055-45c9-a3d0-8cda051383f2
topic_type:
- apiref
api_name:
- TCIS_BUTTONPRESSED
- TCIS_HIGHLIGHTED
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5214f1a2eee757bfdf5b2a81a8916292b9d7f98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358365"
---
# <a name="tab-control-item-states"></a><span data-ttu-id="d9ef7-104">Steuerelement Zustände von Registerkarten</span><span class="sxs-lookup"><span data-stu-id="d9ef7-104">Tab Control Item States</span></span>

<span data-ttu-id="d9ef7-105">Registerkarten-Steuerelemente unterstützen nun einen Element Zustand zur Unterstützung der [**TCM- \_ DeselectAll**](tcm-deselectall.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d9ef7-105">Tab control items now support an item state to support the [**TCM\_DESELECTALL**](tcm-deselectall.md) message.</span></span> <span data-ttu-id="d9ef7-106">Außerdem unterstützt die [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) -Strukturelement Zustands Werte.</span><span class="sxs-lookup"><span data-stu-id="d9ef7-106">Additionally, the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure supports item state values.</span></span>



| <span data-ttu-id="d9ef7-107">Konstante</span><span class="sxs-lookup"><span data-stu-id="d9ef7-107">Constant</span></span>                                                                                                                                                                     | <span data-ttu-id="d9ef7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9ef7-108">Description</span></span>                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <span data-ttu-id="d9ef7-109"><dt>**tcis- \_ ButtonPressed**</dt></span><span class="sxs-lookup"><span data-stu-id="d9ef7-109"><dt>**TCIS\_BUTTONPRESSED**</dt></span></span> </dl> | <span data-ttu-id="d9ef7-110">[Version 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="d9ef7-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="d9ef7-111">Das Registerkarten-Steuerelement ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d9ef7-111">The tab control item is selected.</span></span> <span data-ttu-id="d9ef7-112">Dieser Status ist nur dann sinnvoll, wenn das Style-Flag der [**TCS- \_ Schalt**](tab-control-styles.md) Flächen festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="d9ef7-112">This state is only meaningful if the [**TCS\_BUTTONS**](tab-control-styles.md) style flag has been set.</span></span><br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <span data-ttu-id="d9ef7-113"><dt>**tcis \_ hervorgehoben**</dt></span><span class="sxs-lookup"><span data-stu-id="d9ef7-113"><dt>**TCIS\_HIGHLIGHTED**</dt></span></span> </dl>       | <span data-ttu-id="d9ef7-114">[Version 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="d9ef7-114">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="d9ef7-115">Das Registerkarten-Steuerelement wird hervorgehoben, und die Registerkarte und der Text werden mithilfe der aktuellen Hervorhebungs Farbe gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d9ef7-115">The tab control item is highlighted, and the tab and text are drawn using the current highlight color.</span></span> <span data-ttu-id="d9ef7-116">Wenn Sie High-Color verwenden, handelt es sich hierbei um eine echte Interpolations-und nicht um eine Dithering-Farbe.</span><span class="sxs-lookup"><span data-stu-id="d9ef7-116">When using high-color, this will be a true interpolation, not a dithered color.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d9ef7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9ef7-117">Requirements</span></span>



| <span data-ttu-id="d9ef7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9ef7-118">Requirement</span></span> | <span data-ttu-id="d9ef7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d9ef7-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9ef7-120">Header</span><span class="sxs-lookup"><span data-stu-id="d9ef7-120">Header</span></span><br/> | <dl> <span data-ttu-id="d9ef7-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9ef7-121"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





