---
title: TVM_ENSUREVISIBLE Meldung (kommstrg. h)
description: Stellt sicher, dass ein Struktur Ansichts Element sichtbar ist, erweitert das übergeordnete Element und führt ggf. einen Bildlauf im Strukturansicht-Steuerelement aus. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ EnsureVisible-Makros senden.
ms.assetid: 7053438a-f9ca-4c4c-9da6-46b99fe1e4f8
keywords:
- Windows-Steuerelemente für TVM_ENSUREVISIBLE Meldung
topic_type:
- apiref
api_name:
- TVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06100ee33106736076608aa216d2aebc03b76ebe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949691"
---
# <a name="tvm_ensurevisible-message"></a><span data-ttu-id="c75d9-105">TVM \_ EnsureVisible-Meldung</span><span class="sxs-lookup"><span data-stu-id="c75d9-105">TVM\_ENSUREVISIBLE message</span></span>

<span data-ttu-id="c75d9-106">Stellt sicher, dass ein Struktur Ansichts Element sichtbar ist, erweitert das übergeordnete Element und führt ggf. einen Bildlauf im Strukturansicht-Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="c75d9-106">Ensures that a tree-view item is visible, expanding the parent item or scrolling the tree-view control, if necessary.</span></span> <span data-ttu-id="c75d9-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="c75d9-107">You can send this message explicitly or by using the [**TreeView\_EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c75d9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c75d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c75d9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c75d9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c75d9-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c75d9-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c75d9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c75d9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c75d9-112">Handle für das Element.</span><span class="sxs-lookup"><span data-stu-id="c75d9-112">Handle to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c75d9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c75d9-113">Return value</span></span>

<span data-ttu-id="c75d9-114">Gibt einen Wert ungleich 0 (null) zurück, wenn das System die Elemente im Strukturansicht-Steuerelement aufscrollt und keine Elemente erweitert wurden.</span><span class="sxs-lookup"><span data-stu-id="c75d9-114">Returns nonzero if the system scrolled the items in the tree-view control and no items were expanded.</span></span> <span data-ttu-id="c75d9-115">Andernfalls gibt die Meldung 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c75d9-115">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c75d9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c75d9-116">Remarks</span></span>

<span data-ttu-id="c75d9-117">Wenn die TVM- \_ Meldung "ensureVisible" das übergeordnete Element erweitert, empfängt das übergeordnete Fenster die [TVN \_ itemexpandeing](tvn-itemexpanding.md) -und [TVN \_ itemexpanded](tvn-itemexpanded.md) -Benachrichtigungs Codes.</span><span class="sxs-lookup"><span data-stu-id="c75d9-117">If the TVM\_ENSUREVISIBLE message expands the parent item, the parent window receives the [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="c75d9-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c75d9-118">Requirements</span></span>



| <span data-ttu-id="c75d9-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c75d9-119">Requirement</span></span> | <span data-ttu-id="c75d9-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c75d9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c75d9-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c75d9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c75d9-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c75d9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c75d9-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c75d9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c75d9-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c75d9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c75d9-125">Header</span><span class="sxs-lookup"><span data-stu-id="c75d9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c75d9-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c75d9-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





