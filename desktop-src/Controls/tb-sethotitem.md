---
title: TB_SETHOTITEM (Commctrl.h)
description: 'TB_SETHOTITEM Meldung: Legt das heiße Element in einer Symbolleiste fest.'
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- TB_SETHOTITEM Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TB_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90e5b38675d33a361857c4303fa2a89f22cff29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104178"
---
# <a name="tb_sethotitem-message"></a><span data-ttu-id="2ee35-104">TB \_ SETHOTITEM-Nachricht</span><span class="sxs-lookup"><span data-stu-id="2ee35-104">TB\_SETHOTITEM message</span></span>

<span data-ttu-id="2ee35-105">Legt das heiße Element in einer Symbolleiste fest.</span><span class="sxs-lookup"><span data-stu-id="2ee35-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ee35-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ee35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ee35-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ee35-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ee35-108">Index des Elements, das als "Hot" (Heiß) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2ee35-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="2ee35-109">Wenn dieser Wert -1 ist, ist keines der Elemente heiß.</span><span class="sxs-lookup"><span data-stu-id="2ee35-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="2ee35-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ee35-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2ee35-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2ee35-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ee35-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ee35-112">Return value</span></span>

<span data-ttu-id="2ee35-113">Gibt den Index des vorherigen heißen Elements zurück, oder -1, wenn kein heißes Element vorkommt.</span><span class="sxs-lookup"><span data-stu-id="2ee35-113">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ee35-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ee35-114">Remarks</span></span>

<span data-ttu-id="2ee35-115">Das Verhalten dieser Meldung ist nicht für Symbolleisten definiert, die nicht das [**TBSTYLE \_ FLAT-Format**](toolbar-control-and-button-styles.md) haben.</span><span class="sxs-lookup"><span data-stu-id="2ee35-115">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ee35-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ee35-116">Requirements</span></span>



| <span data-ttu-id="2ee35-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ee35-117">Requirement</span></span> | <span data-ttu-id="2ee35-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2ee35-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee35-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ee35-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2ee35-120">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ee35-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ee35-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ee35-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2ee35-122">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ee35-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ee35-123">Header</span><span class="sxs-lookup"><span data-stu-id="2ee35-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ee35-124"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="2ee35-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





