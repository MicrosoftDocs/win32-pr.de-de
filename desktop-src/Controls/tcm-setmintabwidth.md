---
title: TCM_SETMINTABWIDTH Meldung (kommstrg. h)
description: Legt die minimale Breite von Elementen in einem Registerkarten-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ setmintabwidth-Makros senden.
ms.assetid: c0be3d4e-774c-4233-820f-01ffbb69ecf0
keywords:
- Windows-Steuerelemente für TCM_SETMINTABWIDTH Meldung
topic_type:
- apiref
api_name:
- TCM_SETMINTABWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87208275ed52c638751352761961ce1f42e6944a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340758"
---
# <a name="tcm_setmintabwidth-message"></a><span data-ttu-id="d9c6f-105">TCM- \_ setmintabwidth-Meldung</span><span class="sxs-lookup"><span data-stu-id="d9c6f-105">TCM\_SETMINTABWIDTH message</span></span>

<span data-ttu-id="d9c6f-106">Legt die minimale Breite von Elementen in einem Registerkarten-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="d9c6f-106">Sets the minimum width of items in a tab control.</span></span> <span data-ttu-id="d9c6f-107">Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ setmintabwidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="d9c6f-107">You can send this message explicitly or by using the [**TabCtrl\_SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9c6f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9c6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9c6f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9c6f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d9c6f-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d9c6f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d9c6f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9c6f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9c6f-112">Minimale Breite, die für ein Registerkarten-Steuerelement festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9c6f-112">Minimum width to be set for a tab control item.</span></span> <span data-ttu-id="d9c6f-113">Wenn dieser Parameter auf-1 festgelegt ist, verwendet das Steuerelement die Standard Registerkarten Breite.</span><span class="sxs-lookup"><span data-stu-id="d9c6f-113">If this parameter is set to -1, the control will use the default tab width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9c6f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9c6f-114">Return value</span></span>

<span data-ttu-id="d9c6f-115">Gibt einen int-Wert zurück, der die vorherige minimale Registerkarten Breite darstellt.</span><span class="sxs-lookup"><span data-stu-id="d9c6f-115">Returns an INT value that represents the previous minimum tab width.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9c6f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9c6f-116">Requirements</span></span>



| <span data-ttu-id="d9c6f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9c6f-117">Requirement</span></span> | <span data-ttu-id="d9c6f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d9c6f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9c6f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9c6f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d9c6f-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9c6f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d9c6f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9c6f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d9c6f-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9c6f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9c6f-123">Header</span><span class="sxs-lookup"><span data-stu-id="d9c6f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9c6f-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9c6f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





