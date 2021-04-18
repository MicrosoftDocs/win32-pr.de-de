---
title: TCM_GETCURSEL Meldung (kommstrg. h)
description: Bestimmt die derzeit ausgewählte Registerkarte in einem Registerkarten-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ getcurrsel-Makros senden.
ms.assetid: 1caa7fad-da5a-4b26-8e78-12110c126691
keywords:
- Windows-Steuerelemente für TCM_GETCURSEL Meldung
topic_type:
- apiref
api_name:
- TCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3103931e29d150412192a745f8dde7681cff0e94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338785"
---
# <a name="tcm_getcursel-message"></a><span data-ttu-id="11fe4-105">TCM \_ getcurrsel-Nachricht</span><span class="sxs-lookup"><span data-stu-id="11fe4-105">TCM\_GETCURSEL message</span></span>

<span data-ttu-id="11fe4-106">Bestimmt die derzeit ausgewählte Registerkarte in einem Registerkarten-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="11fe4-106">Determines the currently selected tab in a tab control.</span></span> <span data-ttu-id="11fe4-107">Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ getcurrsel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="11fe4-107">You can send this message explicitly or by using the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="11fe4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="11fe4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11fe4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="11fe4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="11fe4-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="11fe4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="11fe4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11fe4-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="11fe4-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="11fe4-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11fe4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11fe4-113">Return value</span></span>

<span data-ttu-id="11fe4-114">Gibt den Index der ausgewählten Registerkarte zurück, wenn erfolgreich, oder-1, wenn keine Registerkarte ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="11fe4-114">Returns the index of the selected tab if successful, or -1 if no tab is selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="11fe4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11fe4-115">Requirements</span></span>



| <span data-ttu-id="11fe4-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11fe4-116">Requirement</span></span> | <span data-ttu-id="11fe4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="11fe4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11fe4-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11fe4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="11fe4-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11fe4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="11fe4-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11fe4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="11fe4-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11fe4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11fe4-122">Header</span><span class="sxs-lookup"><span data-stu-id="11fe4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="11fe4-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="11fe4-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





