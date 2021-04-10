---
title: LVM_SETITEMPOSITION32 Meldung (kommstrg. h)
description: Verschiebt ein Element an eine angegebene Position in einem Listenansicht-Steuerelement (muss sich in der Symbol Ansicht oder in der kleinen Symbol Ansicht befinden).
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- Windows-Steuerelemente für LVM_SETITEMPOSITION32 Meldung
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 450963e4adf5ea2b0644f8d155145ba577efab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040666"
---
# <a name="lvm_setitemposition32-message"></a><span data-ttu-id="10d1b-104">LVM \_ SETITEMPOSITION32 Meldung</span><span class="sxs-lookup"><span data-stu-id="10d1b-104">LVM\_SETITEMPOSITION32 message</span></span>

<span data-ttu-id="10d1b-105">Verschiebt ein Element an eine angegebene Position in einem Listenansicht-Steuerelement (muss sich in der Symbol Ansicht oder in der kleinen Symbol Ansicht befinden).</span><span class="sxs-lookup"><span data-stu-id="10d1b-105">Moves an item to a specified position in a list-view control (must be in icon or small icon view).</span></span> <span data-ttu-id="10d1b-106">Diese Meldung unterscheidet sich von der Nachricht [**LVM \_**](lvm-setitemposition.md) -Nachricht, dass Sie 32-Bit-Koordinaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="10d1b-106">This message differs from the [**LVM\_SETITEMPOSITION**](lvm-setitemposition.md) message in that it uses 32-bit coordinates.</span></span> <span data-ttu-id="10d1b-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ SetItemPosition32**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="10d1b-107">You can send this message explicitly or by using the [**ListView\_SetItemPosition32**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="10d1b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="10d1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10d1b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10d1b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10d1b-110">Der Index des Listen Ansichts Elements, für das die Position festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="10d1b-110">Index of the list-view item for which to set the position.</span></span>

</dd> <dt>

<span data-ttu-id="10d1b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10d1b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10d1b-112">Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur, die die neue Position des Elements in Listen Ansichts Koordinaten enthält.</span><span class="sxs-lookup"><span data-stu-id="10d1b-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the new position of the item, in list-view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10d1b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10d1b-113">Return value</span></span>

<span data-ttu-id="10d1b-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="10d1b-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="10d1b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10d1b-115">Requirements</span></span>



| <span data-ttu-id="10d1b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10d1b-116">Requirement</span></span> | <span data-ttu-id="10d1b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="10d1b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10d1b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10d1b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="10d1b-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10d1b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10d1b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10d1b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="10d1b-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10d1b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10d1b-122">Header</span><span class="sxs-lookup"><span data-stu-id="10d1b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="10d1b-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="10d1b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

