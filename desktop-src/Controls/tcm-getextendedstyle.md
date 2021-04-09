---
title: TCM_GETEXTENDEDSTYLE Meldung (kommstrg. h)
description: Ruft die erweiterten Stile ab, die zurzeit für das Registerkarten-Steuerelement verwendet werden. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ GetExtendedStyle-Makros senden.
ms.assetid: 983ffcbe-0d8d-4686-83de-fc564744390f
keywords:
- Windows-Steuerelemente für TCM_GETEXTENDEDSTYLE Meldung
topic_type:
- apiref
api_name:
- TCM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8280b7043591dd4fdd0b453c5baea5fe014bd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957039"
---
# <a name="tcm_getextendedstyle-message"></a><span data-ttu-id="227c0-105">TCM \_ GetExtendedStyle-Nachricht</span><span class="sxs-lookup"><span data-stu-id="227c0-105">TCM\_GETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="227c0-106">Ruft die erweiterten Stile ab, die zurzeit für das Registerkarten-Steuerelement verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="227c0-106">Retrieves the extended styles that are currently in use for the tab control.</span></span> <span data-ttu-id="227c0-107">Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="227c0-107">You can send this message explicitly or by using the [**TabCtrl\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="227c0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="227c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="227c0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="227c0-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="227c0-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="227c0-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="227c0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="227c0-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="227c0-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="227c0-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="227c0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="227c0-113">Return value</span></span>

<span data-ttu-id="227c0-114">Gibt einen **DWORD** -Wert zurück, der die erweiterten Stile darstellt, die zurzeit für das Register Steuerelement verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="227c0-114">Returns a **DWORD** value that represents the extended styles currently in use for the tab control.</span></span> <span data-ttu-id="227c0-115">Dieser Wert ist eine Kombination aus [erweiterten](tab-control-extended-styles.md)Formatvorlagen des Register Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="227c0-115">This value is a combination of tab control [extended styles](tab-control-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="227c0-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="227c0-116">Requirements</span></span>



| <span data-ttu-id="227c0-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="227c0-117">Requirement</span></span> | <span data-ttu-id="227c0-118">Wert</span><span class="sxs-lookup"><span data-stu-id="227c0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="227c0-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="227c0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="227c0-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="227c0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="227c0-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="227c0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="227c0-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="227c0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="227c0-123">Header</span><span class="sxs-lookup"><span data-stu-id="227c0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="227c0-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="227c0-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="227c0-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="227c0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="227c0-126">**TCM/ \_ textendecodstyle**</span><span class="sxs-lookup"><span data-stu-id="227c0-126">**TCM\_SETEXTENDEDSTYLE**</span></span>](tcm-setextendedstyle.md)
</dt> </dl>

 

 





