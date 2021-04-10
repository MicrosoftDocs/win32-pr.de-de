---
title: LVM_SETITEMSTATE Meldung (kommstrg. h)
description: Ändert den Zustand eines Elements in einem Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des ListView-Objekts "" vom Typ "ListView" senden \_ .
ms.assetid: aecd14dd-cfd0-4c7c-bddc-f65022de68c9
keywords:
- Windows-Steuerelemente für LVM_SETITEMSTATE Meldung
topic_type:
- apiref
api_name:
- LVM_SETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2120d6d1d2cd3044368ebb343cdf0fe240d805c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103923"
---
# <a name="lvm_setitemstate-message"></a><span data-ttu-id="88a9e-105">LVM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="88a9e-105">LVM\_SETITEMSTATE message</span></span>

<span data-ttu-id="88a9e-106">Ändert den Zustand eines Elements in einem Listenansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="88a9e-106">Changes the state of an item in a list-view control.</span></span> <span data-ttu-id="88a9e-107">Sie können diese Nachricht explizit oder mithilfe des ListView-Objekts "" vom Typ " [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) " senden.</span><span class="sxs-lookup"><span data-stu-id="88a9e-107">You can send this message explicitly or by using the [**ListView\_SetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="88a9e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="88a9e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88a9e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="88a9e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88a9e-110">Der Index des Listen Ansichts Elements.</span><span class="sxs-lookup"><span data-stu-id="88a9e-110">Index of the list-view item.</span></span> <span data-ttu-id="88a9e-111">Wenn dieser Parameter-1 ist, wird die Zustandsänderung auf alle Elemente angewendet.</span><span class="sxs-lookup"><span data-stu-id="88a9e-111">If this parameter is -1, then the state change is applied to all items.</span></span>

</dd> <dt>

<span data-ttu-id="88a9e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="88a9e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88a9e-113">Zeiger auf eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="88a9e-113">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="88a9e-114">Der **statemask** -Member gibt an, welche Zustands Bits geändert werden sollen, und das **State** -Element enthält die neuen Werte für diese Bits.</span><span class="sxs-lookup"><span data-stu-id="88a9e-114">The **stateMask** member specifies which state bits to change, and the **state** member contains the new values for those bits.</span></span> <span data-ttu-id="88a9e-115">Die anderen Elemente werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="88a9e-115">The other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88a9e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88a9e-116">Return value</span></span>

<span data-ttu-id="88a9e-117">Wenn Sie diese Meldung explizit senden, wird **true** zurückgegeben, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="88a9e-117">If you send this message explicitly, it returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="88a9e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88a9e-118">Remarks</span></span>

<span data-ttu-id="88a9e-119">Der Zustandswert eines Elements enthält einen Satz von Bitflags, die den Zustand des Elements angeben.</span><span class="sxs-lookup"><span data-stu-id="88a9e-119">An item's state value includes a set of bit flags that indicate the item's state.</span></span> <span data-ttu-id="88a9e-120">Der Statuswert kann auch Bildlisten Indizes enthalten, die das Zustands Bild des Elements und das Überlagerungs Bild angeben.</span><span class="sxs-lookup"><span data-stu-id="88a9e-120">The state value can also include image list indexes that indicate the item's state image and overlay image.</span></span>

## <a name="requirements"></a><span data-ttu-id="88a9e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88a9e-121">Requirements</span></span>



| <span data-ttu-id="88a9e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88a9e-122">Requirement</span></span> | <span data-ttu-id="88a9e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="88a9e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88a9e-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88a9e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="88a9e-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88a9e-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="88a9e-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88a9e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="88a9e-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88a9e-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="88a9e-128">Header</span><span class="sxs-lookup"><span data-stu-id="88a9e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="88a9e-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="88a9e-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





