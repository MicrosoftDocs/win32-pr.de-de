---
title: LVM_GETCOLUMN Meldung (kommstrg. h)
description: Ruft die Attribute der Spalte eines Listenansicht-Steuer Elements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetColumn-Makros senden.
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- Windows-Steuerelemente für LVM_GETCOLUMN Meldung
topic_type:
- apiref
api_name:
- LVM_GETCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eebf57138d27c31c5594f271e5d36a052b81673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475174"
---
# <a name="lvm_getcolumn-message"></a><span data-ttu-id="5c101-105">LVM \_ GetColumn-Nachricht</span><span class="sxs-lookup"><span data-stu-id="5c101-105">LVM\_GETCOLUMN message</span></span>

<span data-ttu-id="5c101-106">Ruft die Attribute der Spalte eines Listenansicht-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="5c101-106">Gets the attributes of a list-view control's column.</span></span> <span data-ttu-id="5c101-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="5c101-107">You can send this message explicitly or by using the [**ListView\_GetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5c101-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c101-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c101-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c101-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c101-110">Der Index der Spalte.</span><span class="sxs-lookup"><span data-stu-id="5c101-110">The index of the column.</span></span>

</dd> <dt>

<span data-ttu-id="5c101-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c101-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c101-112">Ein Zeiger auf eine [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) -Struktur, die die Informationen angibt, die abgerufen werden sollen, und die Informationen über die Spalte empfängt.</span><span class="sxs-lookup"><span data-stu-id="5c101-112">A pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that specifies the information to retrieve and receives information about the column.</span></span> <span data-ttu-id="5c101-113">Der **Mask** -Member gibt an, welche Spalten Attribute abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5c101-113">The **mask** member specifies which column attributes to retrieve.</span></span> <span data-ttu-id="5c101-114">Wenn das **Mask** -Element den "lvcf" \_ -Textwert angibt, muss der **pszText** -Member die Adresse des Puffers enthalten, der den Element Text empfängt, und der **cchtextmax** -Member muss die Größe des Puffers angeben.</span><span class="sxs-lookup"><span data-stu-id="5c101-114">If the **mask** member specifies the LVCF\_TEXT value, the **pszText** member must contain the address of the buffer that receives the item text and the **cchTextMax** member must specify the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c101-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c101-115">Return value</span></span>

<span data-ttu-id="5c101-116">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="5c101-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c101-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c101-117">Requirements</span></span>



| <span data-ttu-id="5c101-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c101-118">Requirement</span></span> | <span data-ttu-id="5c101-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5c101-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c101-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c101-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5c101-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c101-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5c101-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c101-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5c101-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c101-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5c101-124">Header</span><span class="sxs-lookup"><span data-stu-id="5c101-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c101-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c101-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





