---
title: PGM_SETBORDER Meldung (kommstrg. h)
description: Legt die aktuelle Rahmengröße für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das Pager- \_ setborder-Makro verwenden.
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- Windows-Steuerelemente für PGM_SETBORDER Meldung
topic_type:
- apiref
api_name:
- PGM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a987246a56da213098ba8632044af97ae51462df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040504"
---
# <a name="pgm_setborder-message"></a><span data-ttu-id="b33d9-105">PGM- \_ setborder-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b33d9-105">PGM\_SETBORDER message</span></span>

<span data-ttu-id="b33d9-106">Legt die aktuelle Rahmengröße für das Pager-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="b33d9-106">Sets the current border size for the pager control.</span></span> <span data-ttu-id="b33d9-107">Sie können diese Nachricht explizit senden oder das [**Pager- \_ setborder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="b33d9-107">You can send this message explicitly or use the [**Pager\_SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b33d9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b33d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b33d9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b33d9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b33d9-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="b33d9-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b33d9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b33d9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b33d9-112">Neue Größe des Rahmens in Pixel.</span><span class="sxs-lookup"><span data-stu-id="b33d9-112">New size of the border, in pixels.</span></span> <span data-ttu-id="b33d9-113">Dieser Wert darf nicht größer als die Schaltfläche "Pager" oder kleiner als 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="b33d9-113">This value should not be larger than the pager button or less than zero.</span></span> <span data-ttu-id="b33d9-114">Wenn *LPARAM* zu groß ist, wird der Rahmen mit der gleichen Größe wie die Schaltfläche gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b33d9-114">If *lParam* is too large, the border will be drawn the same size as the button.</span></span> <span data-ttu-id="b33d9-115">Wenn *LPARAM* negativ ist, wird die Rahmengröße auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b33d9-115">If *lParam* is negative, the border size will be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b33d9-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b33d9-116">Return value</span></span>

<span data-ttu-id="b33d9-117">Gibt einen int-Wert zurück, der die vorherige Rahmengröße in Pixel enthält.</span><span class="sxs-lookup"><span data-stu-id="b33d9-117">Returns an INT value that contains the previous border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="b33d9-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b33d9-118">Requirements</span></span>



| <span data-ttu-id="b33d9-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b33d9-119">Requirement</span></span> | <span data-ttu-id="b33d9-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b33d9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b33d9-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b33d9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b33d9-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b33d9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b33d9-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b33d9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b33d9-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b33d9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b33d9-125">Header</span><span class="sxs-lookup"><span data-stu-id="b33d9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b33d9-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b33d9-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





