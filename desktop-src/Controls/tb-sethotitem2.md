---
title: TB_SETHOTITEM2 Nachricht (Commctrl.h)
description: 'TB_SETHOTITEM2 Meldung: Legt das heiße Element in einer Symbolleiste fest.'
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- TB_SETHOTITEM2 Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TB_SETHOTITEM2
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7daf67839837adccfbec99bf03fc4dfff97738db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104138"
---
# <a name="tb_sethotitem2-message"></a><span data-ttu-id="25b28-104">TB \_ SETHOTITEM2-Nachricht</span><span class="sxs-lookup"><span data-stu-id="25b28-104">TB\_SETHOTITEM2 message</span></span>

<span data-ttu-id="25b28-105">Legt das heiße Element in einer Symbolleiste fest.</span><span class="sxs-lookup"><span data-stu-id="25b28-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="25b28-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="25b28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25b28-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25b28-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25b28-108">Index des Elements, das heiß gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="25b28-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="25b28-109">Wenn dieser Wert -1 ist, ist keines der Elemente heiß.</span><span class="sxs-lookup"><span data-stu-id="25b28-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="25b28-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25b28-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="25b28-111">Eine Kombination von HICF \_ xxx-Flags.</span><span class="sxs-lookup"><span data-stu-id="25b28-111">A combination of HICF\_xxx flags.</span></span> <span data-ttu-id="25b28-112">Siehe <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span><span class="sxs-lookup"><span data-stu-id="25b28-112">See <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25b28-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25b28-113">Return value</span></span>

<span data-ttu-id="25b28-114">Gibt den Index des vorherigen heißen Elements oder -1 zurück, wenn kein heißes Element vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="25b28-114">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="25b28-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25b28-115">Remarks</span></span>

<span data-ttu-id="25b28-116">Das Verhalten dieser Meldung ist nicht für Symbolleisten definiert, die nicht über den [**TBSTYLE \_ FLAT-Stil**](toolbar-control-and-button-styles.md) verfügen.</span><span class="sxs-lookup"><span data-stu-id="25b28-116">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="25b28-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25b28-117">Requirements</span></span>



| <span data-ttu-id="25b28-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25b28-118">Requirement</span></span> | <span data-ttu-id="25b28-119">Wert</span><span class="sxs-lookup"><span data-stu-id="25b28-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25b28-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25b28-120">Minimum supported client</span></span><br/> | <span data-ttu-id="25b28-121">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25b28-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25b28-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25b28-122">Minimum supported server</span></span><br/> | <span data-ttu-id="25b28-123">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25b28-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25b28-124">Header</span><span class="sxs-lookup"><span data-stu-id="25b28-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="25b28-125"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="25b28-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





