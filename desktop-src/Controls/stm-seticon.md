---
title: STM_SETICON Meldung (Winuser. h)
description: Eine Anwendung sendet die STM \_ SetIcon-Nachricht, um ein Symbol einem Symbol Steuerelement zuzuordnen.
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- Windows-Steuerelemente für STM_SETICON Meldung
topic_type:
- apiref
api_name:
- STM_SETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9c7e2a007c1f866a1c73b3a1c1a55b157add47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040160"
---
# <a name="stm_seticon-message"></a><span data-ttu-id="b4023-104">STM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="b4023-104">STM\_SETICON message</span></span>

<span data-ttu-id="b4023-105">Eine Anwendung sendet die **STM \_ SetIcon** -Nachricht, um ein Symbol einem Symbol Steuerelement zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="b4023-105">An application sends the **STM\_SETICON** message to associate an icon with an icon control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4023-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4023-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4023-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4023-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4023-108">Handle für das Symbol, das mit dem Symbol Steuerelement verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4023-108">Handle to the icon to associate with the icon control.</span></span>

</dd> <dt>

<span data-ttu-id="b4023-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4023-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4023-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b4023-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4023-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4023-111">Return value</span></span>

<span data-ttu-id="b4023-112">Der Rückgabewert ist ein Handle für das Symbol, das zuvor dem Symbol Steuerelement zugeordnet wurde, oder 0 (null), wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="b4023-112">The return value is a handle to the icon previously associated with the icon control, or zero if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4023-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4023-113">Requirements</span></span>



| <span data-ttu-id="b4023-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4023-114">Requirement</span></span> | <span data-ttu-id="b4023-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b4023-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4023-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4023-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b4023-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4023-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b4023-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4023-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b4023-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4023-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b4023-120">Header</span><span class="sxs-lookup"><span data-stu-id="b4023-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4023-121"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="b4023-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4023-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4023-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="b4023-123">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="b4023-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b4023-124">**STM- \_ getIcon**</span><span class="sxs-lookup"><span data-stu-id="b4023-124">**STM\_GETICON**</span></span>](stm-geticon.md)
</dt> <dt>

<span data-ttu-id="b4023-125">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="b4023-125">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b4023-126">**LoadIcon**</span><span class="sxs-lookup"><span data-stu-id="b4023-126">**LoadIcon**</span></span>](/windows/desktop/api/winuser/nf-winuser-loadicona)
</dt> </dl>

 

