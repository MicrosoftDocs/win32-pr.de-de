---
title: TB_SETBUTTONWIDTH Meldung (kommstrg. h)
description: Legt die minimale und maximale Schaltflächen breite im Symbolleisten-Steuerelement fest.
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- Windows-Steuerelemente für TB_SETBUTTONWIDTH Meldung
topic_type:
- apiref
api_name:
- TB_SETBUTTONWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e105770d72e90108b9c31311f77599520cecea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103760"
---
# <a name="tb_setbuttonwidth-message"></a><span data-ttu-id="aa5c7-104">TB \_ setbuttonwidth-Meldung</span><span class="sxs-lookup"><span data-stu-id="aa5c7-104">TB\_SETBUTTONWIDTH message</span></span>

<span data-ttu-id="aa5c7-105">Legt die minimale und maximale Schaltflächen breite im Symbolleisten-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="aa5c7-105">Sets the minimum and maximum button widths in the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="aa5c7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa5c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa5c7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa5c7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa5c7-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="aa5c7-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="aa5c7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa5c7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa5c7-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die minimale Schaltflächen breite in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="aa5c7-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum button width, in pixels.</span></span> <span data-ttu-id="aa5c7-111">Symbolleisten Schaltflächen werden nie kleiner als dieser Wert sein.</span><span class="sxs-lookup"><span data-stu-id="aa5c7-111">Toolbar buttons will never be narrower than this value.</span></span>

<span data-ttu-id="aa5c7-112">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die maximale Schaltflächen breite in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="aa5c7-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum button width, in pixels.</span></span> <span data-ttu-id="aa5c7-113">Wenn der Text der Schaltfläche zu breit ist, wird das Steuerelement mit Auslassungs Punkten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aa5c7-113">If button text is too wide, the control displays it with ellipsis points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa5c7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa5c7-114">Return value</span></span>

<span data-ttu-id="aa5c7-115">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="aa5c7-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa5c7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa5c7-116">Remarks</span></span>

<span data-ttu-id="aa5c7-117">Legen Sie mit " **TB \_ setbuttonwidth** " die maximale und minimale zulässige Breite für Schaltflächen fest, bevor Sie hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="aa5c7-117">Use **TB\_SETBUTTONWIDTH** to set the maximum and minimum allowed widths for buttons before they are added.</span></span> <span data-ttu-id="aa5c7-118">Legen Sie die tatsächliche Größe von Schaltflächen mit [**TB \_ setbuttonsize**](tb-setbuttonsize.md) fest.</span><span class="sxs-lookup"><span data-stu-id="aa5c7-118">Use [**TB\_SETBUTTONSIZE**](tb-setbuttonsize.md) to set the actual size of buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa5c7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa5c7-119">Requirements</span></span>



| <span data-ttu-id="aa5c7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa5c7-120">Requirement</span></span> | <span data-ttu-id="aa5c7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="aa5c7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa5c7-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa5c7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="aa5c7-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa5c7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aa5c7-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa5c7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="aa5c7-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa5c7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa5c7-126">Header</span><span class="sxs-lookup"><span data-stu-id="aa5c7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa5c7-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa5c7-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

