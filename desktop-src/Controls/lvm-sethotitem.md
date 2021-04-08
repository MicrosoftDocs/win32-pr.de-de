---
title: LVM_SETHOTITEM Meldung (kommstrg. h)
description: Legt das heiße Element für ein Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit senden oder das ListView-Makro "*" verwenden \_ .
ms.assetid: 0aa2b15d-4983-4234-9863-f1fdee09f913
keywords:
- Windows-Steuerelemente für LVM_SETHOTITEM Meldung
topic_type:
- apiref
api_name:
- LVM_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c17bc67c530581b79a87030b31b655f856dd0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739944"
---
# <a name="lvm_sethotitem-message"></a><span data-ttu-id="a9dbf-105">LVM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="a9dbf-105">LVM\_SETHOTITEM message</span></span>

<span data-ttu-id="a9dbf-106">Legt das heiße Element für ein Listenansicht-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="a9dbf-106">Sets the hot item for a list-view control.</span></span> <span data-ttu-id="a9dbf-107">Sie können diese Nachricht explizit senden oder das [**ListView- \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) Makro "\*" verwenden.</span><span class="sxs-lookup"><span data-stu-id="a9dbf-107">You can send this message explicitly or use the [**ListView\_SetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a9dbf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9dbf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9dbf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9dbf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9dbf-110">NULL basierter Index des Elements, das als heißes Element festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9dbf-110">Zero-based index of the item to be set as the hot item.</span></span>

</dd> <dt>

<span data-ttu-id="a9dbf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9dbf-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a9dbf-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a9dbf-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9dbf-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9dbf-113">Return value</span></span>

<span data-ttu-id="a9dbf-114">Gibt den Index des Elements zurück, das zuvor heiß war.</span><span class="sxs-lookup"><span data-stu-id="a9dbf-114">Returns the index of the item that was previously hot.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9dbf-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9dbf-115">Requirements</span></span>



| <span data-ttu-id="a9dbf-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9dbf-116">Requirement</span></span> | <span data-ttu-id="a9dbf-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a9dbf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9dbf-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9dbf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a9dbf-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9dbf-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a9dbf-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9dbf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a9dbf-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9dbf-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a9dbf-122">Header</span><span class="sxs-lookup"><span data-stu-id="a9dbf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9dbf-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9dbf-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





