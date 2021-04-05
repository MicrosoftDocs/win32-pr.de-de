---
title: TVM_SHOWINFOTIP Meldung (kommstrg. h)
description: Zeigt den Infotipp für ein angegebenes Element in einem Strukturansicht-Steuerelement an. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ ShowInfoTip-Makros senden.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- Windows-Steuerelemente für TVM_SHOWINFOTIP Meldung
topic_type:
- apiref
api_name:
- TVM_SHOWINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76f147253800469a800677a242ff0ab0ccdbdfa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859289"
---
# <a name="tvm_showinfotip-message"></a><span data-ttu-id="94db1-105">TVM \_ ShowInfoTip-Meldung</span><span class="sxs-lookup"><span data-stu-id="94db1-105">TVM\_SHOWINFOTIP message</span></span>

<span data-ttu-id="94db1-106">Zeigt den Infotipp für ein angegebenes Element in einem Strukturansicht-Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="94db1-106">Shows the infotip for a specified item in a tree-view control.</span></span> <span data-ttu-id="94db1-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ ShowInfoTip**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="94db1-107">You can send this message explicitly or by using the [**TreeView\_ShowInfoTip**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) macro..</span></span>

## <a name="parameters"></a><span data-ttu-id="94db1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="94db1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94db1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="94db1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="94db1-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="94db1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="94db1-111">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94db1-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94db1-112">Handle für das Element.</span><span class="sxs-lookup"><span data-stu-id="94db1-112">Handle to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94db1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94db1-113">Return value</span></span>

<span data-ttu-id="94db1-114">Gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="94db1-114">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="94db1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94db1-115">Remarks</span></span>

<span data-ttu-id="94db1-116">Von den meisten Anwendungen wird diese Nachricht nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="94db1-116">Most applications do not use this message.</span></span> <span data-ttu-id="94db1-117">Infotips werden automatisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="94db1-117">Infotips are shown automatically.</span></span> <span data-ttu-id="94db1-118">Weitere Informationen finden Sie unter Verwenden von Strukturansicht-Infotipps in der Übersicht [über Tree-View](tree-view-controls.md) -Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="94db1-118">For more information, see Using Tree-view Infotips in the [About Tree-View Controls](tree-view-controls.md) overview.</span></span>

## <a name="requirements"></a><span data-ttu-id="94db1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94db1-119">Requirements</span></span>



| <span data-ttu-id="94db1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94db1-120">Requirement</span></span> | <span data-ttu-id="94db1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="94db1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94db1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94db1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="94db1-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94db1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="94db1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94db1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="94db1-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94db1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="94db1-126">Header</span><span class="sxs-lookup"><span data-stu-id="94db1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="94db1-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="94db1-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





