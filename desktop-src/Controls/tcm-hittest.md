---
title: TCM_HITTEST Meldung (kommstrg. h)
description: Bestimmt, welche Registerkarte, falls vorhanden, an einer angegebenen Bildschirmposition ist. Sie können diese Nachricht explizit oder mithilfe des tabctrl \_ HitTest-Makros senden.
ms.assetid: 0334f616-8d39-4460-a7f8-692a9ffab012
keywords:
- Windows-Steuerelemente für TCM_HITTEST Meldung
topic_type:
- apiref
api_name:
- TCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04787662e417513d8c9c93e45cecd0d8bddc6cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340366"
---
# <a name="tcm_hittest-message"></a><span data-ttu-id="6c1cc-105">TCM- \_ HitTest-Meldung</span><span class="sxs-lookup"><span data-stu-id="6c1cc-105">TCM\_HITTEST message</span></span>

<span data-ttu-id="6c1cc-106">Bestimmt, welche Registerkarte, falls vorhanden, an einer angegebenen Bildschirmposition ist.</span><span class="sxs-lookup"><span data-stu-id="6c1cc-106">Determines which tab, if any, is at a specified screen position.</span></span> <span data-ttu-id="6c1cc-107">Sie können diese Nachricht explizit oder mithilfe des [**tabctrl \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="6c1cc-107">You can send this message explicitly or by using the [**TabCtrl\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c1cc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c1cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c1cc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c1cc-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6c1cc-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="6c1cc-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6c1cc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c1cc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c1cc-112">Zeiger auf eine [**tchittestinfo**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) -Struktur, die die zu überprüfende Bildschirmposition angibt.</span><span class="sxs-lookup"><span data-stu-id="6c1cc-112">Pointer to a [**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) structure that specifies the screen position to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c1cc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c1cc-113">Return value</span></span>

<span data-ttu-id="6c1cc-114">Gibt den Index der Registerkarte zurück, oder-1, wenn sich keine Registerkarte an der angegebenen Position befindet.</span><span class="sxs-lookup"><span data-stu-id="6c1cc-114">Returns the index of the tab, or -1 if no tab is at the specified position.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c1cc-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c1cc-115">Requirements</span></span>



| <span data-ttu-id="6c1cc-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c1cc-116">Requirement</span></span> | <span data-ttu-id="6c1cc-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6c1cc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c1cc-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c1cc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6c1cc-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c1cc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c1cc-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c1cc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6c1cc-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c1cc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c1cc-122">Header</span><span class="sxs-lookup"><span data-stu-id="6c1cc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c1cc-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c1cc-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





