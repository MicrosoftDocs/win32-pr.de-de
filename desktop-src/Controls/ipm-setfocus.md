---
title: IPM_SETFOCUS Meldung (kommstrg. h)
description: Legt den Tastaturfokus auf das angegebene Feld im IP-Adress Steuerelement fest. Der gesamte Text in diesem Feld wird ausgewählt.
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- Windows-Steuerelemente für IPM_SETFOCUS Meldung
topic_type:
- apiref
api_name:
- IPM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d713e0a8b7eb838a2db5c4738c801d4fb76b782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104462"
---
# <a name="ipm_setfocus-message"></a><span data-ttu-id="2aaa8-105">IPM- \_ SetFocus-Nachricht</span><span class="sxs-lookup"><span data-stu-id="2aaa8-105">IPM\_SETFOCUS message</span></span>

<span data-ttu-id="2aaa8-106">Legt den Tastaturfokus auf das angegebene Feld im IP-Adress Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="2aaa8-106">Sets the keyboard focus to the specified field in the IP address control.</span></span> <span data-ttu-id="2aaa8-107">Der gesamte Text in diesem Feld wird ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="2aaa8-107">All of the text in that field will be selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="2aaa8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2aaa8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2aaa8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2aaa8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2aaa8-110">Ein NULL basierter Feld Index, auf den der Fokus festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2aaa8-110">A zero-based field index to which the focus should be set.</span></span> <span data-ttu-id="2aaa8-111">Wenn dieser Wert größer als die Anzahl der Felder ist, wird der Fokus auf das erste leere Feld festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2aaa8-111">If this value is greater than the number of fields, focus is set to the first blank field.</span></span> <span data-ttu-id="2aaa8-112">Wenn alle Felder nicht leer sind, wird der Fokus auf das erste Feld festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2aaa8-112">If all fields are nonblank, focus is set to the first field.</span></span>

</dd> <dt>

<span data-ttu-id="2aaa8-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2aaa8-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2aaa8-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2aaa8-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2aaa8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2aaa8-115">Return value</span></span>

<span data-ttu-id="2aaa8-116">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2aaa8-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2aaa8-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2aaa8-117">Requirements</span></span>



| <span data-ttu-id="2aaa8-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2aaa8-118">Requirement</span></span> | <span data-ttu-id="2aaa8-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2aaa8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2aaa8-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2aaa8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2aaa8-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2aaa8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2aaa8-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2aaa8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2aaa8-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2aaa8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2aaa8-124">Header</span><span class="sxs-lookup"><span data-stu-id="2aaa8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2aaa8-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2aaa8-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





