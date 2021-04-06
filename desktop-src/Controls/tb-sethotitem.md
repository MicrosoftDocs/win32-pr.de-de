---
title: TB_SETHOTITEM Meldung (kommstrg. h)
description: Legt das heiße Element in einer Symbolleiste fest.
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- Windows-Steuerelemente für TB_SETHOTITEM Meldung
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
ms.openlocfilehash: c477a445cb6aae78dd5d31e8d23b8ec3be8c61ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859098"
---
# <a name="tb_sethotitem-message"></a><span data-ttu-id="0e734-104">TB-Nachricht "nach \_ richten"</span><span class="sxs-lookup"><span data-stu-id="0e734-104">TB\_SETHOTITEM message</span></span>

<span data-ttu-id="0e734-105">Legt das heiße Element in einer Symbolleiste fest.</span><span class="sxs-lookup"><span data-stu-id="0e734-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e734-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e734-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e734-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e734-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e734-108">Der Index des Elements, das heiß gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="0e734-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="0e734-109">Wenn dieser Wert-1 ist, ist keines der Elemente heiß.</span><span class="sxs-lookup"><span data-stu-id="0e734-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="0e734-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e734-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0e734-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="0e734-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e734-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e734-112">Return value</span></span>

<span data-ttu-id="0e734-113">Gibt den Index des vorherigen aktiven Elements oder-1 zurück, wenn kein heißes Element vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="0e734-113">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e734-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e734-114">Remarks</span></span>

<span data-ttu-id="0e734-115">Das Verhalten dieser Nachricht ist nicht für Symbolleisten definiert, die nicht den [**\_ flachen tbstyle**](toolbar-control-and-button-styles.md) -Stil aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0e734-115">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e734-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e734-116">Requirements</span></span>



| <span data-ttu-id="0e734-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e734-117">Requirement</span></span> | <span data-ttu-id="0e734-118">Wert</span><span class="sxs-lookup"><span data-stu-id="0e734-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e734-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0e734-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0e734-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e734-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e734-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0e734-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0e734-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e734-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e734-123">Header</span><span class="sxs-lookup"><span data-stu-id="0e734-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e734-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e734-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





