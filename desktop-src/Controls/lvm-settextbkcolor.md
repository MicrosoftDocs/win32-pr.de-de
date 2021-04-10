---
title: LVM_SETTEXTBKCOLOR Meldung (kommstrg. h)
description: Legt die Hintergrundfarbe von Text in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des ListView \_ settextbkcolor-Makros senden.
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- Windows-Steuerelemente für LVM_SETTEXTBKCOLOR Meldung
topic_type:
- apiref
api_name:
- LVM_SETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2247dfd04d90c2b9eacadcb1c38608f519540fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040440"
---
# <a name="lvm_settextbkcolor-message"></a><span data-ttu-id="d75ba-105">LVM- \_ settextbkcolor-Meldung</span><span class="sxs-lookup"><span data-stu-id="d75ba-105">LVM\_SETTEXTBKCOLOR message</span></span>

<span data-ttu-id="d75ba-106">Legt die Hintergrundfarbe von Text in einem Listenansicht-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="d75ba-106">Sets the background color of text in a list-view control.</span></span> <span data-ttu-id="d75ba-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ settextbkcolor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="d75ba-107">You can send this message explicitly or by using the [**ListView\_SetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d75ba-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d75ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d75ba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d75ba-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d75ba-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d75ba-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d75ba-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d75ba-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d75ba-112">Neue Text Hintergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="d75ba-112">New text background color.</span></span> <span data-ttu-id="d75ba-113">Dies kann CLR none sein, \_ Wenn keine Hintergrundfarbe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d75ba-113">This can be CLR\_NONE for no background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d75ba-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d75ba-114">Return value</span></span>

<span data-ttu-id="d75ba-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="d75ba-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d75ba-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d75ba-116">Requirements</span></span>



| <span data-ttu-id="d75ba-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d75ba-117">Requirement</span></span> | <span data-ttu-id="d75ba-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d75ba-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d75ba-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d75ba-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d75ba-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d75ba-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d75ba-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d75ba-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d75ba-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d75ba-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d75ba-123">Header</span><span class="sxs-lookup"><span data-stu-id="d75ba-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d75ba-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d75ba-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





