---
title: LVM_APPROXIMATEVIEWRECT Meldung (kommstrg. h)
description: Berechnet die ungefähre Breite und Höhe, die erforderlich sind, um eine bestimmte Anzahl von Elementen anzuzeigen. Sie können diese Nachricht explizit senden oder das ListView- \_ Suffix "näherateviewrect" verwenden.
ms.assetid: a14331a8-217d-48c6-9489-fb90c4d31b91
keywords:
- Windows-Steuerelemente für LVM_APPROXIMATEVIEWRECT Meldung
topic_type:
- apiref
api_name:
- LVM_APPROXIMATEVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be929d34acad46b75a53a9e0cc8825ec9801e998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949429"
---
# <a name="lvm_approximateviewrect-message"></a><span data-ttu-id="40e85-105">LVM- \_ ungefähre näherungsviewrect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="40e85-105">LVM\_APPROXIMATEVIEWRECT message</span></span>

<span data-ttu-id="40e85-106">Berechnet die ungefähre Breite und Höhe, die erforderlich sind, um eine bestimmte Anzahl von Elementen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="40e85-106">Calculates the approximate width and height required to display a given number of items.</span></span> <span data-ttu-id="40e85-107">Sie können diese Nachricht explizit senden oder das [**ListView- \_ Suffix "näherateviewrect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) " verwenden.</span><span class="sxs-lookup"><span data-stu-id="40e85-107">You can send this message explicitly or use the [**ListView\_ApproximateViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="40e85-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="40e85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40e85-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="40e85-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40e85-110">Die Anzahl der Elemente, die im Steuerelement angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="40e85-110">The number of items to be displayed in the control.</span></span> <span data-ttu-id="40e85-111">Wenn dieser Parameter auf-1 festgelegt ist, wird die Gesamtzahl der Elemente im-Steuerelement in der Nachricht verwendet.</span><span class="sxs-lookup"><span data-stu-id="40e85-111">If this parameter is set to -1, the message uses the total number of items in the control.</span></span>

</dd> <dt>

<span data-ttu-id="40e85-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="40e85-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40e85-113">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist die vorgeschlagene x-Dimension des-Steuer Elements in Pixel.</span><span class="sxs-lookup"><span data-stu-id="40e85-113">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the proposed x-dimension of the control, in pixels.</span></span> <span data-ttu-id="40e85-114">Dieser Parameter kann auf-1 festgelegt werden, damit die Nachricht den aktuellen width-Wert verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="40e85-114">This parameter can be set to -1 to allow the message to use the current width value.</span></span>

<span data-ttu-id="40e85-115">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist die vorgeschlagene y-Dimension des-Steuer Elements in Pixel.</span><span class="sxs-lookup"><span data-stu-id="40e85-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the proposed y-dimension of the control, in pixels.</span></span> <span data-ttu-id="40e85-116">Dieser Parameter kann auf-1 festgelegt werden, damit die Nachricht den aktuellen Height-Wert verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="40e85-116">This parameter can be set to -1 to allow the message to use the current height value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40e85-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40e85-117">Return value</span></span>

<span data-ttu-id="40e85-118">Gibt einen **DWORD** -Wert zurück, der die ungefähre Breite (im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) und die Höhe (im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) für die Anzeige der Elemente in Pixel enthält.</span><span class="sxs-lookup"><span data-stu-id="40e85-118">Returns a **DWORD** value that holds the approximate width (in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) and height (in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) needed to display the items, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="40e85-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40e85-119">Remarks</span></span>

<span data-ttu-id="40e85-120">Das Festlegen der Größe des Listenansicht-Steuer Elements auf der Grundlage der Dimensionen, die von dieser Nachricht bereitgestellt werden, kann das Neuzeichnen und reduzieren der Flimmern optimieren.</span><span class="sxs-lookup"><span data-stu-id="40e85-120">Setting the size of the list-view control based on the dimensions provided by this message can optimize redraw and reduce flicker.</span></span>

## <a name="requirements"></a><span data-ttu-id="40e85-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40e85-121">Requirements</span></span>



| <span data-ttu-id="40e85-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40e85-122">Requirement</span></span> | <span data-ttu-id="40e85-123">Wert</span><span class="sxs-lookup"><span data-stu-id="40e85-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40e85-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40e85-124">Minimum supported client</span></span><br/> | <span data-ttu-id="40e85-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40e85-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="40e85-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40e85-126">Minimum supported server</span></span><br/> | <span data-ttu-id="40e85-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40e85-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="40e85-128">Header</span><span class="sxs-lookup"><span data-stu-id="40e85-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="40e85-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="40e85-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

