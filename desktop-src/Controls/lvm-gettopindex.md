---
title: LVM_GETTOPINDEX Meldung (kommstrg. h)
description: Ruft den Index des obersten sichtbaren Elements ab, wenn es sich in der Liste oder in der Berichtsansicht handelt. Sie können diese Nachricht explizit oder mit dem ListView \_ gettopindex-Makro senden.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- Windows-Steuerelemente für LVM_GETTOPINDEX Meldung
topic_type:
- apiref
api_name:
- LVM_GETTOPINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1cb080588d1825fcbd9e6c5e7b1b573fd7ad2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340360"
---
# <a name="lvm_gettopindex-message"></a><span data-ttu-id="d2c2f-105">LVM \_ gettopindex-Meldung</span><span class="sxs-lookup"><span data-stu-id="d2c2f-105">LVM\_GETTOPINDEX message</span></span>

<span data-ttu-id="d2c2f-106">Ruft den Index des obersten sichtbaren Elements ab, wenn es sich in der Liste oder in der Berichtsansicht handelt.</span><span class="sxs-lookup"><span data-stu-id="d2c2f-106">Retrieves the index of the topmost visible item when in list or report view.</span></span> <span data-ttu-id="d2c2f-107">Sie können diese Nachricht explizit oder mit dem [**ListView \_ gettopindex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="d2c2f-107">You can send this message explicitly or by using the [**ListView\_GetTopIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2c2f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2c2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2c2f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2c2f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d2c2f-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d2c2f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d2c2f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2c2f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d2c2f-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d2c2f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2c2f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2c2f-113">Return value</span></span>

<span data-ttu-id="d2c2f-114">Gibt den Index des Elements zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="d2c2f-114">Returns the index of the item if successful.</span></span> <span data-ttu-id="d2c2f-115">Gibt 0 (null) zurück, wenn das Listenansicht-Steuerelement in der Symbol Ansicht oder in der kleinen Symbol Ansicht angezeigt wird, oder wenn sich das Listenansicht-Steuerelement in der Detailansicht befindet</span><span class="sxs-lookup"><span data-stu-id="d2c2f-115">Returns zero if the list-view control is in icon or small icon view, or if the list-view control is in details view with groups enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2c2f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2c2f-116">Requirements</span></span>



| <span data-ttu-id="d2c2f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2c2f-117">Requirement</span></span> | <span data-ttu-id="d2c2f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d2c2f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c2f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2c2f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d2c2f-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2c2f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2c2f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2c2f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d2c2f-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2c2f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2c2f-123">Header</span><span class="sxs-lookup"><span data-stu-id="d2c2f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2c2f-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2c2f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





