---
title: TCM_GETITEMCOUNT Meldung (kommstrg. h)
description: Ruft die Anzahl der Registerkarten im Registerkarten-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des tabctrl \_ GetItemCount-Makros senden.
ms.assetid: a8ec7d66-fe44-45ca-8f6c-4e75752ebe95
keywords:
- Windows-Steuerelemente für TCM_GETITEMCOUNT Meldung
topic_type:
- apiref
api_name:
- TCM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d638a9be81581605b978695c8504f538967c77f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105741"
---
# <a name="tcm_getitemcount-message"></a><span data-ttu-id="b3123-105">TCM \_ GetItemCount-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b3123-105">TCM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="b3123-106">Ruft die Anzahl der Registerkarten im Registerkarten-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="b3123-106">Retrieves the number of tabs in the tab control.</span></span> <span data-ttu-id="b3123-107">Sie können diese Nachricht explizit oder mithilfe des [**tabctrl \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="b3123-107">You can send this message explicitly or by using the [**TabCtrl\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b3123-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3123-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3123-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b3123-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b3123-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="b3123-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b3123-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3123-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b3123-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="b3123-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3123-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3123-113">Return value</span></span>

<span data-ttu-id="b3123-114">Gibt die Anzahl der Elemente zurück, wenn erfolgreich, andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b3123-114">Returns the number of items if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3123-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3123-115">Requirements</span></span>



| <span data-ttu-id="b3123-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3123-116">Requirement</span></span> | <span data-ttu-id="b3123-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b3123-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3123-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3123-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b3123-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3123-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b3123-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3123-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b3123-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3123-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b3123-122">Header</span><span class="sxs-lookup"><span data-stu-id="b3123-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3123-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3123-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





