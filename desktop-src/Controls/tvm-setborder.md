---
title: TVM_SETBORDER Meldung (kommstrg. h)
description: Legt die Größe des Rahmens für die Elemente in einem Strukturansicht-Steuerelement fest. Sie können die Nachricht explizit oder mithilfe des TreeView \_ setborder-Makros senden.
ms.assetid: 468b46ae-2ab2-4753-a0af-7c644f75ce62
keywords:
- Windows-Steuerelemente für TVM_SETBORDER Meldung
topic_type:
- apiref
api_name:
- TVM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b4401959e2579caab7f2cb4b6eed1ea34481ffa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859000"
---
# <a name="tvm_setborder-message"></a><span data-ttu-id="c0f34-105">TVM- \_ setborder-Meldung</span><span class="sxs-lookup"><span data-stu-id="c0f34-105">TVM\_SETBORDER message</span></span>

<span data-ttu-id="c0f34-106">**Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.**</span><span class="sxs-lookup"><span data-stu-id="c0f34-106">**Intended for internal use; not recommended for use in applications.**</span></span>

<span data-ttu-id="c0f34-107">Legt die Größe des Rahmens für die Elemente in einem Strukturansicht-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="c0f34-107">Sets the size of the border for the items in a tree-view control.</span></span> <span data-ttu-id="c0f34-108">Sie können die Nachricht explizit oder mithilfe des [**TreeView \_ setborder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="c0f34-108">You can send the message explicitly or by using the [**TreeView\_SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0f34-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0f34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0f34-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0f34-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0f34-111">Aktionsflags.</span><span class="sxs-lookup"><span data-stu-id="c0f34-111">Action flags.</span></span> <span data-ttu-id="c0f34-112">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="c0f34-112">This parameter can be one or more of the following values:</span></span>



| <span data-ttu-id="c0f34-113">Wert</span><span class="sxs-lookup"><span data-stu-id="c0f34-113">Value</span></span>                                                                                                                                                         | <span data-ttu-id="c0f34-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c0f34-114">Meaning</span></span>                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="TVSBF_XBORDER"></span><span id="tvsbf_xborder"></span><dl> <span data-ttu-id="c0f34-115"><dt>**tvsbf- \_ xborder**</dt></span><span class="sxs-lookup"><span data-stu-id="c0f34-115"><dt>**TVSBF\_XBORDER**</dt></span></span> </dl> | <span data-ttu-id="c0f34-116">Wendet die angegebene Rahmengröße auf die linke Seite der Elemente im Strukturansicht-Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="c0f34-116">Applies the specified border size to the left side of the items in the tree-view control.</span></span> <br/> |
| <span id="TVSBF_YBORDER"></span><span id="tvsbf_yborder"></span><dl> <span data-ttu-id="c0f34-117"><dt>**tvsbf \_ yborder**</dt></span><span class="sxs-lookup"><span data-stu-id="c0f34-117"><dt>**TVSBF\_YBORDER**</dt></span></span> </dl> | <span data-ttu-id="c0f34-118">Wendet die angegebene Rahmengröße auf den oberen Rand der Elemente im Strukturansicht-Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="c0f34-118">Applies the specified border size to the top of the items in the tree-view control.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="c0f34-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0f34-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0f34-120">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **kurzes** , das die Größe des linken Rahmens in Pixel angibt.</span><span class="sxs-lookup"><span data-stu-id="c0f34-120">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **SHORT** that specifies the size of the left border, in pixels.</span></span> <span data-ttu-id="c0f34-121">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist ein **kurzes** , das die Größe des oberen Rahmens in Pixel angibt.</span><span class="sxs-lookup"><span data-stu-id="c0f34-121">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **SHORT** that specifies the size of the top border, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0f34-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0f34-122">Return value</span></span>

<span data-ttu-id="c0f34-123">Gibt einen **Long** -Wert zurück, der die vorherige Rahmengröße in Pixel enthält.</span><span class="sxs-lookup"><span data-stu-id="c0f34-123">Returns a **LONG** value that contains the previous border size, in pixels.</span></span> <span data-ttu-id="c0f34-124">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält die vorherige Größe des horizontalen Rahmens, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) enthält die vorherige Größe des vertikalen Rahmens.</span><span class="sxs-lookup"><span data-stu-id="c0f34-124">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the previous size of the horizontal border, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the previous size of the vertical border.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0f34-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0f34-125">Remarks</span></span>

<span data-ttu-id="c0f34-126">**Sicherheitswarnung:** Die Verwendung dieser Nachricht kann die Sicherheit des Programms beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="c0f34-126">**Security Warning:** Using this message might compromise the security of your program.</span></span>

<span data-ttu-id="c0f34-127">Der Element Rahmen wird nur für Abstands Zwecke festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c0f34-127">The item border is set just for spacing purposes.</span></span> <span data-ttu-id="c0f34-128">Eine erfolgreiche Einstellung löst eine Neuberechnung der Schiebe leisten aus.</span><span class="sxs-lookup"><span data-stu-id="c0f34-128">A successful setting triggers a recalculation of the scroll bars.</span></span>

<span data-ttu-id="c0f34-129">Diese Meldung wird in zukünftigen Versionen von Comctl32.dll möglicherweise nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c0f34-129">This message may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="c0f34-130">Außerdem ist diese Meldung nicht in "kommctrl. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="c0f34-130">Also, this message is not defined in commctrl.h.</span></span> <span data-ttu-id="c0f34-131">Fügen Sie den Quelldateien Ihrer Anwendung die folgenden Definitionen hinzu, um die Meldung zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="c0f34-131">Add the following definitions to the source files of your application to use the message:</span></span>

``` syntax
#define TVM_SETBORDER (TV_FIRST + 35)
#define TVSBF_XBORDER 0x00000001
#define TVSBF_YBORDER 0x00000002 
```

## <a name="requirements"></a><span data-ttu-id="c0f34-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0f34-132">Requirements</span></span>



| <span data-ttu-id="c0f34-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0f34-133">Requirement</span></span> | <span data-ttu-id="c0f34-134">Wert</span><span class="sxs-lookup"><span data-stu-id="c0f34-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f34-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0f34-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c0f34-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0f34-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0f34-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0f34-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c0f34-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0f34-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0f34-139">Header</span><span class="sxs-lookup"><span data-stu-id="c0f34-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0f34-140"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0f34-140"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0f34-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0f34-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0f34-142">**TreeView \_ setborder**</span><span class="sxs-lookup"><span data-stu-id="c0f34-142">**TreeView\_SetBorder**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
</dt> </dl>

 

