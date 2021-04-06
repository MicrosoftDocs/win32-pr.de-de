---
title: TB_SETHOTITEM2 Meldung (kommstrg. h)
description: Legt das heiße Element in einer Symbolleiste fest.
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- Windows-Steuerelemente für TB_SETHOTITEM2 Meldung
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
ms.openlocfilehash: 7027920e4363b46fcc0b6d9b0d87129e01843318
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742649"
---
# <a name="tb_sethotitem2-message"></a><span data-ttu-id="b0b1d-104">TB \_ SETHOTITEM2 Meldung</span><span class="sxs-lookup"><span data-stu-id="b0b1d-104">TB\_SETHOTITEM2 message</span></span>

<span data-ttu-id="b0b1d-105">Legt das heiße Element in einer Symbolleiste fest.</span><span class="sxs-lookup"><span data-stu-id="b0b1d-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0b1d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0b1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0b1d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0b1d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0b1d-108">Der Index des Elements, das heiß gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="b0b1d-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="b0b1d-109">Wenn dieser Wert-1 ist, ist keines der Elemente heiß.</span><span class="sxs-lookup"><span data-stu-id="b0b1d-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="b0b1d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0b1d-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b0b1d-111">Eine Kombination von hicf \_ xxx-Flags.</span><span class="sxs-lookup"><span data-stu-id="b0b1d-111">A combination of HICF\_xxx flags.</span></span> <span data-ttu-id="b0b1d-112">Weitere Informationen finden Sie unter <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**nmtbhutitem**</a>.</span><span class="sxs-lookup"><span data-stu-id="b0b1d-112">See <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0b1d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0b1d-113">Return value</span></span>

<span data-ttu-id="b0b1d-114">Gibt den Index des vorherigen aktiven Elements oder-1 zurück, wenn kein heißes Element vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="b0b1d-114">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0b1d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0b1d-115">Remarks</span></span>

<span data-ttu-id="b0b1d-116">Das Verhalten dieser Nachricht ist nicht für Symbolleisten definiert, die nicht den [**\_ flachen tbstyle**](toolbar-control-and-button-styles.md) -Stil aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b0b1d-116">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0b1d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0b1d-117">Requirements</span></span>



| <span data-ttu-id="b0b1d-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0b1d-118">Requirement</span></span> | <span data-ttu-id="b0b1d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b0b1d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b1d-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0b1d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b0b1d-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0b1d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0b1d-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0b1d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b0b1d-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0b1d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0b1d-124">Header</span><span class="sxs-lookup"><span data-stu-id="b0b1d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0b1d-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0b1d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





