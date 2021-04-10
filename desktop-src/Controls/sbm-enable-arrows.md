---
title: SBM_ENABLE_ARROWS Meldung (Winuser. h)
description: Eine Anwendung sendet die SBM-Option \_ \_ Pfeile aktivieren, um einen oder beide Pfeile eines ScrollBar-Steuer Elements zu aktivieren oder zu deaktivieren.
ms.assetid: 9646826a-3a7c-490b-822d-7511e4ef2262
keywords:
- Windows-Steuerelemente für SBM_ENABLE_ARROWS Meldung
topic_type:
- apiref
api_name:
- SBM_ENABLE_ARROWS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78895b43ec7908172a6164917b33ac8549088db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956883"
---
# <a name="sbm_enable_arrows-message"></a><span data-ttu-id="d3d94-104">SBM \_ - \_ Meldung "Pfeile aktivieren"</span><span class="sxs-lookup"><span data-stu-id="d3d94-104">SBM\_ENABLE\_ARROWS message</span></span>

<span data-ttu-id="d3d94-105">Eine Anwendung sendet die **SBM-Option \_ \_ Pfeile aktivieren** , um einen oder beide Pfeile eines ScrollBar-Steuer Elements zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d3d94-105">An application sends the **SBM\_ENABLE\_ARROWS** message to enable or disable one or both arrows of a scroll bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3d94-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3d94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3d94-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3d94-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3d94-108">Gibt an, ob die Schiebe leisten Pfeile aktiviert oder deaktiviert sind, und gibt an, welche Pfeile aktiviert oder deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="d3d94-108">Specifies whether the scroll bar arrows are enabled or disabled and indicates which arrows are enabled or disabled.</span></span> <span data-ttu-id="d3d94-109">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="d3d94-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d3d94-110">Wert</span><span class="sxs-lookup"><span data-stu-id="d3d94-110">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="d3d94-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d3d94-111">Meaning</span></span>                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <span data-ttu-id="d3d94-112"><dt>**ESB- \_ Deaktivierung \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d3d94-112"><dt>**ESB\_DISABLE\_BOTH**</dt></span></span> </dl> | <span data-ttu-id="d3d94-113">Deaktiviert beide Pfeile auf einer Schiebe Leiste.</span><span class="sxs-lookup"><span data-stu-id="d3d94-113">Disables both arrows on a scroll bar.</span></span><br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <span data-ttu-id="d3d94-114"><dt>**ESB- \_ Deaktivierung \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d3d94-114"><dt>**ESB\_DISABLE\_DOWN**</dt></span></span> </dl> | <span data-ttu-id="d3d94-115">Deaktiviert den Pfeil nach unten auf einer vertikalen Schiebe Leiste.</span><span class="sxs-lookup"><span data-stu-id="d3d94-115">Disables the down arrow on a vertical scroll bar.</span></span><br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <span data-ttu-id="d3d94-116"><dt>**ESB- \_ Deaktivierung von \_ ltup**</dt></span><span class="sxs-lookup"><span data-stu-id="d3d94-116"><dt>**ESB\_DISABLE\_LTUP**</dt></span></span> </dl> | <span data-ttu-id="d3d94-117">Deaktiviert den Pfeil nach links auf einer horizontalen Schiebe Leiste oder den Pfeil nach oben auf einer vertikalen Schiebe Leiste.</span><span class="sxs-lookup"><span data-stu-id="d3d94-117">Disables the left arrow on a horizontal scroll bar or the up arrow on a vertical scroll bar.</span></span><br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <span data-ttu-id="d3d94-118"><dt>**ESB \_ deaktiviert \_ Links**</dt></span><span class="sxs-lookup"><span data-stu-id="d3d94-118"><dt>**ESB\_DISABLE\_LEFT**</dt></span></span> </dl> | <span data-ttu-id="d3d94-119">Deaktiviert den Pfeil nach links auf einer horizontalen Schiebe Leiste.</span><span class="sxs-lookup"><span data-stu-id="d3d94-119">Disables the left arrow on a horizontal scroll bar.</span></span><br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <span data-ttu-id="d3d94-120"><dt>**ESB- \_ Deaktivieren von \_ rtdn**</dt></span><span class="sxs-lookup"><span data-stu-id="d3d94-120"><dt>**ESB\_DISABLE\_RTDN**</dt></span></span> </dl> | <span data-ttu-id="d3d94-121">Deaktiviert den Pfeil nach rechts auf einer horizontalen Schiebe Leiste oder den Pfeil nach unten auf einer vertikalen Schiebe Leiste.</span><span class="sxs-lookup"><span data-stu-id="d3d94-121">Disables the right arrow on a horizontal scroll bar or the down arrow on a vertical scroll bar.</span></span><br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <span data-ttu-id="d3d94-122"><dt>**ESB- \_ Deaktivierung \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d3d94-122"><dt>**ESB\_DISABLE\_UP**</dt></span></span> </dl>       | <span data-ttu-id="d3d94-123">Deaktiviert den Pfeil nach oben auf einer vertikalen Schiebe Leiste.</span><span class="sxs-lookup"><span data-stu-id="d3d94-123">Disables the up arrow on a vertical scroll bar.</span></span><br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <span data-ttu-id="d3d94-124"><dt>**ESB \_ aktivieren \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d3d94-124"><dt>**ESB\_ENABLE\_BOTH**</dt></span></span> </dl>    | <span data-ttu-id="d3d94-125">Aktiviert beide Pfeile auf einer Schiebe Leiste.</span><span class="sxs-lookup"><span data-stu-id="d3d94-125">Enables both arrows on a scroll bar.</span></span><br/>                                                            |



 

</dd> <dt>

<span data-ttu-id="d3d94-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3d94-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3d94-127">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3d94-127">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3d94-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3d94-128">Return value</span></span>

<span data-ttu-id="d3d94-129">Wenn die Nachricht erfolgreich ist, lautet der Rückgabewert " **true**". Andernfalls ist Sie **false**.</span><span class="sxs-lookup"><span data-stu-id="d3d94-129">If the message succeeds, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3d94-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3d94-130">Requirements</span></span>



| <span data-ttu-id="d3d94-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3d94-131">Requirement</span></span> | <span data-ttu-id="d3d94-132">Wert</span><span class="sxs-lookup"><span data-stu-id="d3d94-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3d94-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3d94-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d3d94-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3d94-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d3d94-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3d94-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d3d94-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3d94-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d3d94-137">Header</span><span class="sxs-lookup"><span data-stu-id="d3d94-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3d94-138"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d3d94-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





