---
title: CCM_DPISCALE Meldung (kommstrg. h)
description: Ermöglicht die automatische Skalierung von hohen DPI-Werten (dpi) in Tree-View Steuerelementen, List-View Steuerelementen, ComboBoxEx-Steuerelementen, Header Steuerelementen, Schaltflächen, Symbolleisten-Steuerelementen, Animations Steuerelementen und Bildlisten.
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- Windows-Steuerelemente für CCM_DPISCALE Meldung
topic_type:
- apiref
api_name:
- CCM_DPISCALE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef978f486f370adf9872d28e1accbacc37a6de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104517"
---
# <a name="ccm_dpiscale-message"></a><span data-ttu-id="566ec-104">CCM \_ dpiscale-Nachricht</span><span class="sxs-lookup"><span data-stu-id="566ec-104">CCM\_DPISCALE message</span></span>

<span data-ttu-id="566ec-105">Aktiviert die automatische Skalierung von hohen dpi [-](tree-view-controls.md)Werten (dpi) in Strukturansicht-Steuerelementen, [Listenansicht-](list-view-control-reference.md)Steuerelementen, [ComboBoxEx](comboboxex-controls.md)-Steuerelementen, [Header](header-controls.md)Steuerelementen, [Schalt](buttons.md)Flächen, [Symbol](toolbar-controls-overview.md)leisten-Steuerelementen, [Animations Steuerelementen](animation-control-overview.md)und [Bildlisten](image-lists.md).</span><span class="sxs-lookup"><span data-stu-id="566ec-105">Enables automatic high dots per inch (dpi) scaling in [Tree-View controls](tree-view-controls.md), [List-View controls](list-view-control-reference.md), [ComboBoxEx controls](comboboxex-controls.md), [Header controls](header-controls.md), [Buttons](buttons.md), [Toolbar controls](toolbar-controls-overview.md), [Animation controls](animation-control-overview.md), and [Image Lists](image-lists.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="566ec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="566ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="566ec-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="566ec-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="566ec-108">Auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="566ec-108">Set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="566ec-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="566ec-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="566ec-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="566ec-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="566ec-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="566ec-111">Return value</span></span>

<span data-ttu-id="566ec-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="566ec-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="566ec-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="566ec-113">Remarks</span></span>

<span data-ttu-id="566ec-114">Die Schnellstart-und [Taskleiste](/windows/desktop/shell/taskbar) sollten keine DPI-Skalierung angeben, da die Bilder bereits skaliert sind.</span><span class="sxs-lookup"><span data-stu-id="566ec-114">Quick Launch and [Taskbar](/windows/desktop/shell/taskbar) should not specify a dpi scaling, because the images are already scaled.</span></span>

<span data-ttu-id="566ec-115">Jedes Steuerelement, das eine mit der SmallIcon-Metrik erstellte Bildliste verwendet, sollte seine Symbole nicht skalieren.</span><span class="sxs-lookup"><span data-stu-id="566ec-115">Any control that uses an image list created with the SmallIcon metric should not scale its icons.</span></span>

> [!Note]  
> <span data-ttu-id="566ec-116">Um diese API zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="566ec-116">To use this API, you must provide a manifest that specifies Comclt32.dll version 6.0.</span></span> <span data-ttu-id="566ec-117">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="566ec-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="566ec-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="566ec-118">Requirements</span></span>



| <span data-ttu-id="566ec-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="566ec-119">Requirement</span></span> | <span data-ttu-id="566ec-120">Wert</span><span class="sxs-lookup"><span data-stu-id="566ec-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="566ec-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="566ec-121">Minimum supported client</span></span><br/> | <span data-ttu-id="566ec-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="566ec-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="566ec-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="566ec-123">Minimum supported server</span></span><br/> | <span data-ttu-id="566ec-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="566ec-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="566ec-125">Header</span><span class="sxs-lookup"><span data-stu-id="566ec-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="566ec-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="566ec-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

